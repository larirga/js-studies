# Introdução ao JavaScript

## Tipos primitivos
São tipos básicos de dados presentes nas linguagens de programação que usa-se ao escrever os programas de computador. 
* String: que representa uma sequência de uma ou mais camadas delimitadas por aspas "" simples ou duplas. 
* Number: são valores numéricos positivos ou negativos, inteiros ou com casas decimais, não se utiliza aspas. 
* Boolean: tipo lógico representado por dois únicos estados verdadeiro(true) ou falso(false) escrito sempre em ingles e sem aspas.
ps: Em caso de dúvidas sobre qual dado é utilizado, usa-se o operador chamado **typeof** que nos retorna uma string dizendo qual é o tipo de dado que passamos para ele verificar. 

## Operadores Aritméticos 
Para fazermos operações aritméticas o JavaScript nos oferece ferramentas para isso, no qual, podemos escrever expressões matemáticas básicas como adição e subtração. 
### Operadores
* Adição: 1 + 1
* Subtração: 10 - 5
* Multiplicação: 2 * 2
* Divisão: 4 / 2
* Exponenciação: 2³ = 2**3 
* Modulo (resto): 4 % 2 (quando quisermos saber o resto de uma divisão)
Os operadores atuam sob dois elementos, um número a esquerda e o outro a direita, por isso, denomina-se *operadores binários*. 
```js
let salario = 3500;
let aumento = 1000.50;
salario + aumento;
4500.5

salario 
4500.5
salario / 2; 
2250.5
```
Esses operadores são muito utilizados para verificar se um número é o par ou ímpar, porque, se o resto da divisão for 0 sabemos que o número que está dividido por 2 é par caso contrário é ímpar. 
5 % 2;
1

## Operadores de Comparação 
">" maior 
">=" maior ou igual
"<" menor 
"<" menor ou igual 
"===" igualdade
"!==" desigualdade
O que todos esses operadores fazem é comparar dois valores e retornar o resultado boleano, uma comparação funciona como se fosse uma pergunta de verdadeiro ou falso. 
```js
2 > 1 
true
```
> PS: O operador de igualdade que avalia se dois valores são iguais, um = sozinho é um valor de atribuição, entretanto, === é operador de comparação. 
```js
10 = = = 10
true
```
Exemplo: 
```js
let notaDaClara = 125; 
let claraPassouNoDesafio = notaDaClara >= 100; 
claraPassouNoDesafio
true 
``` 
## Operadores Lógicos 
E  && 
<br> OU || (pipe)

Para eu ir para a praia é necessário que o dia esteja ensolarado E que seja final de semana. 

O dia esta ensolarado(E) | É final de semana | Vou para a praia
:------------------- | :----------------: | --------------: 
v | v | v
v | f | f
f | v | f

>As duas condições tem que ser verdadeiras. 
```js
let diaEstaEnsolarado = true;
let ehFinalDeSemana = true; 
diaEstaEnsolarado && ehFinalDeSemana;
true
let vouPraPraia = diaEstaEnsolarado && ehFinalDeSemana;
vouPraPraia
true; 
```
Para eu ir para a praia é necessário que o meu carro tenha gasolina ou eu tenha dinheiro para abastecer

O carro tem gasolina (OU)| Eu tenho dinheiro para abastecer | Vou para a praia
:------------------- | :------------------------------: | ---------------:
V | V | V 
V | F | V
F | V | V
F | F | F
> No caso do OU só é necessário que uma afirmação seja verdadeira para que o resultado da expressão seja verdadeiro. 
```js
let carroTemGasolina = false; 
let tenhoDinheiroPraAbastecer = true; 
carroTemGasolina || tenhoDinheiroPraAbastecer;
true

let vouPraPraia = carroTemGasolina || tenhoDinheiroPraAbastecer;
> vouPraPraia
> true
```
## Estruturas Condicionais 
As estruturas condicionais é um meio pelo qual conseguimos expressar nosso raciocínio lógico e situações de decisões do nosso dia a dia de uma forma estruturada. 

Podemos simular cenários do mundo real em que por exemplo expressamos a lógica de funcionamento de um semáforo na nossa lingugagem humana para o nosso entendimento (cores) e depois traduzimos essa regra lógica de forma estruturada em uma lingugagem de programação. 

Exemplos: 

> **Se** eu estudo, então aprendo, **senão**, não aprendo. 
> <br> **Se** nota do desafio prático for >= 100, aprovado, **senão**, não aprovado. 
> <br> **Se** optei por estudar em algum HUB da Trybe, vou para o HUB, **senão**, estudo em casa. 

## IF/ELSE
Esta presente em todas as lingugagens de programação. 
O significado do IF/ELSE é que o **if** é o *se* e o **else** é o *senão*.

>True (Aprovado) <---- NOTA >= 100 ----> False (Não Aprovado)
```js
let notaDesafio = 150;
if(notaDesafio >= 100) {
    console.log("Aprovado");
} else {
    console.log("Não Aprovado");
}
```

O *console* é uma variável que representa o console do browser e atraves dele temos acesso a várias funções do console. Inclusive, o *console.log* é a função log, que imprime os dados passados para ela entre parentêses na tela. 

