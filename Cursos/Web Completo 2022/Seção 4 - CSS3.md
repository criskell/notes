# CSS3

- CSS permite adicionar estilos em documentos CSS.

## Métodos para adicionar CSS

- Inline: Diretamente no atributo `style`.
- Interno: Diretamente na página HTML.

## Seletores

- Selecionam elementos HTML.

## Classes, IDS

- Classes são utilizadas para classificar e IDs para identificar unicamente um elemento.

## Divs e span

- Divs é um container genérico do tipo bloco utilizado para dividir o conteúdo.
- Span é um container genérico do tipo inline.
- Elementos do tipo bloco ocupa toda a tela.

## Bordas

- Propriedade `border`:
  - `<espessura> <estilo> <cor>`
- As propriedades `border-width` (espessura), `border-style` e `border-color` definem características para todos os lados, para os lados na vertical e lados na horizontal ou para lados específicos no sentido horário.

## Fontes e cores

- Formas de utilizar cores:
  - Palavra-chaves
  - Códigos hexadecimais
- Fontes:
  - `font-size`: Tamanho da fonte.
  - `font-family`: Família de fontes.
  - `text-decoration`:
    - `underline`: Sublinhado.
    - `overline`: Linha encima do texto.
    - `line-through`: Linha no meio do texto.



## Cores e imagens de fundos

- Adicionando cores com background-color e imagens com background-image.

```css
/* Para definir cores, utilizamos a propriedade background-color. */
            /* Para adicionar imagens em fundos, utilizamos a propriedade background-image */
            background-image: url(https://sm.ign.com/ign_br/screenshot/default/embargo-sat-19-feb-14-20-pt-even-attack-on-titans-english-vo_dtjc.jpg);
/* Se size(imagem) < size(container) haverá repetições, no eixo X ou eixo Y.*/
/* Valores:*/
/* repeat-x: Repetir no eixo X. */
/* repeat-y: Repetir no eixo Y. */
background-repeat: repeat-x;

/**
Altera o anexamento da imagem em algum lugar.
*/
background-attachment: scroll;

/**
Define a posição da imagem no container.
*/
background-position: center center;

/* Shorthand */
background: blue url();
```



## Estilos externos

- Carregar uma folha de estilos num arquivo externo.
- Vantagens:
  - "Uma única fonte da verdade".

## Box Model

- Descreve os elementos HTML como caixas que possui conteúdo, paddings (espaçamento interno), bordas e margens (espaçamento externo).
- Colapso de margem acontece quando duas margens se juntam.
- `box-sizing: border-box`: O padding + bordas é contabilizada na propriedade `width`.