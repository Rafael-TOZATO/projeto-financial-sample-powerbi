<p align="center">
  <img src="star-schema-power-bi-modelagem-dimensional-banner.png" alt="Star Schema Power BI Modelagem Dimensional Banner" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-AI%20Engineer-success?style=for-the-badge&logo=git" alt="Status">
  <img src="https://img.shields.io/badge/Qualidade-ISO%209001-blue?style=for-the-badge&logo=checkmarx&logoColor=white" alt="ISO 9001">
  <img src="https://img.shields.io/badge/Governança-Indústria%204.0-orange?style=for-the-badge&logo=databricks&logoColor=white" alt="Indústria 4.0">
  <img src="https://img.shields.io/badge/Python-%20AI-yellow?style=for-the-badge&logo=python&logoColor=white" alt="Python & IA">
  <img src="https://img.shields.io/badge/Lean%20Six%20Sigma-Green%20Belt-purple?style=for-the-badge&logo=ercot&logoColor=white" alt="Lean Six Sigma">
  <img src="https://img.shields.io/badge/CI%2FCD-Active-success?style=for-the-badge&logo=githubactions&logoColor=white" alt="CI/CD">
  <img src="https://img.shields.io/badge/CodeQL-Protected-blue?style=for-the-badge&logo=github&logoColor=white" alt="CodeQL">
  <img src="https://img.shields.io/badge/Auto--Merge-Streamlined-informational?style=for-the-badge&logo=git&logoColor=white" alt="Auto-Merge">
  <img src="https://img.shields.io/badge/Governan%C3%A7a-4.0-critical?style=for-the-badge&logo=appveyor&logoColor=white" alt="Governança 4.0">
  <img src="https://img.shields.io/badge/Security-Secured%20%26%20Verified-success?style=for-the-badge&logo=security&logoColor=white" alt="Security">
</p>

<h1 align="center">Financial Sample — Modelagem Dimensional com Power BI</h1>

<p align="center">
  <a href="https://www.microsoft.com/en-us/power-platform/products/power-bi">
    <img src="https://img.shields.io/badge/Power%20BI-Data%20Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI">
  </a>
  <a href="https://github.com/Rafael-TOZATO/projeto-financial-sample-powerbi/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="License MIT">
  </a>
</p>

## 📌 Sobre o Projeto

Este projeto foi desenvolvido a partir do desafio da DIO **“Integrando Dados com MySQL Azure e Transformando com Power BI”**, utilizando a base **Financial Sample**.

O objetivo foi transformar uma tabela única de origem em um modelo dimensional organizado no formato **Star Schema**, separando informações de dimensões e fatos e realizando as transformações necessárias para análise avançada de dados e Business Intelligence.

## 🎯 Objetivos

- Estruturar os dados em um modelo dimensional corporativo.
- Criar tabelas de dimensão e fato otimizadas.
- Organizar e transformar os dados utilizando o Power Query.
- Criar a dimensão calendário utilizando fórmulas DAX.
- Estruturar os relacionamentos eficientes do modelo.
- Reorganizar colunas e tipos de dados para facilitar a análise de negócios.
- Documentar todo o processo de construção e modelagem dimensional.

## 🗄️ Estrutura do Modelo

O projeto foi estruturado com as seguintes tabelas:

- **`Financials_origem`**: Tabela original utilizada como base para a construção do modelo. Mantida no projeto como *backup e referência*, permanecendo oculta no modelo final.
- **`D_Produtos`**: Dimensão responsável pelas informações consolidadas dos produtos (ID, nome, médias de unidades e valores de vendas, mediana e extremos).
- **`D_Produtos_Detalhes`**: Informações complementares relacionadas aos produtos (*Discount Band*, *Sale Price*, *Units Sold*, *Manufacturing Price*).
- **`D_Descontos`**: Dimensão dedicada às regras e informações de desconto associadas.
- **`D_Detalhes`**: Tabela destinada a informações complementares não contempladas nas demais dimensões, preservando a integridade da base original.
- **`D_Calendário`**: Dimensão de calendário criada via **DAX** utilizando a função `CALENDAR()`, estruturando o eixo temporal das análises.
- **`F_Vendas`**: Tabela fato central que concentra os principais registros quantitativos e métricas de vendas, unindo todas as chaves dimensionais.

## 🌟 Modelo Star Schema

O modelo foi organizado seguindo o conceito de **Star Schema** (Esquema Estrela), mantendo a tabela fato como o núcleo de transações cercada pelas tabelas dimensionais normalizadas.

> *Ilustração estrutural do modelo disponível no diretório `docs/modelo_estrela_power_bi.jpg`.*

## ⚙️ Processo de Construção e Pipeline

1. **Importação:** Carga inicial da base *Financial Sample*.
2. **Duplicação:** Criação de referências para a base original para extração das dimensões.
3. **Modelagem:** Separação estruturada entre tabelas de Dimensão e Fato.
4. **Transformação (Power Query):** Tratamento de tipos de dados, limpeza de colunas e padronização.
5. **DAX:** Implementação de colunas calculadas e da tabela dinâmica de calendário.
6. **Relacionamentos:** Estabelecimento de cardinalidade e direção de filtro no Power BI.
7. **Documentação:** Organização e versionamento do arquivo `.pbix` e dos artefatos visuais.

## 🛡️ Governança 4.0 — Segurança e Qualidade

Este repositório adota controles automatizados de Governança 4.0 para assegurar integridade dos artefatos e do código, rastreabilidade das alterações, gestão de dependências e prevenção de exposição de credenciais.

* **Automação de Qualidade e Segurança:** Análises automatizadas e portas de verificação (*status checks*) ativas em segundo plano.
* **Fluxo Sem Atrito:** Dispensa de aprovações manuais redundantes com *auto-merge* habilitado para agilizar entregas.
* **Integridade de Código:** Proteção de branch e bloqueio de *force pushes* para garantir a estabilidade da base principal.

## 📬 Contatos e Canais

- **GitHub:** [Rafael-TOZATO](https://github.com/Rafael-TOZATO)
- **LinkedIn:** [rafaeltozato81](https://www.linkedin.com/in/rafaeltozato81)
- **Medium:** [@ornelas.tozato](https://medium.com/@ornelas.tozato)
- **Dev Hub:** [tozato-ai-core.vercel.app](https://tozato-ai-core.vercel.app)
- **H-Folio:** [h-folio-l0.vercel.app](https://h-folio-l0.vercel.app)
- **Microsoft Learn:** [rafaelornelastozato-2209](https://learn.microsoft.com/pt-br/users/rafaelornelastozato-2209)
- **E-mail:** ornelas.tozato@gmail.com
