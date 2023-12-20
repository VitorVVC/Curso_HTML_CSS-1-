## Anotações Aula [9]

### Tabelas em HTML

- A Tabela é divida em camadas:
  * `<table>` --> A camada de "abertura" da tabela.
  * `<caption>` --> A camada de "descrição" da tabela.Podemo reorganiza-la/estilizar com css.
  * `<thead>` --> Cabeçalho da tabela, onde dentro dela as tags `<tr>` e `<th>` serão usadas para dividir a linha considerada cabeçalho.
  * `<tr>` --> Tag de "abertura" de linhas da tabela, dentro da mesma usaremos outras tags para escrever / organizar a tabela.
  * `<th>` --> Tag para escrevemos o conteúdo do nosso cabeçalho.
  * `<td>` --> Tag para escrevemos o conteúdo de nossas linhas da tabela.
  * `<tbody>` --> Tag utilizada para estruturar o corpo de nossa tabela, após o cabeçalho é onde devemos escrever o conteúdo.
  * `<tfoot>` --> Tag "footer" para tabelas, onde podemos adicionar rodapés a nossas tabelas


- Dicas extras:
  * Considere a utilização de uma `<div>` para estilizar ou programar funcionalidades adicionais para suas tabelas.
  * As tags `<colspan>` e `<rowspan>` podem ser empregadas para controlar a mesclagem de células em linhas ou colunas, proporcionando flexibilidade ao design da tabela.