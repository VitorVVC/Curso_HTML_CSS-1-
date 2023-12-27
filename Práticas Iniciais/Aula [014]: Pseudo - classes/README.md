## Aula [014]

### Pseudo-Classes 

- Oque foi visto?
  * Neste repositório estou documentandouma linha de aprendizagem de HTML + CSS. Sobre peseudo-classes.
  * "Pseudo classes, oque são?": Pseudo-classes são classes e ferramentas já existentes no CSS que podemos utilizar em nossos projetos para estilização.
  * Exemplo: 
  ```css
  .heading:hover {
    background: red;
    }  
  ```

  * Neste trecho visualizamos uma classe `.heading` sendo adicionado ao CSS com um hover de background red.

- `Primeiro momento da aula`
  * Neste momento somos apresentados ao conceito de uma pseudo-classe e também a algumas de muitas delas as quais abordarei a seguir.
  * Link para visualização de todas as pseudo-classes `(Documentação W3S)`: https://www.w3schools.com/css/css_pseudo_classes.asp


  * `hover`
  * Hover é basicamente dar a um elemento o seu estilo proprio, alterado através da ação do usuário, quando o mesmo passar o cursor de seu mouse sobre tal elemento.
  * Código de exemplificação ( CSS )
  ```css
  .heading {
    transition: all 300ms ease-in-out;
    }

    .heading:hover {
    background: red;
    }
  ```
  * `Primeiro código: ` Aqui, estamos estilizando elementos que possuem a classe .heading. A propriedade transition está sendo usada para suavizar as transições de estilo. No caso, all significa que todas as propriedades CSS terão a transição aplicada, 300ms é a duração da transição (300 milissegundos), e ease-in-out é o tipo de função de temporização, indicando que a transição começará suavemente, acelerará no meio e diminuirá no final.
  * `Segundo código: ` Esta regra CSS aplica estilos específicos quando o cursor do mouse está sobre um elemento com a classe .heading. No caso, estamos alterando a cor de fundo (background) para vermelho quando o mouse passa sobre o elemento.

  * `link`
  * Permite que você selecione os links dentro de um elemento. Ela seleciona todos os links, até mesmo os que não foram visitados, incluindo os links ja estilizados em outras classes ou ids com o `hover`, `active` ou `visited`. Para um funcionamento adequado é essencial que ela venha antes das regras: `visited` — `hover` — `active`. O `focus` é uma pseudo-class geralmente usada antes de `a:hover` ou depois, dependendo do resultado esperado.
  * Código de exemplificação ( CSS )
```css
a {
    /* Código 1 */
    color: darkorange;
}

a:link {
    /* Código 2 */
    color: deeppink;
}

a:visited {
    /* Código 3 */
    color: firebrick;
}

a:hover {
    /* Código 4 */
    background: darkblue;
    color: white;
    text-decoration: none;
}

a:active {
    /* Código 5 */
    background: darkslategray;
    color: white;
    text-decoration: none;
}
```
* `Código [1]: ` Esta regra aplica um estilo padrão a todos os links. Define a cor do texto para darkorange.
* `Código [2]: ` Aqui, especificamos o estilo para links que não foram visitados. Define a cor do texto para deeppink.
* `Código [3]: ` Esta regra estiliza links que já foram visitados, alterando a cor do texto para firebrick.
* `Código [4]: ` Ao passar o mouse sobre um link `(:hover)`, a cor de fundo é alterada para darkblue, o texto para white, e a decoração de texto é removida `(text-decoration: none)`. Isso cria um efeito visual quando o usuário interage com o link.
* `Código [5]: ` Esta regra define o estilo para links quando estão sendo clicados `:active`. O fundo se torna darkslategray, o texto white, e a decoração de texto é removida.

`Pseudo classes para INPUT`
* Estas pseudo-classes que virão a seguir não necessariamente são apenas para INPUT porém a forma que estudei elas encaixaram perfeitamente para melhor coompreensão.
* De forma breve abordarei cada uma das pseudo-classes após a visualização de sua escrita.
* Código de exemplificação ( CSS )

```css
input:focus {
    /* Código 1 */
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
    outline: none;
    border: 1px solid black;
}

input:disabled {
    /* Código 2 */
    background-color: rebeccapurple;
    cursor: not-allowed;
}

input:enabled{
    /* Código 3 */
    background-color: blue;
    cursor: auto;
}

input:checked{
    /* Código 4 */
    width: 50px;
    height: 50px;
}

input:checked + p{
    /* Código 5 */
    background: red;
}

.pai .lista li:first-child{
    /* Código 6 */
    background: blueviolet;
}

input:required{
    /* Código 7 */
    background: red;
}
```
  * `Código [1]: ` Quando um input recebe foco `(:focus)`, um efeito de sombra `(box-shadow)` é aplicado, a borda `(border)` é definida como `1px sólida black`, e a borda de foco padrão é removida `(outline: none)`.
  * `Código [2]: ` Estiliza um input `desabilitado`. Define o fundo para `rebeccapurple` e o cursor para `not-allowed`, indicando visualmente que o campo está desativado.
  * `Código [3]: ` Estiliza um input `habilitado`. Define o fundo para `blue` e restaura o cursor para o comportamento padrão `(auto)`.
  * `Código [4]: ` Quando um input está marcado `(:checked)`, o tamanho é alterado para 50x50 pixels.
  * `Código [5]: ` Quando um input está marcado `(:checked)`, o parágrafo adjacente `(+ p)` tem o fundo alterado para `vermelho`.
  * `Código [6]: ` Estiliza o `primeiro elemento li` dentro de uma lista com a `classe .lista`, que está dentro de um elemento com a `classe .pai`. Define o fundo para `blueviolet`.
  * `Código [7]:  `Estiliza inputs que são marcados como obrigatórios `(:required)`. Define o fundo para `vermelho`.