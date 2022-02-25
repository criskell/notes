# Estrutura de dados

- Para utilizar pilhas podemos utilizar o tipo lista e para utilizar filas podemos utilizar a classe collections.deque.

## Compreensão de lista

- Compreensão de lista permite criar uma lista com base em algum outro iterável, permitindo mapeamento e filtramento.
- Compreensão de lista consiste em um par de colchete contendo uma **expressão** seguido de uma cláusula `for` e então **zero** ou **mais** cláusulas `for` ou `if`.
- Estrutura mínima: `[<expressao> <for>]`
- Estrutura: `[expressao <for> [...<for>|<if>]]`
- Por exemplo:

```python
novaLista = [(x, y) for x in range(5) for y in range(5) if x + y > 2]
print(novaLista)

# Equivalente:
novaLista = []

for x in range(5):
    for y in range(5):
        if x + y > 2:
        	novaLista.append((x, y))
            
print(novaLista)
```

- A expressão será **avaliada** no **contexto** da execução em ordem das cláusulas `for` e `if `.

## Instrução del

- A instrução `del` permite remover um item de uma lista a partir de seu índice, remover uma fatia e remover uma variável.

## Sequências

- Sequências: Indexação e fatiamento.

## Tuplas

- Tuplas são sequências imutáveis de valores separados por vírgulas:

  ```python
  minhaTupla = 1, 2, 3, 4, 5, 7, 8, 9
  ```

- Tuplas podem ser delimitadas por parênteses, mas é opcional.

## Desempacotamento de iteráveis

- Podemos empacotar valores em sequências, por exemplo, tuplas:

  ```python
  tupla = 10, 20, 30
  ```

- Podemos desempacotar valores de **iteráveis** (toda sequência é um iterável) utilizando **desempacotamento de iteráveis**:

  ```python
  x, y, z = 10, 20, 30
  x, = 10,
  ```

- O **desempacotamento de iteráveis** desempacota um **iterável** em uma lista *ou* tupla de *variáveis*.

- Podemos **aninhar** o desempacotamento:

  ```python
  [(a1, a2), b, c] = ([10, 11], 20, 30)
  ```

- Operador `*` pode ser utilizado num desempacotamento para **empacotar** o **restante** dos elementos numa **lista**:

  ```python
  a, *bs, c = (10, 20, 30, 50)
  ```

  

## Sets

- Conjuntos matemáticos podem serem utilizados utilizando o tipo de dado `set`.

- **Não-ordenados**.

- Conjuntos são criados utilizando chaves ou a função `set`:

  ```python
  meuConjunto = {1, 2, 3, 3, 4, 5, 7, 7}
  meuConjunto = set([1, 2, 3, 3, 4, 5, 7, 7])
  ```

- Conjuntos suportam operações de diferença `-`, intersecção `|`, união `&` e diferença simétrica `^`.

- Da mesma forma das listas, compreensões de conjuntos são suportadas:

  ```python
  x = {x for x in 1, 2, 3, 4, 5, 7, 8 if x + x != x * x}
  ```

## Dicionários

- Um dicionário mapeia um conjunto de chaves de tipos imutáveis para um conjunto de objetos.
- São indexados por chaves.

### Operações

- Valores de chaves podem serem obtidos e armazenados utilizando colchetes.
- Um par pode ser removido utilizando a instrução `del`.

## Compreensões de dicionários

- Podemos criar dicionários utilizando compreensões de dicionários com expressões `chave:valor`:

  ```python
  {x: y for x in range(10) for y in '0123456789'}
  ```

## Comparação de sequências

- Sequências são comparadas utilizando a **ordem léxicográfica**: primeiro um item é comparado com o outro de uma sequência. Se forem **diferentes**, isto determinará o **resultado** da comparação (o resultado irá depender da ordem entre eles). Caso contrário isso será repetido até o fim das listas.
- Sequências iguais quando comparadas são consideradas iguais.
- A comparação de strings utiliza Unicode.
- Se uma sequência é **subsequência inicial** da outra, a sequência **mais curta** será considerada a **menor**.

