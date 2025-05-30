Exemplos de Queries para Cada Privilégio Específico

Em MySQL, há diversos privilégios individuais que podem ser concedidos. Abaixo, segue uma tabela com alguns dos principais privilégios e um exemplo de query para cada um:

Funcionalidade e Ação:
Com essa query, o usuário admin recebe todas as permissões possíveis no servidor MySQL de forma global:
- ALL: Concede todas as operações (como SELECT, INSERT, UPDATE etc.).
- ON .: O primeiro asterisco abrange todas as bases de dados (schemas) e o segundo abrange todas as tabelas de cada banco de dados, garantindo acesso irrestrito.
- WITH GRANT OPTION: Permite que o usuário repasse esses privilégios a outros usuários, ou seja, ele pode conceder ou revogar privilégios para outros usuários no sistema.
Exemplos de Queries para Privilégios Específicos (em forma de texto):
- SELECT:
Para conceder ao usuário admin a permissão de consultar dados de uma tabela específica, use:
GRANT SELECT ON nome_do_banco.nome_da_tabela TO 'admin';
Essa query permite a leitura de dados nessa tabela.
- INSERT:
Se desejar que o usuário possa inserir registros em uma tabela, utilize:
GRANT INSERT ON nome_do_banco.nome_da_tabela TO 'admin';
Essa query autoriza a inclusão de novos dados.
- UPDATE:
Para permitir que o usuário atualize dados existentes em uma tabela, execute:
GRANT UPDATE ON nome_do_banco.nome_da_tabela TO 'admin';
Com isso, o usuário pode modificar registros já presentes.
- DELETE:
Caso seja necessário que o usuário remova registros de uma tabela, use:
GRANT DELETE ON nome_do_banco.nome_da_tabela TO 'admin';
Essa query concede o permissão para deleção de registros.
- CREATE:
Para autorizar a criação de novas tabelas ou bancos de dados, o comando é:
GRANT CREATE ON nome_do_banco.* TO 'admin';
Assim, o usuário pode criar objetos dentro do escopo definido.
- DROP:
- Se a intenção for permitir a remoção de tabelas ou de bancos de dados, a query é:
GRANT DROP ON nome_do_banco.nome_da_tabela TO 'admin';
Essa query confere o poder de deletar objetos do banco.
- ALTER:
Quando for necessário que o usuário altere a estrutura de tabelas (por exemplo, adicionando ou removendo colunas), utilize:
GRANT ALTER ON nome_do_banco.nome_da_tabela TO 'admin';
- INDEX:
Para permitir a criação ou remoção de índices em tabelas, o exemplo de comando é:
GRANT INDEX ON nome_do_banco.nome_da_tabela TO 'admin';
- EXECUTE:
Caso o usuário precise executar procedimentos armazenados, o comando indicado é:
GRANT EXECUTE ON PROCEDURE nome_do_banco.nome_da_procedure TO 'admin';
- GRANT OPTION (individual):
Se desejar conceder somente a habilidade de repassar privilégios (em um escopo específico), o comando seria:
GRANT GRANT OPTION ON nome_do_banco.* TO 'admin';
Isso permite ao usuário conceder as permissões que ele mesmo possui a outros usuários.

Nota: A query GRANT ALL ON *.* TO 'admin' WITH GRANT OPTION; é um atalho que, em vez de conceder cada privilégio individualmente, aplica todos de forma abrangente. 