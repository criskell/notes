# Contextos de formatação

- Tudo na página faz parte de um contexto de formatação.
- Um contexto de formatação é um ambiente no qual um conjunto de caixas relacionadas são dispostas.
- Podemos pensar numa "área" que foi definida para dispor conteúdos de uma certa maneira.
- Cada contexto tem regras sobre como o layout deve se comportar neste contexto.
- Exemplos:
  - BFC: Irá dispor os elementos de acordo com as regras do layout de blocos.

## Contexto de formatação de bloco

- Um BFC se comportará como um mini-layout dentro do layout, contendo tudo dentro dele.
- `float` e `clear` somente aplicam para elementos no mesmo BFC.
- Margens colapsam somente com elementos no mesmo BFC.
- Contém floats, ou seja, a altura não temos o problema da altura colapsando.

- O elemento mais externo que utiliza regras de block layout em um documento estabelece o primeiro ou o **contexto de formatação de bloco inicial**.
- No elemento `html`, cada elemento irá seguir o fluxo normal, de acordo com as regras de layout `block & inline`.
- Também outros elementos podem criar BFC, contanto que atendam certas condições.
- `display: flow-root`:
  - Estabelece um novo BFC para os descendentes da caixa.
  - O nome `flow-root` refere-se o fato de que a caixa se comportará como um elemento raiz, dado como o layout irá funcionar dentro dele e como o contexto foi criado.

## Contexto de formatação inline

- Existem dentro de outros contextos de formatação
- Podemos pensar como um contexto de um parágrafo
- As caixas dentro deste contexto não tem o modelo de caixas totalmente aplicado:
  - Margens horizontais, paddings horizontais e bordas horizontais serão **aplicadas** e **empurrão** outros elementos horizontalmente.
  - Margens verticais não serão aplicadas.
  - Paddings horizontais e bordas horizontais serão aplicadas mas não farão outros elementos se moverem, de forma que irá ocorrer sobreposição. Isso é devido que as caixas de linha não são empurradas por bordas e paddings.
