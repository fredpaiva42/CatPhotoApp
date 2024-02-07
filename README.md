# Dicionário de HTML

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