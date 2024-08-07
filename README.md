# 📊 Previsão de Estoque Inteligente na AWS com SageMaker Canvas

## 📋 Pré-requisitos

Criei  uma conta na AWS [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)
<img width="977" alt="SageMaker Canvas" src="https://github.com/user-attachments/assets/71a3a2fc-213c-4035-8b9c-7406a812632d">



## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Fiz o upload do dataset no SageMaker Canvas.
<img width="458" alt="dataset" src="https://github.com/user-attachments/assets/ccd79a03-bc90-478a-b6b9-8737166a41fc">


### 2. Construir/Treinar

-   Configurei  as variáveis de entrada e saída de acordo com os dados.
  ![Modelo de configuração](https://github.com/user-attachments/assets/7567e73c-09c4-4652-ae79-96f38816d336)

-   Iniciei  o treinamento do modelo. 
  <img width="1260" alt="Visão geral do modelo" src="https://github.com/user-attachments/assets/692d7461-929e-4b87-877b-b47d82698d4d">


### 3. Analisar

-   Após o treinamento, examinei  as métricas de performance do modelo.
<img width="809" alt="analyze" src="https://github.com/user-attachments/assets/2568710c-54b8-498c-a75d-e721dda5f6e0">

 A Perda Média de Quantilo Ponderada (wQL) avalia a previsão como um todo, média da precisão em pontos de distribuição específicos chamados quantis para quantis P10, P50 e P90. Um valor menor indica um modelo mais preciso.

 Erro Percentual Absoluto Médio (MAPE) é o erro percentual (diferença percentual da média prevista e do valor real) em média em todos os pontos de tempo. Um valor menor indica um modelo mais preciso com MAPE=0 como um modelo perfeito sem erros.

 O Erro Percentual Absoluto Ponderado (WAPE) mede o desvio geral dos valores previstos dos valores observados e é definido pela soma do erro absoluto normalizado pela soma da meta absoluta. Um valor menor indica um modelo mais preciso com WAPE=0 como um modelo perfeito sem erros.

Root Mean Square Error (RMSE) é a raiz quadrada dos erros quadráticos médios. Um RMSE mais baixo indica um modelo mais preciso com RMSE=0 como um modelo perfeito sem erros.

Erro de Escala Absoluto Médio (MASE) é a média do erro absoluto da previsão normalizado pelo erro absoluto médio de um método de previsão de linha de base simples. Um valor menor indica um modelo mais preciso com MASE < 1 como um modelo estimado como melhor do que a linha de base e um MASE > 1 como um modelo estimado como pior do que a linha de base.


### 4. Prever


![single_prediction_results-2](https://github.com/user-attachments/assets/b997bd2d-e6b3-46d3-9942-3555ee72d087)

- Para a previsão p10 em Rosa, espera-se que o valor verdadeiro seja menor do que o valor previsto 10% do tempo.

- Para a previsão p50 em Verde Escuro, espera-se que o valor verdadeiro seja menor do que o valor previsto 50% do tempo. Isso também é conhecido como a previsão mediana.

- Para a previsão p90 em Dourado, Espera-se que o valor verdadeiro seja menor do que o valor previsto 90% do tempo.



