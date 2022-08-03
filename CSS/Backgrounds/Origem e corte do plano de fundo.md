# Origem do plano de fundo

- Determina onde será a origem do posicionamento do plano de fundo.
- Valores:
  - `border-box`: A origem será no `top left` da *border box* do elemento.
  - `padding-box`: A origem será no `top left` do *padding box* do elemento. 
  - `content-box`

## Corte do plano de fundo

- Permite cortar um plano de fundo da área não especificada pela origem do plano de fundo.
- Valores:
  - `border-box`: Não haverá cortes.
  - `padding-box`: A imagem será cortada se sair da *padding box*.
  - `content-box`: A imagem será cortada ao sair da *content box*.