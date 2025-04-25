# 2. Manipulação de Dados
Objetivo: Ensinar boas práticas de organização de dados e manipulação básica usando pandas.

## 2.1. Tabulação de Dados e Padrões
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
