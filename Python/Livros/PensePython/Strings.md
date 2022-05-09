# Strings
- Um tipo de dado composto de sequências de caracteres.
- Para obter um caractere numa string, utiliza-se o operador colchete junto com o índice do caractere.
- Podemos utilizar índices negativos, que conta de trás para frente. -1 indica o último elemento, -2 indica o penúltimo e etc.

## Fatia de string
- Uma fatia de string é uma substring obtida a partir de outra string.
- Sintaxe: `x[n:m]`. Obter uma fatia a partir do n-ésimo termo até o m-ésimo termo (exclusivo).
- Se omitir n, vai do começo da string, se omitir m, vai até o fim da string.

## Operador de formatação
- Formata uma tupla de valores de acordo com uma string de formatação.
- Sintaxe:
```
"string" % (tupla)
```
- Temos sequências de formatação como "%d", "%s", etc.