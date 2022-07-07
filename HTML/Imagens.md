# Imagens

- `img` é para incorporar imagens

- atributos:

  - `title`:
    - texto de suporte para a imagem/título ao alvo
    - não é tão recomendado por causa da inconsistência em leitores de tela, e usuários sem mouse não podem ver
    - alternativa: um texto de suporte diretamente no texto ao redor
  - `width / height`:
    - não é recomendado alterar o tamanho via HTML
    - é recomendado via css
    - use um editor de imagens para colocar no tamanho correto
  - `src`:
    - URL relativa ou absoluta
    - hotlinking é você linkar uma imagem de outro servidor
    - escolha um bom nome para o arquivo (seo)
  - `alt`:
    - breve descrição da imagem
    - casos de uso:
      - quando a imagem não pode ser exibida
      - quando o usuário está utilizando um leitor de tela
      - seo

  ## Texto alternativo

  - O que colocar depende do motivo da imagem:
    - Decoração? é recomendado utilizar planos de fundos CSS para isso. mas, neste caso, utilize `alt=""`
    - Informações?
      - Se a imagem tiver informações significativas, coloque-as essas informações de uma forma breve. Ou então utilize o texto principal
      - Não escreva textos redundantes
    - Links? Utilize um texto de link acessível
    - Texto? Evite colocar textos na imagem. Neste caso, coloque no atributo `alt`

## Figuras

- `figure`
  - representa uma unidade de conteúdo
    - autocontida
    - informação numa forma compacta e fácil
    - pode ir em outros lugares (como um apêndice e outra página), independente do fluxo principal, ou seja, sem afetar ele, se removida
    - informações essenciais que suportam o texto principal
    - referenciada como uma única unidade
  - casos de uso
    - imagens
    - diagramas
    - códigos de exemplo
    - ilustrações
    - fotos
  - autocontida:
    - independente do contexto ao redor
- `figcaption`:
  - descreve o outro conteúdo da `figure`

## Backgrounds vs <img>

- Use o `<img>` quando uma imagem tem um significado, em termos de conteúdo
- use CSS quando é apenas decoração