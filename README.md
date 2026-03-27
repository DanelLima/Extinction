# EXTINCTION

## 1. INTRODUÇÃO

O presente documento tem por finalidade fornecer as informações de como o projeto será desenvolvido, seus objetivos e implicações para aplicá-lo. O projeto Extinction é composto por André Ribamar Martins Da Silva, Alysson Kauã Rocha De Carvalho, Guilherme Alves Rocha, Cayky Emílio Vieira Neves, Daniel Souza De Lima, Flávio Daniel Rocha Santos. 

No contexto do desenvolvimento urbano brasileiro, a Mata Atlântica passou por perdas significativas e, em muitos casos, irrecuperáveis em sua fauna e flora. Estima-se que cerca de 71,6% de sua vegetação nativa tenha sido desmatada. Nesse bioma encontram-se espécies emblemáticas, como o Mico-leão-dourado e as Araucárias, que dependem diretamente da preservação desses ambientes para sua sobrevivência.  

Ao considerar também o Cerrado brasileiro, observa-se que espécies como o Lobo-guará se encontram ameaçadas de extinção. Caso as ameaças atuais, como a expansão urbana, a perda de habitat e a ação humana, continuem, existe a possibilidade de que algumas dessas espécies desapareçam nas próximas décadas. Assim, torna-se necessário ampliar a visibilidade sobre as espécies ameaçadas. Com a disseminação de informações e maior conscientização da população, é possível aumentar o engajamento social na proteção da biodiversidade.  

Nesse contexto, surge a Extinction, uma nova iniciativa desenvolvida com o propósito de auxiliar na proteção de espécies ameaçadas. É importante destacar que nem todos os fatores relacionados ao desaparecimento dessas espécies podem ser abordados, como processos naturais de seleção. Ainda assim, a plataforma pretende atuar como um importante meio de divulgação e conscientização ambiental.  

Portanto, sendo um software multicliente e sem fins lucrativos, a Extinction busca contribuir para a educação ambiental e para a promoção de ações que incentivem a preservação das espécies ameaçadas e de seus habitats naturais. 

## 2. CONTEXTO DE NEGÓCIO

O uso de tecnologias digitais para monitoramento ambiental e reconhecimento de espécies tem se expandido significativamente nos últimos anos. Avanços em áreas como visão computacional, aprendizado de máquina e análise de imagens têm possibilitado o desenvolvimento de sistemas capazes de identificar espécies animais e vegetais a partir de fotografias. Essas tecnologias vêm sendo aplicadas em iniciativas de pesquisa científica, conservação da biodiversidade e ciência-cidadã, ampliando o alcance das atividades de monitoramento ecológico e permitindo maior participação da sociedade na coleta de dados ambientais.
Entre as tecnologias utilizadas nesse domínio destaca-se o uso de frameworks de aprendizado de máquina, como o TensorFlow, que permite o treinamento de modelos de inteligência artificial voltados para tarefas de classificação e reconhecimento de padrões em imagens. A aplicação dessas ferramentas possibilita o desenvolvimento de sistemas capazes de reconhecer automaticamente determinadas espécies a partir de fotografias capturadas por dispositivos móveis, câmeras de monitoramento ou bancos de dados digitais.

