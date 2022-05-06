# Imagens, mídia e elementos de formulário

- Replaced elements são elementos que não possuem seu layout interno alterado.
  - Possuem um aspect ratio (proporção).
  - Exibido com suas dimensões intrínsicas, por padrão.
  - `max-width: 100%` em replaced elements: A imagem ficará menor proporcionalmente se as dimensões intrínsicas ultrapassarem a largura do pai. 
  - Dimensionando replaced elements em caixas pai: `object-fit`
    - cover: O elemento irá ser dimensionado de forma que **preencha** completamente a caixa, mantendo a proporção mas pode ser que partes não sejam exibidas.
    - contain: Se tornará menor para **caber** na caixa.
- Estilos de fontes não herdam por padrão em alguns navegadores.