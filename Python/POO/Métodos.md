# Métodos

- Bound method:

  - Método ligado a uma instância de uma classe.
  - Chamada a um bound method -> (é transformado) Chamada a um unbound method
  - `obj.method()` -> `type(obj).method(obj)`
  - Ao acessar uma função numa instância de uma classe, esta função é transformada num `bound method`.

- Unbound method: Método não ligado a uma instância de uma classe.

  