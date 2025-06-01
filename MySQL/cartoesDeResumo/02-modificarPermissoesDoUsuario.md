Cartão 2: Modificar Permissões ao Usuário
Exemplo Geral – Concedendo Todas as Permissões

GRANT ALL ON *.* TO 'admin' WITH GRANT OPTION;

Funcionalidade e Ação:
- GRANT ALL: Concede todas as permissões possíveis ao usuário.
- ON .: O primeiro asterisco (*) representa todas as bases de dados (schemas) e o segundo—todas as tabelas dentro de cada base. Dessa forma, o usuário admin passa a ter esses privilégios de forma global.
- WITH GRANT OPTION: Permite que o usuário admin repasse essas permissões a outros usuários, ou seja, ele pode conceder ou revogar privilégios além de utilizá-los.