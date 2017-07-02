
Javacript é uma linguagem de programaçao, vamos identificar seus pedaços:
 - function
 - var
 - if
 - else
 - return

 Mas tem algumas coisas nele que não são explicitos. Como os tipos.

 Tipos são as estruturas dos dados. Um dado pode ser um numero, ou um texto, ou uma boleana.

 Em javascript temos os seguintes tipos:
- boolean
  - true ou false // sem aspas
  - o tipo mais primordial
- number
  - 0 // numeros nao precisam de aspas
  - logo 0 e '0' são valores diferentes, um é um numero outro é o texto que representa um numero
  - outra coisa util é que quando numeros sao adcionados a strings eles automaticamete se transformam na representacao de si mesmo e são concatenados, atenção esse comportamento nao é comum a maioria das linguagens
- array
  - ['representado por uma chave', 'com inumeros valores', 1, true, false] // cada item separado por uma virgula pode ser de um tipo distinto
  - o texto é na verdade um array de strings, logo mais trabalharemos esse aspecto
- string
  - 'SempreEnvolvido em aspas, podendo serem simples ou duplas'
  - 'parte A' + ' parte B' ->  'parte A parte B' // operacao bem comum concatenar strings com o sinal de adição
- object
  - {propriedade: 'valor'} // semelhantemente as arrays os objetos podem ter dentro de si qualquer numero de itens, sempre identificados por propriedade e seu valor.
- function
  - funcões sao comandos predeterminados que estao a nossa disposicao
- undefined
  - valor nao definido
- null
  - valor nao definido
 

  
 ```javascript
 // mantenham isso em mente
typeof undefined           // undefined
typeof null                // object
null === undefined         // false
null == undefined          // true
 ``` 