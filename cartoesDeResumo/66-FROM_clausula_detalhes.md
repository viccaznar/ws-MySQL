Cartão 1: O que define a cláusula FROM?

A cláusula FROM é parte fundamental de uma instrução SQL que indica de onde os dados devem ser extraídos. Ela define a(s) tabela(s) ou fonte(s) de dados que servirão de base para a consulta. Sem ela, o SQL não saberia qual conjunto de dados utilizar para responder à consulta definida pela cláusula SELECT.

Exemplo Prático:
Imagine uma aplicação escolar que armazena os dados dos alunos na tabela students. Ao executar:

SELECT name FROM students;

a cláusula FROM informa ao mecanismo de banco de dados que os dados a serem retornados devem vir da tabela students.

Exemplo Lúdico:
Pense na cláusula FROM como escolher a seção de uma biblioteca. Se você quiser ler livros sobre história, você deve ir à estante "História". Assim, a cláusula FROM determina a "estante" (ou tabela) de onde os livros (dados) serão retirados.

Cartão 2: O que a cláusula FROM produz?

A cláusula FROM produz uma estrutura tabular de dados – basicamente, um conjunto de linhas e colunas que formam a base sobre a qual outras operações (como filtros e agrupamentos) serão aplicadas. Ela gera uma "tabela resultante" inicial, que pode ser a tabela completa ou uma relação derivada de junções (joins) e subconsultas.

Exemplo Prático:
Se você executar:

SELECT * FROM students;

a cláusula FROM gera uma tabela contendo todas as linhas e colunas da tabela students. Essa tabela inicial é a base para qualquer refinamento feito com cláusulas adicionais, como WHERE ou GROUP BY.

Exemplo Lúdico:
Imagine que você abre uma grande caixa de brinquedos (a tabela). A cláusula FROM é o ato de abrir a caixa e visualizar todos os brinquedos contidos nela. Essa visão completa (“tabela resultante”) pode depois ser filtrada, organizada ou agrupada conforme a necessidade.

Cartão 7: Por que a cláusula FROM pode gerar resultados errados?

A cláusula FROM pode gerar resultados errados por diversas razões:
- Falta de condições de junção (JOIN): Se você unir tabelas sem especificar corretamente as condições de correspondência, pode causar produtos cartesianos inesperados.
- Ambiguidade em nomes de colunas: Se duas tabelas contiverem colunas com o mesmo nome e não forem explicitadas, pode haver confusão ou erro.
- Dados inconsistentes: Se a fonte de dados (tabela ou view) contiver erros ou dados duplicados, esses problemas se refletirão no resultado produzido pela cláusula FROM.
- 
Exemplo Prático:
Executar um comando:

SELECT * FROM table1, table2;

sem especificar uma condição de junção (via WHERE ou JOIN ON) pode resultar em um produto cartesiano, ou seja, todas as combinações possíveis de linhas das duas tabelas, o que muitas vezes não é o desejado.

Exemplo Lúdico:
Imagine misturar duas caixas de peças de LEGO sem separá-las por cor ou tamanho. Você acabará com uma mistura confusa e provavelmente com combinações que não fazem sentido no modelo final, assim como uma consulta sem condições de join pode gerar um conjunto de dados incorreto.

Cartão 8: Por que a cláusula FROM é a primeira a ser notada pelo banco de dados durante o parse de uma declaração SQL?

Durante o processo de análise (parse) de uma declaração SQL, o mecanismo de banco de dados precisa identificar primeiro de onde os dados serão extraídos. A cláusula FROM define as fontes de dados (tabelas ou subconsultas) e estabelece o contexto para o restante da consulta, como o nome das colunas disponíveis e as relações entre os dados. Por isso, ela é a primeira a ser avaliada, permitindo que o parser construa uma referência completa do “ambiente” de dados.

Exemplo Prático:
Ao executar:

SELECT * FROM students WHERE age > 18;

o mecanismo de banco de dados primeiro verifica a clause FROM students para entender a estrutura da tabela students antes de aplicar o filtro definido pela cláusula WHERE.

Exemplo Lúdico:
Imagine que você está organizando uma festa e, antes de definir as regras de entrada (filtros), precisa saber quantos convidados (dados) estão na lista. Primeiramente, você consulta a lista completa (FROM) para ter o “mapa” dos convidados, e depois aplica outras regras. Assim, o FROM é o ponto de partida para toda a organização.

Cartão 9: Como o FROM se comporta com resultados de uma única tabela, joins, views e subqueries?

- Única Tabela:
Quando a consulta utiliza uma única tabela (por exemplo, FROM students), o FROM simplesmente retorna os dados contidos nessa tabela, estabelecendo um conjunto de dados base (result set).

- Joins:
Ao usar joins (por exemplo, FROM employees JOIN departments ON employees.deptid = departments.deptid), o FROM combina linhas de duas ou mais tabelas de acordo com a condição de junção, produzindo um conjunto composto que integra colunas de ambas as tabelas.

- Views:
Views são consultas armazenadas que se comportam como tabelas. Quando o FROM aponta para uma view, ele utiliza a definição interna da view para gerar o resultado, como se fosse uma tabela tradicional.

- Subqueries:
Em subqueries (consultas aninhadas), o FROM pode referenciar uma subconsulta que produz um conjunto intermediário de dados, o qual é então tratado como uma “tabela derivada” para a consulta externa.

Exemplo Prático

- Única Tabela:     
  
    SELECT name FROM students;

- Join:  

    SELECT employees.name, departments.department_name
    FROM employees JOIN departments ON employees.deptid = departments.deptid;

- View:

    SELECT * FROM view_sales;

- Subquery:

    SELECT avg_salary FROM (
        SELECT AVG(salary) AS avg_salary FROM employees
    ) AS salary_stats;

Exemplo Lúdico:
- Única Tabela: Imagine olhar em uma única estante para ver todos os livros disponíveis.
- Joins: Imagine combinar peças de dois quebra-cabeças diferentes que se encaixam para formar uma imagem completa.
- Views: Pense em uma vitrine que exibe uma coleção pré-selecionada de itens — a view já vem com a seleção feita.
- Subqueries: Imagine um assistente que primeiro prepara uma lista intermediária (subquery) com os itens mais vendidos, e depois você usa essa lista para tomar uma decisão final
