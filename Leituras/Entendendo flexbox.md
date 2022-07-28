# Entendendo flexbox

## Aumentando o tamanho de itens

- Se o espaço restante for positivo e maior que zero, cada item terá seu tamanho aumentado proporcionalmente de acordo com o valor `flex-grow`.
- Para calcular o espaço restante, somamos todas os tamanhos iniciais de cada item e subtraímos do tamanho do container.
- Já para calcular o quanto de espaço será alocado para cada item, multiplicamos o espaço restante pela razão do valor `flex-grow` e todos os valores `flex-grow` de todos os itens.

## Redução do tamanho dos itens

- Quando o espaço restante < 0
- 