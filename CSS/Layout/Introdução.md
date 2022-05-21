# Layout

- As técnicas de layout nos permitem posicionar um elemento numa página em relação aos seguintes fatores:
  - Sua posição no fluxo normal.
  - O container pai.
  - Elementos ao redor dele.
  - Viewport e janela.
- Técnicas de layout:
  - Fluxo normal:
    - Fluxo normal é como o navegador apresenta por padrão os elementos de uma página quando não há nenhum controle dos elementos via CSS.
    - Aqui o HTML é exibido na ordem exata que aparece no código-fonte.
  - Propriedade `display`:
    - Podemos alterar como os elementos são dispostos no fluxo normal, por exemplo: um elemento de nível bloco de comportamento como elemento de nível inline.
      - `inline-block`: A caixa tem algumas características de bloco, mas flui como um conteúdo inline.54
    - No fluxo normal, os elementos possuem um valor padrão para esta propriedade que diz como deverão se comportar.
    - Além disso, permite habilitar layouts mais complexos como Flexbox, Grid e etc.
  - Float:
    - Permite alterar o comportamento de um elemento e dos elementos do tipo bloco que o seguem.
    - O elemento flutuante é movido para esquerda ou direita e o conteúdo ao redor flutua em torno dele.
  - Flexbox:
    - Flexbox é um nome de um módulo CSS que permite facilitar o layout unidimensional de elementos no eixo horizontal ou vertical.
    - O flex converte os elementos filhos em itens flexíveis e o elemento pai passa a se chamar container flexível.
    - A propriedade `flex` especifica como um item deve aumentar ou diminuir.
    - Comportamento padrão:
      - o Flex irá alinhar os elementos um ao lado do outro na direção inline e faz esticarem na direção em bloco até terem a mesma altura.
      - Os itens ficarão no mesmo eixo e não quebrarão se ficarem sem espaços, se espremendo o máximo possível.
  - Grid:
    - Permite o layout em duas dimensões, em linhas e colunas.
    - Propriedades:
      - `display: grid`: Habilita o Grid.
      - `grid-template-rows`: Define faixas de linhas.
      - `grid-template-colunas`: Define faixas de colunas.
  - Propriedade `position`:
    - Permite mover um elemento de onde ele ficaria no fluxo normal para outro local.
    - Valores:
      - `static`: Posicionar o elemento no seu lugar padrão.
      - `relative`: Mover o elemento em relação a sua posição no fluxo normal.
      - `absolute`:
        - Move o elemento completamente para fora do fluxo normal e posiciona usando os deslocamentos das bordas de um bloco que o contém (containing block).
        - Os elementos agem como se não existisse.
      - `fixed`:
        - Fixa um elemento em relação à viewport.
      - `sticky`:
        - Combina `fixed` + `static`.
        - Ao rolar a página, ele ficará `static` até atingir a viewport. Depois disso, fica `fixed`.
  - Layout de tabelas:
    - Permite adicionar um layout de tabela no CSS, utilizando elementos não relacionados a tabelas. Isso também é chamado de tabelas CSS:
    - Declarações:
      - `display: table`: Exibe como uma tabela.
      - `display: table-row`: Exibe como uma linha da tabela.
      - `display: table-cell`: Exibe como uma coluna da tabela.
      - `display: table-caption`: Exibe como uma legenda da tabela.
      - `caption-side: <side>`: Permite alterar o lado da legenda. 
  - Layout de múltiplas colunas:
    - Permite dispor o conteúdo de um elemento em várias colunas.
    - Para ativar:
      - `column-count`: Qtd. de cols.
      - `column-width`: O browser irá criar o **maior** número possível de colunas usando a largura especificada.



## Perguntas

1. O que são técnicas de layout?
2. O que é o fluxo normal?
3. O que são tabelas CSS?
4. O que é float?