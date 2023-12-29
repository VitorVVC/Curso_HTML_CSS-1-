## Aula [015]

### Especifidade CSS

- Oque foi visto?
  * Vimos como funciona a especificade do CSS, tanto em seu calculo quanto em sua "ordem" de prioridades..


- `Maiores pontuações de especificidade do CSS`
  * `ID`
  * `Class`
  * `Atributos`
  * `Pseudo-Classes`
  * `Elementos`
  * `Pseudo-Elementos`

- `Especificando no CSS`
  * Primeiro nivel de especificidade:
```css
    #p {
    /* Especificidade 1 0 0  */
    background: red; 
    }
```
  * Nesta situação estamos estilizando baseado em uma `id`, portanto seu nivel de especificidade é `(1-0-0)`.


  * Segundo nivel de especifiidade
```css
    #p.p{
    /* Especificidade 0 1 0 */
    background: yellow;
    }
```

  * Por assim podemos seguir até o rumo especificado / desejado.
  * Uma função que não é muito recomendada porém mesmo assim abordarei, é a `!important`.

```css
    body{
    background: darkcyan !important;
    }

    body{
    background: darkblue;
    }
```

  * Como nós sabemos, nessa linha de código o `darkblue` se sobressairia sobre o `darkcyan`, porém usando `!important` o navegador interpretará mesmo que escrito anteriormente a cor darkcyan.

<hr>

-`Considerações!`
  * No geral, utilizamos mais `id`,`class`,`pseudo-classes`,`elementos` como forma de especificação em nosso CSS. Utilizar `!important`, e códigos super especificos no geral não é muito proveitoso em um trabalho em equipe.