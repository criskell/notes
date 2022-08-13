# Strings

- String é uma sequência de caracteres.

## Como representar

- Aspas simples ou duplas
- Backticks

## Escape de caracteres

- Significa tratar uma string como um texto ao invés de código.
- Fazemos isso com `\`

## Template literals

- São strings formadas por backticks e que permitem inserir expressões diretamente na string através do `${expressao aqui}`.

## Multilines

- Strings multilines podem ser criadas com template literals, que respeita quebras de linhas.

## Métodos

- Para obter um comprimento: `str.length`
- Para obter um caractere num certo índice: `str[indice]`
- `str.indexOf(substring[, startIndex])`:
  - Retorna o índice da primeira ocorrência de uma substring.
  - O parâmetro `startIndex` é o início da busca.
- `str.includes(substring)`:
  - Determina se uma substring está numa string.
- `str.slice(inicio[, fim])`:
  - Extrai uma substring da string formada pelo caractere de índice `inicio` até, mas não incluindo, o caractere de índice `fim`.
  - Se não informado, `fim` será os caracteres restantes.
- `str.replace(substring, nova)`:
  - Substitui a primeira ocorrência.
- `str.replaceAll(substring, nova)`:
  - Igual ao `.replace`, mas substitui todas as ocorrências.

## Exercícios

1. Qual é a diferença entre `.replace` e `.replaceAll`?
2. Como funciona o `.slice`?
3. Como funciona o segundo parâmetro do `.indexOf()`?
4. Como determinar se uma string contém uma substring?