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

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.

---

Previsão de Estoque – Análise do Modelo (por Wanessa Carvalho)

Esta seção foi adicionada como parte da atividade de melhoria de projeto.

Objetivo:

Desenvolver um modelo de previsão de ESTOQUE_FUTURO utilizando AWS SageMaker Canvas.

Resultados do Modelo:

WAPE: 0.420

MAPE: 1.276

RMSE: 28.700

MASE: 1.194

Avg. wQL: 0.274

O modelo atingiu um desempenho consistente para previsão de curto prazo (7 dias).

Variáveis mais importantes:

VENDAS – 22.72%

ESTOQUE_ONTEM – 18.97%

PRECO – 15.31%

QUANTIDADE_ESTOQUE – 14.78%

SEMANA_DO_ANO – 3.93%

Interpretação das Métricas: 

As métricas obtidas permitem avaliar o desempenho do modelo de previsão para a janela de 7 dias. O WAPE de 0.420 indica que o erro médio ponderado gira em torno de 42% do valor real, o que é aceitável para cenários em que a série apresenta volatilidade, variações súbitas de vendas ou ausência de fortes padrões sazonais. O MAPE de 1.276 reforça que há variações pontuais mais difíceis de capturar, comuns em séries de demanda instável. O RMSE de 28.700 representa a magnitude média do erro em unidades absolutas, e serve como referência direta para decisões de estoque. Já o MASE de 1.194 mostra que o modelo apresenta desempenho melhor que uma previsão ingênua simples, embora ainda haja espaço para aprimoramento. No geral, o modelo é adequado para previsões de curto prazo, especialmente para apoiar reposição contínua.

Possíveis Melhorias: 

1. Algumas estratégias podem elevar a qualidade do modelo nas próximas iterações. Entre elas:

2. Utilizar o modo Standard Build do SageMaker Canvas, que executa um processo mais completo de modelagem e tende a melhorar métricas em séries complexas.

3. Expandir o conjunto de features com variáveis temporais adicionais, como feriados, eventos especiais, indicadores sazonais detalhados e ciclos identificados no histórico.

4. Aumentar o período de dados analisados, incorporando mais histórico para permitir melhor identificação de padrões.

5. Enriquecer o dataset com informações externas, como tendências de mercado, promoções, disponibilidade de fornecedores ou variáveis macroeconômicas.

6. Realizar ajustes no pré-processamento, como identificar outliers e revisar padrões de preenchimento de estoque que possam estar distorcendo a série.

Essas melhorias contribuiriam para reduzir erros, capturar melhor a dinâmica temporal da demanda e tornar o modelo mais robusto em cenários reais de tomada de decisão.

Conclusão:

O modelo é adequado para apoiar decisões de reposição e planejamento, e pode ser melhorado com Standard Build e novas features sazonais.

O modelo foi treinado em AWS SageMaker Canvas (versão 1) com previsão de 7 dias.
Build: Quick Build.
