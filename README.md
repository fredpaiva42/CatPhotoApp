# Dicionário de HTML
## Resultado
![Resultado Final da Página](./Resultado%20Final.jpeg)
## Tag Doctype
- Todas as páginas devem começar com `<!DOCTYPE html>`. Essa string especial é conhecida como uma declaração e garante que o navegador tentará atender às especificações gerais do setor.

## Tag head
- Armazena informações adicionais do site.
- Como a tag `title` que determina o que os navegadores mostrarão na barra de título ou na aba da página.

## Tag meta
- Podemos definir o comportamento do navegador adicionando elementos meta de autofechamento em head. 
```html
<meta charset="UTF-8">
```
- Esse meta informa ao navegador para colocar a marcação em diversos idiomas.
## Tag body
- Todos os elementos de conteúdo da página que devem ser renderizados na página ficam dentro da tag `body`

## Tags de Titulo
- Vão de **h1 a h6**, quanto **menor for seu número** mais **importante** o título é.
- Quando adicionamos um elemento de **título menor** à página, é implícito que estamos **iniciando uma nova subseção**.
```html
<h1>Título principal</h1>
```

## Tag p
- É usada para criar um parágrafo de texto.
```html
<p>Parágrafo</p>
```

## Tag Main
- É responsável por identificar a seção principal do site, muito importante para acessibilidade e SEO.
- **Tag semântica**
```HTML
<main>
    <!--Conteúdo principal-->
</main>
```

## Aninhamento
- Ou **indentação**, é usado para facilitar a leitura do HTML.
- Elementos aninhados (filhos) devem ser colocados dois espaços mais à direita do elemento pai.
```HTML
<!--Elemento pai-->
<main> 
<!--Elementos filhos-->
    <h1></h1>
    <h2></h2>
</main>
```

## Tag img
- Permite que adicionemos imagens ao site.
- Não possui tag de fechamento, esse tipo de tag é conhecida como tag de **fechamento automático.**
- Ela possui dois **atributos** (palavras especiais que controlam o comportamento da Tag), `src` que especifica o **(URL)** onde a imagem está localizada e `alt` que serve para descrição da imagem.
- T**odos os elementos img devem ter um atributo alt**. Ele é usado por leitores de tela para melhorar a acessibilidade e exibido quando a imagem não pode ser carregada.
```HTML
<img src="" alt="">
```

## Tag a
- Serve para fazer **linkar** outra página.
- Possui o atributo `href`, onde colocamos o link da página que queremos redirecionar.
- Qualquer texto/imagem pode ser transformado em link.
- Outro atributo importante da tag a é o `target`, e define o que acontece quando **clicamos** no link:
  - `_blank`: O link é aberto em uma **nova janela ou guia** do navegador.
  - `_self`: O link é aberto na **mesma janela ou guia** em que o link foi clicado. Este é o **padrão**.
  - `_parent`: O link é aberto na **janela pai** da **janela atual**, útil quando se trabalha com **frames**.
  - `_top`: O link é aberto na **janela superior (removendo todos os frames, se houver)**.
```HTML
<a href="https://google.com">google</a>
```

## Tag section
- Permite **separar** os conteúdos em **seções** ou **grupos temáticos**.
- Ajuda a **estruturar e organizar** o conteúdo, **melhora a acessibilidade** e **facilita a leitura** do código.
- É uma **tag semântica**.

## Listas
- `ul` é a tag de **listas não ordenas**.
- Para **criar** um **elemento da lista** é necessário usar a tag `li`.
- `ol` é a tag de **listas ordenadas**.
```html
<!-- Exemplo de Lista não Ordenada -->
<ul>
    <li>Arroz</li>
    <li>Feijão</li>
</ul>
<!-- Exemplo de Lista Ordenada -->
<ol>
    <li>Pegar o pote</li>
    <li>Abrir a tampa</li>
    <li>Pegar a faca</li>
    <li>...</li>
</ol>
```

