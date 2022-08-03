# Conceitos básicos

## O que é CSS Grid Layout

- O **CSS Grid Layout** é um sistema de layout baseado em grade com duas dimensões.

### Por que CSS Grid Layout?

- Diferentemente do Flexbox, o fluxo é baseado em duas direções.
- Permite um dimensionamento fixo e flexível de tracks
- É possível colocar itens numa posição explícita
- Alinhar itens numa área ou a grid inteira

## Modelo de um Grid

- Grid: É conjunto de lines que se intersectam formando rows e columns.
- Container: Contém items + estabalece um contexto de formatação de grid + recebeu `display: grid`.
- Item: Filhos diretos de um container.
- Track: Espaço entre duas *lines* adjacentes.
- Line: Linha que divide o container. Tipos: *row* e *column*
- Area: Um ou mais grid cells. Precisa ser retangulares.
- Cell:
  - Menor unidade em um container criada com a intersecção de quatro lines.
  - Cada item está contido em células.

## Grid explícita e implícita

- Grid explícita:
  - Faixas criadas com `grid-template-rows/columns`
  - O posicionamento e a presença dos itens são previsíveis.
- Grid implícita:
  - Faixas criadas quando algo é colocado fora da grade definida ou devido à quantidade de conteúdo, assim cria as faixas necessárias.
  - O tamanho das faixas na grade implícita são controladas por `grid-auto-columns/rows`
  - O posicionamento e a presença dos itens são impresíveis.

## Containers

- Como criar um container para um grid? `display: grid`
- Por padrão irá ser criado um grid com apenas uma faixa de coluna.

### Alinhamento

- Alinhando itens

## Lines

- Utilizamos linhas para posicionar itens.
- Por padrão, as linhas são numeradas de 1 à N. A primeira linha depende do modo de escrita.

## Células

- Célula é a menor unidade de um Grid.
- Cada item irá ficar em células.

## Áreas

- Uma área é definida quando itens abrangem mais de uma célula por coluna ou linha.

### grid-template-areas e grid-area

- `grid-template-areas` permite definir áreas.
- `grid-area` permite definir em qual área um item irá ficar.

## grid-template-rows/columns

- Especifica as faixas de linhas/colunas.
- Ao misturar faixas com tamanhos absolutos e flexíveis, o tamanho absoluto é retirado do espaço disponível e o espaço disponível restante é distribuído proporcionalmente para cada faixa.

## Posicionamento

## Baseado em linha

- Neste tipo de posicionamento, direcionamos linhas.
- Para definir o posicionamento em rows a partir de line rows:
  - `grid-row-start`
  - `grid-row-end` (opcional, vai até a próxima linha de linha)
- Para definir o posicionamento em colunas a partir de column rows:
  - `grid-column-start`
  - `grid-column-end` (opcional, vai até a próxima linha de coluna)
- Shorthand:
  - `grid-column: grid-column-start / grid-column-end`
  - `grid-row: grid-row-start / grid-row-end`

## Gutters

- Gutters são espaçamento entre linhas e colunas.
- São contabilizados antes da distribuiçõ de espaço para as faixas flexúveis criadas com `fr`.

## Unidade fr

Representa uma fração do espaço disponível.

## Função repeat

`repeat(n, listagem de faixas)`: repete `listagem de faixas` `n` vezes.

## Função minmax

`minmax(a, b)`: Terá no mínimo A e no máximo B.

Usar `auto` em `b` significa usar o conteúdo e irá se referir ao item mais alto numa célula na linha atual.

## Materiais

- [ ] [Complete Guide Grid - CSSTricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
  - Parei no `grid-template`
- [x] [Basic Concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [x] https://www.treinaweb.com.br/blog/css-grid-um-guia-interativo-parte-1-containers