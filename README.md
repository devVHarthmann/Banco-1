# Banco1

## Exercicio 1
 
```sql
--Criar tabela clientes. 
CREATE TABLE Cliente (
    id_cliente INT PRIMARY KEY AUTO_INCREMENT,
    nome_cliente VARCHAR(100),
    email VARCHAR(50),
    data_nascimento DATE,
    telefone VARCHAR(15)
);
```
## Exercicio 2

```sql
--Criar tabela produtos.
CREATE TABLE produtos (
    id_produto INT PRIMARY KEY,
    nome_produto VARCHAR(100) NOT NULL UNIQUE,
    preco_produto DECIMAL(8 , 2 )
);
```
## Exercicio 3  

```sql
--Criar tabela faturas.
CREATE TABLE faturas (
    id_fatura INT PRIMARY KEY,
    data_criaçao timestamp DEFAULT CURRENT_TIMESTAMP,
    valor_fatura DECIMAL(10 , 2 )
);
```

# Exercicios Complementares

```sql
use bdteste;
-- Crie uma tabela chamada "Funcionarios" com os campos ID (chave primária), Nome, Sobrenome e Salário.
CREATE TABLE Funcionarios(
	ID int primary key,
    Nome varchar(50),
    Sobrenome varchar(50),
    Salario double(10,2)
);
-- Adicione uma coluna chamada "DataNascimento" à tabela "Funcionarios" para armazenar a data de nascimento dos funcionários.
ALTER TABLE Funcionarios add DataNascimento date;
-- Crie uma nova tabela chamada "Departamentos" com os campos ID (chave primária) e Nome.
CREATE TABLE Departamentos(
	ID int primary key,
    Nome varchar(50)
);
-- Adicione uma coluna chamada "IDDepartamento" à tabela "Funcionarios" para associar cada funcionário a um departamento.
ALTER TABLE Funcionarios add IDDepartamento int;
-- Crie uma tabela chamada "Projetos" com os campos ID (chave primária) e NomeProjeto.
CREATE TABLE Projetos(
	ID int primary key,
    NomeProjeto varchar(50)
);
-- Crie uma tabela chamada "Alocacoes" com os campos ID (chave primária), IDFuncionario e IDProjeto.
CREATE TABLE Alocacoes(
	ID int primary key
);
-- Renomeie a coluna "Sobrenome" da tabela "Funcionarios" para "Apelido".
ALTER TABLE Funcionarios rename column Sobrenome to Apelido;
-- Crie uma tabela chamada "Clientes" com os campos ID (chave primária) e NomeCliente.
CREATE TABLE Clientes(
	Id int primary key,
    NomeCliente varchar(50)
);
-- Adicione uma coluna chamada "IDCliente" à tabela "Projetos" para associar cada projeto a um cliente.
ALTER TABLE Projetos add IDCliente int;
-- Crie uma tabela chamada "Enderecos" com os campos ID (chave primária), Rua, Cidade e CEP.
CREATE TABLE Enderecos(
	ID int primary key,
    Rua varchar(50),
    Cidade varchar(50),
    CEP int(8)
);
-- Adicione uma coluna chamada "IDEndereco" à tabela "Funcionarios" para armazenar o endereço de cada funcionário.
ALTER TABLE Funcionarios add IDEndereco int;
-- Renomeie a coluna "NomeCliente" da tabela "Clientes" para "NomeEmpresa".
ALTER TABLE Clientes rename column NomeCliente to NomeEmpresa;
-- Crie uma tabela chamada "Pedidos" com os campos ID (chave primária) e DataPedido.
CREATE TABLE Pedidos(
	ID int primary key,
    dataPedido date
);
-- Adicione uma coluna chamada "IDCliente" à tabela "Pedidos" para associar cada pedido a um cliente.
ALTER TABLE Pedidos add IDCliente int;
-- Crie uma tabela chamada "ItensPedido" com os campos ID (chave primária), IDPedido e IDProduto.
CREATE TABLE ItensPedidos(
	ID int primary key,
    IDPedido int,
    IDProduto int
);
-- Crie uma tabela chamada Produtos com os campos ID, NomeProduto, QantidadeProduto e ValorProduto.
CREATE TABLE Produtos(
	ID int primary key,
    NomeProduto varchar(50),
    QuantidadeProduto int,
    ValorProduto double
);
-- Renomeie a coluna "NomeProduto" da tabela "Produtos" para "DescricaoProduto".
ALTER TABLE Produtos rename column NomeProduto to DescricaoProduto;


-- Crie uma tabela chamada "Estoques" com os campos ID (chave primária) e Quantidade.
CREATE TABLE Estoques(
	ID int primary key,
    Quantidade int
);
-- Adicione uma coluna chamada "IDProduto" à tabela "Estoques" para associar cada item de estoque a um produto.
ALTER TABLE Estoques add IDProduto int;
-- Crie uma tabela chamada "Vendas" com os campos ID (chave primária) e DataVenda.
CREATE TABLE Vendas(
	ID int primary key,
    DataVenda date
);
-- Adicione uma coluna chamada "IDCliente" à tabela "Vendas" para associar cada venda a um cliente.
ALTER TABLE Vendas add IDCliente int;
```