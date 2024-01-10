## Aula [019]

### Cores em HTML

- Oque foi visto?
  - Nesta aula dedico minhas anotações sobre o conteúdo de cores em HTML.
  - Vimos como podemos personalizar nossas cores, sites que nos ajudam, modelos de cores em hexadecimal, cores padrões,HSL / HSLA, RGB e  RGBA..

- Links uteis:
  - Color Pick W3S : `https://www.w3schools.com/colors/colors_picker.asp`
  - HTML Colors W3S : `https://www.w3schools.com/html/html_colors.asp`
  - HSL and HSLA W3S : `https://www.w3schools.com/html/html_colors.asp`
  - HTML Color Codes : `https://htmlcolorcodes.com`
  - Color Developer Mozilla : `https://developer.mozilla.org/pt-BR/docs/Web/CSS/color_value`

- `Um pouco do que foi visto:`
```CSS
    .exemplo{
        color: #ff0000;
        color: hsl(0,100%,50%);
        color: rgb(255,0,0);
        color: rgba(255,0,0,1);
        color: red;
    }
```
- `Explicando cada um dos modelos: `
  - Hexadecimal: #ff0000 - Representa a cor vermelha. Cada par de dígitos representa a intensidade de vermelho, verde e azul, respectivamente, em formato hexadecimal.

  - HSL (Hue, Saturation, Lightness): hsl(0, 100%, 50%) - Representa a cor vermelha também. A primeira parte (0) é a tonalidade (hue) em graus, a segunda parte (100%) é a saturação (saturation), e a terceira parte (50%) é a claridade ou luminosidade (lightness).

  - RGB (Red, Green, Blue): rgb(255, 0, 0) - Representa a cor vermelha. Cada valor entre parênteses representa a intensidade de vermelho, verde e azul, respectivamente, em uma escala de 0 a 255.

  - RGBA (RGB com Alpha): rgba(255, 0, 0, 1) - Similar ao RGB, mas com um quarto valor que representa a opacidade (alpha), variando de 0 a 1. Neste exemplo, a cor é totalmente opaca (1).

  - Nome da Cor: red - Usa um nome de cor pré-definido. Existem várias cores com nomes padrão, como red, blue, green, etc.