## Tag figure
- Representa um conteúdo **auto-contido** e permite que associemos uma imagem com uma legendo, por exemplo.
- É usado para **encapsular** qualquer conteúdo que seja **referenciado** de **maneira isolada** do texto principal, como **imagens, gráficos, etc.**
- Para **adicionar legenda** devemos usar a tag `figcaption` dentro da tag `figure`, é nela que vamos escrever a legenda propríamente dita.
```html
<!-- Adiciona a legenda "Este é o logo do site" -->
<figure>
    <img src="" alt="Logo do site">
    <figcaption>Este é o logo do site</figcaption>
</figure>
```

## Tag em
- Serve para **enfatizar** um texto ou palavra, colocando o texto **itálico**.
```html
Texto que vai ser <em>destacado</em>.
```

## Tag strong
- Usamos para indicar que algum texto é de grande *importância ou urgência**. Deixando o texto em **negrito**.

## Tag footer
- Serve para adicionarmos uma seção de **rodapé** à página.

## Formulários
- Para usarmos um formulário na nossa página usamos a tag `form`.
- Dentro da tag `form` temos um atributo `action`, este atributo indica para onde os dados do formulário devem ser enviados.
```html
<form action="/submit-url"></form>
```
- No exemplo acima, o atributo `action` indica que os dados devem ser enviados para `/sumbit-url`.

## Tag input
- Para fazermos a **coleta dos dados**, devemos usar a tag `input`, ela é uma tag de **fechamento automático** e pertime várias maneiras de coletar dados a partir de um formulário da web.
- A tag `input` possui o atributo `type` que nos permite especificar qual tipo de entrada vamos usar. Podemos criar campos de senha, e-mail, de redefinição e muito mais.
  - `text`: entrada do tipo texto;
  - `radio`: entrada de seleção de opção.
    - Para indicar que apenas uma opção pode ser escolhida, precisamos adicionar um atributo `name` em todas as opções e o atributo deve ter o mesmo valor para todas as oções.
    - Os dados do formulário para opções são baseados em seus atributos `name` e `value`. Caso as opções não tenham o atributo `value`, os dados do formulário incluirão `name=on`, o que não é útil quando temos vários botões. Então uma sugestão é usar um `value` com o mesmo valor do `id`.
  - `checkbox`: entrada de seleção para perguntas que tem mais de uma opção.
    - Para que uma caixa de seleção esteja selecionada como padrão, é necessário adicionar o atributo `checked`.
- Para que os dados de um formulário sejam acessados pelo local especificado pelo atributo `action`, é necessário dar ao campo de texto um atributo `name` e atribuir um valor que represente os dados que estão sendo enviados.
- Também temos o atributo `placeholder` que é usado para dar às pessoas uma dica sobre o tipo de informação que deve ser inserido em uma entrada (input).
- Para **impedir que o usuário envie informções faltando**, podemos usar o atributo `required` a uma tag `input`. Este atributo não possui valor.
```html
<input action="text" name="email" placeholder="Email address" required>
```
## Tag button
- Como o próprio nome diz, permite criar um **botão clicável**.
- Assim como o elemento `input`, `button` é um **elemento em linha** (inline), que não aparecem em novas linhas.
- É uma boa prática adicionar o atributo `type` ao `button`, para garantir que ele vai executar a ação correta.
```html
<button type="submit">Submit</button>
```

## Tag label
- **Ajuda a associar o texto** de um elemento `input` ao próprio elemento, serve especialmente para tecnologias assistivas como leitores de tela.
```html
<label><input type="radio">Cat</label>
```
- Outra opção é colocar o texto dentro de uma tag `label` e adicionar um atributo `for` com o mesmo valor do `id` do elemento `input`.
```html
<input type="radio" id="cat">
<label for="cat">Cat</label>
```
## Atributo id
- Serve para **identificar elementos HTML específicos**. Seu valor deve ser **único** para a página inteira.

## Tag fieldset
- Usado para agrupar entradas (inputs) e rótulos (labels) relacionado em um formulário da web. Os elementos `fieldset` são **elementos de nível de bloco**, o que significa que eles aparecem em uma nova linha.

## Tag legend
- Atua como uma legenda para o conteúdo do `fieldset`. Dá ao usuário um contexto sobre o que devem inserir nessa parte do formulário.