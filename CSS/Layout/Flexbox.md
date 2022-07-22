# Flexbox

- Flexbox é um modo de layout para posicionamento e dimensionamento de caixas **flexíveis**

- O que permite?

  - distribuição de espaço e alinhamento de conteúdo
  - a largura e altura se adaptar de acordo com o dispositivo de exibição
  - o container esticar ou comprimir itens

  - alinhamento de itens na horizontal ou vertical

  ## Conceitos e terminologia

  ### Eixos flex

  - Os eixos flex determinam as direções flex ao longo das quais items flex são colocadas em um container.
  - O eixo principal de um container é o eixo principal ao longo do qual itens são colocadas e se estende na *dimensão principal*.
  - Itens são colocados iniciando no *main start* em direção ao *main end*.
  - O tamanho de um item no eixo principal é chamado de *main size*. O tamanho de um item no eixo transversal é chamado de *cross size*. Os tamanhos, respectivamente, podem serem definidos por *largura* ou *altura*, ou vice-versa, dependendo de qual é a direção do eixo principal.
  - O eixo transversal é o eixo perpendicular ao eixo principal e se estende na *dimensão traversal*.
  - Linhas flex são colocadas iniciando na *cross start* até a *cross end*.

  ## Linhas flex

  - Linhas flex são linhas hipotéticas em que itens são colocados.
  - Seguem o eixo principal e são empilhadas ao longo do eixo transversal.

  ## Flex container

  -  É um elemento que recebeu um tipo de exibição interna como `flex` (ex.: `display: inline flex || inline-flex || block flex || flex`) e tornou seus filhos diretos em caixas flexíveis.

### Fluxo de um container

- `flex-direction`:
  - Define o fluxo de exibição dos itens.
  - `row`:
    - Os itens são organizados em linhas da esquerda para a direita.
    - O eixo principal é horizontal.
  - `column`:
    - Os itens são organizados em colunas um abaixo do outro.
  - `row-reverse`: Igual ao `row`, mas da direita para esquerda
  - `column-reverse`: Igual ao `column`, mas de baixo para cima
  
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
  - Após todos os comprimentos flexíveis e quaisquer margens automáticas serem resolvidas.
  - Funciona apenas se os itens não ocuparem todo o container.
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
  - Alinhando itens ao longo do eixo transversal
  - `stretch` (padrão):
    - Os itens preencheram todo o eixo transversal.
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
    - As linhas são distribuídas de forma que preencham todo o container uniformemente.
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

### flex-grow, flex-shrink e flex-basis

- Essas propriedades auxiliam no tamanho dos itens flex e como o container irá lidar com sobra ou falta de espaço.
- `flex-grow`:
  - especifica o fator de crescimento de um item
  - o padrão é 0, ou seja, não crescem, mesmo se tiver espaço sobrando

- `flex-shrink`:
  - especifica o fator de redução de um item
  - quando falta espaço num container, os itens serão reduzidos de acordo com este fator
  - `1` (valor padrão): permite que os itens tenham seus tamanhos reduzidos para caber no container
  - `0`: não permite a redução
  - `x > 0`: diminuirá `x` vezes que outros elementos 

- `flex-basis`:
  - determina o tamanho inicial do item antes da distribuição do espaço restante
  - `0`: Se todos os elementos definidos com isso e com `flex-grow >= 1`, tentará manter todos os elementos com a mesma largura

- `flex` é uma shorthand para `flex-grow`, `flex-shrink` e `flex-basis`
  - `flex: 1 -> flex-grow: 1, flex-shrink: 1, flex-basis: auto`
  - `flex: 0 1 auto (padrão)`
  - `flex: 2 -> flex-grow: 2, flex-shrink: 1, flex-basis: auto`


### Alinhamento

- Alinhar um item específico ao longo do eixo transversal (`align-self`):
  - `auto`: obedece o `align-items`
  - `stretch`: ocupará todo o eixo transversal
  - `baseline`: a linha de base do item será alinhada com as linhas de bases de outras caixas
  - `flex-start`: alinhado ao topo
  - `flex-end`: alinhado no final do eixo
  - `center`: centralizado

### Ordenamento

- A ordem padrão dos elementos é a ordem do código
- Permite especificar a ordem de um elemento, do menor para o maior