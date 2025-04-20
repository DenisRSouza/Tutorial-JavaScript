<em>STRINGS</em>

Strings são usadas para representar texto, e são escritas delimitando seu conteúdo entre aspas:

```js
"Calma Calabreso"
``` 

Alguns caracteres são mais difíceis de serem colocados entre aspas, como por exemplo, colocar aspas dentro de aspas. Além disso, as quebras de linha usados quando você aperta Enter também não podem ser colocados entre aspas.

 Para incluir esses caracteres em uma String devemos utilizar a barra invertida <code> / </code>, quando a barra invertida for encontrado dentro de um texto entre aspas ela indicará que o caractere seguinte possui um significado especial. Quando um caractere <code>n</code> aparecer após uma barra invertida ele será interpretado como uma quebra de linha:
 ```js
 "Essa é a primeira lina/nE essa é a segunda" 
 ```
 Strings não podem ser divididas, multiplicadas nem subtraídas, entretanto, o operador <code>+</code> pode ser usado nelas. Ele não efetua a adição, mas concatena, ou seja, junta duas Strings em uma única String. O próximo exemplo produzirá a String <code>"calabreso"</code> :

 ```js 
 "cal" + "abr" + "eso" 
 ``` 
 
 <em>OPERADORES UNÁRIOS</em>

 O operador <code>typeof</code> retorna o tipo de variável ou expresão, como por exemplo:
 
```js
typeof "John" // retorna uma string
typeof 3.14 // retorna um número
console.log(typeof 4.5) //número 
```

Vamos usar o <code>console.log</code> nos códigos de exemplo para indicar que desejamos ver o resultado da avaliação de algo. Quando você executar tais códigos, o valor produzido será mostrado na tela.

Todos os operadores que vimos operavam em dois valores, mas <code>typeof</code> espera um único valor. Operadores que usam dois valores são chamados binários. O operador <code>-</code> pode ser usado tanto como binário quando como unário:

```js 
console.log(-(10-2)) // -8 
``` 

<em>VALORES BOOLEANOS</em>

O JavaScript possui o tipo Booleano, que tem apenas dois valores: verdadeiro e falso (que são escritos como ) <code>true</code> e <code>false</code>. Por exemplo

```js
console.log(3 > 2) // true 

console.log(3 < 2) // false 
``` 

Strings podem ser comparadas da mesma forma:
```js
console.log("Aardvark" < "Zoroaster")
```
A forma como as Strings são ordenadas é mais ou menos alfabética. <code>"Z" < "a"</code>, as letras maiúsculas terão sempre um valor menor que as minúsculas.

<code>NaN</code> é usador para indicar o resultado de alguma operação que não tenha sentido.

<em>OPERADORES LÓGICOS</em>

O JavaScript dá suporte a três operadores lógicos: and, or e not. O operador <code>&&</code> representa o valor and e seu resultado é apenas verdadeiro se ambos os valores dados à ele forem verdadeiros:

```js
console.log(true && false) // false
console.log(true && true) // true
```

O operador <code>||</code> indica o valor or. Ele produz um valor verdadeiro se qualquer um dos valores dados à ele for verdadeiro: 

```js
console.log(false || true) // true
console.log(false || false) // false
```

Not é escrito usando <code>!</code>. Ele é um operador unário que inverte o valor dado a ele. Por exemplo, <code>!true</code> produz <code>false</code>

O último operador lógico não é unário nem binário, mas ternário. Ele é escrito usando um ponto de interrogação e dois pontos, como mostrado abaixo:

```js
console.log(true ? 1 : 2); // 1
console.log(false? 1 : 2); // 2
```

Esse é um operador condicional. O valor presente à esquerda do ponto de interrogação "seleciona " qual dos dois valores será retornado.

<em>VALORES INDEFINIDOS</em>

Existem dois valores especiais, <code>null</code> e <code>undefined</code>, que são usados para indicar a ausência de um vlaor com significado. Eles são valores por si só mas não carregam nenhum tipo de informação. Tanto faz qual dos dois você vai usar.
