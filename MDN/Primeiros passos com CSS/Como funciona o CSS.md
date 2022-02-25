# Como funciona o CSS

## Passos para renderizar um documento com CSS

- Para renderizar um documento HTML, o navegador deverá combinar o conteúdo com seus estilos.
- Processamento simplificado da renderização:
  - O navegador obtém o HTML.
  - Converte HTML para DOM.
  - Carrega os arquivos vinculados no DOM como imagens, CSS e JS.
  - O navegador analisa (faz o parsing) o CSS e então aplica cada regra a um nó do DOM de acordo com os seletores, construindo uma render tree.
  - A render tree é disposta na estrutura ordenada em que deve aparecer na página a partir das informações do CSS.
  - O navegador faz a pintura da render tree.
  - Diagrama: `Carrega o HTML -> Converte para DOM -> Carrega o CSS -> Analisa o CSS e aplica as regras para cada elemento de acordo com os seletores e cria uma render tree -> A render tree passa por um processo de layout -> A render tree é pintada na tela`

## DOM

- O DOM é uma representação do HTML que tem uma estrutura semalhante a uma árvore onde cada elemento, texto e atributo se torna um nó nesta árvore.

## CSS que o navegador não entende

- Quando um navegador encontra uma propriedade, valor ou seletor que não entende, ele ignora.
- Podemos usar fallbacks com isso junto ao efeito de cascata.
