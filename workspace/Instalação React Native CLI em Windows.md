[Guilherme Andrade Lacerda](https://lacerda53.medium.com/?source=post_page-----f6c5b59a29cb-----------------------------------)



[![Guilherme Andrade Lacerda](https://miro.medium.com/fit/c/32/32/1*8n_LpsF1xijpS00dH2vaYw.png)](https://lacerda53.medium.com/?source=post_page-----f6c5b59a29cb-----------------------------------)[Guilherme Andrade Lacerda](https://lacerda53.medium.com/?source=post_page-----f6c5b59a29cb-----------------------------------)

Creative 🚀 | Gamer 🎮 | Web & App developer 💻📱| Information System

Mar 7, 2020 · -  4 min read

# Instalação React Native CLI em Windows

![img](https://miro.medium.com/max/1400/1*UamXGsZP3z6qclBBYi70Xg.png)

Quando uma pessoa ingressa em novo aprendizado é muito comum a mesma ter dificuldades em certas execuções simples, e não é novidade que esses pequenos problemas acabam virando desanimo ou motivo para abandono desse novo conhecimento. Por esse e outros motivos esse escrito servirá para ajudar as pessoas que estão tendo dificuldades na instalação do React-Native-CLI.

# **1- Instalação Chocolatey**

Chocolatey é um gerenciador de pacotes popular para Windows, através dele que vamos instalar nossas dependências para que toda instalação do react native ocorra bem.

Para instalar o Chocolatey, abriremos o **powershell** em modo **administrador**, e executaremos o seguinte comando:

```
Set-ExecutionPolicy Bypass -Scope Process
```

Isso fará com que nosso powershell não tenha nenhuma restrição para executar scripts.

Logo após vamos executar mais esse comando, esse sim irá baixar e instalar o chocolatey:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Se a instalação estiver dado certo ao executar “choco” no terminal ele deverá retornar a sua versão instalada.

# **2- Instalação Node, Python2, JDK**

Com a janela do powershell ainda aberta, vamos instalar o node.js, python2 e o jdk8, usando o seguinte comando:

```
choco install -y nodejs.install python2 jdk8
```

Se a instalação estiver correta você conseguirá visualizar a versão de cada item instalado por exemplo:

```
node -v
```

# 3- Instalação React-Native-CLI

Para que consigamos criamos projetos e nosso computador reconheça todas funções do react native cli, iremos instala-lo ainda com o powershell em modo administrador:

```
npm install -g react-native-cli
```

Se tudo estiver certo, você conseguirá ver a versão react-native-cli instalada executando:

```
react-native -v
```

# 4- Instalação e configuração do Android

Muitas pessoas criticam o motivo de instalar o Android Studio, sendo que não iremos programar diretamente em Java ou simplesmente pelo fato do mesmo ser pesado, porém o Android Studio tem algumas funcionalidades que iram nos ajudar a rodar a nossa aplicação em um emulador ou direto no seu smartphone, como por exemplo o gerenciador de SDK ou o criador e gerenciador de emuladores, sem falar nas dependências para o android que ele já nos traz.

[***Clique aqui para baixar o Android Studio\***](https://developer.android.com/studio/index.html)

Instale normalmente apenas apertando em “**Next**” até que a instalação seja concluída.

![img](https://miro.medium.com/max/1312/1*XemNLf9kvrNLY3rePIxAOA.png)

Com o Android Studio aberto, clique em **Configure > SDK Manager**, copie o local onde o SDK está instalado que mais tarde iremos usar, depois de copiar selecione qual SDK deseja instalar e clique em OK, cada SDK tem sua versão android, eu instalei o Android 9.0(Pie) e o 10.0(Q), após isso ele pedirá permissão para instalar, permita e instale.

![img](https://miro.medium.com/max/1400/1*8jnrvvKU4SSnvWq6lnUmpw.png)

# 5- Configuração das Variáveis de Ambiente

Após concluir todos os passo a cima, iremos configurar para que todo nosso sistema entenda algumas funcionalidades do android, iremos em **Painel de Controle > Sistema > Configurações avançadas do sistema > Variáveis de Ambiente…**

![img](https://miro.medium.com/max/1238/1*q91OClMBN-NHWnqu88GU9Q.png)

Clique em Novo… dentro de Variáveis de Usuário e preencha da seguinte forma, porém no valor da variável, cole aquele caminho que copiamos do SDK e clique em OK:

![img](https://miro.medium.com/max/1308/1*gGetXFBg6XDHxQUR9idCLw.png)

Depois selecione o Path da variável de usuário e clique em Editar, agora clique em Novo e escreva o seguinte comando:

```
%ANDROID_HOME%\platform-tools
```

Clique em Novo novamente e escreva outro comando após escrever clique em OK até que fechem todas as janelas de variáveis de Ambiente:

```
%ANDROID_HOME%\tools
```

## E pronto.

Para conferir se as variáveis ambientes estão funcionando corretamente, abra seu powershell e execute:

```
adb devices
```

Esse comando deve retornar uma lista de dispositivos detectados, caso tenha algum emulador rodando ou seu celular esteja plugado, ele deve ser listado ao executar esse comando, no meu caso ele retornou meu celular que estava plugado.

![img](https://miro.medium.com/max/898/1*SEmsB4pZ6Ti1fs4TXf_aTw.png)

## Comandos Úteis:

- ***react-native init MeuPrimeiroApp\*** *(Cria um projeto React Native)*
- ***react-native run-android\*** *(Roda o projeto em um dispositivo Android)*
- ***react-native run-ios\*** *(Roda o projeto em um dispositivo IOS)*
- ***adb devices\*** *(Lista Dispositivos conectados)*

**Referencia:**

[Getting Started · React NativeThis page will help you install and build your first React Native app. If you already have React Native installed, you…reactnative.dev](https://reactnative.dev/docs/getting-started)

https://lacerda53.medium.com/?source=post_page-----f6c5b59a29cb-----------------------------------)

