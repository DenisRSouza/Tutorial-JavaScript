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

Essas duas variáveis, <code>preco1</code> e <code>preco2</code> são declaradas com <code>const</code>, esse são valores constantes e não podem ser alterados. 

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
var numero = Number(prompt("Escolha um número:", ""));
if (!isNan(numero))
    alert("Este número elevado ao quadrado é igual a:" + numero * numero);
else
    alert("Isto não é um número");
```

Se tivermos mais do que dois caminhos a escolher, ou seja, quando temos mais coisas para validar/checar, então temos 2 ou mais condições. Neste caso, os pares <code>if</code>/<code>else</code> podem ser "encadeados". Aqui temos um exemplo:

```js
if (A>B){
    console.log("Verdade, A é maior que B")
}
else if (A>C){
    console.log("Verdade, A é maior que C")
}
else{
    console.log("Falso, A é menor que B e C")
}
```

Se for pensar em português, a sequência seria algo assim:
- Se (<code>if</code>) A é maior que B?
- Se for verdade (<code>true</code>), mostre a frase --> Verdade, A é maior que B
- Se for falso (<code>false</code>) --> cheque uma nova condição (<code>else if</code>)
- A é maior que C?
- Se for verdade (<code>true)</code>, mostre a frase --> Verdade, A é maior que C
- Senão (<code>false</code>), mostre a frase --> Falso, A é menor que B e C

<em>LOOPS <code>While</code> E <code>Do</code></em>

Considere um programa que imprime todos os números pares de 0 a 12. Uma forma de escrever isso é repetindo o comando <code>console.log</code> 12 vezes. Isso funciona, mas a ideia de escrever um programa é fazer com que algo seja menos trabalhoso, e não o contrário. O que precisamos é de uma maneira de repetir o código. Essa forma de fluxo de controle é chamada de laço de repetição (loop).

Se combinarmos o laço de repetição a uma variável contadora, conseguiremos fazer algo assim:

```js
var number = 0; //0
while (number <=12>){
    console.log(number);
    number = number +2; //2 ...12
}
```

Nesse loop, queremos imprimir o número atual e somar dois em nossa variável. Sempre que precisarmos executar múltiplas declarações dentro de um loop, nós as envolvemos com chaves( <code>{ }</code> ). As chaves, para as declarações, são similares aos parênteses para as expressões. Uma sequência de declarações encolvidas por chaves é chamada de bloco.

Como um exemplo, podemos escrever um programa que calcula e mostra o valor de 2 elevado à décima potência:

```js
var potencia = 1;
var numero = 0;
while (potencia <= 10) {
  numero = 2 ** potencia;
  console.log(numero);
  potencia = potencia + 1;
}
```

O loop <code>do</code> é uma estrutura de controle similar ao <code>while</code>. A única diferença entre eles é que o <code>do</code> sempre executa suas declarações ao menos uma vez e inicia o teste para verificar se deve parar ou não apenas após a primeira execução:

```js
do{
    var name = prompt("Quem é você?");
}
while (!name);
console.log;
```

Esse programa irá forçar você a informar um nome. Ele continuará pedindo até que seja fornecido um valor que não seja uma string vazia. Aplicar o operador <code>!</code> faz com que o valor seja convertido para o tipo Booleano antes de negá-lo, e todas as strings exceto <code>""</code> convertem para <code>true</code>.

<em> LOOPS <code>for</code></em>

