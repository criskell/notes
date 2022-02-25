# Tipografia

- Tipografia é a arte e o processo de criação na composição e impressão de um texto.
- Significa "impressão dos tipos" onde tipo é uma letra ou caractere.
- Fontes trazem emoções.

## Anatomia dos tipos

- Estuda a estrutura e organização dos tipos.
- Conceitos anatômicos:
  - Linha de base: A linha que todas as letras repousam. O "chão" das letras.
  - Linha descendente: Uma linha que marca as partes descendentes de uma letra.
  - Linha ascendente: Uma linha que marca as partes ascendentes de uma letra.
  - Ascendente: Parte de letras minúsculas que estão para cima da altura x.
  - Descendente: Parte das letras que estão para baixo da linha de base.
  - Altura-x: É a altura da letra x minúscula a partir da linha base. Todas as letras minúsculas de uma fonte segue esta altura.
  - Altura das maiúsculas: Altura das letras maiúsculas a partir da linha base.
  - Corpo: É a altura máxima que uma letra pode ocupar na fonte. Vai da linha descendente até a altura das maiúsculas.
  - Serifa: É um pequeno prolongamento no final de alguns tipos. Ajudam na leitura mas a recomendação é que nas telas as fontes sejam não serifadas.
  - Barra ou filete: Liga duas hastes.
  - Haste: Um traço diagonal ou vertical.
  - Esporão: Pequena projeção na haste.
  - Vertíce: Formado por uma convergência de duas hastes. As letras V e A possuem um vertíce, na base e no topo, respectivamente.
  - Terminal: Elemento que não fecha. A letra r possui um terminal ligado a haste principal.
  - Arco: Uma curva que sai da haste principal. A letra n possui.
  - Braço: Uma haste inclinada ou horizontal que sai da haste principal. A letra k possui.
  - Perna: Haste com uma extremidade ligada a haste principal e possui uma extremidade livre ou ocupada com um pé. Letra k possui.
  - Pé: Sai de uma perna. Letra k possui.
  - Espinha: São as curvas da letra S. Uma curva e contracurva.
  - Barriga: Curva ligada a uma haste principal em dois pontos. A letra b e d possui.
  - Olho: Espaço fechado. As letras O, g e Q possuem.
  - Cauda: Fica abaixo da linha de base.
  - Orelha: Um apêndice presente na letra g.

## Famílias

- Famílias são conjuntos de glifos que possuem as mesmas características anatômicas independentemente de algumas variações como peso, estilo e tamanho.
- Fontes são conjuntos de glifos dentro da família tipográfica que diferem em algumas características. Pode se referir a um arquivo digital também.
- Glifos são signos alfabéticos projetados para reprodução mecânica.

## Categorias de fontes

- Serif: Com serifa.
- Sans-serif: Sem serifa.
- Monoespaçada: A largura de cada glifo é igual. Por exemplo, numa fonte monoespaçada, a largura do glifo m é igual a largura do glifo l.
- Handwriting ou Script: Tenta simular a escrita a mão.
- Display: Não segue as características acima, tenta ser diferente.

## Famílias de fontes com CSS

- Propriedade `font-family`
- Recebe uma lista de famílias, onde irá tentar carregar a primeira e se não der irá carregar a segunda, até terminar a lista.
- Nem todo dispositivo tem a mesma família.
- Devemos usar safe font combinations, que consiste em uma lista de fontes que termina com uma fonte genérica.
- Fontes genéricas referem-se a fontes genéricas com determinadas características disponível no dispostivo. Por exemplo, `monospace` é uma fonte genérica que se refere a uma fonte monoespaçada, não importa qual.

## Tamanhos e medidas

- Existem 2 tipos de medidas:
  - Absolutas: Se referem a uma medida que irá depender da tela.
  - Relativa: Baseado em alguma outra medida.
- A unidade `em` é relativa ao tamanho da fonte padrão.

## Peso e estilo

- Peso:
  - Peso é a grossura de caracteres.
  - Alteramos o peso da fonte com `font-weight`.
  - Podemos escolher um peso entre 100 a 900 ou nomes.
- Estilo:
  - Alteramos o estilo da fonte com `font-style`.
- Ordem do shorthand `font`: `font-style`, `font-weight`, `font-size`, `font-family`.

## Fontes externas

- Podemos importar fontes externas com a @rule `@font-face`:

  ```css
  @font-face {
      src: url('fonte.ttf') format('truetype');
      font-family: 'nome da fonte';
  }
  ```

- A propriedade `src` recebe uma lista de fontes e tenta carregar a primeira fonte que conseguir, começando da esquerda.

## Detectando fontes dentro de imagens

- Ferramentas:
  - WhatFontIs
  - FontSquirrel
  - MyFonts

## Alinhamento de texto no CSS e indentação

- Alinhamento de texto é feito com `text-align`.
- Podemos indentar o início de um texto com `text-indent`.