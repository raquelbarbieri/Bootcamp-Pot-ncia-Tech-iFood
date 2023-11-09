
# JSON

É um agrupamento de dados de uma maneira organizada. 

É como se fosse uma caixa na qual voce guarda um conjunto de dados e vai transferir essa caixa de um lugar para outro. 

**JSON** signifa: JavaScript Object Natation

É um objeto simples, composto por chave e valor, com o objetivo de transferir dados. 

## Transferindo dados com JSON

    let name = "Raquel"
    let age = 28
    let products = ["mouse 2xm", "Teclado mecânico", "Monitor"]
    let productsValues = [29.90, 129.90, 899.99]

    generateInvoice(name, products, productsValues, age)

    function generateInvoice(name){
        console.log("O comprador é " + name)
        console.log("A idade é " + age)
        console.log("---------------------")
        coonsole.log("O produto é " + products[0])
        console.log("O valor é " + productsValues[0])
    }

Esse mesmo código pode ser escrito de maneira mais organizada e simples usando o JSON: 

    let invoice = {
        name: "Raquel",
        age: 28,
        products: {
            0: ["mouse 2xwm", 29.90],
            1: ["teclado mecânico", 129.90],
            2: ["monitor", 899.90]
        }
    }
    console.log(invoice)

Outro exemplo usando o JSON: 

    let invoice = {
        name: "Raquel",
        age: 28,
        products: {
            0: ["mouse 2xwm", 29.90],
            1: ["teclado mecânico", 129.90],
            2: ["monitor", 899.90],
        },
        taxes: "98.90"
    }

    generateInvoice(invoice)

    function generateInvoice(invoice){
        console.log(`O comprador é ${invoice.name}`)
        console.log(`A idade é ${invoice.age}`)
        console.log("----------------")

        for(let index in invoice.products){
            let [productName, productPrice] = invoice.products[index]
        console.log(`- ${productName}: ${productPrice}`)
        }
    }


No JSON, voce pode agrupar as variáveis que estão dentro do mesmo contexto. 

Qualquer linguagem entende o JSON. Isso faz do JSON um protocolo universal de transferência de dados, inclusive de uma linguagem para outro tipo de linguagem através de uma API (ex: Python para JavaScript).

[Mapa da Aventura](https://helpful-jump-17b.notion.site/Estruturas-de-dados-JSON-8bfc6eeb6b2f4e888d7457402351f953)

