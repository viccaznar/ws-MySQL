Cartão 4: Análise da Query – 

SELECT * FROM students WHERE studentid = 6;

- *SELECT : Indica que todas as colunas do registro devem ser retornadas.
- FROM students: Especifica que os dados serão extraídos da tabela students.

- WHERE studentid = 6: Aplica um filtro para recuperar somente os registros cujo studentid seja igual a 6.
Essa consulta retorna exatamente um registro (ou nenhum, se não existir), representando o aluno com o ID 6.

Exemplo Prático:
Em um sistema de cadastro escolar, se um professor deseja visualizar todas as informações do aluno de código 6 para uma reunião, essa consulta é empregada para puxar todo o histórico e dados cadastrais desse aluno.

Exemplo Lúdico:
Imagine que você tem uma lista de presença numerada e precisa encontrar o aluno com o número exato 6. Esse comando é como procurar no quadro de chamadas o aluno com a marcação “6”, ignorando os demais.

Cartão 5: Análise da Query – 

SELECT * FROM students WHERE firstname = 'John';


- *SELECT : Retorna todas as colunas disponíveis.
- FROM students: Consulta realizada na tabela students.
- WHERE firstname = 'John': Filtra os registros para incluir apenas aqueles cujo firstname seja exatamente 'John'.
A consulta traz todos os registros dos alunos chamados "John".

Exemplo Prático:
Em uma escola, se vários alunos se chamam John, essa consulta exibirá uma lista contendo todos os registros desses alunos. Essa informação pode ser utilizada para análises ou para enviar comunicados direcionados.

Exemplo Lúdico:
Imagine que você tem uma caixa cheia de cartões com nomes e precisa selecionar apenas os cartões com o nome "John". Assim, você utiliza um filtro para remover todos os outros nomes, ficando apenas com os cartões desejados

Cartão 6: Análise da Query – SELECT * FROM employees WHERE jobtitle = 'Application Developer';

- *SELECT : Indica que todas as colunas dos registros serão selecionadas.
- FROM employees: Define que a consulta será feita na tabela employees.
- WHERE jobtitle = 'Application Developer': Filtra os registros para incluir somente aqueles cujo cargo (jobtitle) seja ‘Application Developer’.
Essa consulta retorna todos os dados dos funcionários que possuem o cargo de Application Developer.

Exemplo Prático:
Em uma empresa, se o gerente de TI precisa ver todos os desenvolvedores de aplicativos, ele utiliza essa consulta para acessar detalhes dos funcionários que exercem essa função, podendo iniciar avaliações de desempenho ou discutir novos projetos.

Exemplo Lúdico:
Imagine que você está organizando um workshop e deseja convidar somente os “desenvolvedores de aplicativo” de uma lista de funcionários. Esse comando é como selecionar apenas os nomes dos colaboradores que possuem exatamente essa função, filtrando os demais que não se encaixam no perfil
