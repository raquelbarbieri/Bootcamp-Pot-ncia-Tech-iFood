
## Funções


[Mapa de Aventura](https://helpful-jump-17b.notion.site/Mapa-de-aventura-91f3e9bd923842149d4dba754dc65c07?p=6d66bf3dd4074a8eae993687f8df020e&pm=c)

Uma função nada mais é do que uma pequena fábrica para a qual voce vai enviar coisas e ela vai fazer uma ação e te devolver um resultado.

Uma função é sempre uma ação.

Tem que chamar a função no código. Ex:

	torrar()

	function torrar(){
		console.log(“torrando pão”)
	}

Ex2 - função dentro de função:

	torrar()

	function torrar(){
		console.log(“torrando pão”)
		injetarPao()
	}

	function injetarPao(){
		console.log(“injetar o pão”)
	}

Tudo o que fica dentro das chaves é o escopo da função.

## Importante! 

- Funções nao podem começar com número
- não colocar espaços no nome
- Usar verbos no nome das funções, pois isso vai remeter a ações
- Criar uma função para cada ação - é uma boa prática que facilita na hora de identificar o que cada função executa e evita que mais de uma coisa quebre no código se der erro 
- Uma function main chama todas as funções que voce escreveu no seu código, assim, voce não precisa chamar uma por uma
- Indentação: Visualmente, o Tab ajuda a visualizar o código que está dentro de uma determinada chave. Ajuda a organizar o código. 

## Dicas
- Respeite a indentação. Abriu uma chave, dá um Tab. 
- Métodos também são funções. 

 O Python não usa chaves, como o JavaScript


## Funções com Parâmetros

Uma mesma função executa resultados diferentes.

Ex:

    torrar(“pão de forma”)
    torrar(“pão integral”)

    function torrar(pao){
	console.log(“torrada feita com “ + pão)
    }

O resultado desse código será:

torrada feita com pão de forma
torrada feita com pão integral

Porque o “pão” foi substituído pelos textos das funções

var declara uma variável de maneira global

Boa prática: colocar os valores opcionais ao final da função

Interpolação de Strings: O uso de ${} substitui o uso de +, mas tudo deve estar dentro de crases (``)


## Funções com retorno
Exemplo 1:

    let resultado = soma(5, 5)

    console.log("O resultado dessa função é " + resultado)

    function soma(numA, numB){
        let somatorio = numA + numB
        retorn somatorio
    }

Exemplo 2:

    let userName = getFirstName("Felipe Amaral Silveira Cantos")

    console.log("Seja bem-vindo " + userName)

    function getFirstName(name){
        let firstName = name.split(" ")[0]
        return firstName
    }

No exemplo 2, [0] é a posição da parte do texto que eu quero, no caso, a posição 0. 

Se o nome tiver - ao invés de espaço, o código poderia ser assim:

let userName = getFirstName("Felipe Amaral Silveira Cantos")

    let userName = getFirstName("Felipe-Amaral-Silveira-Cantos", "-")

    console.log("Seja bem-vindo " + userName)

    userName = getFirstName("Carlos Silva Han Solo", " ")

    console.log("Seja bem-vindo " + userName)

    function getFirstName(name, splitChar){
        let firstName = name.split(splitChar)[0]
        return firstName
    }

Essa função pega um nome inteiro e fatia esse nome para pegar a posição que eu quero. 

