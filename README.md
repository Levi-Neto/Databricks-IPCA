Projeto IPCA com Databricks, Spark e Delta Lake
Este projeto realiza a coleta, tratamento e armazenamento dos dados do IPCA utilizando a API pública do Banco Central do Brasil (BACEN), com processamento em Python, Pandas e PySpark,
e persistência no Delta Lake dentro do ambiente Databricks.

Objetivo

Demonstrar um pipeline simples de dados que:
Consome dados de uma API pública
Realiza tratamento e conversão de tipos
Processa os dados com Spark
Armazena os dados em formato Delta
Cria uma tabela consultável no Databricks
O projeto tem fins educacionais e de portfólio

Fonte dos Dados

API do Banco Central do Brasil (BACEN)
Série: IPCA (código 433)
Período: 2004 a 2024

Tecnologias Utilizadas
Python
Requests
Pandas
PySpark

Fluxo do Projeto
Consumo da API do BACEN via requests
Criação de um DataFrame Pandas
Conversão e tratamento dos dados:
Datas
Valores numéricos
Conversão do DataFrame Pandas para Spark
Definição explícita de schema
Persistência dos dados em formato Delta Lake
Criação de tabela Delta no Databricks
Exportação dos dados para CSV

Estrutura dos Dados

O dataset final contém:

Data → Data de referência do IPCA
IPCA → Valor mensal do índice

Como executar

Este projeto foi desenvolvido para execução em ambiente Databricks.

Passos gerais:

Criar um notebook Python no Databricks
Copiar o código do projeto
Executar as células em ordem
Os dados serão salvos no Delta Lake e registrados como tabela

Saídas do Projeto

Dados persistidos em Delta Lake
Tabela Delta: ipca_table
Arquivo CSV exportado para /dbfs/FileStore/tables/ipca_data.csv

Observações

O projeto utiliza dados públicos
Pode ser facilmente expandido para:
Análises temporais
Agregações com Spark SQL
Dashboards
Integração com outros dados econômicos
Databricks

Delta Lake
