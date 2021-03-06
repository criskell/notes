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

- Dado uma subclasse (opcional) e uma instância desta subclasse (opcional), o `super([type, [, object-or-type]])` irá retornar um objeto proxy que delega chamadas a métodos para os métodos de outra classe.
- Delega chamadas a métodos para uma classe pai ou irmã de `type`.
- `object-or-type` determina o MRO.
- Chama o próximo método no MRO.
- Se passar uma instância de uma classe em `object-or-type`, o MRO será de `type(object-or-type)`.
- A busca é feita nas classes que ficam depois de `type` no MRO.
- `super() = super(__class__, self)`

## Herança múltipla

- Definir várias classes bases, ou seja, herda atributos e métodos de várias classes pais.
- O problema do diamante ocorre quando temos duas classes de B e C tal que ambas herdam de A, e uma classe D que herda de B e C. Tendo um método m de A, sobrescrito em B e/ou C, qual método de A, B ou C deverá ser herdado por D?
- Herança múltipla cooperativa:
  - "Na herança múltipla cooperativa, você escreve algumas classes, cada uma implementando um pequeno conjunto de recursos e, em seguida, herda dessas classes para criar várias combinações diferentes de recursos."


## Method Resolution Order

- O MRO é a ordem em que um método/atributo deve ser pesquisado em classes ancestrais.
- o Python utiliza o algoritmo **C3 linearization** para gerar o MRO.
- Resumo:
  - Se uma classe possui múltiplos pais, a ordem dos pais no **MRO** permanecerá a mesma.
  - Uma classe filha sempre precede os pais.


## Mixin

- Mixin é uma classe com uma funcionalidade extra.