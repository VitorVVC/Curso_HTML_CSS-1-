### Aula [023]


### Media queries e breakpoints

- `Links uteis`
  - `https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_media_queries/Using_media_queries`
  - `https://www.w3schools.com/cssref/css3_pr_mediaquery.php`
  -  `https://devfacts.com/media-queries-breakpoints-2021/`

### `Media Queries em CSS`
  - Media queries são uma técnica fundamental em design responsivo, permitindo que você ajuste o estilo de um site com base nas características do dispositivo ou da janela de visualização. Elas são especialmente úteis para criar layouts que se adaptam a diferentes tamanhos de tela. Abaixo estão alguns conceitos importantes:
  
- `[1]` Sintaxe Básica:
  - Uma media query começa com a palavra-chave `@media` seguida de uma condição, como a largura da tela.

```css
    @media only screen and (max-width: 600px) {
    /* Estilos aplicados quando a largura da tela for no máximo 600px */
    body {
        background-color: lightblue;
    }
}
```

- `[2]` Tipo de Mídia:
  - Você pode especificar o tipo de mídia, como `screen` (tela), `print` (impressão) ou `speech` (voz).
```css
    @media print {
    /* Estilos aplicados apenas quando a página é impressa */
    body {
        font-size: 12px;
    }
}
```

- `[3]` Condições combinadas:
  - Você pode combinar condições usando and e or.
```css
    @media only screen and (min-width: 600px) and (max-width: 1200px) {
    /* Estilos aplicados quando a largura da tela estiver entre 600px e 1200px */
    header {
        display: none;
    }
}
```

### `Breakpoints `
- Breakpoints são pontos específicos em que a aparência do layout do seu site muda para se adequar a diferentes tamanhos de tela. Ao utilizar media queries, você pode definir esses pontos de quebra para otimizar a experiência do usuário. Alguns exemplos práticos

- `Mobile First:`
  - Comece estilizando para dispositivos móveis e, em seguida, use media queries para adicionar estilos à medida que a largura da tela aumenta.

```css
    /* Estilos padrão para dispositivos móveis */
    body {
        font-size: 14px;
    }
    /* Media query para tablets */
    @media only screen and (min-width: 600px) {
    body {
        font-size: 16px;
    }
    }
    /* Media query para desktops */
    @media only screen and (min-width: 1200px) {
    body {
        font-size: 18px;
    }
    }
```

- `Tecnica de layout responsivo:`
  - Utilize breakpoints para ajustar a estrutura do layout conforme necessário.

```css
    /* Estilos padrão para dispositivos móveis */
    .container {
        width: 100%;
    }
    /* Media query para tablets */
    @media only screen and (min-width: 600px) {
    .container {
        width: 80%;
    }
    }
    /* Media query para desktops */
    @media only screen and (min-width: 1200px) {
    .container {
        width: 60%;
    }
    }
```