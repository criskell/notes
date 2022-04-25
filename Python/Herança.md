# Herança

- ```python
  class ClasseDerivada(<expressao>):
      pass
  ```

- Herança é um relacionamento entre classes, de forma que há uma classe que herda todas as características e comportamentos de outra.

- Dizemos: A (classe filha/subclasse/classe herdeira) é B (classe mãe/superclasse/e as vezes ancestral).

- `<expressao>` deve retornar um objeto de classe base.

- A definição de classes derivadas lembram da classe base.

- Se um atributo (de dados ou métodos) não for encontrado na classe derivada, irá ser procurado na classe base e assim sucessivamente até achar o atributo.

- Sobscrever um método é alterar seu comportamento.

- Toda classe herda da classe object, mesmo que implicitamente.

## Função super

- `super()`

## Herança múltipla

- Definir várias classes bases, ou seja, herda atributos e métodos de várias classes pais.
- O problema do diamante ocorre quando temos duas classes de B e C tal que ambas herdam de A, e uma classe D que herda de B e C. Tendo um método m de A, sobrescrito em B e/ou C, qual método de A, B ou C deverá ser herdado por D?

## Method Resolution Order

- O MRO é a ordem em que um método/atributo deve ser pesquisado em classes ancestrais.

## Mixin

- Mixin é uma classe com uma funcionalidade extra.