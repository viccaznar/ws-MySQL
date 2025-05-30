Cartão Extra: Análise das Consultas SQL Exemplificadas
Consulta 1:

SELECT name FROM students WHERE id = 5;

Esta consulta faz o seguinte:
- SELECT name: Retorna apenas a coluna name dos registros.
- FROM students: Indica que os dados virão da tabela students.
- WHERE id = 5: Filtra os registros para retornar somente aquele cujo id é igual a 5.
- 
Exemplo Prático:
Em um sistema escolar, se cada aluno tem um id único, essa consulta permite buscar o nome do aluno cujo id é 5.

Exemplo Lúdico:
Imagine que você tenha um livro de registros dos alunos e precise encontrar rapidamente o nome do aluno que aparece na página 5. Essa consulta é como pedir ao bibliotecário para buscar justamente o nome que está registrado com o número 5.

SELECT * FROM students WHERE age < 6;

Esta consulta realiza as seguintes operações:
- *SELECT : Retorna todas as colunas para cada registro.
- FROM students: Extração dos dados da tabela students.
- WHERE age < 6: Aplica um filtro para selecionar apenas os registros em que o valor da coluna age seja menor que 6.
  
Exemplo Prático:
Em um contexto escolar, essa consulta pode ser utilizada para identificar todos os alunos que têm menos de 6 anos, talvez para dados relativos a educação infantil ou para preparar um ambiente apropriado.

Exemplo Lúdico:
Imagine que você precise organizar uma atividade para crianças pequenas. Ao consultar o “livro de registros” da escola, você deseja listar todos os alunos com idade inferior a 6 anos. Essa consulta, assim como uma triagem, garante que apenas as informações dos “pequenos” sejam apresentadas.
