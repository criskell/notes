# Container

- A estrutura de um grid é definida no container, já o posicionamento de elementos filhos serão definidos neles.
- Um container é definido declarando `display: grid`
  - Isto cria um novo contexto de formatação de grid para filhos diretos
  - Os elementos filhos agora serão dispostos numa **grade**

## Dimensionamento

### Grid implícita

- `grid-auto-rows/columns`:
  - Especifica o tamanho das tracks implícitas criadas quando não há células para acomodar um item, quando posiciona um item fora da grade explícita e etc.

## Posicionamento

### Automático

- O algoritmo de posicionamento automático coloca os itens na grade automaticamente.
- `grid-auto-flow`:
  - Controla como o algoritmo de posicionamento automático trabalha.
  - `row` (padrão):
    - O algoritmo irá preencher as linhas primeiro.
  - `column` (padrão):
    - O algoritmo irá preencher as linhas primeiro.

## Áreas

### grid-template-areas

- Especifica um modelo de grade.
- Este modelo de grade é composta por strings, onde cada string é uma linha.
- Em cada linha, há um nome de uma área e repetir este nome faz com que esta área se expanda por várias células.
- Um ponto significa uma célula vazia.
- Ao definir uma área utilizando isso, a row line inicial e a column line inicial será chamada `<area>-start` e a row line final e a column line final será `<area>-end`.

### grid-template

- Shorthand para `grid-template-columns`, `grid-template-rows` e `grid-template-areas`.
- Valores:
  - `none`
  - Dois valores: `<grid-template-rows> / <grid-template-columns>`
  - Três valores:
    - Definimos uma barra.
    - Depois da barra, fica as colunas
    - Antes da barra, fica as áreas e linhas, com 1 ou mais ocorrências de uma linha com esta sintaxe:
      - Nome da line inicial da linha
      - String que nem o `grid-template-areas`
      - Tamanho da linha
      - Nome da line final da linha, que será a mesma  que a line inicial da posterior.

## Gutters

- A propriedade `gap/column-gap/row-gap/grid-column-gap/grid-gap/grid-row-gap` cria uma gutter entre linhas/colunas.

## Alinhamento

- `place-items`:
  - shorthand
  - `align-items justify-items`
- `place-content`:
  - shorthand
  - `align-content justify-content`

### Eixo inline

- `justify-items`:
  - Alinha os itens ao longo do eixo inline (dentro de suas colunas).
  - Valores:
    - `start`: Os itens são alinhados ao início da célula
    - `end`
    - `center`
    - `stretch`: Os itens esticam.
- `justify-content`:
  - Alinha a grid (colunas) dentro do container, caso haja espaço disponível, ao longo do eixo inline.
  - Valores:
    - `start`: Alinha a grid ao início.
    - `end`: Alinha a grid ao fim.
    - `center`: Alinha a grid ao centro do container.
    - `space-between`: Haverá um espaço uniforme entre cada item, mas não nas extremidades
    - `space-around`: Haverá um espaço uniforme ao redor de cada item, com as extremidades com metade do tamanho
    - `space-evenly`: Haverá um espaço uniforme entre cada item, até nas extremidades
    - `stretch`: Redimensionam os itens para que ocupam todo o container.

### Eixo block

- `align-items`:
  - Alinha os itens ao longo do eixo de bloco.
  - Valores:
    - `start`
    - `end`
    - `center`
    - `stretch`: preenche toda a altura da **célula**
- `justify-content`:
  - Alinha a grid dentro do container, caso haja espaço disponível, ao longo do eixo de bloco.
  - Valores:
    - `start`: Alinha a grid ao início.
    - `end`: Alinha a grid ao fim.
    - `center`: Alinha a grid ao centro do container no eixo de bloco.
    - `space-between`: Haverá um espaço uniforme entre cada item, mas não nas extremidades
    - `space-around`: Haverá um espaço uniforme ao redor de cada item, com as extremidades com metade do tamanho
    - `space-evenly`: Haverá um espaço uniforme entre cada item, até nas extremidades
    - `stretch`: Redimensionam os itens para que ocupam toda a altura do container.