# Espaço de nomes

- Cada objeto tem vários nomes.
- Namespace é um mapeamento entre nomes e objetos.
- Tipos de namespaces:
  - Built-in:
    - Contém nomes built-in.
    - O Python cria ao iniciar e destrói ao finalizar
  - Global:
    - Contém nomes dos módulos.
  - Delimitador:
    - Namespace de uma função que contém outra função.
  - Local:
    - Contém nomes locais de funções.
    - Criado sempre que uma função é executada.

# Escopo

- Escopo é uma região textual de um programa que permite o acesso direto a um namespace.
- Traz uma cadeia implícita de namespaces: define **quais** namespaces serão examinados e em que **ordem**.
- Quando dizemos que `x` está no escopo de uma função, dizemos que `x` está no namespace local ou em outros namespaces.
- Durante a execução, pode existir 2 ou mais escopos aninhados:
  - **L**ocal
  - **E**nclosing: Funções delimitadoras
  - **G**lobal
  - **B**uilt-in
- `nonlocal`: leitura e atribuições para o primeiro escopo que não é local nem global.
- `global`: leitura e atribuições para o escopo que guarda os nomes globais.
- Sem nenhuma declaração `nonlocal` e `global`, atribuições vão para o escopo mais interno.
- Variáveis em escopos mais externos, sem `global` ou `nonlocal`, são somente leitura.
- Atribuições apenas vinculam nomes a objetos.

## Referências

- Variáveis guardam referências.
- O operador de atribuição copia o conteúdo da variável e o conteúdo da variável é uma referência.
- O operador `==` compara o conteúdo da variável (referência).
- A passagem de parâmetros copia o conteúdo da variável (referência), funciona como uma atribuição.

## Variáveis

- Variáveis são nomes simbólicos que são referências para objetos.
- Atribuir um nome a um objeto (ex.: `x = ...`), cria uma *binding* do nome `x` para o objeto `...`.
- Argumentos são passados para parâmetros via atribuição, ou seja, os parâmetros são apenas outros nomes para os objetos passados via argumentos e fazer uma *reatribuição* dos parâmetros alteram apenas para qual objeto o parâmetro aponta.
- Cada parâmetro se torna um novo apelido.