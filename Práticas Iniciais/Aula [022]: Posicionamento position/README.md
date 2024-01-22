## Aula [022]

### Posicionamento Position

- `Links uteis:`
  - `https://www.w3schools.com/css/css_positioning.asp`

- Oque foi visto ?
  - Vimos bastante sobre `position`.
  - Position `static`,`relative`,`absolute`,`fixed` e `sticky`.


- `static`
  - O valor padrão. Elementos com posição estática são posicionados no fluxo normal do documento. As propriedades `top`,`right`,`bottom` e `left` não tem efeito quando `position` é `static`.

```css
    .elemento {
        position: static;
    }
```

- `Relative`
  - Um elemento com posição relativa é posicionado em relação à sua posição normal. Ou seja, você pode mover o elemento usando as propriedades `top`, `right`, `bottom` e `left`, sem afetar o layout dos outros elementos.
  - Ele não afeta a viewport e nem elementos ao redor, somente seu elemento.
```css
    .elemento {
        position: relative;
        top: 10px;
        left: 20px;
    }
```

- `Absolute`
  - Um elemento com posição absoluta é removido do fluxo normal do documento e posicionado em relação ao seu ancestral mais próximo que não tenha posição estática. Se não houver tal ancestral, ele será posicionado em relação ao elemento `<html>`.
```css
    .elemento {
        position: absolute;
        top: 50px;
        left: 100px;
    }
```

- `Fixed`
  - Um elemento com posição fixa é removido do fluxo normal e é posicionado em relação à janela de visualização, portanto, ele permanecerá fixo mesmo ao rolar a página.
```css
    .elemento {
        position: fixed;
        top: 0;
        right: 0;
    }
```

- `Sticky`
  - Um elemento com posição pegajosa é um pouco como uma mistura de relativo e fixo. O elemento é tratado como relativo até que ele atinja um determinado ponto enquanto rola a página, momento em que ele se torna fixo.
  - Ela pode se tornar uma fixa e "se fixar" novamente a outro elemento com position também sticky.

```css
  .elemento {
    position: sticky;
    top: 20px;
  }
```
