## Aula [10]

## Formulários & Inputs com HTML
-Links de referencia:
  * Documentacão de inputs: (https://www.w3schools.com/html/html_form_input_types.asp)
  * Documentacão de formatacão: (https://developer.mozilla.org/pt-BR/docs/Learn/Forms/How_to_structure_a_web_form)
  * HTML Color Picker: (https://www.w3schools.com/colors/colors_picker.asp)
<hr>
  
-`<Input de texto>`

-`<form>`
  * Tag para "criar" um formulário.
  * Dentro desta tag entrará todo o conteudo de nosso formulario.
-`<label>`
  * Tag para criacão de uma label que recebe com `<for>` o id do input.
-`<input>`
  * Tag para criacão do input.Recebe um type(text,radio,checkbox e etc), um nome e ID. Pode-se adicionar outros requisitos, como placeholder, required,value e muitos outros.

```html
    <form action="#" method="get" target="_blank" autocomplete="off">
        <p>O meu formulário</p>
        <!-- Input de texto -->
        <p>
            <label for="nome">Nome:</label>
            <input type="text" name="nome" id="nome" placeholder="Seu nome" required>
        </p>
    </form>
```
  * Dentro do código acima nos criamos um simples formulario de entrada para nomes.
  * Passamos também "required" para o formulário so poder ser enviado caso o campo acima seja respondido de acordo.

-`<Input de checkboxes>`

```html
        <!-- Checkboxes -->
        <p>
            <label for="dev">Sou um dev</label>
            <input type="checkbox" name="dev" id="dev" value="sim">
            <br>
            <label for="dev2">Sou um dev2</label>
            <input type="checkbox" name="dev2" id="dev2" value="sim">
            <br>
            <label for="dev3">Sou um dev3</label>
            <input type="checkbox" name="dev3" id="dev3" value="sim">
        </p>
```
  * No código acima criamos uma checkbox com vários itens para o usuário poder marcar.

-`<Radio Buttons>`

```html
        <!-- Radio buttons -->
        <p>
            Gênero: <br>
            <label for="feminino">Feminino</label>
            <input type="radio" name="escolha-genero" id="feminino" value="feminino">
            <br>
            <label for="masculino">Masculino</label>
            <input type="radio" name="escolha-genero" id="masculino" value="masculino">
            <br>
            <label for="prefiro-não-responder">Prefiro não responder</label>
            <input type="radio" name="escolha-genero" id="prefiro-não-responder" value="prefiro-não-responder">
        </p>
```

  * No código acima criamos "botões radio" que são botões de multiplica escolha porem apenas uma marcacão do usuário, como no exemplo de genero. O usuario só poderá escolher um.
  * Porém sua estrutura é diferente das anteriormente citadas, pois todas as opcões devem seguir o mesmo "name" e apenas possuirem id's e valores diferentes para se receber no back-end.

-`<Data Input>`

```html
        <!-- Input de data -->
        <p>
            <label for="datetime-local">Data de nascimento:</label>
            <input type="datetime-local" name="datetime-local" id="datetime-local" required value="2023-04-20T20:00">
        </p>
```
  * No código acima nos novamente criamos uma label com input, porém dessa vez passamos datetime-local como o tipo. Podendo ter sido apenas "date, "datetime" ou "datetime-local".. Oque difere estas tres formatacoes de tempo é que na primeira possuimos apenas a data, na segunda data e hora enquanto na terceira, data e hora e algum tipo de timeZone.. Que por padrão ele pega o de nossa máquina.
  * Fugindo um pouco do conceito de datas e retornando as tags HTML, nós passamos este campo do formulário como required e um "valor" predeteriminado para sofrer mudancas sob o desejo do usuário.

-`<Input de Hora>`

```html
        <!-- Input de hora -->
        <p>
            <label for="time">Time:</label>
            <input type="time" name="time" id="time" required value="20:00:01">
        </p>
```
  * No código acima criamos um input de hora, como de exemplo posso lhe dizer que alguns softwares de marcacão de cirurgias, mesas de restaurante e entre outros podem vir a utilizar, portanto é cabivel o estudo deste tipo de input.Por mais que possamos pegar data + hora se faz util este tipo de input em n aplicacões
  * Enfim, passamos como type o "time", colocamos como required e o seu valor padrão para sofrer alteracões com o usuário.

-`<Input de cores>`
```html
        <!-- Input de cor -->
        <p>
            <label for="cor">Cor favorita:</label>
            <input type="color" name="cor" id="cor" required value="#FF0000">
        </p>
```

  * No código acima nós passamos para o usuário qual a sua cor favorita, por meio de uma label que já foi comentada. Pelo type color e passando o valor padrão como vermelho através de hexadecimal.
  * Dentro do site o usuário pode mudar a variacão da cor para encontrar a que mais se adequa com seu gosto ou mesmo passar o valor de R G B.

-`<Input de email>`
```html
        <!-- Input de email -->
        <p>
            <label for="email">Seu email:</label>
            <input type="email" name="email" id="email" placeholder="email@email.com">
        </p>
```

  * No input acima descrevo o input mais básico de email possivel, o navegador trata execões como a falta de @ ou de uma localizacao deste @, a falta do .com e etc.. Porém com JS / Back-end podemos tratar de forma muito mais precisa e condizente com nossa aplicaco..
  * Fora isso utilizo um placeholder para o usuario antes de inputar algo ter uma base de como pode escrever o conteudo naquela caixa.

-`<Input de senha>`

```html
        <!-- Input de senha -->
        <p>
            <label for="password">Sua senha:</label>
            <input type="password" name="password" id="password" placeholder="Digite sua senha">
        </p>
```

  * No input acima tratamos de uma senha, portanto e de suma importancia que coloquemos o type "password" para assim oque for digitado pelo usuario fique "escondido" ao inves de sua senha real ser mostrada diante de seu navegador.

-`<Input de range>`

```html
      <!-- Input de range -->
        <p>
            <label for="range">Range: </label>
            <input type="range" list="tickmarks" name="range" id="range">
            <datalist id="tickmarks">
                <option value="0" label="0%"></option>
                <option value="10"></option>
                <option value="20"></option>
                <option value="30"></option>
                <option value="40"></option>
                <option value="50" label="50%"></option>
                <option value="60"></option>
                <option value="70"></option>
                <option value="80"></option>
                <option value="90"></option>
                <option value="100" label="100%"></option>
            </datalist>
        </p>
```

  * Input de range é algo que o meu navegador e outros não conseguem ainda renderizar com total precisão, porém estarei documentando-o mesmo assim.
  * Ele trata-se de uma datalist com diversas options para cobrir um "nivel / range". Passando do 0 ao 100 com valores entre tais numeros e exibindo apenas 0 , 50 e 100.

-`<Input de arquivo>`

```html
        <!-- Input de arquivo -->
        <p>
            <label for="foto">Sua foto:</label>
            <input type="file" name="foto" id="foto" accept=".png,.svg,image/*" multiple>
        </p>
```
  * No input acima colocamos o type arquivo para podermos filtrar diante de "accept", aceitando .pngs, .svgs e qualquer tipo de "image". Além disso aceitando multiplos arquivos.

-`<Input de numeros>`
```html
        <!-- Input de número delimitado por uma funcão -->
        <p>
            <label for="number">Number:</label>
            <input type="number" name="number" id="number" placeholder="Digite um número de 10 a 50" min="10" max="50" step="2">
        </p>
        
        <!-- Input de número descrito pelo usuario -->
        <p>
            <label for="number">Number:</label>
            <input type="number" name="number" id="number" placeholder="Digite qualquer numero">
        </p>
```

  * Em ambos os exemplos de input recebemos numeros, a diferenca está em como delimitamos. No exemplo UM delimitamos numeros de 10 a 50 e no exemplo dois aceitamos qualquer tipo de numero.

-`<Input de URL>`
```html
        <!-- Input de URL -->
        <p>
            <label for="url">Sua url:</label>
            <input type="url" name="url" id="url" placeholder="URL">
        </p>
```

  * No input acima fornecemos o type url para aceitar apenas URL'S.Novamente o navegador automaticamente trata a entrada de dados erradas por nós, porém poderiamos fazer isso tranquilamente com auxilio do back-end.

-`<Dropdown com opcões>`
```html
        <!-- Dropdown com opções -->
        <p>
            <label for="select">Selecione alguma opção:</label>
            <select name="select" id="select">
                <optgroup label="Teste UM">
                    <option value="qualquer-1" label="Valor 1"></option>
                    <option value="qualquer-2" label="Valor 2"></option>
                    <option value="qualquer-3" label="Valor 3"></option>
                    <option value="qualquer-4" label="Valor 4"></option>
                </optgroup>
            </select>
        </p>
```

  * No código acima nos oferecemos ao usuario escolher entre 4 opcões que estão dentro de uma de uma select, select essa que possui um grupo chamado teste UM e armazena qualquer 1 até 4.

-`<Área de texto>`
```html
        <!-- Área de texto -->
        <p>
        <div id="div-textArea">Digite o que achou do nosso site abaixo</div>
        <label for="textArea"></label>
        <textarea name="textArea" id="textArea" cols="30" rows="10" placeholder="Digite aqui"></textarea>
        </p>
```

  * No código acima nos passamos em uma div estilizada a frase "Digite oque achou do nosso site abaixo". E logo abaixo passamos uma area em texto para o usuário "livremente" escrever, claro se o mesmo quiser.
  * Com delimitacao de 30 colunas com 10 linhas o local é livre de escrita.

-`<Botões de Envio e Reset>`

```html
        <p>
            <button type="submit"> Enviar </button>
            <button type="reset"> Reset </button>
        </p>
```

  * Por mais que não sejam ferramentas de input DIRETO do usuario complementam este conteudo. Dois botões que se colocados dentro de `<form>` e passados como type submit e reset desempenharam tal atividade em nosso formulário.

<hr>

- Consideracões:
  * Todos os códigos foram desenvolvidos de forma em que todos estivessem dentro de `<form>` até o seu final `</form>`.
  * E claro todos estão sujeitos a melhorias com CSS e funcoes de back-end, este conteúdo é apenas o "esqueleto" de inputs web.