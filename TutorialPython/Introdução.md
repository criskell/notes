# Introdução

- Tipos de dados:
  - int
  - float
  - str
  - bool
- Divisão sempre retorna um float.
- Operadores aritméticos: +, -, +, /, %, //
- A divisão de piso (`//`) descarta a parte fracionária.
- No modo interativo, a variável _ armazena o último resultado.
- Numa operação aritmética com operandos de tipo diferente do float, o Python converterá automaticamente o inteiro para float.

## Strings

- Sequência de caracteres.
- Strings podem ser concatenadas com o operador `+` e repetidas com o operador `*`.
- Duas ou mais strings literais juntas na mesma linha são concatenadas automaticamente.
- Strings podem ser indexadas.
- Temos suporte para índices negativos, onde a contagem é feita pela direita.
- Dado que -0 é 0, índices negativos começam em -1.

### Strings raw

- Strings cruas são strings em que as sequências de escape são ignoradas:

  ```python
  print(r"oi\nea\e")
  ```

### Fatiamento

- São substrings de strings.
- Sintaxe:

```python
string[n:m]
```

- O fatiamento é selecionado a partir do elemento de índice `n` e vai até, mas não incluindo, o elemento de índice `m`.
- Se omitir `n`, o padrão é zero e se omitir m o padrão é o tamanho da string.

## Listas

- Conjunto de elementos.

- Listas podem ser fatiadas e indexadas, assim como as strings.

- Listas são mutáveis.

- Podem ser concatenadas com o operador `+` e repetidas com o operador `*`.

- Atribuição a fatias é possível:

  ```python
  xs = [1, 2, 3, 4]
  xs[1:3] = ['x', 'x'] # xs = [1, 'x', 'x', 4]
  ```

  