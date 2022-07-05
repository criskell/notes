# Box sizing

Links:

https://planflow.dev/blog/what-is-box-sizing-in-css-how-does-it-work

https://tympanus.net/codrops/css_reference/box-sizing/https://tympanus.net/codrops/css_reference/box-sizing/

https://www.devmedia.com.br/css-box-sizing/36830

https://levelup.gitconnected.com/css-box-sizing-property-and-how-it-works-f7ac1c3a76b0

https://webplatform.github.io/docs/css/properties/box-sizing/

http://sergiolopes.org/css-box-sizing-border-box/

https://aastudio.fr/box-sizing.html



- Determina como a largura e altura, totais, são calculadas
- Permite alterar o que compõem a largura e altura de um elemento
- `content-box` (modelo padrão):
  - `width` e `height` se aplica somente a área de conteúdo
  - a caixa se adapta para as bordas e preenchimentos, ou seja, são adicionadas à largura e altura especificada
  - a largura total é conteúdo + borda + preenchimento
  - a caixa se expande ao adicionar bordas ou preenchimentos
  - o preenchimento e borda fica fora da largura e altura especificada
- `border-box`:
  - `width` e `height` são aplicados incluindo conteúdo, preenchimento e borda
  - o conteúdo se adapta para acomodar as bordas e preenchimentos. a largura e altura é aplicada a caixa inteira
  - a largura total é a soma da largura do conteúdo (no mínimo 0, obtida através da subtração da soma de bordas e preenchimentos da largura especificada) + borda + preenchimento
  - a caixa tenta ao máximo não se expandir, com o conteúdo reduzindo
  - a caixa começa a medir sua altura e largura a partir da borda, e a área de conteúdo será reduzida
  - o preenchimento e borda fica dentro da largura e altura especificada