Apesar dos avanços tecnológicos disponíveis, a implementação de soluções baseadas em inteligência artificial para reconhecimento de espécies ainda enfrenta desafios significativos no contexto brasileiro. Um dos principais problemas está relacionado à escassez de dados de campo estruturados e de alta qualidade para treinamento de modelos de aprendizado de máquina. Para que algoritmos de visão computacional funcionem de maneira eficiente, é necessário um grande volume de imagens rotuladas e representativas das espécies em diferentes condições ambientais, ângulos, idades e variações naturais.
No Brasil, especialmente em determinadas regiões, ainda existem lacunas importantes na disponibilidade de conjuntos de dados específicos para treinamento de modelos voltados ao reconhecimento da biodiversidade local. Muitas bases de dados disponíveis são voltadas para espécies de outras regiões do mundo ou apresentam quantidade limitada de registros para espécies brasileiras, o que dificulta a construção de modelos confiáveis para identificação automática. De acordo com relatórios de conservação ambiental, o Brasil possui uma das maiores biodiversidades do planeta, concentrando cerca de 15% a 20% das espécies conhecidas mundialmente, o que reforça a necessidade de ferramentas adequadas para monitoramento e identificação da fauna e flora.
Outro desafio relevante está na integração prática entre modelos de inteligência artificial e aplicações de software. Embora frameworks como o TensorFlow ofereçam recursos robustos para treinamento de redes neurais e classificação de imagens, sua incorporação em sistemas de uso cotidiano — como aplicações web ou móveis — pode apresentar complexidades técnicas. Entre essas dificuldades estão a otimização do desempenho do modelo, a redução do tamanho dos arquivos gerados, a adaptação para execução em dispositivos com recursos limitados e a garantia de respostas rápidas durante o processo de reconhecimento de imagens.
Além disso, o desenvolvimento de soluções nesse domínio frequentemente depende da utilização de bases de dados abertas e confiáveis sobre espécies ameaçadas. No Brasil, um dos principais conjuntos de informações disponíveis publicamente é a lista de espécies ameaçadas publicada pelo Ministério do Meio Ambiente. Esses dados incluem informações sobre o status de conservação das espécies, classificação de risco de extinção e distribuição geográfica aproximada. Entretanto, essas bases de dados frequentemente apresentam limitações relacionadas à atualização, padronização ou integração direta com ferramentas de aprendizado de máquina, exigindo processos adicionais de tratamento, organização e adaptação dos dados.
Nesse contexto, diferentes grupos de usuários são impactados por essas limitações. Entre os principais usuários e interessados nesse domínio estão:

•	pesquisadores e biólogos, que necessitam de dados confiáveis para estudos científicos e monitoramento de espécies;

•	órgãos ambientais e instituições governamentais, responsáveis pela elaboração de políticas públicas e programas de conservação;

•	organizações não governamentais voltadas à preservação ambiental, que utilizam dados para campanhas e projetos de conservação;

•	educadores e estudantes, que buscam informações sobre biodiversidade para fins educacionais;

•	cidadãos interessados em natureza e ciência-cidadã, que participam da coleta e registro de dados ambientais.
O mercado e o domínio de aplicação relacionados ao monitoramento da biodiversidade e reconhecimento de espécies têm crescido globalmente, impulsionados pelo aumento das preocupações ambientais, pela ampliação de projetos de ciência-cidadã e pela popularização de dispositivos móveis com câmeras de alta qualidade. Entretanto, ainda existem lacunas importantes relacionadas à disponibilidade de dados regionais, à padronização das informações e à acessibilidade das ferramentas tecnológicas para usuários não especializados.
No cenário internacional, já existem algumas soluções digitais voltadas à identificação de espécies e monitoramento da biodiversidade. Entre elas destacam-se plataformas como o iNaturalist e o Seek by iNaturalist, que utilizam inteligência artificial e colaboração da comunidade para identificar espécies a partir de imagens enviadas pelos usuários. Essas plataformas apresentam pontos fortes, como grande volume de dados colaborativos, comunidades ativas de especialistas e integração com bases científicas.
Entretanto, essas soluções também apresentam algumas limitações no contexto brasileiro. Entre elas estão a menor cobertura de determinadas espécies regionais, dificuldades relacionadas à identificação precisa em ambientes específicos e a limitação de informações detalhadas sobre espécies locais ameaçadas. Além disso, muitas dessas plataformas dependem fortemente da contribuição de comunidades científicas e voluntários para validação das observações, o que pode gerar atrasos ou inconsistências na classificação das espécies.
Dessa forma, observa-se que, embora existam tecnologias e plataformas voltadas ao reconhecimento de espécies e ao monitoramento da biodiversidade, ainda persistem desafios relacionados à disponibilidade de dados locais, à integração entre inteligência artificial e aplicações digitais e ao aproveitamento eficiente de bases de dados abertas sobre biodiversidade. Essas limitações evidenciam lacunas importantes no domínio de aplicação e indicam a necessidade de aprimoramento das ferramentas existentes para apoiar iniciativas de conservação ambiental, pesquisa científica e conscientização da sociedade sobre a preservação da biodiversidade.


## 3. POSICIONAMENTO

