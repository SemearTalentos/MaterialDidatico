# Fundamentos de Programação
## Encontro 1: O interruptor, linguagens e Javascript
O nosso projeto se propõe a trasnformar qualquer um interessado em um desenvolvedor de aplicativos, websites e outros serviços web. Hoje as possibilidades são inumeras, e as necessidades por bons profissionais maiores ainda.

Tudo começa nessa matéria. Aqui vamos desmitificar as habilidades dos seres incompreendidos que chamamos de programadores. Vamos entender que você executa um programa toda vez que acende a lâmpada do seu quarto. 

Também perceberemos o por que chamamos o computador de computador, afinal de contas, nós não usamos ele apenas para computar... ou será que usamos?

Calma, não fuja. Tudo a seu tempo, nesse momento, tente responder para si mesmo, o que é um programa de computador?
    - COLOQUE AQUI SUA RESPOSTA


### O que é programar?
Se você chegou a uma resposta que se assemelha a a alguma dessas, você já começou bem.

Mas vamos esquecer esses conceitos. Vamos nos concentrar agora apenas na lâmpada do seu quarto e o interruptor que liga e desliga a luz.

Consideremos a situação. 
A - Se o interruptor está `desligado` a lampada esta `desligada`
B - Se o interruptor está `ligado` a lampada esta `ligada`

 |   | Interruptor | Lâmpada/resultado   |
 |---|-------------|-----------|
 | A | desligado   | desligada |
 | B | ligado      | ligado    |

Vamos começar a usar uma linguagem mais simples, descobriremos que tudo em programação é sobre simplificar. Entao o ligado será escrito como `1`, e o desligado como `0` 

 |   | Interruptor | Lâmpada/resultado   |
 |---|-------------|-----------|
 | A | 0           | 0         |
 | B | 1           | 1         |

Isso aqui é também um set de instruções que pode ser executado pelo computador. Na verdade, esse é o programa mais simples que qualquer computador pode executar. Ele recebe um dado e devolve esse dado. No nosso caso, esse dado entra como um estimulo fisico, apertar o interruptor, e sai em forma de luz. Logo o dado é processado. Claro que quando falamos em processamento, não é algo tao simples como isso.

Mas vamos aprender a simplificar ainda mais esse nosso diagrama?

Vamos dar letras para os nossos elementos:

 |   | i           | r         |
 |---|-------------|-----------|
 | A | 0           | 0         |
 | B | 1           | 1         |
 
 #### Ação
 Vamos escrever essa instrução em javascript? Acompanhe as proximas linhas copiando-as para o console do seu navegador.(instruçoes para acessar o console)

 ##### Como usar o console
 ###### Acessando

 ###### Operações
 - matemática
 - o = e o 'enter'
 - retorno
 Sobre o sinal `=`. Repare que não estamos perguntando se a lampada é igual a `0`, estamos inserindo o numero `0` na variavel lampada e interruptor. Até inserirmos qualquer coisa numa variavel, ela esta vazia, depende da linguagem para afirmarmos qual é o estado exato dessa variavel sem valor. Em javascript temos 2 tipos de estados vazios, `null` e `undefined`.

```javascript
function acionarInterruptor(a) { 
    // o que entra no argumento, é o que sai. Essa é a função mais simples.
    return a
}
```
Vamos deixar isso mais interesante?
O que acabamos de fazer é a parte mais importante dessa função, mas podemos incrementar.

```javascript
function acionarInterruptor(a) { 
    // o que entra no argumento, é o que sai. Essa é a função mais simples.
    var r
    if(a == 0) {
        r = 'lampada apagada'
    } else {
        r = 'lampada acessa'

    }
    // assim como no quarto transformamos o inpulso fisico em luminoso, aqui estamos transformando o numerico em texto. Parabens, este é o seu primeiro processamento de dados.
    return r
}
```

```javascript
function mudarBackground(valor) {
    document.querySelector('body').style.background = 'rgb(' + valor + ')'
    return valor
}

function acionarInterruptor(a) { 
    // o que entra no argumento, é o que sai. Essa é a função mais simples.
    var r
    if(a == 0) {
        r = 'lampada apagada'
        mudarBackground('0,0,0')
    } else {
        r = 'lampada acessa'
        mudarBackground('255,255,255')
    }
    // assim como no quarto transformamos o inpulso fisico em luminoso, aqui estamos transformando o numerico em texto. Parabens, este é o seu primeiro processamento de dados.
    return r
}
```

