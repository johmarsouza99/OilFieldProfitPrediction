
# Oil Field Profit Prediction

Este projeto utiliza técnicas de aprendizado de máquina e estatísticas para identificar as melhores regiões para exploração de poços de petróleo, com o objetivo de maximizar os lucros e minimizar os riscos. A análise foi realizada em dados sintéticos fornecidos pela empresa de mineração OilyGiant.

# 📋 Descrição do Projeto
O objetivo deste projeto é selecionar a região mais rentável para o desenvolvimento de poços de petróleo com base em dados históricos de três regiões. 

A abordagem inclui a construção de modelos de regressão linear para prever volumes de reservas e o uso de técnicas de bootstrapping para analisar o risco e a distribuição de lucros.

## Etapas do Projeto
### 1. Importação e Análise Exploratória dos Dados

Dados carregados para três regiões, cada um com 100.000 amostras e cinco colunas.
Verificação de duplicatas e valores ausentes: nenhum encontrado.
Exclusão da coluna id para o treinamento do modelo, pois não é relevante para a previsão.

### 2. Treinamento dos Modelos de Regressão

Modelos de regressão linear foram treinados para prever o volume de reservas.
Resultados de desempenho:

- Região 01: RMSE = 37.579, R² = 0.280 (desempenho moderado)

- Região 02: RMSE = 0.893, R² = 1 (melhor desempenho)

- Região 03: RMSE = 40.03, R² = 0.205 (pior desempenho)

As médias dos volumes reais e preditos foram semelhantes em todas as regiões.
### 3. Análise do Volume Mínimo Necessário

- O volume mínimo necessário para evitar perdas é de 111.11 unidades.
- Nenhuma região atende a esse critério de volume mínimo por conta própria.
### 4. Avaliação da capacidade de gerar lucro ao selecionar os 200 melhores pontos.
#### 4.1. Análise de Lucro dos 200 Poços Selecionados

- Região 01 obteve o maior lucro bruto de $33.21 milhões.
- Utilizou-se técnicas de bootstrapping para uma análise mais detalhada do risco de perdas.
### 5. Distribuição de Lucros e Riscos

- A análise gráfica revelou que a Região 02 possui um intervalo de confiança de 95% totalmente positivo, enquanto as regiões 01 e 03 apresentam risco de lucro negativo.
- Região 02 apresentou a melhor média de lucro ($4.29 milhões) e o menor risco de perdas (1.9%).

# 🧠 Técnicas Utilizadas
- Análise Exploratória de Dados
- Modelagem de Regressão Linear
- Técnicas de Bootstrapping para análise de risco
- Métricas de Avaliação: RMSE e R²
- Seleção de Amostras e Análise de Lucros

# 📁 Estrutura do Projeto
- ``data/``: Arquivos de dados sintéticos para as três regiões (geo_data_0.csv, geo_data_1.csv, geo_data_2.csv).
- ``notebooks/``: Notebooks Jupyter com a análise e modelagem.
- ``src/``: Scripts Python para o treinamento e análise dos modelos.
- ``README.md``: Este documento.

# 📝 Resultados
- A Região 02 foi identificada como a mais promissora para exploração, com um lucro médio elevado e um risco mínimo de perdas, atendendo aos critérios da empresa.
- As técnicas de bootstrapping forneceram uma análise detalhada da distribuição de lucros, reforçando a confiabilidade da escolha.

# 📈 Futuras Melhorias
- Testar outros modelos de aprendizado de máquina para potencialmente melhorar a precisão das previsões.
- Incorporar variáveis adicionais, se disponíveis, para aumentar a robustez do modelo.
- Realizar uma análise mais detalhada do risco econômico, considerando variáveis externas, como oscilações no preço do petróleo.
- Avaliar um caso com mais pontos de análise para determinar o melhor local