> Se você entendeu tudo siga com a aula senão volte para aulas anteriores.
```js
let entendiTudo = true; 
if(entendiTudo){ 
    console.log("Seguir a aula");
} else {
    console.log("Não seguir a aula");
}
```
### Estrutura Condicional Encadeada
Usamos quando precisamos adicionar mais de uma condição na nossa estrutura, como por exemplo:
```js
if(condicao1) {
} else if(condicao2) {
} else {
}
```
### Funcionamento de um Semáforo:
<br>

> **Se** a luz do semáforo está verde, então siga em frente! **senão, se** estiver amarela, atenção, luz ficará vermelha e o sinal fechará! **senão**, pare! luz vermelha. 
<br>

```js
let luzSemaforo = "Verde";
if(luzSemaforo === "Verde") {
    console.log("Siga em frente");
} else if(luzSemaforo === "Amarela") {
    console.log("Atenção! Sinal ficará vermelho!");
} else { 
    console.log("Sinal vermelho! Pare!");
}
```
### Gerações: 
<br>

> * Ano de nascimento menor ou igual a 1945 = Geração silenciosa.
> * Ano de nascimento maior que 1945 e ano de nascimento menor ou igual a 1964 = Boomers.
> * Ano de nascimento maior que 1965 e ano de nascimento menor ou igual a 1980 = Geração x. 
> * Ano de nascimento maior que 1980 e ano de nascimento menor ou igual a 1996 = Millenials.
> * Ano de nascimento maior que 1996 = Geração Z.

<br>

```js
if(anoDeNascimento <= 1954) {
    resultado = "Geração Silenciosa" 
} else if(anoDeNascimento <= 1964) {
    resultado = "Boomers"
} else if(anoDeNascimento <= 1980) {
    resultado = "Geração X"
} else if(anoDeNascimento <= 1996) {
    resultado = "Millenials"
} else {
    resultado = "Geração Z"
}
```
## Arrays
Um Array é uma estrutura capaz de armazenar um conjunto de valores.

> Imagina que deseja fazer uma lista das pessoas aprovadas em um processo seletivo (Joana, Maria, Lucas, Mateus e Paula) e precisamos armazenar essas informações no nosso código.
```js
let listaDeNomes = ["Joana", "Maria", "Lucas", "Mateus", "Paula"];
```
>Se escrever listaDeNomes irá aparecer o número **5**, esse número representa o tamanho do Array. 
Uma propriedade muito importante de um Array é que cada um dos seus *elementos* possuem um **ÍNDICE**, isso significa que os elementos são enumerados sequencialmente. 

```js
> listaDeNomes [0];
< "Joana"
```
PS: Na programação a contagem sempre começa do 0, no caso desse Array, o índice do nome Joana é o 0, no nome Maria é o 1 e o índice do nome Lucas é 2. 

### Adicionar um elemento ao Array já existente: 
Pensando no nosso Array anterior, mais uma pessoa foi aprovada no processo seletivo e temos que adicionar o nome dela na lista. 

<br>

> Os arrays possuem um comando chamado **PUSH** que nos permite adicionar um novo elemento no final do Array.
> 
<br>

```js
 listaDeNomes.push("José");
```
>No console o tamanho do Array é mostrado sempre que seu valor é impresso ou quando a gente adiciona um novo elemento. Entretanto, há um jeito de acessar diretamente as informações, se a gente digitar o nome da nossa variável, e logo em seguida um (.) e depois a palavra **LENGTH** recebemos o número inteiro que representa o tamanho do Array.

```js
listaDeNomes.length;
6
let tamanhoDaListaDeNomes = listaDeNomes.length;
```
Um uso muito comum do atributo **LENGTH** é saber qual a última posição de um array independente do tamanho que ele tiver, a gente sempre começa a contagem das posições do 0, então o último índice do Array vai ser sempre: **TAMANHO DO ARRAY -1**, em um Array de 6 posições a última posição é o 5. 

```js
listaDeNomes[listaDeNomes.length - 1];
```

