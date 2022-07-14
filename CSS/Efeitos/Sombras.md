# Sombras

## box-shadow

- Cria uma sombra ao redor da caixa (ou dentro).
- A forma da sombra é afeta por propriedades como `border-radius`
- `inset`: uma palavra-chave para a sombra ficar para dentro
- Recebe 4 valores:
  - Deslocamento horizontal: se for positivo, irá ser empurrada da esquerda. caso seja negativa, irá ser empurrada da direita
  - Deslocamento vertical
  - Raio de desfoque (blur radius):
    - Quanto maior, mais borrada/desfalcada a sombra é
    - Quanto menor, mais nítida ela é
  - Raio de propagação (spread radius):
    - Especifica o tamanho da sombra
  - Cor
    - O padrão é do texto
- Pode receber mais sombras com `,`
- Se o container do elemento onde a sombra é aplicada possuir `overflow: hidden`, a sombra não sairá de dentro.

## Sombras em textos

- `text-shadow`
- É a mesma coisa que o `box-shadow`, mas não tem um valor `spread` e tão menos permite a palavra-chave `inset` e a sombra irá ser aplicada ao texto
- A sombra, diferente do `box-shadow`, não é recortado *ao redor da forma da caixa*, portanto, se o texto for transparante/semi transparante, a sombra irá aparecer sob ele

## drop-shadow

- É um filtro CSS que adiciona sombras às curvas de uma imagem recortada
- Filtros CSS permitem adicionar efeitos ao pixeis do elemento
- Tem os mesmos valores que `box-shadow`, mas não permite o valor `spread` e nem a palavra-chave inset.
- Permite várias sombras, através de várias funções na propriedade `filter`
  - As sombras são desenhadas a partir de um ponto de referência, que é a última sombra desenhada
