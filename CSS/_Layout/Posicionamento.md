# Posicionamento

- A propriedade `position` especifica como o elemento deve ser posicionado.
- O posicionamento permite substituir o comportamento no fluxo normal.

## Posicionamento estático

- É posicionado de acordo com o fluxo normal.

## Tipos

### Posicionamento relativo

- A caixa é posicionada no seu lugar no fluxo normal
- Podemos modificar a posição final com as propriedades de deslocamento
- Permanece **in-flow**, mas **deslocado**

### Posicionamento absoluto

- A caixa é removida completamente do fluxo normal, ou seja, o espaço que ocuparia no fluxo normal é ocupado pelo próximo elemento e os elementos passam a não "enxergar" o elemento
- As propriedades de deslocamento passam a definir distância dos lados de um **containing block**.
- geralmente é posicionado em relação ao ancestral mais próximo posicionado e caso contrário é posicionado em relação ao body.
- O elemento é posicionado em relação a um contexto de posicionamento (containing block).
- Se o elemento não tiver um elemento posicionado como ancestral, estará contido e posicionado no **initial containing block**, assim como o elemento raiz, que tem as dimensões da viewport, assim será exibido fora do `html` e posicionado a `viewport`.

### Posicionamento fixo

- É igual ao posicionamento absoluto, mas a caixa permanece fixa em relação à viewport (dependendo do containing block)

## Posicionamento sticky

- É posicionado `relative` até que atinja um limite, a partir do qual se torna `fixed`
- São "sticky" (pegajosos) relativos a um elemento ancestral mais próximo com um mecanismo de rolagem

## Contextos de posicionamento

- É o elemento o qual um outro elemento é posicionado em relação
- Alteramos o contexto posicionando um elemento ancestral do elemento

## Propriedades de deslocamento

- Determina a real localização de um elemento no documento
- `top`, `left`, `right`, `bottom`
- Podemos pensar que ao aplicar estas propriedades, uma *força invisível* empurrará a caixa no lado especificado, movendo-a na direção **oposta**.

## z-index

- Elementos posicionados ficam empilhados acima de elementos não posicionados.
- Elementos posicionados posteriores na ordem de origem ficam encima de elementos posicionados na ordem de origem.
- A propriedade `z-index` determina a ordem de empilhamento no eixo z de elementos **posicionados**, ou seja, onde ficarão.
- O eixo z é uma linha imaginária que percorre da superfície da tela até o rosto.

#### Contextos de empilhamento

- Contexto de empilhamento são grupos de elementos que compartilham um pai comum.
- o `z-index` dos elementos num contexto são relativos a ordem de empilhamento do pai.