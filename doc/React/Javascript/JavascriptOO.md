# Javascript em Orientação ao Objeto

Para trabalhar com Javascript e sua orientação ao Objeto. Podemos definir da seguinte forma:


```javascript
// declaração da classe
class Casa{

    // você precisa declarar um construtor para declarar variáveis
    constructor(corAtributo, quantidateJanelasAtributo{
        this.cor = corAtributo;
        this.quantidade = quantidateJanelasAtributo;
    }

    // declaração de métodos
    abrirPortao(){

    }

    // declaração do método estático
    static abrirPortao(){

    }

}

// instanciação do objeto

var casa = new Casa();
casa.abrirPortao();

```

### @Curiosidades

* O Javascript contém uma o CaseSentive, o que informa que as classes podem receber nomes com letras minuscula para fazer a declaração de classes.
* `this` pode ser usado para acessar um atributo ou definir o atributo da classe;
    * Ele também pode chamar os métodos.
* Métodos estáticos, você não precisa de instanciar o objeto. Então você não precisa gastar valor de memória.
* instanciação com as classes com `extends`.

* A sobreescrita do método das classes:

```javascript

class Animal{
    dormir(){
        document.write('+Dormir');
    }
}

class Cao extends Animal{
    dormir(){
        document.write('+Dormir sendo escrito');
    }
}

```

Lembrando que o uso da palabra `super` você consegue acessar os atributos e métodos da classe pai. Exemplo:


```javascript
class Cao extends Animal{
    
    // rescrever o construtor
    constructor(cor, peso, raça){
        // você mesmo assim precisa escrever os métodos do animal.
        super(cor, peso);
        this.raça = raça;
    }

    latir(){
        // code...
    }

    dormir(){
        // método do pai.
        super.dormir();
        document.write(' como um cão');
    }
}
```

### **Literais** e **Json**

> a Diferença dos objetos literais e dos objetos a partir de Json e quase nula, porque um é usada para __código__ outro é usado para __comunicação__ entre serviços

* Objeto `Literal` é um objeto definido diretamente

```javascript

var objetoLiteral = {
    cor: 'Marrom',
    peso: 30,
    raça: 'Labrador',
    filhotes: {
        filho1: 'Generio',
        filho2: 'Generico'
    }
}

// exibindo os atributos diretamente
document.write(objetoLiteral.cor);

```

Ele é criado com a função de armazenamento na maioria dos casos. Objeto estático `pré-definido`;

    * exemplos de uso:
        O que pode ser definido como:
    
```javascript
// para a criação de textos
var formatacaoTexto = {
    cor: "Amarelo",
    tamanho: 30
};

// posição de imagem
var imagem = {
    posicao: "centro",
    tamanho: {
        largura: 200,
        altura: 300
    } 
};
```

* Objeto de `Json` é um objeto 

normalmente objetos do tipo `Json` ele são usados para _consultas_ ou _inforamções_:

```json
{
    "atributo": "qualidade"
}
```

no código ficaria:

```javascript
var objetoJson = '{"cor": "Marrom", "peso": 30, "raca": "Labrador"}';

var objetoConvertido = JSON.parse(objetoJson);

```

### Exemplo:

```javascript
class Objeto extends ObjetoFather{
    constructor(atributo){
        this.atributo = atributo;
    }

    getAtributo(){
        return this.atributo;
    }

    setAtributo(atributo){
        this.atributo = atributo
    }

    static abrirPortao(){
        document.write('Abrir Portão');
    }
}

var objetoGenerico = new Objeto;
```