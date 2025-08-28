# Análise de Sentimentos em Tweets com VADER e BERTimbau

## Descrição do Projeto
Este projeto coleta tweets reais contendo uma hashtag de interesse (ex: #educacao, #saude, #politica) e realiza uma análise de sentimentos utilizando diferentes métodos. O objetivo é comparar o desempenho de modelos em português e inglês, e gerar uma tabela comparativa dos resultados.

## Metodologia

### Coleta de Dados
- Tweets coletados usando a API gratuita do X (até 100 tweets por hashtag).
- Os dados foram salvos em um arquivo CSV: [`tweets_coletados.csv`](./tweets_coletados.csv).

### Análise de Sentimentos
Foram aplicados os seguintes métodos:

1. **VADER PT**: Sentiment analysis diretamente em português.
2. **VADER EN**: Sentiment analysis em inglês, após tradução dos tweets.
3. **BERTimbau PT**: Modelo BERT específico para português (usando nlptown/bert-base-multilingual-uncased-sentiment), com conversão de stars para score numérico.

Todos os resultados foram padronizados para o formato:
Positivo (0.80)
Neutro (0.50)
Negativo (0.20)

### Resultados
- Foi criada uma **tabela comparativa** com os resultados de todos os métodos.
- Foram gerados **gráficos**:
  - Barras com score médio por método
  - Histogramas comparando a distribuição de sentimentos entre os métodos

### Observações
- O VADER em português tem limitações, pois o modelo original foi treinado em inglês.  
- A tradução para inglês ajuda a aplicar VADER EN, mas pode alterar nuances do texto.  
- O BERTimbau apresentou resultados mais coerentes em português, capturando melhor o sentimento dos tweets.

## Como acessar os arquivos
- CSV com os tweets coletados: [`tweets_coletados.csv`](./tweets_coletados.csv)
- Código-fonte do projeto: `notebook.ipynb` ou `script.py`

## Autor
Arthur Gonçalves Farias dos Reis

