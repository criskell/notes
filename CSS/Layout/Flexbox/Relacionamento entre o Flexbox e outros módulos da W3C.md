# Relacionamento do Flexbox com outros módulos da W3C

## Box Alignment

- Este módulo define técnicas de alinhamento e justificação para todos os métodos de layout.
- O Flexbox reproduz propriedades de alinhamento e justificação que serão substituídos pelo módulo Box Alignment quando o mesmo for concluído.
- Todos os valores definidos neste módulo se aplicam ao Flexbox.
- Isto acontece para não atrasar o avanço da especificação do Flexbox.

## Modo de escrita

- O módulo do Flexbox tem consiência sobre a especificação do Modo de Escrita.
- Este módulo traz suporte aos diferentes modos de escritas existentes.

## Flexbox e outros métodos de layout

- Quando um elemento se torna um container flex, ele irá se comportar como um "block-level container" que estabelece um containing block, assim:
  - Floats não invadem
  - Margens do container não colapsam
- Além disso, quando elementos se tornam flex items, floats, clear e vertical-align não se aplicam e eles permanecem em fluxo normal

## Flexbox e Grid

- Flexbox é um modelo de layout unidimensional e Grid é um modelo de layout bidimensional.
- No Flexbox passamos bastante tempo configurando diretamente o dimensionamento dos itens enquanto no Grid passamos tempo configurando o dimensionamento diretamente no container.
- Ao alterar o tamanho de um item no Flexbox para se alinhar com os itens acima, podemos considerar um layout bidimensional (Grid).

## display: contents

- A especificação define um novo valor para `display`, este valor irá remover este elemento do processo de geração de caixas e de layout e seus descendentes serão movidos para cima para participar do layout em que o elemento estava participando.
- Casos de uso
  - Ter um wrapper somente para fins semânticos.

## Exercícios

1. O módulo "Box Alignment" define o que?
2. Por que a spec do Flexbox possui algumas propriedades do módulo *Box Alignment*?
3. Qual é a diferença essencial do sistema de Grid CSS e Flexbox?
4. Digamos que eu tenha um container flex multilinhas (`flex-wrap: wrap`) com 8 itens e 4 em cada linha, e eu estou alterando a largura de um elemento para alinhar com os elementos acima dele. Seria melhor eu usar Grid ou não? 
5. O que é o valor `contents` em `display`? 