# Posicionamento baseado em linhas

- Este método consiste em posicionar itens em áreas definidas explicitamente por linhas.
- Itens que não são posicionados na Grid, são posicionados automaticamente pelo *algoritmo de posicionamento automático*.
- Cada line é indexada a partir de 1 e se relaciona com o modo de escrita.

## Posicionando itens via linhas

- `grid-[row|column]-start / grid-[row|column]-end`:
  - Define a linha de coluna/linha inicial e a linha de coluna/linha final.
  - Se não especificar a linha final, irá abranger apenas uma track.
- `grid-(row|column)`:
  - Shorthand
  - um valor = `start`, abrange apenas uma faixa.
  - dois valores = `start / end`
- `span n`:
  - Ao utilizar no `end`, quantas linhas estenderá a partir do início.

### grid-area

- `grid-area` permite definir a área de um item através da identificação das lines.
  - `grid-row-start`
  - `grid-column-start`
  - `grid-row-end`
  - `grid-column-end`

## Gutters

- Gutters são espaçamentos entre tracks
- Especificados pelas propriedades `gap, row-gap, column-gap`
- `gap` é shorthand
  - um valor = para todos
  - dois valores = linha, coluna
- Ao posicionar itens via linhas, podemos pensar que cada gap estendesse o tamanho da linha, e um item que começa numa linha, começa depois deste espaço.

## span

- `span n`: irá abranger `n` trilhas.

## Exercícios

1. Como posicionar um elemento por linhas através do `grid-area` e sem ele?
2. O que são gutters?
3. Num container com duas colunas e duas linhas, foi configurado um gap de 20px entre colunas e linhas. Quero posicionar um elemento para que começe depois do primeiro gap entre colunas e abranja somente uma faixa de coluna. Como fazer isso utilizando a shorthand `grid-column`?
4. As linhas que dividem a grid em linhas e colunas, são indexadas a partir de 0 ou 1?
5. Como fazer com que um item começando na linha de coluna 1 abranja duas colunas utilizando `span`?