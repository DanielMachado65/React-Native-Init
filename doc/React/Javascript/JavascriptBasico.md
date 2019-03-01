# Javascript Básico

### `Var` x `Let`

A diferença de declaração de variáveis de `var` para `let`. Com a declaração do código simples: 

```javascript
// var nome = "Jamilton" ; = global

function exibirNome(){
    var nome = 'Jamilton';
    document.write(nome);

    if (true) {
        let nome2 = "Pedro"; 
        document.write(nome2);
    }

    document.write(nome);
}

exibirNome();
document.write(nome);
```

O que acontece que `var` é equivalente ao escopo __local/global__. Ao contrário da `let` que ficará destinada ao __bloco__.

