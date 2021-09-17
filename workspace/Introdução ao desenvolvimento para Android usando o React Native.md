# Introdução ao desenvolvimento para Android usando o React Native

- Artigo - 07/02/2022

  

Este guia ajudará você a começar a usar o React Native no Windows para criar um aplicativo multiplataforma que funcionará em dispositivos Android.

## Visão geral

O React Native é uma estrutura de aplicativo móvel de [software livre](https://github.com/facebook/react-native) criada pelo Facebook. Ele é usado para desenvolver aplicativos para Android, iOS, Web e UWP (Windows) fornecendo controles de interface do usuário nativos e acesso completo à plataforma nativa. O uso do React Native exige uma compreensão dos conceitos básicos do JavaScript.

## Comece a usar o React Native instalando as ferramentas necessárias

1. [Instale o Visual Studio Code](https://code.visualstudio.com/) (ou o editor de códigos de sua preferência).

2. [Instalar o Android Studio para Windows](https://developer.android.com/studio). Por padrão, o Android Studio instala o último SDK do Android. O React Native exige o SDK do Android 6.0 (Marshmallow) ou superior. Recomendamos usar o último SDK.

3. Crie caminhos de variável de ambiente para o SDK do Java e o SDK do Android:

   - No menu de pesquisa do Windows, insira: "Editar as variáveis de ambiente do sistema". Isso abrirá a janela **Propriedades do Sistema**.
   - Escolha **Variáveis de Ambiente…** e **Novo…** em **Variáveis de usuário**.
   - Insira o nome da variável e o valor (caminho). Os caminhos padrão para os SDKs do Java e do Android são mostrados a seguir. Se você tiver escolhido uma localização específica para instalar os SDKs do Java e do Android, atualize os caminhos de variável de acordo.
     - JAVA_HOME: C:\Arquivos de Programas\Android\Android Studio\jre\jre
     - ANDROID_HOME: C:\Users\username\AppData\Local\Android\Sdk

   ![Screenshot of adding environmental variable path](https://docs.microsoft.com/pt-br/windows/images/add-environmental-variable-path.png)

4. [Instalar o NodeJS para Windows](https://nodejs.org/en/) O ideal é considerar o uso do [nvm (Gerenciador de Versão do Node) para Windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) se você está trabalhando com vários projetos e a versão do NodeJS. Recomendamos instalar a última versão do LTS para novos projetos.

 Observação

O ideal também é instalar e usar o [Terminal do Windows](https://www.microsoft.com/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab) para trabalhar com sua CLI (interface de linha de comando) preferida, bem como o [Git para o controle de versão](https://git-scm.com/downloads). O [JDK do Java](https://www.oracle.com/java/technologies/javase-downloads.html) vem empacotado com o Android Studio v2.2 e posterior, mas se você precisar atualizar o JDK separadamente do Android Studio, use o [Windows x64 Installer](https://www.oracle.com/java/technologies/javase-jdk14-downloads.html).

## Criar um projeto com o React Native

1. Use o [npx](https://www.npmjs.com/package/npx), a ferramenta de executor de pacote que é instalada com o **npm**, para criar um projeto do React Native. no prompt de comando do Windows, no PowerShell, no [Terminal do Windows](https://www.microsoft.com/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab) ou no terminal integrado do VS Code (Exibir Terminal Integrado).

   PowerShellCopiar

   ```powershell
   npx react-native init MyReactNativeApp
   ```

2. Abra o novo diretório "MyReactNativeApp":

   PowerShellCopiar

   ```powershell
   cd MyReactNativeApp
   ```

3. Se você quiser executar o projeto em um dispositivo Android de hardware, conecte o dispositivo ao computador com um cabo USB.

4. Se quiser executar seu projeto em um Android Emulator, você não precisará realizar nenhuma ação, pois o Android Studio é instalado com um emulador padrão. Caso deseje executar seu aplicativo no emulador para um dispositivo específico. Clique no botão **Gerenciador de AVD** na barra de ferramentas.

   ![Screenshot of the AVD Manager button](https://docs.microsoft.com/pt-br/windows/images/android-studio-avd-manager.png).

5. Para executar o projeto, insira o comando a seguir. Isso abrirá uma nova janela de console exibindo o Node Metro Bundler.

   PowerShellCopiar

   ```powershell
   npx react-native run-android
   ```

   ![Screenshot of Metro Bundler in a console window](https://docs.microsoft.com/pt-br/windows/images/metro-bundler-console.png)

   ![Screenshot of the default React Native app running in an Android emulator](https://docs.microsoft.com/pt-br/windows/images/react-native-android-emulator.png)

    Observação

   Se você estiver usando uma nova instalação do Android Studio e ainda não tiver feito nenhum outro desenvolvimento no Android, poderá receber erros na linha de comando ao executar o aplicativo sobre como aceitar licenças para o SDK do Android. Como "Aviso: licença para o pacote do SDK do Android Plataforma 29 não aceita".Para resolver isso, clique no botão **Gerenciador de SDK** no Android Studio ![Screenshot of the SDK Manager button](https://docs.microsoft.com/pt-br/windows/images/android-studio-sdk-manager.png). Ou, então, você pode listar e aceitar as licenças com o comando a seguir, lembrando-se de usar o caminho para a localização do SDK no computador.

   PowerShellCopiar

   ```powershell
   C:\Users\[User Name]\AppData\Local\Android\Sdk\tools\bin\sdkmanager --licenses
   ```

6. Para modificar o aplicativo, abra o diretório do projeto `MyReactNativeApp` no IDE de sua preferência. Recomendamos usar o VS Code ou o Android Studio.

7. O modelo de projeto criado pelo `react-native init` usa uma página principal chamada `App.js`. Essa página é pré-preenchida com muitos links úteis para informações sobre o desenvolvimento do React Native. Adicione um texto ao primeiro elemento de **Texto**, como a cadeia de caracteres "OLÁ, MUNDO" exibida abaixo.

   JavaScriptCopiar

   ```javascript
   <Text style={styles.sectionDescription}>
     Edit <Text style={styles.highlight}>App.js</Text> to change this
     screen and then come back to see your edits. HELLO WORLD!
   </Text>
   ```

8. Recarregue o aplicativo para mostrar as alterações feitas. Há várias maneiras de fazer isso.

   - Na janela do console do Metro Bundler, digite "r".
   - No emulador de dispositivo do Android, toque duas vezes em "r" no teclado.
   - Em um dispositivo Android de hardware, agite o dispositivo para abrir o menu de depuração do React Native e selecione 'Recarregar'. ![Screenshot of the React Native debug menu](https://docs.microsoft.com/pt-br/windows/images/react-native-debug-menu.png)

## Recursos adicionais

- [Desenvolver aplicativos de tela dupla para Android e obter o SDK de dispositivo do Surface Duo](https://docs.microsoft.com/pt-br/dual-screen/android/)
- [Adicionar exclusões do Windows Defender para aprimorar o desempenho](https://docs.microsoft.com/pt-br/windows/android/defender-settings)
- [Habilitar o suporte de virtualização para aprimorar o desempenho do Emulador](https://docs.microsoft.com/pt-br/windows/android/emulator#enable-virtualization-support)

------

## Conteúdo recomendado

- [React Native para o desenvolvimento de aplicativos da área de trabalho do Windows](https://docs.microsoft.com/pt-br/windows/dev-environment/javascript/react-native-for-windows)

  Instale o React Native para Windows e comece a usar o desenvolvimento de aplicativos da área de trabalho do Windows usando os componentes do React Native.

- [Instalar o React no Windows](https://docs.microsoft.com/pt-br/windows/dev-environment/javascript/react-on-windows)

  Configure um ambiente de desenvolvimento do React no Windows 10.

- [Instalar o Vue.js diretamente no Windows](https://docs.microsoft.com/pt-br/windows/dev-environment/javascript/vue-on-windows)

  Um guia para ajudar você a começar a usar as estruturas da Web Vue.js diretamente no Windows.

- [Instalar o Next.js no Windows](https://docs.microsoft.com/pt-br/windows/dev-environment/javascript/nextjs-on-wsl)

  Um guia para ajudar você a começar a usar as estruturas da Web Next.js no Subsistema do Windows para Linux.