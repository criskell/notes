# Gráficos vetoriais

## Tipos de imagens

- Imagens raster:
  - Definidas usando uma grade de pixels
  - Cada pixel possui uma posição exata e uma cor
- Imagens vetoriais:
  - Geradas por um algoritmo
  - Uma imagem vetorial contém informações de shape (forma) e caminho (path) para renderizar uma imagem
  - Não possui informações sobre cada pixel
  - SVG é um formato para gráficos vetoriais
- Exemplo:
  - A medida que uma imagem raster é ampliada, os pixels começam a aumentar de tamanho para preencher vários pixels na tela, ficando menos nítida
  - Já quando uma imagem vetorial é ampliada, ela irá parecer nítida, pois a imagem será gerada de acordo com o tamanho necessário exatamente na mesma forma

## SVG

- SVG é um formato para descrever imagens vetoriais
- Num arquivo SVG há formas e efeitos para aplicar nesta forma para exibir a imagem
- Vantagens:
  - Tem como colocar texto num SVG e se estiver utilizando SVG inline é possível ter mais SEO.
  - Cada componente da imagem pode ser manipulada por CSS ou JS, dependendo do tipo de carregamento do SVG (se for img, inline, etc.)

### Como incluir SVG

- Podemos incluir SVG utilizando um elemento `img` ou fundos CSS.
  - Prós:
    - Pode ser passível de cache
  - Contras:
    - Não pode ser manipulada via JS ou CSS fora do SVG
- Também podemos incluir SVG inline, cujo código estará diretamente no HTML.
  - Prós:
    - Permite manipular via CSS ou JS
    - Podemos utilizar pseudo-classes e animações CSS em SVG
  - Contras:
    - Duplicidade de código, como estilos CSS inline
    - Não permite fazer cache da imagem
- Até dá para incluir via `iframe`, visto que SVG pode ser visto como uma página num navegador web

## Exercícios

1. O que são imagens raster e o que são imagens vetoriais? Se eu ampliar uma imagem raster e uma imagem vetorial, o que irá acontecer com as duas?
2. O que é o formato SVG, como funciona de forma simplificada e quais as vantagens de utilizar SVG?
3. Quais são as 4 formas de adicionar SVG?
