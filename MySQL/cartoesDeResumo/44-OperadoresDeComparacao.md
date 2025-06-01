Cartão 7: O que são Operadores de Comparação no MySQL?

Operadores de comparação são usados para fazer comparações entre valores ou expressões, retornando um resultado booleano (verdadeiro ou falso). Os principais operadores de comparação no MySQL incluem:

- = : Igual a
- < : Menor que
- > : Maior que
- <= : Menor ou igual a
- >= : Maior ou igual a
- <> ou != : Diferente de
  
Exemplo Prático:

Na consulta

SELECT * FROM students WHERE age < 6;

o operador < seleciona os registros onde a coluna age tem um valor inferior a 6.

Exemplo Lúdico:
Imagine que você está comparando a altura de duas pessoas. Se disser “João é mais alto que Maria”, você utiliza uma comparação (maior que). Esses operadores de comparação funcionam da mesma forma no MySQL, avaliando se um valor é menor, maior ou igual a outro, como se você estivesse medindo e comparando alturas.
