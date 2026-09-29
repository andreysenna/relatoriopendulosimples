# Período do pêndulo simples para grandes amplitudes

Análise de dados experimentais do período de oscilação de um pêndulo simples em
diferentes comprimentos e ângulos de lançamento, feita em Python.
Trabalho da disciplina de Laboratório de Mecânica Física II ([sua instituição]).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USUARIO/REPO/blob/main/relatorio2.ipynb)

## Objetivo

- Calcular o período de oscilação a partir de medidas de 10 oscilações.
- Estimar a aceleração da gravidade local (g) por regressão linear (mínimos quadrados).
- Avaliar como o período varia com o ângulo de lançamento (5° a 40°).

## Dados

Medidas de tempo de 10 oscilações, com 5 repetições (T1 a T5), para:

- Comprimentos: 100, 90, 80 e 70 cm
- Ângulos: 5°, 10°, 20°, 30° e 40°


## Método

1. Média, desvio padrão e erro padrão das 5 repetições para cada comprimento e ângulo.
2. Período: T = (tempo médio) / 10.
3. Ajuste linear de T² em função de L, usando os dados de 5° e 10°, pois
   T² = (4π²/g)·L. A gravidade sai da inclinação da reta.
4. Incertezas dos parâmetros e de g por propagação de erro.
5. Ajuste linear do período em função do ângulo para cada comprimento, com
   todas as retas no mesmo gráfico.

## Resultados

- g ≈ 10,84 ± 0,59 m/s² (erro relativo de 5,4%).
- O valor de referência (9,81 m/s²) fica dentro do intervalo de confiança de 95%.
- O coeficiente linear da reta T² × L não é zero (0,40 ± 0,17 s²), o que sugere um
  erro sistemático na medida do comprimento.
- O período aumenta com o ângulo nos quatro comprimentos, como esperado para
  amplitudes maiores.

## Bibliotecas

Python, pandas, NumPy, Matplotlib.

