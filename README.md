# 🔄 Pipeline de Replicação de Dados (MySQL → SQL Server com Qlik Replicate)

## 📝 Sobre o Projeto

Projeto de engenharia de dados focado na criação de uma pipeline de replicação utilizando Qlik Replicate.

O objetivo foi integrar dados entre MySQL (origem) e SQL Server (destino), garantindo transferência eficiente, consistente e monitorada entre bancos de dados heterogêneos.

---

## 🏗️ Arquitetura da Solução

Fluxo da pipeline:

MySQL (Source)  
↓  
Qlik Replicate (Task de Replicação)  
↓  
SQL Server (Target)

---


![Arquitetura](./imagens/architecture.png)

Fluxo da pipeline:

MySQL (Source Endpoint)
↓
Qlik Replicate (Replication Task)
↓
SQL Server (Target Endpoint)



## 💻 Tecnologias Utilizadas

- Qlik Replicate  
- MySQL  
- SQL Server  
- MySQL Workbench  

---

![Consulta MySQL](./imagens/mysql-query.png)

## ⚙️ Implementação

- Configuração do Source Endpoint (MySQL)  
- Configuração do Target Endpoint (SQL Server)  
- Criação da tarefa de replicação  
- Seleção de tabelas do schema *sakila*  
- Execução com estratégia **Full Load**  

---
📊 Monitoramento da Replicação

![Monitoramento](./imagens/replicate-monitor.png)

## 📊 Monitoramento

A replicação foi acompanhada via painel do Qlik Replicate, permitindo observar:

- Progresso da carga (100% concluído)  
- Tabelas processadas  
- Taxa de transferência (throughput)  
- Ausência de erros  

## ✅ Resultado

- Integração bem-sucedida entre MySQL e SQL Server  
- Replicação completa dos dados  
- Garantia de consistência entre origem e destino  
- Monitoramento eficiente da pipeline  

---

## 🎯 Diferencial do Projeto

Este projeto demonstra na prática a construção de pipelines de integração de dados, abordando conceitos essenciais de engenharia de dados como replicação, integração entre sistemas e confiabilidade na transferência de dados.

---

## 🧑‍💻 Autora

Tatiana Kamioka  
🔗 LinkedIn: https://linkedin.com/in/tatiana-kami  
🔗 GitHub: https://github.com/Tatianakami
