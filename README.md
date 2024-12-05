# Portfolio_Estoque_Modelagem_de_Dados

# Sobre o projeto

Empresas que lidam com grande volume de produtos em seus estoques necessitam de controle constante desses itens. No contexto hospitalar, esse controle é muito requisitado visto o impacto da falta de seus produtos.

Com esse contexto em mente, foi proposto esse projeto para explorar como organizar os dados de controle de um estoque, mais especificamente como melhorar a disposição de tais informações a partir da Modelagem e Normalização dos Dados. Além da revisão da organização, também foi realizada a aplicação desses dados em um dashboard, simulando a possibilidade de análise deles.

Considerando o uso comum do **Microsoft Excel** para controle de dados, mesmo havendo possibilidades mais adequadas, nesse projeto foi escolhido trabalhar nessa situação partindo e entregando os dados em arquivo de **Excel**.

Assim, o projeto foi dividido em duas partes:

**Parte 1**: Foco na construção da **Modelagem e Normalização dos Dados**, construindo modelo físico da modelagem voltada para o **Excel**.

**Parte 2**: Centrada na construção do **Dashboard** usando **PowerBI**, explorando a análise dos dados.

# Sobre o conjunto de dados

Os dados usando nesse projeto são totalmente fictícios e criados com ajuda da IA Gemini. 

Foi estabelecida inicialmente uma única tabela com os dados de estoque. Para mais detalhes, conferir o arquivo “Estoque_Modelagem_de_dados_PARTE_1” no repositório no GitHub.

| Código | Nome do Produto | Fabricante | Quantidade em Estoque | Data de Validade | Departamento que Utiliza | Unidade de Medida | Lote | Fornecedor | Categoria do produto | Quantidade mínima em estoque | Data da Última Compra |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P001 | Seringa 5ml | BD | 120 | 31/12/2024 | Pronto-Socorro | Caixa com 10 unidades | L1234 | Distribuidora Médica | Materiais para injeção | 50 | 01/01/2024 |
| P002 | Bandagem 5cm x 10m | Johnson & Johnson | 45 | 30/06/2025 | Cirurgia | Rolo | L2345 | Mega Farmácia | Materiais para curativo | 20 | 15/02/2024 |
| P003 | Álcool 70% | White Martins | 250 | 31/12/2024 | Pronto-Socorro | Litro | L3456 | Química Industrial | Produtos de limpeza | 100 | 20/03/2024 |

Dessa forma, ficaram evidentes problemas com a organização, manutenção e atualização desses dados:

- **Repetição de dados:** O código do produto e o fabricante se repetem em várias linhas, o que aumenta o risco de inconsistências.
- **Dependências funcionais inadequadas:** A quantidade em estoque, data de validade e unidade de medida dependem do produto e do departamento que utiliza.
- **Facilidade de inconsistências:** Alterar a informação de um produto em uma linha pode não ser refletido em outras linhas.
- **Dificuldade de manutenção:** A tabela se torna difícil de manter e atualizar, pois as informações estão dispersas.
- **Desperdício de espaço:** A repetição de dados ocupa mais espaço de armazenamento.

# Objetivo e questões norteadoras

Visando a resolução dos problemas encontrados, ao longo desse trabalho, foi construído e entregue um **modelo de físico e normalizado do conjunto de dados** com foco de uso em **Excel** e um **Dashboard** usando **PowerBI.**

### **Objetivo**

Explorar os diferentes conceitos da Modelagem e Normalização de dados, assim como a aplicação das informações tratadas em um Dashboard.

**Para a elaboração do dashboard, foram consideradas as seguintes questões:**

- Quantos produtos há por categoria?
- Quantos produtos estão com estoque abaixo do mínimo, tanto em valor absoluto quanto relativo?
- Qual departamento mais utiliza os produtos es estoque?
- Há quantos pedidos de reposição por período?
- Qual a média de tempo entre a realização do pedido de reposição e a previsão de entrega?
