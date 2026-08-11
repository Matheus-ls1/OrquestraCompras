<img width="300" height="150" alt="mermaid-diagram-2026-08-10-214856" src="https://github.com/user-attachments/assets/0f69ed5a-362a-4bd2-987b-94e645de4644" /># Introdução e Objetivos {#section-introduction-and-goals}

# Descrição
O OrquestraCompras é uma plataforma web inteligente que auxilia
usuários na busca e combinação de produtos disponíveis em diferentes
lojas de e-commerce.

O usuário informa os produtos desejados, orçamento, preferências e
restrições. O sistema utiliza agentes de Inteligência Artificial para
pesquisar produtos em lojas de e-commerce, analisar os resultados e
montar combinações adequadas aos critérios definidos.

A plataforma utiliza um modelo de linguagem (LLM) para auxiliar na
interpretação das necessidades do usuário e na análise das opções
encontradas.

### Requisitos Funcionais
| ID | Descrição |
|---|---|
| RF01 | O sistema deve permitir o cadastro de usuários. |
| RF02 | O sistema deve permitir que o usuário realize login. |
| RF03 | O sistema deve permitir informar os produtos que deseja pesquisar. |
| RF04 | O sistema deve permitir definir um orçamento máximo para a busca. |
| RF05 | O sistema deve permitir selecionar as lojas de e-commerce que serão pesquisadas. |
| RF06 | O sistema deve pesquisar produtos nos e-commerces selecionados. |
| RF07 | O sistema deve coletar informações como nome, preço, imagem e link dos produtos. |
| RF08 | O sistema deve utilizar IA para analisar os produtos encontrados. |
| RF09 | O sistema deve montar combinações de produtos respeitando o orçamento e as restrições informadas. |
| RF10 | O sistema deve apresentar ao usuário as combinações recomendadas. |
| RF11 | O sistema deve disponibilizar o link da loja original para cada produto recomendado. |
| RF12 | O sistema deve armazenar o histórico das buscas realizadas pelo usuário. |

## Objetivos de Qualidade {#_objetivos_de_qualidade}

::: formalpara-title
**Conteúdo**
:::

Os três principais (máx. cinco) objetivos de qualidade para a
arquitetura cujo cumprimento é de maior importância para as principais
partes interessadas. Nós realmente queremos dizer objetivos de qualidade
para a arquitetura. Não os confunda com objetivos de projeto. Eles não
são necessariamente idênticos.

Considere esta visão geral de tópicos potenciais (com base no padrão ISO
25010):

![Categorias de Requisitos de
Qualidade](images/01_2_iso-25010-topics-EN-2023.drawio.png)

::: formalpara-title
**Motivação**
:::

Você deve saber os objetivos de qualidade de suas partes interessadas
mais importantes, pois elas influenciarão decisões arquiteturais
fundamentais. Certifique-se de ser muito concreto sobre essas
qualidades, evite chavões. Se você, como arquiteto, não sabe como a
qualidade do seu trabalho será julgada...​

::: formalpara-title
**Forma**
:::

Uma tabela com objetivos de qualidade e cenários concretos, ordenados
por prioridades

## Partes Interessadas {#_partes_interessadas}

::: formalpara-title
**Conteúdo**
:::

Visão geral explícita das partes interessadas do sistema, ou seja, todas
as pessoas, funções ou organizações que

-   devem conhecer a arquitetura

-   precisam ser convencidas da arquitetura

-   precisam trabalhar com a arquitetura ou com código

-   precisam da documentação da arquitetura para seu trabalho

-   precisam tomar decisões sobre o sistema ou seu desenvolvimento

::: formalpara-title
**Motivação**
:::

Você deve conhecer todas as partes envolvidas no desenvolvimento do
sistema ou afetadas pelo sistema. Caso contrário, você pode ter
surpresas desagradáveis ​​mais tarde no processo de desenvolvimento. Essas
partes interessadas determinam a extensão e o nível de detalhes do seu
trabalho e seus resultados.

::: formalpara-title
**Forma**
:::

Tabela com nomes de funções, nomes de pessoas e suas expectativas com
relação à arquitetura e sua documentação.

+-------------+---------------------------+---------------------------+
| Função/Nome | Contato                   | Expectativas              |
+=============+===========================+===========================+
| *\<         | *\<Contato-1\>*           | *\<Expectativa-1\>*       |
| Função-1\>* |                           |                           |
+-------------+---------------------------+---------------------------+
| *\<         | *\<Contato-2\>*           | *\<Expectativa-2\>*       |
| Função-2\>* |                           |                           |
+-------------+---------------------------+---------------------------+

# Restrições Arquiteturais {#section-architecture-constraints}

::: formalpara-title
**Conteúdo**
:::

Qualquer requisito que restrinja arquitetos de software em sua liberdade
de decisões de design e implementação ou decisão sobre o processo de
desenvolvimento. Essas restrições às vezes vão além de sistemas
individuais e são válidas para organizações e empresas inteiras.

::: formalpara-title
**Motivação**
:::

Arquitetos devem saber exatamente onde são livres em suas decisões de
design e onde devem aderir às restrições. Restrições devem sempre ser
tratadas; elas podem ser negociáveis, no entanto.

::: formalpara-title
**Forma**
:::

Tabelas simples de restrições com explicações. Se necessário, você pode
subdividi-las em restrições técnicas, restrições organizacionais e
políticas e convenções (por exemplo, diretrizes de programação ou
controle de versão, convenções de documentação ou nomenclatura)

::: formalpara-title
**Mais informações**
:::

