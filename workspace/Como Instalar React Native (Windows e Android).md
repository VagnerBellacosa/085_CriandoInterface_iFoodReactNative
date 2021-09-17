[Alexandre Freire](https://dev.to/alexandrefreire)

Posted on 19 de ago. de 2020

# Como Instalar React Native (Windows e Android)

### Instalando dependências

Você precisará do Node, a interface da linha de comando React Native, Python2, um JDK e Android Studio.

Embora você possa usar qualquer editor de sua escolha para desenvolver seu aplicativo, será necessário instalar o Android Studio para configurar as ferramentas necessárias para criar seu aplicativo React Native para Android.

Node, Python2, JDK
Recomendamos instalar o Node e o Python2 via Chocolatey , um gerenciador de pacotes popular para Windows.

O React Native também requer uma versão recente do Java SE Development Kit (JDK) , bem como o Python 2. Ambos podem ser instalados usando o Chocolatey.

Abra um prompt de comando do administrador (clique com o botão direito do mouse em Prompt de comando e selecione “Executar como administrador”) e execute o seguinte comando:

```
choco install -y nodejs.install python2 jdk8
```



Se você já instalou o Node no seu sistema, verifique se é o Node 8.3 ou mais recente. Se você já possui um JDK em seu sistema, verifique se é a versão 8 ou mais recente.

Você pode encontrar opções adicionais de instalação na página Downloads do node .

### A CLI nativa do React

O node é fornecido com o npm, que permite instalar a interface da linha de comandos do React Native.

Execute o seguinte comando em um prompt de comando ou shell:

```
npm install -g react-native-cli
```



Se você receber um erro como Cannot find module 'npmlog', tente instalar npm diretamente: curl -0 -L https://npmjs.org/install.sh | sudo sh.

### Ambiente de desenvolvimento Android

A configuração do seu ambiente de desenvolvimento pode ser um pouco entediante se você é novo no desenvolvimento do Android. Se você já conhece o desenvolvimento do Android, é necessário configurar algumas coisas. Em qualquer um dos casos, siga cuidadosamente as próximas etapas.

1. Instale o Android Studio Baixe e instale o Android Studio . Escolha uma configuração “Personalizada” quando solicitado a selecionar um tipo de instalação. Verifique se as caixas ao lado de todas as opções a seguir estão marcadas:

Android SDK
Android SDK Platform
Performance (Intel ® HAXM)( Veja aqui para AMD )
Android Virtual Device
Em seguida, clique em “Avançar” para instalar todos esses componentes.

Se as caixas de seleção estiverem acinzentadas, você poderá instalar esses componentes posteriormente.

Depois que a instalação estiver concluída e a tela de boas-vindas aparecer, continue com a próxima etapa.

1. Instale o SDK do Android O Android Studio instala o SDK do Android mais recente por padrão. A criação de um aplicativo React Native com código nativo, no entanto, requer o Android 9 (Pie)SDK em particular. SDKs adicionais do Android podem ser instalados através do SDK Manager no Android Studio.

O SDK Manager pode ser acessado na tela “Bem-vindo ao Android Studio”. Clique em “Configurar” e selecione “Gerenciador de SDK”.

O Gerenciador de SDK também pode ser encontrado na caixa de diálogo “Preferências” do Android Studio, em Aparência e comportamento → Configurações do sistema → SDK do Android .

Selecione a guia “Plataformas do SDK” no Gerenciador de SDK e marque a caixa ao lado de “Mostrar detalhes do pacote” no canto inferior direito. Procure e expanda a Android 9 (Pie)entrada e verifique se os seguintes itens estão marcados:

Android SDK Platform 28
Intel x86 Atom_64 System Image ou Google APIs Intel x86 Atom System Image
Em seguida, selecione a guia “Ferramentas do SDK” e marque a caixa ao lado de “Mostrar detalhes do pacote” aqui também. Procure e expanda a entrada “Android SDK Build-Tools” e verifique se 28.0.3está selecionada.

Por fim, clique em “Aplicar” para baixar e instalar o Android SDK e ferramentas de criação relacionadas.

1. Configure a variável de ambiente ANDROID_HOME As ferramentas React Native exigem que algumas variáveis de ambiente sejam configuradas para criar aplicativos com código nativo.

Abra o painel de Sistema em Sistema e Segurança no Painel de Controle do Windows, em seguida, clique em Alterar configurações … . Abra o avançado guia e clique em Variáveis de ambiente … . Clique em Novo … para criar uma nova ANDROID_HOMEvariável de usuário que aponte para o caminho para o seu Android SDK:

O SDK é instalado, por padrão, no seguinte local:

c:\Users\YOUR_USERNAME\AppData\Local\Android\Sdk
Você pode encontrar a localização real do SDK na caixa de diálogo “Preferências” do Android Studio, em Aparência e comportamento → Configurações do sistema → SDK do Android .

Abra uma nova janela do Prompt de Comando para garantir que a nova variável de ambiente seja carregada antes de prosseguir para a próxima etapa.

1. Adicione ferramentas de plataforma ao Path Abra o painel de Sistema em Sistema e Segurança no Painel de Controle do Windows, em seguida, clique em Alterar configurações … . Abra o avançado guia e clique em Variáveis de ambiente … . Selecione a variável Path e clique em Edit . Clique em Novo e adicione o caminho às ferramentas de plataforma na lista.

O local padrão para esta pasta é:

c:\Users\YOUR_USERNAME\AppData\Local\Android\Sdk\platform-tools
Criando um novo aplicativo
Use a interface da linha de comandos do React Native para gerar um novo projeto do React Native chamado “AwesomeProject”:

```
react-native init AwesomeProject
```



Isso não é necessário se você estiver integrando o React Native em um aplicativo existente, se “ejetado” do Create React Native App ou se estiver adicionando suporte Android a um projeto existente do React Native (consulte o Código específico da plataforma ). Você também pode usar uma CLI de terceiros para iniciar seu aplicativo React Native, como Ignite CLI .

[Opcional] Usando uma versão específica
Se você deseja iniciar um novo projeto com uma versão específica do React Native, use o --versionargumento:

```
react-native init AwesomeProject --version X.XX.X
react-native init AwesomeProject --version react-native@next
```



### Preparando o dispositivo Android

Você precisará de um dispositivo Android para executar seu aplicativo React Native Android. Pode ser um dispositivo Android físico ou, mais comumente, você pode usar um Dispositivo Virtual Android que permite emular um dispositivo Android no seu computador.

De qualquer forma, você precisará preparar o dispositivo para executar aplicativos Android para desenvolvimento.

### Usando um dispositivo físico

Se você possui um dispositivo Android físico, pode usá-lo para desenvolvimento no lugar de um AVD conectando-o ao computador usando um cabo USB e seguindo as instruções aqui .

### Usando um dispositivo virtual

Se você usar o Android Studio para abrir ./AwesomeProject/android, poderá ver a lista de dispositivos virtuais Android (AVDs) disponíveis, abrindo o “AVD Manager” no Android Studio. Procure um ícone parecido com este:

### Gerenciador Android AVD Studio

Se você acabou de instalar o Android Studio, provavelmente precisará criar um novo AVD . Selecione “Criar dispositivo virtual …”, escolha qualquer telefone da lista e clique em “Avançar” e selecione a imagem Nível 28 da API de torta .

Se você não possui o HAXM instalado, clique em “Instalar HAXM” ou siga estas instruções para configurá-lo e volte ao Gerenciador do AVD.

Clique em “Avançar” e depois em “Concluir” para criar seu AVD. Nesse ponto, você deve poder clicar no botão triângulo verde ao lado do seu AVD para iniciá-lo e prosseguir para a próxima etapa.

Executando seu aplicativo React Native
Execute react-native run-android dentro da pasta do projeto React Native:

```
cd AwesomeProject
react-native run-android
```



Se tudo estiver configurado corretamente, você verá o novo aplicativo em execução no emulador do Android em breve.

react-native run-android é apenas uma maneira de executar seu aplicativo – você também pode executá-lo diretamente no Android Studio.

Se você não conseguir fazer isso funcionar, consulte a página Solução de problemas .

Modificando seu aplicativo
Agora que você executou o aplicativo com sucesso, vamos modificá-lo.

Abra App.js no seu editor de texto de sua escolha e edite algumas linhas.
Pressione a R tecla duas vezes ou selecione Reloadno menu Desenvolvedor ( Ctrl + M) para ver suas alterações!

### É isso aí!

Parabéns! Você executou e modificou com êxito seu primeiro aplicativo React Native.
[![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--SOknn73L--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/dqnclkc62es66h4ysto7.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--SOknn73L--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/dqnclkc62es66h4ysto7.png)

### O que agora?

Ative o Live Reload no menu do desenvolvedor. Seu aplicativo será recarregado automaticamente sempre que você salvar as alterações!
Se você deseja adicionar esse novo código do React Native a um aplicativo existente, consulte o Guia de integração .