# Como o CSS funciona

## Renderização

- Para renderizar um documento HTML com CSS, o navegador deverá **combinar informações de estilos** com o documento. Os passos, simplificados, são:
  1. Carregar o HTML.
  2. Converter o HTML para o DOM -- uma representação na memória do computador com uma estrutura semelhante a uma árvore.
  3. Carregar os arquivos vinculados no DOM como CSS e JS.
  4. O CSS é carregado, analisado (processo de *parsing*) e cada regra é aplicada a cada nó do DOM, resultando numa árvore de renderização.
  5. A árvore de renderização passa por um processo de layout onde ela é disposta na estrutura que deve aparecer na tela, com suas posições calculadas e etc.
  6. O processo de pintura começa a acontecer.
- Quando o CSS encontra alguma coisa que não conhece como propriedades, valores, ele ignora.

## Leitura de seletores

- Os navegadores leem um seletor da direita para a esquerda, ou seja, começa do **seletor-chave** (último seletor) e dado os combinadores, irá para o próximo(s) elemento(s).

  ```css
  /*
  Corresponde aos elementos do tipo `ul` que possui um ancestral correspondente ao seletor `body`
  */
  body ul {
      font-weight: bold;
  }
  ```

  