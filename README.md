Data Replication Lab — MySQL → SQL Server using Qlik Replicate
📌 Overview

Este projeto demonstra a criação de uma pipeline de replicação de dados utilizando Qlik Replicate, replicando dados de um banco MySQL para Microsoft SQL Server.

O objetivo do laboratório foi compreender como configurar endpoints, criar tarefas de replicação e monitorar a transferência de dados entre bancos heterogêneos.

🏗️ Arquitetura da Replicação

A replicação foi configurada seguindo o fluxo abaixo:




Fluxo da pipeline:

MySQL (Source Endpoint)
        ↓
Qlik Replicate (Replication Task)
        ↓
SQL Server (Target Endpoint)
🧰 Tecnologias Utilizadas

Qlik Replicate

MySQL

Microsoft SQL Server

MySQL Workbench

⚙️ Etapas da Implementação
1️⃣ Criação do Source Endpoint

Configuração da conexão com o banco MySQL no Qlik Replicate.

2️⃣ Criação do Target Endpoint

Configuração da conexão com o banco Microsoft SQL Server.

3️⃣ Criação da Replication Task

Configurações utilizadas:

Task Name: replicate_mysql_sqlserver
Replication Profile: Unidirectional
Task Option: Full Load
4️⃣ Seleção das Tabelas

Schema utilizado:

sakila

Tabela utilizada para validação da replicação:

store
📊 Monitoramento da Replicação

Após iniciar a replicação, o progresso da tarefa foi acompanhado na aba Monitor do Qlik Replicate Web Console.

Durante o monitoramento foi possível observar:

Total Completion (100%) indicando conclusão do Full Load

Completed Tables mostrando tabelas processadas

Loading Tables indicando tabelas em processamento

Throughput representando a velocidade de transferência de registros

Errors (0) confirmando que nenhuma falha ocorreu




🔍 Validação dos Dados no MySQL

Para validar os dados na origem foi executada a seguinte consulta no MySQL Workbench:

SELECT * FROM sakila.store;

Resultado retornado:

store_id	manager_staff_id	address_id	last_update
1	1	1	2006-02-15
2	2	2	2006-02-15

A imagem abaixo mostra a consulta executada e o retorno dos registros.




✅ Resultado

A replicação foi executada com sucesso demonstrando:

Conexão entre MySQL e SQL Server

Execução da replicação utilizando Full Load

Monitoramento da execução da tarefa

Transferência correta dos dados entre os bancos

📚 Conceitos Aplicados

Durante este laboratório foram praticados os seguintes conceitos:

Data Replication

Source e Target Endpoints

Replication Tasks

Full Load Replication

Monitoramento de execução

Validação de dados replicados

👩‍💻 Autora

Tatiana Kamioka Lima

Estudante de Ciência da Computação
Interesse em Engenharia de Dados e Análise de Dados
