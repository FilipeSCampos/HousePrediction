# Projeto de Análise e Modelagem de Dados Imobiliários

Este projeto tem como objetivo realizar a análise exploratória e a modelagem preditiva de preços de imóveis com base em um conjunto de dados de imóveis na Califórnia. Serão utilizadas as bibliotecas Pandas, NumPy, scikit-learn, Seaborn e Matplotlib para manipulação de dados, visualização e treinamento de modelos de regressão.

## Descrição

O projeto está estruturado em um único arquivo Python, `House_Price_Prediction.ipynb`, que contém o código responsável pela análise dos dados, pré-processamento, treinamento dos modelos de regressão linear, Random Forest e XGBoost, além de avaliar o desempenho desses modelos em relação a métricas como MSE, MAE e R².

### Dados

O conjunto de dados é armazenado no arquivo `housing.csv` e contém informações sobre os imóveis, incluindo características como o número de quartos, o número de banheiros, a renda média da área, a proximidade do oceano, entre outros.

### Análise e Pré-processamento

- Carregamos os dados do arquivo CSV usando a biblioteca Pandas e realizamos uma análise exploratória para entender a distribuição das variáveis e identificar valores ausentes.

- Realizamos o pré-processamento dos dados, removendo as linhas com valores ausentes usando o método `dropna()` do Pandas.

- Aplicamos uma transformação logarítmica em algumas das colunas numéricas para reduzir a escala e tornar a distribuição mais próxima da normal.

- Transformamos a coluna categórica 'ocean_proximity' em variáveis binárias usando o método `pd.get_dummies()` do Pandas.

### Modelagem Preditiva

Neste projeto, utilizamos três modelos de regressão diferentes:

#### 1. Regressão Linear

A regressão linear é um modelo que visa estabelecer uma relação linear entre a variável dependente (preço do imóvel) e as variáveis independentes (outras características do imóvel). O modelo tenta encontrar a melhor linha reta que se ajusta aos dados e é treinado através do método dos mínimos quadrados.

#### 2. Random Forest

O Random Forest é um modelo de aprendizado de máquina baseado em árvores de decisão. Ele cria várias árvores de decisão durante o treinamento e faz a previsão combinada dessas árvores para obter um resultado final mais robusto e geralmente mais preciso.

#### 3. XGBoost

O XGBoost (Extreme Gradient Boosting) é um algoritmo de aprendizado de máquina baseado em gradient boosting. Ele é conhecido por sua eficiência e precisão em problemas de regressão e classificação. O XGBoost é uma extensão do algoritmo de gradient boosting que utiliza a técnica de regularização para evitar overfitting.

### Avaliação do Desempenho

Após treinar os modelos, avaliamos o desempenho de cada um deles usando métricas de erro, como o Erro Quadrático Médio (MSE), Erro Absoluto Médio (MAE) e o coeficiente de determinação R². Essas métricas nos ajudam a entender o quão bem os modelos estão se ajustando aos dados de treinamento e de teste.

## Como Usar

1. Clone este repositório em sua máquina local usando o comando:
```
git clone "http link"
```

2. Certifique-se de ter as bibliotecas necessárias instaladas. Caso não as tenha, você pode instalá-las usando o comando:
```
pip install pandas numpy sklearn seaborn matplotlib xgboost geopandas folium
```

3. Baixe o arquivo `housing.csv` e o shapefile `tl_2019_06_cousub.shp` e coloque-os na pasta do projeto.

4. Abra o arquivo Python `House_Price_Prediction.ipynb` em seu ambiente de desenvolvimento Python.

5. Execute o código Python para realizar a análise exploratória dos dados, pré-processamento, treinamento dos modelos e avaliação do desempenho.

6. Ao final da execução, você obterá os resultados das métricas de desempenho dos modelos.

7. Os gráficos gerados estarão disponíveis para visualização e análise.

## Contribuições

Contribuições são bem-vindas! Caso tenha sugestões de melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

