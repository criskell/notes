# Flexbox

- Flexbox é um método de layout unidimensional para organizar itens em linhas e colunas
- Itens são ditos flexíveis, ou seja, expandem ou encolhem para caber num certo espaço

## Por que usar

- distribuição de espaço e alinhamento de conteúdo
- a largura e altura se adaptar de acordo com o dispositivo de exibição
- o container esticar ou comprimir itens

- alinhamento de itens na horizontal ou vertical

## Modelo do Flexbox

### Eixos

- Os itens de um container flex são dispostos ao longo de dois eixos.
- O eixo principal percorre a direção na qual itens são colocadas e se estende na *dimensão principal*. O início deste eixo é chamado de *main start* e o fim é chamado de *main end*.
- O tamanho de um item ou container no eixo principal é chamado de *main size*. O tamanho de um item ou container no eixo transversal é chamado de *cross size*. Os tamanhos, respectivamente, podem serem definidos por *largura* ou *altura*, ou vice-versa, dependendo de qual é a direção do eixo principal.
- O eixo transversal percorre perpendicularmente ao eixo principal e se estende na *dimensão traversal*.
- Linhas flex são colocadas iniciando na *cross start* até a *cross end*.

## Linhas

- Linhas flex são linhas hipotéticas em que itens são colocados.
- Seguem o eixo principal e são empilhadas ao longo do eixo transversal.

## Flex container

-  É um elemento que recebeu um *tipo de exibição interna* como `flex` e tornou seus filhos diretos em caixas flexíveis.

### Fluxo de um container

- `flex-direction`:
  - Determina a direção em que o eixo principal percorre.
  - `row`:
    - Itens serão dispostos em linhas.
    - O eixo principal irá fluir na dimensão *inline*, com o *main start* localizado onde as frases começam no modo de escrita. Já o eixo transversal irá fluir na dimensão dos blocos.
    - São linhas com base no modo de escrita e direção do texto:
      - Por exemplo, ao utilizar o Inglês, um idioma com o modo de escrita horizontal da esquerda para a direita, a linha será horizontal com o `main-start` na esquerda pois é o lado em que as frases começam no inglês.
      - Já em idiomas verticais como Japonês, uma linha percorre verticalmente com `main-start` no topo.
  - `column`:
    - Itens serão dispostos em colunas.
    - O eixo principal irá fluir na dimensão dos blocos, com o *main start* localizado onde os blocos começam no modo de escrita. Já o eixo transversal irá fluir na dimensão inline.
  - `row-reverse`:
    - Igual ao `row`, mas na direção inversa.
    - O *main start* será a borda final do container.
  - `column-reverse`:
    - Igual ao `column`, mas na direção inversa
- `flex-wrap`
  - Controla se o container é de única linha ou de múltiplas linhas.
  - `nowrap`:
    - O container é de única linha
    - Os itens serão ajustados para caber em apenas uma única linha, sem ultrapassar a largura do container, caso não seja possível, ocorrerá um overflow.
  - `wrap`:
    - O container é de múltiplas linhas
    - Itens serão quebrados em novas linhas ao longo do eixo transversal se for necessário
  - `wrap-reverse`:
    - O mesmo acima, mas com as direções trocadas
- A propriedade `flex-flow` é uma shorthand para `flex-direction` e `flex-wrap`:
  - `flex-flow: row wrap`
  - `flex-flow: column nowrap`

### Alinhamento

- `justify-content`:
  - Alinha os itens ao longo do eixo principal.
  - Estes valores tratam da distribuição do espaço disponível no container, ou seja, funciona apenas se os itens não ocuparem todo o container.
  - Após todos os comprimentos flexíveis e quaisquer margens automáticas serem resolvidas.
  - `flex-start`: Alinha ao início da linha
  - `flex-end`: Alinha ao fim da linha
  - `center`: Alinha os itens centralmente
  - `space-between`:
    - Os itens são distribuídos uniformemente ao longo da linha
    - O primeiro elemento fica no início e o último fica no fim e dois elementos adjacentes possuem espaçamento igual.
    - `X--Y--Z`
  - `space-around`:
    - Os itens são distribuídos uniformemente
    - O primeiro e segundo item não fica nas extremidades do container e possuirão espaçamentos na borda esquerda/direita, menores que os espaçamentos que não estão na extremidade
    - Há um espaçamento na esquerda e direita de cada item, e juntando esses espaçamentos dará um espaçamento maior que nas extremidades
    - `-X--Y--Z-` (exemplo)
  - `space-evenly`:
    - Os ítens são distribuídos uniformemente
    - Todos os espaçamentos, incluindo das extremidades, são distribuídos de forma igualitária
    - `--X--Y--Z--` (exemplo)
