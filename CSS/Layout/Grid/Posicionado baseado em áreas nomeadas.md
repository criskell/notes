# Posicionamento baseado em áreas nomeadas

- Este tipo de posicionamento consiste em definir áreas nomeadas em que os itens irão preencher e então posicionar e dimensionar estas áreas no `grid-template-areas`.

## Definindo uma área nomeada

- Para definir uma área nomeada, utilizamos a propriedade `grid-area` nos itens definida com um nome para esta área. E logo em seguida definimos o posicionamento desta área no `grid-template-areas`.
- Alternativamente, para definir uma área, podemos especificar todas as 4 linhas que delimitam tal área, ou definir o nome desta área nas propriedades `grid-column/row*`, por exemplo:
  - `grid-row: header -> grid-row-start: header; grid-row-end: header; (shorthand)`


## Modelo de áreas

- Para definir o posicionamento das áreas especificadas com `grid-area`, a propriedade `grid-template-areas` é utilizada.
- Podemos deixar células vazias com `.`, e podemos repetir este `.` de forma que seja somente uma célula, contanto que não colocamos espaço em branco.
- É possível utilizar espaço em branco extra para alinhar as colunas no **valor**.
- As áreas especificadas devem ser retangulares.
- Em cada linha deve haver o mesmo número de células.

## Linhas e áreas nomeadas implícitas

- Ao definir uma área nomeada, irá ser criadas **linhas implícitas de grade** para cada borda desta área, com o nome da área + sufixo `-start` e `-end`, inversamente, ao definir as lines, por exemplo, na hora de definir colunas e linhas, irá ser criada uma **área de grade nomeada implícita**

## Exercícios

1. O que difere o posicionamento baseado em áreas nomeadas do posicionamento baseado em linhas?
2. O que a propriedade `grid-template-areas` especifica?
3. Quantas células serão criadas num container definido com `grid-template-areas: ". . ......... ..."`?
4. É permitido utilizar mais de um espaço para alinhar as colunas num `grid-template-areas`, fazendo uma espécie de arte ASCII?
5. O que a propriedade `grid-area` definida com um nome especifico? Qual é a diferença entre especificar linhas que delitam esta área?
6. Como funciona a shorthand `grid-template`?