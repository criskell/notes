# Cascata e herança

- Cascata, herança e especifidade controlam como o CSS é aplicado ao HTML e como conflitos são resolvidos.

## Regras conflitantes

- A cascata e especifidade são mecanismos utilizados quando há declarações conflitantes de uma mesma propriedade para um mesmo elemento.

## Cascata

- Folha de estilos em **cascata**
- Cascata diz que quando há declarações conflitantes em regras com a mesma especifidade a declaração que vem por último será utilizada.

## Especifidade

- A especifidade é como o navegador decide qual regra será aplicada quando os seletores forem diferentes mas para um mesmo elemento.
- A especifidade é uma medida do quão específica é a *seleção* de um seletor.

## Calculando a especifidade

- De forma **aproximada**, podemos calcular a especifidade um selector específico utilizando um número da ordem de unidades de milhares onde os números de:
  - O número de unidades são iguais ao número de elementos no **seletor geral**.
  - O número de dezenas são iguais ao número de seletores de classes, pseudo-classes e de atributos no **seletor geral**.
  - O número de centenas são iguais ao número de identificadores no **seletor geral**.
  - O número de unidades de milhar é igual a 1 se a declaração estiver num atributo `style`.

## Herança

- Valores de algumas propriedades são herdadas do elemento pai quando não forem informadas.
- `font-family`, `color` são algumas propriedades com herança.

### Valores universais de herança

- Controla a herança.
- `inherit`: Herda o valor da propriedade do elemento pai.
- `initial`: Usa o valor inicial da propriedade.
- `unset`: Usa valor "natural" da propriedade. Herda o valor ou usa o valor inicial.

### Propriedade all

- A propriedade `all` é utilizado para alterar quase todas as propriedades para um valor universal de herança.

### !important

- `!important` é utilizado para tornar uma coisa mais específica ainda substituindo as regras normais de cascata.
- Para substituir uma declaração importante é preciso colocar uma outra declaração importante numa regra posterior com mesma especifidade ou numa regra com mais especifidade.

## Localização do CSS

- A importância de uma declaração irá depender também da localização de sua folha de estilos.
- As declarações conflitantes serão aplicadas nesta ordem, com as declarações posteriores substituindo as anteriores:
  - Declarações do navegador.
  - Declarações do usuário.
  - Declarações do autor.
  - Declarações importantes do autor.
  - Declarações importantes do usuário.
