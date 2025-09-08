
# Business Intelligence no E-commerce **Tudo Aqui**

## Problema de Negócio
A **Tudo Aqui** é uma empresa brasileira de e-commerce em crescimento.  
Até então, suas decisões estratégicas eram tomadas de forma **intuitiva**, sem apoio em dados, o que ocasionou **prejuízos financeiros** e falta de clareza sobre a performance do negócio.  

Para mudar esse cenário, o CEO decidiu adotar a metodologia **Data Driven** e implementar uma solução de **Business Intelligence com Power BI** para embasar a tomada de decisão.  

O objetivo é estruturar **análises e dashboards** que permitam à diretoria monitorar indicadores essenciais do negócio e apoiar a definição de **estratégias de crescimento**.

**Dataset utilizado:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/code  

---

##  Contexto
- **Ferramenta escolhida:** Power BI Desktop (considerando custo-benefício).  
- **Estrutura de entregas:** cada frente de análise (Produto, Pagamentos, Pedidos, Avaliações, Vendedores e Vendas) terá **no máximo 2 dashboards**.  
- **Escopo inicial:** construção da **Visão Produto**, seguida por **Visão Pagamentos** e **Visão Pedido**.  

---

##  Modelo de Dados (Schema)

O modelo foi estruturado em formato de **Esquema Estrela (Star Schema)**, com a tabela fato  **Pedidos (orders)** no centro, conectada a uma tabela calendário.  

| **Tabela Fato** | **Tabela Dimensão** |
|-----------------|-----------------------|
| **orders (pedidos)**<br>Contém os registros de pedidos realizados, funcionando como a base central do modelo.<br>**Principais campos:** `order_id`, `customer_id`, `data de compra`, `order_approved_at`. |  **calendario (tempo)**<br>Criada manualmente, não estava presente no dataset original.<br>**Campos:** `Data`, `Ano`, `Mês`, `Ano/Mês`, `Dia da Semana`, `Nome do Mês`, `Nome do Semestre`.<br>**Relacionamento:** conecta-se a **orders** via `data de compra`.<br>**Função:** é uma **tabela dimensão de tempo**, necessária para análises temporais (ex.: evolução mensal, sazonalidade, taxa de crescimento). |

<p align="center"> <b>Modelagem dos Dados</b></p>  

<p align="center">
  <img width="817" height="319" alt="image" src="https://github.com/user-attachments/assets/3c3d7baa-b2f1-4dd2-9f50-c2863db0bcb0" />
</p>

---

## Premissas da Análise
1. O projeto será desenvolvido em etapas (**Produto → Pagamentos → Pedidos → etc.**).  
2. Os dashboards seguem as **cores e identidade visual da empresa**.  
3. Cada visão contém **segmentações interativas** para explorar os dados.  

---

## ⚙Estratégia da Solução
A solução foi estruturada em **cartões de indicadores, gráficos analíticos e segmentações**, fornecendo clareza e permitindo **investigações rápidas**.  

---

###  Visão Produto
**Solicitações do CEO:**
- Quantidade de Produtos Cadastrados.  
- Quantidade Total de Categorias.  
- Quantidade Total de Fotos.  
- Quantidade de Produtos por Categoria.  
- Quantidade de Fotos por Categoria.  
- **Segmentação:** Categoria de Produto.  

<p align="center"><b>Dashboard Visão Produto</b></p>  

<p align="center">
  <img width="600" height="502" alt="image" src="https://github.com/user-attachments/assets/3dadacdf-ec83-429a-924c-d99c8dec1d8f" />
</p>
 

---

### Visão Pagamentos
**Solicitações do CEO:**

**Cartões:**
- Quantidade de pedidos.  
- Valor total de pagamentos.  
- Quantidade de pagamentos.  
- Quantidade de pagamentos por tipo de pagamento.  

**Análises Gráficas:**
- Valor total de pagamentos (por status do pedido).  
- Quantidade de pagamentos (por tipo de pagamento).  
- Hierarquia de valor médio de pagamentos (por status e tipo).  
- Detalhes dos pedidos por tipo de pagamento.  

**Segmentações:**
- Número do pedido.  
- Tipo de pagamento.  
- Status do pedido.  

<p align="center"> <b>Dashboard Visão Pagamentos</b></p>  

<p align="center">
  <img width="600" height="501" alt="image" src="https://github.com/user-attachments/assets/94fa9375-7cc1-46f5-bcee-99582bdb5730" />
</p>

---

###  Visão Pedido
**Solicitações do CEO:**

**Cartões:**
- Quantidade de pedidos.  
- Quantidade de clientes.  
- Pedidos por ano (2017 e 2018).  
- Taxa de Crescimento (2017–2018).  

**Análises Gráficas:**
- Pedidos x Meta Anual.  
- Pedidos x Meta Mensal (2018).  
- Pedidos por Estado.  
- Detalhes da Quantidade de Pedidos (por Ano, Mês, Estado e Cidade) 
- Meta de Pedidos (por Ano, Mês, Estado e Cidade) 

**Segmentações:**
- Data de Compra.  
- Ano/Mês.  
- Estado e Cidade do Cliente.  
- Status do Pedido.  

<p align="center"><b>Dashboard Visão Pedidos</b></p>  

<p align="center">
 <img width="600" height="501" alt="image" src="https://github.com/user-attachments/assets/9ab1baa5-891f-4f01-9c6e-07d12e8e498b" />
</p>

---

## Insights da Análise
- **Produto:** o catálogo é amplo, mas algumas categorias concentram a maior parte dos produtos e fotos, indicando potencial foco para campanhas.  
- **Pagamentos:** predominância de determinados meios de pagamento; análise por status mostra gargalos em alguns fluxos.  
- **Pedidos:** crescimento consistente entre 2017 e 2018, com destaque para alguns estados que concentram a maior parte dos pedidos.  

---

## Resultados
A adoção do **Power BI** permitiu à **Tudo Aqui**:  
- Reduzir a dependência de decisões intuitivas.  
- Acompanhar indicadores críticos em tempo real.  
- Identificar padrões de comportamento de clientes e operações.  
- Apoiar a diretoria na definição de **metas e estratégias baseadas em dados**.  

---

##  Próximos Passos
1. Expandir as análises para as próximas frentes: **Avaliações, Vendedores e Vendas**.  
2. Criar **painéis de acompanhamento contínuo** (atualização automática de dados).  
3. Explorar análises temporais mais avançadas (**sazonalidade e previsões**).  
4. Implementar comparativos com metas em todas as visões.  

---
