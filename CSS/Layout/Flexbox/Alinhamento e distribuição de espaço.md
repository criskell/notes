# Alinhamento e distribuição de espaço

## Containers

- `justify-content`:
  - Trata os itens como um grupo e especifica como o espaço disponível é distribuído entre eles.
  - `flex-start`:
    - Alinha ao início da linha
    - O espaçamento disponível fica do lado direito do último
  - `flex-end`:
    - Alinha ao fim da linha
    - O espaçamento disponível fica do lado esquerdo do início
  - `center`: Alinha os itens centralmente
  - `space-between`:
    - O espaçamento é colocado entre itens.
    - O primeiro elemento fica no início e o último fica no fim e dois elementos adjacentes possuem espaçamento igual.
    - `X--Y--Z`
  - `space-around`:
    - O espaçamento é colocado ao redor dos itens, em cada lado
    - O primeiro e último item não fica nas extremidades do contêiner e possuirão espaçamentos na borda esquerda/direita, menores que os espaçamentos que não estão na extremidade
    - Há um espaçamento na esquerda e direita de cada item, e juntando esses espaçamentos dará um espaçamento maior que nas extremidades
    - `-X--Y--Z-` (exemplo)
  - `space-evenly`:
    - Os ítens são distribuídos uniformemente
    - Todos os espaçamentos, incluindo das extremidades, são distribuídos de forma igualitária
    - `--X--Y--Z--` (exemplo)
- `align-items`:
  - Alinha os itens em relação uns ao outros no eixo cruzado.
  - Em containers com mais de uma linha, cada linha irá agir como um novo container.
  - Só funciona se houver espaço disponível na linha atual, assim como `align-self`.
  - Aplica `align-self` para todos os itens.
  - `stretch` (padrão):
    - Estica os itens para preencherem todo o espaço disponível no eixo transversal.
    - A altura do container pode ser definida pelo item mais alto ou por uma altura explícita. Já em containers com mais de uma linha, cada linha irá agir como um novo container, e esta linha terá a altura do item mais alto e assim os itens irão se dimensionar na dimensão transversal em relação ao item mais alto.
  - `flex-start`:
    - Serão alinhados a partir ao cross start da linha.
  - `flex-end`:
    - Serão alinhados a partir ao cross end.
  - `center`:
    - Os itens serão centralizados entre o *cross-start* e o *cross-end* da linha entre si
  - `baseline`:
    - As baselines da primeira linha de cada item serão alinhadas
- Determinando como será feita a distribuição de linhas geradas pela propriedade `flex-wrap` ao longo do eixo transversal. (`align-content`):
  - Trata as linhas como um grupo e distribui o espaço disponível no eixo transversal
  - Funciona apenas se tiver espaço sobrando no container.
  - `normal` (valor padrão): São colocados em sua posição padrão.
  - `stretch`: As linhas se estendem para ocupar o espaço restante.
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

### Espaçamento

- A propriedade `gap` permite customizar o espaçamento entre itens flex:
  - Shorthand para `column-gap` e `row-gap`

## Itens

- Alinhar um item específico ao longo do eixo transversal (`align-self`):
  - `auto`: obedece o `align-items`
  - `stretch`: ocupará todo o eixo transversal
  - `baseline`: a linha de base do item será alinhada com as linhas de bases de outras caixas
  - `flex-start`: alinhado ao topo
  - `flex-end`: alinhado no final do eixo
  - `center`: centralizado

## Dúvidas

### Qual é a diferença entre `align-self` e `align-items`

A diferença é que o `align-items` define um alinhamento padrão para todos os itens ao longo do eixo transversal da linha atual do container. Já o `align-self` permite que um item anule este alinhamento padrão.

## Exercícios

1. O que o valor `auto` em `align-self` faz?
2. Quais são as propriedades de distribuição de espaço ao longo do eixo transversal e ao longo do eixo principal?
