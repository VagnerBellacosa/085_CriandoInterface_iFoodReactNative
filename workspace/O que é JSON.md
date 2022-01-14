
Artigo[Invista em você! Saiba como a DevMedia pode ajudar sua carreira.](https://www.devmedia.com.br/o-que-e-json/23166#modulo-mvp)

# O que é JSON

## Veja neste artigo sobre JSON onde começaremos pelo básico sobre e avançaremos para exemplos mais complexos nos próximos artigos.

- SUPORTE AO ALUNO
- ANOTAÇÕES
- FAVORITAR
- CONCLUÍDO
- **53**GOSTEI
- 

- **53**
- 
- 

Suporte ao alunoAnotarMarcar como concluído

[Artigos](https://www.devmedia.com.br/artigos/)[Java](https://www.devmedia.com.br/artigos/java)O que é JSON

### Afinal, o que é JSON?

JSON é basicamente um formato leve de troca de informações/dados entre sistemas. Mas **JSON significa JavaScript Object Notation**, ou seja, só posso usar com JavaScript correto? Na verdade não e alguns ainda caem nesta armadilha.

O JSON além de ser um formato leve para troca de dados é também muito simples de ler. Mas quando dizemos que algo é simples, é interessante compará-lo com algo mais complexo para entendermos tal simplicidade não é? Neste caso podemos comparar o JSON com o [formato XML](https://www.devmedia.com.br/xml-tutorial/24936).

Veja esse [Tutorial completo sobre JSON](http://www.devmedia.com.br/introducao-ao-formato-json/25275)

#### Vamos visualizar esta diferença?

##### XML

```
<note>
<to>Tove</to>
<from>Jani</from>
<heading>Reminder</heading>
<body>Don't forget me this weekend!</body>
</note>
```

##### JSON

```
{
   "id":1,
   "nome":"Alexandre Gama",
   "endereco":"R. Qualquer"
}
```

Bom, é notável a diferença. Visualmente o segundo trecho (em JSON) é mais fácil de ler. Mas só existe essa diferença entre os dois? Na verdade não. Podemos listar algumas outras vantagens:

### Vantagens do JSON:

- Leitura mais simples
- Analisador(parsing) mais fácil
- JSON suporta objetos! Sim, ele é tipado!
- Velocidade maior na execução e transporte de dados
- Arquivo com tamanho reduzido
- Quem utiliza? Google, Facebook, Yahoo!, Twitter...

Estas são algumas das vantagens apresentadas pelo JSON. Agora vamos ao que interessa: Código! Vamos fazer um exemplo extremamente simples nesta primeira parte e avançaremos no próximo artigo, inclusive falando sobre JSON em páginas Web.

Qual biblioteca usar?
Existem diversas bibliotecas para trabalharmos com [JSON](https://www.devmedia.com.br/json-tutorial/25275) e [Java](https://www.devmedia.com.br/guias/java). Usaremos no nosso estudo o json.jar que você pode baixar tranquilamente neste link.

O nosso caso de estudo será simples: Teremos uma classe Carro que será a nossa classe [POJO](https://pt.wikipedia.org/wiki/Plain_Old_Java_Objects) e a classe EstudoJSON que terá o nosso famoso método main.

Classe Carro.

```
package br.com.json;

public class Carro {
    private Long id;
    private String modelo;
    private String placa;

    public Long getId() {
        return id;
    }
    public void setId(Long id) {
        this.id = id;
    }
    public String getModelo() {
        return modelo;
    }
    public void setModelo(String modelo) {
        this.modelo = modelo;
    }
    public String getPlaca() {
        return placa;
    }
    public void setPlaca(String placa) {
        this.placa = placa;
    }

        //Aqui fizemos o Override do método toString() para visualizar a impressão com o System.out.println()
    @Override
    public String toString() {
        return "[id=" + id + ", modelo=" + modelo + ", placa=" + placa
                + "]";
    }

}
```

Esta é uma classe simples, onde temos os atributos Id, Modelo e Placa. Agora teremos a classe EstudoJSON.

```
package br.com.json;

import org.json.JSONArray;
import org.json.JSONException;
import org.json.JSONObject;

public class EstudoJSON {
    public static void main(String[] args) throws JSONException {
        adicaoSimplesDeDados();
    }
}
```

Repare que criamos o método adicaoSimplesDeDados() que conterá o código de exemplo:

```
private static void adicaoSimplesDeDados() throws JSONException {
    //Criação do objeto carro e atribuição dos valores
    Carro carro = new Carro();
    carro.setId(1l);
    carro.setModelo("Celta");
    carro.setPlaca("AAA1234");

    //Criação do objeto carroJson
    JSONObject carroJson = new JSONObject();
    //Inserção dos valores do carro no objeto JSON
    carroJson.put("id", carro.getId());
    carroJson.put("Modelo", carro.getModelo());
    carroJson.put("Placa", carro.getPlaca());

    //Impressão do objeto JSON
    System.out.println(carroJson);
}
```

Se executarmos este código, veremos que foi impresso no console o seguinte:

```
{"id":1,"Modelo":"Celta","Placa":"AAA1234"}
```

Você desenvolvedor mais atento vai reparar que existe um objeto impresso: Um Long! Isso mesmo! Como vimos, o JSON consegue armazenar objetos! Podemos inclusive armazenar um objeto do tipo Carro mesmo:

Modificamos o nosso método main:

```
public class EstudoJSON {
    public static void main(String[] args) throws JSONException {
        adicaoSimplesDeDados();

        adicaoDeUmObjeto();
    }
}
```

E adicionamos o método adicaoDeUmObjeto():

```
private static void adicaoDeUmObjeto() throws JSONException {
    Carro carro = new Carro();
    carro.setId(1l);
    carro.setModelo("Celta");
    carro.setPlaca("AAA1234");

    JSONObject carroJson = new JSONObject();
    //Adição do objeto carro
    carroJson.put("Carro", carro);

    System.out.println(carroJson);
}
```

Neste caso foi impresso no console o seguinte:

```
{"Carro":"[id=1, modelo=Celta, placa=AAA1234]"}
```

Simples não? Como o JSON trabalha com coleção de pares nome/valor, podemos imprimir um valor específico simplesmente chamando o nome que desejamos.

```
System.out.println(carroJson.get("Modelo"));
```

Veja que neste caso queremos somente o modelo do carro, bastando fazer a chamada get("nome que desejamos")!

##### Conclusão

É isso pessoal! Vimos as vantagens do JSON e vimos como é simples começar a trabalhar com ele. Nos próximos artigos veremos exemplos mais complexos e veremos algo mais real onde faremos chamadas à API do Facebook!

#### Links Úteis

- [Laravel e Passport: Criando APIs com autenticação](http://www.devmedia.com.br/curso/laravel-e-passport-criando-apis-com-autenticacao/2026):
  Neste curso aprenderemos a implementar o recurso de autenticação via tokens usando OAuth em um web service RESTful construído com o framework Laravel.
- [Spring MVC: Como criar sua primeira aplicação web](http://www.devmedia.com.br/curso/spring-mvc-como-criar-sua-primeira-aplicacao-web/2024):
  Neste curso você aprenderá a criar a sua primeira aplicação web utilizando o Spring MVC.
- [JPA: Como usar a anotação @GeneratedValue](http://www.devmedia.com.br/jpa-como-usar-a-anotacao-generatedvalue/38592):
  Nesta documentação você aprenderá a utilizar a anotação @GeneratedValue, a qual deve ser declarada quando a geração do valor da chave-primária é de responsabilidade do banco de dados.

#### Saiba mais sobre JSON ;)

- [Como manipular dados em JSON no .NET](http://www.devmedia.com.br/curso/como-manipular-dados-em-json-no-net/1905):
  O formato JSON é atualmente um dos mais utilizados na representação, armazenamento e tráfego de dados entre aplicações, principalmente web services.
- [Jackson 2: Convertendo Java para JSON](http://www.devmedia.com.br/jackson-2-convertendo-java-para-json/34295):
  Nesse vídeo você verá como fazer uso da API do Jackson 2 para converter conteúdo JSON para objetos Java e vice-versa.

Tecnologias:

- [Java](https://www.devmedia.com.br/java/)

AnotarMarcar como concluído