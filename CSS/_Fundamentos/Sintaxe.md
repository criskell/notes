# Sintaxe

Propriedades:

- Identificadores que definem um recurso estilístico
- Cada propriedade possui um conjunto de valores válidos

Valores:

- Como o recurso deve ser manipulado pelo navegador.

Declarations:

- É um par de propriedade-valor.
- Se o valor é inválido para a propriedade, a declaração é inválida.

Blocos:

- Bloco agrupa declarações
- Cada declaração num bloco precisa terminar com `;`, com exceção da última
- Blocos são estruturas delimitados por chaves

Grupo de seletores:

- Seletores separados por vírgulas

Conjunto de regras:

- Um grupo de seletores associados a um bloco de declarações é chamada de regra ou conjunto de regras (ruleset)

Statements:

- Um statement começa com um caractere != espaço em branco, e termina no primeiro `;` ou `}`
- onde `;` e `}` devem estar fora de uma string, não devem ser escapados e não incluído em outro par de chaves, colchetes ou parênteses
- Tipos de statements:
  - Rulesets
  - At-rules
- Aninhamento:
  - Statements que são utilizadas em regras do grupo condicional (at-rules)
  - Só aplicam se uma condição for atendida
  - Regras do grupo condicional podem conterem rulesets e alguns tipos de at-rules

At-rules:

- Começam com `@`, seguido por um identificador e vão até o próximo `;` ou até o final do próximo bloco.