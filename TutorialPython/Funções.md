# Funções

- Bloco de código nomeado que pode ser chamado dado alguns argumentos (dados) e retornar outros dados (valor de retorno).

## Definição de funções

- Para criar uma função é necessário o uso da palavra-chave def:

```python
def <nome-funcao>(<parametros-formais>):
    <corpo-da-funcao>
```

- O que fica entre parênteses são os parâmetros formais.

### Docstrings

- Docstrings são strings que são colocadas na primeira linha do bloco da função e são utilizadas para documentação.

```python
def soma(x, y):
    """soma dois numeros"""
    return x + y
```

## Execução de funções

- Ao executar uma função, uma tabela de símbolos é criada para armazenar variáveis locais da função.
- As funções possuem escopo léxico.
- Argumentos são passados por valor, onde valor é uma referência para algum objeto.
- Caso não haja um valor de retorno explícito, o padrão é None.

## Instrução return

- Finaliza a execução de uma função e retorna para a função chamadora.
- A instrução return sem qualquer argumento retorna None.

## Argumentos padrão

- Cada parâmetro pode receber um argumento padrão:

```python
def minhaFuncao(argumento=valorPadrao):
    pass
```

- Os argumentos padrões dos parâmetros são avaliados no momento em que a definição é avaliada, no escopo da definição.
- Chamado de argumento opcional.

## Argumentos nomeados (keyword arguments)

- Argumentos nomeados são argumentos passados com o nome do parâmetro:

```python
exemploFuncao(1, nomeDoArgumento=valor)
```

## Parâmetros especiais

- Os tipos de parâmetros podem serem somente posicional, posicional ou nomeado ou somente nomeado.
- Podemos especificar o tipo de parâmetro para os argumentos serem passados **somente-posição** ou **somente-nome** utilizando os símbolos `/` e `*`.
- Se não especificados, os argumentos poderão ser passados por **nome ou posição**.

### Parâmetros somente-posição

- Para parâmetros serem somente-posição, coloque eles depois de uma `/`:

  ```python
  def somentePosicao(x, y, /):
      pass
  ```

### Parâmetros somente-nome

- Para parâmetros serem somente-nome, coloque `*` antes deles:

```python
def teste(*, somenteNomeado, somenteNomeado2):
    pass
```



## Empacotamento de argumentos

- Empacotar argumentos é o processo em que juntamos todos os argumentos não correspondidos com um parâmetro numa única variável.

- Parâmetros formais no formato `*args` recebe todos os **argumentos posicionais** com exceção dos **parâmetros já correspondidos**.

- Parâmetros formais no formato `**kwargs` recebe todos os **argumentos nomeados** com exceção dos **parâmetros já correspondidos**.

- Depois destes parâmetros **variádicos**, os parâmetros formais são somente-nomeados.

- Parâmetros **somente-posicionais** podem serem utilizados no parâmetro `**kwargs` sem ambiguidade:

```python
def exemplo(name, /, **kwargs):
    print('name' in kwargs)
    
exemplo(10, **{'name': 'sem ambiguidade'})  # nao vai da erro, vai retornar True
```

## Desempacotamento de iteráveis de argumentos

- Podemos "desempacotar" argumentos posicionais a partir de um iterável e passar para uma função utilizando o operador `*`:

```python
print(*["mensagem 1", "mensagem 2"])
```

- Podemos fazer o mesmo com um dicionário para passar argumentos nomeados, mas utilizando a sintaxe `f(**dicionario)`:

  ```python
  def exemploFuncao(x, y):
      return x + y
  
  exemploFuncao(**{'y': 10, 'x': 20})
  ```



## Expressões lambda

- Podemos criar objetos funções de uma forma mais simples e com menos linhas utilizando expressões lambda.
- Essas funções não possuem nomes e possuem somente uma linha.
- Possuem escopo léxico.