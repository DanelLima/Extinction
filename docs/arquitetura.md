# Arquitetura

[Voltar ao início](../README.md)

## Visão geral

O sistema tem três processos: o app mobile, a API e o serviço de identificação de espécies. O app fala apenas com a API, que orquestra o banco de dados, a IA, os arquivos e as notificações. Docker Compose sobe a API, o MySQL e o serviço de identificação juntos.

```mermaid
flowchart LR
    App["App mobile<br/>React Native + Expo"] -->|"REST e WebSocket"| API["API<br/>Java 17 + Spring Boot"]
    API -->|"JDBC"| DB[("MySQL 8.4")]
    API -->|"HTTP"| IA["Serviço de identificação<br/>Python + FastAPI + BioCLIP 2"]
    API -->|"Expo Push API"| Push["Notificações push"]
    App -->|"Leaflet"| Mapa["OpenStreetMap"]
```

## Camadas do backend

Cada pacote Java tem uma responsabilidade definida, e toda requisição autenticada passa antes pelo filtro de segurança.

![Camadas do backend](images/arquitetura/camadas.png)

## Decisões principais

### Identificação no servidor com BioCLIP 2

A primeira abordagem foi treinar um classificador próprio em TensorFlow. Ela exigia muitas imagens rotuladas, escassas para espécies brasileiras. A equipe migrou para o BioCLIP 2, um modelo aberto e pré-treinado, executado em um serviço Python separado.

Com isso, o resultado é o mesmo em qualquer aparelho, o modelo pode ser atualizado sem publicar o app e a inferência roda em um pool assíncrono próprio, sem travar as demais requisições. A API devolve até 5 candidatas com confiança mínima de 20%, e o usuário sempre confirma a espécie.

![Classificador tradicional comparado ao BioCLIP 2](images/arquitetura/bioclip.png)

### Modo offline com padrão Outbox

Trilhas e áreas rurais costumam ter pouco sinal. O avistamento é salvo no aparelho com um UUID e enviado em ordem quando a conexão volta, com novas tentativas em caso de falha. O UUID torna o envio idempotente, então reenvios não criam duplicatas. A espécie é identificada na sincronização, e o usuário confirma antes de publicar.

![Sincronização de um avistamento registrado sem conexão](images/arquitetura/offline.png)

### Autenticação stateless

A API usa JWT em todas as requisições autenticadas, senhas com BCrypt e controle de acesso por perfil. O login com Google e Apple é validado no backend por OIDC, que então emite o JWT interno.

![Requisição autenticada passando pelo filtro JWT](images/arquitetura/filtro-jwt.png)

![Login social](images/arquitetura/login-social.png)

### Tempo real com WebSocket

Chat, novos avistamentos e notificações usam WebSocket. O token é validado no handshake, então uma conexão sem autenticação é recusada antes de abrir.

![Sequência do envio de uma mensagem no chat](images/arquitetura/chat.png)

![Do evento de domínio ao celular](images/arquitetura/notificacoes.png)

## Fluxo de publicação

![Sequência de publicação de um avistamento](images/arquitetura/publicacao.png)

## Modelo de dados

![Modelo de dados: tabelas do núcleo](images/arquitetura/dados-nucleo.png)

Tabelas adicionadas nos MVPs 0.2 e 1.0:

![Modelo de dados: tabelas adicionadas](images/arquitetura/dados-mvps.png)

## Próximas evoluções

- Migrações versionadas de banco de dados.
- Limite de requisições nos endpoints públicos.
- Integração automática com bases oficiais de status de conservação.
