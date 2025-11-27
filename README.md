<img src="https://github.com/cristovao0/lab-aws-sagemaker-canvas-estoque/blob/main/resources/images.jpg" width="160" height="160">

📌 1. Visão Geral do Projeto

Este projeto foi desenvolvido como parte do desafio da DIO: “Previsão de Estoque Inteligente na AWS com SageMaker Canvas”.
O objetivo é utilizar Machine Learning no-code para criar um sistema que preveja a demanda futura de produtos, ajudando negócios a tomarem decisões mais estratégicas sobre estoque, compras e reposições.

Para tornar o desafio mais realista e prático, optei por simular o estoque de um E-commerce de Restaurante, pois esse cenário apresenta um alto volume de vendas, variações sazonais e grande impacto de promoções e feriados — condições ideais para demonstrar o poder de predição do SageMaker Canvas.

🍽️ 2. Por que escolher um E-commerce de Restaurante?

A escolha desse tipo de negócio foi estratégica:

✔ Permite análises ricas e visualmente interessantes

✔ Simular dados é simples e natural (vendas, promoções, feriados)

✔ Ideal para mostrar insights relevantes que um restaurante realmente usaria

✔ Combina alta variabilidade → excelente para treinar modelos de ML

✔ Fica incrível visualmente no relatório final, no Canvas e no GitHub

Com esse tipo de dataset, podemos demonstrar o que empresas reais fazem para:

prever demanda,

ajustar estoque,

evitar rupturas,

otimizar compras,

planejar promoções,

antecipar picos.

📊 3. Criação e Seleção do Dataset

Com a ajuda do ChatGPT, defini o escopo do dataset e gerei um arquivo CSV com:

✔ 5 produtos diferentes

✔ 600 linhas simuladas

✔ Preço, promoção, estoque, reposição

✔ Tendência online

✔ Fim de semana

✔ Feriados (impactam fortemente as vendas)

Esse arquivo foi salvo na pasta datasets do repositório.

O dataset contém colunas realistas e perfeitas para modelos de time series forecasting, incluindo vendas_dia, que é a variável alvo.

🛠️ 4. Construir e Treinar o Modelo no SageMaker Canvas

Após importar o dataset no SageMaker Canvas:
<img src="https://github.com/cristovao0/lab-aws-sagemaker-canvas-estoque/blob/main/resources/Criando%20o%20modelo%201.png" width="1920" height="1080">

o Canvas automaticamente identificou padrões importantes,

gerou gráficos de comportamento de vendas,

mostrou tendência semanal,

analisou impacto de feriados,

mostrou preços, promoções e variações diárias.

🎯 Coluna Alvo (Target):
<img src="https://github.com/cristovao0/lab-aws-sagemaker-canvas-estoque/blob/main/resources/modelo%20configurado.png" width="1920" height="1080">
vendas_dia
A escolha dessa coluna permite prever:

vendas de amanhã,

dos próximos 7 dias,

dos próximos 30 dias.

Essas previsões permitem:

prever ruptura de estoque,

planejar reposições,

ajustar compras,

reduzir custos,

estimar faturamento futuro.

⚡ 5. Treinando Dois Modelos: Quick Build vs Standard Build

Para fins de comparação, treinei dois modelos:

🚀 Quick Build
<img src="https://github.com/cristovao0/lab-aws-sagemaker-canvas-estoque/blob/main/resources/modelo%20quickbuild.png" width="1920" height="1080">

Treinamento mais rápido

Menos camadas de análise

Menor custo computacional

Ideal para testes iniciais

<strong>PS: Não irei conseguir fazer as comparações dos modelos pois enquanto gerava o modelo standart todos os meus créditos gratis foram consumidos</strong>, mas deixarei aqui um resumo do que o pesquisei sobre a Stadart Build

🧩 Standard Build

Mais robusto

Testa mais algoritmos

Avaliação mais profunda

Resultados mais estáveis

Melhor desempenho geral

Ambos os modelos retornaram métricas importantes que avaliam a qualidade das previsões.

📐 6. Interpretação das Métricas do Modelo

Aqui está a explicação clara e prática de cada métrica retornada pelo Canvas:

🔍 1. Avg. wQL — Weighted Quantile Loss

Essa métrica é usada para avaliar previsões de séries temporais baseadas em quantis (p50, p90 etc.).

Como interpretar:

< 0.20 → Excelente

Quanto menor → melhor

Essa métrica considera a incerteza do futuro, por isso é muito usada pela AWS.

🔍 2. MAPE — Mean Absolute Percentage Error

Mede o erro percentual médio do modelo.

Como interpretar:

< 10% → nível profissional

10–20% → muito bom

20–30% → aceitável

30% → fraco

🔍 3. WAPE — Weighted Absolute Percentage Error

Versão mais estável do MAPE, pois leva em conta o volume de vendas.

Como interpretar:

0.20–0.30 → modelo bom e consistente

Quanto menor → melhor

🔍 4. RMSE — Root Mean Squared Error

Erro médio em unidades reais (quantas unidades o modelo erra, em média).

É muito útil para entender o impacto na operação:

RMSE de 11 significa que o modelo erra cerca de 11 unidades para cima ou para baixo.

🔍 5. MASE — Mean Absolute Scaled Error

Compara seu modelo com um modelo "ingênuo" ("amanhã = hoje").

Como interpretar:

< 1.0 → modelo melhor que o naive

= 1.0 → igual

1.0 → pior

É uma das métricas mais importantes para séries temporais reais.

📌 7. Insights Obtidos no Canvas

Durante a análise, o SageMaker identificou colunas com maior impacto na previsão:

preco_dia — elasticidade de preço

tendencia_online_idx — comportamento digital

estoque_inicial / estoque_final — risco de ruptura

dia_semana — sazonalidade semanal

feriado — forte impacto em vendas

promocao / desconto_pct — aumento significativo de demanda

Esses insights permitem que empresas tomem decisões mais inteligentes sobre:

compras,

preços,

promoções,

gestão de estoque,

planejamento de demanda.

🎯 8. Conclusão

Este projeto demonstra como, mesmo sem código, é possível construir um modelo de previsão robusto utilizando o AWS SageMaker Canvas.

Combinando:

um dataset bem projetado,

engenharia de features realista,

análise de impacto,

e comparação entre dois tipos de modelos,

foi possível criar um sistema inteligente capaz de prever vendas e otimizar estoque de forma simples e profissional.

Esse projeto pode ser expandido com:

gráficos avançados,

testes com novos produtos,

integração com dashboards,

criação de APIs via AWS Lambda + API Gateway.



