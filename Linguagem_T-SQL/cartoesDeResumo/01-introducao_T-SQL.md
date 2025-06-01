# Conceitos de SQL 🎓

## **SQL (Structured Query Language)**
    - Linguagem utilizada para manipular e consultar dados em bancos de dados relacionais.
    - Usado para criar, atualizar, excluir e recuperar informações.
    - Suportado por diversos sistemas como **Microsoft SQL Server, MySQL, PostgreSQL, MariaDB e Oracle**.



    🔹 **Exemplo lúdico:** Pense no SQL como um garçom em um restaurante 🍽️. Você (cliente) faz 
        um pedido (consulta SQL) e ele retorna exatamente o prato que você pediu (dados da consulta). 



    🔹 **Exemplo prático:** Utilizar `SELECT * FROM Clientes WHERE Cidade = 'São Paulo';` para 
        obter todos os clientes que moram em São Paulo.



## **Padrão ANSI SQL**
    - Define regras para manter compatibilidade entre diferentes sistemas de bancos de dados.
    - Cada fornecedor pode adicionar extensões próprias ao SQL.



    🔹 **Exemplo lúdico:** Imagine um jogo de tabuleiro 🎲 com regras básicas, mas cada grupo de 
        jogadores adiciona suas próprias variações.  



    🔹 **Exemplo prático:** O **T-SQL (Transact-SQL)** é uma extensão do SQL usada pelo 
        Microsoft SQL Server para oferecer funcionalidades avançadas.



## **Transact-SQL (T-SQL)**
    - Dialeto do SQL usado em bancos de dados da Microsoft.
    - Permite a criação de **procedimentos armazenados** e **gestão de usuários**.



    🔹 **Exemplo lúdico:** Pense no T-SQL como um superpoder do SQL 🦸. Além de fazer consultas, ele pode automatizar tarefas e reforçar a segurança dos dados.  



    🔹 **Exemplo prático:** Criar um procedimento armazenado para inserir novos clientes no 
        banco: 

        ```sql
        CREATE PROCEDURE AddCliente (@Nome VARCHAR(50), @Cidade VARCHAR(50))
        AS
        INSERT INTO Clientes (Nome, Cidade) VALUES (@Nome, @Cidade);
        ```  



## **Linguagem Declarativa vs Procedural**
    - Linguagem declarativa (como SQL): Define o que precisa ser feito, sem especificar como.
    - Linguagem procedural: Especifica cada etapa para alcançar um resultado.



    🔹 **Exemplo lúdico**: Pedir uma pizza 🍕 declarativamente: "Quero uma pizza de calabresa."
        Pedir proceduralmente: "Pegue a massa, espalhe molho, adicione calabresa, asse no forno...".



    🔹 **Exemplo prático**: No SQL, você escreve SELECT * FROM Produtos WHERE Preco < 50;, 
        e o banco de dados decide como executar a consulta de forma eficiente



## **Dados Relacionais e Chaves**
    - Um banco de dados relacional organiza dados em tabelas interligadas.
    - Cada tabela tem uma chave primária única e pode conter chaves estrangeiras para conectar dados.



    🔹 **Exemplo lúdico**: Um álbum de figurinhas 📖 onde cada página representa uma entidade
        (cliente, produto, pedido) e os números das figurinhas conectam os dados.



    🔹 **Exemplo prático**:
        - Tabela Cliente com CustomerID (chave primária).
        - Tabela Pedidos com OrderID (chave primária) e CustomerID (chave estrangeira) para indicar qual cliente fez o pedido.



## **Processamento Baseado em Conjunto**
    - SQL trabalha com conjuntos de dados em massa, em vez de manipular uma linha por vez.
    - Operações ocorrem simultaneamente, melhorando eficiência.



    🔹 **Exemplo lúdico**: Um show de mágica 🎩 onde todas as cartas aparecem ao mesmo tempo, e
        não uma por uma.



    🔹 **Exemplo prático**:
        Em vez de percorrer clientes um por um, você pode atualizar todos ao mesmo tempo:

        ```sql
        UPDATE Clientes SET Status = 'Ativo' WHERE UltimaCompra > '2025-01-01';
        ```



## **Ordenação de Resultados**
    - Os dados em bancos relacionais não possuem uma ordem fixa.
    - Para garantir ordenação, use ORDER BY.



    🔹 **Exemplo lúdico**: Em uma biblioteca 📚, os livros podem estar misturados. Para 
        organizá-los, você pede para ordená-los por título.



    🔹 **Exemplo prático**

        ```sql
        SELECT * FROM Produtos ORDER BY Preco DESC;
        ```
        Retorna todos os produtos ordenados pelo preço, do maior para o menor.