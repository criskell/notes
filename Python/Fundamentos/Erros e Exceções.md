# Erros e exceções

- Existem dois tipos de erros que podem ocorrer: **erros de sintaxe** e **exceções**.

## Erros de sintaxe

- Erros de sintaxe são erros que ocorrem devido que uma expressão ou sentença não está sintaticamente correta.

## Exceções

- Exceções são erros que ocorrem durante a execução.

- Exemplo de **mensagem de erro** de uma exceção:

  ```python
  Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
  TypeError: can only concatenate str (not "int") to str
  ```

- A última linha apresenta **o que aconteceu**.

- O **traceback** apresenta o **contexto** de **onde** ocorreu a exceção.

## Tratamento de exceções

- O tratamento de exceções é feito com a declaração `try`.

  ```python
  try: # esta e a clausula try
  	x = int('x')
      estaLinhaNaoSeraExecutadaNunca()
  except ValueError: # esta e a clausula except ou de excecao
      print('oi')
  ```

- A cláusula `try` primeiro é executada e se houver alguma exceção ocorrida numa determinada instrução, as instruções seguintes a ela serão ignoradas e as cláusulas `except` serão testadas para verificar se correspondem com a exceção.

- Se uma cláusula `except` for encontrada, todas as instruções dela serão executadas e a execução continua após a a instrução `try`. Caso contrário, a exceção continuará para uma instrução `try` mais externa e as instruções seguintes a declaração `try` serão ignoradas.

- Uma classe numa cláusula `except` é compatível com uma exceção se for a mesma classe ou se for uma classe base dela.

- A cláusula `else` pode ser utilizada para executar código quando não houver exceção na cláusula `try`.

- A exceção pode ter zero ou mais argumentos **associados**.

- Os tratadores de exceções podem capturar exceções não tratadas do interior de funções invocadas (mesmo que a função foi invocada indiretamente) dentro de uma cláusula `try` , por exemplo:

  ```python
  def f():
      g()
      
  def g():
      1 / 0
  
  try:
  	f()
  except ZeroDivisionError:
      print("Divisão por zero")
  ```

- Podemos obter a instância da exceção adicionando um nome de uma variável após o nome da exceção na cláusula de exceção, precedido por `as`. Exemplo: `except ZeroDivisionError as e:`

- As instâncias de exceções definem o método `__str__` para exibir os argumentos da exceção.

- Os argumentos da exceção, convertidos para string com `__str__`, são exibidos no "detalhe" da mensagem.

## Levantando exceções

- A declaração `raise` permite levantar uma exceção.
- O argumento da instrução `raise` indica a exceção. Pode ser uma instância ou classe.
- Uma instrução `raise` sozinha dentro de uma cláusula de exceção permite levantar a exceção novamente.

## Encadeamento de exceções

- O encadeamento de exceções é levantar uma exceção ligada a uma outra exceção que foi a causadora dela.
- Podemos encadear uma exceção causadora a outra com `raise NovaExcecao from ExcecaoCausadora`.
- Numa cláusula `except` ou `finally`, o encadeamento de exceções acontece automaticamente quando uma exceção for levantada nela. Para desativar isso quando uma exceção é diretamente levantada na cláusula utilizamos `raise x from None`.

## Cláusula finally

- A instrução `try` pode conter uma cláusula `finally` que é **sempre** executada como a **última tarefa** antes da conclusão da instrução `try`, independentemente da ocorrência ou não de exceções. Com isso:
  - Quando ocorre uma exceção não tratada por nenhuma cláusula `except` ou quando ocorre em cláusulas `except` e `else`, a cláusula `finally` é executada e depois a exceção é levantada ou re-levantada.
  - Quando uma instrução `break`, `return` ou `continue` é encontrada na cláusula `try`, a cláusula `finally` é executada antes da execução da instrução.
  - Quando uma instrução `break`, `return` ou `continue` é encontrada na cláusula `finally`, exceções não são levantadas.
- Casos de uso: liberar um recurso mesmo que um erro ocorre.

## Ações de limpeza pré-definidas

- Alguns objetos como arquivos definem ações de limpeza padrões.
- A instrução `with` permite utilizar um objeto e que ao terminar de utilizar ele, executar a ação de limpeza do objeto sempre, mesmo que ocorra um erro.
