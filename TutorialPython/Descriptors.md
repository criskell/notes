# Descriptors

- Descriptors descrevem atributos de um objetos. Permite adicionar atributos gerenciados a um objeto.
- Se um objeto tem pelo menos um método do protocolo descriptor, é dito que este objeto é um descriptor.
- Se na cadeia de pesquisa encontrar um descriptor, o Python substituirá seu comportamento pelo comportamento definido em algum método, dependendo do caso.

## Cadeia de pesquisa

- Todo objeto no Python possui um dicionário `__dict__` que contém todos os atributos do objeto.
- Um objeto é uma classe, portanto possui um atributo `__dict__` que contém todos os métodos e atributos da classe.
- Cadeia de pesquisa de atributos ao acessar com notação de ponto:
  1. Pesquisa em `obj.__dict__`
  2. Se não encontrar, pesquisa em `type(obj).__dict__`
  3. Se não encontrar, pesquisa nas classes bases de `type(obj)`

## Protocolo de descriptor

- O protocolo, de um modo geral, consiste nos seguintes métodos:

  ```python
  descriptor.__get__(self, obj, type=None) -> value
  descriptor.__set__(self, obj, value) -> None
  descriptor.__delete__(self, obj) -> None
  ```

- Tipo de descriptors:

  - descriptor de não-dados: Quando definimos apenas o método `__get__` .
  - descriptor de dados: Quando definimos `__set__` ou `__delete__`.

### Métodos

- **`d.__get__(self, owner, type)`**: Obtém o valor do descritor. Onde:
  - `owner`: Objeto o qual o descritor está sendo acessado ou `None` se estiver sendo acessado por uma classe.
  - `type`: Tipo do objeto.
- **`d.__set__(self, obj, value)`**:  Altera o valor.
- **`d.__delete__`**
- **`d.__set_name__(self, owner, name)`**: Chamado ao instanciar um descritor em um atributo de uma classe, onde:
  - `name`: nome do atributo.
- Os métodos somente serão chamados se a instância da classe do descriptor aparecer no dicionário da classe proprietária ou no dicionário das classes pais.
- Na expressão `obj.x`, `obj` pode ser uma instância ou uma classe:
  - Instância:
    - Quem controla o acesso é o método `__getattribute__`, assim: `type(obj).__dict__['x'].__get__(obj, type(obj))`.
    - Precedência:
      - Data descriptors
      - Variáveis de instância
      - Non-data descriptors
      - `__getattr__`
  - Classe:
    - Quem controla o acesso é o método `__getattribute__`, assim: `class.__dict__['x'].__get__(obj, class)`.

## Funções como descriptors

- Objetos do tipo função são non-data descriptors.
- Ao acessar um objeto função por meio de um atributo num objeto, um método vinculado é retornado.