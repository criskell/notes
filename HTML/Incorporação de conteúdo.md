# Incorporação de conteúdo

- Os elementos `iframe`, `object` e `embed` permitem incorporar conteúdo em páginas web.

## História

- No início da web era comum utilizar frames e framesets para criar sites
  - frames são partes do site que são carregadas num frameset
  - um frameset permite dizer como e onde irá ficar cada quadro na página
- Mais tarde surgiram o Flash e o Java Applets, que permitem incorporar conteúdo rico numa página como vídeos, animações e PDFs, através de elementos como `object` e `embed`
- Mas isso gerou muitos problemas e agora as formas de incorporar conteúdo é com elementos com `iframe`, `video` e `canvas`

## iframes

- São elementos que permitem incorporar *documentos* ao documento atual.
- Atributos:
  - `src`: URL que aponta para o documento.
  - `width / height`: Definem o tamanho do `iframe`
  - `allowfullscreen`: Permite que o `iframe` entre em tela cheia via a *API Fullscreen*.
  - `sandbox`: Habilita configurações de segurança altas.
- É permitido utilizar um conteúdo fallback dentro do elemento, para mostrar caso o navegador não suporte o elemento `iframe`.
- Uma borda é mostrada por padrão em navegadores em `iframe`, podemos desativar com CSS.
- É recomendado definir o atributo `src` via JS para diminuir o tempo de carregamento "oficial" da página.

### Segurança

- Iframes é um vetor de ataque comum em páginas web
- Clickjacking é uma técnica onde pessoas ruins tentam incorporar um documento malicioso ao seu site (ou o contrário) por meio de um iframe invisível para roubar dados.
- Recomendações:
  - Incorporar outros documentos somente quando seja extremamente necessário.
  - Usar HTTPS:
    - Reduz a adulteração do conteúdo
    - Previne que iframes acessem o conteúdo pai e vice-versa
  - Usar o atributo `sandbox`:
    - Sandbox é um "container" que executa código sem que ele afete a base de código principal
    - O atributo `sandbox` serve para impor restrições.
  - Utilizar diretivas CSP:
    - CSP significa política de segurança de conteúdo
    - Fornece um conjunto de cabeçalhos para proteger o site
    - Configurar `X-Frame-Options` para `DENY`, para previnir que o site site seja incorporado

## object e embed

- São elementos de uso geral para incorporar conteúdo como PDFs para ser usados por, por exemplo, plugins.

- `embed`:

  - `src`: URL para o conteúdo externo.
  - `width / height`: Tamanho da caixa para ser controlada por um plugin.
  - `type`: Tipo MIME do conteúdo.
  - Parâmetros para o plugin são passados via atributos.
  - Conteúdo fallback não suportado

- `object`

  - `data`: URL para o conteúdo externo.

  - `width / height`: Tamanho da caixa controlada por um plugin.

  - `type`: Tipo MIME do conteúdo.

  - Parâmetros para alimentar o plugin são fornecidos via elementos `param` (obsoleto)

  - Conteúdo fallback depois do param.

  - Incorporar um PDF:

    ```html
    <object
            data="URL DO PDF AQUI"
            type="application/pdf"
            width="800"
            height="200">
        <p>
            Você não possui um plug-in para ler PDFs. É possível <a href="URL DO PDF AQUI" download="URL PARA SALVAR ">baixar este PDF (10mb)</a>.
        </p>
    </object>
    ```

## Exercícios


1. Quais são os elementos que permitem incorporar conteúdos mais gerais?
2. Para agrupar `iframe` utilizamos um *frameset*, onde cada *iframe* é chamado de *frame*. Tal afirmação é verdadeira ou falsa? Por que?
3. Em relação ao HTML5, a incorporação de conteúdo atingiu outro nível, de que forma e como era antes do HTML5?
4. Qual é o objetivo primordial de iframes?
5. Um cliente quer incorporar um documento apontado pela URL https://exemplo.com em sua página web utilizando apenas HTML com tamanho 800 por 500 e que seja permitido habilitar o modo de exibição em tela cheia utilizando a API *Fullscreen*, além disso, deve impor várias configurações de segurança e exibir um conteúdo de *fallback*. Qual elemento deve utilizar e com quais atributos e com qual conteúdo?
6. Por que não é recomendado configurar o atributo `src` no HTML?
7. O que é CSP?
8. O que é clickjacking?
9. Cite 4 dicas de segurança para Iframe.
10. O que o cabeçalho `X-Header-Options: DENY` faz?
11. Com qual elemento podemos incorporar um PDF e quais são os elementos de uso geral além do `iframe` para incorporação de conteúdo?
12. O que é sandbox e o que o atributo `sandbox` faz em elementos `iframe`?
13. Por que utilizar HTTPs ao utilizar iframes? Reduzir a adulteração de conteúdos, talvez?
14. Como configurar um `object` para apontar para a URL `https://exemplo.com`?
15. O que o elemento `param` faz?