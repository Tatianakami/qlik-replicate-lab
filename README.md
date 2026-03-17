Data Replication Lab — MySQL → SQL Server using Qlik Replicate
📌 Overview

Este projeto demonstra a criação de uma pipeline de replicação de dados utilizando Qlik Replicate, replicando dados de um banco MySQL para Microsoft SQL Server.

A atividade foi realizada em ambiente de laboratório utilizando uma máquina virtual de treinamento, com foco em compreender como configurar endpoints, criar tarefas de replicação e monitorar a execução.

🏗️ Arquitetura da Replicação

Fluxo de dados configurado:

MySQL (Source Endpoint)
        │
        ▼
Qlik Replicate Task
        │
        ▼
SQL Server (Target Endpoint)
🖼️ Arquitetura da solução

(Inserir imagem aqui)

images/architecture.png
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
4️⃣ Seleção das tabelas

Schema utilizado:

sakila

Tabela utilizada para validação:

store
📊 Monitoramento da Replicação

Após iniciar a tarefa de replicação, o progresso foi acompanhado através da aba Monitor no Qlik Replicate Web Console.

Durante o monitoramento foi possível observar:

Total Completion (100%) indicando que o processo de Full Load foi concluído.

Completed Tables, mostrando quantas tabelas já foram processadas.

Loading Tables, indicando tabelas ainda em carregamento.

Throughput, que representa a velocidade de transferência de registros.

Errors (0) confirmando que nenhuma falha ocorreu durante a replicação.

Esse painel permite acompanhar a execução da tarefa em tempo real e verificar se a replicação está ocorrendo corretamente.

🖼️ Monitor da replicação

(Inserir imagem aqui)

images/replicate-monitor.png
🔍 Validação dos Dados no MySQL

Para validar os dados na origem, foi executada a seguinte consulta no MySQL Workbench:

SELECT * FROM sakila.store;

Resultado retornado:

store_id	manager_staff_id	address_id	last_update
1	1	1	2006-02-15
2	2	2	2006-02-15
🖼️ Consulta executada no MySQL

(Inserir imagem aqui)

images/mysql-query.png
✅ Resultado

A replicação foi executada com sucesso, demonstrando:

Conexão entre MySQL e SQL Server

Execução da tarefa com Full Load

Monitoramento da execução da replicação

Transferência correta de dados entre os bancos

📚 Conceitos aplicados

Durante este laboratório foram praticados os seguintes conceitos:

Data Replication

Configuração de Source e Target Endpoints

Criação de Replication Tasks

Full Load Replication

Monitoramento de execução

Validação de dados replicados

👩‍💻 Autora

Tatiana Kamioka

Estudante de Ciência da Computação
Foco em Data Engineering | Análise de Dados
