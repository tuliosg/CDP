# 2. Organização e pré-processamento
Ao trabalharmos com dados, dificilmente encontraremos o chamado "caminho feliz". Ou seja, é improvável que os dados que coletamos estarão prontos para análise.

Voltando à comparação com a cozinha, na maioria das vezes precisaremos peneirar a farinha, remover as cascas e talos da cenoura ou até separar as gemas das claras para que obtenhamos o melhor bolo de cenoura possível. Essas ações possibilitam que o bolo tenha uma qualidade superior, mesmo que possam ser entendidas como uma alteração na condição original dos ingredientes.

No universo dos dados, essas "alterações" constituem o que chamamos de organização e pré-processamento. Assim como no nosso bolo de cenoura imaginário, a qualidade da nossa análise — e da nossa pesquisa como um todo — aumenta substancialmente quando realizamos essas ações.

A organização é a etapa onde os dados são estruturados em formatos legíveis tanto por humanos quanto por máquinas. Nesse processo, seguimos uma série de padrões e regras para minimizar erros nas etapas posteriores. Já no pré-processamento, os dados são verificados, evidenciando qualquer possível problema, seja no conjunto de dados em si ou na tabulação. Além disso, é nessa etapa onde começamos a explorar e transformar os dados, entendendo quais variáveis e tipos de dados estão no conjunto, filtrando ocorrências, verificando valores, entre outras ações.

Nesse módulo, exploraremos a organização e pré-processamento dos dados, abordando princípios de organização, limpeza de dados e transformações. 

## 2.1. Organização de dados
Antes de aplicar análises, fazer inferências e construir gráficos, precisamos entender os nossos dados. E, para isso, é essencial que eles estejam devidamente organizados. Com um conjunto de dados organizados, estamos não só facilitando o nosso próprio trabalho, como também tornando esses dados reutilizáveis para outros pesquisadores. 

Uma das formas mais amplamente utilizadas para a organização de dados de pesquisa é a planilha. Ainda que muito propensas a erros e ineficientes para algumas etapas do trabalho com dados, as planilhas cumprem bem o seu papel na hora de servir como estruturas para inserção e armazenamento. E, quando somos **consistentes** na tabulação e na organização, estamos diminuindo ao máximo o número de erros que podem ocorrer (Freitag, 2021; Broman e Woo, 2018).

Organizar dados de forma eficaz exige consistência e atenção meticulosa. Para guiar este processo, desenvolvemos **os princípios de organização de dados**. Cada princípio apresenta recomendações práticas, explicações conceituais e alertas sobre erros comuns que pesquisadores frequentemente cometem durante essa etapa.

No âmbito desse curso, escolhemos o Google Planilhas para a apresentação inicial dos princípios e, mais adiante, veremos como aplicá-los também através da programação, usando a biblioteca `pandas`. O Google Planilhas foi escolhido por ser uma solução gratuita, com estrutura semelhante ao Excel e que permite o compartilhamento com outras pessoas através do Google Drive.

---

## Príncipios de organização de dados
Organizamos esses princípios em um formato inspirado nos "10 mandamentos dos dados" de Freitag (2021), incorporando também contribuições dos trabalhos de Brooman e Woo (2018), Wickham (2014), Borer et. al (2009) e do livro/comunidade The Turing Way (2025).

### **Estruture a planilha no formato: ocorrências X variáveis**  
Na planilha, cada coluna representa uma variável e as células representam as ocorrências/observações daquela variável. Dessa forma, cada linha é uma amostra. A estrutura esperada é:  

*Tabela 1. Adaptado de Freitag (2021)*  
| Variável | Variável | Variável |  
|---|---|---|  
| Ocorrência | Ocorrência | Ocorrência |  
| Ocorrência | Ocorrência | Ocorrência |  
| Ocorrência | Ocorrência | Ocorrência |  

