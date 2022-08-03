# Modelo do Flexbox

## Eixos

- Os itens de um container flex são dispostos ao longo de dois eixos.
- O eixo principal percorre a direção na qual itens são colocadas e se estende na *dimensão principal*. O início deste eixo é chamado de *main start* e o fim é chamado de *main end*.
- O tamanho de um item ou container na dimensão principal é chamado de *main size* é definido por `width` ou `height`.
- O tamanho de um item ou container no eixo transversal é chamado de *cross size*.
- Os tamanhos, respectivamente, podem serem definidos por *largura* ou *altura*, ou vice-versa, dependendo de qual é a direção do eixo principal.
- Itens podem ter um *min/max main size*, definidos pela `min/max width/height`, o que estiver na dimensão principal.
- O tamanho preferido é o tamanho especificado por `width` e `height`
- O tamanho `min-content` é o tamanho mínimo do item sem que ocorra overflow. Aqui leva em consideração todas as quebras de linhas.
- O tamanho `max-content` é o tamanho máximo que o item pode ter para conter o conteúdo. Se o texto não possuir alguma formatação que quebre ele, é apenas uma linha.
- O eixo transversal percorre perpendicularmente ao eixo principal e se estende na *dimensão traversal*.
- Linhas flex são colocadas iniciando na *cross start* até a *cross end*.

## Linhas

- Linhas flex são linhas hipotéticas em que itens são colocados.
- Seguem o eixo principal e são empilhadas ao longo do eixo transversal.

## Flex container

-  É um elemento que recebeu um *tipo de exibição interna* como `flex` e tornou seus filhos diretos em caixas flexíveis.

## Itens

- Cada item de um flex container é uma caixa flexível