Cartão Explicativo 2: INSERT INTO tablename VALUES (value1, value2, value3, ...);

INSERT INTO tablename VALUES (value1, value2, value3, ...);

insere uma nova linha na tabela especificada (tablename) usando todos os valores na ordem em que as colunas foram definidas durante a criação da tabela. Esse método é adequado quando você deseja inserir dados para todas as colunas e conhece exatamente a ordem definida.

Exemplo Prático:
Suponha que a tabela students tenha a seguinte definição:
- id (INT)
- name (VARCHAR)
- class (VARCHAR)
- age (INT)
  
Para inserir um novo aluno com todas as colunas preenchidas, poderíamos usar:

INSERT INTO students VALUES (2, 'Bruno', 'História', 22);

Esse comando insere uma nova linha na tabela com o id 2, nome "Bruno", na turma "História" e com idade 22.

Exemplo Lúdico:
Imagine que você está escrevendo um novo cartão em um fichário onde o formato dos cartões já está pré-determinado e na mesma ordem. Se cada cartão espera que você escreva primeiro o número de identificação, depois o nome, a turma e, por fim, a idade, você simplesmente preenche o cartão na ordem exata.

INSERT INTO tablename (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);

é utilizado para inserir uma nova linha especificando exatamente quais colunas serão preenchidas. Essa forma é útil quando você não deseja ou não precisa inserir dados para todas as colunas (por exemplo, quando algumas colunas possuem valores padrão ou permitem nulos) ou quando a ordem das colunas na tabela não é conhecida pelo usuário.

Exemplo Prático:
Suponha que na tabela students você queira inserir um novo aluno, mas a coluna age pode ser opcional e, portanto, você não a deseja preencher neste momento. Você pode executar:

INSERT INTO students (id, name, class) VALUES (3, 'Carla', 'Biologia');

Esse comando insere os valores somente nas colunas id, name e class, deixando age com seu valor padrão ou nulo.
Exemplo Lúdico:
Imagine preencher um formulário onde você marca apenas os campos obrigatórios, como "Nome" e "Turma", e deixa outros campos em branco porque eles não são obrigatórios ou serão preenchidos depois. Você está definindo explicitamente quais informações está fornecendo, sem depender de uma ordem pré-definida