Notem que **a primeira linha da planilha é o cabeçalho**, que deve sempre estar presente neste local. Assim, se coletarmos os nomes e as idades de um grupo de pessoas, ao tabularmos esses dados, devemos ter algo semelhante à Tabela 2.

*Tabela 2. Exemplo de organização de dados. Elaboração própria*
| nome | idade |  
|---|---|  
| Fulano da Silva | 38 |  
| Ciclana Alves | 62 |  
| Beltrano Batista | 79 |  

No exemplo, podemos notar uma consequência da adoção desse princípio: **as células correspondentes à uma mesma coluna devem conter apenas um tipo de informação** — a coluna `"nome"` contém apenas dados textuais, enquanto a coluna `"idade"` possui apenas dados numéricos.

Resumindo:
1. Uma coluna = uma variável;
2. Uma célula = uma informação;
3. Uma linha = uma amostra;
4. A primeira linha deve ser o cabeçalho.


### **Construa um cabeçalho limpo e descritivo**  
No cabeçalho ficam os rótulos das colunas, ou seja, o nome da variável contida naquela coluna. A nomenclatura presente no cabeçalho deve ser clara sobre o que será encontrado ali. Se estamos tratando das idades de pessoas, é indicado inserir rótulos como `idade` ou `idade_anos` no cabeçalho.

Os principais pontos de atenção na hora de definir essas nomenclaturas são:

1. **Não utilize acentuações, caracteres especiais ou espaços em branco**  
   Adote o underline "_" como espaço. Prefira escrever apenas com letras minúsculas. Elimine todos os acentos. Exemplificando: transforme `Nome e Sobrenome` em `nome_sobrenome`, `Classificação` em `classificacao` e `Anotação 1` em `anotacao_1`;  

2. **Adote uma nomenclatura curta e descritiva**  
    Por exemplo: ao trabalhar na tabulação de dados de uma aplicação de uma prova que tem data, hora de começar e hora de terminar, não nomeie as colunas como `Data`, `Começo` e `Final`. Troque para `data_aplicacao`, `hora_inicio` e `hora_fim`. Com essa transformação, o conteúdo das colunas é melhor descrito e com uma nomenclatura sucinta.


### **Cuidado com espaços em branco**  
Espaços em branco são um problema. Para além de células ou colunas inteiras em branco, o espaço em branco é um dos problemas mais comuns em planilhas de dados, o que acarreta em erros nos momentos de processamento e análise. É fundamental ter atenção na tabulação, tomando cuidado para não deixar espaços em branco em qualquer posição.  

Por exemplo: `"classificacao "`, `" classificacao"` e `"classificacao"`, podem até ser a mesma palavra mas são completamente diferentes para a máquina e, no momento de analisar esses dados, serão contadas como ocorrências distintas.


### **Adote um padrão para codificar variáveis categóricas**  
Conjuntos de dados muitas vezes possuem variáveis categóricas, como informações acerca de um participante ou categorias pertencentes à uma classificação/avaliação. Essas variáveis devem ter um **padrão consistente** para cada ocorrência.

Por exemplo, se foram tabuladas informações sobre o grau de escolaridade, adote valores únicos para cada grau, como `"médio completo"` para quem possuir ensino médio completo, e `"superior incompleto"` para quem possuir ensino superior incompleto. Não escreva `"Ensino médio"` em algumas ocorrências, `"Ensino Superior incompleto"` em outras. 

Adote **apenas um padrão** para cada caso e use-o. E lembre-se, letras maiúsculas e minúsculas são diferentes, então mantenha a codificação sempre idêntica em todos os aspectos.


### **Use um valor fixo para lidar com dados ausentes**  
Dados ausentes vão — ou melhor, não vão — aparecer e isso deve ser padronizado. Escolha uma forma para indicar que há um dado faltante naquele campo. Então, para casos onde o valor se perdeu e/ou não há nenhum registro dele, adote códigos como:

* `"NA"` (comum para usuários de R);
* `"Null"` (comum para usuários de Python);
* `"valor ausente"` (para tornar mais legível). 

