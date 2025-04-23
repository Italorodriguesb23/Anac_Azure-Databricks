✈️ Projeto ANAC - Análise de Acidentes Aéreos com Azure + Databricks
🔍 Descrição
Este projeto tem como objetivo realizar a ingestão, transformação e análise de dados públicos da ANAC (Agência Nacional de Aviação Civil) relacionados a acidentes e incidentes aéreos no Brasil, utilizando uma arquitetura Lakehouse com camadas Bronze, Prata e Gold.

A infraestrutura foi montada com Azure Data Lake integrado ao Databricks, utilizando PySpark para os processamentos e SQL para as consultas analíticas.

🗂️ Estrutura em Camadas
🔸 Bronze:
-Armazenamento dos dados brutos extraídos do portal da ANAC, sem nenhum tratamento.

🔹 Prata:
-Aplicação de limpezas iniciais como remoção de nulos, padronização de dados e tipos de colunas.

🥇 Gold:
-Transformações finais para análise de negócio, com as seguintes propostas implementadas:

-Seleção de colunas relevantes para a análise.

-Criação de uma nova coluna com a soma de todas as lesões (leves, graves e fatais).

-Renomeação de colunas para nomes mais intuitivos.

-Remoção de registros com classificações indesejadas: Indeterminado, Sem Registro e Exterior.

-Inclusão de uma coluna data_atualizacao com a data e hora de atualização dos dados.

-Salvamento da camada Gold em formato Parquet, particionada por estado.

-Criação de consultas SQL específicas para o Estado de São Paulo (SP).

🛠️ Tecnologias Utilizadas:
-Azure Data Lake Storage Gen2

-Azure Databricks

-Apache Spark com PySpark

-SQL (em notebooks Databricks)

-Parquet (formato de armazenamento)
