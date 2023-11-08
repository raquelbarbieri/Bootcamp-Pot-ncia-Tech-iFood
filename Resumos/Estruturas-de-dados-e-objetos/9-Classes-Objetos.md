
# O que são classes e objetos

## Relação entre classes e objetos

Na programação, as **classes** padronizam o formato de uma estrutura de dados.

Os **objetos** mantêm a padronização da classe (como uma forma) e implementa seus valores das propriedades.
Também têm métodos inteligentes (funções próprias).

**Instanciar um objeto**
É criar um novo objeto com base em uma classe. 
É como fazer um bolo de outro sabor, mas usando a mesma forma.

Representação de objetos é qualquer coisa. 

## Criando objetos na prática

A classe pode ter comportamento.
Guarda objetos e funções. 

O this chama a classe dentro do escopo dessa classe, no JavaScript.

    class formaDeBolo{
        constructor(saborDaMassa, saborRecheio){
            this.saborDaMassa = saborDaMassa
            this.saborRecheio = saborRecheio
        }
    }

    let boloFesta = new formaDeBolo("massa de chocolate", "recheio de nutella")

    console.log(boloFesta)

## Trabalhando com métodos e propriedades

Um método nada mais é do que uma função que trabalha em contexto de uma classe. 

Diferente de um JSON que é só uma estrutura de dados simples e pura, a classe tem comportamento, comportando objetos e funções.

Um padrão para nominar um tipo de dados do sistema é criado através de uma classe. 

Ex: para guardar os dados do usuário, a classe será Usuario.

Exemplo de classe formaDeBolo:

    class formaDeBolo{
        constructor(saborDaMassa, saborRecheio){
            this.saborDaMassa = saborDaMassa
            this.saborRecheio = saborRecheio
        }
        
        escrever(){
        	console.log(`Um delicioso bolo de ${this.saborDaMassa} com recheio de ${this.saborRecheio}`)
        }
        
        assar(){
        console.log("bolo assando de " + this.saborDaMassa)
        }
    }

    let boloFesta = new formaDeBolo("chocolate", "nutella")
    let boloPremium = new formaDeBolo("baunilha", "coco")

    boloFesta.escrever()
    boloPremium.escrever()
    boloPremium.assar()


## Comparando com outras linguagens

Escrevendo o mesmo código, mas na linguagem Python:

    class FormaDeBolo:
        def __init__(self, sabor_da_massa, sabor_recheio):
            self.sabor_da_massa = sabor_da_massa
            self.sabor_recheio = sabor_recheio

        def escrever(self):
        print(f'Um delicioso bolo de {self.sabor_da_massa} com recheio de {self.sabor_recheio}')

        def assar(self):
            print(f'bolo assando de {self.sabor_da_massa}')

    bolo_festa = FormaDeBolo("chocolate", "nutella")
    bolo_premium = FormaDeBolo("baunilha", "coco")

    bolo_festa.sabor_da_massa = "floresta negra"

    bolo_festa.escrever()
    bolo_premium.escrever()
    bolo_premium.assar()


[Mapa da Aventura](https://helpful-jump-17b.notion.site/Trabalhando-com-Objetos-5cd5de91c7794142948140819ae4b9cc)

