# Geradores

- Geradores é um mecanismo para criar iteradores.
- São funções que retornam um objeto **generator**.
- Produz uma sequência de resultados.
- São escritos como funções que possuem `yield` (expressão), esta instrução retorna dados.
- Quando o `next` é executado, a função irá executar o código até uma instrução `yield`.

### Expressões de geradores

- Funcionam de forma semelhante a compreensões de listas, mas com parênteses ao invés de colchetes:

  ```python
  (x for x in range(5))
  ```

## Métodos e funções

- `x = next(g)`: Executa as **próximas** instruções no gerador até encontrar uma expressão `yield x`, retornando `x`. Na próxima vez que for chamado, irá continuar na próxima instrução do `yield`.
- `z = g.send(y)`: A expressão `yield x` irá avaliar para o valor `y` no gerador e as próximas instruções serão executadas até encontrar `yield z`, retornando `z`.
- `x = g.throw(e)`: Lança a exceção `e` no ponto em que o gerador parou e continua as próximas instruções do gerador, retornando `x` caso o gerador gere `x`. Se o gerador sair sem gerar um valor, a exceção será devolvida para o chamador.

## Declaração "yield from"

- Conecta geradores, delegando o trabalho de gerar valores para um subgerador.
- A declaração `yield from <iterable>` gera valores a partir de `iter(iterable)` para o chamador do gerador, além de receber valores do chamador e enviar para `iter(iterable)` através do método `iter(iterable).send`.
- `x = yield from <subgenerator>`: Se houver um `return y` em `<subgenerator>`, então `y = x` ao terminar o gerador.