Cartão Explicativo 1: Do que é feita uma condição no MySQL?

Uma condição no MySQL é construída a partir de expressões lógicas que utilizam:
- Colunas e constantes: Valores extraídos dos registros ou fixos;
- Operadores de comparação: Como =, <, >, <=, >=, <>, que comparam valores;
- Operadores lógicos: Como AND, OR e NOT, que combinam múltiplas comparações.
Esses elementos formam uma expressão que, ao ser avaliada, retorna verdadeiro (TRUE) ou falso (FALSE) para cada registro.

Exemplo Prático:
Ao filtrar registros de uma tabela de alunos, uma condição pode ser

studentid = 6

Isso verifica, em cada registro, se o valor da coluna studentid é igual a 6.

Exemplo Lúdico:
Imagine que você está usando uma peneira para separar bolas de diferentes cores.
- Colunas/constantes: São as bolas com cores diversas.
- Operadores de comparação: São as regras “selecionar somente as bolas vermelhas”.
- Operadores lógicos: Permitem combinar regras, como “bolas vermelhas e grandes”.
A condição é como a peneira que só deixa passar as bolas que atendem à regra, retornando “sim” (aceita) ou “não” (rejeita) para cada bola.
