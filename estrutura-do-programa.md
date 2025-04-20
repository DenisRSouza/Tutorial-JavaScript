<em>EXPRESSÕES E AFIRMAÇÕES</em>

Um fragmento do código que produz um valor é chamado de expressão. Todo valor que é escrito literalmente (<code>como 73</code> ou <code>Davi Brito</code>) é um expressão. 

Fazendo uma analogia, se uma expressão corresponde ao fragmento de uma sentença, uma afirmação, no JavaScript, corresponde a uma frase completa em linguagem humana. Um programa é simplesmente uma lista de afirmações. 

O tipo mais simples de afirmação é uma expressão com um ponto e vírgula depoia dela:

```js
1;
!false;
```

No exemplo anterior, as afirmações produzem o valor <code>1</code> e <code>true</code> e então imediatamente os jogam fora novamente. Não deixam nenhuma expressão no mundo. Quando executamos um programa, nada acontece.

<em>VARIÁVEIS</em>

Para pegar e guardar valores, o JavaScript fornece uma coisa chamada variável:

```js
var caught = 5*5;
```

A declaração anterior criou uma variável chamada <code>caught</code> e a usou para armazenar o valor que foi produzido pela multiplicação 5 por 5.

Depois de uma variável ter sido definida, seu nome pode ser usado como uma expressão. O valor da expressão é o valor atual mantida pela variável. Por exemplo:

```js
var ten = 10;
console.log(ten * ten);
//100
```

Nomes de variáveis podem ser quase qualquer palavra, menos a palavra reservada para a palavra-chave. Não pode haver espaços incluídos. Dígitos nuéricos podem também ser parte dos nomes de variáveis (<code>catch22</code> é um nome válido, por exemplo), mas um nome não pode iniciar com um dígito numérico. O nome de uma variável também não pode incluir pontuação, exceto pelos caracteres <code>$</code> e <code>_</code>

O operador <code>=</code> oide ser usado a qualquer hora em variáveis existentes para desconectá-las de seu valor atual e então apontá-las para um novo:

```js
var mood = "light";
console.log(mood);
// light
moood = "dark";
console.log(moood)
//dark
```

Um exemplo. Para lembrar da quantidade de reais que Sig ainda lhe deve, você cria uma variável. E então quando ele lhe paga 30 reais, você dá a essa variável um novo valor:

```js
var SigDeve = 200;
SigDeve = SigDeve - 30;
console.log(SigDeve);
//170
```

```js
const preco1 =5;
const preco2 =6;
let total = preco1 + preco2;
```

Essas duas variáveis, <code>preco1</code> e <code>preco 2</code> são declaradas com <code>const</code>, esse são valores constantes e não podem ser alterados. 

A variável <code>total</code> é declarada com <code>let</code> e seu valor pode ser alterado

<em>FUNÇÕES</em>

Uma função é um pedaço de programa envolvido por um valor. Este valor pode ser aplicado a dim de executar o programa envolvido. Por exemplo, no ambiente do navegador, a variável <code>alert</code> detém a função de mostrar uma pequena caixa de diálogo com uma mensagem:

```js
alert("Bom dia!");
```
<em>FUNÇÃO <code>console.log</code></em>

A maioria dos sistemas JavaScript fornecem uma função <code>console.log</code> que escreve seus argumentos de texto na saída do dispositivo:

```js
var x = 30;
console.log("o valor de x é", x);
//o valor de x é 30
```

<em>RETORNANDO VALORES</em>

Temos a função <code>Math.mx</code> , que pega dois números e retorna o maior entre eles:

```js
console.log(Math.max(2, 4));
```
No exemplo abaixo, temos uma expressão chamada <code>Math.min</code>, que é o oposto de <code>Math.max</code>, é usada como uma das entradas para o operador de soma:

```js
console.log(Math.min(2, 4) + 100);
```

<em><code>prompt</code> e <code>confirm</code></em>

O ambiente fornecido pelos navegadores contém algumas outras funções para mostrar janelas. Você pode perguntar a um usuário uma questão OK/Cancel usando <code>confirm</code>. Isto retorna um valor booleano: <code>true</code> se o usuário clica em OK e <code>false</code> se o usuário clica em Cancel.

```js
confirm("Então, vamos?");
```
<code>prompt</code> pode ser usado para criar uma questão "aberta". O primeiro argumento é a questão; o segundo é o texto que o usuário inicia. Uma linha de texto pode ser escrita dentro da janela de diálogo e a função vai retornar isso como uma string:

```js
prompt("Me diga tudo o que você sabe", "...");
//retorna um valor do tipo string
```

Essas duas funções não são muito utilizadas na programação moderna para web, principalmente porque você não tem controle sobre o modo que a janela vai aparecer.

<em>FLUXO DE CONTROLE</em>

Quando seu programa contém mais que uma declaração, as declarações são executadas previsivelmente de cima para baixo. Como por exemplo, o programa a seguir tem duas declarações. A primeira pergunra ao usuário por um número, e a segunda, que é executada depois, mostra o quadrado desse número:

```js
var numero = Number(prompt("Escolha um número", ""));
alert("Este número elevado ao quadrado é igual a:" + numero * numero);
```

A função <code>Number</code> converte o valor para um número. Nós precisamos desta conversão pois o resultado do <code>prompt</code> é um valor do tipo <code>string</code>, e nós queremos um número.

<em>EXECUÇÃO CONDICIONAL</em>

A Execução Condicional é onde escolhemos entre duas rotas baseado em um valor booleano (ou seja, <code>true</code> ou <code>false</code>). A execução condicional é escrita com a palavra <code>if</code>. No caso mais simples, essa palavra é usada se, e somente se, uma certa condição existir. No programa anterior, por exemplo, podemos mostrar o quadrado do dado fornecido como entrada somente se ele for realmente um número:

```js
var numero = Number(prompt("Escolha um número", ""));
if (!isNaN(numero)) // se variável numero for não Not a Number
    alert("Este número elevado ao quadrado é" + numero*numero);
```

Você frequentemente não terá um código que executa apenas quando uma condição for verdadeira, mas também que lida com outros casos. A palavra-chave <code>else</code> pode ser usada, juntamente com <code>if</code>, para criar dois caminhos distintos de execução:

```js
var numero = Numbee(prompt("Escolha um número:", ""));
if (!Nan(numero))
    alert("Este número elevado ao quadrado é igual a:" + numero * numero);
else
    alert("Isto não é um número")
```