O fundamental é manter a consistência, usando sempre o mesmo código em todo o conjunto de dados.

**Importante:** *Dados faltantes não devem ser confundidos com zeros. Por exemplo: um participante que intencionalmente não respondeu uma questão, não produz um dado faltante na nossa planilha e sim um zero (uma resposta em branco). Nesses casos, devemos codificar adequadamente essa resposta (ex.: `'não respondeu'`) em vez de marcá-la como dado ausente.*


### **Se quiser trabalhar nos dados, faça uma cópia**  
É comum encontrar casos de planilhas que alteraram os dados após a inserção de fórmulas ou mesclagem de células. Modificações assim podem ocasionar erros no momento da análise ou até mesmo a perda dos dados.

Evite esse problema lembrando do seguinte: o(s) arquivo(s) originais onde estão seus dados devem ser **intocáveis**. Não faça análises, manipulações, adição de fórmulas ou qualquer outro tipo de alteração na planilha original dos seus dados — se quiser trabalhar nos dados, faça uma cópia da planilha e modifique apenas ela.


### **Evite formatações na planilha**   
Deixe todas as funcionalidades do ambiente de lado. Apenas os dados devem estar na sua planilha, então, toda a formatação da planilha pode acabar atrapalhando. Esqueça as seguintes funções:

* Mesclar células;
* Usar fórmulas nas células;
* Usar formatação específica de células nos dados (como a formatação em data ou em moeda);
* Colorir, trocar fontes, adicionar bordas, entre outras formatações de estilo.  

A Figura 1 apresenta uma tabela com formatação, exibindo o que não deve ser feito. Já a Figura 2, traz como seria a tabela da Figura 1 seguindo o princípio apresentado.

*Figura 1. Exemplo de tabela formatada a ser evitada. Elaboração própria*
<figure>
   <img src="../2. Organização e pré-processamento/imgs/fig1-ex_tabela_formt.png" height="150">
</figure>

*Figura 2. Tabela da Figura 1 sem formatações. Elaboração própria*
<figure>
   <img src="../2. Organização e pré-processamento/imgs/fig2-ex_tabela_normal.png" height="110">
</figure>


Caso deseje construir uma planilha mais elaborada ou visivelmente bonita, siga o princípio anterior, crie uma cópia e trabalhe apenas na cópia.


### **Estruture seus dados de forma consistente**  
A recomendação principal é manter todos os dados em apenas uma planilha — sem outros arquivos ou múltiplas páginas na mesma planilha. Porém, caso seja necessário ter múltiplos arquivos, mantenha uma estrutura consistente dos dados, com o mesmo padrão de codificações para os dados e para as colunas. Se houver alguma coluna para identificação, seja de participante ou de experimento, mantenha ela em todos os arquivos de dados como uma forma de chave que liga todos os valores. Segue um exemplo:

*Tabela 3. Preferências de métodos de café. Elaboração própria*
| id_participante | metodo_cafe |  
|--|--|  
| TSG | v60 |  
| NSSC | prensa francesa |  

*Tabela 4. Avaliação de marcas de café. Elaboração própria*
| id_participante | marca_cafe | avaliacao |  
|---|---|---|  
| TSG | maraçá | 0 |  
| TSG | nelita | 2 |  
| TSG | 2 corações | 1 |  
| NSSC | maraçá | 0 |  
| NSSC | nelita | 4 |  
| NSSC | 2 corações | 2|  


Nas duas tabelas acima, o que "conecta" os dados é a coluna `id_participante`. Através dela, sabemos qual o método favorito de cada participante e também as notas para cada marca de café. Portanto, caso seja necessário integrar (unir) esses dados, essa será a coluna chave. 


### **Exporte, armazene e cuide dos seus dados**  
Para exportar, armazenar e cuidar dos dados de modo a preservá-los da melhor forma, alguns cuidados devem ser tomados:

