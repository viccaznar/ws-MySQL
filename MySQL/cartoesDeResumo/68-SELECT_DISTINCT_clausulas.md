Cartão 1: O que define a cláusula SELECT DISTINCT?

A cláusula SELECT DISTINCT é utilizada para retornar apenas valores únicos (não duplicados) a partir das colunas selecionadas em uma consulta SQL. Enquanto o comando SELECT normal pode retornar várias linhas com o mesmo valor em determinadas colunas, o DISTINCT filtra os resultados, garantindo que cada valor pessoalmente exibido seja único.
- Propósito: Eliminar duplicidades no conjunto de resultados.
- Funcionalidade: Quando você se depara com dados repetidos em uma coluna (ou conjunto de colunas), o DISTINCT os reduz a um único registro para cada valor distinto.

Exemplo Prático:
Imagine que em uma tabela de alunos, vários registros possam ter o mesmo primeiro nome. Se o objetivo for criar uma lista de nomes únicos para, por exemplo, enviar uma comunicação personalizada, utiliza-se:

SELECT DISTINCT firstname FROM students;

Esse comando retorna uma lista de todos os primeiros nomes cadastrados, mas sem repetições.

Exemplo Lúdico:
Pense em uma cesta com maçãs variadas, onde algumas maçãs são idênticas em cor e tamanho. Se você quiser criar uma “coleção única” apenas com os tipos de maçãs sem repetições, você separa cada tipo uma única vez – exatamente como o SELECT DISTINCT escolhe cada valor apenas uma vez, ignorando os “clones” que se repetem.