Consulte [Architecture Constraints](https://docs.arc42.org/section-2/)
na documentação do arc42.

# Contexto e Escopo {#section-context-and-scope}

::: formalpara-title
**Conteúdo**
:::

Contexto e escopo - como o nome sugere - delimita seu sistema (ou seja,
seu escopo) de todos os seus parceiros de comunicação (sistemas e
usuários vizinhos, ou seja, o contexto do seu sistema). Ele especifica,
portanto, as interfaces externas.

Se necessário, diferencie o contexto de negócios (entradas e saídas
específicas do domínio) do contexto técnico (canais, protocolos,
hardware).

::: formalpara-title
**Motivação**
:::

As interfaces de domínio e as interfaces técnicas para componentes
externos estão entre os aspectos mais críticos do seu sistema.
Certifique-se de entendê-las completamente.

::: formalpara-title
**Forma**
:::

Várias opções:

-   Diagramas de contexto

-   Listas de componentes externos e suas interfaces.

::: formalpara-title
**Mais informações**
:::

Consulte [Context and Scope](https://docs.arc42.org/section-3/) na
documentação do arc42.

## Contexto Negocial {#_contexto_negocial}

::: formalpara-title
**Conteúdo**
:::

Especificação de **todos** os componentes externos (usuários, sistemas
de TI, ...​) com explicações de entradas e saídas ou interfaces
específicas do domínio. Opcionalmente, você pode adicionar formatos
específicos do domínio ou protocolos de comunicação.

::: formalpara-title
**Motivação**
:::

Todas as partes interessadas devem entender quais dados são trocados com
o ambiente do sistema.

::: formalpara-title
**Forma**
:::

Todos os tipos de diagramas que mostram o sistema como uma caixa preta e
especificam as interfaces de domínio para os componentes externos.

Como alternativa (ou adicionalmente), você pode usar uma tabela. O
título da tabela é o nome do seu sistema, as três colunas contêm o nome
do componente externo, as entradas e as saídas.

**\<Diagrama ou Tabela\>**

**\<opcionalmente: Explicação das interfaces de domínio externo\>**

## Contexto Técnico {#_contexto_técnico}

::: formalpara-title
**Conteúdo**
:::

Interfaces técnicas (canais e mídias de transmissão) que vinculam seu
sistema ao seu ambiente. Além disso, um mapeamento de entrada/saída
específica de domínio para os canais, ou seja, uma explicação de qual
E/S usa qual canal.

::: formalpara-title
**Motivação**
:::

Muitas partes interessadas tomam decisões arquiteturais com base nas
interfaces técnicas entre o sistema e seu contexto. Especialmente os
designers de infraestrutura ou hardware decidem essas interfaces
técnicas.

::: formalpara-title
**Forma**
:::

Por exemplo, diagrama de implantação UML descrevendo canais para
sistemas vizinhos, junto com uma tabela de mapeamento mostrando os
relacionamentos entre canais e entrada/saída.

**\<Diagrama ou Tabela\>**

**\<opcionalmente: Explicação das interfaces técnicas\>**

**\<Mapeamento de entrada/saída para canais\>**

# Estratégia de Solução {#section-solution-strategy}

::: formalpara-title
**Conteúdo**
:::

Um breve resumo e explicação das decisões fundamentais e estratégias de
solução que moldam a arquitetura do sistema. Inclui

-   decisões de tecnologia

-   decisões sobre a decomposição de nível superior do sistema, por
    exemplo, uso de um padrão arquitetural ou *design pattern*

-   decisões sobre como atingir as principais metas de qualidade

-   decisões organizacionais relevantes, por exemplo, selecionar um
    processo de desenvolvimento ou delegar certas tarefas a terceiros.

::: formalpara-title
**Motivação**
:::

Essas decisões formam os pilares da sua arquitetura. Elas são a base
para muitas outras decisões detalhadas ou regras de implementação.

::: formalpara-title
**Forma**
:::

Mantenha as explicações dessas decisões-chave curtas.

Motive o que foi decidido e por que foi decidido dessa forma, com base
na declaração do problema, metas de qualidade e principais restrições.
Consulte os detalhes nas seções a seguir.

::: formalpara-title
**Mais informações**
:::

Consulte [Solution Strategy](https://docs.arc42.org/section-4/) na
documentação do arc42.

# Visão de Blocos de Construção {#section-building-block-view}

::: formalpara-title
**Conteúdo**
:::

A visão de blocos de construção mostra a decomposição estática do
sistema em blocos (módulos, componentes, subsistemas, classes,
interfaces, pacotes, bibliotecas, frameworks, camadas, partições,
níveis, funções, macros, operações, estruturas de dados, ...​) bem como
suas dependências (relacionamentos, associações, ...​)

Esta visão é obrigatória para toda documentação de arquitetura. Em
analogia a uma casa, esta é a *planta baixa*.

::: formalpara-title
**Motivação**
:::

Mantenha uma visão geral do seu código-fonte tornando sua estrutura
compreensível por meio de abstração.

Isso permite que você se comunique com suas partes interessadas em um
nível abstrato sem revelar detalhes de implementação.

::: formalpara-title
**Forma**
:::

A visão de blocos de construção é uma coleção hierárquica de caixas
pretas e caixas brancas (veja a figura abaixo) e suas descrições.

![Hierarquia de blocos de construção](images/05_building_blocks-EN.png)

**Nível 1** é a descrição da caixa branca do sistema geral, juntamente
com descrições de caixa preta de todos os blocos de construção contidos.

**Nível 2** amplia alguns blocos de construção do nível 1. Portanto, ele
contém a descrição da caixa branca dos blocos de construção selecionados
do nível 1, juntamente com descrições de caixa preta de seus blocos de
construção internos.

**Nível 3** amplia os blocos de construção selecionados do nível 2, e
assim por diante.

::: formalpara-title
**Mais informações**
:::

Consulte [Building Block View](https://docs.arc42.org/section-5/) na
documentação do arc42.

## Visão Sistêmica Geral de Caixa Branca {#_visão_sistêmica_geral_de_caixa_branca}

Aqui você descreve a decomposição geral do sistema usando o seguinte
modelo de caixa branca. Ele contém

-   um diagrama de visão geral

-   uma motivação para a decomposição

-   descrições de caixa preta dos blocos de construção contidos. Para
    isso, oferecemos alternativas:

    -   use *uma* tabela para uma visão geral curta e pragmática de
        todos os blocos de construção contidos e suas interfaces

    -   use uma lista de descrições de caixa preta dos blocos de
        construção de acordo com o modelo de caixa preta (veja abaixo).
        Dependendo da sua escolha de ferramenta, esta lista pode ser
        subcapítulos (em arquivos de texto), subpáginas (em uma Wiki) ou
        elementos aninhados (em uma ferramenta de modelagem).

-   (opcional:) interfaces importantes, que não são explicadas nos
    modelos de caixa preta de um bloco de construção, mas são muito
    importantes para entender a caixa branca. Já que há tantas maneiras
    de especificar interfaces, por que não fornecer um modelo específico
    para elas? No pior caso, você tem que especificar e descrever
    sintaxe, semântica, protocolos, tratamento de erros, restrições,
    versões, qualidades, compatibilidades necessárias e muito mais. Na
    melhor das hipóteses, você conseguirá usar exemplos ou descrições
    simples.

***\<Diagrama de Visão Geral\>***

Motivação

:   *\<explicação textual\>*

Blocos de Construção Contidos

:   *\<Descrição dos blocos de construção contidos (caixas pretas)\>*

Interfaces Importantes

:   *\<Descrição de interfaces importantes\>*

Insira suas explicações de caixas pretas do nível 1:

Se você usar a forma tabular, você descreverá apenas suas caixas pretas
com nome e responsabilidade de acordo com o seguinte esquema:

+----------------------+-----------------------------------------------+
| **Nome**             | **Responsabilidade**                          |
+======================+===============================================+
| *\<caixa preta 1\>*  | *\<Texto\>*                                   |
+----------------------+-----------------------------------------------+
| *\<caixa preta 2\>*  | *\<Texto\>*                                   |
+----------------------+-----------------------------------------------+

Se você usar uma lista de descrições de caixa preta, então você preenche
um modelo de caixa preta separado para cada bloco de construção
importante. Seu título é o nome da caixa preta.

### \<Nome Caixa Preta 1\> {#_nome_caixa_preta_1}

Aqui você descreve \<caixa preta 1\> de acordo com o seguinte modelo de
caixa preta:

-   Propósito/Responsabilidade

-   Interface(s), quando não são extraídas como parágrafos separados.
    Essas interfaces podem incluir qualidades e características de
    desempenho.

-   (Opcional) Características de qualidade/desempenho da caixa preta,
    por exemplo, disponibilidade, comportamento de tempo de execução,
    ...​.

-   (Opcional) Local do diretório/arquivo

-   (Opcional) Requisitos atendidos (se você precisar de rastreabilidade
    para requisitos).

-   (Opcional) Problemas/questões/riscos abertos

*\<Propósito/Responsabilidade\>*

*\<Interface(s)\>*

*\<(Opcional) Características de Qualidade/Desempenho\>*

*\<(Opcional) Local do Diretório/Arquivo\>*

*\<(Opcional) Requisitos Cumpridos\>*

*\<(opcional) Problemas/Riscos Abertos\>*

### \<Nome Caixa Preta 2\> {#_nome_caixa_preta_2}

*\<modelo de caixa preta\>*

### \<Nome Caixa Preta n\> {#_nome_caixa_preta_n}

*\<modelo de caixa preta\>*

### \<Nome Interface 1\> {#_nome_interface_1}

...​

### \<Nome Interface m\> {#_nome_interface_m}

## Nível 2 {#_nível_2}

Aqui você pode especificar a estrutura interna de (alguns) blocos de
construção do nível 1 como caixas brancas.

Você tem que decidir quais blocos de construção do seu sistema são
importantes o suficiente para justificar uma descrição tão detalhada.
Por favor, prefira relevância à completude. Especifique blocos de
construção importantes, surpreendentes, arriscados, complexos ou
voláteis. Deixe de fora partes normais, simples, chatas ou padronizadas
do seu sistema

### Caixa Branca *\<Bloco de Construção 1\>* {#_caixa_branca_bloco_de_construção_1}

...​descreve a estrutura interna do *bloco de construção 1*.

*\<modelo de caixa branca\>*

### Caixa Branca *\<Bloco de Construção 2\>* {#_caixa_branca_bloco_de_construção_2}

*\<modelo de caixa branca\>*

...​

### Caixa Branca *\<Bloco de Construção m\>* {#_caixa_branca_bloco_de_construção_m}

*\<modelo de caixa branca\>*

## Nível 3 {#_nível_3}

Aqui você pode especificar a estrutura interna de (alguns) blocos de
construção do nível 2 como caixas brancas.

Quando precisar de níveis mais detalhados de sua arquitetura, copie esta
parte do arc42 para níveis adicionais.

### Caixa Branca \<\_Bloco de Construção x.1\_\> {#_caixa_branca_bloco_de_construção_x_1}

Especifica a estrutura interna do *bloco de construção x.1*.

*\<modelo de caixa branca\>*

### Caixa Branca \<\_Bloco de Construção x.2\_\> {#_caixa_branca_bloco_de_construção_x_2}

*\<modelo de caixa branca\>*

### Caixa Branca \<\_Bloco de Construção y.1\_\> {#_caixa_branca_bloco_de_construção_y_1}

*\<modelo de caixa branca\>*

# Visão de Tempo de Execução {#section-runtime-view}

::: formalpara-title
**Conteúdo**
:::

A visão de tempo de execução descreve o comportamento concreto e as
interações dos blocos de construção do sistema na forma de cenários das
seguintes áreas:

-   casos de uso ou recursos importantes: como os blocos de construção
    os executam?

-   interações em interfaces externas críticas: como os blocos de
    construção cooperam com os usuários e sistemas vizinhos?

-   operação e administração: lançamento, inicialização, parada

-   cenários de erro e exceção

Observação: O principal critério para a escolha de cenários possíveis
(sequências, fluxos de trabalho) é sua **relevância arquitetural**.
**Não** é importante descrever um grande número de cenários. Você deve
documentar uma seleção representativa.

::: formalpara-title
**Motivação**
:::

Você deve entender como (instâncias de) blocos de construção do seu
sistema realizam seu trabalho e se comunicam em tempo de execução. Você
capturará principalmente cenários em sua documentação para comunicar sua
arquitetura às partes interessadas que estão menos dispostas ou capazes
de ler e entender os modelos estáticos (visão de bloco de construção,
visão de implantação).

::: formalpara-title
**Forma**
:::

Há muitas notações para descrever cenários, por exemplo,

-   lista numerada de etapas (em linguagem natural)

-   diagramas de atividade ou fluxogramas

-   diagramas de sequência

-   BPMN ou EPCs (cadeias de processos de eventos)

-   máquinas de estado

-   ...​

::: formalpara-title
**Mais informações**
:::

Consulte [Runtime View](https://docs.arc42.org/section-6/) na
documentação do arc42.

## \<Cenário de Tempo de Execução 1\> {#_cenário_de_tempo_de_execução_1}

-   *\<inserir diagrama de tempo de execução ou descrição textual do
    cenário\>*

-   *\<inserir descrição dos aspectos notáveis ​​das interações entre as
    instâncias do bloco de construção descritas neste diagrama.\>*

## \<Cenário de Tempo de Execução 2\> {#_cenário_de_tempo_de_execução_2}

## ...​

## \<Cenário de Tempo de Execução n\> {#_cenário_de_tempo_de_execução_n}

# Visão de Implantação {#section-deployment-view}

::: formalpara-title
**Conteúdo**
:::

A visão de implantação descreve:

1.  infraestrutura técnica usada para executar seu sistema, com
    elementos de infraestrutura como localizações geográficas,
    ambientes, computadores, processadores, canais e topologias de rede,
    bem como outros elementos de infraestrutura e

2.  mapeamento de blocos de construção (de software) para esses
    elementos de infraestrutura.

Frequentemente, os sistemas são executados em ambientes diferentes, por
exemplo, ambiente de desenvolvimento, ambiente de teste, ambiente de
produção. Nesses casos, você deve documentar todos os ambientes
relevantes.

Documente especialmente uma visão de implantação se seu software for
executado como um sistema distribuído com mais de um computador,
processador, servidor ou contêiner ou quando você projeta e constrói
seus próprios processadores e chips de hardware.

De uma perspectiva de software, é suficiente capturar apenas os
elementos de uma infraestrutura que são necessários para mostrar uma
implantação de seus blocos de construção. Arquitetos de hardware podem
ir além disso e descrever uma infraestrutura em qualquer nível de
detalhe que precisem capturar.

::: formalpara-title
**Motivação**
:::

O software não roda sem hardware. Essa infraestrutura subjacente pode e
influenciará um sistema e/ou alguns conceitos transversais. Portanto, é
necessário conhecer a infraestrutura.

::: formalpara-title
**Forma**
:::

Talvez um diagrama de implantação de nível mais alto já esteja contido
na seção 3.2. como contexto técnico com sua própria infraestrutura como
UMA caixa preta. Nesta seção, pode-se ampliar esta caixa preta usando
diagramas de implantação adicionais:

-   UML oferece diagramas de implantação para expressar essa visão.
    Use-o, provavelmente com diagramas aninhados, quando sua
    infraestrutura for mais complexa.

-   Quando suas partes interessadas (de hardware) preferirem outros
    tipos de diagramas em vez de um diagrama de implantação, deixe-os
    usar qualquer tipo que seja capaz de mostrar nós e canais da
    infraestrutura.

::: formalpara-title
**Mais informações**
:::

Consulte [Deployment View](https://docs.arc42.org/section-7/) na
documentação do arc42.

## Nível de Infraestrutura 1 {#_nível_de_infraestrutura_1}

![Uploadin<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.2.0/css/all.min.css" type="text/css"?>
<svg id="graph-30" width="100%" xmlns="http://www.w3.org/2000/svg" style="overflow: hidden; max-width: 100%; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); background-color: rgb(2, 8, 23);" role="graphics-document document" aria-roledescription="c4" height="100%" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:ev="http://www.w3.org/2001/xml-events"><defs><symbol id="graph-30-computer" width="24" height="24"><path transform="scale(.5)" d="M2 2v13h20v-13h-20zm18 11h-16v-9h16v9zm-10.228 6l.466-1h3.524l.467 1h-4.457zm14.228 3h-24l2-6h2.104l-1.33 4h18.45l-1.297-4h2.073l2 6zm-5-10h-14v-7h14v7z"></path></symbol></defs><defs><symbol id="graph-30-database" fill-rule="evenodd" clip-rule="evenodd"><path transform="scale(.5)" d="M12.258.001l.256.004.255.005.253.008.251.01.249.012.247.015.246.016.242.019.241.02.239.023.236.024.233.027.231.028.229.031.225.032.223.034.22.036.217.038.214.04.211.041.208.043.205.045.201.046.198.048.194.05.191.051.187.053.183.054.18.056.175.057.172.059.168.06.163.061.16.063.155.064.15.066.074.033.073.033.071.034.07.034.069.035.068.035.067.035.066.035.064.036.064.036.062.036.06.036.06.037.058.037.058.037.055.038.055.038.053.038.052.038.051.039.05.039.048.039.047.039.045.04.044.04.043.04.041.04.04.041.039.041.037.041.036.041.034.041.033.042.032.042.03.042.029.042.027.042.026.043.024.043.023.043.021.043.02.043.018.044.017.043.015.044.013.044.012.044.011.045.009.044.007.045.006.045.004.045.002.045.001.045v17l-.001.045-.002.045-.004.045-.006.045-.007.045-.009.044-.011.045-.012.044-.013.044-.015.044-.017.043-.018.044-.02.043-.021.043-.023.043-.024.043-.026.043-.027.042-.029.042-.03.042-.032.042-.033.042-.034.041-.036.041-.037.041-.039.041-.04.041-.041.04-.043.04-.044.04-.045.04-.047.039-.048.039-.05.039-.051.039-.052.038-.053.038-.055.038-.055.038-.058.037-.058.037-.06.037-.06.036-.062.036-.064.036-.064.036-.066.035-.067.035-.068.035-.069.035-.07.034-.071.034-.073.033-.074.033-.15.066-.155.064-.16.063-.163.061-.168.06-.172.059-.175.057-.18.056-.183.054-.187.053-.191.051-.194.05-.198.048-.201.046-.205.045-.208.043-.211.041-.214.04-.217.038-.22.036-.223.034-.225.032-.229.031-.231.028-.233.027-.236.024-.239.023-.241.02-.242.019-.246.016-.247.015-.249.012-.251.01-.253.008-.255.005-.256.004-.258.001-.258-.001-.256-.004-.255-.005-.253-.008-.251-.01-.249-.012-.247-.015-.245-.016-.243-.019-.241-.02-.238-.023-.236-.024-.234-.027-.231-.028-.228-.031-.226-.032-.223-.034-.22-.036-.217-.038-.214-.04-.211-.041-.208-.043-.204-.045-.201-.046-.198-.048-.195-.05-.19-.051-.187-.053-.184-.054-.179-.056-.176-.057-.172-.059-.167-.06-.164-.061-.159-.063-.155-.064-.151-.066-.074-.033-.072-.033-.072-.034-.07-.034-.069-.035-.068-.035-.067-.035-.066-.035-.064-.036-.063-.036-.062-.036-.061-.036-.06-.037-.058-.037-.057-.037-.056-.038-.055-.038-.053-.038-.052-.038-.051-.039-.049-.039-.049-.039-.046-.039-.046-.04-.044-.04-.043-.04-.041-.04-.04-.041-.039-.041-.037-.041-.036-.041-.034-.041-.033-.042-.032-.042-.03-.042-.029-.042-.027-.042-.026-.043-.024-.043-.023-.043-.021-.043-.02-.043-.018-.044-.017-.043-.015-.044-.013-.044-.012-.044-.011-.045-.009-.044-.007-.045-.006-.045-.004-.045-.002-.045-.001-.045v-17l.001-.045.002-.045.004-.045.006-.045.007-.045.009-.044.011-.045.012-.044.013-.044.015-.044.017-.043.018-.044.02-.043.021-.043.023-.043.024-.043.026-.043.027-.042.029-.042.03-.042.032-.042.033-.042.034-.041.036-.041.037-.041.039-.041.04-.041.041-.04.043-.04.044-.04.046-.04.046-.039.049-.039.049-.039.051-.039.052-.038.053-.038.055-.038.056-.038.057-.037.058-.037.06-.037.061-.036.062-.036.063-.036.064-.036.066-.035.067-.035.068-.035.069-.035.07-.034.072-.034.072-.033.074-.033.151-.066.155-.064.159-.063.164-.061.167-.06.172-.059.176-.057.179-.056.184-.054.187-.053.19-.051.195-.05.198-.048.201-.046.204-.045.208-.043.211-.041.214-.04.217-.038.22-.036.223-.034.226-.032.228-.031.231-.028.234-.027.236-.024.238-.023.241-.02.243-.019.245-.016.247-.015.249-.012.251-.01.253-.008.255-.005.256-.004.258-.001.258.001zm-9.258 20.499v.01l.001.021.003.021.004.022.005.021.006.022.007.022.009.023.01.022.011.023.012.023.013.023.015.023.016.024.017.023.018.024.019.024.021.024.022.025.023.024.024.025.052.049.056.05.061.051.066.051.07.051.075.051.079.052.084.052.088.052.092.052.097.052.102.051.105.052.11.052.114.051.119.051.123.051.127.05.131.05.135.05.139.048.144.049.147.047.152.047.155.047.16.045.163.045.167.043.171.043.176.041.178.041.183.039.187.039.19.037.194.035.197.035.202.033.204.031.209.03.212.029.216.027.219.025.222.024.226.021.23.02.233.018.236.016.24.015.243.012.246.01.249.008.253.005.256.004.259.001.26-.001.257-.004.254-.005.25-.008.247-.011.244-.012.241-.014.237-.016.233-.018.231-.021.226-.021.224-.024.22-.026.216-.027.212-.028.21-.031.205-.031.202-.034.198-.034.194-.036.191-.037.187-.039.183-.04.179-.04.175-.042.172-.043.168-.044.163-.045.16-.046.155-.046.152-.047.148-.048.143-.049.139-.049.136-.05.131-.05.126-.05.123-.051.118-.052.114-.051.11-.052.106-.052.101-.052.096-.052.092-.052.088-.053.083-.051.079-.052.074-.052.07-.051.065-.051.06-.051.056-.05.051-.05.023-.024.023-.025.021-.024.02-.024.019-.024.018-.024.017-.024.015-.023.014-.024.013-.023.012-.023.01-.023.01-.022.008-.022.006-.022.006-.022.004-.022.004-.021.001-.021.001-.021v-4.127l-.077.055-.08.053-.083.054-.085.053-.087.052-.09.052-.093.051-.095.05-.097.05-.1.049-.102.049-.105.048-.106.047-.109.047-.111.046-.114.045-.115.045-.118.044-.12.043-.122.042-.124.042-.126.041-.128.04-.13.04-.132.038-.134.038-.135.037-.138.037-.139.035-.142.035-.143.034-.144.033-.147.032-.148.031-.15.03-.151.03-.153.029-.154.027-.156.027-.158.026-.159.025-.161.024-.162.023-.163.022-.165.021-.166.02-.167.019-.169.018-.169.017-.171.016-.173.015-.173.014-.175.013-.175.012-.177.011-.178.01-.179.008-.179.008-.181.006-.182.005-.182.004-.184.003-.184.002h-.37l-.184-.002-.184-.003-.182-.004-.182-.005-.181-.006-.179-.008-.179-.008-.178-.01-.176-.011-.176-.012-.175-.013-.173-.014-.172-.015-.171-.016-.17-.017-.169-.018-.167-.019-.166-.02-.165-.021-.163-.022-.162-.023-.161-.024-.159-.025-.157-.026-.156-.027-.155-.027-.153-.029-.151-.03-.15-.03-.148-.031-.146-.032-.145-.033-.143-.034-.141-.035-.14-.035-.137-.037-.136-.037-.134-.038-.132-.038-.13-.04-.128-.04-.126-.041-.124-.042-.122-.042-.12-.044-.117-.043-.116-.045-.113-.045-.112-.046-.109-.047-.106-.047-.105-.048-.102-.049-.1-.049-.097-.05-.095-.05-.093-.052-.09-.051-.087-.052-.085-.053-.083-.054-.08-.054-.077-.054v4.127zm0-5.654v.011l.001.021.003.021.004.021.005.022.006.022.007.022.009.022.01.022.011.023.012.023.013.023.015.024.016.023.017.024.018.024.019.024.021.024.022.024.023.025.024.024.052.05.056.05.061.05.066.051.07.051.075.052.079.051.084.052.088.052.092.052.097.052.102.052.105.052.11.051.114.051.119.052.123.05.127.051.131.05.135.049.139.049.144.048.147.048.152.047.155.046.16.045.163.045.167.044.171.042.176.042.178.04.183.04.187.038.19.037.194.036.197.034.202.033.204.032.209.03.212.028.216.027.219.025.222.024.226.022.23.02.233.018.236.016.24.014.243.012.246.01.249.008.253.006.256.003.259.001.26-.001.257-.003.254-.006.25-.008.247-.01.244-.012.241-.015.237-.016.233-.018.231-.02.226-.022.224-.024.22-.025.216-.027.212-.029.21-.03.205-.032.202-.033.198-.035.194-.036.191-.037.187-.039.183-.039.179-.041.175-.042.172-.043.168-.044.163-.045.16-.045.155-.047.152-.047.148-.048.143-.048.139-.05.136-.049.131-.05.126-.051.123-.051.118-.051.114-.052.11-.052.106-.052.101-.052.096-.052.092-.052.088-.052.083-.052.079-.052.074-.051.07-.052.065-.051.06-.05.056-.051.051-.049.023-.025.023-.024.021-.025.02-.024.019-.024.018-.024.017-.024.015-.023.014-.023.013-.024.012-.022.01-.023.01-.023.008-.022.006-.022.006-.022.004-.021.004-.022.001-.021.001-.021v-4.139l-.077.054-.08.054-.083.054-.085.052-.087.053-.09.051-.093.051-.095.051-.097.05-.1.049-.102.049-.105.048-.106.047-.109.047-.111.046-.114.045-.115.044-.118.044-.12.044-.122.042-.124.042-.126.041-.128.04-.13.039-.132.039-.134.038-.135.037-.138.036-.139.036-.142.035-.143.033-.144.033-.147.033-.148.031-.15.03-.151.03-.153.028-.154.028-.156.027-.158.026-.159.025-.161.024-.162.023-.163.022-.165.021-.166.02-.167.019-.169.018-.169.017-.171.016-.173.015-.173.014-.175.013-.175.012-.177.011-.178.009-.179.009-.179.007-.181.007-.182.005-.182.004-.184.003-.184.002h-.37l-.184-.002-.184-.003-.182-.004-.182-.005-.181-.007-.179-.007-.179-.009-.178-.009-.176-.011-.176-.012-.175-.013-.173-.014-.172-.015-.171-.016-.17-.017-.169-.018-.167-.019-.166-.02-.165-.021-.163-.022-.162-.023-.161-.024-.159-.025-.157-.026-.156-.027-.155-.028-.153-.028-.151-.03-.15-.03-.148-.031-.146-.033-.145-.033-.143-.033-.141-.035-.14-.036-.137-.036-.136-.037-.134-.038-.132-.039-.13-.039-.128-.04-.126-.041-.124-.042-.122-.043-.12-.043-.117-.044-.116-.044-.113-.046-.112-.046-.109-.046-.106-.047-.105-.048-.102-.049-.1-.049-.097-.05-.095-.051-.093-.051-.09-.051-.087-.053-.085-.052-.083-.054-.08-.054-.077-.054v4.139zm0-5.666v.011l.001.02.003.022.004.021.005.022.006.021.007.022.009.023.01.022.011.023.012.023.013.023.015.023.016.024.017.024.018.023.019.024.021.025.022.024.023.024.024.025.052.05.056.05.061.05.066.051.07.051.075.052.079.051.084.052.088.052.092.052.097.052.102.052.105.051.11.052.114.051.119.051.123.051.127.05.131.05.135.05.139.049.144.048.147.048.152.047.155.046.16.045.163.045.167.043.171.043.176.042.178.04.183.04.187.038.19.037.194.036.197.034.202.033.204.032.209.03.212.028.216.027.219.025.222.024.226.021.23.02.233.018.236.017.24.014.243.012.246.01.249.008.253.006.256.003.259.001.26-.001.257-.003.254-.006.25-.008.247-.01.244-.013.241-.014.237-.016.233-.018.231-.02.226-.022.224-.024.22-.025.216-.027.212-.029.21-.03.205-.032.202-.033.198-.035.194-.036.191-.037.187-.039.183-.039.179-.041.175-.042.172-.043.168-.044.163-.045.16-.045.155-.047.152-.047.148-.048.143-.049.139-.049.136-.049.131-.051.126-.05.123-.051.118-.052.114-.051.11-.052.106-.052.101-.052.096-.052.092-.052.088-.052.083-.052.079-.052.074-.052.07-.051.065-.051.06-.051.056-.05.051-.049.023-.025.023-.025.021-.024.02-.024.019-.024.018-.024.017-.024.015-.023.014-.024.013-.023.012-.023.01-.022.01-.023.008-.022.006-.022.006-.022.004-.022.004-.021.001-.021.001-.021v-4.153l-.077.054-.08.054-.083.053-.085.053-.087.053-.09.051-.093.051-.095.051-.097.05-.1.049-.102.048-.105.048-.106.048-.109.046-.111.046-.114.046-.115.044-.118.044-.12.043-.122.043-.124.042-.126.041-.128.04-.13.039-.132.039-.134.038-.135.037-.138.036-.139.036-.142.034-.143.034-.144.033-.147.032-.148.032-.15.03-.151.03-.153.028-.154.028-.156.027-.158.026-.159.024-.161.024-.162.023-.163.023-.165.021-.166.02-.167.019-.169.018-.169.017-.171.016-.173.015-.173.014-.175.013-.175.012-.177.01-.178.01-.179.009-.179.007-.181.006-.182.006-.182.004-.184.003-.184.001-.185.001-.185-.001-.184-.001-.184-.003-.182-.004-.182-.006-.181-.006-.179-.007-.179-.009-.178-.01-.176-.01-.176-.012-.175-.013-.173-.014-.172-.015-.171-.016-.17-.017-.169-.018-.167-.019-.166-.02-.165-.021-.163-.023-.162-.023-.161-.024-.159-.024-.157-.026-.156-.027-.155-.028-.153-.028-.151-.03-.15-.03-.148-.032-.146-.032-.145-.033-.143-.034-.141-.034-.14-.036-.137-.036-.136-.037-.134-.038-.132-.039-.13-.039-.128-.041-.126-.041-.124-.041-.122-.043-.12-.043-.117-.044-.116-.044-.113-.046-.112-.046-.109-.046-.106-.048-.105-.048-.102-.048-.1-.05-.097-.049-.095-.051-.093-.051-.09-.052-.087-.052-.085-.053-.083-.053-.08-.054-.077-.054v4.153zm8.74-8.179l-.257.004-.254.005-.25.008-.247.011-.244.012-.241.014-.237.016-.233.018-.231.021-.226.022-.224.023-.22.026-.216.027-.212.028-.21.031-.205.032-.202.033-.198.034-.194.036-.191.038-.187.038-.183.04-.179.041-.175.042-.172.043-.168.043-.163.045-.16.046-.155.046-.152.048-.148.048-.143.048-.139.049-.136.05-.131.05-.126.051-.123.051-.118.051-.114.052-.11.052-.106.052-.101.052-.096.052-.092.052-.088.052-.083.052-.079.052-.074.051-.07.052-.065.051-.06.05-.056.05-.051.05-.023.025-.023.024-.021.024-.02.025-.019.024-.018.024-.017.023-.015.024-.014.023-.013.023-.012.023-.01.023-.01.022-.008.022-.006.023-.006.021-.004.022-.004.021-.001.021-.001.021.001.021.001.021.004.021.004.022.006.021.006.023.008.022.01.022.01.023.012.023.013.023.014.023.015.024.017.023.018.024.019.024.02.025.021.024.023.024.023.025.051.05.056.05.06.05.065.051.07.052.074.051.079.052.083.052.088.052.092.052.096.052.101.052.106.052.11.052.114.052.118.051.123.051.126.051.131.05.136.05.139.049.143.048.148.048.152.048.155.046.16.046.163.045.168.043.172.043.175.042.179.041.183.04.187.038.191.038.194.036.198.034.202.033.205.032.21.031.212.028.216.027.22.026.224.023.226.022.231.021.233.018.237.016.241.014.244.012.247.011.25.008.254.005.257.004.26.001.26-.001.257-.004.254-.005.25-.008.247-.011.244-.012.241-.014.237-.016.233-.018.231-.021.226-.022.224-.023.22-.026.216-.027.212-.028.21-.031.205-.032.202-.033.198-.034.194-.036.191-.038.187-.038.183-.04.179-.041.175-.042.172-.043.168-.043.163-.045.16-.046.155-.046.152-.048.148-.048.143-.048.139-.049.136-.05.131-.05.126-.051.123-.051.118-.051.114-.052.11-.052.106-.052.101-.052.096-.052.092-.052.088-.052.083-.052.079-.052.074-.051.07-.052.065-.051.06-.05.056-.05.051-.05.023-.025.023-.024.021-.024.02-.025.019-.024.018-.024.017-.023.015-.024.014-.023.013-.023.012-.023.01-.023.01-.022.008-.022.006-.023.006-.021.004-.022.004-.021.001-.021.001-.021-.001-.021-.001-.021-.004-.021-.004-.022-.006-.021-.006-.023-.008-.022-.01-.022-.01-.023-.012-.023-.013-.023-.014-.023-.015-.024-.017-.023-.018-.024-.019-.024-.02-.025-.021-.024-.023-.024-.023-.025-.051-.05-.056-.05-.06-.05-.065-.051-.07-.052-.074-.051-.079-.052-.083-.052-.088-.052-.092-.052-.096-.052-.101-.052-.106-.052-.11-.052-.114-.052-.118-.051-.123-.051-.126-.051-.131-.05-.136-.05-.139-.049-.143-.048-.148-.048-.152-.048-.155-.046-.16-.046-.163-.045-.168-.043-.172-.043-.175-.042-.179-.041-.183-.04-.187-.038-.191-.038-.194-.036-.198-.034-.202-.033-.205-.032-.21-.031-.212-.028-.216-.027-.22-.026-.224-.023-.226-.022-.231-.021-.233-.018-.237-.016-.241-.014-.244-.012-.247-.011-.25-.008-.254-.005-.257-.004-.26-.001-.26.001z"></path></symbol></defs><defs><symbol id="graph-30-clock" width="24" height="24"><path transform="scale(.5)" d="M12 2c5.514 0 10 4.486 10 10s-4.486 10-10 10-10-4.486-10-10 4.486-10 10-10zm0-2c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm5.848 12.459c.202.038.202.333.001.372-1.907.361-6.045 1.111-6.547 1.111-.719 0-1.301-.582-1.301-1.301 0-.512.77-5.447 1.125-7.445.034-.192.312-.181.343.014l.985 6.238 5.394 1.011z"></path></symbol></defs><defs><marker id="graph-30-arrowhead" refX="9" refY="5" markerUnits="userSpaceOnUse" markerWidth="12" markerHeight="12" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z"></path></marker></defs><defs><marker id="graph-30-arrowend" refX="1" refY="5" markerUnits="userSpaceOnUse" markerWidth="12" markerHeight="12" orient="auto"><path d="M 10 0 L 0 5 L 10 10 z"></path></marker></defs><defs><marker id="graph-30-crosshead" markerWidth="15" markerHeight="8" orient="auto" refX="16" refY="4"><path fill="black" stroke="#000000" stroke-width="1px" d="M 9,2 V 6 L16,4 Z" style="stroke-dasharray: 0, 0;"></path><path fill="none" stroke="#000000" stroke-width="1px" d="M 0,1 L 6,7 M 6,1 L 0,7" style="stroke-dasharray: 0, 0;"></path></marker></defs><defs><marker id="graph-30-filled-head" refX="18" refY="7" markerWidth="20" markerHeight="28" orient="auto"><path d="M 18,7 L9,13 L14,7 L9,1 Z"></path></marker></defs><g id="viewport-20260811004736769" class="svg-pan-zoom_viewport" transform="matrix(0.5162866508707087,0,0,0.5162866508707087,205.1130622980457,101.2471634599773)" style="transform: matrix(0.516287, 0, 0, 0.516287, 205.113, 101.247);"><style>#graph-30{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;fill:#ccc;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#graph-30 .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#graph-30 .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#graph-30 .error-icon{fill:#a44141;}#graph-30 .error-text{fill:#ddd;stroke:#ddd;}#graph-30 .edge-thickness-normal{stroke-width:1px;}#graph-30 .edge-thickness-thick{stroke-width:3.5px;}#graph-30 .edge-pattern-solid{stroke-dasharray:0;}#graph-30 .edge-thickness-invisible{stroke-width:0;fill:none;}#graph-30 .edge-pattern-dashed{stroke-dasharray:3;}#graph-30 .edge-pattern-dotted{stroke-dasharray:2;}#graph-30 .marker{fill:lightgrey;stroke:lightgrey;}#graph-30 .marker.cross{stroke:lightgrey;}#graph-30 svg{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;}#graph-30 p{margin:0;}#graph-30 .person{stroke:#cccccc;fill:#1f2020;}#graph-30 .node .neo-node{stroke:#ccc;}#graph-30 [data-look="neo"].node rect,#graph-30 [data-look="neo"].cluster rect,#graph-30 [data-look="neo"].node polygon{stroke:url(#graph-30-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#graph-30 [data-look="neo"].swimlane.cluster rect{filter:none;}#graph-30 [data-look="neo"].node path{stroke:url(#graph-30-gradient);stroke-width:1px;}#graph-30 [data-look="neo"].node .outer-path{filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#graph-30 [data-look="neo"].node .neo-line path{stroke:#ccc;filter:none;}#graph-30 [data-look="neo"].node circle{stroke:url(#graph-30-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#graph-30 [data-look="neo"].node circle .state-start{fill:#000000;}#graph-30 [data-look="neo"].icon-shape .icon{fill:url(#graph-30-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#graph-30 [data-look="neo"].icon-shape .icon-neo path{stroke:url(#graph-30-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#graph-30 :root{--mermaid-font-family:"trebuchet ms",verdana,arial,sans-serif;}</style><g></g><g class="person-man"><rect x="150" y="167" fill="#08427B" stroke="#073B6F" width="426" height="135" rx="2.5" ry="2.5" stroke-width="0.5"></rect><text fill="#FFFFFF" font-family="&quot;Open Sans&quot;, sans-serif" font-size="12" font-style="italic" lengthAdjust="spacing" textLength="50" x="338" y="187">&lt;&lt;person&gt;&gt;</text><image width="48" height="48" x="339" y="197" xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAIAAADYYG7QAAACD0lEQVR4Xu2YoU4EMRCGT+4j8Ai8AhaH4QHgAUjQuFMECUgMIUgwJAgMhgQsAYUiJCiQIBBY+EITsjfTdme6V24v4c8vyGbb+ZjOtN0bNcvjQXmkH83WvYBWto6PLm6v7p7uH1/w2fXD+PBycX1Pv2l3IdDm/vn7x+dXQiAubRzoURa7gRZWd0iGRIiJbOnhnfYBQZNJjNbuyY2eJG8fkDE3bbG4ep6MHUAsgYxmE3nVs6VsBWJSGccsOlFPmLIViMzLOB7pCVO2AtHJMohH7Fh6zqitQK7m0rJvAVYgGcEpe//PLdDz65sM4pF9N7ICcXDKIB5Nv6j7tD0NoSdM2QrU9Gg0ewE1LqBhHR3BBdvj2vapnidjHxD/q6vd7Pvhr31AwcY8eXMTXAKECZZJFXuEq27aLgQK5uLMohCenGGuGewOxSjBvYBqeG6B+Nqiblggdjnc+ZXDy+FNFpFzw76O3UBAROuXh6FoiAcf5g9eTvUgzy0nWg6I8cXHRUpg5bOVBCo+KDpFajOf23GgPme7RSQ+lacIENUgJ6gg1k6HjgOlqnLqip4tEuhv0hNEMXUD0clyXE3p6pZA0S2nnvTlXwLJEZWlb7cTQH1+USgTN4VhAenm/wea1OCAOmqo6fE1WCb9WSKBah+rbUWPWAmE2Rvk0ApiB45eOyNAzU8xcTvj8KvkKEoOaIYeHNA3ZuygAvFMUO0AAAAASUVORK5CYII="></image><text x="363" y="253" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 16px; font-weight: bold; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Cliente / Usuário Final</tspan></text><text x="363" y="291" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 14px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Pessoa que busca itens, define orçamento e lojas de preferência.</tspan></text></g><g class="person-man"><rect x="150" y="402" fill="#1168BD" stroke="#3C7FC0" width="962" height="87" rx="2.5" ry="2.5" stroke-width="0.5"></rect><text fill="#FFFFFF" font-family="&quot;Open Sans&quot;, sans-serif" font-size="12" font-style="italic" lengthAdjust="spacing" textLength="51" x="605.5" y="422">&lt;&lt;system&gt;&gt;</text><text x="631" y="440" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 16px; font-weight: bold; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">OrquestraCompras</tspan></text><text x="631" y="478" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 14px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Sistema web inteligente que recebe os critérios do usuário, dispara agentes de IA para buscar produtos em e-commerces e retorna combos otimizados.</tspan></text></g><g class="person-man"><rect x="150" y="589" fill="#999999" stroke="#8A8A8A" width="485" height="87" rx="2.5" ry="2.5" stroke-width="0.5"></rect><text fill="#FFFFFF" font-family="&quot;Open Sans&quot;, sans-serif" font-size="12" font-style="italic" lengthAdjust="spacing" textLength="101" x="342" y="609">&lt;&lt;external_system&gt;&gt;</text><text x="392.5" y="627" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 16px; font-weight: bold; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Sites de E-commerce Alvo</tspan></text><text x="392.5" y="665" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 14px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Plataformas de terceiros onde os agentes realizam as buscas de produtos.</tspan></text></g><g class="person-man"><rect x="735" y="589" fill="#999999" stroke="#8A8A8A" width="580" height="87" rx="2.5" ry="2.5" stroke-width="0.5"></rect><text fill="#FFFFFF" font-family="&quot;Open Sans&quot;, sans-serif" font-size="12" font-style="italic" lengthAdjust="spacing" textLength="101" x="974.5" y="609">&lt;&lt;external_system&gt;&gt;</text><text x="1025" y="627" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 16px; font-weight: bold; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Provedor de LLM / IA</tspan></text><text x="1025" y="665" dominant-baseline="middle" fill="#FFFFFF" style="text-anchor: middle; font-size: 14px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">APIs de Inteligência Artificial utilizadas para o parsing inteligente e raciocínio dos agentes.</tspan></text></g><g><line x1="479.5798922800718" y1="302" x2="686.3164179104477" y2="402" stroke-width="1" stroke="#444444" marker-end="url(#graph-30-arrowhead)" style="fill: none;"></line><text x="779.4481550952598" y="352" dominant-baseline="middle" fill="#444444" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Configura o ambiente desejado, orçamento e lojas, e visualiza os combos</tspan></text><text x="779.4481550952598" y="369" dominant-baseline="middle" fill="#444444" font-style="italic" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">[HTTPS / Web]</tspan></text><path fill="none" stroke-width="1" stroke="#444444" d="M796.1301518438178,489 Q845.4660807818179,539 993.4738675958188,589" marker-end="url(#graph-30-arrowhead)"></path><text x="1017.3020097198182" y="539" dominant-baseline="middle" fill="#444444" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Envia prompts e recebe análises estruturadas</tspan></text><text x="1017.3020097198182" y="556" dominant-baseline="middle" fill="#444444" font-style="italic" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">[API REST]</tspan></text><path fill="none" stroke-width="1" stroke="#444444" d="M676.7646420824295,489 Q642.1505721541566,539 538.3083623693379,589" marker-end="url(#graph-30-arrowhead)"></path><text x="758.5365022258837" y="539" dominant-baseline="middle" fill="#444444" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">Navega e extrai dados de produtos (preço, imagem, link)</tspan></text><text x="758.5365022258837" y="556" dominant-baseline="middle" fill="#444444" font-style="italic" style="text-anchor: middle; font-size: 12px; font-weight: normal; font-family: &quot;Open Sans&quot;, sans-serif;"><tspan dy="0" alignment-baseline="mathematical">[HTTP / Scraping]</tspan></text></g><text x="482.5" y="20">Diagrama de Contexto (Nível 1) - OrçaApp</text></g></svg>g mermaid-diagram-2026-08-10-214856.svg…]()


Descreva (geralmente em uma combinação de diagramas, tabelas e texto):

-   distribuição de um sistema para vários locais, ambientes,
    computadores, processadores, .., bem como conexões físicas entre
    eles

-   justificativas ou motivações importantes para esta estrutura de
    implantação

-   recursos de qualidade e/ou desempenho desta infraestrutura

-   mapeamento de artefatos de software para elementos desta
    infraestrutura

Para vários ambientes ou implantações alternativas, copie e adapte esta
seção do arc42 para todos os ambientes relevantes.

***\<Diagrama de Visão Geral\>***

Motivação

:   *\<explicação em forma de texto\>*

Características de Qualidade e/ou Desempenho

:   *\<explicação em forma de texto\>*

Mapeamento de Blocos de Construção para Infraestrutura

:   *\<descrição do mapeamento\>*

## Nível de Infraestrutura 2 {#_nível_de_infraestrutura_2}

Aqui você pode incluir a estrutura interna de (alguns) elementos de
infraestrutura do nível 1.

Copie a estrutura do nível 1 para cada elemento selecionado.

### *\<Elemento de Infraestrutura 1\>* {#_elemento_de_infraestrutura_1}

*\<diagrama + explicação\>*

### *\<Elemento de Infraestrutura 2\>* {#_elemento_de_infraestrutura_2}

*\<diagrama + explicação\>*

...​

### *\<Elemento de Infraestrutura n\>* {#_elemento_de_infraestrutura_n}

*\<diagrama + explicação\>*

# Conceitos Transversais {#section-concepts}

::: formalpara-title
**Conteúdo**
:::

Esta seção descreve globalmente, as principais regulamentações e ideias
de soluções que são relevantes em várias partes (= transversais) do seu
sistema. Esses conceitos geralmente estão relacionados a vários blocos
de construção. Eles podem incluir muitos tópicos diferentes, como

-   modelos, especialmente modelos de domínio

-   padrões de arquitetura ou *design patterns*

-   regras para usar tecnologia específica

-   principais decisões, geralmente técnicas, de natureza abrangente (=
    transversais)

-   regras de implementação

::: formalpara-title
**Motivação**
:::

Os conceitos formam a base para a *integridade conceitual*
(consistência, homogeneidade) da arquitetura. Portanto, eles são uma
contribuição importante para atingir as qualidades internas do seu
sistema.

Alguns desses conceitos não podem ser atribuídos a blocos de construção
individuais, por exemplo segurança ou proteção.

::: formalpara-title
**Forma**
:::

A forma pode ser variada:

-   documentos conceituais com qualquer tipo de estrutura

-   trechos ou cenários de modelos transversais usando notações das
    visualizações de arquitetura

-   amostra de implementações, especialmente para conceitos técnicos

-   referência ao uso típico de *frameworks* padrão (por exemplo, usando
    Hibernate para mapeamento de objeto/relacional)

::: formalpara-title
**Estrutura**
:::

Uma estrutura potencial (mas não obrigatória) para esta seção poderia
ser:

-   Conceitos de domínio

-   Conceitos de Experiência do Usuário (UX)

-   Conceitos de proteção e segurança

-   Padrões de arquitetura e *design patterns*

-   Estruturas internas

-   Conceitos de desenvolvimento

-   Conceitos operacionais

Observação: pode ser difícil atribuir conceitos individuais a um tópico
específico nesta lista.

![Tópicos possíveis para conceitos
transversais](images/08-concepts-EN.drawio.png)

::: formalpara-title
**Mais informações**
:::

Veja [Concepts](https://docs.arc42.org/section-8/) na documentação do
arc42.

## *\<Conceito 1\>* {#_conceito_1}

*\<explicação\>*

## *\<Conceito 2\>* {#_conceito_2}

*\<explicação\>*

...​

## *\<Conceito n\>* {#_conceito_n}

*\<explicação\>*

# Decisões Arquiteturais {#section-design-decisions}

::: formalpara-title
**Conteúdo**
:::

Decisões arquiteturais importantes, caras, de grande escala ou
arriscadas, incluindo justificativas. Com \"decisões\", queremos dizer
selecionar uma alternativa com base em critérios fornecidos.

Use seu julgamento para decidir se uma decisão de arquitetura deve ser
documentada aqui nesta seção central ou se é melhor documentá-la
localmente (por exemplo, dentro do modelo de caixa branca de um bloco de
construção).

Evite redundância. Consulte a seção 4, onde você já capturou as decisões
mais importantes da sua arquitetura.

::: formalpara-title
**Motivação**
:::

As partes interessadas do seu sistema devem ser capazes de compreender e
refazer suas decisões.

::: formalpara-title
**Forma**
:::

Várias opções:

-   ADR (Architecture Decision Record) ([Documentando Decisões de
    Arquitetura](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions))
    para cada decisão importante

-   Lista ou tabela, ordenada por importância e consequências ou:

-   mais detalhada em forma de seções separadas por decisão

::: formalpara-title
**Mais informações**
:::

Veja [Architecture Decisions](https://docs.arc42.org/section-9/) na
documentação do arc42. Lá você encontrará links e exemplos sobre ADR.

# Requisitos de qualidade {#section-quality-scenarios}

::: formalpara-title
**Conteúdo**
:::

Esta seção contém todos os requisitos de qualidade como árvore de
qualidade com cenários. Os mais importantes já foram descritos na seção
1.2. (objetivos de qualidade)

Aqui você também pode capturar requisitos de qualidade com menor
prioridade, que não criarão altos riscos quando não forem totalmente
alcançados.

::: formalpara-title
**Motivação**
:::

Como os requisitos de qualidade terão muita influência nas decisões
arquiteturais, você deve saber para cada parte interessada o que é
realmente importante para eles, concreto e mensurável.

::: formalpara-title
**Mais informações**
:::

Veja [Quality Requirements](https://docs.arc42.org/section-10/) na
documentação do arc42.

## Árvore de qualidade {#_árvore_de_qualidade}

::: formalpara-title
**Conteúdo**
:::

A árvore de qualidade (conforme definido no ATAM -- Architecture
Tradeoff Analysis Method) com cenários de qualidade/avaliação como
folhas.

::: formalpara-title
**Motivação**
:::

A estrutura de árvore com prioridades fornece uma visão geral para um
número às vezes grande de requisitos de qualidade.

::: formalpara-title
**Forma**
:::

A árvore de qualidade é uma visão geral de alto nível das metas e
requisitos de qualidade:

-   refinamento em forma de árvore do termo \"qualidade\". Use
    \"qualidade\" ou \"utilidade\" como raiz

-   um mapa mental com categorias de qualidade como ramos principais

Em qualquer caso, a árvore deve incluir links para os cenários da seção
a seguir.

## Cenários de Qualidade {#_cenários_de_qualidade}

::: formalpara-title
**Conteúdo**
:::

Concretização de requisitos de qualidade (às vezes vagos ou implícitos)
usando cenários (de qualidade).

Esses cenários descrevem o que deve acontecer quando um estímulo chega
ao sistema.

Para arquitetos, dois tipos de cenários são importantes:

-   Cenários de uso (também chamados de cenários de aplicação ou
    cenários de caso de uso) descrevem a reação do tempo de execução do
    sistema a um determinado estímulo. Isso também inclui cenários que
    descrevem a eficiência ou o desempenho do sistema. Exemplo: O
    sistema reage à solicitação de um usuário em um segundo.

-   Cenários de mudança descrevem uma modificação do sistema ou de seu
    ambiente imediato. Exemplo: Funcionalidade adicional é implementada
    ou requisitos para um atributo de qualidade mudam.

::: formalpara-title
**Motivação**
:::

Os cenários tornam os requisitos de qualidade concretos e permitem medir
ou decidir mais facilmente se eles são atendidos.

Especialmente quando você quer avaliar sua arquitetura usando métodos
como ATAM você precisa descrever suas metas de qualidade (da seção 1.2)
mais precisamente até um nível de cenários que podem ser discutidos e
avaliados.

::: formalpara-title
**Form**
:::

Tabular ou texto livre.

# Riscos e Débitos Técnicos {#section-technical-risks}

::: formalpara-title
**Conteúdo**
:::

Uma lista de riscos técnicos identificados ou débitos técnicos,
ordenadas por prioridade

::: formalpara-title
**Motivação**
:::

"Gerenciamento de riscos é gerenciamento de projetos para adultos" (Tim
Lister, Atlantic Systems Guild.)

Este deve ser seu lema para detecção e avaliação sistemáticas de riscos
e débitos técnicos na arquitetura, que serão necessárias para as partes
interessadas da gerência (por exemplo, gerentes de projeto,
proprietários de produtos) como parte da análise geral de riscos e
planejamento de medição.

::: formalpara-title
**Forma**
:::

Lista de riscos e/ou débitos técnicos, provavelmente incluindo medidas
sugeridas para minimizar, mitigar ou evitar riscos ou reduzir débitos
técnicos.

::: formalpara-title
**Mais informações**
:::

Veja [Risks and Technical Debt](https://docs.arc42.org/section-11/) na
documentação do arc42.

# Glossário {#section-glossary}

::: formalpara-title
**Conteúdo**
:::

Os termos técnicos e de domínio mais importantes que suas partes
interessadas usam ao discutir o sistema.

Você também pode ver o glossário como fonte para traduções se trabalhar
em equipes multilíngues.

::: formalpara-title
**Motivação**
:::

Você deve definir claramente seus termos, para que todas as partes
interessadas

-   tenham um entendimento idêntico desses termos

-   não usem sinônimos e homônimos

::: formalpara-title
**Forma**
:::

Uma tabela com colunas \<Termo\> e \<Definição\>.

Possivelmente mais colunas, caso precise de traduções.

::: formalpara-title
**Mais informações**
:::

Veja [Glossary](https://docs.arc42.org/section-12/) na documentação do
arc42.

+----------------------+-----------------------------------------------+
| Termo                | Definição                                     |
+======================+===============================================+
| *\<Termo-1\>*        | *\<definição-1\>*                             |
+----------------------+-----------------------------------------------+
| *\<Termo-2\>*        | *\<definição-2\>*                             |
+----------------------+-----------------------------------------------+
