Cartão Explicativo: Como Mostrar as Tabelas Dentro de um Servidor Usando SHOW

No MySQL, para listar as tabelas disponíveis em um banco de dados específico, utiliza-se o comando:

SHOW TABLES;

Passos e Funcionamento:
- Conexão ao Servidor:
Primeiramente, você deve estar conectado a um servidor MySQL. Essa conexão é feita normalmente por parâmetros como usuário, senha e endereço do servidor (usando, por exemplo, mysql -u seu_usuario -p -h seu_servidor).

- Selecionar o Banco de Dados:
O comando SHOW TABLES; lista as tabelas do banco de dados atualmente ativo, ou seja, aquele que foi selecionado com o comando USE nome_do_banco;.

- Exemplo: Se você executar USE school;, o comando SHOW TABLES; mostrará todas as tabelas criadas no banco de dados school.

- Listagem de Tabelas:
Após selecionar o banco de dados desejado, ao emitir SHOW TABLES;, o MySQL retorna uma lista simples com os nomes de todas as tabelas existentes nesse banco. Essa listagem é útil para confirmar se as tabelas foram criadas conforme o esperado ou para inspecionar a estrutura do seu ambiente de dados.

Exemplo Prático na Realidade
Imagine uma escola que usa um servidor MySQL para gerenciar seus dados. Esse servidor tem vários bancos de dados, entre eles o banco de dados school, que contém tabelas como students, teachers e courses.
- Passo 1: Conectar ao servidor:

mysql -u admin -p -h localhost

- Passo 2: Selecionar o banco de dados da escola:

USE school;

- Passo 3: Mostrar as tabelas disponíveis:

SHOW TABLES;

Como resultado, o MySQL exibirá algo como:

+--------------------+
| Tables_in_school   |
+--------------------+
| students           |
| teachers           |
| courses            |
+--------------------+

Dessa forma, o administrador pode rapidamente verificar quais tabelas estão presentes no banco de dados school.

Exemplo Lúdico (Analogia)
Imagine que um banco de dados seja como uma biblioteca e as tabelas sejam as prateleiras organizadas por assunto. Para saber quais prateleiras (tabelas) estão disponíveis em uma determinada seção da biblioteca (banco de dados):
- Conecte à Biblioteca (Servidor): Você chega à biblioteca.
- Escolha a Seção: Você entra na seção específica da biblioteca (por exemplo, a seção de "História", que seria o banco de dados school).
- Visualize as Prateleiras: Ao olhar ao redor, você vê a lista de prateleiras (como students, teachers e courses) onde os livros estão organizados.

Usar o comando SHOW TABLES; é como pedir ao bibliotecário para listar todas as prateleiras daquela seção, facilitando encontrar onde cada tipo de informação está armazenado.
