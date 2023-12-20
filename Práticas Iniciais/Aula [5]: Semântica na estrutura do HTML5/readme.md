### Anotações aula [5]

## Tags de Separação de conteúdo:

- `<header>` (Cabeçalho)
  * Marca a introdução de um conteúdo ou seção. Pode conter logotipos, títulos, menus de navegação e etc.
  * Exemplo:
    ```html
    <header>
      <h1>Meu Site</h1>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Sobre</a></li>
          <li><a href="#">Contato</a></li>
        </ul>
      </nav>
    </header>
    ```

- `<nav>` (Navegação)
  * Define uma seção de navegação. Pode conter links ou outros elementos de navegação.
  * Exemplo: Acima usado juntamente ao `<header>`

- `<main>` (Conteúdo principal)
  * Contém o conteúdo principal da página, excluindo cabeçalhos, rodapés e barras laterais.
  * Exemplo:
    ```html
    <main>
      <h2>Artigos recentes</h2>
      <!-- Conteúdo principal da página -->
    </main>
    ```

- `<section>` (Seção)
  * Agrupa um conteúdo tematicamente relacionado e geralmente possui um cabeçalho.
  * Pode e deve ser usado também quando não possuir outro separador mais semântico para a solução atual.
  * Exemplo:
    ```html
    <section>
      <h2>Seção 1</h2>
      <!-- Conteúdo relacionado à Seção 1 -->
    </section>
    
    <section>
      <h2>Seção 2</h2>
      <!-- Conteúdo relacionado à Seção 2 -->
    </section>
    ```

- `<article>` (Artigo)
  * Define um conteúdo independente e autônomo, como um post de um blog ou notícia.
  * Exemplo:
    ```html
    <article>
      <h2>Título do Artigo</h2>
      <p>Conteúdo do artigo...</p>
    </article>
    ```

- `<aside>` (Barra lateral)
  * Contém conteúdo relacionado ao conteúdo circundante, como barras laterais ou caixas de informações.
  * Exemplo:
    ```html
    <aside>
      <h2>Publicidade</h2>
      <!-- Conteúdo da barra lateral -->
    </aside>
    ```

- `<footer>` (Rodapé)
  * Define um rodapé para um documento ou seção. Pode conter informações de copyright, links para páginas relacionadas e etc.
  * Exemplo:
    ```html
    <footer>
      <p>&copy; 2023 Meu Site</p>
      <nav>
        <ul>
          <li><a href="#">Política de Privacidade</a></li>
          <li><a href="#">Termos de Serviço</a></li>
        </ul>
      </nav>
    </footer>
    ```
