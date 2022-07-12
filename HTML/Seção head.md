# head

- O head é a parte que não é exibida para o usuário que contém metadados do documento.
- Títulos:
  - O elemento `title` representa o título do documento.
- Metadados:
  - Dados que descrevem dados.
  - Criados utilizando o elemento `meta`, que representam metadados que não podem ser representados de outra forma (`<title>`, `<link>`, `<script>` e etc).
  - Atributos do elemento `meta`:
    - `charset`: Especifica a codificação de caracteres do documento (o conjunto de caracteres que o documento é permitido utilizar).
    - `name` e `content`:
      - `name`: Especifica o tipo do elemento meta.
      - `content`: O conteúdo meta.
  - `<meta name="description" content="descricao">`:
    - Contém a descrição do documento.
    - Adicionando a descrição com palavras-chaves, pode ajudar no SEO do site.
  - Outros tipos de metadados:
    - Alguns sites tem outros tipos de metadados que podem ser utilizados por outros sites (como redes sociais), por  exemplo:
    - OpenGraphData: Protocolo de metadados mais ricos para a web.
  - Ícones:
    - Temos diversos tipos, como favicons e ícones para dispositivos Apple.
    - Favicons:
      - São chamados assim devido ao seu uso na barra de favoritos
      - Ícones 16x16 que são utilizados na aba no navegador, barra de favoritos e etc.
      - `<link rel="icon" href="caminho.para.icone">`
- CSS:
  - Elemento `<link rel="stylesheet">`
- Scripts:
  - Elemento `script`.
  - Atributos:
    - `src`: Caminho para o script.
    - `defer`: Carrega o script depois que terminar de analisar o HTML.
- Linguagem primária do documento:
  - Atributo `lang` no elemento `html`: Altera a **linguagem primária do documento**, permitindo que a página seja indexada mais facilmente e ajudando na acessibilidade.
  - Podemos utilizar este atributo em outras partes do documento, para marcar diferentes conteúdos com uma linguagem diferente da principal.

## Elemento meta

- Representa metadados que não são representados por outros elementos.
- O tipo de metadado depende dos atributos:
  - Se definir `name`, será metadados em nível do documento
  - `http-equiv`:
    - é uma diretiva pragma, ou seja, fornece informações como cabeçalhos HTTP, mas com nomes um pouco diferentes
    - pode alterar o comportamento dos servidores e o navegador
  - `charset`, é uma declaração do charset
- Atributos:
  - `http-equiv`:
    - Define uma diretiva pragma.
    - Valores:
      - `content-type`: tipo mime + charset

## Perguntas de revisão

1. O que é o **head**?
2. O que são metadados?
3. O que é o elemento `meta`? Descreva os atributos `name`, `content` e `charset`.
4. Como alterar a linguagem primária do documento e por que mudar?
5. Como alterar a linguagem para diferentes seções do documento?
6. O que é o atributo `defer` e por que utilizar?
7. O que é o OpenGraphData e quais são seus casos de uso?
8. Cite 2 tipos de ícones que podemos adicionar em sites.
9. O que são favicons, como adicionar num site e por que são chamados assim?
10. Quais são os casos de uso do elemento `meta` para descrição?
11. Qual é a diferença do elemento `meta` para outros elementos como `title` e `link`?