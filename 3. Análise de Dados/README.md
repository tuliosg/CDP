# 3. Análise de Dados
Objetivo: Aplicar estatística descritiva e medidas de associação em dados de pesquisa.

## 3.1. Estatística Descritiva
### Teoria:		
Medidas de tendência central e sua interpretação
Medidas de dispersão e sua relevância
Distribuições e normalidade
Visualização de estatísticas descritivas

### Prática:
Cálculo de média, mediana e moda (.mean(), .median(), statistics.mode())
Análise de dispersão (.std(), .var(), .quantile())
Contagem de frequências (.value_counts())
Geração de resumos estatísticos (.describe())
Teste de normalidade (scipy.stats.shapiro()) qq plot

## 3.2. Medidas de Associação
### Teoria:		
Correlação e causalidade: diferenças importantes
Tipos de correlação e quando usá-las
Concordância entre avaliadores em pesquisas linguísticas

### Prática:
Correlação de Pearson (df.corr(), scipy.stats.pearsonr())
Coeficiente Kappa (sklearn.metrics.cohen_kappa_score())
Testes de hipóteses simples (scipy.stats.ttest_ind())
Interpretação e visualização de correlações

## 3.3. Introdução à NLTK para Análise Textual Básica
### Teoria:		
Conceitos fundamentais de processamento de linguagem natural
Aplicações em pesquisas linguísticas e psicológicas
Limitações e considerações éticas

### Prática:
Tokenização e contagem de palavras (nltk.word_tokenize())
Análise de frequência de termos (nltk.FreqDist())
Identificação de n-gramas (nltk.ngrams())
