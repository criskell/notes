# Iteradores e iteráveis

- Iterável é um objeto capaz de retornar um item de cada vez. Possui um método `__getitem__` ou `__iter__`, que retorna um iterador.
- Iterador:
  - Representa um fluxo de dados
  - Define como fazer a iteração (`__next__`) de um iterável
  - Lembra do estado da iteração
  - Iteradores são iteráveis: devem possuir um método `__iter__` que retorna ele próprio.
  - `next`: Retorna o próximo item no iterador e altera o iterador para apontar para o próximo elemento.

- Tipos de iterações:
  - Definida: Iteração com a especificação do número de repetições. `for`
  - Indefinida: Iteração com a repetição de um bloco de código até que uma condição seja atendida. `while`
- Loop for:
  - O `for` é um loop de **iteração definido** baseado em iteradores (ou coleções).
  - Ao receber um iterável, usa a função `iter` para obter um iterador.
  - Para cada chamada `next()`, associa o objeto retornado à variável de loop.
  - Termina a iteração quando recebe uma exceção `StopIteration`.
- `iter` retorna um iterador de um iterável.
- Iteradores são preguiçosos, ou seja, não gera um objeto a menos que solicitado.