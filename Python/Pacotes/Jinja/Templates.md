# Templates

- São arquivos de texto que pode produzir qualquer formato baseado em texto.
- Variáveis/expressões: Substítuido na renderização.
- Tags: Controla a lógica dos templates.
- Delimitadores:
  - `{% ... %}`: Declarações de controle (statements)
  - `{{ ... }}`:
    - Expressões para imprimir saída.
    - Representam partes variáveis da página.
  - `{# ... #}`: Comentários
- Variáveis:
  - Passadas pela aplicação.
  - Podemos acessar atributos ou outros elementos.
  - Acesso a um atributo: `x.y` ou `x[y]`
  - Acessar uma variável/atributo que não existe devolve um valor não indefinido.
  - O tratamento para valores indefinidos é definido pela aplicação. Por padrão produz uma string vazia se impresso ou iterado e um erro nos outros casos.

## Filtros

- Modificam uma variável
- Podem ser adicionados com `|`
- O resultado de um filtro é passado para outro.
- Podem ter argumentos opcionais entre parênteses.

## Testes

- Testes testam uma variável/expressão contra uma expressão comum.
- Para testar uma variável/expressão: `variavel is nome_do_teste(...argumentoN)`
- Se possui somente um argumento não há necessidade de parênteses: `x is test y`

## Declarações condicionais

- Sintaxe:

  - ```jinja2
    {% if <teste> %}
    	<verdadeiro>
    {% else %}
    	<falso>
    {% endif %}
    ```

## Loops

- A estrutura de controle `for` permite percorrer uma lista de elementos:

  - ```jinja
    {% for elemento in lista %}
    	...
    {% endfor %}
    ```

## Herança

- Permite derivar um modelo de um modelo base, reutilizando templates.
- `{% extends "a" %}`: Estabelece uma relação de herança.
- `{% block %}`: Define um bloco que pode ser substituído nos modelos derivados.