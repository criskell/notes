# POO

- Classes é uma forma de organizar dados e funcionalidades juntos.
- Classe é um tipo e podemos criar instâncias a partir dela.
- Instâncias tem atributos para manter o estado e métodos para alterar o estado.

## O que é OOP

- OOP é um paradigma de programação com base no conceito de "objetos" que possuem dados e comportamentos.

## Objeto no Python

- Objeto, no Python, é abstração de dados. Possui: Tipo, identidade e valor.
- Objeto é uma instância de um tipo.

## Classes

```python
class F:
    declaracao1
    declaracao2
    declaracaoN
```

- Dentro podemos ter várias declarações além de definições de métodos.
- Ao executar uma definição de classe, um novo namespace é criado e o escopo local é associado a este namespace. Atribuições e definições de métodos vão para este namespace.
- Ao executar toda uma definição, um objeto classe é criado com o conteúdo deste namespace o escopo local antigo é reativado e o nome da classe é vinculado ao objeto classe.

## Objeto de classe

- Operações: Referências a atributos e instaciação.
- Referências a atributos:
  - `Classe.atributo`
  - Os nomes de atributos válidos são todos os nomes do namespace da classe.
- Instanciação:
  - `Classe()`
  - Cria uma nova instância da classe `Classe`.
  - O método `__init__` serve para inicializar o estado de instâncias.
  - Instanciar é criar um novo objeto.

## Objeto de instância

- Operações: Referências de atributos
- Dois tipos de referências:
  - Atributo de dados
  - Atributo de método
- Atributo de método: Método é uma função que "pertence" a um objeto. Todos os atributos do tipo função da classe definem métodos correspondentes em instâncias.

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

## Encapsulamento

- Encapsular é esconder os dados de uma classe e o funcionamento dos comportamentos.
- Encapsulamento pode ser visto como o agrupamento de dados e métodos (getters e setters) que operam nestes dados.

## Propriedades

- Propriedade é um atributo numa classe que foi criada utilizando o decorator `@property`.

## Polimorfismo

- Polimorfismo é a capacidade de um código ser referenciado de várias formas.
- Duck typing é um estilo de programação em que não testamos o tipo do objeto para ver se atende uma interface e simplesmente chamamos o método.

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