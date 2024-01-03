## Aula [017]

### Propriedades especificas do Box-Model

- Oque foi visto nesta aula?
  * Neste repositorio estarei documentando meu aprendizado com algumas propriedades especificas do Box-Model, como `display`, `box-sizing`, formas de manipularmos `width` e `height`.

- `Box-Sizing`
  * Esta propriedade de CSS determina como funcionará nosso "bloco" de conteúdo, no caso deste repositorio uma `div`.
  * Fora isto, esta propriedade é utilizada para definir como as dimensões totais de um elemento são calculadas, incluindo bordas e preenchimento.
  
- `box-sizing: content-box;`
  * Nas dimensões totais do elemento, apenas o conteúdo é considerado.
  * O preenchimento (padding), bordas e margens não são incluídos no cálculo da largura e altura do elemento.
  * Este é o comportamento padrão do modelo de box-sizing.
  
- `box-sizing: padding-box;`
  * Nas dimensões totais do elemento, tanto o conteúdo quanto o preenchimento (padding) são considerados.
  * As bordas e margens não são incluídas no cálculo da largura e altura do elemento.
  * Este valor não é amplamente suportado em todos os navegadores e não é comumente utilizado.
  
- `box-sizinh: border-box`
  * Nas dimensões totais do elemento, o conteúdo, preenchimento (padding) e bordas são todos considerados.
  * A margem ainda não é incluída no cálculo da largura e altura do elemento.
  * Este valor é frequentemente utilizado porque facilita o dimensionamento e layout dos elementos.

- `Considerações sobre Box-Sizing.`
  * Claro que usaremos tal box-sizing referente a situação e necessidades. Porém ainda assim é preferivel utilizar `border-box` ao meu ver. Pois ela facilita e nos da mais controle no momento de estilização de nossas aplicações, desconsiderando a margem e fazendo ela ser utilizada apenas como porcentagem de distancia entre um box model e outro.
  * Contudo, claro o `content-box`, é o modelo padrão e não atoa, todo o conteudo e modificações são feitas sem alterações na altura e largura do nosso box-model, oque já é por si só muito agradavel.
  * Já o `padding-box`, vimos em aula porém eu hoje não vejo necessidade e situações para sua utilização, fora não ser amplamente suportada como os outros dois modelos, ela mesma é "instável". Pois "desregula" a sua altura e largura referente as modificações que forem sendo aplicadas ao box-model utilizados.

- `Display`
  * Neste tópico estarei abordando tanto o display `block`, quanto o display `inline` que são os mais comumente utilizados.

- `Display: Block`
  * block é comumente utilizada para definir um elemento como um bloco. Isso significa que o elemento ocupará toda a largura disponível e começará em uma nova linha. Alguns elementos HTML padrão, como `<div>`, são naturalmente de bloco.
  * Exemplo:
```css
    .block-element {
        display: block;
        width: 100%;
        background-color: #3498db;
        color: #fff;
        padding: 10px;
        margin-bottom: 10px;
    }
```

- `Display: Inline`
  * Em contraste, a propriedade display: inline faz com que um elemento seja formatado como uma caixa inline, permitindo que outros elementos fiquem ao lado dele na mesma linha. No entanto, elementos inline não aceitam largura `(width)` e altura `(height)` diretamente.
  * Exemplo:
```css
    .inline-element {
        display: inline;
        background-color: #e74c3c;
        color: #fff;
        padding: 5px;
        margin-right: 10px;
    }
```

- `Considerações sobre Display`
  * A escolha entre display: block e display: inline depende do layout desejado. Elementos de bloco são ideais para seções de layout, enquanto elementos inline são úteis para conteúdo que terão segmento na mesma linha, como texto ou links.


- `Um pouco sobre width e height`
  * No CSS deste repositorio foram passadas varias funções e estilos dentro deste tópico.
  * Tais como: `overflow: auto;`, `max-width: 600px`, `min-width: 0` entre outras. Abaixo fornecerei o trecho abordado e também logo em sequencia breves explicações sobre cada uma das funções utilizadas.
```css
.texto {
    box-sizing: border-box;
    display: block;
    background: red;
    width: 100%;
    max-width: 600px;
    min-width: 0;
    height: 100%;
    max-height: 500px;
    min-height: 100px;
    overflow: auto;
    margin: 0 auto 50px auto;
    padding: 50px;
    border: 5px solid black;
    border-width: 5px;
    border-style: groove;
    border-color: blueviolet;
}
```

`width: 100%;`
Define a largura do elemento como 100% da largura do seu contêiner pai.
max-width: 600px;

`max-width: 600px;`
Estabelece a largura máxima do elemento como 600 pixels. O elemento não poderá ultrapassar esse valor, mesmo que a largura do contêiner pai permita mais espaço.

`min-width: 0;`
Define a largura mínima do elemento como 0. Isso pode ser útil para garantir que o elemento não tenha uma largura menor do que o permitido pelo seu conteúdo ou por outros estilos aplicados.

`height: 100%;`
Define a altura do elemento como 100% da altura do seu contêiner pai.

`max-height: 500px;`
Estabelece a altura máxima do elemento como 500 pixels. Assim como max-width, essa propriedade impede que o elemento ultrapasse essa altura.

`min-height: 100px;`
Define a altura mínima do elemento como 100 pixels. Semelhante a min-width, isso assegura que o elemento tenha pelo menos essa altura, mesmo que o conteúdo seja menor.

`overflow: auto;`
Define o comportamento de overflow do conteúdo. Neste caso, se o conteúdo dentro do elemento exceder suas dimensões, barras de rolagem serão adicionadas automaticamente.

`margin: 0 auto 50px auto;`
Define margens do elemento. 0 para margem superior e inferior, auto para margens esquerda e direita. A utilização de auto nas margens laterais é uma técnica comum para centralizar o elemento horizontalmente.

`padding: 50px; `
Define o preenchimento interno do elemento como 50 pixels. Isso adiciona espaço interno ao redor do conteúdo do elemento.

`border: 5px solid black; `
Define uma borda de 5 pixels, sólida (solid), e de cor preta.

`border-width: 5px;`
Define a largura da borda como 5 pixels. Este valor é uma parte da propriedade border e pode ser usado para especificar a largura da borda separadamente.

`border-style: groove; `
Define o estilo da borda como "groove", que cria uma borda tridimensional que dá a aparência de estar entalhada na tela.

`border-color: blueviolet;`
Define a cor da borda como azul-violeta.


