Cartão Explicativo 3: O MySQL é Case Sensitive?

A sensibilidade a maiúsculas e minúsculas (case sensitivity) no MySQL depende do contexto e das configurações do servidor.
- Keywords (palavras-chave): Normalmente não são case sensitive; isto é, select, SELECT ou SeLeCt serão interpretados da mesma forma.
- Identificadores (nomes de tabelas, colunas, etc.): A sensibilidade pode variar. Em sistemas operacionais como Linux, os identificadores costumam ser case sensitive por padrão (por exemplo, Alunos e alunos podem ser tratados como tabelas distintas). Em ambientes Windows, geralmente não há sensibilidade, pois o sistema de arquivos é case insensitive.
- Constantes e dados armazenados: São comparados conforme a collation definida; strings podem ser case sensitive ou não, dependendo dessa configuração

Exemplo Prático:
Em um servidor MySQL rodando no Linux, se você criou uma tabela chamada Clientes e depois tentar acessar clientes, poderá ocorrer um erro, pois os nomes diferem em maiúsculas e minúsculas. Já os comandos SQL, como SELECT e FROM, funcionam independente da capitalização, desde que estejam escritos corretamente em sua sintaxe.

Exemplo Lúdico:
Imagine que você tem etiquetas para caixas em uma biblioteca. Em um ambiente “case sensitive”, a etiqueta “Livros” é diferente de “livros” – cada uma leva a um conjunto específico de prateleiras. Em contrapartida, as instruções da biblioteca (como “emprestar” ou “devolver”) são compreendidas mesmo que escritos com letras maiúsculas ou minúsculas, pois essas regras sempre têm o mesmo sentido.

