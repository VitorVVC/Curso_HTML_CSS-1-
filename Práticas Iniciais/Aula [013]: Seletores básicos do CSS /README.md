## Aula [013]

### Seletores básicos do CSS

- Oque foi visto?
  * Neste repositório o qual armazeno minha décima terceira aula de HTML & CSS estamos vendo seletores básicos do CSS.
  * Veremos como selecionar atributos através de classes, ID's, Tags genericas, Tudo que houver no documento HTML, Como especificamos no CSS oque há no HTML com tags pais, filhas e irmãos.

- `Primeira parte da aula`
  * Neste momento introdutório vimos como selecionarmos estilos especificos para classes, os quais utilizamos: `.classe-qualquer`.
  * Vimos também como especificarmos qual elemento queremos estilizar, por exemplo: `.classe-qualquer .h1`. No código mostrado nos estamos especificando que queremos estilizar o H1 de uma classe qualquer.. Poderia ser feito também atribuindo ao H1 uma classe, por exemplo: `.classe-qualquer .heading`. Desta forma nós atribuimos ao antigo H1 uma classe heading, que poderá ser reaproveitada em seus estilos para outros cabecalhos similares e muitas outras possibilidades.
  * `Herança`: Neste tópico entendemos que caso exista uma tag pai e dentro desta tag tenha outra tag, esta "outra tag" é chamada de filha, e caso optemos por não definir nada a ela, ela recebera atributos do pai.
  * Como por exemplo:
  ```html
    <head>
        <style>
            .pai {
                color: red;
            }
        </style>
    </head>

    <body>
        <div class="pai">Pai
            <div class="filha">Filha</div>
        </div>
    </body>
  ```
  * No exemplo acima, a div filha só existe dentro da div pai. E como estilizamos a div pai a filha acaba "herdando" tais atributos.
  * Uma forma de contornar isso seria
  ```html
    <style>
        div {
        color: initial;
        margin-left: 20px;
        }
    </style>
  ```
  * Desta forma nós dizemos que *TODA* div terá sua cor inicial, se não for informado qual a cor da div por meio de outros método ela terá a cor padrão do sistema.
  
-`Como estilizar um elemento ESPECIFICO que esteja dentro de um "pai"?`
  * A resposta para este questionamento é simples, vamos supor este código:
```html
    <head>
        <style>
            .pai {
                color: red;
            }
        </style>
    </head>

    <body>
        <div class="pai">Pai
            <div class="filha">Filha
                <div class = "filha-da-filha">Filha da filha</div>
            </div>
        </div>
    </body>
```
  * Neste caso, como podemos estilizar apenas a filha?
  * Resposta:
  ```html
  <style>
    .pai>.filha {
    /* Child Selector */
    color: blue;
    }
  </style>
  ```
  * O nome deste método é "Child Selector", por mais explicativo que o nome seja, em resumo selecionamos apenas a class filha que houver dentro de outra classe pai. Caso desejassemos mais especificade e consequentemente estilizar-mos a filha da filha, basta fazer isto:
  ```html
  <style>
    .pai>.filha>.filha-da-filha {
    /* Child Selector */
    color: darkblue;
    }
  </style>
  ```
  <hr>

- `Segunda parte da aula`