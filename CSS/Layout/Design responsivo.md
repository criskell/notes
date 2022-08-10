# Design responsivo

- Responsive Web Design (RWD) é uma abordagem ao web design, que consiste num conjunto de práticas recomendas para adaptar um site para a variabilidade de dispositivos existentes.
  - Grids fluídas
  - Imagens fluídas
  - Media queries

## Tipos de layouts

- Layout fluído contém elementos dimensionados com medidas em porcentagem.
  - Vantagens:
    - O layout irá se adaptando de acordo com a largura do navegador.
  - Desvantagens:
    - Em telas menores, o layout fica esmagado
    - Em telas maiores, há linhas de textos maiores
- Layout fixo contém elementos dimensionados com medidas absolutas como `px`.
  - Vantagens:
    - Facilidade no design
    - Não temos o problema de layouts fluídos, onde em telas maiores, há linhas de textos maiores
  - Desvantagens:
    - Há muito espaço em branco nas bordas
    - Aparecimento de barras de rolagem

## Histórico

- *Camerom Adams* publicou um artigo em 2004 citando uma abordagem para criar layouts que mudam de acordo com a resolução da tela, com o uso de JS.
- *Zoe Mickley Gillenwater*: layout fluído + fixo
- *Ethan Marcotte* criou o termo *design responsivo* no blog *alistapart* e descreveu 3 técnicas
  - Grades fluídas
  - Imagens fluídas
  - Media queries

## Media queries

- Media queries executam uma série de testes sobre o dispositivo e aplica estilos dependendo do resultado.
- Breakpoint é ponto o qual um layout se altera quando uma media query é verdadeira.
- Mobile first consiste em começar com um layout para mobile e ir crescendo nos tamanhos de tela.

## Imagens fluídas

- Imagens fluídas são imagens que reduzem à medida que o seu container se torna menor, mas nunca crescem.
- Isso é alcançado por meio de `max-width: 100%`