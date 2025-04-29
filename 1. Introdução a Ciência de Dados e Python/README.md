# 1. Introdução à Ciência de Dados e Python
O primeiro capítulo aborda uma introdução aos principais conceitos na área de dados e também ao Python, a linguagem de programação que será utilizada ao longo do curso.

## 1.1. Dados: o que são, de onde vêm e por que são importantes?
Começando pelo principal objeto de estudo desse curso, os "dados"... bem, mas o que são "dados"?  
A depender de onde essa pergunta seja feita, as respostas serão diferentes mas, em sua maioria, trarão elementos semelhantes, como: 
* Resultados de medições;
* Observações documentadas;
* Valores.

Ainda que haja uma gama de possíveis descrições para o que são dados, podemos resumir da seguinte forma:
> Dados são uma coleção de valores (ou unidades básicas de significado) que transmitem informações.

Apeasr da presença da palavra "valores" na definição, dados não devem ser entendidos apenas como números. A seguir vão alguns exemplos de dados:

* As alturas, em metros, das pessoas que participaram desse curso;
* A cor da pelagem dos gatos que vivem na UFS;
* Os cafés favoritos das pessoas que trabalham no LAMID.

Ao longo do curso, vocês serão estimulados a transpor o conhecimento visto aqui para a sua própria realidade e pesquisa. Então, vamos começar pensando: **quais são os dados da sua pesquisa?**  

Para ajudar, deixo aqui uma lista com alguns dados que "aparecem" frequentemente nas pesquisas do laboratório:

* _Corpus_: o conjunto de textos ou registros orais em uma determinada língua que serve como base para diversas análises;
* Rastreamento ocular: o registro da posição dos olhos de uma pessoa e o caminho que eles percorreram em um texto ou imagem;
* Entrevistas sociolinguísticas: dados de fala, gestos e posições.

O universo dos dados é gigantesco e diverso. Não se assustem, admirem a vastidão e descubram, a seguir, como começar a desbravá-lo!

### 1.2. Ciência de Dados
É da necessidade de explorar essa vastidão que emerge a Ciência de Dados (CD), a área que engloba as teorias, conceitos, metodologias e ferramentas necessárias para aprender com ou sobre os dados[^1].

[^1]: https://alan-turing-institute.github.io/rds-course/modules/m1/1.1-WhatIsDataScience.html#what-is-research-data-science

A única certeza que temos sobre a Ciência de Dados é que não há um consenso sobre sua definição ou sobre o corpo de conhecimentos que a compõe. Como apontado por Grus (2016), *“[...] basicamente não importa como você define data science, pois você encontrará praticantes para quem a definição está total e absolutamente errada.”*

Mas, no contexto desse curso, vamos definir da seguinte forma: **Ciência de Dados é a área do conhecimento que nos capacita a aprender com e sobre dados**.

É através dos conhecimentos que a ciência de dados oferece que nos tornamos capazes de:
* Encontrar e distinguir o que são dados e quais nos interessam;
* Organizar dados da melhor forma;
* Explorar os dados, suas características e peculiaridades;
* Entender quais informações aqueles dados transmitem;
* Transformar essas informações em conhecimento.

Desenvolver essas habilidades exige tempo e dedicação ao estudo da ciência de dados, então, vamos dar o pontapé inicial dessa trilha e apresentar os "equipamentos" que servirão de base para esse estudo. 

Começaremos pela programação, um conhecimento técnico que nos habilita a ensinar computadores e resolver problemas utilizando-os. É através dela que implementamos muitas das técnicas e soluções em ciência de dados. Assim, a próxima seção é dedicada a explicação das bases da programação.

## 1.3. Introdução à Programação
Existem diversas formas de trabalhar com ciência de dados, e algumas delas são conhecidas, como o Excel e o SPSS. Porém, o foco desse curso não é somente no ferramental, ou seja, nos softwares prontos que podemos utilizar, e sim no conjunto completo: teorias, modos de pensar, técnicas, ferramentas e aplicações.

