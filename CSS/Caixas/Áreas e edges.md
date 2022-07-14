# Áreas

- Cada caixa possui uma área de conteúdo e áreas circundantes de preenchimento, borda e margem
- Podem ser divididas em segmentos superior, direito, inferior e esquerdo
- O perímetro de cada área é chamada de `edge` e é dividida em 4 lados.



# Edges

- inner edge / content edge:
  - envolve a área de conteúdo e define a *caixa de conteúdo*
- padding edge:
  - envolve o preenchimento da caixa.
  - Se o preenchimento possuir 0 largura no determinado lado, a padding edge coincide com a content edge
  - Define a padding box, que contém as áreas de conteúdo e de preenchimento.

- border edge:
  - circunda a borda da caixa e define a `border box`, que contém as áreas de conteúdo, preenchimento e borda.

  - se a borda tiver largura zero num lado, irá coincidir com a padding edge neste lado.

- margin edge / outer edge:
  - A margem é delimitada pela *margin edge* ou *outer edge*
  - a *edge* da margem circunda a margem da caixa e define a **caixa de margem**, que contém as áreas de conteúdo, preenchimento, borda e margem.