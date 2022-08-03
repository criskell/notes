# Itens

## Posicionamento

### Lines

- `grid-[row/column]-[start-end]`:
  - Determina a line de linha e coluna de início e fim.
  - Valores:
    - Número da linha
    - Nome da linha
    - `span <numero>`: Irá expandir por `<numero>` faixas
    - `span <nome>`: Irá expandir até a próxima line com o nome `<nome>`
    - `auto`: Algoritmo de posicionamento automático / Irá preencher apenas 1 faixa
  - Se `*-end` não for especificado, assumimos `span 1`
  - Shorthand:
    - `grid-column/row`:
      - `inicio / fim`

## Áreas

- `grid-area`:
  - Permite especificar um nome para o item
  - Ou, é uma shorthand: `grid-row-start / grid-column-start / grid-row-end / grid-column-end`

## Alinhamento

- `justify-self`:
  - Alinha um item em sua própria célula ao longo do eixo inline.
  - Aceita os mesmos valores que `justify-items`
- `align-self`:
  - Alinha um item em sua própria célula ao longo do eixo de bloco.
  - Aceita os mesmos valores que `align-items`
- `place-self`:
  - Shorthand para `<align-self> <justify-self>`