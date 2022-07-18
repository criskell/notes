# Propriedades lógicas

- As propriedades lógicas permitem o controle do layout por meio de mapeamentos lógicos de dimensão e direção
- Enquanto as propriedades físicas relacionam com o monitor, as propriedades e valores lógicos se relacionam com o fluxo de texto
- A especificação introduz mapeamentos de propriedades físicas para as suas contrapartes lógicas/relativas ao fluxo, ou seja, que dependem do modo de escrita e da direção de texto.
- Vantagens:
  - Ao utilizar propriedades lógicas para, por exemplo, margens, as regras de margens são persistidas, independente do idioma e direção do texto

## Terminologia

- Dimensão de bloco:
  - Dimensão perpendicular ao fluxo de texto numa linha.
  - Direção na qual os blocos como parágrafos fluem um após o outro.
- Dimensão inline:
  - Dimensão paralela ao fluxo de texto numa linha.
  - Dimensão na qual uma linha de texto é disposta.
- Fluxo de bloco:
  - Direção em que os blocos são empilhados.
  - A direção em que os parágrafos progridem.
- Fluxo inline:
  - É como o texto flui em uma frase (por exemplo, em `pt`, é da esquerda para a direita)
  - Alteramos a direção utilizando a propriedade `writing-mode`

## Dimensionamento

- Equivalência de propriedades relativas ao fluxo de texto:
  - `[(max|min)-](width|height)` -> `[(max|min)-](inline-size|block-size)`

## Início e fim

- `start` e `end`, que resultam em `block-start`, `block-end`, `inline-start`, `inline-end`

## Posicionamento e espaçamento

- (padding|margin)-(block|inline)[-(start|end)]
- inset-(block|inline)[-(start|end)] (equivalente as propriedades de deslocamento)

## Bordas

- `border-(inline|block)-(start|end)`
- `border-(start|end)<block>-(start|end)<inline>-radius`

## Unidades

- `vh` <-> `vb`
- `vw` <-> `vi`