**É aí onde entra a programação.**

Uma pergunta comum é, *"Por que aprender a programar se muitos softwares já fazem o que eu preciso?"*.  

Isso não só é uma dúvida válida como também implica em decisões importantes. Às vezes, um trabalho pode ser iniciado e finalizado somente no Excel — inclusive, veremos esse tipo de ocorrência ao longo do curso —, e isso é ótimo. Se a pessoa responsável souber e entender que aquela tarefa só precisa do Excel e mais nada, ela acabou de aplicar um dos conhecimentos da ciência de dados — saber o que usar para cada ocasião.

Contudo, diversos problemas vão requerer uma flexibilidade muito maior, ou terão etapas mais longas que só com um software as coisas não vão ser resolvidas. Casos comuns são:

* Quantidade massiva de dados;
* Construção de gráficos de forma dinâmica;
* Corrigir/limpar/transformar muitos dados de uma só vez;
* Implementar suas próprias funções.

Além disso, a ciência de dados se manifesta muitas vezes através da programação. É programando que a gente consegue implementar novos métodos de análise, construir novas formas de coletar dados, organizar diversos arquivos mais rapidamente (todas essas mágicas que vocês já devem ter visto Profª Raquel ou Prof Julian fazendo).

### 1.3.1. Cozinhando com programação
Programas consistem em uma série de etapas para solucionar um dado problema, e a organização dessas etapas se dá através de um algoritmo. Uma das analogias mais comuns para introduzir o conceito de programação — e de algoritmo — é:
> Um algoritmo nada mais é do que uma receita.

Ao programar, você "ensina" o computador a realizar as tarefas que você deseja, assim, o programa que você escreve é como uma receita que a máquina vai seguir. A tabela abaixo traz os conceitos por trás de uma boa receita:

| Na receita | Na programação |  
|:----------|:--------------|  
| pote, xícara | variáveis |  
| ingredientes | valores das variáveis |  
| secos, molhados | tipos de dados (os tipos das variáveis) |  
| ações da receita (sovar, misturar, assar)     | funções |  
| repetições na receita (bater por 30 min) | loops |  
| fogão, batedeira | bibliotecas |  
| a receita pronta | a saída ou resultado do programa |

Vamos entender um pouco melhor cada um desses pedaços do nosso bolo:
* **Variável**: uma variável pode ser entendida como um lugar onde algo será guardado/armazenado. Por isso que na receita as variáveis são os potes ou os utensílios de medida.
   > Ex.: Coloque 300g de farinha de trigo. Ao armazenar esses 300g de farinha de trigo em uma cumbuca, você acabou de usar a variável cumbuca e agora o valor dela é "300g de farinha".

* **Valores das variáveis**: o valor de uma variável é aquilo que está sendo armazenado na variável naquele momento. 
   > Ex.: Enquanto não enchermos uma xícara com óleo, a variável xícara não tem nenhum valor. Mas, ao despejar o óleo, a xícara passa a ter o valor "150mL de óleo".

* **Tipos de dados**: cada variável pode armazenar alguns tipos de dados, ou seja, os valores delas tem uma característica específica. Na programação podemos definir, de forma básica, que os tipos de dados são: textos e números. Esses tipos "básicos" são ramificados, gerando tipos mais específicos — e restritos —, e também podem ser mais elaborados, gerando as chamadas **estruturas de dados**.
   > Ex.: Na receita, definimos que os tipos de dados (ou os tipos aceitáveis para as variáveis) seriam secos e molhados. Assim, sabemos qual o tipo de dado armazenado em cada variável, o que já implica nos tipos de operações que podemos fazer com elas.

* **Funções**: uma função pode ser definida como uma estrutura que recebe uma entrada, executa uma operação com essa entrada e gera uma saída. Assim como na matemática, podemos pensar em uma função que realiza somas, então precisamos de duas varíaveis — nesse caso, dois números — para somarmos e o resultado da operação é a nossa saída.
   > Ex.: Na nossa receita, as funções são as ações que vamos fazer com o conteúdo de algumas variáveis. Então, na função `bater`, podemos inserir todos os ingredientes secos e molhados como entrada, e o resultado — a saída — será uma mistura homogênea.