1. Nomeie o(s) arquivo(s) seguindo um padrão consistente e as mesmas recomendações apresentadas na nomeação de colunas — nomenclaturas descritivas, sem espaços em branco e sem caracteres especiais ou símbolos. Estruturas como `"titulo-do-conjunto_autor_ano_versao.csv"` ou `"autor_titulo-do-conjunto_data-de-atualizacao.csv"` são recomendadas;
   
2. Adote formatos não proprietários e que armazenem apenas os dados na hora de exportar suas planilhas, como o *CSV* (valores separados por vírgula) ou *TSV* (valores separados por tabulações). Esses formatos são legíveis por praticamente todos os softwares disponíveis para leitura de planilhas e também por linguagens de programação;
   
3. Mantenha sempre um backup dos seus dados — preferencialmente em mais de um dispositivo ou na nuvem. Isso diminui a chance de perda dos dados. Assim, salve em diferentes dispositivos, deixe uma cópia em nuvens (como o Google Drive ou Dropbox) ou mantenha uma cópia em alguma plataforma de compartilhamento de repositórios (como o GitHub ou o OSF).


### **Registre os metadados**  
Metadados são informações que descrevem nossos conjuntos de dados, auxiliando na sua documentação e catalogação. O nível de detalhe dos metadados depende do tipo de projeto e de como ele será documentado. O recomendado, no contexto da organização de dados, é um arquivo separado da planilha — este pode ser um arquivo texto (txt), markdown (md) ou pdf — contendo os seguintes elementos:

1. **Informações sobre a aquisição dos dados**: foi uma coleta de dados, uma raspagem na internet, uma curadoria de dados já existentes? É a descrição sobre a origem daqueles dados e a metodologia envolvida nessa aquisição — data(s) de coleta, colaboradores, local de coleta, instrumentos utilizados, entre outras informações;
   
2. **Dicionário dos dados**: o propósito de um dicionário de dados é explicar o que cada uma das variáveis dos dados significa. O seu formato mais simples é:

| Variável | Nomenclatura da coluna | Descrição |  
|---|---|---|  
| Nome da variável | Rótulo adotado na coluna | Descrição da coluna | 

Como exemplo, voltemos a tabela 4:

*Tabela 5. Dicionário de dados da Tabela 4. Elaboração própria*

| Variável | Coluna | Descrição |  
|---|---|---| 
| ID do participante | `id_participante` | Código de identificação do participante |  
| Marca do café | `marca_cafe` | Nome da marca do café avaliado |  
| Avaliação do participante | `avaliacao` | Avaliação, de 0 a 10, do participante sobre o café |  

## Guia de referência rápida

Antes de avançarmos para a aplicação prática, vamos consolidar os dez princípios abordados. A tabela a seguir serve como um guia de referência rápida que poderá ser consultado durante suas atividades de organização de dados.

