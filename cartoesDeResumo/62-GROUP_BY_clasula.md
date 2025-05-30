Cartão 5: O que define a cláusula GROUP BY?

A cláusula GROUP BY agrupa os registros que compartilham um mesmo valor em uma ou mais colunas. Ela é útil ao usar funções agregadas como COUNT, SUM, AVG, etc., pois permite resumir os dados agrupando-os por critérios específicos.

Exemplo Prático:
Caso um gerente de RH deseje saber quantos funcionários existem por departamento, ele pode usar:

SELECT department, COUNT(*) FROM employees GROUP BY department;

Aqui, os registros são agrupados com base na coluna department e contados.

Exemplo Lúdico:
Imagine que você possui uma coleção de selos e decide organizar por país. A ação de colocar todos os selos do mesmo país juntos é como o agrupamento feito pelo GROUP BY — todos os itens com a mesma característica ficam juntos para melhor análise ou contagem.
