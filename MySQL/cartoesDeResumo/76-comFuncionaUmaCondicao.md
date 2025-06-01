Cartão Explicativo 2: Como funciona uma condição no MySQL?

Quando uma condição é aplicada em uma consulta:
- Avaliação Registro a Registro: O mecanismo do MySQL verifica cada linha da tabela.
- Avaliação Booleana: Para cada registro, a expressão é calculada. Se o resultado for TRUE, o registro satisfaz a condição e é incluído no resultado. Se for FALSE, o registro é descartado.
- Filtragem Dinâmica: A cláusula WHERE utiliza essa condição para “filtrar” os dados, retornando somente os registros que cumprem o critério definido.
- 
Exemplo Prático:
Considere a consulta:

SELECT * FROM students WHERE studentid = 6;

Para cada registro na tabela students, o MySQL verifica se o campo studentid é igual a 6. Somente os registros que retornarem TRUE para essa comparação serão exibidos.

Exemplo Lúdico:
Imagine um segurança na porta de uma festa:
- O segurança (condição) verifica cada convidado (registro).
- Se o convidado tem o crachá com o número “6” (condição verdadeira), ele pode entrar.
- Se não tiver, é impedido.
Dessa forma, somente os “convidados” que cumprem a regra são admitidos na festa.
