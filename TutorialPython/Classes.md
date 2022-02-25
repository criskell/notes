# Classes

- Classes é uma forma de organizar dados e funcionalidades juntos.
- Classe é um tipo e podemos criar instâncias a partir dela.
- Instâncias tem atributos para manter o estado e métodos para alterar o estado.

## [Plano de estudos]

- Ainda falta: Entender mais sobre tudo
- Dúvidas:
  - Instância x Objeto
  - Objeto de instância, objeto de método, variáveis de classe e instância
  - Herança e Herança múltipla
  - Geradores
  - Atributos de dados x atributo de métodos (objeto de instâncias)
- Artigos para ler:
  - https://panda.ime.usp.br/pensepy/static/pensepy/13-Classes/classesintro.html#:~:text=O%20Python%20%C3%A9%20uma%20linguagem,orientada%20%C3%A0%20objetos%20(POO).&text=Na%20programa%C3%A7%C3%A3o%20orientada%20%C3%A0%20objetos,os%20dados%20quanto%20as%20funcionalidades.
  - https://www.alura.com.br/conteudo/python-3-avancando-orientacao-objetos
  - http://pythonclub.com.br/oo-de-outra-forma-1.html
- Cursos:
  - Python da USP
  - OOP da UNIVESP
  - OOP do CursoEmVídeo

## O que é OOP

- OOP é um paradigma de programação com base no conceito de "objetos" que possuem dados e comporamentos.

## Objeto no Python

- Objeto, no Python, é abstração de dados. Possui: Tipo, identidade e valor.
- Objeto é uma instância de um tipo.

## Escopo e espaço de nomes

- Cada objeto tem vários nomes.
- Espaço de nomes é um mapeamento entre nomes e objetos.
- Escopo é uma região textual de um programa que permite o **acesso direto** a um namespace.
- Um namespace local é criado sempre para uma invocação de uma função.
- Durante a execução, existem 3 ou mais escopos aninhados:
  1. Escopo local
  2. Escopos de funções delimitadoras
  3. Escopo global do módulo atual
  4. Escopo embutido
- O escopo local fora de uma função é o escopo global do módulo.
- Sem nenhuma declaração `nonlocal` e `global`, atribuições vão para o escopo mais interno.
- Variáveis em escopos mais externos, sem nenhuma declaração, são somente leitura.
- `nonlocal`: leitura e atribuições para o primeiro escopo que não é local nem global.
- `global`: leitura e atribuições para o escopo que guarda os nomes globais.
- Atribuições apenas vinculam nomes a objetos.

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

## Variável de instância e de classe

- Variável de instância são variáveis para instâncias específicas e variáveis de classes são compartilhadas por todas as instâncias.

## Herança

- ```python
  class ClasseDerivada(<expressao>):
      pass
  ```

- `<expressao>` deve retornar um objeto de classe base.

- A definição de classes derivadas lembram da classe base. Se um atributo não for encontrado na classe derivada, irá ser procurado na classe base e assim sucessivamente até achar o atributo.

### Herança múltipla

- Definir várias classes bases.

## Variáveis privadas

- Não há suporte para variáveis privadas.
- Desfiguração de nomes: todas as ocorrências de nomes `<n>` no formato `__<name>` (com no máximo um sublinhado no final) numa definição de classe, serão substituídas por `_<nomedaclasse><n>`

## Iteradores

- Iteradores definem uma função `__next__` que retorna o próximo item e levanta uma exceção `StopIteration` quando não há mais itens para iterar.
- O método `__iter__` é utilizado para retornar iteradores.
- O laço `for` chama a função `iter` no objeto para retornar um iterador.

## Geradores

- Geradores é um mecanismo para criar iteradores.
- São escritos como funções que possuem `yield`, esta instrução retorna dados.
- Quando o `next` é executado, sempre a função volta de onde parou.

### Expressões de geradores

- Funcionam de forma semelhante a compreensões de listas, mas com parênteses ao invés de colchetes:

  ```python
  (x for x in range(5))
  ```

  