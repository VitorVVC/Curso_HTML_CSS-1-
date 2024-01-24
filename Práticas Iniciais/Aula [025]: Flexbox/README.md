## Aula [025]

### Flexbox

- `Links uteis`
  - `https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Flexbox#um_aparte_no_modelo_flex`.
  - `https://flexboxfroggy.com`.
  - `https://css-tricks.com/snippets/css/a-guide-to-flexbox/`

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

- `flex-wrap`
  -  Esta propriedade controla se os itens no contêiner flexível devem ser distribuídos em uma única linha ou em várias linhas. Existem três valores principais para flex-wrap:
  -  `nowrap (padrão)`: Todos os itens são dispostos em uma única linha.
  -  `wrap`: Os itens são dispostos em várias linhas, se necessário.
  -  `wrap-reverse`: Os itens são dispostos em várias linhas, mas em ordem reversa.
  -  Se você definir `flex-wrap: wrap;` e o conteúdo não couber em uma única linha, ele será automaticamente movido para a próxima linha.

- `align-content`
  - Esta propriedade controla o alinhamento de linhas no contêiner flexível quando há espaço extra na direção transversal. Ela só tem efeito quando há mais de uma linha no contêiner. Os valores para align-content incluem:
  - `flex-start`: Linhas são alinhadas no início do contêiner.
  - `flex-end`: Linhas são alinhadas no final do contêiner.
  - `center`: Linhas são centralizadas no contêiner.
  - `space-between`: O espaço restante é distribuído igualmente entre as linhas.
  - `space-around`: O espaço restante é distribuído igualmente ao redor das linhas.
  - `stretch`: Linhas são esticadas para preencher o contêiner.
  - A propriedade align-content afeta a disposição das linhas quando há espaço extra na direção transversal. Se flex-wrap for nowrap, align-content não terá efeito, pois não há várias linhas.

- `inline-flex`
  - `display: flex;`:
    - O valor flex faz com que o contêiner flexível seja exibido como um bloco, ocupando toda a largura disponível na linha.
    - Elementos com display: flex geralmente começam em uma nova linha e ocupam toda a largura disponível.
  - `display: inline-flex;`
    - O valor inline-flex faz com que o contêiner flexível seja exibido como um elemento de linha, permitindo que outros elementos apareçam na mesma linha.
    - Elementos com display: inline-flex se ajustam ao conteúdo na mesma linha, permitindo que outros elementos (como texto ou outros elementos inline) apareçam ao lado do contêiner flexível.

- `flex-flow`
  - A propriedade flex-flow é uma propriedade abreviada no CSS que combina as propriedades flex-direction e flex-wrap em uma única declaração. Isso simplifica a escrita do código, fornecendo uma maneira concisa de definir a direção principal dos itens e se eles devem ser dispostos em uma única linha ou em várias linhas.
  - `<flex-direction>`: Pode ser row, row-reverse, column ou column-reverse.
  - `<flex-wrap>`: Pode ser nowrap, wrap ou wrap-reverse.
  - O uso de flex-flow é opcional, e você pode continuar usando `flex-direction` e `flex-wrap` separadamente se preferir. No entanto, quando você precisa definir ambos, flex-flow oferece uma maneira mais compacta de fazer isso.

- `flex-grow`
  - A propriedade flex-grow é uma propriedade do Flexbox no CSS que define a capacidade de um item flexível crescer em relação aos outros itens flexíveis dentro do mesmo contêiner flexível. Ela especifica a proporção em que os itens devem ocupar o espaço disponível.
  - A propriedade flex-grow aceita um valor numérico, que representa a proporção do espaço disponível que um item flexível deve ocupar em relação aos outros itens flexíveis. Quanto maior o valor de flex-grow, mais espaço o item flexível receberá em relação aos outros itens.
  - Se todos os itens têm o mesmo valor de flex-grow, eles compartilham igualmente qualquer espaço adicional disponível. Se alguns itens têm um valor maior que outros, eles receberão uma parte maior do espaço extra.

- `flex-basis`
  - A propriedade flex-basis é uma propriedade do modelo de layout Flexbox no CSS. Ela define o tamanho inicial de um item flexível antes que o espaço adicional seja distribuído de acordo com as propriedades flex-grow, flex-shrink, e o tamanho disponível.
  - A propriedade flex-basis aceita valores que podem ser uma dimensão absoluta (como pixels ou porcentagens) ou uma palavra-chave (como auto ou content). Aqui estão alguns exemplos:

- `flex`
  - A propriedade flex é uma propriedade abreviada que combina as propriedades `flex-grow`, `flex-shrink` e `flex-basis` em uma única declaração. Ela fornece uma maneira mais concisa de definir o comportamento de um item flexível em relação ao seu tamanho e à distribuição de espaço em um contêiner flexível.
  - `<flex-grow>`: Um número que representa a proporção do espaço adicional que o item pode ocupar em relação aos outros itens flexíveis.
  - `<flex-shrink>`: Um número que representa a proporção do espaço que o item pode encolher em relação aos outros itens flexíveis.
  - `<flex-basis>`: Um valor que representa o tamanho inicial do item antes de qualquer espaço adicional ser distribuído.

- `align-self`
  - A propriedade align-self é uma propriedade do modelo de layout Flexbox no CSS que permite ajustar o alinhamento de um item flexível em relação à linha transversal do contêiner flexível. Essa propriedade tem um efeito individual sobre cada item flexível, permitindo que você modifique o alinhamento de um item específico, enquanto os outros itens permanecem alinhados conforme as propriedades de alinhamento do contêiner.
  - A propriedade align-self aceita os seguintes valores:
  - `auto`: O comportamento padrão, onde o item flexível herda o valor da propriedade align-items do contêiner flexível pai.
  - `flex-start`: Alinha o item no início da linha transversal.
  - `flex-end`: Alinha o item no final da linha transversal.
  - `center`: Centraliza o item ao longo da linha transversal.
  - `baseline`: Alinha o item à linha de base do contêiner.
  - `stretch`: Estica o item para preencher toda a altura da linha transversal.

- `order`
  - A propriedade order é uma propriedade do modelo de layout Flexbox no CSS que define a ordem de exibição dos itens flexíveis dentro do contêiner flexível. Ela permite reorganizar visualmente os itens sem alterar a ordem do código HTML.
  - A propriedade order aceita um valor numérico. Os itens são exibidos em ordem crescente com base nos valores fornecidos. Um valor menor de order resulta em uma exibição mais à esquerda ou no início do contêiner, enquanto um valor maior de order resulta em uma exibição mais à direita ou no final do contêiner.
