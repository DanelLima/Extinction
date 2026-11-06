# Produto e requisitos

[Voltar ao início](../README.md)

## Visão

O Extinction é voltado a trilheiros, fotógrafos amadores, estudantes, pesquisadores e biólogos. O diferencial em relação a ferramentas de pesquisa como o iNaturalist é o formato: posts informativos, geolocalizados e sociais, que aproximam o público geral da conservação.

| Parte interessada | Papel |
|---|---|
| Cidadãos | Alimentam a base com fotos e avistamentos |
| Pesquisadores e biólogos | Validam as identificações e usam os dados |
| Equipe de desenvolvimento | Cuida da qualidade do produto e das entregas |
| IBAMA, ICMBio e IUCN | Publicam as listas oficiais usadas como referência, sem parceria formal até aqui |

## Escopo

O Documento de Requisitos v2.1 reúne 24 requisitos funcionais, 13 não funcionais, 25 regras de negócio e 10 histórias de usuário, com cenários de aceitação em Dado, Quando e Então.

### Backlog priorizado com MoSCoW

| Prioridade | História | Pontos |
|---|---|---:|
| Must | HU01 Cadastro | 8 |
| Must | HU02 Login | 5 |
| Must | HU03 Recuperação de senha | 3 |
| Must | HU04 Postagem com foto e IA | 13 |
| Must | HU05 Mapa | 8 |
| Must | HU08 Alterar perfil e LGPD | 11 |
| Should | HU06 Feed | 5 |
| Should | HU07 Enciclopédia | 8 |
| Should | HU09 Mensagens | 8 |
| Should | HU10 Seguir | 5 |
|  | **Total** | **74** |

### Regras de negócio em destaque

- A idade mínima para criar conta é de 13 anos, em conformidade com a LGPD.
- A senha tem pelo menos 8 caracteres, com letras e números, e é guardada com BCrypt.
- O login é bloqueado por 15 minutos na sexta tentativa errada.
- O selo de conservação usa apenas as categorias oficiais da IUCN e do MMA.
- Coordenadas fora do Brasil ou em alto-mar são rejeitadas.
- Excluir a conta anonimiza os dados pessoais e preserva os avistamentos como "Usuário Removido".

### Metas não funcionais

| Meta | Valor |
|---|---|
| Resposta da IA | Até 5 s |
| Usuários simultâneos no teste de carga | 100 |
| Registros guardados offline | 100 |
| Consumo de bateria com GPS e câmera | Até 30% por hora |
| Plataformas | Android 10+ e iOS 15+ |
| Segurança | BCrypt, JWT e TLS 1.3 |
| Idiomas da API | Português e inglês |

## Planejamento

O projeto foi dividido em três MVPs, cada um com duas iterações de uma semana.

| Entrega | Data | Objetivo |
|---|---|---|
| MVP 0.1 | 10/10/2026 | Conta segura e avistamento identificado por IA |
| MVP 0.2 | 24/10/2026 | Uso em campo sem conexão, mapa e gestão de conta |
| MVP 1.0 | 07/11/2026 | Comunidade, curadoria, login social e regressão completa |

### Definition of Done

Uma entrega só conta como pronta com testes aprovados e evidência, revisão por outro integrante, teste manual de ponta a ponta, ambiente Docker subindo do zero, demonstração gravada, nenhum defeito crítico ou alto em aberto e documentos atualizados.

### Riscos

| Risco | Severidade | Mitigação |
|---|---|---|
| Complexidade do modo offline | Alta | Iteração dedicada e testes de idempotência escritos antes |
| Login Apple exige programa pago | Média | Preparação antecipada e demonstração com Google, se necessário |
| Latência do BioCLIP em CPU | Média | Aquecimento do modelo, timeout e redimensionamento de imagens |
| Equipe de 4 pessoas | Média | Prioridades concentradas nos primeiros MVPs e escopo congelado em 01/11 |
| SMTP da recuperação de senha | Baixa | Conta de teste configurada desde a primeira iteração |
| Divergências entre documentos | Baixa | Visão, Requisitos e Arquitetura alinhados na versão 2.1 |

## Documentos

- [Documento de Visão v2.1 (PDF)](documentos/Documento-de-Visao.pdf)
- [Documento de Requisitos v2.1 (PDF)](documentos/Documento-de-Requisitos.pdf)
- [Visão inicial, de março de 2026](historico/visao-inicial-2026-03.md), mantida como registro histórico do escopo da época