* **Loops**: os loops são estruturas que permitem a repetição de ações. Essas estruturas são construídas pensando em reduzir o nosso trabalho no momento de programar, então, ao invés de chamarmos uma função 30 vezes, podemos colocar a função em um loop e pedir para executá-la 30 vezes.
   > Ex.: Voltemos à função `bater`. Para ela funcionar, precisamos misturar todos os ingredientes em um recipiente só, então, precisamos repetir essa ação de `misturar`. O loop entra justamente para evitar escrever "misture a farinha de trigo, misture a manteiga, misture o ovo..."". Com os loops, podemos criar algo tipo `para cada ingrediente disponível: misture`. Assim, entendemos que vamos misturar todos os ingredientes selecionados.

* **Bibliotecas**: semelhante às bibliotecas reais, elas são utilizadas para "pegarmos" um determinado conhecimento e usar no nosso programa. Muitas vezes, as funções que queremos utilizar já foram construídas, então precisamos importar a biblioteca que contêm essas funções e usá-las. Em resumo, bibliotecas são conjuntos de scripts (algoritmos) já prontos que podem ser reutilizados e aplicados em diferentes programas.
   > Ex.: Imaginem ter que criar um forno do zero apenas para assar o nosso bolo... muito complicado. É por isso que podemos "importar" a função `assar` da biblioteca `forno`. Assim, com a nossa massa pronta, pegamos emprestada essa função do forno e aplicamos na nossa produção.

* **Saída**: programas são construídos para que tragam algum resultado, e esse resultado pode ser chamado de **saída** do programa. A saída nada mais é do que o resultado final da execução de todas as operações.
   > Ex.: Nada melhor que o bolo pronto. Após todas as definições das variáveis, aplicação das funções, execuções de loops, utilizar funções de bibliotecas, temos finalmente o resultado: um bolo quentinho para comer com café.

Partindo desses conceitos iniciais, começamos a entender melhor como funciona a programação e os programas. Agora, temos que detalhar alguns dos conceitos básicos, principalmente os que carregam "dados" nos seu nomes, pois são eles que vocês verão com maior frequência.

### 1.3.2. Tipos e estruturas de dados
Aprofundando o que foi visto na seção anterior, chegamos nos tipos e nas estruturas de dados utilizadas na programação e na ciência de dados.

Os tipos de dados definem a categoria de cada dado. E, para cada categoria, temos algumas especificações, como os limites ou o domínio daquele conjunto. Vejam a seguir:

* **Dados numéricos**
  * **Inteiros**: são os números, positivos e negativos, que não possuem casas decimais e o zero.
      > 0, 1, 2, 3...
  * **Decimais** (números com ponto flutuante): são os números que possuem casas decimais.
      > 1.5, 2,68, 3.14... 

* **Dados booleanos**: são aqueles que podem assumir apenas dois valores, representando "verdadeiro" ou "falso".
      > (False, True), (0, 1), (Falso, Verdadeiro) 

* **Caracteres**
  * **Strings** (cadeias de caracteres): as strings são qualquer conjunto de caracteres (letras, símbolos, números), e elas são encontradas entre aspas.
      > "Essa é uma string", "Esse curso dura 15 horas", "Olá :)"

Ao unirmos alguns dados, sejam de tipos iguais ou diferentes, precisamos de meios de organizá-los, e é aí onde entram as estruturas de dados. São elas que fornecem as formas que podemos agrupar um ou mais dados. Dentre as estruturas mais comuns estão:

* Lista: uma lista é uma estrutura de dados unidimensional que armazena dados de mesmo tipo. 
  > Um exemplo comum é a lista de compras que algumas pessoas fazem para ir ao mercado. Lista: feijão, arroz, óleo, pão...

