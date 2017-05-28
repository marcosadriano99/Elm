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


<h2>Sintaxe básica</h2>

<h3>Variáveis e constantes - inicialização e comandos de atribuição</h3>

<p>Para declarar variáveis, é utilizado o comando <i>var</i>, e, para atribuir, o símbolo de <i>=</i>, da mesma forma que no JavaScript.</p>

~~~~
var x = "hello, world"

print (x)
hello, world
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

É usado o <i>if</i> e <i>else</i>.

~~~~
var x = "hello world";

if (x === "hello, world") print ("true");
else print ("false");
~~~~

<h3>Estruturas de repetição</h3>

<h5>While</h5>

~~~~
var x = 0;

while (x <= 5){x++; print("teste")}
teste
teste
teste
teste
teste
teste
~~~~

<h5>Do while</h5>

~~~~
var x = 0;

do{print(x); x++;} while(x <= 5);
0
1
2
3
4
5
5
~~~~

<h5>For</h5>

~~~~
for(var x = 5; x >= 0; x--) print(x);
5
4
3
2
1
0
~~~~

<h3>Vetores e strings</h3>

~~~~
var x = ["email um", "email dois", "email tres"];

for (var y = 0; y < x.length; y++) print(x[y]);
email um
email dois
email tres
~~~~

<h2>Sintaxe OO</h2>

<h3>Criando classes e objetos</h3>

<p>Criando Classe e objeto (function):</p>

~~~~
function Pessoa(_nome){
this.nome = _nome;
}
pessoa = new Pessoa("Pedro");

Literais:
var carro = {
marca: "Ford",
modelo: "Ka",
getDetalhes: function (){
return this.marca + ' - ' + this.modelo;
	}
}

carro.modelo = "Novo Ka";
alert(carro.getDetalhes());
~~~~



<h3>Métodos</h3>

~~~~
carro = {
        Marca : "Ford",
        Modelo : "Ka",
        Caracteristicas : ["Preto", 1.0, "2 portas"],
         
        exibirDetalhes : function(){
          alert("Marca: " + this.Marca + " - Modelo: " + this.Modelo)
        }  
    }
     
    carro.exibirDetalhes();
    alert(carro.Caracteristicas[0])
      
    var Pessoa = { nome : "Maria", idade : 30, sexo: "F" } 
     
    var mapa = { 
        cantoSuperiorEsquerdo : { x : 1, y : 1 },
        cantoSuperiorDireito : { x : 10, y : 1 },
        cantoInferiorEsquerdo : { x : 1, y : 10 },
        cantoInferiorDireito : { x : 10, y : 10 }
    }
     
    alert(mapa.cantoInferiorDireito.x); 
 ~~~~

<h3>Construtores</h3>

~~~~
class Produto {
  constructor(paramNome, paramPreco){
    this.nome = paramNome;
    this.preco = paramPreco;
  }
  calculaDesconto() {
     return this.preco * 0.1;
  }
}
var produto1 = new Produto("Blusa", 120);
var produto2 = new Produto("Calça", 300);
produto1.calculaDesconto(); //12
produto2.calculaDesconto(); //30
~~~~

<h3>Herança</h3>

<p>1 – Prototype-chaining Inheritance

Antes de pensarmos na herança, vamos escrever uma função construtora 

utilizando o Pseudo-classical pattern para representar a Pessoa :
var Pessoa = function(nome, email){
    this.nome = nome;
    this.email = email
};
 
Pessoa.prototype.fala = function(){
    console.log("Olá, meu nome é "+this.nome+" e meu email é 

"+this.email);
};

Mas note que, deste modo, nada impede que um desenvolvedor instancie uma 

pessoa com um email inválido:
var leoInvalido = new Pessoa("Leonardo", "emailinvalido");

Por estarmos utilizando uma função construtora, fica fácil resolver esse 

problema:
var Pessoa = function(nome, email){
    this.nome = nome;
    
    if(emailEhValido(email))
       this.email = email
};

Bacana, já temos a nossa Pseudo-classe representando uma Pessoa.
Mas, como disse anteriormente, nós precisamos de um outro tipo de pessoa: 

uma PessoaFisica, que possui CPF e sabe dizê-lo:
var PessoaFisica = function(nome, email, cpf){
    this.nome = nome;
    this.email = email;
    this.cpf = cpf;
};
 
PessoaFisica.prototype.dizCpf = function(){
    console.log(this.cpf);
};

Mas note que, do jeito que implementamos a função construtora 

PessoaFisica, ela não está verificando se o email foi preenchido 

corretamente como estávamos fazendo na Pessoa!

Vamos então reaproveitar a verificação que escrevemos anteriormente. Para 

isso, basta chamar a função Pessoa utilizando a nossa instância (this) 

como referência.

Essa técnica é chamada de Constructor Stealing :

~~~~
var PessoaFisica = function(nome, email, cpf){
    Pessoa.call(this, nome, email);
    this.cpf = cpf;
};
 
PessoaFisica.prototype.dizCpf = function(){
    console.log(this.cpf);
};
~~~~

Isso fará com que nossa PessoaFisica tenha todos os atributos que uma pessoa.</p>

<h3>Categorias de exeções</h3>

<p>
<b>EvalError</b> Cria uma instância que representa um erro que ocorre em relação ao

Função global eval (). </p>
<p><b>InternalError</b> Cria uma instância que representa um erro que ocorre quando um

Erro interno no mecanismo JavaScript é lançado. Por exemplo. "demais

Recursão "</p>
<p><b>RangeError</b> Cria uma instância que representa um erro que ocorre quando um valor numérico

Variável ou parâmetro está fora do seu intervalo válido. </p>
<p><b>ReferenceError</b> Cria uma instância que representa um erro que ocorre quando de-

Referenciando uma referência inválida.</p>
<p><b>SyntaxError</b> Cria uma instância que representa um erro de sintaxe que ocorre enquanto

Analisar código em eval ().</p>
<p><b>TypeError</b> Cria uma instância que representa um erro que ocorre quando uma variável

Ou parâmetro não é de um tipo válido.</p>
<p><b>URIError</b> Cria uma instância que representa um erro que ocorre quando encodeURI

() Ou decodeURI () passam parâmetros inválidos.</p>

<h3>Captura e lançamento de exceções</h3>

~~~~
try {
	document.write('teste');
}

catch(erro) {
	alert("erro no js: " + erro);
}
~~~~

<h3>Criar novas exeções</h3>

~~~~
try {
	if (codigo < 10) {
		throw "erro_1";
	} else {
		if (codigo > 100) {
			throw "erro_2";
		}
	}
} catch (erro) {
	if (erro == "erro_1") {
		alert('Codigo é menor que 10');
	} 
	if (erro == "erro_1") {
		alert('Codigo é maior que 100');
	}
}
~~~~
