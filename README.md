# Elm

<b>Componentes:</b><br/>
Jules Brendo - <b>GitHub nickname:</b> - <b>Matrícula:</b> 2015101111<br/>
Marcos Adriano Rocha de Oliveira - <b>GitHub nickname:</b> marcosadriano99 - <b>Matrícula:</b> 20141011110298<br/>
Paulo Victor Freire Ribeiro Damasceno - <b>GitHub nickname:</b> pvictorfreitas - <b>Matrícula:</b> 20141011110085

<h2>Resumo</h2>

<p>Elm  é uma linguagem de programação específica de domínio para a criação declarativa de interfaces de usuário gráficas baseadas em web browser . Elm é puramente funcional , e é desenvolvido com ênfase na usabilidade , desempenho e robustez. Sendo considerada uma linguagem bastante pequena e simples, torna-se fácil então a criação de interfaces gráficas para a Internet. Elm quando compilada tem como alvos JavaScript, HTML e CSS. Elm é uma linguagem ainda muito jovem, inicialmente concebida por Evan Czaplicki como sua tese em 2012. O primeiro lançamento de Elm veio com muitos exemplos e um editor on-line que tornou mais fácil para experimentar em um navegador web.  Evan Czaplicki juntou-se a Prezi em 2013 para trabalhar em Elm, e em 2016 mudou-se para NoRedInk como um Engenheiro de Código Aberto, também começando a Elm Software Foundation. Atualmente está na versão 0.16.</p>
<p>Elm utiliza o paradigma de programação FRP (Functional Reactive Programming), ou seja, é uma linguagem funcional que está alerta ao tempo. Por outro lado desenvolvimento em Elm diverge da maioria das alternativas porque não utiliza a arquitetura MVC (Model, View & Controller). O fluxo de informação num programa Elm, que corre dentro do navegador de Internet, segue apenas uma direção.
</p>  


<h2>Instalação e uso</h2>
<p>
Para instalar a linguagem Elm é necessário o Node.Js para proceder à sua compilação. A infra-estrutura Elm também disponibiliza um gestor de pacotes, ferramenta de testes unitários, REPL (Read, Evaluate, Print, Loop), debugger e instaladores para Windows e Mac que podem ser descarregados em http://elm-lang.org. A instalação em Ubuntu é feita com os seguintes comandos, começando por instalar o Node.Js seguida da instalação de Elm:
</p>
<p>

$ curl -sL https://deb.nodesource.com/setup_5.x | sudo -E 
bash -
$ sudo apt-get install -y nodejs
$ npm install -g elm


</p>
<p>
Agora estamos prontos para criar o nosso primeiro programa em Elm. A forma mais simples é partir de uma infra-estrutura e preencher apenas algumas funções. Esta infra-estrutura será responsável pelo fluxo de informação e pela recepção de sinais a que o nosso programa responderá (o tempo, o clicar e mover do rato e o teclado são exemplos de sinais). Os sinais registados no programa levarão a uma mudança no estado do programa e consequentemente a uma atualização da interface gráfica.
</p>

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