*IMAGEM*

* Dicionário: o dicionário é uma estrutura de dados construída no modo "chave: valor". Essa estrutura segue o formato de um dicionário de palavras, onde encontramos "palavra: significado". O seu uso é muito comum na elaboração de tabelas e no armazenamento de dados textuais.
  > Na programação, os dicionários ficam entre chaves: {"palavra": "significado"} .

*IMAGEM*

* Tabela: apesar de não ser um formato nativo da programação, essa estrutura é de suma importância na área de dados. As tabelas são estruturas bidimensionais formadas por linhas e colunas que podem armazenar diversos tipos de dados. Tabelas podem ser entendidas como a união de várias listas, sendo cada lista uma coluna e os seus valores as linhas correspondentes. Um local onde tabelas são usadas como estrutura de dados padrão é em softwares de planlihas, como Google Planilhas ou Excel. Diversas bibliotecas de manipulação de dados — como o pandas, que aparecerá no próximo módulo — implementam esse tipo de estrutura[^2].

[^2]: Apesar das tabelas não serem nativas algumas linguagens de programação implementam matrizes, que são estruturas no formato linhas x colunas que armazenam dados numéricos.

*IMAGEM*

Ao somarmos as bases da programação que vimos com as especificações de tipos e estruturas de dados, podemos começar a pôr a mão na massa. Na próxima seção, será apresentado o ambiente do Google Colab, o local onde nós vamos desenvolver todos os códigos do curso e, após as devidas apresentações, terão alguns códigos práticos para assimilarmos o conteúdo visto até aqui.

#### Prática
* Criação de variáveis para armazenar dados de pesquisa
* Construção de listas, e dicionários e dataframes
* Implementação de loops simples para processamento repetitivo
* Desenvolvimento de funções básicas

## 1.4. Google Colab
O Google Colaboratory, comumente chamado de Colab, é um serviço da Google que permite a criação de Jupyter Notebooks sem a necessidade de configurações para uso e sem custos.

E o que seria um Jupyter Notebook?  
O Jupyter Notebook é um ambiente web de programação interativa estruturado em células, permitindo a inserção de código, texto, gráficos e imagens. O principal componente interacional do notebook é a execução dos blocos de código de maneira indepentende. Além disso, por conta dos blocos de texto (e outros recursos visuais), é muito mais fácil apresentar e explicar os códigos desenvolvidos. A Figura 1 apresenta uma visão geral de um Notebook no Colab.

*Figura 1. Visão geral. Fonte: Autoria própria*
<figure>
   <img src="../1. Introdução a Ciência de Dados e Python/imgs/visao_geral_colab.png" height="250">
</figure>

As Figuras 2 e 3 exibem alguns dos recursos disponíveis no Notebook.

*Figura 2. Célula de código. Fonte: https://osf.io/un8cw/*
<figure>
   <img src="../1. Introdução a Ciência de Dados e Python/imgs/ex1_calculo-no-colab.png" height="250">
</figure>

*Figura 3. Plotagem de gráfico. Fonte: https://osf.io/un8cw/*
<figure>
   <img src="../1. Introdução a Ciência de Dados e Python/imgs/ex2_plot.png" height="250">
</figure>




#### Teoria
* Vantagens do notebook para documentação de pesquisa
* Estrutura de células de código e markdown

#### Prática
* Navegação básica no Colab
* Execução de células de código
* Formatação de texto com markdown para documentar análises
* Compartilhamento de notebooks com colaboradores

## 1.5. Princípios de Ciência Aberta e Reprodutibilidade - Introdução
* O que é ciência aberta e por que é importante
* A crise de reprodutibilidade nas ciências
* Benefícios da pesquisa transparente e reprodutível





<p align="right">
    <small>
    <strong>Ciência de Dados para Pesquisa </strong></br>
    <I> Módulo 1 - Introdução à Ciência de Dados e Python </I>
    </small>
</p>
