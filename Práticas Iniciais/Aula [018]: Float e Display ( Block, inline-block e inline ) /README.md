## Aula [018]

### Float e Display ( Block, inline-block e inline )

- Oque foi visto ?
  * Neste repositorio estarei armazenando uma aula com breves explicações sobre displays e float no CSS..
  * Propriedades essas que são utilizadas de N maneiras e para N soluções.. Mas abordarei breves resumos sobre ambos os conteúdos ao decorrer deste documento.

- `Float`
  * Oque é um float ?..
  * De forma breve, um elemento que possua float acabará por estar em um estado de "flutuar". Quando possuimos um elemento `block` e queremos que não consuma toda a tela, utilizamos um `float: left`, assim ele após consumir seu espaço referente a altura e largura "flutuará" para a esquerda. Possuindo tal comportamento fica mais simples de montarmos "grids" e outros elementos que precisem da propriedade block de forma mais organizada, estruturada e semântica.
  
- `Clear`
  * O clear é uma propriedade que anda ao lado do float, pois fazendo elementos flutuarem precisamos depois de um tempo os "limpar" para dar entrada a novos elementos e propriedades, para isso utilizamos o `clear: `. O clear é uma propriedade que pode ser passada para qualquer atributo, para antes do mesmo ser colocado ele limpe o float anterior...
  * Uma forma de fazer isso de forma "automática" e simples, é inserir um pseudo-elemento `:after`, desta forma:

```css
    .grid::after{
        content: '';   
        display: block;
        clear: both;
    }
```
  * Desta forma, teremos após a `div` com a class `grid`, um content vazio, sendo do tipo block para "pular" uma linha e o `clear: both;`, que limpará todos os lados para dar segmento ao elemento que vier a seguir.


- `Display`
  * Por mais que anteriormente, em outros repositórios, eu tenha abordado esse tema, estarei reforçando esse conhecimento e adicionando novas informações referentes a esta aula.

  * O que é um display?
  * Bom, um display é a "forma de se comportar" que um elemento terá, sendo os mais comuns: `inline`, `inline-block`, `block` & `grid`. Por padrão, algumas tags e elementos se comportam com displays específicos, como a `div`, que é um separador de conteúdo em bloco, e a `span`, que é inline.

  * Este tipo de atributo é de extrema importância no momento de estruturarmos nossas aplicações, servindo como divisor de águas entre sites organizados, estruturados, e semânticos, versus sites sem semântica e amarrados a gambiarras.