### 3.1 Declaração do problema
|||
|-----|-----|
|O problema de| espécies ameaçadas de extinção afetam a fauna brasileira, o equilíbrio em que a espécie está localizada e a possibilidade de nunca mais vermos certas espécies|
|afeta| o ecossistema natural do local, pois esse equilíbrio é muito frágil; se retirarmos uma parte para o local, acaba gerando uma superpopulação da espécie que precisava da outra para ser controlada|
|cujo impacto é|desequilíbrio no ambiente em que essas espécies estão.|
|uma solução de sucesso deveria| trazendo visibilidade aos animais, pessoas vão se importar mais com eles, ganhando visibilidade para que o governo também possa olhar mais para eles e cuidar melhor.<br>Informar localidade de algumas espécies que pessoas não sabem onde estão ou o que são.<br>Ajudar a preservar as vidas dessas espécies e fauna local, ao criar um pequeno movimento que irá ajudar.|

---

### 3.2 Declaração da visão do software
**Para**  
Pessoas no geral.

**Que**

1. Localizar espécies isoladas, que alguns não sabem que estão em extinção por falta de informação.  
2. Falta de informação sobre as espécies, pessoas podem às vezes matá-las por estarem perto de suas casas, se for um animal, por exemplo.

**O**  
Extinction.

**É um**  
Software-Web.

**Que**  
Preserva espécies, traz conhecimento sobre as mesmas, conscientizando as pessoas.

**Diferente de**  
Plataforma Salve.

**Nosso produto**  
Plataforma Salve não tem posts como forma de divulgação, tendo informação bruta sobre as espécies, como ficha técnica completa.

**Nosso funciona**  
A base de posts, com informações sobre a espécie do post e localidade.

---

## 4. DESCRIÇÃO DAS PARTES INTERESSADAS

| Nome | Descrição | Responsabilidades |
|-----|-----|-----|
| LifeSaver | Pessoas que gostam da natureza veem uma importância nela, não a tratam como nada. | • Terá identificação.<br>• garante que o sistema terá extras informações nos posts.<br>• garante que haverá localidade nos posts.<br>• Identificação para cada espécie.<br>• informação sobre cada espécie para entendimento.<br>• localização de cada espécie postada |


**5 REQUISITOS**

**5.1 REQUISITOS FUNCIONAIS**

**[RF001] Reconhecimento de Espécie via Machine Learning**
O sistema deve permitir que o usuário tire uma foto ou suba uma imagem para que a IA
identifique a espécie de fauna ou flora automaticamente.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF002] Mapeamento de Avistamento (GPS)**
O sistema deve capturar automaticamente as coordenadas geográficas (latitude e longitude)
no momento em que um usuário registrar um novo avistamento.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF003] Validação de Status de Extinção**
Após a identificação, o sistema deve consultar uma base de dados (API) para atribuir o selo
de conservação correto (Ex: "Em Perigo", "Vulnerável", "Extinta na Natureza").
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF004] Sincronização de Dados Offline**
O sistema deve permitir que o usuário registre avistamentos sem conexão com a internet e
realize o upload automático assim que detectar um sinal ativo.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF005] Feed de Interação Comunitária**
O sistema deve exibir uma linha do tempo com as descobertas de outros usuários, permitindo
interações como curtidas e comentários.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF006] Enciclopédia Pessoal (Catálogo)**
O sistema deve manter um histórico organizado (álbum) de todas as espécies que o usuário já
catalogou, funcionando como um "log de conquistas".
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF007] Ranking de Usuários (Gamificação)**
O sistema deve listar os usuários com maior número de avistamentos validados para
incentivar a participação na coleta de dados.
Prioridade: ◻ Essencial ◻ Importante ⌧ Desejável

