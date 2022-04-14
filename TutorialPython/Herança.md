# Herança

- ```python
  class ClasseDerivada(<expressao>):
      pass
  ```

- Herança é um relacionamento entre classes, de forma que há uma classe que herda todas as características e comportamentos de outra.

- Dizemos: X (classe filha) é Y (classe mãe).

- `<expressao>` deve retornar um objeto de classe base.

- A definição de classes derivadas lembram da classe base.

- Se um atributo (de dados ou métodos) não for encontrado na classe derivada, irá ser procurado na classe base e assim sucessivamente até achar o atributo.

- Sobscrever um método é alterar seu comportamento.

- Toda classe herda da classe object, mesmo que implicitamente.

## super()

- `super()`

## Herança múltipla

- Definir várias classes bases.
- O problema do diamante ocorre quando temos uma classe A que herda de B e C tal que ambos herdam de D. Tendo um método m de A, sobrescrito em B e/ou C, qual método em B ou C deverá ser invocado?

## MRO

- O MRO é a ordem em que um método/atributo deve ser pesquisado em classes ancestrais.

## Mixin

- Mixin é uma classe com uma funcionalidade extra.