Cartão 6: Significado dos Trechos *.* e GRANT OPTION
- *.*:
 
- O primeiro asterisco indica todas as bases de dados existentes no servidor.

- O segundo asterisco representa todas as tabelas dentro de cada base de dados.

Dessa forma, ao utilizar *.*, as permissões concedidas se aplicam globalmente, sem restrição a um único banco ou tabela.


- GRANT OPTION:

Este trecho permite que o usuário, além de usar os privilégios que foram concedidos, também possa repassar esses privilégios a outros usuários. Isso significa que o usuário pode executar comandos para conceder ou revogar acesso, aumentando significativamente seu controle sobre o ambiente MySQL