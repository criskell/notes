# Integração do Grid

## Grid e Flexbox

- Grid se diferencia do Flexbox pois é um layout bidimensional ao invés de um layout unidimensional.

  - Controlamos (alinhamos, dimensionamos, etc) ao mesmo tempo linhas e colunas. Por exemplo:
    - Quero alinhar os itens na linha, mas eu quero também alinhar o item com os itens acima dele
  - As linhas do Flexbox são tratadas de forma independente, como se fosse um novo container flex, diferente do Grid.

- Grid trabalha principalmente a partir do layout ao invés do conteúdo. Diferente do Flexbox, que trabalha a partir de uma noção mais chegada ao conteúdo dos itens.

  - Mesmo que possamos dimensionar trilhas a partir do conteúdo, a trilha inteira é afeta, diferente do Flexbox.

- Flex-basis e fr:

  - A `fr` atribui uma proporção do espaço disponível para cada track, mas

  - ao invés de definir uma lista fixa de colunas, podemos utilizar a função `repeat` e imitar os comportamentos do Flexbox, junto com as quebras de linhas

  - Podemos utilizar as unidades `fr`, junto com `minmax` e `auto-fit` e ainda assim controlar as linhas e colunas ao mesmo tempo:

    - ```css
      .container {
          /**
          Primeiro o navegador irá quantas colunas de 200px (tamanho mínimo) caberão no container.
          As colunas sem conteúdo serão colapsadas para zero.
          Depois disso, o espaço disponível é compartilhado igualmente para todas as
          colunas.
          O minmax() representa um intervalo de tamanho.
          */
          grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      }
      ```

### Alinhamento

- As propriedades de alinhamento foram trazidas para a spec Box Alignment e podem ser utilizadas no grid, mas de forma adaptada.
- No Grid, podemos alinhar itens ao longo de sua área (que pode ser composta por uma célula ou mais).

## Grid e o posicionamento absoluto

- Ao posicionar de forma absoluta um item de grade, ele não irá participar do layout de grid:
  - dimensionamento
  - e o algoritmo de posicionamento automático
- Quando um item está posicionado de forma absoluta e o container está posicionado de forma relativa, este container irá ser o containing block.
- Se o item estiver posicionado numa área do grid, esta área será o containing block.
- Se um elemento absolutamente posicionado estiver aninhado num grid item que está posicionado numa área do grid e estabelece um contexto de posicionamento, o containing block será esta área do grid.

## Grid e o display

- O valor `contents` do `display` permite que um grid item não exiba mais sua caixa, e todos os seus filhos diretos (e assim os descendentes) são colocados em sua mesma posição, se tornando grid items.