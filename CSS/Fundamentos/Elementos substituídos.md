# Elementos substituídos

- Elementos cujo conteúdo está fora do escopo do modelo de formatação do CSS.
- O conteúdo será substituído na fase de *preparação* do documento.
- Propriedades que manipulam o objeto de um elemento substituído na caixa de conteúdo:
  - `object-fit`
  - `object-position`
- Possuem um aspect ratio (proporção).
- Exibido com suas dimensões intrínsicas, por padrão.
- `max-width: 100%` em replaced elements: A imagem ficará menor proporcionalmente se as dimensões intrínsicas ultrapassarem a largura do container. 

## Dimensionamento

- A largura e altura especificados para uma imagem devem atender a proporção da imagem, caso contrário ela será comprimida ou esticada.
- A propriedade `object-fit` especifica como o conteúdo de um elemento substituído como imagens devem ser redimensionado para preencher um container. Possíveis valores:
  - `fill`:
    - A imagem será redimensionada para se encaixar na proporção do container
    - Se as proporções não corresponderem, ela será esticada ou comprimida
  - `contain`:
    - A imagem será redimensionada de acordo com a proporção do container. Se as proporções não corresponderem, a imagem será colocada numa espécie de letterbox.
    - A imagem inteira será colocada
  - `cover`:
    - A imagem será redimensionada para se encaixar na proporção do container. Se as proporções não corresponderem, a imagem será cortada para encaixar.
    - Preserva a proporção da imagem
  - `none`:
    - A imagem não será redimensionada, comprimida nem esticada
    - Não respeita a proporção do container

## Posicionamento

- A propriedade `object-position` especifica como o conteúdo de um elemento substituído deve ser posicionado na caixa do elemento.
- As áreas que não foram cobertas pelo objeto mostram o plano de fundo de um elemento, ou seja, é possível definir um plano de fundo num elemento de imagem.
- Recebe como valor um conjunto de valores que definem a posição 2D.
- Se comporta como a propriedade `background-position`

## Exercícios

1. O que são elementos substituídos e por que são chamados de "substituídos"?
2. O que a propriedade `object-fit` e `object-position` faz?
3. Quais são os valores da propriedade `object-fit`?