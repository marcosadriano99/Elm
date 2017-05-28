# Elm

<b>Componentes:</b><br/>
Jules Brendo - <b>GitHub nickname:</b> - <b>Matrícula:</b> 2015101111<br/>
Marcos Adriano Rocha de Oliveira - <b>GitHub nickname:</b> marcosadriano99 - <b>Matrícula:</b> 20141011110298<br/>
Paulo Victor Freire Ribeiro Damasceno - <b>GitHub nickname:</b> pvictorfreitas - <b>Matrícula:</b> 20141011110085

<h2>Resumo</h2>

<p> O Rhino é uma implementação open source do JavaScript baseada na linguagem Java. A função dessa implementação é possibilitar o reaproveitamento de um código JavaScript dentro do código Java. A utilização do Rhino é bem simples e prática, ele foi criado com a intenção de reaproveitar códigos, assim ganhando produtividade, por não precisar fazer dois códigos idênticos em linguagens diferentes. </p>
<p> O principal mantenedor do Rhino é o Mozilla e seu projeto foi iniciado em 1997, na Netscape. Sua programação é orientada a objetos. 
</p>

<h2>Instalação e uso</h2>

<p>Para ... </p>

~~~~


~~~~

<h2>Elm funcional</h2>

<li>Sem erros de tempo de execução na prática. Sem <i>null</i>. Sem <i>undefined</i>.</li>
<li>Mensagens de erro amigáveis ​​que o ajudam a adicionar recursos mais rapidamente.</li>
<li>Código que bem arquitetado permanece bem arquitetado como seu aplicativo cresce.</li>
<li>Validação semântica automaticamente aplicada para todos os pacotes Elm.</li>
</ul>

<h2>Sintaxe</h2>

<h3>Variáveis e constantes - inicialização e comandos de atribuição</h3>

<p>Para declarar variáveis, é necessário apenas colocar o nome da variável e atribuir, usando o símbolo de <i>=</i>.</p>

~~~~
x = "hello, world"

"hello, world" : string
~~~~

<h3>Operadores relacionais e lógicos</h3>

| Operador  | Descrição |
| ------------- | ------------- |
| ==  | Igual a  |
| <> ou !=  | Diferente de  |
| ===  | Idêntico  |
| !==  | Diferente  |
| > | Maior que  |
| < | Menor que  |
| >=  | Maior ou igual  |
| <=  | Menor ou igual  |
| &&  | E  |
| ||  | Ou  |

<h3>Operadores aritméticos</h3>

| Operadores  | Descrição |
| ------------- | ------------- |
| + | Adição  |
| - | Subtração  |
| *  | Multiplicação  |
| /  | Divisão  |
| %  | Módulo |
| ++  | Incremento  |
| --  | Decremento  |

<h3>Estruturas de controle condicional</h3>

~~~~
if True then "hello" else "world"

"hello" : string

if False then "hello" else "world"

"world" : string
~~~~

<h3>Registros</h3>

~~~~

point = { x = 3, y = 4 }

{ x = 3, y = 4 } : { x : number, y : number1 }

point.x

3 : number

bill = { name = "Gates", age = 57 }

{ age = 57, name = "Gates" } : { age : number, name : string }

bill.name

"Gates" : string

~~~~

<h3>Estruturas de repetição</h3>
