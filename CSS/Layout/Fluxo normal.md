# Fluxo normal

- É a maneira padrão em que os elementos numa página web são dispostos se não houver alterações no layout.
- Como os elementos são dispostos por padrão:
  1. O box model é aplicado, ou seja, toda margem, padding, borda e etc. é aplicada.
  2. Os elementos do nível de bloco preenchem todo o espaço na dimensão inline disponível no elemento que o contém e cresce na dimensão de bloco para acomodar seu conteúdo. Já os elementos do nível inline, seu tamanho é o tamanho suficiente para acomodar seu conteúdo e não podemos alterar sua largura e nem altura, pois eles apenas vivem nos elementos de bloco.
  3. Os elementos de nível de bloco são dispostos na direção do fluxo de bloco, com cada bloco aparecendo em uma nova linha. Já os elementos de nível inline são dispostos na direção de conteúdo inline, ou seja, irão ficar numa mesma linha até não sobrar espaço, ponto esse que irão para uma nova linha.
  4. Se houver dois elementos adjacentes com margens que se tocam, as margens será colapsada.
