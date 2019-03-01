# React

> em termos técnicos explica-se esse documento o React como em si uma tecnologia.

```javascript
// classe javascript classe. 
// IDEIA: Component ele ajuda para componentes
class App extends React.Component{

}
```


#### O que é? 

O `React` é uma biblioteca de Javascript. Que funciona muito bem sozinho. 
    * React - contém os **Javascript**
    * ReactDOM - conduz no DOM da aplicação. 


#### Para que serve?

Produzir conteúdo útil para os usuários e criar uma interação. (HTML) criando assim componentes dinâmicos. 

* EventHandler - dectecção de evento de um usuário.
  * para poder dar interação com o usuário.


#### @Redux

pacote de terceiros que ajudam no desenvolvimento. 


#### JSX

Parece um `HTML` para determinar qual é o conteúdo que vai aparecer na tela do usuário


### Version

para conseguir rodar uma versão especifica do projeto você deve usar:

```shell
react-native init --version="0.44.0" <nome_do_app>/
```

#### Simuladores

tem diferença entre processadores da **INTEL** para a **AMD**.

### Run on your Devise

O que você tem que fazer é deixar o seu celular como modo desenvolvedor. 

```
react-native run-android
```

Para executar a atualização no aplicativo você clica com `R + R`

### métodos alternativos para executar

o que acontece é que pode ocorrer erros, justamente por conta de falha de build. Porque na verdade são várias __Promisses__ (etapas) que são feitas, que se espera que a cada etapa precise da fase anterior. 

* ### Etapas
    * para etapa de inicialização é feita um `react init`
    * Graddle vai fazer uma análise das depêndias para rodar
    * Gerar o __apk__. Que você consegue acessando dentro do projeto do android. (_é um comando gerado dentro do graddle_)
    
    ```
        graddlew assembleDebug
    ```
    
    * O __apk__ vai para a pasta de `build/outputs/apk`;

    * Rodar `react-native start` - _React Pagging_ el. 

    * Criar uma ponte com o despositivo com o computador. Fazendo um direcionamento com `adb reverse < nome da porta > < nome da porta local>` 

    * Instalação dentro do dispositivo, acessando dentro do computador para instalar no dispositivo:

    ```
    cd android\app\build\outputs\apk\adb install < nome do arquivo apk >
    ```

    * Pronto agora temos o aplicativo rodando dentro da aplicação.


* ### Adb (Android Debug Brigde)
    O que é um debugador do android

    Podemos verificar o que está sendo executado no computador `adb device`. Que traz uma lista de dispositivos conectados.

    Podemos fazer o brigde (_ponte_) com o comando `adb reverse tcp:8081 tcp:8081`

    Podemos disparar comandos para dentro do aplicativo: `adb shell input keyevent 46 46`
        * no caso desse comando foi disparado um comando de tecla.
        * `adb shell input keyevent 82`. Você vai abrir o comando do _Android_
    
    Para você conseguir disparar qualquer evento você deverá colocar o `adb shell input < comando >`

--------------------

### First Application

O primeiro aplicativo conforme:

```shell
react-native init first_application 

# ir para dentro do application e instalar a opção do EsLint
npm install --save-dev eslint-config-rallycoding 
```

Criar um arquivo de configuração do projeto: `.eslintrc`;

```
{
    "extends": "raillycoding"
}
```

temos a seguinte parte:

```

index.android.js

```

O que precisamos fazer por primeiro é __incorpoar__.

```javascript
// módulo do react que agora pode ser acesada para essa variável
var React = require('react');

var Text = require('react-native').Text;

var AppRegistry = require('react-native').AppRegistry;

// return de um componente
const App = function (){
    return (
        <Text> Meu primeiro App </Text>
    )
}

AppRegistry.registerComponent('app1',function(){return App});

```

tem a criação e utilização de componentes.
* `const` - foi utilizado porque o valor do __App__ só vai ser de leitura. 
* Renderizar o compontent nativo do _Android_ para texto: {`Text`}
* Registrar um component com `AppRegistry.registerComponent('nome_do_app', function CallBack(){return Elemento})`