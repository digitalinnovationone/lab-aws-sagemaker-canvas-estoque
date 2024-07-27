# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

O dataset escolhido foi o "canvas-sample-retail-electronics-forecasting", modelo ideal para a prática do SageMaker. Ele contém as colunas:

- item_id: Identificador único de produtos.
- location: Loja onde as vendas ou inventários foram registrados.
- time_stamp: Data e hora do registro.
- demand: Demanda por item na data especificada.
- price: Preço de venda do item.
- product_category: Categoria do produto.

### 2. Construir/Treinar

Na etapa de construção do modelo no SageMaker, as variáveis foram configuradas:

- Variável-alvo: "price" (para previsão de preço).
- Timestamp: Data e hora dos registros.
- Identificador único: "item_id".
- Agrupador: "location".

Após selecionar o "quick-build" por se tratar de uma prática, treinei o modelo em modo Standart.

### 3. Analisar

Métricas de desempenho do modelo:

- Avg. wQL: Média da precisão em quantis ponderados (P10, P50, P90). Valor de 0.017 indica alta precisão.
- MAPE: Erro percentual médio das previsões. Valor de 0.012 (1.2% de erro médio).
- WAPE: Erro absoluto ponderado. Valor de 0.013 (1.3% de erro absoluto).
- RMSE: Raiz quadrada da média dos erros quadráticos. Valor de 2.278, sugerindo baixa média de erros quadráticos.
- MASE: Erro absoluto escalado. Valor de 0.000, indicando precisão excepcional.

A análise revelou que:

- "demand": Contribui com 57,97% para a acurácia do modelo.
- "product_category": Contribui com 42,03% para a acurácia do modelo.

### 4. Prever

SageMaker Canvas oferece previsões em "batch" ou individual. Com muitos SKUs, a previsão em "batch" é inviável no tier gratuito. Foram feitas previsões individuais, com intervalos de P10 (pessimista) e P90 (otimista) e P50 como previsão estável. Estimativas de lucro ou prejuízo podem ser obtidas para o período previsto (3 meses a partir do último dado).

