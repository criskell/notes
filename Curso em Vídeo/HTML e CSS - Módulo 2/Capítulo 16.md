# Capítulo 16

## Modelo de caixas

- Todo elemento no HTML é exibido como uma caixa. Esta caixa pode conter ou ser contida por caixas.

### Anatomia de uma caixa

- Cada caixa possui (de dentro pra fora):
  - Conteúdo: O conteúdo possui largura e altura. O par largura e altura é chamada de box-size.
  - Preenchimento: O espaço entre o conteúdo e a borda.
  - Borda: Um contorno que circunda o conteúdo.
  - Outline: Um outro contorno que circunda as camadas anteriores.
  - Margem: Um espaço da borda (ou outline) para fora.

### Classificação de caixas

- Uma caixa pode ser:
  - Block-level: Ela inicia e termina com uma nova linha, ocupa todo o espaço do elemento que o contém.
  - Inline-level: Ela não inicia e nem termina uma nova linha, e ocupa o espaço necessário para que seja exibido. Geralmente ocupa pequenos espaços.

### Grouping tags

- Grouping tags são tags que agrupam elementos em partes de um layout.

#### Tags

- header: Área relativa a cabeçalhos do site, artigos, etc.
- nav: Contém links de navegação.
- main: Agrupa o conteúdo principal do site.
- section: Define uma seção de conteúdo na página.
- article: É um conteúdo que contém um mesmo assunto e que pode ser lido de forma independente.
- footer: Rodapé do site.
- aside: Área de conteúdo periférico e complementar a um artigo ou seção.

##  Caixas com vértices arredondados

- Podemos arrendondar vertíces da borda de caixas com a propriedade `border-radius`.
- Utilizando com dois argumentos: `x y`
  - Topo superior esquerdo e topo inferior direito é igual a x.
  - Topo superior direito e topo inferior esquerdo é igual a y.
- Utilizando com quatro argumentos: `a b c d`
  - Topo superior esquerdo é igual a `a`.
  - Topo superior direito é igual a `b`.
  - Topo inferior direito é igual a `c`.
  - Topo inferior esquerdo é igual a `d`.

## Bordas personalizáveis

- Podemos personalizar bordas com imagens com as propriedades `border-image-*`.