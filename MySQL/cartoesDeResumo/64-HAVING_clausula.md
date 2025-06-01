Cartão 7: O que define a cláusula HAVING?

A cláusula HAVING é similar à WHERE, mas é aplicada sobre os resultados agrupados por uma cláusula GROUP BY. Ela filtra os grupos depois que as agregações (como contagem ou soma) foram executadas, permitindo especificar condições para cada grupo.

Exemplo Prático:
Se quisermos listar apenas os departamentos que possuem mais de 10 funcionários, utilizaríamos:

SELECT department, COUNT(*) as total FROM employees
GROUP BY department
HAVING COUNT(*) > 10;

Dessa forma, somente os departamentos com mais de 10 funcionários serão exibidos.

Exemplo Lúdico:
Imagine que você está organizando uma competição e dividiu os participantes em equipes. Depois de contar o número de membros de cada equipe, você decide que só as equipes com mais de 5 membros poderão competir. O HAVING é como esse critério aplicado após a formação dos grupos, filtrando os que cumprem a condição
