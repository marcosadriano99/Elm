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


~~~~

$ curl -sL https://deb.nodesource.com/setup_5.x | sudo -E <br>
bash - <br>
$ sudo apt-get install -y nodejs <br>
$ npm install -g elm <br>


~~~~

</p>

<h2>Elm funcional</h2>

<li>Sem erros de tempo de execução na prática. Sem <i>null</i>. Sem <i>undefined</i>.</li>
<li>Mensagens de erro amigáveis ​​que o ajudam a adicionar recursos mais rapidamente.</li>
<li>Código que bem arquitetado permanece bem arquitetado como seu aplicativo cresce.</li>
<li>Validação semântica automaticamente aplicada para todos os pacotes Elm.</li>
</ul>

<br/>

<p>Elm não tenta ter nenhuma relação com o JavaScript, diferentemente das outras linguagens que são compiladas pra ele. É uma linguagem completamente distinta, com seu ecossistema próprio, e que por acaso precisa do JavaScript para poder rodar nos browsers.</p>

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
| // | Divisão inteira |
| ^ | Exponenciação |
| %  | Módulo |
| Negate | Negativo |

<h3>Estruturas de controle condicional</h3>

<p>Quando você deseja ter comportamento condicional em Elm, você usa expressões if then else.</p>

~~~~
if True then "hello" else "world"

"hello" : string

if False then "hello" else "world"

"world" : string
~~~~

<p>As palavras-chave if then else são usadas para separar o condicional e os dois ramos para que não precisamos de parênteses ou chaves.</p>

<h3>Registros</h3>

<p>Um registro é um conjunto de pares chave-valor, semelhante a objetos em JavaScript ou Python. Você vai achar que eles são extremamente comuns e úteis em Elm! Vamos ver alguns exemplos básicos.</p>

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

<p>Assim, podemos criar registros usando chaves e campos de acesso usando um ponto. Elm também tem uma versão de acesso de registro que funciona como uma função. Iniciando a variável com um ponto, você está dizendo, por favor, acesse o campo com o seguinte nome . Isso significa que .nome uma função que obtém o nome do registro.</p>

<h3>Listas</h3>

<p>As listas são uma das estruturas de dados mais comuns em Elm. Elas mantêm uma seqüência de dados relacionados, semelhante a matrizes em JavaScript.</p>

~~~~

nomes = [ "Marcos", "Paulo", "Jules" ]

["Alice","Bob","Chuck"] : string

List.isEmpty nomes

False : bool

List.length nomes

3 : int

List.reverse nomes

["Jules","Paulo","Marcos"] : List string

numeros = [1,4,3,2]

[1,4,3,2] : List number

List.sort numeros

[1,2,3,4] : List number

~~~~

<h3>Funções</h3>

Função isNegative que leva em algum número e verifica se é menor que zero. O resultado será <i>True</i> ou <i>False</i>.</p>

~~~~

isNegative n = n < 0

<function>

isNegative 4

False : bool

isNegative -7

True : bool

isNegative (-3 * -4)

False : bool

~~~~

<h2> Gerenciamento de erros </h2>
<p> Uma das grandes vantagens de Elm é que não te runtime exceptions, ou seja, jamais veremos erros de execução na prática, aquele velho conhecido: </p>

~~~~~
uncaught TypeError: undefined is not a function
~~~~~

<p>O Elm trata os erros como dados (data), e existem três estruturas de dados que o ajudam a lidar com o erro de duas formas diferentes, elas são:</p>

~~~~~
Maybe <br>
Result <br>
Task <br>
~~~~~

<p>O objetivo do Result e do Task são os mesmos, tornar clara a possibilidade de falha e garantir que ela seja tratada adequadamente, a diferença é que o Task também funciona quando temos um código que funciona de forma assincrona.</p>

<p> Um exemplo de utilização do Maybe é a implementação de campos opcionais. Ex:</p>

~~~~~
Type alias User = <br>
{ name : String <br>
, age : Maybe : Int <br>
}
~~~~~

<p> O diferencial do Elm é que se, por exemplo, fosse necessário verificar a idade de um user, seria impossível escrever código onde você esquece que os usuários podem não ter uma idade, o Elm pode se certificar disso, por meio da obrigação do uso da empressão "case", que é necessária para lidar com os dados, porque você precisa usar os construtores "nothing" ou "just" para cria-lo. Isso faz com que o compilador possa identificar as possibilidades.</p>

<h2> Compilador inteligente <h2>
<p> Um dos pontos mais fantásticos do Elm são as mensagens de erro do compilador. Segue o exemplo em que digitamos butto ao invés de button:</p>

~~~~~
view mode = <br>
div [] [butto [onClick Decrement] [text "-"] ]
~~~~~

<p>mensagem de erro:</p>

~~~~~
cannot find variable 'butto'<br>
2| [butto [onClick Decrement] [text "-"]<br> 
   ^^^^<br>
Maybe you want one of the following?<br>
button<br>
html.button
~~~~~
