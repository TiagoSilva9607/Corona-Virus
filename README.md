# Corona Vírus

O tema escolhido para o trabalho final da disciplina de Aprendizagem Automática II é o Corona Vírus e pretende-se dividir o trabalho nas seguintes fases:

- Análise do problema
- Planeamento do problema
- Análise dos dados
- Preparação dos dados
- Construção do modelo
- Visualização dos resultados

## Análise do problema

O Corona Vírus é uma doença infeciosa recente que tem causado graves consequências mundiais a nível económico, físico ou mental. Com este trabalho é pretendido termos uma melhor perceção sobre o tema e verificarmos a sua evolução em tempo real.

É importante referir que, todas as previsões efetuadas podem variar substancialmente devido ás medidas de prevenção e comportamento da sociedade nos diferentes países. As previsões efetuadas sejam a nível mundial ou de cada país apenas analisa o histórico de dados diários, sendo que, as diferentes medidas efetuadas por cada país podem melhorar ou piorar a evolução do vírus. O modelo não tem a capacidade de analisar as diferentes alterações na sociedade e, portanto, apenas analisa o passado.

## Planeamento do problema

Nesta fase o nosso foco é determinar os objetivos para o trabalho, bem como as vantagens na sua implementação.

Os objetivos estabelecidos para o trabalho são:

- Analisar os dados mundiais e os dados de cada país detalhadamente.
- Fazer previsões para os próximos 10 dias para cada país e a nível mundial.
- Apresentar gráficos com todos os resultados obtido.
- Criação de website capaz de mostrar toda a analise de dados efetuada.
- O website ser capaz de fazer previsões para cada país e a nível mundial.
- O website ser capaz de mostrar todas as previsões efetuadas.

##

## Base de dados

Toda a base de dados foi obtida no seguinte github:

[https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series](https://github.com/CSSEGISandData/COVID19/tree/master/csse_covid_19_data/csse_covid_19_time_series)

Os csv&#39;s utilizados foram:

- [Casos confirmados a nível global](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv) 
- [Mortes confirmadas a nível global](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv)
- [Recuperados confirmados a nível global](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_recovered_global.csv)

## Análise dos dados

- [Análise dos dados](https://github.com/jpbsa98/Corona-Virus/blob/master/DataAnalysisNotebook.ipynb)

## Preparação dos dados, construção do modelo Regressão Linear e Visualização dos resultados

- [Contrução do modelo e visualização de resultados](https://github.com/jpbsa98/Corona-Virus/blob/master/TestesOutrosModelos.ipynb)

## Preparação dos dados, construção do modelo LSTM e Visualização dos resultados

- [Contrução do modelo e visualização de resultados](https://github.com/jpbsa98/Corona-Virus/blob/master/LstmPredictionsNotebook.ipynb)

## Preparação dos dados, construção do modelo GRU e Visualização dos resultados

- [Contrução do modelo e visualização de resultados](https://github.com/jpbsa98/Corona-Virus/blob/master/GRUPredictionsNotebook.ipynb)



## Análise de resultados

Nesta secção vão ser analisados os modelos desenvolvidos ao longo do projeto. Além de analisar os resultados de cada um individualmente, irão ser feitas comparações entre os três modelos.

### Regressão linear

Os resultados obtidos na regressão linear não foram os desejados, o modelo mostrou dificuldade em efetuar previsões nos dias iniciais da pandemia acusando casos excessivos e consequentemente casos a menos nos casos finais. Uma melhor otimização dos hiperparâmetros no futuro poderia levar a melhores resultados.

Para uma melhor análise os resultados podem ser visualizados no - [Regressão Linear Predictions](https://github.com/jpbsa98/Corona-Virus/blob/master/TestesOutrosModelos.ipynb).


### LSTM's

Outra abordagem que o grupo utilizou foi o uso de Redes Neuronais Recorrentes(RNN's) que são capazes de interpertar sequências temporais, no entanto devido ao tamanho limitado do nosso dataset as LSTM's podem ter dificuldades em atingir o seu potêncial.

No entanto, os resultados mostraram-se bastante satisfatórios e superiores à regressão linear. Os resultados podem ser analisados em detalhe no - [Lstm Predictions](https://github.com/jpbsa98/Corona-Virus/blob/master/LstmPredictionsNotebook.ipynb).

### GRU's

Também nas redes RNN's e muito similares ás LSTM's existem as GRU's. As limitações encontradas para as LSTM's também se verificam nas GRU's e consequentemente os seus resultados foram bastante similares tanto na previsão de casos diários como na previsão de mortes. 

Para uma melhor análise os resultados podem ser visualizados no - [Gru Predictions](https://github.com/jpbsa98/Corona-Virus/blob/master/GRUPredictionsNotebook.ipynb).

### GRU's vs LSTM's

#### Previsão GRU's para os casos diários
![Previsão GRU's para os casos diários](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Gru_CasosDiarios.png)

#### Previsão LSTM's para os casos diários
![Previsão LSTM's para os casos diários](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Lstm_CasosDiarios.PNG)

Como se pode analisar, ambos os resultados são muito satisfatórios e equiparáveis entre eles. Para uma melhor análise comparar os resultados dos dois notebook's( previsão dos proximos 50 dias e previsão de mortes)

## Corona Alert(Web Site)


### Tutorial de utilização

#### Ambiente Anaconda

##### 1. Dependências

- conda install numpy
- conda install matplotlib
- conda install pandas
- conda install random
- conda install Flask
- conda install seaborn
- conda install sklearn
- conda install tensorflow
#### 2. Adicionar o projeto ao Flask

##### 2.1. Windows

cd C:\path\to\WEBapp\
set FLASK_APP=main.py

##### 2.2. Linux

cd C:\path\to\WEBapp\
export FLASK_APP=main.py

#### 3. Correr a aplicação

flask run

#### 4. Abrir a aplicação

Depois de correr a aplicação é necessário abrir o browser e colocar o seguinte endereço:

- [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

### Funcionalidades
O website construido permite aceder a todos os paises do mundo de modo dinámico e obter a totalidade de informações sobre os casos de corona virus nesse pais, além de gráficos personalizados para cada pais, é possivel também efetuar uma previsão para cada pais individualmente e obter o gráfico de previsão.
Deste modo o website permite obter uma experiencia inovadora e dinámica de interação com o nosso modelo LSTM e obter os resultados de modo simples e intuitivo

### Interface
### Página Inicial
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_world_wide.PNG)

#### Vários gráficos disponiveis
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_world_wide2.PNG)


### Página por país, exemplo Portugal
#### Página personalizada por país 
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_country.PNG)

### Pesquisa de paises dinámico
#### O nosso website contém dados de mais de 200 paises.
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_dynamic_search.PNG)


### Previsão dos casos
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_country_predicting.PNG)
#### Gráficos dinámicos de previsão para todos os países do mundo
![Website Preview](https://github.com/jpbsa98/Corona-Virus/blob/master/Images/Website_country_predicted.PNG)


