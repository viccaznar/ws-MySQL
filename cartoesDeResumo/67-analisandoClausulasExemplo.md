Cartão 2: Análise de SELECT DISTINCT firstname FROM students;

- Comando: SELECT DISTINCT firstname FROM students;
- O que ele faz:
- SELECT DISTINCT firstname: Indica que serão exibidos apenas valores únicos contidos na coluna firstname.
- FROM students: Define que a fonte dos dados é a tabela students.
Se houver alunos com o mesmo primeiro nome, aparecerá apenas uma ocorrência daquele nome na listagem.

Exemplo Prático:
Em uma escola, se houver 100 registros de alunos e 30 deles tiverem o mesmo primeiro nome "Ana", a consulta retornará "Ana" apenas uma vez. Essa lista única pode ser útil para análises de popularidade de nomes.

Exemplo Lúdico:
Imagine que você está organizando uma lista de presença onde quer saber quais nomes distintos aparecem, sem repetir “Ana”, “Carlos” ou “Beatriz” várias vezes. O comando SELECT DISTINCT funciona como um filtro que só permite a entrada de um exemplar decada nome.

Cartão 3: Análise de SELECT DISTINCT class FROM students;

- Comando: SELECT DISTINCT class FROM students;
- O que ele faz:
- SELECT DISTINCT class: Mostra apenas os valores distintos presentes na coluna class.
- FROM students: A tabela de onde os dados serão extraídos é students.
Essa consulta retorna a lista única de turmas ou classes existentes.

Exemplo Prático:
Se em uma escola a tabela students contém registros de alunos distribuídos em turmas como "1A", "1B", "2A", e muitos registros se repetem, essa consulta exibirá cada turma somente uma vez. Assim, o coordenador pode saber rapidamente todas as classes existentes sem repetições.

Exemplo Lúdico:
Imagine uma caixa de lápis de cor onde há muitas unidades de cada cor. Se você quiser saber quais cores estão disponíveis, sem contar cada lápis, o comando SELECT DISTINCT seria como separar apenas uma unidade de cada cor – resultando em uma lista única de cores diferentes.

Cartão 4: Análise de SELECT DISTINCT class, age FROM students;

- Comando: SELECT DISTINCT class, age FROM students;
- O que ele faz:
- SELECT DISTINCT class, age: Retorna combinações únicas das colunas class e age.
- FROM students: Indica que os dados serão obtidos da tabela students.
Aqui, o DISTINCT não opera de forma individual para cada coluna, mas considera a combinação dos valores. Duas linhas que possuam a mesma combinação de turma e idade serão retornadas apenas uma vez.

Exemplo Prático:
Em uma tabela onde vários alunos da turma "1A" têm a mesma idade (digamos 15), essa consulta retornará a combinação ("1A", 15) uma única vez. Se outra turma ou idade diferente aparecer, essa combinação será apresentada também.

Exemplo Lúdico:
Imagine que você está catalogando brinquedos por tipo e cor. Se você tem vários brinquedos do mesmo tipo e cor, o comando SELECT DISTINCT mostrará cada combinação única uma vez – como “Carro Vermelho”, “Boneca Azul” etc., sem listar o mesmo item repetidamente.

Cartão 5: Análise de SELECT DISTINCT jobtitle FROM employees;

- Comando: SELECT DISTINCT jobtitle FROM employees;
- O que ele faz:
- SELECT DISTINCT jobtitle: Recupera somente os valores distintos contidos na coluna jobtitle.
- FROM employees: Os dados são extraídos da tabela employees.
Isso retorna uma lista única de cargos existentes na empresa, eliminando repetições quando vários funcionários têm o mesmo cargo.

Exemplo Prático:
Em uma empresa grande, se houver dezenas de funcionários com o cargo "Analista", a consulta exibirá "Analista" uma única vez. Essa lista pode ajudar os gestores a saber quais tipos de cargos existem na organização sem se preocupar com quantas vezes cada cargo se repete.

Exemplo Lúdico:
Pense em um festival de talentos onde muitos participantes podem ter a mesma habilidade, como cantar ou dançar. Se você quiser listar os talentos únicos apresentados, o comando SELECT DISTINCT funcionaria como um filtro que só permite listar “Cantor” ou “Dançarino” uma vez, independentemente de quantos se apresentem com aquele talento.
