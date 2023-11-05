# Prevendo o valor das ações do S&P

## Visão Geral

O conjunto de dados, é sobre os preços históricos de ações (últimos 5 anos) para todas as empresas atualmente encontradas no índice S&P 500. 

Você pode conferir o dataset e o projeto na íntegra clicando abaixo:

Link dataset: https://www.kaggle.com/datasets/camnugent/sandp500

Link do código do projeto: https://github.com/gustavoptavares/Acoes-Mercado-Financeiro/blob/main/A%C3%A7%C3%B5es_S%26P.ipynb

## Problema e Solução

Vamos analisar os dados o conjunto de dados sobre os preços históricos de ações. A quantidade de dados financeiros na web é aparentemente infinita, vamos entender, no detalhe, aspectos relacionados as empresas encontradas no índice S&P 500, como:

• Enteder o conjunto de dados e a os preços mudam ao longo do tempo.

• Elaborar os modelos preditivos para prever o valor das ações.

## O Processo

O primeiro passo do projeto foi adquirir os dados. Utilizamos os dados do portal Kaagle, carregando-o no Google Colab, para a exploração e análise dos dados utilizando a linguagem de programação Python e suas bibliotecas, como Pandas, Matplotlib, Tensorflow e Scikit-Learn. Neste projeto foi feito, uma análise exploratória, e serão criados 3 modelos preditivos, com o objetivo de prever o valor da ação. Serão utilizados os algoritmos de regressão linear, de redes neurais LSTM (Long Short-Term Memory) e o ARIMA (Auto Regressive Integrated Moving Averages).	

## Resultados

A regressão linear tem um desempenho excelente, com erros absolutos e quadrados muito baixos e um coeficiente de determinação quase perfeito. Isso indica que o modelo tem uma precisão notável para a maioria das previsões.

O modelo LSTM, que é um tipo de rede neural recorrente especializada em capturar relações temporais em séries temporais, tem erros absolutos e quadrados significativamente maiores do que a regressão linear, indicando que ele não foi tão preciso. No entanto, o R² ainda é muito alto, o que significa que, apesar dos erros maiores, o modelo ainda captura bem a variação dos dados.

O modelo ARIMA, um modelo clássico para previsão de séries temporais, apresenta erros absolutos e quadrados extremamente altos, e um R² negativo. Isso indica que o modelo ARIMA não conseguiu capturar a variação dos dados e na verdade fez previsões piores do que um modelo ingênuo que sempre prevê a média dos dados.

## Conclusões

A regressão linear é claramente o modelo mais preciso entre os três, com o menor MAE e MSE e o maior R², indicando que ele pode prever a variação dos dados quase perfeitamente.

O modelo LSTM, apesar de não tão preciso quanto a regressão linear, ainda é um modelo robusto com um bom R².

O ARIMA, por outro lado, parece inadequado para os dados em questão, já que suas previsões são muito piores do que um modelo simples de previsão da média. Isso pode acontecer se a série temporal tiver características, como não-estacionariedade ou padrões complexos, que não são bem modelados pelo ARIMA