| Princípio | Descrição | Recomendação-chave |
|-----------|-----------|-------------------|
| **1. Estruture a planilha no formato: ocorrências X variáveis** | Cada coluna representa uma variável e cada linha representa uma amostra. A primeira linha deve ser o cabeçalho. | Uma coluna = uma variável; Uma célula = uma informação; Uma linha = uma amostra; A primeira linha = cabeçalho. |
| **2. Construa um cabeçalho limpo e descritivo** | O cabeçalho deve conter rótulos claros que descrevam o conteúdo de cada coluna. | Não utilize acentos, caracteres especiais ou espaços em branco. Adote o underline "_" como espaço, use letras minúsculas e nomenclaturas curtas e descritivas. |
| **3. Cuidado com espaços em branco** | Espaços em branco causam problemas no processamento e análise de dados. | Evite espaços em branco no início ou final de texto, em células ou colunas inteiras. Lembre-se que `"classificacao "`, `" classificacao"` e `"classificacao"` são interpretadas como entradas diferentes. |
| **4. Adote um padrão para codificar variáveis categóricas** | Variáveis categóricas devem seguir um padrão consistente em todas as ocorrências. | Escolha um único formato para cada categoria e mantenha-o idêntico em todo o conjunto de dados, respeitando inclusive letras maiúsculas e minúsculas. |
| **5. Use um valor fixo para lidar com dados ausentes** | Dados ausentes devem ser representados de forma padronizada. | Adote códigos como `"NA"`, `"Null"` ou `"valor ausente"` para indicar dados faltantes, mantendo consistência em todo o conjunto. |
| **6. Se quiser trabalhar nos dados, faça uma cópia** | Os arquivos originais de dados devem permanecer intactos. | Não faça análises, manipulações ou adição de fórmulas na planilha original — trabalhe sempre em uma cópia. |
| **7. Evite formatações na planilha** | Formatações podem atrapalhar o processamento dos dados. | Não mescle células, não use fórmulas, formatações específicas (data/moeda), cores, fontes diferenciadas ou bordas. |
| **8. Estruture seus dados de forma consistente** | Se necessário usar múltiplos arquivos, mantenha a mesma estrutura entre eles. | Mantenha o mesmo padrão de codificação em todos os arquivos e inclua colunas de identificação que permitam conectar os diferentes conjuntos de dados. |
| **9. Exporte, armazene e cuide dos seus dados** | Dados bem armazenados são dados preservados. | Nomeie arquivos com padrão consistente, use formatos não proprietários (CSV, TSV), e mantenha backups em múltiplos locais. |
| **10. Registre os metadados** | Metadados são informações sobre os dados que auxiliam na documentação. | Crie um arquivo separado contendo informações sobre a aquisição dos dados e um dicionário detalhado que explique cada variável. |

---

## 2.2. Aplicando os princípios
Para fixarmos ainda mais esses princípios na mente de vocês, preparamos algumas práticas. Nelas, vamos observar planilhas com erros comuns e aplicar algumas das recomendações vistas aqui, organizando os dados da melhor forma.

O contexto dos exercícios é: uma escola deseja avaliar mais rapidamente o desempenho dos discentes e, para isso, começou a adotar a prática de tabular os dados das provas, visando uma análise automática desses dados. Nas planilhas, inseriram os dados de três discentes, suas informações e seus respectivos desempenhos nas provas de português e matemática. O problema é que diversas pessoas tabularam esses dados, cada um do seu jeito, e a coisa desandou. 

As informações que temos são:
* Discentes: os discentes se chamam Ana, Bruno e Carlos;
* Ano escolar: todos são do 6º ano;
* Turma: Ana e Carlos são da Turma A e Bruno é da Turma B;
* Presença nas provas: Ana e Bruno fizeram todas as provas (português e matemática), e Carlos fez a prova de matemática porém faltou na de português.

O trabalho aqui é organizar cada uma das planilhas abaixo seguindo os princípios apresentados.

1. [**Problemas de estrutura**](../2.%20Organização%20e%20pré-processamento/planilhas/pratica-estruturacao.xlsx): Alguém foi sucinto demais na hora da tabulação e acabou juntando mais ocorrências do que deveria;
2. [**Cabeçalho extenso**](../2.%20Organização%20e%20pré-processamento/planilhas/pratica-cabecalho.xlsx): Uma planilha onde o padrão do cabeçalho é não ter padrão;
3. [**Variáveis diversas**](../2.%20Organização%20e%20pré-processamento/planilhas/pratica-nomenclatura-variaveis.xlsx): Nessa planilha, cada ocorrência de variável parece ser única de tão diferentes que são suas codificações;
4. [**Dado ausente ou faltante?**](../2.%20Organização%20e%20pré-processamento/planilhas/pratica-dado-ausente.xlsx): Notaram a falta de Carlos na prova de português e acrescentaram na planilha.

> Todas as planilhas utilizadas nos exercícios práticos estão na pasta 📁 [**planilhas**](../2.%20Organização%20e%20pré-processamento/planilhas/).


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
   <I> Módulo 2 - Organização e pré-processamento </I>
   </small>
</p>