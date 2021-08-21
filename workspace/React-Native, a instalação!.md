# React-Native, a instalação!

Finalmente vamos começar com uma parte mais prática sobre o React-Native. Caso você não saiba do que estamos falando, você pode se guiar pelo índice abaixo. Vamos nessa!

### Índice

- [O que é React-Native?](https://www.koder.com.br/blog/o-que-e-react-native/)
- [**React-Native, a instalação!**](http://www.koder.com.br/blog/react-native-a-instalacao/) ***(Você está aqui)\***
- Construindo seu primeiro aplicativo com React-Native ***(Em produção…)\***

### Hora da prática

![img](https://cdn-images-1.medium.com/max/800/1*nJf_IxeKGy608Nwt0rhDkg.gif)

Antes de começarmos a falar de comandos, você precisa saber sobre o ambiente que estou usando, afinal esse tutorial é baseado nele. Então estaremos considerando aqui que você está utilizando uma distribuição baseada em[ *Debian*](https://www.debian.org/) *(ou o próprio)*. No meu caso é uma instalação limpa do [*Xubuntu 18.04.*](https://xubuntu.org/release/18-04/)

Vamos desenvolver um aplicativo para [*Android*](https://www.android.com/), mas caso você tenha um *MacOS* disponível, possuindo o [Xcode](https://developer.apple.com/xcode/) e o [*React-Native*](https://facebook.github.io/react-native/) instalados, você poderá executar também para [*IOS*](https://www.apple.com/br/ios/ios-12/?&mnid=si2dXXXt0-dc_mtid_209258i342853_pcrid_296229365656_&cid=wwa-br-kwgo-iphone-slid-&mtid=209258i342853&aosid=p238&anonymizeip=set) sem problemas, mas lembre-se que o foco ainda é o *Android*.

Numa distribuição [*Linux*](https://www.linux.org/) podemos instalar programas de várias formas, vou sempre escolher aquilo que for mais fácil para cada caso, assim você instala as coisas facilmente e eu consigo um texto mais didático, fechado?

### Instalando o Android Studio

Ainda que futuramente você escolha não utilizar o [*Android Studio*](https://developer.android.com/studio) para testar seu aplicativo, fazendo uso do seu próprio *smartphone* conectado a um cabo *usb*, você necessitará instalá-lo. Não há meio mais simples de efetuar *download* dos *SDKs do Android*, que é uma dependência para o *React-Native*. Além disso você possui a vantagem de ter vários dispositivos para testar, **de relógios à \*TVs\***.

**Vamos pelo meio mais simples?** Acesse seu terminal e digite o comando:

```
sudo snap install android-studio --classic
```

Distribuições como o [Ubuntu](https://www.ubuntu.com/) e [Fedora](https://getfedora.org/), contém o gerenciador de pacotes [*Snap*](https://snapcraft.io/) pré-instalado. Mas não posso alongar o texto quanto a isso, pois foge completamente do assunto. Apenas saiba que ele é seguro e que muitas empresas como *Google*, *Spotify* e *Microsoft* o apoiam.

Agora você pode encontrar o *Android Studio* nos seus aplicativos, é só procurar na barra de pesquisa do seu sistema. Ao abrir o *Android-Studio* você verá a seguinte tela:

![img](https://cdn-images-1.medium.com/max/800/1*5iokVFW2TUZKLQpJlTJ_Vg.png)

Nesse ponto basta clicar em *“next”*, você verá algo parecido com a seguinte imagem:

![img](https://cdn-images-1.medium.com/max/800/1*iZOF1xTmNvM_Pv4PJQof0w.png)

Aqui você pode selecionar a opção *“standard”* ou *“padrão”* dependendo do seu pacote de tradução. Lembrando que estou considerando uma instalação limpa. A próxima tela é para simplesmente escolher o tema que você deseja para seu *Android Studio*, selecione qualquer opção e prossiga até encontrar a seguinte tela:

![img](https://cdn-images-1.medium.com/max/800/1*U4PX3ix2tRdHnLxpnRaIZw.png)

Acima você pode ver uma lista de coisas que o *Android Studio* vai instalar para você conseguir utilizá-lo. Uma hora podemos ver isso detalhadamente, mas não nesse tutorial, no momento escolha a opção *“next”*.

Você verá uma nova janela com a opção *“finish”* e algumas instruções sobre um tal de [*kvm*](https://www.linux-kvm.org/page/Main_Page), que vamos detalhar mais a frente nesse tutorial, a princípio clique em *“finish”*. Agora, vá buscar um café. Sério mesmo, na boa, **vai demorar.**

E aí? Acabou? Ah ok… então na próxima tela pode clicar em *“finish”* novamente. As informações que você está visualizando são apenas uma descrição do que foi instalado. Agora você deve ter visto isso:

![img](https://cdn-images-1.medium.com/max/800/1*ENABRf_8WNuzk0DySJt--w.png)

É só clicar em *“Start a new Android Studio project”.* Dessa forma você verá essas opções de inicialização de projeto:

![img](https://cdn-images-1.medium.com/max/800/1*BtEV6nuEt8168PnFZdITfg.png)

Caso você fosse construir um aplicativo diretamente com *Android Studio*, de forma nativa, essas opções seriam úteis, mas como só queremos explorar algumas ferramentas do editor, você pode clicar em *next* com a opção *“add no activity”* selecionada.

![img](https://cdn-images-1.medium.com/max/800/1*mxRnPq9mcA8wRD7eqEvaRQ.png)

A imagem acima corresponde ao que está em seu monitor, escolha qualquer nome de aplicação e clique em *“finish”*.

![img](https://cdn-images-1.medium.com/max/1200/1*EE5VJWobuIbQUHQJaIHcpg.png)

E aqui estamos! Com o *Android Studio* funcional. Agora você precisa gerar um emulador de um *smatphone* usando o *Android Studio*. Para isso, basta clicar na opção *AVD Manager*, em destaque na imagem acima. Isso deve abrir a seguinte tela:

![img](https://cdn-images-1.medium.com/max/1200/1*G9GLWcUq_AypmrKnULeFfA.png)

Ai você já sabe né? Clique em *“Create virtual device”*. E então você verá isso:

![img](https://cdn-images-1.medium.com/max/1200/1*JehsOTwrgvNERdt7ksjB1w.png)

Essa é a hora de você escolher um **modelo de smartphone** para rodar a sua **emulação do \*Android\***, tem várias opções bacanas, escolha uma a seu gosto e prossiga. Eu vou ficar com o ***Pixel 2\*** mesmo. Após escolher e clicar em cima da opção desejada, pressione *“next”.* Agora vai abrir uma janela conforme abaixo:

![img](https://cdn-images-1.medium.com/max/1200/1*HJncszfT2IG_XCwcx8uyZQ.png)

Você precisa efetuar o *download* de uma **máquina virtual**, eu escolhi a primeira opção, que contém o ***Android 9+\***. Escolha a versão que você deseja e clique em *“Download”*, **além de buscar mais um café**. *Sim, vai demorar*. Ah! Vai abrir uma tela logo depois desta, que você vai precisar clicar respectivamente em *“accept”* e *“next”*. **Agora sim, o café.**

Logo após o *download* ser concluído, você deve clicar em “*finish”* e em seguida vai retornar para essa tela:

![img](https://cdn-images-1.medium.com/max/800/1*JhquJRJ0BC6pOGrq597Z4Q.png)

Agora você pode usar essa imagem de sistema selecionando-a como no exemplo da imagem acima, clicando novamente em *“next”* em seguida. Chegou a hora de configurar sua virtualização do *Android,* você deve estar vendo algo parecido com a imagem abaixo:

![img](https://cdn-images-1.medium.com/max/800/1*fEVWqZ4-K13Wbdgd2JnffQ.png)

Você pode dar um nome qualquer para sua emulação. Eu aconselho você dar um clique na opção *“show advanced settings”* e selecionar a opção *“cold boot”*. Sempre que você iniciar seu emulador, você terá o *“boot”* do *Android* iniciado ao invés de congelar o estado de onde parou na última vez. Mas calma! Suas informações ainda estarão salvas lá.

Pela minha experiência, usar o *“cold boot”* se tornou a melhor opção. Caso não esteja nesse modo e haja um travamento na sua aplicação, ao reiniciar, o emulador vai voltar ao estágio onde ocorreu o travamento, se tornando trabalhoso torná-lo operável novamente. No caso do *“cold boot”* ele sempre reiniciará o *Android* por completo, como é o uso comum.

Agora clique em “*finish”* e veremos essa tela:

![img](https://cdn-images-1.medium.com/max/1200/1*CgL0YkmIbSO2kI31jDxxkg.png)

**Pronto! É só usar? Não. Não é…** Lembra que falei que iriamos falar sobre o *KVM*? Chegou a hora. **O \*KVM\* é uma solução de virtualização** para sistemas operacionais baseados em ***Linux\***. *C*om ele você pode gerar vários tipos de máquinas virtuais. O *Android Studio* quando instalado em um ambiente *Linux* faz uso dessa ferramenta.

Você deve ter percebido que em algumas imagens desse tutorial, aparece um erro em vermelho dizendo ***“/dev/kvm device: permission denied”.\*** Isso se deve ao fato de que, só o *superusuário (sudo, root)* do sistema tem acesso a criar máquinas virtuais, ou simplesmente, você ainda nem tem instalado a solução do *KVM.*

Se você não tiver o *KVM* instalado*,* como é o caso dessa instalação limpa que estou utilizando, execute o seguinte comando:

```
sudo apt install qemu-kvm
```

Simples né? Agora você precisa inserir o seu usuário no grupo do *KVM.* Permissões, grupos e usuários em distribuições *Linux* são deveras importantes, sugiro que você dê uma olhada mais profundamente para compreender o assunto caso não o conheça. Por hora, siga dessa forma:

```
sudo adduser seu-usuario kvm
```

Para finalizarmos essa parte, execute este último comando:

```
sudo chown seu-usuario /dev/kvm
```

**Pronto!** Agora você pode rodar sua máquina virtual, ele abrirá o modelo do *smartphone* que você escolheu com a versão do *Android* que você baixou, mais ou menos assim:

![img](https://cdn-images-1.medium.com/max/1200/1*WDN5-rXaGrkGobRvhNAqEg.png)

Agora, depois de todo esse sofrimento e espera, **é que de fato vamos passar a instalar o \*React-Native.\***

![img](https://cdn-images-1.medium.com/max/800/1*UPqmcUGbtSvPi0ewZs-U6w.gif)

### Instalando o React-Native

O *React-Native* é instalado via gerenciador de pacotes [*NPM*](https://www.npmjs.com/)*.* Isso significa que você irá precisar instalar tanto o [*NodeJ*S](https://nodejs.org/en/) quanto o próprio *NPM (Sim, na família Debian de distribuições o NPM é instalado a parte).*

Para você instalar o *NodeJ*S e o *NPM*, é só utilizar o comando abaixo:

```
sudo apt install nodejs && sudo apt install npm
```

Agora realmente, vamos instalar o *React-Native:*

```
sudo npm install -g react-native-cli
```

O nosso amigo *React-Native,* precisa de sua ajuda para encontrar os *SDKs* que instalamos via *Android Studio,* podemos torná-lo acessível alterando o arquivo *“.bashrc”* que se encontra normalmente, na sua *home (“/home/seu-usuario”)*.

Você pode pressionar *“ctrl+h”* para ver os arquivos ocultos e abri-lo com seu editor favorito, ou acessá-lo via terminal usando editores como *nano* e *vi*. **Não importa como você vai fazer isso**, desde que coloque as seguintes linhas no final do arquivo ***“.bashrc”\***:

```
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

Agora você pode criar o seu projeto *React-Native* com esse comando, no diretório em que tiver preferência, via terminal:

```
react-native init NomeDoSeuProjeto
```

Esse comando que executamos gerou um diretório “NomeDoSeuProjeto”, entre nele.

Você precisará saber qual é o número da *API* da versão do *Android* utilizada no emulador. É simples, lembra que você escolheu uma versão do *Android* para emular certo? Duas imagens acima *(descrição da imagem: “Emulador: Versão do Android escolhido para emulação”)*, caso você não lembre, na coluna *“Target”* estará descrito o nome da versão do *Android* escolhida. Você pode consultar [*nesse link*,](https://developer.android.com/studio/releases/platforms) o número que representa essa versão, no meu caso, escolhi o ***Android 9+\*** e o número da minha versão é ***28\***.

Considerando que você está no ***diretório raiz\*** *(não no nutella, no raiz mesmo)* de seu projeto, ponha o número da versão *(28 no meu caso)* no arquivo que se encontra em *“android/build.gradle”*, nas linhas *“compileSdkVersion”* e *“targetSdkVersion”,* caso já não esteja o número correto.

```
buildscript {
    ext {
        buildToolsVersion = "28.0.3"
        minSdkVersion = 16
        compileSdkVersion = 28
        targetSdkVersion = 28
        supportLibVersion = "28.0.0"
    }
    repositories {
        google()
        jcenter()
    }
...
```

Agora é a parte da alegria. Abra seu *Android-Studio,* clique novamente em *avd-manager* conforme já fizemos no tópico de instalação do *Android-Studio,* e abra seu emulador gerado. **Com o emulador rodando,** dentro da pasta do seu projeto, execute a seguinte instrução via terminal:

```
react-native run-android
```

Após esse comando finalizar, no seu emulador aparecerá o seu aplicativo *Android* rodando com uma tela de boas vindas do *React-Native.* Parecido com essa imagem:

![img](https://cdn-images-1.medium.com/max/800/1*B7auwQQMD1C446eb1RYkug.png)

### Acabou!

![img](http://www.koder.com.br/wp-content/uploads/2019/06/starkexpo.gif)

**Parabéns!** O *React-Native* está instalado e devidamente operável. Agora podemos investir na parte legal de um tutorial prático, **ver seu \*app\* funcionar**. **Quer ver mais?** A terceira parte logo sai, fazer um material desses não é tão rápido assim, então fique de olho ![😉](https://s.w.org/images/core/emoji/13.0.0/svg/1f609.svg)

- [Sem categoria](https://www.koder.com.br/blog/?categoria=sem-categoria)