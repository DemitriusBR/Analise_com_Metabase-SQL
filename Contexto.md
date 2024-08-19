# **Contexto**


## Descrição 
No competitivo setor de Edtech, onde a inovação e a aquisição de clientes desempenham papéis cruciais, nossa empresa está focada em acelerar seu crescimento aumentando a base de usuários cadastrados. Como analista de dados, a tarefa é utilizar a análise de dados para identificar padrões e oportunidades que possam impulsionar a estratégia de aquisição e conversão de clientes.

Para alcançar esses objetivos, desenvolvemos um dashboard avançado utilizando SQL, que integra e analisa informações cruciais sobre nossos leads. A análise dos dados coletados permite não apenas entender o status atual do crescimento de novos usuários, mas também definir estratégias e ações direcionadas para melhorar a eficácia dos processos de vendas e marketing.

O foco principal é explorar e avaliar vários aspectos da aquisição de leads, desde a geração inicial até a conversão final, passando pela interação e o engajamento com as demonstrações do produto. Com base nos dados, identificamos os pontos fortes e as áreas que necessitam de melhorias, oferecendo insights que ajudam a moldar a estratégia da empresa para o próximo ano.

A análise dos dados é fundamental para alcançar uma compreensão profunda de como diferentes segmentos de leads reagem às nossas estratégias de marketing e vendas, e como podemos ajustar nossas abordagens para maximizar a eficiência e o impacto. Através da implementação das recomendações derivadas das análises, esperamos não apenas aumentar a quantidade de leads convertidos, mas também melhorar a experiência geral dos clientes, ajustando nossa oferta para atender melhor às suas necessidades e expectativas.

## Sobre os Dados

Os dados disponíveis para a análise são extraídos de várias tabelas interconectadas, que fornecem uma visão abrangente do ciclo de vida dos leads. A seguir, uma descrição detalhada das tabelas e seus componentes:

### 1. `leads_basic_details`

Esta tabela contém informações fundamentais sobre cada lead, como:
- **lead_id**: Identificador único do lead.
- **age**: Idade do lead, que pode ajudar a identificar os segmentos demográficos mais promissores.
- **gender**: Sexo do lead, útil para segmentar campanhas e ofertas.
- **current_city**: Cidade de residência, importante para estratégias de marketing localizadas.
- **current_education**: Nível de educação, que pode influenciar o tipo de oferta ou conteúdo relevante.
- **parent_occupation**: Ocupação dos pais, fornecendo contexto adicional sobre o background socioeconômico.
- **lead_gen_source**: Fonte de origem do lead, crucial para avaliar a eficácia das campanhas de marketing.

### 2. `sales_managers_assigned_leads_details`

Esta tabela rastreia a alocação de leads para os gerentes de vendas, com detalhes como:
- **snr_sm_id**: ID do gerente de vendas sênior responsável pela supervisão.
- **jnr_sm_id**: ID do gerente de vendas júnior que lida diretamente com o lead.
- **assigned_date**: Data em que o lead foi atribuído ao gerente de vendas júnior.
- **cycle**: Ciclo em que o lead foi atribuído, oferecendo insights sobre a carga de trabalho e a gestão de leads.

### 3. `leads_interaction_details`

Esta tabela detalha as interações com os leads, incluindo:
- **jnr_sm_id**: ID do gerente de vendas júnior responsável pela interação.
- **lead_id**: Identificador único do lead.
- **lead_stage**: Estágio do lead (liderança, conscientização, consideração, conversão), crucial para entender o progresso e as necessidades de cada lead.
- **call_done_date**: Data da chamada, que pode ajudar a analisar a eficiência das interações.
- **call_status**: Status da chamada (successful, unsuccessful), para avaliar a eficácia das abordagens.
- **call_reason**: Motivo da chamada, ajudando a identificar quais razões são mais eficazes em cada estágio.

### 4. `leads_demo_watched_details`

Informações sobre as demonstrações assistidas pelos leads estão nesta tabela:
- **lead_id**: Identificador único do lead.
- **demo_watched_date**: Data em que a demonstração foi assistida, importante para entender o engajamento.
- **language**: Idioma da demonstração, relevante para adaptar o conteúdo às preferências dos leads.
- **watched_percentage**: Porcentagem da demonstração assistida, útil para avaliar o interesse e o envolvimento.

### 5. `leads_reasons_for_no_interest`

Esta tabela oferece detalhes sobre as razões para a falta de interesse dos leads:
- **lead_id**: Identificador único do lead.
- **reasons_for_not_interested_in_demo**: Motivo para a falta de interesse na demonstração.
- **reasons_for_not_interested_in_consideration**: Motivo para não considerar o produto.
- **reasons_for_not_interested_in_conversion**: Motivo para a falta de interesse na conversão.
