## Aula[015]

### Herança e propriedades.

- Oque foi visto? 
  * Neste repositorio estarei documentando uma breve aula que tive sobre heranças e propriedades que são passadas para elementos filhos.
  * No HTML tudo que houver dentro de tags pais automaticamente será herdado também por "tags filhas".
  * Como no exemplo abaixo, onde na tag `<body>` passamos elementos como, cor e todas as demais tags herdam de body este mesmo comportamento.
```css
    body{
        color: red;
        font-family: sans-serif;
        font-size: 20px;
    }
```

  * Também foi dito que caso necessário, podemos delegar que tags tenham comportamento `initial`, para assim não herdarem tal atributo, como por exemplo: 
```css
    p{
        color: initial;
    }
```
  * Desta forma a cor da tag `<p>` não será herdada do body.
  * Contudo, podemos delegar especificamente que tal tag herde algo de seu "pai", utilizando: `inherit`.
  
```css
    p{
        color: inherit;
    }
```

  * Desta forma a cor da tag `<p>` volta a herdar a cor de seu pai, no caso body.