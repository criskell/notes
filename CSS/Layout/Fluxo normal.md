# Fluxo normal

- É a maneira padrão em que os elementos numa página web são dispostos se não houver alterações no layout.
- Caixas no fluxo normal faz parte de um contexto de formatação (bloco ou inline).
- Contexto de formatação de blocos:
  - Num contexto de formatação de bloco, os blocos são dispostos verticalmente sequencialmente.
- Contexto de formatação inline:
  - As caixas inline são dispostas horizontalmente.
- Dentro/fora do fluxo:
  - Dentro do fluxo:
    - Aparece na ordem do HTML.
    - Não está fora do fluxo.
  - Fora do fluxo:
    - Float, `position: fixed || absolute`, elemento `html`
    - Caixas que saíram de sua posição do fluxo normal e não possui uma interação com o conteúdo ao redor normal.
    - Itens fora do fluxo criam um novo contexto de formatação de blocos.
- Como funciona:
  1. Box model: O **box model** é aplicado.
  2. Aplicar o dimensionamento dos elementos `block` e `inline`:
     - Os elementos do nível de **bloco** preenchem todo o espaço na dimensão inline disponível no elemento que o contém e cresce na dimensão de bloco para acomodar seu conteúdo.
     - Já os elementos do nível **inline**, seu tamanho é o tamanho suficiente para acomodar seu conteúdo e não podemos alterar sua largura e nem altura, pois eles apenas vivem nos elementos de bloco.
  3. Fazer o layout dos elementos:
     - Os elementos de nível de **bloco** são dispostos na **direção do fluxo de bloco**, com cada bloco aparecendo em uma **nova linha**.
     - Já os elementos de nível **inline** são dispostos na direção de conteúdo inline, ou seja, irão ficar numa mesma linha até não sobrar espaço, ponto esse que irão para uma nova linha.
  4. Colapso de margem: Se houver dois elementos adjacentes com margens que se tocam, as margens será colapsada.
