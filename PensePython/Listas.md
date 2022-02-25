# Listas
- Conjunto de elementos ordenados.
- Acessar lista por um índice: lista[i].
- Quando os colchetes aparecem no lado esquerdo de uma atribuição, ele pode modifica elementos da lista.

## Função range
- Retorna um iterável de números.
- Se receber dois argumentos, cria uma sequência do primeiro número recebido até o último número recebido mas não inclui o último número.
- Se receber apenas um, cria uma sequência do zero até algum número.
- O terceiro argumento é utilizado para especificiar o **passo**, o espaço entre dois números numa sequência.

## Operadores + e *
- O operador + concatena uma lista e o operador * repete elementos de uma lista.

## Operadore in
- Operador in verifica se um elemento está numa lista.

## Mutabilidade
- A lista pode ser alterada.
- Podemos utilizar o colchete no lado esquerdo de uma atribuição para atualizar.
- Podemos utilizar slicing para atualizar múltiplos elementos de uma só vez.
```
list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
list[1:4] = ['x', 'x', 'x']
list # [1, 'x', 'x', 'x', 5, 6, 7, 8, 9]
list[1:4] = []
list # [1, 5, 6, 7, 8, 9]
```