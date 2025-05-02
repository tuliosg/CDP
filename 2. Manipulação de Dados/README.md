# 2. Manipulação e pré-processamento de dados
Ao trabalharmos com dados, dificilmente encontraremos o chamado "caminho feliz". Ou seja, é improvável que os dados que coletamos estarão prontos para análise.

Voltando à comparação com a cozinha, na maioria das vezes precisaremos peneirar a farinha, remover as cascas e talos da cenoura ou até separar as gemas das claras para que obtenhamos o melhor bolo de cenoura possível. Essas ações possibilitam que nosso bolo tenha uma qualidade superior, mesmo que possam ser entendidas como uma alteração na condição original dos ingredientes.

No universo dos dados, chamamos essas "alterações" de manipulação ou pré-processamento. Assim como no nosso bolo de cenoura imaginário, a qualidade da nossa análise — e da nossa pesquisa como um todo — aumenta substancialmente quando realizamos essas ações.

Nesse módulo, exploraremos a manipulação e pré-processamento dos dados, abordando as etapas de tabulação, organização, limpeza e transformação.

## 2.1. Organização de dados
Antes de aplicar análises, fazer inferências e construir gráficos, precisamos entender os nossos dados. E, para isso, é essencial que eles estejam devidamente organizados. Com um conjunto de dados organizados, estamos não só facilitando o nosso próprio trabalho, como também tornando esses dados reutilizáveis para outros pesquisadores. 

Uma das formas mais amplamente utilizadas para a organização de dados em pesquisas é a planilha. Ainda que muito propensas a erros e ineficientes para algumas etapas do trabalho com dados, as planilhas cumprem bem o seu papel na hora de servir como estruturas para inserção e armazenamento. E, quando somos **consistentes** na tabulação e na organização, estamos diminuindo ao máximo o número de erros que podem ocorrer (Freitag, 2021; Broman e Woo, 2018).

Organizar os dados requer consistência e atenção. E, para explicar cada etapa de uma boa organização, elaboramos os **princípios de organização de dados**, tomando como base os "10 mandamentos dos dados" apresentados por Freitag (2021) e as recomendações de Broman e Woo (2018), em "Data Organization in Spreadsheets".

Cada um dos princípios traz recomendações, explicações, erros comuns e exemplos práticos de como podem ser utilizados na pesquisa. No âmbito desse curso, escolhemos o Google Planilhas para a apresentação inicial dos princípios e, mais adiante, veremos como aplicá-los também através da programação. O Google Planilhas foi escolhido por ser uma solução gratuita, com estrutura semelhante ao Excel e que permite o compartilhamento com outras pessoas através do Google Drive.

### Príncipios de organização de dados
* **Estruture a planilha no formato: ocorrências X variáveis**
    Na planilha, cada coluna representa uma variável e as linhas representam uma ocorrência daquela variável. A estrutura fica da seguinte forma:  

    *Tabela 1. Adaptado de Freitag (2021)*  
    | Variável | Variável | Variável |  
    |---|---|---|  
    | Ocorrência | Ocorrência | Ocorrência |  
    | Ocorrência | Ocorrência | Ocorrência |  
    | Ocorrência | Ocorrência | Ocorrência |  

    Assim, se coletarmos os nomes e as idades de um grupo de pessoas, ao tabularmos esses dados, devemos chegar em uma estrutura semelhante à da Tabela 2.

    *Tabela 2. Exemplo de organização de dados. Fonte: elaboração própria*
    | nome | idade |  
    |---|---|  
    | nome sobrenome 1 | idade 1 |  
    | nome sobrenome 2 | idade 2 |  
    | nome sobrenome 3 | idade 3 |  

* **Siga a ordem da planilha**
    Comece sempre pela primeira linha da primeira coluna da planilha, e não deixe linhas ou colunas em branco. 

* **Adote um padrão consistente para codificar variáveis categóricas**
    Conjuntos de dados muitas vezes possuem variáveis categóricas, como informações acerca de um participante ou categorias pertencentes à uma classificação/avaliação. Essas variáveis devem ter um padrão consistente para cada ocorrência. Se há informações sobre o grau de escolaridade, adote valores únicos para cada grau, por exemplo "médio completo" para quem possuir ensino médio completo, e "superior incompleto" para quem possuir ensino superior incompleto. Não escreva "Ensino médio" em algumas ocorrências, "Ensino Superior incompleto" em outras, adote **apenas um padrão** para cada caso e use-o.

* **Use um valor fixo para lidar com dados ausentes**
    Dados ausentes vão (ou melhor, não vão) aparecer e isso deve ser padronizado. Escolha uma forma para indicar que há um dado faltante naquele campo. Para casos onde o valor se perdeu e/ou não há nenhum registro dele, adote códigos como "NA" (comum para usuários de R), "Null" (comum para usuários de Python) ou até mesmo "valor ausente" para tornar mais legível. Mais uma vez, o importante é ser consistente.*
    \* *Dados faltantes não devem ser confundidos com zeros. Por exemplo: um participante que intencionalmente não respondeu uma questão não produz um dado faltante na nossa planilha e sim um zero (uma resposta em branco). Esses zeros entram como uma ocorrência de uma variável categórica, devendo possuir um padrão específico para cada caso.*

* **Estruture seus dados de forma consistente**
    A recomendação principal é manter todos os dados em apenas uma planilha — sem outros arquivos ou múltiplas páginas na mesma planilha. Porém, caso seja necessário ter múltiplos arquivos, mantenha uma estrutura consistente dos dados, com o mesmo padrão de codificações para os dados e para as colunas.




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