```javascript
function mudarBackground(valor) {
    document.querySelector('body').style.background = 'rgb(' + valor + ')'
    return valor
}

function acionarInterruptor(a) { 
    // o que entra no argumento, é o que sai. Essa é a função mais simples.
    var r
    if(!a) {
        r = 'lampada apagada'
        mudarBackground('0,0,0')
    } else {
        r = 'lampada acessa'
        mudarBackground(a)
    }
    // assim como no quarto transformamos o inpulso fisico em luminoso, aqui estamos transformando o numerico em texto. Parabens, este é o seu primeiro processamento de dados.
    return r
}
```
Programação é sempre por partes.
Primeiro, descobrimos qual a logica, com aquele truque da tabela com entrada e resultado.

Despois, vamos adicionando os penduricalhos, no nosso caso, primeiro exibimos uma frase simples no console. depois mudamos a cor do fundo.

### Pausa
### O que é uma linguagem?

Uma linguagem então é um conjunto de comandos, iguais esses que fizemos, mas que resolvem a necessidade não de acender uma lampada, mas de resolver outras necessidades.

Logo, linguagens tem intençoes, são criadas a partir de outras, normalmente ou elas tendem a melhorar algo especifico em uma determinada linguagem ou inovar em como fazer aquilo.

Por exemplo o javascript que usamos, ele foi criado para trazer interaçoes e dinamismo as paginas de web. Então aquela linha document.getelement é uma das bases na qual ele foi criado.

Linguagens evoluem, as vezes mudam seu foco. Como ocorre hoje também com o javascript. Tem aplicacoes inteiras em javascript que nem mesmo reconhecem mais essa linha document, ou DOM, por que esta sendo usado fora do navegador.

Do mesmo modo que o javascript, construido com base na Linguagem C, temos o C#, C++, JAVA. Mas cada uma com a sua propria proposta e intenção.

Exemplos dessas linguagens, resolvendo o caso da lampada.
```C
C
```
```C++
C++
```
```C#
C#
```
```JAVA
JAVA
```

```Objective-C
Objective-C
```

```Swifty
Swifty
```

```lua
lua
```
```python
Python
````
```ruby
Ruby

```
#### Sintax
syntax is the set of rules.
Regras que o programador e o computador concordam.

### Classificação de linguagens

 - Por níveis
   - Alto nível
   - Baixo nível
 - Por Tipagem
   - tipagem fraca
   - tipagem forte
 - Por runtime
   - Compilada
   - Interpretada

A lógica é compartilhda por todas, e nesse curso, vamos focar especificamente na logica. E em como resolver problemas com ela.

Vamos também aprender como encarar uma linguagem nova e descobrir onde estao os recursos dela.

Nossos exercicios aqui vão ser todos feitos com base no javascript. Mas sempre trarei exemplo do recuso nas outras linguagens.

### Bora mais uma vez?
Para finalizar vamos complicar nossa situação da lampada.

No problema que resolvemos o estado do interruptor era enviado para o resultado final. Mas e se eu quiser adicionar 2 interruptores no meu quarto? Essa solução nao me parece muito boa. Vamos pensar construir nossa logica 

interruptor `a` e interruptor `b`

 | a | b | r |
 |---|---|---|
 |0|0|0|
 |1|0|1|
 |0|1|1|
 |1|1|1|

 O que eu quero dizer aqui, que se `a` ou `b` forem verdadeiros eu quero que minha lampada se acenda. Mas esse ainda não é o comportamento ideal. Para apagar essa lampada meus dois interruptores precisam estar desligados. Vamos mudar o foco, pensemos como se os interruptores fossem capinhas, eles mandam apenas um sinal. Não mandam o estado. Esse estado fica dentro da lampada, ela precisa saber se esta ou nao ligada. E ela precisa reagir de acordo.

 `s` para sinal.
 `l` para lampada.

  | s | l | r |
  |---|---|---|
  |0|0|0|
  |1|0|1|
  |0|1|1|
  |1|1|0|

 Esse tipo de arquiterura, nos permite nao colocar apenas mais 1 interruptor, mas sim, qualquer numero de interruptores. Não nos importamos em quem envia o sinal. Mas se ele chega ou não.

 ```javascript
var lampada = false
var corGlobal

function mudarBackground(valor) {
    document.querySelector('body').style.background = 'rgb(' + valor + ')'
    return valor
}

function escolherCor() {
    var cor
    if (!lampada) {
        cor = '0,0,0'
    } else if(corGlobal) {
        cor = corGlobal
    } else {
        cor = '255,255,255'
    }
    mudarBackground(cor)
    return cor
}

function acionarInterruptor() { 
    // Nesse caso nao precisamos de um argumento
    lampada = !lampada // `!` nega a realidade do valor, se era verdadeiro vira falso
   return escolherCor()
}

 ```

 Vamos descobrir que esse tipo de coisa é o mais comum no javascript. Por ele ser uma linguagem voltada para eventos.