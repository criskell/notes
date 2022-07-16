# Posicionamento

- A propriedade `position` especifica como o elemento deve ser posicionado.

## Valores

- `static`:
	- A caixa é posicionada em relação ao fluxo normal
	- Propriedades de deslocamento e `z-index` não tem efeito.
- `relative`:
	- Significa "relativo a si mesmo"
	- A caixa é posicionada no seu lugar no fluxo normal
	- Podemos modificar a posição final com as propriedades de deslocamento
	- Permanece **in-flow**, mas **deslocado** em relação a si mesmo, não deixa espaço para trás
	- Cria um novo sistema de coordenadas para seus filhos, ou seja, se torna o ponto de referência para os deslocamentos dos mesmos
- `absolute`:
    - A caixa é removida completamente do fluxo normal, ou seja, o espaço que ocuparia no fluxo normal é ocupado pelo próximo elemento e os elementos passam a não "enxergar" o elemento
    - As propriedades de deslocamento passam a definir distância dos lados de um **containing block**.
    - geralmente é posicionado em relação ao ancestral mais próximo posicionado e caso contrário é posicionado em relação ao body.
    - O elemento é posicionado em relação a um contexto de posicionamento (containing block).
    - Se o elemento não tiver um elemento posicionado como ancestral, estará contido e posicionado no **initial containing block**, assim como o elemento raiz, que tem as dimensões da viewport, assim será exibido fora do `html` e posicionado a `viewport`.
- `fixed`:
	- É igual ao posicionamento absoluto, mas a caixa permanece fixa em relação a alguma referência.
- `sticky`:

  - É posicionado `relative` até que atinja um limite, a partir do qual se torna `fixed`

  - São "sticky" (pegajosos) relativos a um elemento ancestral mais próximo com um mecanismo de rolagem


## Contextos de posicionamento

- Geralmente é dito que `position ∊ (relative, absolute, fixed)` cria um contexto de posicionamento, o qual outros elementos filhos com posicionamento são posicionados em relação.

## Propriedades de deslocamento

- Determina a real localização de um elemento no documento
- `top / bottom`:
  - `position: absolute / fixed`: distância entre o lado superior/inferior da *outer edge* do elemento e o lado superior/inferior da *edge* do containing block
  - `position: relative`: distância em que a *top/bottom edge* de um elemento é movida abaixo/acima da sua posição original
  - se forem definidas `top / bottom` e a altura não está especificada (ou auto ou 100%) e o elemento está *absolutamente posicionado*, então tais propriedades são respeitadas
  - em outros casos, caso a altura esteja *restringida* ou `position = relative`, `bottom` é ignorado
- `left / right`:
  - `position: absolute / fixed`: distância da *left/right edge* do elemento da *left/right edge* do containing block
  - `position: relative`: distância em que a *left/right edge* do elemento é movida para a direita/esquerda a partir de sua posição no fluxo normal
  - se definir ambos e não houver restrições como restrição na largura, o elemento irá alterar seu tamanho para atender as propriedades. caso contrário, `left` terá precedência (no caso de LTR)
- No caso dessas props em `sticky`
  - se moverá em relação ao ancestral mais próximo com uma caixa de rolagem ou viewport
  - limitado aos limites do container
- Podemos pensar que ao aplicar estas propriedades, uma *força invisível* empurrará a caixa no lado especificado, movendo-a na direção **oposta**.
- Casos:
  - Definindo direções opostas:
    - se definir top / bottom, bottom será ignorado. O mesmo se aplica horizontalmente. (ltr, analogamente para rtl)
    - se ambas forem definidas, `height = auto` e for *absolutamente posicionado*, o el. irá expandir