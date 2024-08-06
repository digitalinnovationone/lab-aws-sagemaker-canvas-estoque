# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Este desafio proposto como conclusão do curso referente a Machine Learning (ML) através do SageMaker Canvas, uma aplicação AWS no-code que permite que você trenine modelos para que realizem analises preditivas, generativa, etc.

## Principais caracteristicas

- Análise de probabilidade - Beneficiando a empresa com insights dos dados analisados
- Facilitando tomada de decisões - Com os insights obtidos, é possível tomar decisões de forma estratégica utilizando os dados.
- Agilização do processo de análise - Após o treinamento inicial, o modelo pode continuar sendo utilizado com informações atualizadas, e continuará com o conhecimento do treinamento prévio, agilizando o processo para futuras analises.

## 🚀 Passo a Passo

### 1. Importação de dados

-   Através dos dados obtidos do dataset, foi possivel realizar o treinamento e posterior análise dos mesmos.
-   O modelo do datset escolhido, consiste nas vendas e valores variáveis, contendo ID do produto, data das transações, n° de vendas e valor variavel.

### 2. Construir/Treinar

-   Com as informações obtidas, foi necessario configurar os modelos de entrada e saida.
-   Assignando as colunas com suas correspondentes informações, a configuração está completa.
-   Com a configuração completa, o modelo escolhido para realizar o treinamento foi o de quickbuild, permitindo uma visualização prática e completa.

### 3. Analise de métricas

-  Avg. wQL
    1.000
-   MAPE
    1.000
-   WAPE
    1.000
-  RMSE
    1.133
-   MASE
    0.131

### 4. Prever

- Precisão das Previsões: As métricas MAPE e WAPE indicam que o modelo tem alta precisão nas previsões;
- Erro Médio: O RMSE sugere que o modelo tem um erro médio aceitável, considerando a escala dos dados.
