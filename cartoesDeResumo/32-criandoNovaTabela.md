Cartão 4: Criando uma Nova Tabela – Analisando a Query

Query de Exemplo:
CREATE TABLE students(
    id INT NOT NULL PRIMARY KEY,
    name VARCHAR(40) NOT NULL,
    class VARCHAR(20) NOT NULL,
    age INT
);

- CREATE TABLE students: Inicia a criação de uma nova tabela chamada students.
  
id INT NOT NULL PRIMARY KEY:
  
- id: Nome da coluna que identifica unicamente cada registro.  
- INT: Tipo de dado numérico (inteiro).  
- NOT NULL: Garante que essa coluna não aceite valores nulos (deve sempre haver um valor).  
- PRIMARY KEY: Define essa coluna como a chave primária, que é usada para identificar cada registro de forma única.
  
name VARCHAR(40) NOT NULL:
  
- name: Nome da coluna destinada a armazenar nomes.  
- VARCHAR(40): Define que os dados serão cadeias de caracteres com no máximo 40 caracteres.  
- NOT NULL: Impede a inserção de registros sem um nome.

class VARCHAR(20) NOT NULL;
  
- class: Especifica a coluna que armazena a turma ou classe.  
- VARCHAR(20): Permite armazenar até 20 caracteres.  
- NOT NULL: Garante que cada registro deve ter um valor nesta coluna.
  
age INT:

- age: Coluna para armazenar a idade.
- INT: Tipo de dado numérico.
- Pode aceitar valores nulos se não for declarado NOT NULL.
- 
Exemplo Prático:
Uma escola deseja criar uma tabela para armazenar os dados de seus alunos. Ela cria a tabela students exatamente assim para garantir que cada aluno tenha um identificador único (id), nome e classe obrigatórios, e opcionalmente a idade, que pode ser preenchida ou deixada em branco se a informação não estiver disponível.

Exemplo Lúdico:
Imagine que você está organizando uma lista de alunos para um passeio escolar. Você precisa de uma lista onde cada aluno tenha um número de identificação (id), seu nome, a turma que frequentam, e, se possível, sua idade. O comando CREATE TABLE é como montar uma ficha de cadastro para cada aluno, definindo exatamente quais informações serão registradas em cada ficha.




