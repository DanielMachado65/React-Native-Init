# Configuração do Ambiente

> Foi utilizado para a configuração do ambiente esse [link](https://github.com/Rocketseat/ambiente-react-native). Para as dúvidas a seguir entrar em contato com o criador. 

### Linux

Para configurar o ambiente Linux. você pode utilizar: 

```bash
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
sudo apt install nodejs
sudo npm install -g react-native-cli
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk


# Versão do Linux 32 bits
sudo apt-get install gcc-multilib lib32z1 lib32stdc++6


# Próximo passo (instalar Android Studio) - distruibuição de Intellij

https://developer.android.com/studio/#downloads


# [Opctional] o próximo passo é configurar Genymotion - emulador Android. 
sudo apt-get install virtualbox
chmod +x genymotion-2.2.2_x64.bin
./genymotion-2.2.2_x64.bin

    ## alterar a versão 2.2.2
    ./genymotion
```

