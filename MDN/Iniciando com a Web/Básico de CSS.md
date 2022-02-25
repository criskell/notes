# Básico de CSS

- CSS é uma linguagem de folha de estilos.

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