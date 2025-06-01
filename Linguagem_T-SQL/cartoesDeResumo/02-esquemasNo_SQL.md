# Conceitos: Trabalhar com Esquemas em SQL Server 🗂️

## 1. Esquemas e Namespaces Lógicos
    🔹 - **Conceito:**  
        Esquemas são agrupamentos lógicos de objetos de banco de dados (como tabelas) que ajudam a organizar e isolar os dados. Permitem separar, por exemplo, objetos de vendas em um esquema (Sales) e objetos de produção em outro (Production), evitando conflitos quando tabelas possuem o mesmo nome.
    
    🔹 - **Exemplo Lúdico:**  
        Imagine um grande armário de brinquedos 🎲, onde cada gaveta (esquema) guarda um tipo diferente de brinquedo. Assim, mesmo que duas gavetas contenham um "carrinho", eles ficam organizados e identificados de forma diferente.
    
    🔹 - **Exemplo Prático:**  
        No SQL Server, uma tabela pode ser definida assim:  

        ```sql
        CREATE TABLE Sales.Customer (
            CustomerID INT PRIMARY KEY,
            Nome VARCHAR(100)
        );
        ```

        Outra tabela pode ser criada em outro esquema:

        ```sql
        CREATE TABLE Production.Product (
            ProductID INT PRIMARY KEY,
            escricao VARCHAR(100)
        );
        ```

## 2. Nomenclatura Hierárquica e Nome Qualificado
    🔹- **Conceito**:
        SQL Server utiliza uma nomenclatura hierárquica para identificar objetos de forma única. Um nome totalmente qualificado inclui o nome do servidor, banco de dados, esquema e o nome do objeto (por exemplo, uma tabela). Isso torna possível distinguir, por exemplo, uma tabela Order no esquema Sales de uma outra tabela Order no esquema Production.

    🔹- **Exemplo Lúdico**:
        Pense no endereço de uma casa 🏠: para encontrá-la com precisão, usamos país, estado, cidade, rua e número. Assim, cada parte da hierarquia ajuda a identificar exatamente a localização, assim como o nome qualificado identifica de forma única uma tabela.

    🔹 - **Exemplo Prático**:
        Um exemplo de nome totalmente qualificado pode ser

        ```sql
        SELECT * FROM Server1.StoreDB.Sales.Order;
        ```

        - Quando se trabalha dentro do mesmo banco de dados, pode-se referenciar a tabela assim:

        ```sql
        SELECT * FROM Sales.Order;
        ```

## 3. Nomenclatura Hierárquica
    - Os bancos de dados SQL Server utilizam uma estrutura hierárquica para nomear objetos.
    - Um nome totalmente qualificado inclui servidor, banco de dados, esquema e tabela.
    
    🔹 Exemplo lúdico: Como um endereço de uma casa 🏠, que inclui o país, estado, cidade, 
        rua e número.

    🔹 Exemplo prático: Para acessar uma tabela específica, pode-se referenciá-la com seu 
        nome completo:

        ```sql
        SELECT * FROM Server1.StoreDB.Sales.Order;
        ```