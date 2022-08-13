# Media queries

- Media queries aplica um conjunto de regras CSS se uma *regra* sobre o ambiente o qual a página é renderizada **corresponde**.

## Sintaxe básica

- Consiste em `@media`, seguido opcionalmente de um *tipo de mídia*, e regras sobre *recursos de mídia*.

## Tipos de mídias

- Tipos de mídias para aplicar regras CSS:
  - `all`
  - `screen`
  - `print`

## Recursos de mídia

- Numa consulta de mídia, podemos escrever regras sobre *media features*.
- Algumas media features:

### *-width, *-height

- Para aplicar CSS conforme as dimensões do dispositivo, utilize `width` e `height`.
- Para aplicar de acordo com uma *faixa* de dimensionamento, utilize `min/max`

### hover

- Se o usuário pode **pairar** (ex.: passar o mouse encima) sobre elementos.
- Exemplos: `@media all (hover: hover)`

### pointer

- É sobre o tipo de dispositivo que pode apontar.
- Valores:
  - `none`: Não há dispositivo para apontar elementos.
  - `coarse`: O dispositivo é de um tipo mais "grosso" e menos preciso, como uma tela touchscreen
  - `fine`: O dispositivo é de um tipo mais "preciso" e menos "grosso", como um trackpad ou mouse

### orientation

- Orientação do dispositivo: (paisagem/retrato).
- Valores:
  - `landscape`
  - `portrait`

## AND, OR e NOT

- Para combinar regras sobre recursos de mídia (ou então combinar com o tipo de mídia), utilize o "conectivo" `and`.
- Para fornecer um conjunto de consultas, utilize `,`, onde as regras serão aplicadas se *qualquer* consulta seja atendida.
  - Exemplos:
    - `@media screen and (max-width: 200px), print and (max-width: 200pt)`: As regras desta consulta serão aplicadas somente se:
      - a mídia de saída for do tipo `screen` E tiver uma largura no máximo de `200px` OU
      - a mídia de saída for do tipo `print` E tiver uma largura de no máximo `200pt`
- Para negar uma consulta de mídia, utilize `not`.
  - Exemplos:
    - `@media not (max-width: 200px)`. Esta consulta será atendida somente se o dispositivo possuir uma largura máxima que `200px`.

## Breakpoints

- Breakpoint é o ponto no qual um layout começa a ser alterado por uma media query.
- Para escolher breakpoints, podemos utilizar o devtools e ir dimensionando a viewport até que o conteúdo começa a ficar ruim, e então devemos incluir um breakpoint.
- Mobile-first design é uma forma de design responsivo para a web que consiste em começar com uma pequena visualização e então ir adicionando mais estrutura ao site.
- Desktop-first design é uma forma de design responsivo que consiste em começar em uma largura mais ampla e ir adicionando breakpoints à medida que diminuímos a viewport no devtools.

## Alternativas

- As alternativas para as consultas de mídia é utilizar tecnologias como Grid, Flex e Multicol, que cria um layout flexível e responsivo.
- Podemos isso com media queries.

## meta: viewport

- Este tipo de *metatag* configura a viewport.
- `<meta name="viewport" content="width=device-width, initial-scale=1">`:
  - Define a largura da viewport para a largura real do dispositivo. Os dispositivos costumam mentir sobre a largura da viewport, para por exemplo: `960px`. Isso é bom para sites não responsivos (sites não responsivos ficam muito ruim se a viewport fosse menor), mas ruim para sites responsivos.
  - Define o zoom inicial como `1`.

## Exercícios

1. O que são media queries?
2. O que são breakpoints e quando devo incluir eles?
3. Qual é a diferença entre desktop-first design e mobile-first design?
4. O que o elemento `<meta name="viewport" content="width=device-width, initial-scale=1">` faz?
5. Explique os recursos de mídia (media features) `orientation` (2 valores), `pointer` (3 valores), `hover` (1 valor), `width/height/min-width/max-width/min-height/max-height`.
6. Dado as consultas de mídia `@media (min-width: 300px)`, `@media (max-width: 500px)`, como fazer para combinar-los?
7. Como utilizar uma lógica "OU" nas consultas de mídia.
8. Quais são os tipos de mídia existentes que podemos utilizar em media queries? É obrigatório emitir? O que acontece se omitir?