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

- Para definir cores, utilizamos a propriedade **background-color**.
-  Para adicionar imagens em fundos, utilizamos a propriedade **background-image**. Por exemplo: `background-image: url(https://sm.ign.com/ign_br/screenshot/default/embargo-sat-19-feb-14-20-pt-even-attack-on-titans-english-vo_dtjc.jpg);`
- Se `tamanho(imagem) < tamanho(container)`, haverá repetições, no eixo X ou eixo Y. Para controlar esta repetição: `background-repeat`. Valores:
  - `repeat-x`: Repetir no **eixo X**.
  - `repeat-y`: Repetir no **eixo Y**.

- Alterar o posicionamento na imagem no container: `background-position`.
- Shorthand: `background`
- Alterar o anexamento/fixamento da imagem: `background-attachment`

## Estilos externos

- Carregar uma folha de estilos num arquivo externo.
- Vantagens:
  - "Uma única fonte da verdade".

## Box Model

- Descreve os elementos HTML como caixas que possui conteúdo, paddings (espaçamento interno), bordas e margens (espaçamento externo).
- Colapso de margem acontece quando duas margens se juntam.
- `box-sizing: border-box`: O padding + bordas é contabilizada na propriedade `width`.

## Elementos flutuantes

- A propriedade **float** faz com que altere se o fluxo dos elementos, fazendo determinados elementos **flutuar** na direita ou esquerda.
- Ao fazer isso, o elemento sai do fluxo normal do documento e vai para um outro fluxo (flutuante). 
- O elemento pai não expande até o final dos elementos flutuantes, acha que não existe.
- Propriedade **clear**: Limpa o fluxo flutuante num outro lado.

## Elementos inline, inline-block e block

- Elementos block:
  - Ocupa toda a largura do pai e fica um abaixo do outro.
- Elementos inline:
  - Dimensionamento intrínsico e não fica nova linha.
- Elementos inline-block:
  - Itens um abaixo do outro e seu dimensionamento é intrínsico.