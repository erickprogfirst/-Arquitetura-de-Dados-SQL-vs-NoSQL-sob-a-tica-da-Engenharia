# 🗄️ -Arquitetura-de-Dados-SQL-vs-NoSQL-sob-a-otica-da-Engenharia

## 🎯 Sobre o Projeto
Este repositório foi criado para consolidar conceitos, definições e insights avançados sobre o ecossistema de Bancos de Dados Relacionais (SQL) e Não Relacionais (NoSQL). O foco principal é entender como essas tecnologias se aplicam no dia a dia e nos desafios de um Engenheiro de Dados.

---

## 🏗️ O Papel do Engenheiro de Dados
O Engenheiro de Dados é o arquiteto responsável por projetar, construir e manter a infraestrutura de dados (pipelines). A escolha entre SQL e NoSQL não é uma questão de "qual é o melhor", mas sim de **"qual resolve o problema de arquitetura atual de forma mais eficiente, escalável e com menor custo"**. 

A decisão correta impacta diretamente a performance de ferramentas de Business Intelligence (como Power BI) e a eficiência de armazenamento em ambientes Cloud (como Google Cloud Platform).

---

## 🏛️ Bancos de Dados Relacionais (SQL)

### 📌 Conceito
Os bancos de dados relacionais armazenam dados em tabelas rigidamente estruturadas (linhas e colunas) que se relacionam entre si através de chaves (Primary Keys e Foreign Keys). Eles utilizam a linguagem SQL (Structured Query Language) para manipulação e consulta.

### ⚙️ Características Principais
* **Esquema Rígido (Schema-on-write):** A estrutura do dado deve ser definida antes da inserção.
* **Propriedades ACID:**
  * **A**tomicidade: Tudo ou nada na transação.
  * **C**onsistência: O banco vai de um estado válido para outro.
  * **I**solamento: Transações simultâneas não interferem umas nas outras.
  * **D**urabilidade: Dados gravados estão seguros, mesmo em caso de falha.
* **Escalabilidade Vertical:** Geralmente escalam melhor adicionando mais poder computacional (CPU, RAM) a um único servidor.

### 💼 Casos de Uso na Engenharia
* **Sistemas Transacionais (OLTP):** ERPs, sistemas contábeis e financeiros onde a integridade do dado (ACID) é inegociável.
* **Data Warehouses (OLAP):** Armazenamento de dados históricos modelados (ex: Star Schema) para consumo de analistas e dashboards.

---

## 🌐 Bancos de Dados Não Relacionais (NoSQL)

### 📌 Conceito
Criados para lidar com o volume, velocidade e variedade do Big Data. Eles quebram o paradigma tabular e permitem o armazenamento de dados não estruturados ou semi-estruturados.

### ⚙️ Características Principais
* **Esquema Flexível (Schema-on-read):** Os dados podem ser inseridos sem uma estrutura pré-definida, ideal para fontes de dados dinâmicas.
* **Teorema CAP:** Em sistemas distribuídos, é possível garantir apenas duas das três propriedades simultaneamente: **C**onsistência, **D**isponibilidade (Availability) e **T**olerância a Partições.
* **Escalabilidade Horizontal:** Desenhados para escalar adicionando mais servidores (nós) ao cluster, distribuindo a carga de forma barata.

### 🗂️ Tipos de NoSQL
1. **Chave-Valor (Key-Value):** Altíssima performance para leituras simples (ex: Redis, DynamoDB).
2. **Documentos:** Armazena dados em formatos como JSON/BSON, excelente para catálogos e e-commerces (ex: MongoDB, Couchbase).
3. **Colunares (Wide-Column):** Otimizados para consultas rápidas em grandes volumes de dados (ex: Apache Cassandra, HBase).
4. **Grafos:** Focados nas relações e conexões entre os dados (ex: Neo4j).

### 💼 Casos de Uso na Engenharia
* Aplicações web de alto tráfego, catálogos de produtos dinâmicos, análise de logs em tempo real e IoT (Internet das Coisas).

---

## ⚖️ Comparativo Direto: SQL vs NoSQL

| Característica | Relacional (SQL) | Não Relacional (NoSQL) |
| :--- | :--- | :--- |
| **Estrutura** | Tabelas, Linhas, Colunas | Chave-valor, Documentos, Grafos, Colunares |
| **Esquema** | Rígido (Pré-definido) | Flexível (Dinâmico) |
| **Escalabilidade** | Vertical (Mais hardware) | Horizontal (Mais servidores) |
| **Integridade** | ACID | Teorema CAP / BASE |
| **Exemplos** | PostgreSQL, MySQL, SQL Server | MongoDB, Redis, Cassandra, Neo4j |

---

## 💡 Insights Finais e Conclusão
Como Engenheiro de Dados, a flexibilidade técnica é o maior ativo. 
* Use **SQL** quando o domínio dos dados for conhecido, as relações entre entidades forem complexas e a consistência transacional for prioritária. 
* Use **NoSQL** quando o foco for escalabilidade horizontal massiva, evolução rápida de aplicações e dados estruturalmente imprevisíveis. 
* Em arquiteturas modernas (Data Lakes, Lakehouses), é muito comum e recomendado o uso de abordagens **poliglotas**, onde SQL e NoSQL coexistem no pipeline para extrair o melhor de cada tecnologia.

---
*Projeto desenvolvido como parte do aprimoramento contínuo em Engenharia de Dados e Arquitetura de Sistemas.*
