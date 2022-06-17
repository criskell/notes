# Fluxo normal

- Também chamado de Flow Layout/Block and inline layout.
- É o layout/forma padrão em que os elementos numa página web são dispostos se não fizermos alterações no layout:
  - Elementos/caixas **inline** fluem na direção **inline** (direção em que as **palavras** fluem no modo de escrita, por exemplo, horizontalmente)
  - Elementos/caixas de **bloco** fluem na direção de **bloco** (direção em que os **parágrafos** fluem no modo de escrita, por exemplo, verticalmente)
- Cada caixa no fluxo normal participa de um **contexto de formatação** (inline ou de bloco).
- Caixas de **nível de bloco** participam em um contexto de formatação de bloco e caixas em **nível inline** participam de um contexto de formatação inline.
- **Essencialmente**, o fluxo normal é um **conjunto de coisas** que trabalham **juntas** e que se **conhecem** no layout. Uma coisa **fora** deste fluxo funciona de forma **independente**.

## Contextos de formatação

- Contexto de formatação de **blocos**:
  - Num contexto de formatação de **bloco**, num modo de escrita **horizontal**, os elementos de bloco são dispostos **verticalmente**, um abaixo do outro (assim como os parágrafos no Português). Já num modo de escrita **vertical**, os blocos são dispostos **horizontalmente**.
  - Margens separam elementos irmãos.
  - Por padrão, o bloco irá consumir todo o espaço disponível na **direção inline** do *containing block*.
  - Os blocos começam na **borda inicial** do *containing block*. Assim, por exemplo, como as frases começariam num modo de escrita horizontal.
  - Margens que se "tocam" colapsam.
- Contexto de formatação **inline**:
  - Elementos inline são dispostos na direção em que as frases são escritas no modo de escrita atual (horizontalmente, no português), um após o outro.
  - Se não caber na direção inline, a caixa gerada pelo elemento é quebrada para a próxima linha, também chamada de caixa de linha.
  - O tamanho da caixa de linha na direção de bloco (altura, no português) é determinada pela caixa mais alta na caixa de linha.
  - Caixas anônimas são criadas para manter tudo em uma caixa.

## display

- A propriedade `display` determina o *tipo de exibição*.
- *tipo de exibição* possui:
  - **tipo de exibição externo**:
    - Determina como a caixa irá se comportar juntamente com os outras caixas no mesmo contexto de formatação.
    - Alguns valores:
      - `block`: A caixa se comporta como uma caixa de nível de bloco.
  - **tipo de exibição interno**:
    - Determina como as caixas filhas serão dispostas.
    - Alguns valores:
      - `flow`: Os elementos dentro da caixa se comportarão em fluxo normal, sendo exibidos inline ou como blocos.

## In-flow e out-of-flow

- **In-flow**:
  - Cada caixa que está em fluxo (normal), irá ser disposta com o layout de bloco & inline.
  - Aparece na ordem do HTML.
  - Não está fora do fluxo.
  - Todos os elementos estão em fluxo com exceção dos elementos fora do fluxo.
- **Fora do fluxo**:
  - Float, `position: fixed || absolute`, elemento raiz `html`
  - Caixas que **saíram** de sua posição do fluxo normal e **não possui uma interação** com o conteúdo ao redor normal. Os elementos in-flows não sabem que o out-of-flow existem.
  - Itens fora do fluxo criam um novo contexto de formatação de bloco. O que está dentro dele pode ser visto como um mini-layout.
  - Exemplos:
    - Floats:
      - Primeiro o float é colocado em sua posição no fluxo normal, tirado do fluxo (fica fora de fluxo) e depois movido para algum lado o máximo possível.
      - Os elementos seguintes continuarão em fluxo normal, portanto, ficarão por baixo dos floats e apenas as caixas de linhas são encurtadas.
    - Posicionamento absoluto (e fixo):
      - A caixa é retirada do fluxo normal e o espaço que antes ele ocupava, fica para outro elemento.
    - O elemento raiz, `html`, age como o container para todo o documento e estabelece um BFC.

## Overflow

- Um overflow ocorre quando há mais conteúdo que pode caber em uma caixa.
- Podemos controlar o overflow utilizando `overflow`:
  - É um shorthand para as propriedades `overflow-x` e `overflow-y`.
  - `overflow: <overflow-x = overflow-y>`
  - `overflow: <overflow-x> <overflow-y>`
  - Valores:
    - `visible`
    - `scroll`: Mostra sempre barras de rolagem.
    - `auto`: Mostras as barras de rolagens nas direções necessárias.
- Indicando overflow:
  - No eixo inline:
    - `text-overflow`
    - Indica um o overflow de texto na direção inline.
    - Valores:
      - `clip`: Corta o overflow.
      - `ellipsis`: Mostra uma elipse.

## O algoritmo do fluxo normal: resumo

  1. Box model: O **box model** é aplicado.
  2. Aplicar o dimensionamento dos elementos `block` e `inline`:
     - Os elementos do nível de **bloco** preenchem todo o espaço na dimensão inline disponível no elemento que o contém e cresce na dimensão de bloco para acomodar seu conteúdo.
     - Já os elementos do nível **inline**, seu tamanho é o tamanho suficiente para acomodar seu conteúdo e não podemos alterar sua largura e nem altura, pois eles apenas vivem nos elementos de bloco.
  3. Fazer o layout dos elementos:
     - Os elementos de nível de **bloco** são dispostos na **direção do fluxo de bloco**, com cada bloco aparecendo em uma **nova linha**.
     - Já os elementos de nível **inline** são dispostos na direção de conteúdo inline, ou seja, irão ficar numa mesma linha até não sobrar espaço, ponto esse que irão para uma nova linha.
  4. Colapso de margem: Se houver dois elementos adjacentes com margens que se tocam, as margens será colapsada.
