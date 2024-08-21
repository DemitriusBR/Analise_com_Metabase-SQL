# Projeto de Análise de Leads

## Visão Geral

Este projeto tem como objetivo desenvolver uma solução de análise de dados para otimizar o processo de gerenciamento de leads e melhorar as estratégias de vendas. Utilizamos dados provenientes de várias fontes para criar dashboards interativos que permitem à equipe de negócios gerar planos de ação eficazes para aumentar a conversão e o crescimento da empresa.

## Estrutura dos Dados

Os dados utilizados no projeto estão divididos em várias tabelas, cada uma com informações específicas sobre os leads, interações e respostas a demonstrações. Abaixo está uma visão geral das tabelas e suas principais colunas:

### `leads_basic_details`
- **lead_id**: Identificador único do lead. [string]
- **age**: Idade do lead. [int]
- **gender**: Sexo do lead. [string]
- **current_city**: Cidade de residência do lead. [string]
- **current_education**: Detalhes da educação atual do lead. [string]
- **parent_occupation**: Ocupação do pai do lead. [string]
- **lead_gen_source**: Fonte a partir da qual o lead é gerado. [string]

### `sales_managers_assigned_leads_details`
- **snr_sm_id**: Identificador único do gerente de vendas sênior. [string]
- **jnr_sm_id**: Identificador único do gerente de vendas júnior. [string]
- **assigned_date**: Data em que os leads foram atribuídos ao gerente de vendas júnior. [data]
- **cycle**: Ciclo em que o lead é atribuído. [string]
- **lead_id**: Identificador único do lead. [string]

### `leads_interaction_details`
- **jnr_sm_id**: Identificador único do gerente de vendas júnior. [string]
- **lead_id**: Identificador único do lead. [string]
- **lead_stage**: Estágio do lead quando contatado pelo gerente de vendas júnior. Pode ser "leadership", "awareness", "consideration", "conversion". [string]
- **call_done_date**: Data da chamada feita para o lead pelo gerente de vendas júnior. [data]
- **call_status**: Status da chamada feita ao lead. "successful" se o lead atender, "unsuccessful" em todos os outros casos. [string]
- **call_reason**: Motivo para ligar para o lead. [string]

### `leads_demo_watched_details`
- **lead_id**: Identificador único do lead. [string]
- **demo_watched_date**: Data em que a sessão de demonstração é assistida pelo lead. [data]
- **language**: Idioma em que a sessão de demonstração é assistida pelo lead. Pode ser "English", "Telugu" ou "Hindi". [string]
- **watched_percentage**: Porcentagem da sessão assistida pelo lead (de 100). [float]

### `leads_reasons_for_no_interest`
- **lead_id**: Identificador único do lead. [string]
- **reasons_for_not_interested_in_demo**: Motivo declarado pelo lead para a falta de interesse em assistir à sessão de demonstração. [string]
- **reasons_for_not_interested_in_consideration**: Motivo declarado pelo lead para não considerar o produto como uma solução. [string]
- **reasons_for_not_interested_in_conversion**: Motivo declarado pelo lead para a falta de interesse em conversão. [string]

## Processo de Desenvolvimento

O desenvolvimento do projeto foi realizado em várias etapas, utilizando SQL para consultar e manipular os dados e Metabase para criar dashboards interativos. A seguir está um resumo das principais etapas e técnicas utilizadas:

### 1. Configuração do Ambiente
- **Ferramentas Utilizadas**: Metabase para consultas SQL e criação de dashboards.
- **Objetivo**: Integrar as tabelas de dados e preparar o ambiente para consultas e visualizações.

### 2. Consultas SQL
Realizamos consultas SQL para extrair os dados necessários para análise e visualização. As consultas incluíram:
```sql
SELECT * FROM leads_basic_details;
SELECT * FROM sales_managers_assigned_leads_details;
SELECT * FROM leads_interaction_details;
SELECT * FROM leads_demo_watched_details;
SELECT * FROM leads_reasons_for_no_interest;
```
## 3. Criação de Dashboards

Desenvolvemos dashboards no Metabase para visualizar e analisar os dados. As etapas foram:

### Etapa 01: Gráfico de Pizza
- **Objetivo**: Visualizar a distribuição de leads por fonte de genero.
- **Tabela**: `leads_basic_details`
- **Códgio utilizado** :
  
![image](https://github.com/user-attachments/assets/c91cf3e0-9042-4264-8a8d-24ae00306599)


### Etapa 02: Gráfico de Cartão
- **Objetivo**: Exibir métricas agregadas sobre a idade dos leads.
- **Tabela**: `leads_basic_details`
- **Códgio utilizado** :

![image](https://github.com/user-attachments/assets/0d111a56-229b-4fd7-8e49-0895e817f52c)


### Etapa 03: Gráfico de Barras
- **Objetivo**: Comparar o número de leads por escolaridade.
- **Tabela**: `leads_basic_details`
- **Códgio utilizado** :

![image](https://github.com/user-attachments/assets/2a11c7bf-2246-4f52-806c-83536b36f3cd)


### Etapa 04: Tabela de Médias
- **Objetivo**: Exibir a média de "porcentagem de assistido" por idioma, apenas para valores maiores que 0.5.
- **Tabela**: `leads_demo_watched_details`
- **Códgio utilizado** :

![image](https://github.com/user-attachments/assets/ac3e328b-1a28-4a1c-b8f3-26e6a8935e7e)


### Etapa 05: Gráfico de Linhas
- **Objetivo**: Mostrar a quantidade de ligações atendidas ao longo do tempo, por plataforma.
- **Tabelas**: `leads_basic_details`, `leads_interaction_details`
- **Códgio utilizado** :

![image](https://github.com/user-attachments/assets/004efee0-0115-4fe1-8051-8eea995a13bf)


