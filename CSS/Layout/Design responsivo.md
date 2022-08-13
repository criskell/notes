# Design responsivo

- Responsive Web Design (RWD) é uma abordagem ao web design, que consiste num conjunto de práticas recomendas para adaptar um site para a variabilidade de dispositivos existentes.
  - Grids fluídas
  - Imagens fluídas e imagens responsivas
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

- *Cameron Adams* publicou um artigo em 2004 citando uma abordagem para criar layouts que mudam de acordo com a resolução da tela, com o uso de JS.
- *Zoe Mickley Gillenwater*: layout fluído + fixo
- *Ethan Marcotte* criou o termo *design responsivo* no blog *alistapart* e descreveu 3 técnicas
  - Grades fluídas
  - Imagens fluídas
  - Media queries

## Media queries

- Media queries executam uma série de testes sobre o dispositivo e aplica estilos dependendo do resultado.
- Breakpoint é ponto o qual um layout se altera quando uma media query é verdadeira.
- Mobile first consiste em começar com um layout para mobile e ir crescendo nos tamanhos de tela.

## Imagens responsivas

- Imagens *fluídas* são imagens que reduzem à medida que o seu container se torna menor, mas nunca crescem.
- Isso é alcançado por meio de `max-width: 100%`
- Há desvantagens nesta abordagem:
  - Desperdiço de largura de banda
  - Querer um aspect ratio diferente para diferentes dispositivos
  - Exibir uma imagem melhor adequada (por exemplo, mostrando os detalhes principais) em diferentes dispositivos
- Alternativamente, podemos utilizar imagens **responsivas** alcançadas por meio do elemento `picture` e dos atributos `srcset` e `sizes` do elemento `img`, junta com outras técnicas como esta

## Grades flexíveis

- Não segmentamos todos os dispositivos para criar um layout com um "pixel perfeito"
- Ao invés disso, utilizamos poucos breakpoints ativados quando o conteúdo começa a ficar ruim, neste momento alteramos todo o layout
- As seguintes tecnologias são responsivas por padrão e permitem criar uma grid flexível:
  - Multicol:
    - Informando `column-width`, criará tantas colunas quantas puderem caber no container, e então distribuirá o espaço disponível.
  - Flexbox:
    - A flexibilidade de uma grid é alcançada utilizando as propriedades `flex-grow/shrink/basis`
    - Os itens irão crescer ou diminuir conforme a quantidade de espaço disponível
  - Grid:
    - A flexibilidade pode ser alcançada utilizando a unidade `fr`

### Convertendo um layout pixel para flexível

- Fórmula: target / contexto = resultado
- Exemplo:
  - Coluna de `60px` em um contexto (o container) de `180px`, será `60 / 180 = 0.33333333333`, e convertendo em porcentagem (movendo o ponto para duas casas à direita): `33.333333333%`

## Tipografia responsiva

- Alterar o tamanho das fontes de acordo com a quantidade de espaço.
- Abordagens:
  - Breakpoints
  - Unidades da viewport:
    - Utilizando as unidades de viewport para dimensionar uma fonte, o tamanho da fonte estará em função da viewport.
    - Mas estando em função apenas à viewport, isto não permitirá que o usuário aplique o zoom.
    - Solução: `calc(<unidade que o usuario pode ampliar> + <unidade da viewport>)`

## Elemento meta

- `viewport` é um tipo de elemento meta que podemos utilizar para configurar a viewport. Recebe um conjunto de parâmetros no formato `nome1=valor1, nome2=valor2, nomeN=valorN`. Parâmetros disponíveis:
  - `width`:
    - Define a largura da viewport.
    - O valor `device-width` faz com que corresponda à largura do dispositivo.
  - `initial-scale`:
    - Define o zoom inicial do site.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`:
  - Sem este elemento definido no HTML, o navegador em dispositivos mobile irão mentir sobre a largura da viewport, e definir para uma largura maior que do dispositivo, por exemplo: `960px` e diminuirão o zoom da página.
  - Isso foi feito por que quando os celulares foram lançados, os sites não eram otimizados para dispositivos móveis. A Apple foi a precursora disso.
  - Definir o elemento acima previne este comportamento do celular.

## Exercícios

1. O que é design da web responsivo (Responsive Web Design - RWD)? É apenas uma tecnologia do CSS ou engloba o HTML também?
2. Quais são os dois tipos de layouts que podemos criar com `px` e `%`?
3. O que são imagens *fluídas* e quais são as desvantagens? Cite 3 técnicas para criar imagens responsivas.
4. O que são media queries, breakpoints e o mobile-first design?
5. O que são grades flexíveis? Além de um layout que podemos alcançar por meio de múltiplas colunas CSS, quais são as outras 3 técnicas que podemos usar?
6. Como converter um layout em pixels para porcentagem?
7. O que é tipografia responsiva? Como podemos criar tipografia responsiva sem a utilização de media queries e breakpoints, mesmo assim mantendo a *acessibilidade* para que o usuário possa aumentar ou diminuir o zoom da fonte?
8. Quais são as ferramentas que temos a disposição para criar RWD? Cite pelo menos 5.
9. Qual é o comportamento do dispositivo mobile quando o elemento `meta` do tipo *viewport* não é definido? Por que há este comportamento, de onde surgiu? Qual é a solução para isso?