# Descriptors

- Descriptors descrevem atributos de um objetos.
- Se um objeto tem pelo menos um método do protocolo descriptor, é dito que este objeto é um descriptor.
- O comportamento padrão é obter, atualizar ou excluir um atributo do dicionário de um objeto (`__dict__`).
- Se na cadeia de pesquisa encontrar um descriptor, o Python substituirá seu comportamento padrão pelo comportamento definido em algum método.
- Só funcionam quando colocados em variáveis de classes e não em variáveis de instância.

## Métodos `__getattr__` e `__getattribute__`

- `obj.__getattr__(self, key)`: Chamado se não for possível encontrar um atributo da maneira usual.
- `obj.__getattribute__(self, key)`: Chamado sempre quando ocorre um acesso a um atributo.

## Cadeia de pesquisa

- Todo objeto no Python possui um dicionário `__dict__` que contém todos os atributos do objeto.
- Um objeto é uma classe, portanto possui um atributo `__dict__` que contém todos os métodos e atributos da classe.
- Cadeia de pesquisa de atributos ao acessar com notação de ponto:
  1. Pesquisa em `obj.__dict__`
  2. Se não encontrar, pesquisa em `type(obj).__dict__`
  3. Se não encontrar, pesquisa nas classes bases de `type(obj)` no MRO.
- Ao escanear a cadeia de namespaces, a precedência irá ser de:
  1. Data-descriptors
  2. Variáveis de instância
  3. Non-data descriptors e Variáveis de classes
- Os métodos somente serão chamados se a instância da classe do descriptor aparecer no dicionário da classe proprietária ou no dicionário das classes pais.

## Protocolo de descriptor

- O protocolo, de um modo geral, consiste nos seguintes métodos:

  ```python
  descriptor.__get__(self, obj, type=None) -> value
  descriptor.__set__(self, obj, value) -> None
  descriptor.__delete__(self, obj) -> None
  ```

## Tipo de descriptors:

- descriptor de não-dados: Tem somente `__get__`.
- descriptor de dados: Possui `__set__` e/ou `__delete__`.

### Métodos

- **`d.__get__(self, owner, type)`**: Obtém o valor do descritor. Onde:
  - `owner`: Objeto o qual o descritor está sendo acessado ou `None` se estiver sendo acessado por uma classe.
  - `type`: Tipo do objeto.
- **`d.__set__(self, obj, value)`**:  Altera o valor.
- **`d.__delete__`**
- **`d.__set_name__(self, owner, name)`**: Chamado ao instanciar um descritor em um atributo de uma classe, onde:
  - `name`: nome do atributo.
  - `owner`: classe.

## Funções como descriptors

- Objetos do tipo função são non-data descriptors.
- Ao acessar um objeto função por meio de um atributo num objeto, um método vinculado é retornado.