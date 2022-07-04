# Modelo de caixa

- Tudo exibido pelo CSS são caixas.
- Comportamento das caixas:
  - `display`
  - dimensões definidas
  - seu conteúdo
- O modelo de caixa descreve como o margin, border e padding são adicionados a este retângulo.
- As áreas de margin, border e padding possui um perímetro chamado de edge. Cada edge define uma caixa.
- Se não definirmos um segmento (direito, esquerdo, cima, baixo) de uma área específica, a edge desta área tocará a edge da área anterior.
- O retângulo mais interno é a caixa de conteúdo e o mais externo é a caixa de margem.

## Dimensionamento da caixa

- `box-sizing`:
  - Especifica o dimensionamento da caixa.
  - Valores:
    - `content-box`: `width` e `height` incluem apenas o conteúdo.
    - `padding-box`: `width` e `height` incluem conteúdo + preenchimento.
    - `border-box`: `width` e `height` incluem conteúdo + preenchimento + borda.
- Modelo de caixa padrão (`box-sizing: content-box`):
  - Se adicionarmos `padding || border`, a largura/altura real da caixa não refletirá as propriedades `width` e `height`.