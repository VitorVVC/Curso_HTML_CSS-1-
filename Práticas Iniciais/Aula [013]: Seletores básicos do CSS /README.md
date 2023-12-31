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
  * Neste momento da aula vamos aprender como estilizars irmãos.
  * Mas afinal, oque são irmãos em HTML?
  ```html
    <div class="pai">
        <h1>Lorem</h1>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates, fuga!</p>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates, fuga!</p>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates, fuga!</p>
    </div>
  ```
  * No código acima `<h1>` e `<p>` são irmãos.Pois ambos derivam ( são filhos ) da div "pai".
  * Portanto para selecionarmos ambos no CSS é cabivel tao código:
  ```css
  .pai h1+p {
    /* Adjacent sibling selector */
    color: red;
    }
  ```
  * Chamamos este efeito de código de `Adjacento Sibling Selector`.
  * Que nada mais é que determinar efeitos e estilos para dois elementos filhos de um mesmo pai ( irmãos ), através de uma tag apenas.

- Aproveitarei para abordar também o `General Sibling Selector`
  * Nada mais é que "capturar" todos os elementos posteriores a um outro elemento, seja ele classes ou tags padrões, como neste exemplo:
```css
    .pai .um~.dois {
    color: red
    /* General sibling selector*/
    }
```

  * Ele selecionará todos os elementos da classe dois que vierem posteriormente aos elementos da classe um.
  * Um paralelo deste tipo de seletor seria este:
```css
    .pai .um+.dois {
    color: pink
    }   
```

  * Neste exemplo ele captura apenas o PRIMEIRO elemento da classe dois que vier seguido de um elemento da classe UM.

- Demonstração:
  ```html
       <div class="pai">
        <div class="dois">2</div>
        <div class="um">1</div>
        <div class="dois">2</div>
        <div class="dois">2</div>
        <div class="dois">2</div>
        <div class="um">1</div>
        <div class="dois">2</div>
        <div class="dois">2</div>
        <div class="dois">2</div>
     </div>
  ```
  * Caso use este código com ambos os seletores acima verá que apenas o dois seguido de um ficará em rosa enquanto os demais ficarão vermelho.

-`Terceira parte da aula`
  * Neste momento da aula veremos seletores de atributos.
  * Leve este código em consideração para outras explicações:
```html
   <input type="checkbox" checked>
    <input type="checkbox">
    <!-- <h1 class="heading" meu-atributo="valor1 valor2 valor3">Lorem</h1> -->
    <h1 class="heading" meu-atributo="comecou">Lorem</h1>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
    <h1 class="heading">Lorem</h1>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
    <p class="p">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga quis eaque doloremque modi culpa perferendis esse
        cum saepe sunt assumenda necessitatibus quam voluptate at id sapiente in, minima laborum nesciunt.
    </p>
```
  * No código acima existe N maneiras de selecionar os atributos, porém a seguir introduzirei as mais "comuns".

  * Seleção através de um atributos em específico:
```css
[meu-atributo~="valor1"] {
    color: red;
}
```

  * Utilizando o seletor `[meu-atributo~="valor1"]` em CSS, estaremos selecionando elementos nos quais o atributo `meu-atributo` contenha a palavra "valor1". Este seletor não limita a busca ao que está dentro das aspas, mas sim verifica se a palavra "valor1" está presente em qualquer parte do valor do atributo, oferecendo uma maneira flexível de estilizar elementos com base em determinados conteúdos em atributos específicos.
  
  * Seleção de todos os atributos que iniciarem com "N" valor:

```css
[meu-atributo^="c"] {
    color: blueviolet;
}
```

  * Como no caso do exemplo em HTML existe um atributo chamado começou o código em CSS estará aplicando nele, pois `[meu-atributo^="c"]` basicamente expressa que qualquer atributo que inicie com C receba tais comportamentos que serão passados após as chaves.

  * Seleção de todos os atributos que possuam "n" em algum momento de sua estrutura:

```css
[meu-atributo*="ou"] {
    color: green;
}
```

  * Ainda no caso do começou ele aqui será aplicado a cor green. Pois passando `[meu-atributo*="ou"]`. Você está dizendo que todos os atributos que possuerem em algum momento de sua estrutura as letra "ou" nessa sequencia atuem da tal maneira demandada após as chaves.

  * Seleção de atributos padrões do HTML:

```css

[checked] {
    width: 50px;
    height: 50px;
}
```

  * Por mais que essa não seja a forma correta de modificarmos um atributo já declarado por padrão podemos também fazer dessa forma.Delegar que o atributo checked atue diferente do padrão
  * Porém para isso usamos pseudo-classes.Conteúdo que virá a seguir.
  
  

