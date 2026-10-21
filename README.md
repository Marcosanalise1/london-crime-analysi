# 🛡️ Análise de Criminalidade e Priorização de Segurança Pública em Londres (2008–2016)

> **Projeto desenvolvido na formação em Análise de Dados pela EBAC**, cobrindo o ciclo completo de dados: desde a extração e validação em nuvem com Python e SQL no Google BigQuery até a construção de um dashboard analítico no Power BI focado na tomada de decisão.

---

## 🛠️ Tecnologias e Ferramentas

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=sqlite&logoColor=white)
![Google BigQuery](https://img.shields.io/badge/Google_BigQuery-669DF6?style=for-the-badge&logo=googlebigquery&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C94C?style=for-the-badge&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

---

## 🎯 Objetivo do Projeto

Analisar os registros de criminalidade em Londres entre **2008 e 2016**, identificando padrões temporais, categorias de infrações mais frequentes e distritos (*boroughs*) críticos. O projeto visa responder a perguntas estratégicas de alocação de recursos policiais, além de demonstrar a integração técnica entre **Python, SQL, BigQuery e Power BI** em um pipeline de dados robusto.

---

## 📊 Estrutura do Dashboard (Power BI)

O relatório foi estruturado em **1 página analítica**:

1. **Página 1:** Panorama da evolução anual, sazonalidade, tipos e distribuição de crimes, distribuição por bairros. Os principais KPIs (~5 milhões de registros, bairro crítico e maior incidência), tendências temporais e evolução das categorias ano a ano.

---

## 🔍 Etapas e Metodologia

### 1. Extração & Conexão Cloud (Google BigQuery + Python)
Conexão direta ao BigQuery através de script Python utilizando a biblioteca oficial `google.cloud.bigquery`.
* **Projeto no BigQuery:** `projeto-london-crime-506516`
* **Tabela Analisada:** `projeto-london-crime-506516.london_crime.crime_by_lsoa`
* Conversão automatizada de consultas SQL para DataFrames **Pandas** para checagens locais.

### 2. Validação & Qualidade dos Dados (Data Quality)
Antes da etapa de visualização, foram executadas queries SQL para auditoria da base:
* **Integridade:** Identificação de valores nulos, contagem total de registros e checagem de tipos de dados.
* **Consistência Numérica & Temporal:** Verificação de amplitudes de datas (2008 a 2016), meses fora do intervalo válido (1-12) e verificação de valores negativos.

---

## 💡 Principais Insights & Recomendações

* **Distrito Crítico:** **Westminster** lidera com folga o volume acumulado de ocorrências (~386 mil registros no período).
* **Predominância por Categoria:** *Burglary* (roubos) representa a maioria esmagadora das ocorrências nos distritos prioritários, sendo o grande gargalo de Westminster.
* **Ponto de Atenção Temporal:** A categoria *Violence Against the Person* (violência contra a pessoa) apresentou tendência constante de crescimento ao longo dos anos, exigindo monitoramento preventivo prioritário.
* **Recomendação Estratégica:** Direcionar reforço e policiamento ostensivo focado em *Burglary* nos distritos de maior incidência (*Westminster, Lambeth e Southwark*), enquanto são implementadas políticas preventivas específicas para conter a curva ascendente de crimes violentos.

---

## 📁 Estrutura de Arquivos do Repositório

```text
├── README.md                           <-- Documentação do projeto
├── Tarefa EBAC crimes Londres.pbix      <-- Arquivo do Power BI
├── Tarefa EBAC crimes Londres.pdf        <-- Versão em PDF do Dashboard
└── Tarefa EBAC crimes Londres.py <-- Script Python/SQL de conexão e validação
