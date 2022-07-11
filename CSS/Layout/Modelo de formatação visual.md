# Modelo de formatação visual

- De acordo com o modelo de formatação visual: Para cada elemento no HTML, 0, 1 ou N caixas são geradas para um elemento.

## O fluxo

- O fluxo de um elemento `A` consiste em `A` **e** todos os elementos em fluxo cujo ancestral **fora de fluxo** mais próximo é `A`.
- O fluxo são todos os elementos descendentes um elemento fora de fluxo, exceto os elementos aninhados em outro elemento fora de fluxo pois estão "ocultos".
- Portanto, o fluxo seria um conjunto de coisas que trabalham **juntas** no layout. Elementos fora do fluxo são dispostos independentemente.

## Fluxo normal

- Elementos em fluxo normal pertencem a um contexto de formatação `block` ou `inline`.
- `Block-level box` participa de `BFC` e `inline-level participa` de `inline FC`.

## Elementos block-level, box-level e etc

- `Block-level element`:
  - São formatados visualmente como blocos.
  - Geram uma caixa de nível de bloco principal:
    - Contém: Caixas descendentes + conteúdo gerado.
    - É a caixa que participa em qualquer esquema de posicionamento.
- `Block container`: Contém apenas caixas block-level ou estabelece um inline formatting context (ou seja, possui apenas `inline box`).
- `Block-level box`:
  - Caixas que participam de um BFC.
  - (com algumas exceções) é também uma block container box.
- `Block box`: `block-level box` que é `block container box`, ou seja:
  - Participa de um BFC.
  - Contém caixas block-level ou estabelece um inline formatting context.

- `Block level`: Conteúdo que participa num layout de bloco.
- `block layout`: O layout dos `block-level box`s dentro de um BFC.

## Contextos de formatação

- É uma área em que foi configurada para exibir conteúdos numa certa maneira. Ou melhor ainda:
- É mais um **estado** de uma caixa que define as **regras de layout** para si mesma e para as caixas descendentes. Ou melhor ainda:
- É um ambiente no qual um conjunto de caixas relacionadas são dispostas.
- BFC (Block formatting context):
  - É uma região onde ocorre a disposição de caixas de blocos e onde os floats interagem com outros elementos.
