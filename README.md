# 📊 Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Neste projeto utilizei do ChatGPT e SageMaker Canvas para desenvolver um sistema de estoque inteligente com Machine learning (ML).

## 🎯 Objetivos Deste Desafio de Projeto (Lab)

O objetivo deste desafio é aprimorar minhas habilidade com Machine Learning low-code, aprender mais sobre o Amazon SageMaker e principalemente aprender como a inteligência artificial pode ajudar no mercado profissional ajudando empresas com tomada de decisões e previsões futuras.

## 🚀 Passo a Passo

### 1. Desenvolver Dataset

-   Utilizei o ChatGPT para desenvolver um DataSet com informações fícticias utilizando o seguinte prompt:

Crie um arquivo CVS contendo as colunas (ID_Produto, ID_Cliente, Valor, Data, Quantidade_estoque).
utilizarei estes dados para treinamento de um modelo de estoque inteligente.

{REGRAS}

- Sempre que um produto chegar a quantidade 10 reabasteça o material,
- Preencha o arquivo com no minimo 6 compras de produtos variados ficticios por dia.
- Preencha ao arquivo comecando do dia 01-07-2024 terminando em 17-07-2-2024

### 2. Construir/Treinar

-   No SageMaker Canvas, importei o dataset criado.
-   Configurei as variáveis de entrada e saída.
-   Iniciei o treinamento do modelo.

### 3. Analisar

-   Após o treinamento, examinei as métricas de performance do modelo.
-   Verifiquei as principais características que influenciam as previsões que foram a quantidade de material em estoque (quantidade_estoque) e o valor do produto (valor).

### 4. Prever

-   Usei o modelo treinado para fazer previsões de estoque.
-   Analisando as previsões geradas notamos claramente que o principal influenciador nos nossos resultados é a quantidade de material em estoque, ja que quando aumentamos a quantidade em estoque de 50 para 10 notamos uma diminuição significativa de vendas para todos os produtos.
-   Notamos também que o produto P007 não tem alterações relevantes nas vendas independente da quantidade em estoque ou valor, o que pode indicar um grande volume de saída, possibilitando talvez o aumento do estoque deste material.
-   O produto P005 teve um aumento de 63% de saída quanto alteramos o valor de 70 para 50.
-   O produto P003 teve um aumento de 80% de saída quando aumentamos a quantidade em estoque de 10 para 100, o que pode indicar um maior volume de compras em maiores quantidades.
-   Os demais produtos possuem alterações relevantes somente quando diminuimos o período analisado, consequentimente alterações negativas, o que pode indicar a necessidade de mais atenção nesses produtos.

## Agradecimentos

Espero que tenham gostado do meu projeto, se quiserem podem me seguir aqui no Github e no linkedin para mais projetos:
https://www.linkedin.com/in/andr%C3%A9-abichabicki-46b5b1193/
