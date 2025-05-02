# 2. Manipulação e pré-processamento de dados
Ao trabalharmos com dados, dificilmente encontraremos o chamado "caminho feliz". Ou seja, é improvável que os dados que coletamos estarão prontos para análise.

Voltando à comparação com a cozinha, na maioria das vezes precisaremos peneirar a farinha, remover as cascas e talos da cenoura ou até separar as gemas das claras para que obtenhamos o melhor bolo de cenoura possível. Essas ações possibilitam que nosso bolo tenha uma qualidade superior, mesmo que possam ser entendidas como uma alteração na condição original dos ingredientes.

No universo dos dados, chamamos essas "alterações" de manipulação ou pré-processamento. Assim como no nosso bolo de cenoura imaginário, a qualidade da nossa análise — e da nossa pesquisa como um todo — aumenta substancialmente quando realizamos essas ações.

Nesse módulo, exploraremos a manipulação e pré-processamento dos dados, abordando as etapas de tabulação, organização, limpeza e transformação.

## 2.1. Tabulação e organização de dados
Antes de aplicar análises, fazer inferências e construir gráficos, precisamos entender os nossos dados. E, para isso, é essencial que eles estejam devidamente organizados. Com um conjunto de dados organizados, estamos não só facilitando o nosso próprio trabalho, como também tornando esses dados reutilizáveis para outros pesquisadores. 

Uma das formas mais amplamente utilizadas para a tabulação e organização de dados em pesquisas é a planilha. Ainda que muito propensas a erros e ineficientes para algumas etapas do trabalho com dados, as planilhas cumprem bem o seu papel na hora de servir como estruturas para inserção e armazenamento de dados. E, quando somos **consistentes** na tabulação e na organização, estamos diminuindo ao máximo o número de erros que podem ocorrer (Freitag, 2021; Broman e Woo, 2018).







### Teoria:
"10 Mandamentos dos Dados" 
Princípios de estruturação de dados em planilhas
Padrões de codificação e classificação
Documentação adequada de dados e metadados

### Prática:
Padrões de codificação e classificação de dados qualitativos
Problemas comuns em planilhas de pesquisa e como evitá-los:
Nomenclatura de variáveis (sem acentos, espaços ou caracteres especiais)
Uma observação por linha, uma variável por coluna
Consistência na codificação de valores ausentes
Documentação de procedimentos de coleta e processamento

## 2.2. Introdução ao Pandas
Carregamento de dados (pd.read_csv(), pd.read_excel())
Inspeção básica (.head(), .info(), .describe())
Seleção de dados (.loc[], .iloc[], filtros booleanos)
Indexação e consulta (df[df['coluna'] > 10])

## 2.3. Limpeza Básica de Dados

### Teoria:		
Tipos comuns de problemas em dados de pesquisa
Estratégias de limpeza e transformação
Fluxo de trabalho para preparação de dados

### Prática:
Tratamento de valores ausentes (.dropna(), .fillna())
Remoção de duplicatas (.drop_duplicates())
Verificação de consistência (.value_counts())
Transformação de tipos de dados (.astype(), .apply())
Renomeação e reorganização de colunas (.rename(), .drop())

## 2.4. Transformação e Agregação de Dados
### Teoria:		
Conceitos de groupby e agregação
Criação de variáveis derivadas
Junção de diferentes fontes de dados

### Prática:
Agrupamento e resumo (.groupby().agg())
Criação de novas colunas (df['nova_coluna'] = df['coluna'] * 2)
Mesclagem de DataFrames (.merge(), .join())


---

<p align="right">
   <small>
   <strong>Ciência de Dados para Pesquisa </strong></br>
   <I> Módulo 1 - Introdução à Ciência de Dados e Python </I>
   </small>
</p>