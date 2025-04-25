# 1. Introdução à Ciência de Dados e Python
O primeiro capítulo aborda uma introdução aos principais conceitos na área de dados e também ao Python (a linguagem de programação que será utilizada ao longo do curso).

## 1.1. Dados: o que são, de onde vêm e por que são importantes?
Começando pelo principal objeto de estudo desse curso, os "dados"... bem, mas o que são "dados"?
A depender de onde essa pergunta seja feita, as respostas serão diferentes mas, em sua maioria, trarão elementos semelhantes, como: 
* Resultados de medições;
* Observações documentadas;
* Valores.

Ainda que haja uma gama de possíveis descrições para o que são dados, podemos resumir da seguinte forma:
> Dados são uma coleção de valores (ou unidades básicas de significado) que transmitem alguma informação. Assim, um dado é um valor individual dessa coleção.

Não pensem que por ter escrito "valores" que dados são apenas números. A seguir vão alguns exemplos de dados:
* As alturas, em metros, das pessoas que participaram desse curso;
* A cor da pelagem dos gatos que vivem na UFS;
* Os cafés favoritos das pessoas que trabalham no LAMID.

Ao longo do curso, vocês serão estimulados a transpor o conhecimento visto aqui para a sua própria realidade, para a sua própria pesquisa. Então, vamos começar pensando: **o que são os dados na sua pesquisa?**  
Para ajudar, vou deixar aqui uma lista com alguns dados que "aparecem" frequentemente nas pesquisas do laboratório:

* _Corpus_: é o conjunto de textos ou registros orais em uma determinada língua e que serve como base para diversas análises. Lembram da Linguística de corpus?;
* Rastreamento ocular: a posição dos olhos de uma pessoa e o caminho que eles percorreram em um texto ou imagem;
* Entrevistas sociolinguísticas: dados de fala, gestos e posições.

O universo dos dados é gigantesco e diverso. Não se assustem, admirem a vastidão!

### 1.2. Ciência de Dados
É desse contexto que emerge a Ciência de Dados, a área que engloba as teorias, conceitos, metodologias e ferramentas necessárias para aprender com ou sobre os dados[^1].
[^1]: https://alan-turing-institute.github.io/rds-course/modules/m1/1.1-WhatIsDataScience.html#what-is-research-data-science

A única certeza que temos sobre a Ciência de Dados é que não há um consenso sobre sua definição ou sobre o corpo de conhecimentos que a compõe. Como apontado por Grus (2016), *“[...] basicamente não importa como você define data science, pois você encontrará praticantes para quem a definição está total e absolutamente errada.”*

No contexto desse curso, **Ciência de Dados é a área do conhecimento que nos capacita a aprender com dados**.

É através dos conhecimentos que a Ciência de Dados nos oferece que seremos capazes de:
* Encontrar e distinguir o que são dados e quais nos interessam;
* Organizar esses dados da melhor forma;
* Explorar os dados, suas características e peculiaridades;
* Entender quais informações aqueles dados transmitem;
* Transformar essas informações em conhecimento.

*Acrescentar exemplos de pesquisas do LAMID que têm uso ou aplicações de dados*

## 1.3. Introdução à Lógica de Programação
Existem algumas formas de fazer ciência de dados, e muitas delas são conhecidas, como o Excel, o SPSS e a linguagem R. E o foco desse curso não é necessariamente no ferramental, ou seja, nos programas/softwares que podemos utilizar para isso e sim no conjunto completo: teorias, modos de pensar, ferramentas e aplicações.

**É aí onde entra a programação.**

Uma pergunta comum é *"Por que aprender a programar se muitos softwares já fazem o que eu preciso?"*.  
Isso não só é uma dúvida válida como também implica em decisões importantes. As vezes um trabalho pode ser iniciado e finalizado somente no Excel - inclusive veremos esse tipo de ocorrência ao longo do curso -, e isso é ótimo. Se a pessoa responsável souber e entender que aquela tarefa só precisa do Excel e mais nada, ela acabou de aplicar um dos conhecimentos da ciência de dados - saber o que usar para cada ocasião (é o famigerado "não vamos matar uma barata com um tiro").

Contudo, diversos problemas vão requerer uma flexibilidade muito maior, ou terão etapas mais longas que só com um software as coisas não vão ser resolvidas. Casos comuns são:

* Quantidade massiva de dados (um dia abram uma planilha de rastreio ocular ou de gestos faciais);
* Construção de gráficos de forma mais dinâmica;
* Corrigir/limpar/transformar muitos dados de uma só vez;
* Implementar suas próprias funções - as vezes construir uma função no Excel pode ser muito mais complexo do que simplesmente programar.

Além disso, a ciência de dados se manifesta muitas vezes através da programação. É programando que a gente consegue implementar novos métodos de análise, construir novas formas de coletar dados, organizar diversos arquivos mais rapidamente (todas essas mágicas vocês já devem ter visto Profª Raquel ou Prof Julian fazendo).

### 1.3.1. Cozinhando com programação
Uma das analogias mais comuns para introduzir o conceito de programação (e de algoritmo) é que:
> Um algoritmo nada mais é do que uma receita.

Ao programar, você "ensina" o computador a realizar as tarefas que você deseja, assim, o programa que você escreve é como uma receita. 
| Na receita | Na programação |  
|:----------:|:--------------:|  
| pote, xícara | variáveis |  
| ingredientes | valores das variáveis |  
| secos, molhados | tipos de dados (os tipos das variáveis) |  
| ações da receita (sovar, misturar, assar)     | funções |  
| repetições na receita (bater por 30 min) | loops |  
| fogão, batedeira | bibliotecas |  
| a receita pronta | a saída ou resultado do programa |

Vamos entender um pouco melhor cada um desses pedaços do nosso bolo (programa):
* Variável: uma variável pode ser entendida como um lugar onde algo será guardado/armazenado. Por isso que na receita as variáveis são os potes ou os utensílios de medida.
   > Exemplo: Coloque 300g de farinha de trigo. Ao armazenar esses 300g de farinha de trigo em uma cumbuca, você acabou de usar a variável cumbuca e agora o valor dela é "300g de farinha".

* Valores das variáveis: o valor de uma variável é aquilo que está sendo armazenado na variável naquele momento. 
   > Exemplo: Enquanto não enchermos uma xícara com óleo, a variável xícara não tem nenhum valor. Mas, ao despejar o óleo, a xícara passa a ter o valor "150mL de óleo".

* Tipos de dados: cada variável pode armazenar alguns tipos de dados, ou seja, os valores delas tem uma característica específica. Na programação podemos definir, de forma básica, que os tipos de dados são: textos e números

#### Teoria
* Variáveis e tipos de dados (inteiros, strings, booleanos) - Variáveis como "caixas" para armazenar informações (analogias com conceitos linguísticos)
* Estruturas de dados básicas (listas, dicionários, dataframes)
* Loops (for, while) e condicionais (if-else) como ferramentas de decisão e repetição
* Funções como "receitas" para tarefas repetitivas em pesquisa

#### Prática
* Criação de variáveis para armazenar dados de pesquisa
* Construção de listas, e dicionários e dataframes
* Implementação de loops simples para processamento repetitivo
* Desenvolvimento de funções básicas

## 1.4. Ambiente de Trabalho: Google Colab e Jupyter Notebook
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





---
<small>
<strong>Ciência de Dados para Pesquisa</strong> | 
Edição especial: <I>Ciências Humanas</I>  <br>
Organizador: Túlio Gois
</small>
