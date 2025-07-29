# 🚀 Projeto de ETL Local

Este projeto tem como objetivo demonstrar uma arquitetura simples e funcional de ETL rodando localmente, utilizando ferramentas como **Python**, **Apache Hop**, **PostgreSQL** e **Power BI**, simulando um fluxo real de dados empresariais.

---

## 🤝 Alinhamento com os Stakeholders

Durante a fase inicial, em reuniões com os representantes da empresa, foram identificadas as principais necessidades analíticas. Os indicadores-chave (KPIs) definidos foram:

1. 📊 Vendas por período  
2. 👨‍💼 Vendas por vendedor  
3. 📦 Vendas por produto

Esses indicadores orientam toda a estrutura de dados e a modelagem do Data Warehouse.

---

## 🏗️ Arquitetura da Solução

Os dados de origem foram simulados por meio de arquivos **Excel** gerados em **Python**, representando um ambiente transacional. A arquitetura do processo segue o fluxo abaixo:

1. **Extração** dos dados em Excel  
2. **Transformação** com Apache Hop  
3. **Carga na área de Staging (PostgreSQL)**  
4. **Tratamento incremental e envio ao DW**  
5. **Visualização dos dados no Power BI**

<p align="center">
  <img src="https://github.com/user-attachments/assets/f3d9b9e6-9fa6-4db2-86de-3515fc33011b" width="800px" />
</p>

---

## 🧠 Modelagem de Banco de Dados

Para possibilitar análises eficientes, foi adotado o modelo **Star Schema** (Esquema em Estrela), que facilita a visualização dos dados e garante performance nas consultas.

<p align="center">
  <img src="https://github.com/user-attachments/assets/0efb8b67-74f9-43a8-88da-cc9ce2951463" width="800px" />
</p>

---

## 🔄 Carga de Dados para o Banco Staging

A carga inicial dos dados é feita por meio do **Apache Hop**. O pipeline principal é responsável por ler os dados em Excel e inseri-los no banco staging. As etapas utilizadas foram:

1. 📥 Microsoft Excel Input  
2. 🧭 Get System Info (para rastrear data/hora da carga)  
3. 🛢️ Table Output

<p align="center">
  <img src="https://github.com/user-attachments/assets/c8432d99-d252-417e-92a1-ea2a16a1cffd" width="500px" />
</p>

---

## ⚙️ Automatização com Workflow

Para executar todos os pipelines em sequência e de forma automatizada, foi criado um **workflow** dentro do Apache Hop:

<p align="center">
  <img src="https://github.com/user-attachments/assets/34f8daf5-0818-4a4e-8dab-d046bc7bc94d" width="500px"/>
</p>

---

## 📥 Carga Incremental no Data Warehouse

A etapa final consiste em realizar a carga incremental dos dados tratados para o **Data Warehouse**, garantindo que apenas novos registros ou atualizações sejam aplicados, evitando retrabalho e duplicações.

<p align="center">
  <img src="https://github.com/user-attachments/assets/003c27c2-85f1-4140-8be6-56b472106c99" width="500px"/>
</p>

---

## 📊 Dashboard

Após concluir as etapas de extração, transformação e carga dos dados, é hora de transformar essas informações em insights visuais por meio de um dashboard interativo. Utilizamos o Power BI para criar visualizações intuitivas que facilitam a análise e a tomada de decisões. 

<p align="center">
  <img src="https://github.com/user-attachments/assets/cbb83dc4-acb7-4060-b7f4-1415c9ae6501" width="500px" />

</p>

[🔗 Clique aqui para acessar o dashboard interativo no Power BI](https://app.powerbi.com/view?r=eyJrIjoiOGRlZmMyMTUtZmQxMi00MWU3LTg0M2UtMjg0Y2MzZjg5YTg2IiwidCI6ImUwZjRhNWZkLWEzZTItNDZlOS1iYjEyLTliZDdjZjI2Y2U4YiJ9)

---

## 📌 Tecnologias Utilizadas

* 🐍 Python (geração de dados)
* 📊 Power BI (visualização dos dados)
* 🐘 PostgreSQL (armazenamento dos dados)
* 🛠️ Apache Hop (ETL e workflows)

---

## ✍️ Autor

**Eduardo Callejon**  
Estudante em Análise e Engenharia de Dados  

---

