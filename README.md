
# Predição de Inadimplência  – Desafio Banco Bari

Este projeto tem como objetivo prever a probabilidade de inadimplência de clientes com base em características financeiras, auxiliando na tomada de decisão para concessão de crédito imobiliário.

---

## Objetivo

Criar um modelo de machine learning capaz de prever quais clientes têm maior risco de inadimplência, com base em dados como renda mensal, valor do imóvel, score de crédito, entre outros.

---

## Tecnologias Utilizadas

- Python
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib / Seaborn
- imbalanced-learn (RandomOverSampler)
- Google Colab

---

## Pré-processamento dos Dados

- Conversão de colunas String para tipo float
- Criação da variável `percentualFinanciado`
- Padronização dos dados com `StandardScaler`
- Balanceamento da base com `RandomOverSampler`

---

## Modelo Utilizado

- XGBoostClassifier
  - `n_estimators=100`
  - `max_depth=5`
  - `scale_pos_weight` ajustado para tratar o desbalanceamento
  - Threshold ajustado para 0.3 para melhor recall da classe inadimplente

---

## Avaliação do Modelo

- Acurácia: 77%
- Recall da classe 1 (inadimplente): 35%
- Precision da classe 1: 22%
- Gráficos:
  - Matriz de confusão
  - Curva ROC
  - Curva Precisão vs Recall
  - Importância das variáveis

---

## Geração do CSV Final

Foi gerado o arquivo `previsoes_clientes.csv` contendo:
- `id_cliente`: identificador do cliente
- `prob_inadimplencia`: probabilidade estimada de inadimplência (classe 1)

O arquivo está ordenado do cliente mais arriscado para o menos arriscado.

---


## Observações Finais

Este projeto foi desenvolvido como parte do Desafio Prático do Programa de Estágio do Banco Bari (2025).
