## Aula [020]

### Unidades de medidas do CSS

- O que foi visto?
  - Nesta aula de hoje nos foi apresentado varias unidades de medidas, com foco nas mais utilizadas pelo mercado e mais semânticas.
  - Abordarei abaixo um pouco sobre cada uma das unidades de medidas.


- `Absolute Lengths`
  - Absolute Lengths são unidades de medidas absolutas, que ao serem declaradas atuaram como unidades fixas em comprimento expresso. 
  - Estas unidades não são recomendadas para uso nas telas, porque o tamanho de telas variam, enquanto estas unidades não !
  - No entando elas podem tranquilamente serem utilizadas por meio de saida. Como em algum layout de impressão.
  
  
    | Unidade | Descrição       |
    | ------- | --------------- |
    | `cm`    | centimeters     |
    | `mm`    | millimeters     |
    | `in`    | inches (1in = 96px = 2.54cm) |
    | `px`    | pixels (1px = 1/96th of 1in) |
    | `pt`    | points (1pt = 1/72 of 1in)   |
    | `pc`    | picas (1pc = 12 pt)           |


- `Relative Lengths`
  - Relative Lengths são unidades que especificam um comprimento relativo a outra propriedade de comprimento.
  - Elas são melhores dimensionadas em diferentes meios de renderização
  - E em sua grande maioria seguirão o tamanho de seus "pais". Logo após a demonstração abordarei mais este conceito.

    | Unit   | Description                                                    |
    | ------ | -------------------------------------------------------------- |
    | `em`   | Relative to the font-size of the element (2em means 2 times the size of the current font) |
    | `ex`   | Relative to the x-height of the current font (rarely used)    |
    | `ch`   | Relative to the width of the "0" (zero)                        |
    | `rem`  | Relative to the font-size of the root element                  |
    | `vw`   | Relative to 1% of the width of the viewport                    |
    | `vh`   | Relative to 1% of the height of the viewport                   |
    | `vmin` | Relative to 1% of the viewport's smaller dimension             |
    | `vmax` | Relative to 1% of the viewport's larger dimension              |
    | `%`    | Relative to the parent element                                  |

- `Mais utilizadas && Vistas nesta aula`
    - `em: Relative to the Font-size of the Element`
      - O em é uma unidade de medida relativa ao tamanho da fonte do elemento pai. Por exemplo, se o tamanho da fonte do elemento pai for 16 pixels, 1em será equivalente a 16 pixels. Se aplicado a um elemento filho, será relativo à fonte do pai mais imediato que tenha uma fonte especificada.
    - `rem: Relative to the Font-size of the Root Element`
      - Similar ao em, mas rem é relativo ao tamanho da fonte do elemento raiz `(normalmente o <html>)`. Isso evita herança de tamanhos de fonte em cascata, facilitando a criação de layouts mais previsíveis.
    - `vw: Relative to 1% of the Width of the Viewport `
      - A unidade vw representa uma porcentagem da largura total da viewport (a área visível da janela do navegador). Se você definir algo para 10vw, isso significa que será 10% da largura da viewport, independentemente do tamanho da tela.
    - `vh: Relative to 1% of the Height of the Viewport`
      - Similar ao vw, mas relativo à altura da viewport. Se você definir algo para 10vh, isso significa que será 10% da altura da viewport.
    - `vmax: Relative to 1% of the Viewport's Larger Dimension`
      - O vmax é relativo a 1% da dimensão maior da viewport, seja a largura ou a altura. Ele ajusta automaticamente com base na maior dimensão da viewport.
    - `%: Relative to the Parent Element`
      - A unidade percentual (%) é relativa ao elemento pai. Por exemplo, se você definir a largura de um elemento como 50%, ele ocupará metade da largura do seu elemento pai.