# Desafio da semana #4

```js
/*
Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.
*/
var isTruthy = function(x){
    return !!x;
// Invoque a função criada acima, passando todos os tipos de valores `falsy`.
isTruthy("");
isTruthy(undefined);
isTruthy(null);
isTruthy(NaN);
isTruthy(0);
isTruthy(-0);
isTruthy(false)
/*
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.
*/

isTruthy(" ");
isTruthy(!false);
isTruthy(1);
isTruthy(20 * 0);
isTruthy([]);
isTruthy({});
isTruthy("Tiago");
isTruthy(!console.log(););
isTruthy(39 + 39);
isTruthy(22 - 22);

/*
Declare uma variável chamada `carro`, atribuindo à ela um objeto com as
seguintes propriedades (os valores devem ser do tipo mostrado abaixo):
- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
*/
var carro = {marca: "myMarca",
			 modelo: "Fiat",	
			 placa: "1234-ABC",
			 ano: 2017,
			 cor: "Prata",
			 quantasPortas: 4,
			 quantidadePessoas: 0
};

/*
Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.
*/
var mudarCor = function(cor){
	carro.cor = cor;
}

/*
Crie um método chamado `obterCor`, que retorne a cor do carro.
*/
var obterCor =  function(){
	return carro.cor;
};

/*
Crie um método chamado `obterModelo` que retorne o modelo do carro.
*/
obterModelo = function(){
	return carro.modelo;
};

/*
Crie um método chamado `obterMarca` que retorne a marca do carro.
*/
obterMarca = function(){
	return carro.obterMarca;
};

/*
Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.
*/
obterMarcaModelo = function(){
	return "Esse carro é um " + carro.marca + " "+carro.modelo+;
};

/*
Crie um método que irá adicionar pessoas no carro. Esse método terá as
seguintes características:
- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse
número não precisa encher o carro, você poderá acrescentar as pessoas aos
poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método
deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por
parâmetro for ultrapassar o limite de assentos do carro, então você deve
mostrar quantos assentos ainda podem ser ocupados, com a frase:
	
- Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno
citado acima, no lugar de "pessoas".
*/
var carro = {marca: "myMarca",
			 modelo: "Fiat",	
			 placa: "1234-ABC",
			 ano: 2017,
			 cor: "Prata",
			 quantasPortas: 4,
			 quantidadePessoas: 0,
			 assentos: 5
};

var adicionarPessoas = function(x){
var limitePessoas = 5;
var totalPessoas = carro.quantidadePessoas + x;
	if(carro.quantidadePessoas === carro.assentos && x >= carro.assentos){
	return "Carro cheio";
}	
if(totalPessoas > carro.assentos ){
	var qnt =  carro.assentos - carro.quantidadePessoas;
	var plurorsing = qnt === 1 ? "pessoa" : "pessoas";
	return "Só cabe mais "+ qnt + " "+plurorsing;
}
carro.quantidadePessoas += x;
return "já temos "+carro.quantidadePessoas+" no carro";
};


/*
Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?
*/
carro.obterCor();//rosa
// Mude a cor do carro para vermelho.
carro.mudarCor("vermelho");

// E agora, qual a cor do carro?
//vermelho

// Mude a cor do carro para verde musgo.
carro.mudarCor("verde musgo");

// E agora, qual a cor do carro?
//verde musgo

// Qual a marca e modelo do carro?
//myMarca - modelo: "Fiat

// Adicione 2 pessoas no carro.
adicionarPessoas(2);

// Adicione mais 4 pessoas no carro.
adicionarPessoas(4); 

// Faça o carro encher.
adicionarPessoas(3);

// Tire 4 pessoas do carro.
adicionarPessoas(-4);

// Adicione 10 pessoas no carro.
adicionarPessoas(10);

// Quantas pessoas temos no carro?
//1
```