## STRINGS
Uma propriedade muito importante das strings é que elas podem ser *concatenadas*. Na parte de operadores aritméticos viu-se que quando usamos os operadores "+" entre dois valores númericos, acontece uma soma matemática desses numeros. Quando utilizamos esse mesmo operador entre duas Strings, o que acontece é chamado de **CONCATENAÇÂO**, por exemplo, se eu tenho uma string com meu primeiro nome e outro com meu último nome, se eu somar essas duas variáveis elas vao ser concatenadas, ou seja, uma vai ser adicionada no final da outra. 
```js
let primeiroNome = "Larissa";
let ultimoNome = "Rodrigues";
let nomeCompleto = primeiroNome + ultimoNome;
nomeCompleto
"LarissaRodrigues"
```
Para que exista espaço entre o nome Larissa e o Rodrigues precisamos concatenar uma outra String contendo o espaço entre as duas variáveis. 
```js
nomeCompleto = primeiroNome + "  " + ultimoNome;
"Larissa Rodrigues"
```
Uma STRING é uma sequência de caracteres, por conta disso, uma string com a mensagem **"Bem vindo!"** se compõe por uma sequência de caracteres. Se declararmos a variável mensagem = "Bem vindo!" e depois agregarmos mensagem.length, receberemos como retorno a quantidade de caracteres que esse texto possui e também, conseguiremos acessar cada caractere do texto através do índice da sua posição. 
O primeiro exemplo, é a primeira posição e o segundo é a última posição. 
```js
mensagem [0];
"B"
mensagem [mensagem.length - 1];
"!"
```
## Estrutura de repetição 
Imagine que a gente queira escrever um código que dada uma variável ou número imprimimos todos os resultados da tabuada desse número ou seja, precisamos imprimir a multiplicação desse número por 1 até 9. 
```js
let numero = 7;
console.log(numero * 1);
console.log(numero * 2);
console.log(numero * 3);
console.log(numero * 4);
console.log(numero * 5);
console.log(numero * 6);
console.log(numero * 7);
console.log(numero * 8);
console.log(numero * 9);
```
Essa forma, é mais trabalhosa de se fazer essa estrutura. Por conta disso, acrescentaremos o **FOR**. A sintaxe dessa estrutura começa com o **FOR**, seguido de um parêntese, a primeira coisa dentro do parêntese vai ser a declaração de uma variável que terá o objetivo de contar as nossas repetições. No caso da tabuada, a gente quer repetir o mesmo comando do número 1 até o número 9, então, inicializa-se essa variável "contador" valendo 1. Nessa mesma linha, define-se até quando eu quero que o meu código se repita. Iniciamos com o contador valendo 1 e queremos que ele chegue até o 9, ou seja, desejo que o meu código se repita enquanto o meu contador for menor ou igual a 9. E por último, dentro do parêntese eu tenho que definir como a minha variável "contador" vai ser atualizada a cada repetição, na primeira repetição ela vale 1, na segunda 2 e assim por diante. Desejamos que a cada repetição ela seja acrescida em uma unidade ou seja a cada repetição a variável "contador" vai ser atualizada para valer seu próprio valor + 1. É necessário definir qual o código a gente quer repetir para, para isso, abre e fecha a chave {} que delimita o bloco do código. 
```js
let numero = 7;
for(let contador = 1; contador <=9; contador = contador++){
    console.log(numero + contador);
}
```
> Contador = contador + 1 ou contador++

## For e array
Lista array de pessoas aprovadas. 
```js
let listaDeNomes = ["Joana", "Maria", "Lucas"];
for(let index = 0; index < listaDeNomes.length; indice++) {
    let = "Boas Vindas," + listaDeNomes[index] + !;
    console.log(mensagem)
}
```
Índice | 0 | 1 | 2
:------|:-:| :--: | ---:
Nome | Joana | Maria | Lucas

>A grande vantagem de se usar uma estrutura de repetiçãpo é que independente do tamanho do array o código continua sendo o mesmo, porque ele já esta preparado para percorrer da posição zero até a última posição baseado no tamanho do array. 

## Função 
Funções são blocos de código que encapsularam instruções que executam uma tarefa específica. Elas visam modularizar nossos programas, ou seja, dividir, um programa em partes menores, em que, essas partes menores tenham uma única responsabilidade.
### Exemplos: 
```js
Função 1
2 * 2; 

Função 2 
IP (n>=100){
    console.log("Aprovado");
}

Função 3
let quadrados = [ ];
for(let = 0; i<= 10; i++) {
    quadrados.push(i * i);
}
```

```js
function nomeDaFuncao( ){
    // código
}
```
"( )" -> entrada de valores, parâmetros separados por ","

```js
function nomeDaFuncao(param1, param2) {
    console.log(param1);
    console.log(param2);
}
```
Outra particularidade de uma função é que podemos fazer com que ela retorne **(RETURN)** um valor. 
```js
function nomeDaFuncao (param1, param2){
    return param1 + param2;
}
```
Pode-se declarar variáveis dentro de uma função se necessário. 
```js
function nomeDaFuncao (param1, param2) {
    let resultado = param1 + param2;
    return resultado;
}
```
Incovando uma função: <br>
nomeDaFuncao (10,20); <- com parâmetros <br>
nomeDaFuncao( ); <- sem parâmetros 
## Funcionalidade do carro (jogo)
Ligar e desligar:
```js
let statusCarro = "desligado";
function ligarDesligar() {
    if (statusCarro == "desligado") {
        statusCarro = "ligado";    
    } else {
        statusCarro = "desligado";
    }
    return statusCarro;
} 
```
Acelerar: 
```js
let aceleracao = 0; 
function acelerar(incremento) {
    aceleracao = aceleracao + incremento;
    return "Acelerando a " + aceleracao + "m/s²"
}
```
Frear:
```js
function frear(decremento) {
    aceleracao = aceleracao - decremento;
    return "Desacelerando para " + aceleracao + "m/s²";
}
```
Giro do volante: 
```js
let rotacaoDoVolante = 0;
function girarVolante(anguloRotacao) {
    rotacaoDoVolante = anguloRotacao;
    return rotacaoDoVolante + "°";
}
```