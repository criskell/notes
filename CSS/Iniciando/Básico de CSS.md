# Básico de CSS

- CSS é uma linguagem de folha de estilos utilizada para apresentar de forma agradável um documento como HTML, XML e SVG.

## Sintaxe

- O CSS é uma linguagem baseada em **regras** que agrupam estilos para serem aplicados em um ou mais elementos.
- Cada regra possui um bloco de declaração que consiste em várias declarações separadas por `;`.
- Cada declaração é um par nome/valor onde nome é o nome da propriedade e valor é um valor para esta propriedade.

## Anatomia de um conjunto de regras CSS

```
/**
 * Abaixo fica um conjunto de regras CSS.
 */
seletor {
	propriedade: valor; /* declaração */
}
```

- Isto tudo é chamado de **conjunto de regras** ou simplesmente regra.
- Partes do conjunto de regras:
  - Seletor: seleciona os elementos a serem estilizados.
  - Chaves: Inicia um **bloco de declarações**.
  - Declaração: Par de propriedade e valor.
  - Propriedade: Determinado estilo do elemento.
  - Valor: Valor da propriedade.

## Tipos de seletores

- Seletor de elemento ou seletor de tipo
- Seletor de ID
- Seletor de classe
- Seletor de atributo: Seleciona elementos com um atributo. Exemplo: `[src]`
- Seletor de pseudo-classe: Seleciona os elementos especificados, mas somente quando estiverem num determinado estado. Exemplo: `a:visited`.

## Caixas

- O layout do CSS é principalmente baseado no modelo de caixas, ou seja, muitas vezes estamos escrevendo propriedades de uma caixa como margem, preenchimento e borda.