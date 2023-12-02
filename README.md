**Relatório Geral de Análise Meteorológica: Bacias do Rio das Velhas**

**1. Identificação e Fonte de Dados:**
A fonte primária de dados para esta análise são as informações relacionadas à precipitação total mensal, obtidas pelo Instituto Nacional de Meteorologia (INMET) das estações próximas às bacias do Rio das Velhas.

**2. Proposta de Investigação:**
Considerando a importância da água nas bacias do Rio das Velhas, este relatório propõe uma investigação sobre a relação entre precipitação e vazão nessa região, visando entender como as condições hidrológicas são afetadas pela intensidade anual de precipitação.

**3. Variável Meteorológica Escolhida:**
A variável escolhida para análise é a precipitação total mensal.

**4. Seleção de Estações:**
Foram selecionadas dez estações próximas ou contidas na mesma região delimitada: CONTAGEM, BELO HORIZONTE (PAMPULHA), DIAMANTINA, CURVELO, PIRAPORA, SETE LAGOAS, BELO HORIZONTE - CERCADINHO, JABOTICATUBAS, RIO-ACIMA, SANTA-LUZIA, e VESPASIANO.

**5. Período de Análise:**
A coleta, organização e filtragem dos dados foram realizadas para o período de 2018 a 2022.

**6. Importação dos Dados para Tabelas Geográficas:**
As informações foram importadas para tabelas geográficas, otimizando a utilização da localização das estações meteorológicas. Duas tabelas foram criadas: "weather_stations" com informações detalhadas de cada estação e "rainfall_data" para armazenar os dados pluviométricos, referenciados pelo identificador único de cada estação.

**7. Análise e Hipótese: Investigação da Relação entre Vazão e Precipitação Anual:**
A hipótese central sugere uma relação proporcional direta entre a vazão do Rio das Velhas e a intensidade anual de precipitação. A tabela 'monthly_flow_rio_das_velhas' servirá como base para a análise.

**8. Quantidade de Dados Válidos por Estação e Coluna:**
Ao analisar a quantidade de dados válidos em cada estação por coluna, observou-se que, para a coluna 'DataMedicao', todas as estações possuem 60 registros válidos. No entanto, na coluna 'valorMedida', há variações indicando a possibilidade de dados ausentes ou não registrados em algumas estações. Essas discrepâncias destacam a importância de tratamento cuidadoso de dados faltantes durante a análise.

**9. Reconstrução do Dicionário de Dados:**

**rainfall_data:**
- **DataMedicao:** A data da medição da precipitação refere-se ao último dia do mês, representando a média mensal da precipitação diária.
- **valorMedida:** Trata-se da medição da PRECIPITAÇÃO TOTAL MENSAL (AUT).
- **id_estacao_fk:** Representa a chave estrangeira do id das estações.

| Coluna         | Tipo de Dados  | Qtd. Valores Únicos | Qtd. Total de Valores |
|----------------|----------------|---------------------|------------------------|
| DataMedicao    | datetime64[ns] | 60                  | 591                    |
| valorMedida    | object         | 389                 | 591                    |
| id_estacao_fk  | int64          | 10                  | 591                    |


**weather_stations:**
- **id_estacao:** Representa o id da estação meteorológica.
- **estacao:** Representa o nome da estação meteorológica.
- **latitude:** Representa a coordenada geográfica de latitude.
- **longitude:** Representa a coordenada geográfica de longitude.

| Coluna       | Tipo de Dados | Qtd. Valores Únicos | Qtd. Total de Valores |
|--------------|---------------|---------------------|------------------------|
| id_estacao   | int64         | 10                  | 10                     |
| estacao      | object        | 10                  | 10                     |
| latitude     | float64       | 10                  | 10                     |
| longitude    | float64       | 10                  | 10                     |

Este relatório proporciona uma visão abrangente do processo de construção do Banco de Dados Geográfico (BDG), as fontes de dados utilizadas, metadados coletados e as visualizações produzidas para análise meteorológica nas bacias do Rio das Velhas.