- `align-items`:
  - Controla onde os itens ficam ao longo do eixo transversal
  - `stretch` (padrão):
    - Estica os itens para preencherem todo o container.
  - `flex-start`:
    - Serão alinhados a partir ao cross start da linha.
  - `flex-end`:
    - Serão alinhados a partir ao cross end.
  - `center`:
    - Os itens serão centralizados entre o *cross-start* e o *cross-end* da linha.
  - `baseline`:
    - As baselines da primeira linha de cada item serão alinhadas
- Determinando como será feita a distribuição de linhas geradas pela propriedade `flex-wrap` ao longo do eixo transversal. (`align-content`):
  - Funciona apenas se tiver espaço sobrando no container.
  - `stretch` (padrão):
    - As linhas se estendem para ocupar o espaço restante.
  - `flex-start`: Distribui as linhas no início do container.
  - `flex-end`: Distribui as linhas no final do container.
  - `center`: Centraliza as linhas
  - `space-between`:
    - Haverá um espaçamento entre linhas
    - Não haverá espaçamento nas extremidades do eixo transversal
  - `space-around`:
    - Haverá um espaçamento entre linhas, até nas extremidades
  - `space-evenly`:
    - As linhas terão espaçamento uniforme e igual incluindo as extremidades

## Espaçamento

- A propriedade `gap` permite customizar o espaçamento entre itens flex:
  - Shorthand para `column-gap` e `row-gap`

## Itens

- Cada item de um flex container é uma caixa flexível

### Dimensionamento de itens flexíveis

- Essas propriedades auxiliam no tamanho dos itens flex e como o container irá lidar com sobra ou falta de espaço.
- `flex-grow`:
  - especifica o fator de crescimento
  - permite que o item cresça caso haja espaço disponível
  - largura do item = (flex-grow / total de flex-grow no container) * espaço disponível + largura inicial (flex-basis) onde espaço disponível = antes do flex-glow
- `flex-shrink`:
  - especifica o fator de redução de um item
  - quando falta espaço num container (espaço livre negativo), os itens serão reduzidos de acordo com este fator
- `flex-basis`:
  - Determina o tamanho inicial do item antes de qualquer coisa
  - Valores:
    - `auto`: O tamanho é computado como o valor da propriedade do tamanho principal
  - Tem prioridade sobre `width`
  - `flex-basis: 0`: Se todos os elementos definidos com isso e com `flex-grow >= 1`, tentará manter todos os elementos com a mesma largura
- `flex`:
  - shorthand para `flex-grow`, `flex-shrink` e `flex-basis`
  - sintaxes:
    - Um valor:
      - No caso de um número, é interpretado como `flex: <numero> 1 0`
      - No caso de um valor válido para a propriedade `width`, é interpretado como `flex: 1 1 <width>`
      - `auto`: `flex: 1 1 auto`
    - Dois valores:
      - 1º: `<number> -> flex-grow`
      - 2º: `<number> -> flex-shrink (~> flex-basis = 0) || <width> -> flex-basis (~> flex-shrink = 1)`
    - Três valores:
      - `flex-grow flex-shrink flex-basis`



### Alinhamento

- Alinhar um item específico ao longo do eixo transversal (`align-self`):
  - `auto`: obedece o `align-items`
  - `stretch`: ocupará todo o eixo transversal
  - `baseline`: a linha de base do item será alinhada com as linhas de bases de outras caixas
  - `flex-start`: alinhado ao topo
  - `flex-end`: alinhado no final do eixo
  - `center`: centralizado

### Ordenamento

- `order`:
  - Especifica a ordem do elemento
  - O padrão é 0
  - Itens com valores mais altos aparecerão depois de itens com valores mais baixos.
  - Itens com o mesmo valor irão aparecer na ordem de origem.

## Dúvidas

### Diferença entre flex-basis e width

- O que `flex-basis` irá se aplicar depende do `flex-direction`:
  - Se for `row`, controla a largura
  - Se for `column`, controla a altura
- Diferenças principais:

| flex-basis                                                   | width                          |
| ------------------------------------------------------------ | ------------------------------ |
| Se aplica apenas à itens flexíveis                           | Se aplica a todos os elementos |
| Funciona apenas no eixo principal, ou seja, não é possível controlar a largura de um elemento com o container `flex-direction: column` | Funciona em todos os eixos     |
| Não tem efeitos em itens flexíveis absolutamente posicionados | Possui efeito                  |

- Semelhanças:
  - Não tem diferença em termos de como são *renderizados*, a menos que `flex-basis` seja `auto` ou `content`
  - `flex-basis` e `width` são *resolvidos* de forma idêntica, a menos que `flex-basis` seja `auto` ou `content`, nestes casos pode usar a largura do conteúdo (onde a largura também usaria)
  - `(flex-basis: x || width: x || height: x) && flex-shrink >= 1`, não significa necessariamente que a largura/altura renderizada, pois pode vim a encolher