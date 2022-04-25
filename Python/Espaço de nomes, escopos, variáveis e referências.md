- Escopo e espaço de nomes

  - Cada objeto tem vários nomes.
  - Espaço de nomes é um mapeamento entre nomes e objetos.
  - Escopo é uma região textual de um programa que permite o **acesso direto** a um namespace.
  - Um namespace local é criado sempre para uma invocação de uma função.
  - Durante a execução, existem 3 ou mais escopos aninhados:
    1. Escopo local
    2. Escopos de funções delimitadoras
    3. Escopo global do módulo atual
    4. Escopo embutido
  - O escopo local fora de uma função é o escopo global do módulo.
  - Sem nenhuma declaração `nonlocal` e `global`, atribuições vão para o escopo mais interno.
  - Variáveis em escopos mais externos, sem nenhuma declaração, são somente leitura.
  - `nonlocal`: leitura e atribuições para o primeiro escopo que não é local nem global.
  - `global`: leitura e atribuições para o escopo que guarda os nomes globais.
  - Atribuições apenas vinculam nomes a objetos.

  ## Referências

  - Variáveis guardam referências.
  - O operador de atribuição copia o conteúdo da variável e o conteúdo da variável é uma referência.
  - O operador `==` compara o conteúdo da variável (referência).
  - A passagem de parâmetros copia o conteúdo da variável (referência), funciona como uma atribuição.