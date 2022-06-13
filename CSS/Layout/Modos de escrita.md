# Modo de escrita

- A especificação CSS define como a alteração no modo de escrita afeta o flow layout.
- direção base inline (`inline base direction`):
  - direção em que o conteúdo é colocado numa linha. 
  - define o início e o fim da direção inline.
  - o início é onde as frases começam e o fim é onde as linhas de texto terminam.
- direção de blocos (`block flow direction`):
  - direção em que os blocos se empilham.
  - alterando via `writing-mode`, altera a direção inline também.
- Direção do caractere é a direção para qual um caractere aponta.

## Propriedade writing-mode

Os valores desta propriedade controlam o fluxo dos blocos:

- horizontal-tb: significa uma direção de blocos de cima para cima e a direção inline horizontal
- vertical-rl: direção de blocos da direita para a esquerda com uma direção inline vertical
- vertical-lr: direção de blocos da esquerda para a direita com uma direção inline vertical

## Caixas com um modo de escrita diferente do pai
- Caixas inline-level -> inline-block

- Caixas block-level:

  - estabelecem um BFC.
  - ou seja, se o *inner display type* for *flow*, irá ser convertido para *flow-root*.

## Elementos substituídos

- Não alterão sua orientação por causa do modo de escrita. Devem corresponder ao modo de escrita.

## Propriedades e valores lógicos
- As propriedades e valores logicos mapeiam para as direções de bloco ou inline e não para direções físicas.
- Isso torna útil para escrever componentes que funcionam para diferentes modos de escrita.