**[RF008] Filtro de Mapa Interativo**
O sistema deve permitir que o usuário filtre o mapa por tipo de espécie, data ou nível de risco
de extinção.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF009] Manter Cadastro de Usuário**
O sistema deve permitir criar, ler, atualizar e desativar contas de usuário.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF010] Gerenciar Dados do Perfil**
O sistema deve permitir que o usuário edite suas informações públicas (nome, foto de perfil,
bio) e visualize suas estatísticas (total de espécies catalogadas).
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF011] Criar Postagem de Avistamento**
O sistema deve permitir que o usuário publique uma foto acompanhada da espécie
identificada e da localidade capturada.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF012] Excluir/Editar Postagem**
O usuário autor da postagem deve poder remover ou corrigir informações de sua publicação.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF013] Listar Feed de Postagens**
O sistema deve recuperar e exibir as postagens de forma cronológica ou por relevância para
os usuários.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF014] Consultar Informações da Espécie**
O sistema deve permitir a busca e leitura de dados detalhados de uma espécie (nome
científico, habitat) a partir do banco de dados.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF015] Atribuir Selo de Especialista**
O sistema deve vincular ao perfil do usuário, um selo de especialista para aqueles que
comprovem conhecimento na área (biólogos, veterinários)
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF016] Registrar Coordenadas de Avistamento**
O sistema deve persistir a Latitude e Longitude de cada nova postagem para alimentar o
mapa interativo.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF017] Filtrar Avistamentos por Localidade**
O sistema deve permitir a leitura de pontos geográficos dentro de um raio específico ou
região selecionada no mapa.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RF018] Executar Inferência de Imagem**
O sistema deve enviar a imagem capturada para a classe Tensorflow e receber como retorno a
predição da espécie com sua respectiva porcentagem de confiança.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF019] Vincular Espécie à Postagem**
O sistema deve permitir que uma ou mais espécies identificadas pelo TensorFlow sejam
associadas a uma postagem específica no momento da publicação ou edição.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF020] Desvincular Espécie de Postagem**
O sistema deve permitir a remoção do vínculo entre uma espécie e uma postagem, caso a
identificação seja invalidada por um especialista.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF021] Consultar Espécies por Postagem**
O sistema deve recuperar todas as espécies associadas a uma idPostagem específica para
exibição no feed ou detalhes do avistamento.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RF022] Listar Postagens por Espécie**
O sistema deve ser capaz de filtrar e exibir todas as postagens que contenham uma idEspecie
específica, permitindo visualizar a distribuição geográfica daquela espécie no mapa.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**5.2 REQUISITOS NÃO FUNCIONAIS**
**[RNF001] Segurança**
O sistema deve ser projetado para ser seguro, com recursos para proteger a
privacidade e confidencialidade dos usuários, como criptografia de senha, autenticação em
dois fatores e medidas de segurança para evitar ataques de hackers.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RNF002] Escalabilidade**
O sistema deve ser projetado para lidar com um grande número de usuários. 
Ele deve ser capaz de escalar facilmente conforme a demanda aumentar e
garantir que o desempenho não seja afetado negativamente.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RNF003] Usabilidade**
O sistema deve ser fácil de usar e navegar para garantir a melhor experiência do
usuário. Deve ter uma interface intuitiva e amigável, além de instruções claras para os
usuários.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RNF004] Tempo de Resposta (Performance)**
O processamento da imagem pelo modelo de Machine Learning para identificação da espécie
não deve ultrapassar 20 segundos.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RNF005] Disponibilidade Offline (Confiabilidade)**
O banco de dados local deve ser capaz de armazenar pelo menos 100 registros completos
(imagem + metadados) enquanto o dispositivo estiver sem conexão.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RNF006] Eficiência Energética**
O aplicativo deve ser otimizado para que o uso contínuo do GPS e câmera não consuma mais
de 30% de bateria por hora de uso ativo.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RNF007] Integridade de Dados Geográficos**
O sistema deve implementar filtros de validação para impedir que avistamentos de espécies
terrestres sejam registrados em coordenadas localizadas em oceanos ou desertos
incompatíveis.
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável

**[RNF008] Modularidade da API de Espécies**
A arquitetura do sistema deve permitir a substituição ou atualização da base de dados
científica (IUCN/IBAMA) sem a necessidade de alteração no núcleo do código-fonte.
Prioridade: ⌧ Essencial ◻ Importante ◻ Desejável

**[RNF009] Portabilidade**
O sistema deve ser desenvolvido de forma a garantir uma experiência fluida tanto em
sistemas Android quanto iOS
Prioridade: ◻ Essencial ⌧ Importante ◻ Desejável
