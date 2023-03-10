# Business Intelligence - ETL e Carga Incremental com Pentaho Data Integration e Pentaho Server

Projeto Desenvolvido no Pentaho Data Integration de ETL e carga. Onde foi criado stages, dimensões, fato, data warehouse e um Job principal para executar a carga incremental via Pentaho Server.

1) O projeto se inicia através da organização primeiramente da Stage Area.

Stage das Tabelas Dimensões:

- Stage Clientes
- Stage Detalhe dos Pedidos
- Stage Pedidos
- Stage Produtos

Stage da Tabela Fato:

Stage Fato Pedidos

2) Job das Stages para envio dos dados semi tratados das stages para o Banco de dados nesse exemplo chamado de 'stg' no HeidiSQL.

3) A partir dos stages é criado o Data Warehouse, com chaves específicas criadas para cada tabela Dimensão e Fato carregado a partir de um 2 Job's. 

4) Carregamento das tabelas Dimensão e Fato no DW e criação de uma nova Dimensão Calendário. 

5) Lookup das tabelas e criação de tabelas de Log.

6) Criação da carga incremental nesse exemplo realizado com Merge diff, atualizando somente os dados alterados e mantendo o restante dos dados iguais. 

7) Criação de um Job principal para executar todas as tranformações e cargas de forma otimizada.

8) Conexão com Pentaho Server e gerar agendamento da carga incremental. 




1. Stage Area


Stage Dimensão Cliente

![stg1](https://user-images.githubusercontent.com/109915092/213242116-ac9ae94e-08bf-4786-978a-6b39a6a7abf0.png)

Stage Dimensão Detalhe do Pedidos

![stg2](https://user-images.githubusercontent.com/109915092/213245972-b1ae474b-5792-4adf-9bba-8b6292ee500f.png)

Stage Dimensão Pedidos

![stg3](https://user-images.githubusercontent.com/109915092/213252561-7948b9af-25e6-499d-b374-637a1cff7f58.png)


Stage Dimensão Produtos

![stg4](https://user-images.githubusercontent.com/109915092/213253037-ce48dc17-337a-4d74-b550-7e99555693c8.png)

Stage Fato Pedidos

![stg5](https://user-images.githubusercontent.com/109915092/213253417-cd081ac5-5b1e-4240-97d2-f322d5d959d5.png)


2. Job das Stages carregado no SQL

![Job Stages](https://user-images.githubusercontent.com/109915092/213254997-ab174490-d786-4a31-8800-b31423129c8f.png)

![Heidisql](https://user-images.githubusercontent.com/109915092/213309438-59d960a6-65a0-4595-9031-9a6e57330bab.png)


3. Criação das Tabelas Dimensão e Fato e posteriormente o carregamento dos dados no Dataware House 

Dimensão Cliente

![dim cliente](https://user-images.githubusercontent.com/109915092/213872209-b607883e-64b4-400a-985a-a918ba4358c0.png)

Dimensão Pedidos

![dim pedidos](https://user-images.githubusercontent.com/109915092/213872309-03cb566a-7bc3-4f11-acf7-072373381e23.png)

Dimensão Produtos

![dim produtos](https://user-images.githubusercontent.com/109915092/213872402-bf760b56-ff63-4a8a-99cd-258a83b5b69c.png)

Criação Dimensão Calendário 

![dim calendario](https://user-images.githubusercontent.com/109915092/213872572-d8685868-96ed-4946-a9e4-617e68e4be46.png)

Fato Pedidos

![fato pedidos](https://user-images.githubusercontent.com/109915092/213872678-c3f44a9f-a911-4ebe-852d-76be01071203.png)

Job para carregamento das Tabelas Dimensões no DW

![job dimensoes](https://user-images.githubusercontent.com/109915092/213872917-d7b37699-653f-47bd-8f91-a1cf8b70f577.png)

Job para carregamento da Tabela Fato no DW

![Job fato](https://user-images.githubusercontent.com/109915092/213873062-3d2e0bac-3734-466d-a056-ff99a904bc64.png)

![image](https://user-images.githubusercontent.com/109915092/213873157-94caed47-76ad-4e98-981e-e08aff3c628a.png)

Job Principal executando de forma automatizada todas as etapas desenvolvidas até o momento

![job principal](https://user-images.githubusercontent.com/109915092/213875384-562c4138-4d6f-4439-81ba-57eaf1a3c34f.png)


Conexão com Pentaho Server

![conexao pentaho server](https://user-images.githubusercontent.com/109915092/213875552-ff36ad53-79f6-4e9d-970c-6f3101a09013.png)

![concetado pentaho server](https://user-images.githubusercontent.com/109915092/213875619-231a6c49-7dae-48c7-804d-68725f47cf11.png)

![navegador pentaho server](https://user-images.githubusercontent.com/109915092/213875686-4e66e05f-950d-4650-a14b-f52b3a3fda63.png)


 Job Principal conectado ao Pentaho Server
 
 ![job principal pentaho server](https://user-images.githubusercontent.com/109915092/213876015-3f29d4e3-ba4f-4875-aa81-15713e354158.png)
 
 Agendamento da Carga Incremental (automizar processos e atualizações diárias)
 
 ![agendamento carga pentaho server](https://user-images.githubusercontent.com/109915092/213876186-2989ca08-90ec-48cf-9ede-329f1851032d.png)


