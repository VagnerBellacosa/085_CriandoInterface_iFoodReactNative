[Henrique Weiand](https://medium.com/@henrique.weiand?source=post_page-----27e650db4238-----------------------------------)

Aug 6, 2019· - 3 min read



![img](https://miro.medium.com/max/1400/1*OVxQLX_4Zr78m9YRW-FLqg.jpeg)

# React-Native — Navegando entre telas com react-navigation

Vamos falar sobre navegação entre telas? Siim!!

Um recurso mais do que básico em qualquer aplicação é a possibilidade de navegar entre diversas telas e ir interagindo, certo? Com isso surgiram varias maneira no React-Native para isso, porem uma lib de maior destaque já há algum tempo é a react-navigation

[React Navigation · Routing and navigation for your React Native appsRouting and navigation for your React Native appsRouting and navigation for your React Native appsreactnavigation.org](https://reactnavigation.org/en/)

Vou então aplicar então uma paginação simples para que vocês consigam ver como é fácil mexer nela.

Vamos primeiramente iniciar um projeto com o comando

```
react-native init exemploNavegacao
```

Como você já deve saber esse comando demora um pouco, então aguarde

![img](https://miro.medium.com/max/1400/1*wqlV8Qih-nyTQR1wqofzng.gif)

Feito isso, entre na pasta do projeto conforme o nome que você colocou e vamos logo de largada instalar algumas libs com os seguintes comandos

```
npm install --save react-navigation react-native-gesture-handler react-native-reanimated
```

Três libs para que as coisas funcionem bem por aqui, ok?

Esse passo também pode demorar um pouco…

Ao finalizar as instalações, estando ainda dentro do diretório do projeto no terminal execute

```
react-native link
```

Para fazer a mágica acontecer com as libs nativas e o react-native

## Para IOS

Se seu caso é ios, logo após os passos anteriores acesse a pasta ios com `cd /ios` e la dentro rode outro comando

```
pod install
```

Caso tenha algum problema, sugiro seguir os passos da página oficial

[Getting started · React NavigationReact Navigation is born from the React Native community's need for an extensible yet easy-to-use navigation solution…reactnavigation.org](https://reactnavigation.org/docs/en/getting-started.html)

## Para Android

Utilizando o comando link do react-native as conexões entre as libs já devem estar prontas ;) caso não funcione posteriormente algo, verifique também na [documentação oficial.](https://reactnavigation.org/docs/en/getting-started.html)

Feito os primeiros passos, vamos finalmente executar nosso projeto com `react-native run-ios` ou `react-native run-android` dependendo da sua plataforma. Aguarde que pode levar alguns minutos também!

![img](https://miro.medium.com/max/704/1*5kq0jWQFOHd2WZwQGSVYbw.png)

Projeto rodando! Ok? todos chegaram até aqui?

Vou continuar o esquema default de pastas e arquivos do React-native, apenas neste `App.js` vou praticamente zera-lo, deixando assim

<iframe src="https://medium.com/media/57bbc5a17353e0386d10349db2a128e0" allowfullscreen="" frameborder="0" height="370" width="692" title="" class="eg aq as ag dq" scrolling="auto" style="box-sizing: inherit; height: 369.983px; top: 0px; left: 0px; width: 691.997px; position: absolute;"></iframe>

Chegando neste resultado

![img](https://miro.medium.com/max/696/1*Fgx_LLlKjvehDn05DaZu2g.png)

Lembra que nossos install do navigation já estão todos prontos? Então vamos apenas configurar. Para isso crie um arquivo chamado `Routes.js` pode ser na root mesmo das pastas junto com `App.js` ele vai possuir o seguinte conteúdo

<iframe src="https://medium.com/media/a951b45b2d0fcf233a922d997888b21f" allowfullscreen="" frameborder="0" height="348" width="692" title="" class="eg aq as ag dq" scrolling="auto" style="box-sizing: inherit; height: 347.986px; top: 0px; left: 0px; width: 691.997px; position: absolute;"></iframe>

Vamos editar tbm o script `index.js` colocando o seguinte conteúdo

<iframe src="https://medium.com/media/b7031f596d8e442159d764af80f12951" allowfullscreen="" frameborder="0" height="150" width="692" title="" class="eg aq as ag dq" scrolling="auto" style="box-sizing: inherit; height: 149.983px; top: 0px; left: 0px; width: 691.997px; position: absolute;"></iframe>

Vamos criar um outro script chamado `Sobre.js` com o conteúdo

<iframe src="https://medium.com/media/81a76cbe6ff2e522cec294f9dabd127f" allowfullscreen="" frameborder="0" height="370" width="692" title="" class="eg aq as ag dq" scrolling="auto" style="box-sizing: inherit; height: 369.983px; top: 0px; left: 0px; width: 691.997px; position: absolute;"></iframe>

E uma última alteração em nosso `App.js`

<iframe src="https://medium.com/media/c6ec7e2083e4db0bf8f6a53f7c390c07" allowfullscreen="" frameborder="0" height="413" width="692" title="" class="eg aq as ag dq" scrolling="auto" style="box-sizing: inherit; height: 412.986px; top: 0px; left: 0px; width: 691.997px; position: absolute;"></iframe>

E pronto! tudo esta configurado, vamos ver o resultado

![img](https://miro.medium.com/max/704/1*a_GYV8jP_KG4usa1_5C0oA.gif)

Então é isso pessoal! Para quem ficou com dúvidas em como ficou o esquema de pastas e scripts o resultado é esse

![img](https://miro.medium.com/max/374/1*dmeWUzTvPg2P-TQevD38nQ.png)

41

1











## [More from Datainfo](https://medium.com/datainfo?source=post_page-----27e650db4238-----------------------------------)

Follow

Datainfo não só uma empresa de desenvolvimento de software mas também de conteúdos tecnicos na área

![Jader Fuck](https://miro.medium.com/fit/c/22/22/0*aqxE6HIaYtvFDJTe.)[Jader Fuck](https://medium.com/@jaderfck?source=post_page-----27e650db4238----0-------------------------------)[·Aug 2, 2019](https://medium.com/datainfo/react-native-ciclo-de-vida-ad5f1a9945be?source=post_page-----27e650db4238----0-------------------------------)[React Native — Ciclo de vidaHey Dev! Na aula de hoje, complementando o Assunto de componentes Stateful vs Stateless, vamos aprender sobre o ciclo de vida e como utilizarmos ele a nosso favor. E para entendermos melhor, já vamos começar com um exercício, e pra variar, ainda derivado da nossa saudosa aula1. Go on! Inicialmente…](https://medium.com/datainfo/react-native-ciclo-de-vida-ad5f1a9945be?source=post_page-----27e650db4238----0-------------------------------)[4 min read](https://medium.com/datainfo/react-native-ciclo-de-vida-ad5f1a9945be?source=post_page-----27e650db4238----0-------------------------------)[![React Native — Ciclo de vida](https://miro.medium.com/fit/c/101/101/1*VQyh78RnXt9zOL1WXJDJHg.png)](https://medium.com/datainfo/react-native-ciclo-de-vida-ad5f1a9945be?source=post_page-----27e650db4238----0-------------------------------)Share your ideas with millions of readers.[Write on Medium](https://medium.com/new-story?source=post_page_footer_cta_write----------------------------------------)![Jader Fuck](https://miro.medium.com/fit/c/22/22/0*aqxE6HIaYtvFDJTe.)[Jader Fuck](https://medium.com/@jaderfck?source=post_page-----27e650db4238----1-------------------------------)[·Aug 1, 2019](https://medium.com/datainfo/react-native-stateful-vs-stateless-941be877c8d8?source=post_page-----27e650db4238----1-------------------------------)[React Native — Stateful vs StatelessE aí dev! Já caminhamos muito, já aprendemos bastante coisa, e vamos aprender mais ainda! Hoje vamos falar sobre componentes Stateful e Stateless! Prosseguindo com o nosso projeto Aula1, temos dois componentes, o componente Botao e o “componente” App. Ambos os componentes são Stateful e já veremos o por quê:](https://medium.com/datainfo/react-native-stateful-vs-stateless-941be877c8d8?source=post_page-----27e650db4238----1-------------------------------)[2 min read](https://medium.com/datainfo/react-native-stateful-vs-stateless-941be877c8d8?source=post_page-----27e650db4238----1-------------------------------)![Henrique Weiand](https://miro.medium.com/fit/c/22/22/1*10oK1ckMFT4OSU3yaBXGmg.jpeg)[Henrique Weiand](https://medium.com/@henrique.weiand?source=post_page-----27e650db4238----2-------------------------------)[·Aug 1, 2019](https://medium.com/datainfo/react-native-packager-e-comandos-9c237271eafa?source=post_page-----27e650db4238----2-------------------------------)[React-Native: Packager e comandosEste post será mais rápido, vamos ver alguns comandos para iniciar de fato o projeto assim como o packager rodando. Para quem está com iOS Dentro da pasta do projeto criado, lembrando para criar um novo projeto você pode executar o comando react-native init NOME_DO_PROJETO logo após entre no projeto…](https://medium.com/datainfo/react-native-packager-e-comandos-9c237271eafa?source=post_page-----27e650db4238----2-------------------------------)[2 min read](https://medium.com/datainfo/react-native-packager-e-comandos-9c237271eafa?source=post_page-----27e650db4238----2-------------------------------)[![React-Native: Packager e comandos](https://miro.medium.com/fit/c/101/101/1*MBOMEJyHGTLwiUZpLRD5vA.png)](https://medium.com/datainfo/react-native-packager-e-comandos-9c237271eafa?source=post_page-----27e650db4238----2-------------------------------)![Henrique Weiand](https://miro.medium.com/fit/c/22/22/1*10oK1ckMFT4OSU3yaBXGmg.jpeg)[Henrique Weiand](https://medium.com/@henrique.weiand?source=post_page-----27e650db4238----3-------------------------------)[·Jul 31, 2019](https://medium.com/datainfo/react-native-arquitetura-e-comparações-1663f77e0a57?source=post_page-----27e650db4238----3-------------------------------)[React-Native — Arquitetura e comparaçõesUm player que vem se destacando cada vez mais no mercado o React não só no ambiente mobile mas para a web, leva alguns conceitos principalmente em reutilização de conhecimento e agilidade. O React-Native é um projeto disponibilizado pelo Facebook, que nos permite o build de nativo e não web…](https://medium.com/datainfo/react-native-arquitetura-e-comparações-1663f77e0a57?source=post_page-----27e650db4238----3-------------------------------)[React Native](https://medium.com/tag/react-native?source=post_page-----27e650db4238---------------react_native--------------------)[3 min read](https://medium.com/datainfo/react-native-arquitetura-e-comparações-1663f77e0a57?source=post_page-----27e650db4238----3-------------------------------)[![React-Native — Arquitetura e comparações](https://miro.medium.com/fit/c/101/101/1*TYSItoF9SLnlqpergPaAVA.png)](https://medium.com/datainfo/react-native-arquitetura-e-comparações-1663f77e0a57?source=post_page-----27e650db4238----3-------------------------------)![Jader Fuck](https://miro.medium.com/fit/c/22/22/0*aqxE6HIaYtvFDJTe.)[Jader Fuck](https://medium.com/@jaderfck?source=post_page-----27e650db4238----4-------------------------------)[·Jul 31, 2019](https://medium.com/datainfo/react-native-configurando-proptypes-8c230279a1ad?source=post_page-----27e650db4238----4-------------------------------)[React Native — Configurando propTypesE aí dev! E com essa aula, continuamos a nossa jornada a respeito das propriedades de componentes em React Native! Primeiro de tudo, para começar os PropTypes, vamos precisar instalar a lib prop-types , então vamos no nosso PowerShell e rodar o seguinte comando: npm install --save prop-types e agora…](https://medium.com/datainfo/react-native-configurando-proptypes-8c230279a1ad?source=post_page-----27e650db4238----4-------------------------------)[2 min read](https://medium.com/datainfo/react-native-configurando-proptypes-8c230279a1ad?source=post_page-----27e650db4238----4-------------------------------)[![React Native — Configurando propTypes](https://miro.medium.com/fit/c/101/101/1*n4hNGk8l25DUtGUYpknzMQ.png)](https://medium.com/datainfo/react-native-configurando-proptypes-8c230279a1ad?source=post_page-----27e650db4238----4-------------------------------)

[Read more from Datainfo](https://medium.com/datainfo?source=post_page-----27e650db4238-----------------------------------)