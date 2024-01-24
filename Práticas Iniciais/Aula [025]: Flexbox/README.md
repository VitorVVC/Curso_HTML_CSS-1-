## Aula [025]

### Flexbox

- `Links uteis`
  - `https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Flexbox#um_aparte_no_modelo_flex`.

- `Oque é flexbox?`
  - O Flexbox é um modelo de layout bidimensional que permite que você crie designs complexos e alinhamentos de elementos de maneira mais eficiente do que os modelos de layout tradicionais. Ele introduz um novo valor de propriedade chamado `display: flex;`, que transforma um contêiner em um contêiner flexível.

- `flex-direction`
  - Essa propriedade define a direção principal dos itens no contêiner flexível. Existem quatro valores principais para flex-direction:
  - `row`: Itens são dispostos na direção da linha (da esquerda para a direita por padrão).
  - `row-reverse`: Semelhante a row, mas os itens são dispostos da direita para a esquerda.
  - `column`: Itens são dispostos na direção da coluna (de cima para baixo por padrão)
  - `column-reverse`: Semelhante a column, mas os itens são dispostos de baixo para cima.

- `justify-content`
  - Essa propriedade define como os itens são distribuídos ao longo do eixo principal do contêiner. Existem vários valores para justify-content:
  - `flex-start`: Itens são alinhados no início do contêiner.
  - `flex-end`: Itens são alinhados no final do contêiner.
  - `center`: Itens são centralizados no contêiner.
  - `space-between`: O primeiro item é colocado no início, o último item é colocado no final, e o espaço restante é distribuído igualmente entre os itens.
  - `space-around`: O espaço restante é distribuído igualmente em torno de todos os itens.
  - `space-evenly`: O espaço é distribuído igualmente entre os itens, incluindo os espaços antes e depois do primeiro e último itens.


- `align-items`
  - Esta propriedade define como os itens são alinhados ao longo do eixo transversal do contêiner. Os valores possíveis para align-items incluem:
  - `stretch`: Itens são esticados para preencher o contêiner.
  - `flex-start`: Itens são alinhados no início do contêiner.
  - `flex-end`: Itens são alinhados no final do contêiner.
  - `center`: Itens são centralizados no contêiner.
  - `baseline`: Itens são alinhados à linha de base do contêiner.

- `gap`
  - A propriedade gap é usada em layouts flexíveis para definir o espaço entre os itens em um contêiner flexível. Ela é especialmente útil quando você deseja adicionar espaçamento entre elementos filhos sem a necessidade de usar margens ou preenchimentos.
  - A propriedade gap é aplicada ao contêiner flexível e aceita valores para espaçamento na direção da linha (horizontal, se a direção principal for row ou row-reverse) e na direção da coluna (vertical, se a direção principal for column ou column-reverse).

