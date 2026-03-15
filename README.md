# EXTINCTION

## 1. INTRODUÇÃO

No contexto do desenvolvimento urbano brasileiro, a Mata Atlântica passou por perdas
significativas e, em muitos casos, irrecuperáveis em sua fauna e flora. Estima-se que cerca de
71,6% de sua vegetação nativa tenha sido desmatada. Nesse bioma encontram-se espécies
emblemáticas, como o Mico-leão-dourado e as Araucárias, que dependem diretamente da
preservação desses ambientes para sua sobrevivência.

Ao considerar também o Cerrado brasileiro, observa-se que espécies como o Lobo-guará
encontram-se ameaçadas de extinção. Caso as ameaças atuais, como a expansão urbana, a perda
de habitat e a ação humana, continuem, existe a possibilidade de que algumas dessas espécies
desapareçam nas próximas décadas. Assim, torna-se necessário ampliar a visibilidade sobre as
espécies ameaçadas. Com a disseminação de informações e maior conscientização da população,
é possível aumentar o engajamento social na proteção da biodiversidade.

Nesse contexto, surge a Extinction, uma nova iniciativa desenvolvida com o propósito de
auxiliar na proteção de espécies ameaçadas. É importante destacar que nem todos os fatores
relacionados ao desaparecimento dessas espécies podem ser abordados, como processos naturais
de seleção. Ainda assim, a plataforma pretende atuar como um importante meio de divulgação e
conscientização ambiental.

Portanto, sendo um software multicliente e sem fins lucrativos, a Extinction busca
contribuir para a educação ambiental e para a promoção de ações que incentivem a preservação
das espécies ameaçadas e de seus habitats naturais.

## 2. CONTEXTO DE NEGÓCIO

O uso de tecnologias digitais para monitoramento ambiental e reconhecimento de
espécies tem se expandido significativamente nos últimos anos. Avanços em áreas como visão
computacional, aprendizado de máquina e análise de imagens têm possibilitado o
desenvolvimento de sistemas capazes de identificar espécies animais e vegetais a partir de
fotografias. Essas tecnologias vêm sendo aplicadas em iniciativas de pesquisa, conservação da
biodiversidade e ciência-cidadã, permitindo ampliar o alcance das atividades de monitoramento
ecológico.

Entre as tecnologias utilizadas nesse domínio destaca-se o uso de frameworks de
aprendizado de máquina, como o TensorFlow, que permite o treinamento de modelos de
inteligência artificial voltados para tarefas de classificação e reconhecimento de padrões em
imagens. A aplicação dessas ferramentas possibilita o desenvolvimento de sistemas capazes de
reconhecer automaticamente determinadas espécies a partir de fotografias capturadas por
dispositivos móveis, câmeras de monitoramento ou bancos de dados digitais.

Apesar dos avanços tecnológicos disponíveis, a implementação de soluções baseadas em
inteligência artificial para reconhecimento de espécies ainda enfrenta desafios significativos no
contexto brasileiro. Um dos principais problemas está relacionado à escassez de dados de campo
estruturados e de alta qualidade para treinamento de modelos de aprendizado de máquina. Para
que algoritmos de visão computacional funcionem de maneira eficiente, é necessário um grande
volume de imagens rotuladas e representativas das espécies em diferentes condições ambientais,
ângulos, idades e variações naturais.

No Brasil, especialmente em determinadas regiões como o Distrito Federal, ainda
existem lacunas importantes na disponibilidade de conjuntos de dados específicos para
treinamento de modelos voltados ao reconhecimento da biodiversidade local. Muitas bases de
dados disponíveis são voltadas para espécies de outras regiões do mundo ou apresentam
quantidade limitada de registros para espécies brasileiras, o que dificulta a construção de modelos
confiáveis para identificação automática.

Outro desafio relevante está na integração prática entre modelos de inteligência artificial
e aplicações de software. Embora frameworks como o TensorFlow ofereçam recursos robustos
para treinamento de redes neurais e classificação de imagens, sua incorporação em sistemas de
uso cotidiano — como aplicações web ou móveis — pode apresentar complexidades técnicas.
Entre essas dificuldades estão a otimização do desempenho do modelo, a redução do tamanho dos
arquivos gerados, a adaptação para execução em dispositivos com recursos limitados e a garantia
de respostas rápidas durante o processo de reconhecimento de imagens.

Além disso, o desenvolvimento de soluções nesse domínio frequentemente depende da
utilização de bases de dados abertas e confiáveis sobre espécies ameaçadas. No Brasil, um dos
principais conjuntos de informações disponíveis publicamente é a lista de espécies ameaçadas
publicada pelo Ministério do Meio Ambiente. Esses dados incluem informações sobre o status de
conservação das espécies, classificação de risco de extinção e distribuição geográfica
aproximada.

O uso de dados abertos provenientes de órgãos governamentais representa uma
importante oportunidade para o desenvolvimento de aplicações voltadas à conservação ambiental,
pois permite que pesquisadores, desenvolvedores e instituições utilizem informações oficiais
como base para novos sistemas e análises. Entretanto, essas bases de dados frequentemente
apresentam limitações relacionadas à atualização, padronização ou integração direta com
ferramentas de aprendizado de máquina, exigindo processos adicionais de tratamento,
organização e adaptação dos dados.

Nesse cenário, observa-se que, embora existam tecnologias avançadas capazes de apoiar
o reconhecimento automatizado de espécies e o monitoramento ambiental, ainda persistem
desafios relacionados à disponibilidade de dados locais, à integração entre inteligência artificial e
aplicações digitais e ao aproveitamento eficiente de bases de dados abertas sobre biodiversidade.

Essas limitações evidenciam lacunas importantes no domínio de aplicação e indicam
oportunidades para o desenvolvimento de soluções tecnológicas que facilitem o acesso à
informação e o reconhecimento de espécies em contextos regionais específicos.

## 3. POSICIONAMENTO

### 3.1 Declaração do problema
|----|----|
|O problema de| espécies ameaçadas de extinção afetam a fauna brasileira, o equilíbrio em que a espécie está localizada e a possibilidade de nunca mais vermos certas espécies|
|afeta| o ecossistema natural do local, pois esse equilíbrio é muito frágil; se retirarmos uma parte para o local, acaba gerando uma superpopulação da espécie que precisava da outra para ser controlada|
|cujo impacto é|desequilíbrio no ambiente em que essas espécies estão.|
|uma solução de sucesso deveria| trazendo visibilidade aos animais, pessoas vão se importar mais com eles, ganhando visibilidade para que o governo também possa olhar mais para eles e cuidar melhor|
Informar localidade de algumas espécies que pessoas não sabem onde estão ou o que são.
Ajudar a preservar as vidas dessas espécies e fauna local, ao criar um pequeno movimento que irá ajudar.|

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
