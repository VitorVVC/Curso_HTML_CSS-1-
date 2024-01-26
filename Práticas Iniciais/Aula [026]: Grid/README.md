### Aula [026]


- `Links uteis:`
  - `https://caniuse.com` --> Site para procurar se sua tecnlogia CSS é suportada em alguns navegadores.
  - `https://developer.mozilla.org/pt-BR/docs/Web/CSS/grid`
  - `https://www.w3schools.com/css/css_grid.asp`
  - `https://css-tricks.com/snippets/css/complete-guide-grid/`


- Oque foi visto?
  - Vimos do mais básico ao um pouco mais avançado conceito de GRID


-`grid`
  - A propriedade display: grid em CSS permite que você crie layouts de grade em um contêiner, tornando mais fácil organizar elementos filhos em linhas e colunas.
  - `grid-template-columns` e `grid-template-rows`:
    - Define o número e o tamanho das colunas e linhas da grade. Você pode especificar tamanhos absolutos, porcentagens ou usar palavras-chave como auto e fr (fração).
    ```css
    .container {
        grid-template-columns: 100px 100px 100px;
        grid-template-rows: 50px 50px;
    }
    ```


-`gap`
  - Define o espaçamento entre as células da grade (colunas e linhas). Pode ser uma unidade absoluta (px, em) ou uma porcentagem.


- `Atalhos com grid-template`
  - Você pode usar a propriedade grid-template para definir todas as propriedades de grade em uma única linha.
  ```css
    .container {
        grid-template: repeat(2, 50px) / repeat(3, 1fr);
        gap: 10px;
    }
  ```