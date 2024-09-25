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