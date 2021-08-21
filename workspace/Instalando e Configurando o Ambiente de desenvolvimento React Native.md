# Instalando e Configurando o Ambiente de desenvolvimento React Native

Neste artigo vou apresentar como instalar e configurar o ambiente de um projeto com React Native no Linux. O React Native é um framework JavaScript para realizar o desenvolvimento de aplicativos nativos Android e IOS utilizando o JavaScript. Para configurar um projeto inicial vamos precisar:

- Node.js
- npm
- Java
- QEMU KVM
- Android Studio
- React Native CLI



### Instalando o Node.js

Para utilizar o framework React Native é necessário possuir o **Node.js**. Abra o terminal Linux e atualize o **cache APT**.

```
sudo apt update
```

Realize a instalação do Node.js.

```
sudo apt install nodejs
```

### Instalando o NPM

Vamos instalar o gerenciador de pacotes **NPM**, para instalarmos e gerenciarmos o React Native e as demais dependências do nosso projeto. Realize a instalação do NPM.

```
sudo apt install npm
```

### Instalando o Java

Vamos instalar o **Java** que é necessário para utilizarmos o Android Studio. Primeiro adicione o repositório do java ao **APT**.

```
sudo add-apt-repository ppa:webupd8team/java
```

Após adicionado o novo repositório atualize o **cache APT**.

```
sudo apt-get update
```

Realize a instalação do Java Runtime Environment.

```
sudo apt install default-jre
```

Realize a instalação do Java Development Kit.

```
sudo apt install openjdk-8-jdk
```

### Instalando o QEMU KVM

Vamos instalar o **QEMU KVM**, que é necessário para utilizarmos o emulador de Android para testarmos nosso aplicativo. Realize a instalação do QEMU KVM.

```
sudo apt install qemu-kvm
```

Adicione o seu usuário ao grupo do **KVM**.

```
sudo adduser $USER kvm
```

Altere o usuário do utilitário **KVM** para o seu usuário.

```
sudo chown $USER /dev/kvm
```

### Instalando o Android Studio

Vamos instalar o **Android Studio** que é necessário no desenvolvimento de aplicações para o Android.

Realize o download do Android Studio no link: https://developer.android.com/studio. Acesse o diretório onde foi realizado o download e realize a extração dos arquivos.

```
gzip -d android-studio-ide-193.6821437-linux.tar.gz
tar -zxvf android-studio-ide-193.6821437-linux.tar
```

Mova os arquivos extraídos para o diretório **/opt/google/** .

```
sudo mv android-studio /opt/google/
```

Acesse o diretório **bin** e utilize o **script** de instalação do android studio

```
cd bin
sudo ./studio.sh
```

Siga as instruções do utilitário de instalação do Android Studio.

Agora vamos realizar a configuração, para que seja possível iniciar o Android Studio apenas clicando em um link no menu de aplicativos do Ubuntu.

Primeiro crie um link simbólico do executável para o diretório **/bin**, para que seja possível iniciar o Android Studio utilizando o comando **android-studio**, independentemente do diretório de trabalho atual.

```
sudo ln -sf /opt/android-studio/bin/studio.sh /bin/android-studio
```

Agora para configurar o link no menu crie o arquivo **/usr/share/applications/android-studio.desktop** com seu editor de texto de preferência.

```
sudo vim /usr/share/applications/android-studio.desktop
```

E adicione o seguinte conteúdo no mesmo

```
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio 4.0.2
Comment=Android Studio
Exec=bash -i "/opt/google/android-studio/bin/studio.sh" %f
Icon=/opt/google/android-studio/bin/studio.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=jetbrains-android-studio
Name[en_GB]=android-studio.desktop
```

**Observação:** Confira se os caminhos que estão descritos no conteúdo acima são os mesmos em seu computador.

### Instalando o React Native CLI

Vamos instalar o **React Native CLI** (interface de linha de comando), que é o utilitário principal que nos permite utilizar comandos do react native por linha de comando. 

```
sudo npm install -g react-native-cli
```

### Configurando as variáveis de ambiente

Por último temos que configurar algumas variáveis de ambiente, para que possamos utilizar todas as ferramentas no desenvolvimento com o React Native. Abra o arquivo **.bashrc** com seu editor de preferência.

O arquivo **.bashrc** possui comandos que são executados no momento em que o usuário inicia um **shell** que não requer autenticação.

```
sudo vim $HOME/.bashrc
```

Cole o seguinte conteúdo no final dele

```
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

Após isto temos todo nosso ambiente configurado para começarmos o desenvolvimento de aplicativos Android utilizando o **React Native**. No artigo [Iniciando o desenvolvimento de um App Android com React Native](https://irias.com.br/blog/iniciando-desenvolvimento-app-android-react-native/) parto deste ponto e apresento como criar nossa primeira aplicação com o React Native.

O projeto está disponível em meu GitHub: https://github.com/andersonirias/react-native-tutorial.

![img](https://secure.gravatar.com/avatar/caebd4e8a2065973eb995c3f7d34641c?s=49&d=mm&r=g)Autor[Anderson Irias](https://irias.com.br/blog/author/anderson-irias/)Publicado em[10 de outubro de 2020](https://irias.com.br/blog/instalando-configurando-ambiente-react-native/)Categorias[Desenvolvimento](https://irias.com.br/blog/category/desenvolvimento/), [React Native](https://irias.com.br/blog/category/react-native/), [React Native Tutorial](https://irias.com.br/blog/category/react-native-tutorial/)Tags[Desenvolvimento](https://irias.com.br/blog/tag/desenvolvimento/), [JavaScript](https://irias.com.br/blog/tag/javascript/), [Node.js](https://irias.com.br/blog/tag/node-js/), [React Native](https://irias.com.br/blog/tag/react-native/)

## Um comentário em “Instalando e Configurando o Ambiente de desenvolvimento React Native”

1. Pingback: [Criando o primeiro componente com React Native – Irias Lab](https://irias.com.br/blog/criando-o-primeiro-componente-com-react-native/)