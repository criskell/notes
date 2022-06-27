# Tabelas

- Tabela é um conjunto de dados estruturados em linhas e colunas (chamados de dados tabulares).
- O conteúdo de uma tabela fica no elemento `table`.
- Por que são importantes:
  - Permite encontrar um valor que facilmente estabelece uma relação entre diferentes tipos de dados
  - São interpretadas facilmente associando cabeçalhos de linha e/ou colunas com os dados, por pessoas **visuais**.
- Podem ser aninhadas uma dentro da outra, mas isso não é recomendado.

## Células, cabeçalhos e linhas

- `tr`: representa uma linha na tabela.
- `td`:
  - O menor container de uma tabela é uma célula, criada pelo elemento `td`.
  - Se não houver uma linha envolvendo, cada `td` ficará automaticamente numa mesma linha, alinhados.
- `th`:
  - O elemento `th` representa um cabeçalho de uma tabela, semanticamente e visualmente.
  -  Um cabeçalho de uma tabela é uma célula especial, que fica no início de uma linha ou coluna, que indica o tipo de dados que se segue na linha ou coluna.
  - Por que são importantes?
    - O design parece bem melhor, geralmente
    - Ajuda a encontrar dados mais facilmente
    - Ajuda na acessibilidade: permite ler de uma vez todos os dados de uma linha ou coluna de um cabeçalho.

## Mesclagem de células

- `colspan`: estende a célula em N colunas
- `rowspan`: estende a célula em N linhas.

## Estilos comuns para colunas

- o elemento `col` permite especificar um estilo para uma coluna inteira, sem repetição de código.
- O atributo `span` estende esta coluna para N colunas, especifica o número de colunas em que deseja aplicar o estilo.
- Cada `col` deve estar num `colgroup`.
- Especifique todas as colunas, talvez?

## Legendas

- Fornecem uma descrição da tabela.
- Logo abaixo da tag de abertura `table`.

## Estrutura

- Por que utilizar uma marcação estrutural:
  - Para facilitar o entendimento do código
  - Para selecionar seções da tabela diretamente via CSS ou JS
- `thead`:
  - Envolve o conteúdo de cabeçalho.
  - Deve estar abaixo do `colgroup`
- `tbody`:
  - Envolve o conteúdo da tabela que não é cabeçalho nem rodapé.
- `tfoot`:
  - Envolve o conteúdo de rodapé.
  - Mesmo que não esteja no final da tabela, no código, o navegador irá renderizar na parte inferior da tabela.
  - Exemplos: Somatório

## Acessibilidade

- Semântica: Utilizar cabeçalhos de linhas e de colunas

- `scope`:

  - Atributo de `th`
  - Define para qual células este elemento é um *cabeçalho*
  - `row`: cabeçalho para a linha de onde está
  - `col`: cabeçalho para a coluna de onde está.
  - `colgroup`: cabeçalho que é um título que fica no topo de um grupo de colunas (outros cabeçalhos de subtítulos)
  - `rowgroup`: cabeçalho que é um título para outros cabeçalhos de linha que são subtítulos

- `headers`:

  - Atributo de `td`
  - Define quais são os cabeçalhos de uma célula, pelo IDs separados por espaços
  - Alternativa ao atributo `headers`

  