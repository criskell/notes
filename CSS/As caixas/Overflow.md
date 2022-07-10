# Overflow

Um overflow ocorre quando um conteúdo vaza das dimensões fixas da caixa.

Controlando o estouro (conteúdo que vaza):

- `visible`:
  - o estouro é visível
  - pode ser visto fora da caixa de preenchimento
- `hidden`:
  - o conteúdo é cortado ao sair da padding box
  - permite scroll apenas via JS
  - estabelece um BFC
- `scroll`:
  - o conteúdo é recortado para caber na padding box
  - aparece um scoll para visualizar o estouro, mesmo que o conteúdo não seja recortado.
  - estabelece um BFC
- `auto`:
  - aparece o scroll somente se for necessário
  - se o conteúdo caber na padding box, se comporta como visible. caso contrário, irá aparecer scrolls
  - estabelece um BFC