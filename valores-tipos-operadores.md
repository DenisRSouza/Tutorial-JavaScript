<em>STRINGS</em>

Strings são usadas para representar texto, e são escritas delimitando seu conteúdo entre aspas:

<code>"Calma Calabreso"</code>

Alguns caracteres são mais difíceis de serem colocados entre aspas, como por exemplo, colocar aspas dentro de aspas. Além disso, as quebras de linha usados quando você aperta Enter também não podem ser colocados entre aspas.

 Para incluir esses caracteres em uma String devemos utilizar a barra invertida <code> / </code>, quando a barra invertida for encontrado dentro de um texto entre aspas ela indicará que o caractere seguinte possui um significado especial. Quando um caractere <code>n</code> aparecer após uma barra invertida ele será interpretado como uma quebra de linha:
 <code>"Essa é a primeira lina/nE essa é a segunda" </code>

 Strings não podem ser divididas, multiplicadas nem subtraídas, entretanto, o operador <code>+</code> pode ser usado nelas. Ele não efetua a adição, mas concatena, ou seja, junta duas Strings em uma única String. O próximo exemplo produzirá a String <code>"calabreso"</code> :

 <code>"cal" + "abr" + "eso"</code>

 <em>OPERADORES UNÁRIOS</em>

 O operador <code>typeof</code> retorna o tipo de variável ou expresão, como por exemplo:

<code>typeof "John" // retorna uma string</code>
<code>typeof 3.14 // retorna um número</code>
<code>console.log(typeof 4.5) //número </code>

Vamos usar o <code>console.log</code> nos códigos de exemplo para indicar que desejamos ver o resultado da avaliação de algo. Quando você executar tais códigos, o valor produzido será mostrado na tela.

Todos os operadores que vimos operavam em dois valores, mas <code>typeof</code> espera um único valor. Operadores que usam dois valores são chamados binários. O operador <code>-</code> pode ser usado tanto como binário quando como unário:
<code> console.log(-(10-2)) // -8 </code>

<em>VALORES BOOLEANOS</em>
O JavaScript possui o tipo Booleano, que tem apenas dois valores: verdadeiro e falso (que são escritos como ) <code>true</code> e <code>false</code>. Por exemplo

<code>console.log(3 > 2) // true </code>

<code>"console.log(3 < 2) // false </code>
