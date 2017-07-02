# Fundamentos de Programação
## Encontro 1: O interruptor, a NASA e o computador
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

Linguagens evoluem, as vezes mudam seu foco. Como ocorre hoje com javascript. Tem aplicacoes inteiras que nem mesmo reconhecem mais essa linha document, ou DOM, por que esta sendo usado fora do navegador.

E ainda usando o javascript, ele foi construido com base na Linguagem C, junto com C#, C++, JAVA. Entao teremos muitas coisas semelhantes entre si. Mas cuidado, podem ser semelhantes, mas nao sao iguais.

Exemplos dessas linguagens, resolvendo o caso da lampada.

#### Sintax

### Classificação de linguagem

 - Por níveis
 - Por Tipagem
 - Por runtime

 ### Tipos de dados
 Versao composta.

O modo como enviamos os comandos para a maquina, no nosso caso temos muito mais botões a disposição do que os dois do caso da lâmpada. No nosso caso escolhemos uma outra série de verbos, e guardem isso verbos. Para interagir com o computador.

Sobre verbos e Comandos elétricos. Com reles. Um pequeno exemplo.

Por de trás. O computador entende apenas o que a lâmpada entende, mas ele é uma combinação complexa e intrínseca de semicondutores, que são uma espécie de reles com muito mais comportamentos disponíveis que os simples normalmente fechados e normalmente aberto.

Maaas, a verdade é que tudo isso é apenas para ser sabido, ta la no fundo, e ficar simples de compreender o que vamos fazer.
Como programar?
Vamos entender nossos verbos, esses são comuns a maioria das linguagens.
- Variaveis, Loops, assign, retorno, funções.

Por que inglês?
Basicamente pq é onde foi feita a linguagem, como o comando se chama no fim pouco importa, mas o proncipal é seu comportamento.

Vamos identificar os verbos no Javascript.
Var
Function
=
(parametros)
números
strings
arrays
objetos
Tudo isso vai ficar mais claro quando aplicarmos. Escolhemos o javascript pq é a mais fácil de se começar e nossa aula de mercado usará esse conhecimento.

Escrevendo o caso da lâmpada com javascript.
Escrevendo o caso do rele com javascript.

