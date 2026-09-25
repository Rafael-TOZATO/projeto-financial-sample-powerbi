# 📊 Financial Sample — Modelagem Dimensional com Power BI

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Analytics-F2C811?logo=powerbi&logoColor=black)
![Projeto](https://img.shields.io/badge/Projeto-DIO-blue)
![Modelo](https://img.shields.io/badge/Modelo-Star%20Schema-orange)

## Sobre o projeto

Este projeto foi desenvolvido a partir do desafio da DIO **“Integrando Dados com MySQL Azure e Transformando com Power BI”**, utilizando a base **Financial Sample**.

O objetivo foi transformar uma tabela única de origem em um modelo dimensional organizado no formato **Star Schema**, separando informações de dimensões e fatos e realizando as transformações necessárias para análise dos dados no Power BI.

## Objetivos

- Estruturar os dados em um modelo dimensional.
- Criar tabelas de dimensão e fato.
- Organizar e transformar os dados utilizando Power Query.
- Criar a dimensão calendário com DAX.
- Estruturar os relacionamentos do modelo.
- Reorganizar as colunas para facilitar a análise.
- Documentar o processo de construção do modelo.
- Desenvolver uma estrutura adequada para análise de dados e Business Intelligence.

## Estrutura do modelo

O projeto foi estruturado com as seguintes tabelas:

### `Financials_origem`

Tabela original utilizada como base para a construção do modelo.

Foi mantida no projeto como **backup e referência**, permanecendo oculta no modelo final.

### `D_Produtos`

Dimensão responsável pelas informações consolidadas dos produtos, incluindo:

- ID do produto
- Produto
- Média de unidades vendidas
- Média do valor de vendas
- Mediana do valor de vendas
- Valor máximo de venda
- Valor mínimo de venda

### `D_Produtos_Detalhes`

Contém informações detalhadas relacionadas aos produtos:

- ID do produto
- Discount Band
- Sale Price
- Units Sold
- Manufactoring Price

### `D_Descontos`

Dimensão relacionada às informações de desconto:

- ID do produto
- Discount
- Discount Band

### `D_Detalhes`

Tabela destinada às informações complementares que não foram contempladas nas demais dimensões, permitindo preservar detalhes relevantes da base original.

### `D_Calendário`

Dimensão de calendário criada utilizando **DAX**, por meio da função `CALENDAR()`.

A dimensão permite estruturar informações temporais para análises baseadas em datas.

### `F_Vendas`

Tabela fato responsável por concentrar os principais registros utilizados na análise de vendas, incluindo:

- ID do produto
- Produto
- Units Sold
- Sales Price
- Discount Band
- Segment
- Country
- Salers
- Profit
- Date

## Modelo Star Schema

O modelo foi organizado seguindo o conceito de **Star Schema**, mantendo a tabela fato como núcleo do modelo e as tabelas dimensionais ao seu redor.

![Modelo Star Schema](docs/modelo_estrela_power_bi.jpg)

## Processo de construção

O desenvolvimento foi realizado seguindo as etapas propostas no desafio:

1. Importação da base Financial Sample.
2. Criação de cópias da tabela original.
3. Seleção das colunas necessárias para cada dimensão.
4. Criação das tabelas dimensionais.
5. Construção da tabela fato.
6. Tratamento e transformação dos dados no Power Query.
7. Ajuste dos tipos de dados.
8. Reorganização das colunas.
9. Criação da dimensão calendário utilizando DAX.
10. Estruturação do modelo no formato Star Schema.
11. Organização visual do modelo no Power BI.
12. Salvamento do projeto `.pbix`.
13. Registro visual do modelo para documentação.
14. Documentação do projeto neste repositório.

## Power Query

Durante o processo de transformação foram realizados tratamentos como:

- definição dos tipos de dados;
- conversão de campos para texto, número e data;
- organização das colunas;
- tratamento de informações necessárias ao modelo;
- preparação das tabelas para utilização no modelo dimensional.

O Power Query foi utilizado como etapa de preparação e transformação dos dados antes da modelagem.

## DAX

A dimensão calendário foi criada utilizando a função `CALENDAR()`.

```DAX
D_Calendário =
CALENDAR(
    MIN(F_Vendas[Date]),
    MAX(F_Vendas[Date])
)
```

A função `CALENDAR()` foi utilizada para criar uma tabela contendo o intervalo de datas necessário para a análise temporal do projeto.

## Desafio técnico e solução adotada

O roteiro original propunha a utilização do **MySQL Azure** como parte do processo de integração.

Durante a execução do projeto, houve uma limitação relacionada ao processo de acesso ao ambiente Azure, que exigia uma etapa de assinatura com cartão de crédito.

Para não interromper o desenvolvimento, foi adotada uma abordagem alternativa utilizando **XAMPP, MySQL e phpMyAdmin**, permitindo trabalhar com a estrutura dos dados localmente e prosseguir com a preparação e transformação da base no Power BI.

Essa adaptação permitiu manter o foco nos principais objetivos técnicos do desafio: **tratamento de dados, modelagem dimensional, criação do Star Schema e utilização do Power BI**.

## Resultado

O resultado é um modelo dimensional estruturado para análise dos dados da Financial Sample, com separação entre dimensões e fato e documentação do processo de construção.

O projeto demonstra conhecimentos práticos em:

- Power BI;
- Power Query;
- DAX;
- modelagem dimensional;
- Star Schema;
- transformação de dados;
- organização de bases para Business Intelligence.

## Arquivos do projeto

```text
Projeto_Financial_Sample_PowerBI/
│
├── Projeto_Financial_Sample_PowerBI.pbix
├── README.md
│
└── docs/
    └── modelo_estrela_power_bi.jpg
```

## Portfólio profissional

**Portfólio:**  
https://tozato-dev-hub.vercel.app

**Medium:**  
https://medium.com/@ornelas.tozato

## Sobre

Projeto desenvolvido como parte da formação prática em **Data Analytics e Business Intelligence**, com foco em modelagem de dados, transformação e construção de modelos analíticos utilizando Power BI.

---

**Projeto desenvolvido por Rafael Ornelas Tozato**
