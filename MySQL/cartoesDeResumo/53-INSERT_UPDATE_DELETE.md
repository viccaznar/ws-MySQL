Cartão 5: INSERT, UPDATE e DELETE

Estes são os principais comandos dentro do DML:
- INSERT: Insere um novo registro (linha) em uma tabela.
- UPDATE: Modifica dados existentes em um registro já inserido.
- DELETE: Remove um registro de uma tabela.

Exemplo Prático:
Para a tabela students:
- INSERT INTO students VALUES (1, 'João', 'Matemática', 16); insere um novo aluno.
- UPDATE students SET name = 'João Silva' WHERE id = 1; altera o nome do aluno com o id 1.
- DELETE FROM students WHERE id = 1; remove o aluno com o id 1 do banco de dados.

Exemplo Lúdico:
Considere um mural de avisos:
- INSERT é como colar um novo aviso no mural,
- UPDATE é quando você retira um aviso antigo e cola uma versão atualizada,
- DELETE é simplesmente tirar o aviso que já não é mais necessário.
