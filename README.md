# Previsão de Tarifas Aéreas com SARIMA e XGBoost

Projeto de Ciência de Dados voltado à previsão de tarifas aéreas domésticas no Brasil utilizando técnicas de Séries Temporais e Machine Learning.

O objetivo foi desenvolver um modelo capaz de antecipar o comportamento dos preços das passagens aéreas a partir de dados históricos da ANAC, avaliando diferentes abordagens preditivas e estratégias de validação temporal.

## Objetivo

Responder à seguinte pergunta:

**É possível prever tarifas aéreas domésticas utilizando apenas o comportamento histórico dos preços?**

Para isso foram comparadas abordagens estatísticas clássicas e algoritmos de Machine Learning, avaliando desempenho, robustez e aplicabilidade prática.

## Dados Utilizados

* Microdados de tarifas aéreas da ANAC
* Série temporal mensal de preços médios
* Dados históricos utilizados para treinamento e validação dos modelos

## Tecnologias

* Python
* Pandas
* NumPy
* Statsmodels
* Scikit-learn
* XGBoost
* Matplotlib
* Google Colab

## Metodologia

### Modelos Avaliados

* SARIMA
* SARIMA otimizado por Grid Search (AIC)
* XGBoost
* Média Móvel (Baseline)
* Último Valor Observado (Naive)

### Estratégias de Validação

* Holdout temporal
* Rolling Window Validation (Walk-Forward)

### Métricas

* MAE
* RMSE
* MAPE

## Principais Resultados

| Modelo                | MAE    | RMSE   | MAPE   |
| --------------------- | ------ | ------ | ------ |
| XGBoost               | 64,78  | 80,73  | 7,03%  |
| SARIMA Rolling Window | 63,90  | 79,10  | 7,19%  |
| SARIMA Otimizado      | 65,81  | 77,06  | 7,35%  |
| Média Móvel           | 78,58  | 101,05 | 9,48%  |
| Naive                 | 107,22 | 128,27 | 12,80% |

## Principais Insights

* O XGBoost apresentou o menor erro percentual médio (MAPE de 7,03%).
* O SARIMA apresentou maior estabilidade em termos de RMSE.
* A validação por Rolling Window reduziu significativamente os erros em comparação à previsão direta tradicional.
* Os modelos conseguiram capturar com sucesso os padrões sazonais observados no mercado aéreo brasileiro.

## Conclusão

Os resultados demonstram que tanto abordagens estatísticas clássicas quanto modelos de Machine Learning podem produzir previsões robustas para tarifas aéreas.

A combinação de validação temporal adequada, otimização de hiperparâmetros e comparação com benchmarks simples permitiu construir um pipeline preditivo consistente e aplicável a cenários reais de planejamento e análise de mercado.

## Possíveis Evoluções

* Inclusão de variáveis macroeconômicas (SARIMAX)
* Utilização de câmbio e preço do combustível aeronáutico
* Modelos híbridos combinando SARIMA e XGBoost
* Deflacionamento da série utilizando IPCA

## Autor

Flávio Estevam Nogueira Andrade

Ciência de Dados | Economia | Machine Learning | Inteligência Artificial
