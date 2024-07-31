# Avaliação de Previsões de Estoque para Itens 13 e 18

## Descrição do Projeto

Este projeto visa avaliar as previsões de estoque para os itens 13 e 18, utilizando um modelo de Machine Learning implementado na AWS. As previsões incluem os quantis P10, P50 e P90 para diferentes datas, representando diferentes níveis de confiança nos valores previstos de estoque.

## Dados Analisados

Foram analisados dados de estoque para os seguintes itens:

- **Item 13**
  - Previsões para P10, P50 e P90:
    - P10: Quantil de 10%
    - P50: Mediana (Quantil de 50%)
    - P90: Quantil de 90%

- **Item 18**
  - Previsões para P10, P50 e P90:
    - P10: Quantil de 10%
    - P50: Mediana (Quantil de 50%)
    - P90: Quantil de 90%

## Resultados

### Item 13

| Data       | P10     | P50     | P90     |
|------------|---------|---------|---------|
| 2024-02-09 | 33.474  | 35.906  | 65.124  |
| 2024-02-10 | 14.866  | 51.763  | 95.053  |
| 2024-02-11 | 39.670  | 72.969  | 73.020  |
| 2024-02-12 | 30.880  | 40.573  | 69.773  |
| 2024-02-13 | 35.117  | 41.270  | 68.813  |

### Item 18

| Data       | P10     | P50     | P90     |
|------------|---------|---------|---------|
| 2024-02-09 | 27.380  | 65.654  | 87.804  |
| 2024-02-10 | 27.115  | 31.290  | 55.228  |
| 2024-02-11 | 19.965  | 71.361  | 91.179  |
| 2024-02-12 | 35.682  | 70.226  | 78.499  |
| 2024-02-13 | 40.984  | 67.216  | 92.997  |

## Considerações Finais

Essas previsões ajudam a entender as possíveis variações no estoque e podem ser utilizadas para melhorar o planejamento e a gestão de recursos.
