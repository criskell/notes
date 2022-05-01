# POO

- Classes é uma forma de organizar dados e funcionalidades juntos.
- Classe é um tipo e podemos criar instâncias a partir dela, que são objetos deste tipo.
- Instâncias tem atributos para manter o estado e métodos para alterar o estado.

## Objeto no Python

- Objeto, no Python, é abstração de dados.
- Possui: Tipo, identidade e valor.
- Objeto é uma instância de um tipo.
- Possui uma quantidade de referências também.

## Classes

```python
class nome-da-classe(classes-bases):
    corpo-da-classe
```

- Dentro podemos ter várias declarações além de definições de métodos.
- Ao executar uma definição de classe, um novo namespace é criado e o escopo local é associado a este namespace. Atribuições e definições de métodos vão para este namespace.
- Ao executar toda uma definição, um objeto classe é criado com o conteúdo deste namespace o escopo local antigo é reativado e o nome da classe é vinculado ao objeto classe.

### Objeto de classe

- Operações: Referências a atributos e instaciação.
- Possui atributos.
- Referências a atributos:
  - `Classe.atributo`
  - Os nomes de atributos válidos são todos os nomes do namespace da classe.
  - Atributos implícitos:
    - `__dict__`: Contém o namespace da classe.
- Instanciação:
  - `Classe()`
  - Cria uma nova instância da classe `Classe`.
  - O método `__init__` serve para inicializar o estado de instâncias.
  - Instanciar é criar um novo objeto.

## Instâncias

- Instância de uma classe é um objeto.

### Objeto de instância

- Operações: Referências de atributos
- Dois tipos de referências:
  - Atributo de dados
  - Atributo de método
- Atributo de método: Método é uma função que "pertence" a um objeto. Todos os atributos do tipo função da classe definem métodos correspondentes em instâncias.
- Busca de atributos: Se não for encontrado na instância, irá procurar na classe e se não achar procura nas classes bases.

## Objeto de método

- Chamar um método com é equivalente a chamar a função correspondente com o objeto instância no primeiro argumento.
- O primeiro argumento de funções definidas em classes é o `self`.
- Objetos de método possuem um objeto de instância e um objeto de função.
- O escopo global associado a um método é sempre o namespace global do módulo.

## Variável de instância e de classe

- Variável de instância são variáveis para instâncias específicas e variáveis de classes são compartilhadas por todas as instâncias.
- Numa pesquisa de atributo, variáveis de instância são priorizadas.
- Para alterar uma variável de uma classe, devemos utilizar o nome da classe e não uma instância dela, caso contrário iremos criar uma variável de instância.

## Variáveis privadas e protegidas

- Não há suporte para variáveis privadas.
- Desfiguração de nomes: todas as ocorrências de nomes `<n>` no formato `__<name>` (com no máximo um sublinhado no final) numa definição de classe, serão substituídas por `_<nomedaclasse><n>`
- Geralmente, atributos na forma `__attr` são chamados de privados e atributos na forma `_attr` de protegidos.
- Atributos privados são ditos para serem acessados somente por sua classe.
- Atributos protegidos são ditos para serem acessados somente por sua classe e subclasses.

## Métodos estáticos

```python
class A:
    @staticmethod
    def f():
        ...
```

- Um método estático é um método que não precisa de uma instância da classe.
- Podemos chamar na classe ou numa instância.

## Métodos de classes

```python
class A:
    @classmethod
    def f(cls):
        ...
```

- Métodos de classes são ligadas a uma classe.
- Podemos chamar na classe ou na instância.