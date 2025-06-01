Cartão Explicativo: Selecionando um Banco de Dados com o Comando USE

- Propósito do Comando USE:
O comando USE é empregado para definir o banco de dados ativo na sua sessão corrente no servidor MySQL. Isso significa que, uma vez conectado ao servidor, você pode ter vários databases (bancos de dados) disponíveis, e o comando USE diz ao MySQL qual deles deve ser o alvo das consultas e operações seguintes.

- Importante Diferenciação:
É fundamental entender que o comando USE não é utilizado para selecionar ou alternar entre diferentes servidores. A escolha do servidor é feita durante o processo de conexão (por exemplo, por meio do parâmetro -h na linha de comando ou pela configuração da ferramenta de gerenciamento).

O comando USE apenas muda o contexto dentro do mesmo servidor, direcionando as operações para um banco de dados específico.

- Como Funciona:
Ao emitir um comando como USE onlineshop;, você está instruindo o servidor MySQL a tornar o banco de dados chamado "onlineshop" o database padrão para todos os comandos SQL subsequentes. Assim, você não precisa digitar o nome do banco de dados em cada consulta.

Exemplo Prático na Realidade
Imagine o seguinte cenário:
Uma empresa possui um servidor MySQL que abriga vários bancos de dados — por exemplo, school, company e onlineshop.
- Se um administrador deseja trabalhar com os dados de comércio eletrônico, ele precisa definir o banco de dados ativo para onlineshop.
- Ao conectar-se ao servidor (usando, por exemplo, mysql -u admin -p -h server.example.com), o administrador executa o comando:

USE onlineshop;

- A partir de então, todas as consultas, como uma inserção de novos produtos ou a consulta de pedidos, serão realizadas no contexto do banco onlineshop sem a necessidade de especificá-lo em cada comando.

Exemplo Lúdico
Imagine uma grande biblioteca (o servidor MySQL) com várias salas temáticas (os bancos de dados).
- Você, como usuário dessa biblioteca, precisa escolher em qual sala deseja trabalhar ou consultar os livros.
- O comando USE é equivalente a dizer: “Eu vou para a sala de História” ou “Eu vou para a sala de Ficção Científica.”
- Assim, se você digitar USE onlineshop;, é como se você estivesse indicando: “Hoje, vou trabalhar na sala dedicada à minha loja virtual” — e todas as informações (ou livros) que você procura estarão organizadas ali.
- Se precisar mudar para outra sala (ou banco), basta emitir novamente um comando USE com o novo nome, mantendo-se sempre dentro da mesma biblioteca (servidor).
