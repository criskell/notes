# Dimensionamento de itens flexíveis

- `flex-grow`:

  - Especifica o fator de crescimento a partir do `flex-basis`
- O espaço positivo disponível dentro do container será distribuído seguindo uma proporção especificada por `flex-grow`
  - Espaço alocado para cada item é obtido da seguinte forma:
  - Multiplicamos o espaço restante pela razão do valor `flex-grow` e todos os valores `flex-grow` de todos os itens.
- `flex-shrink`:

  - Especifica o fator de redução de um item
  - Quando o espaço restante < 0
  - Para calcular o quanto de espaço um item irá ceder:
    - `S = flex-shrink * flex-basis`
    - `fatorDeEncolhimentoDoItem = S do item / somatório do S de todos os itens `
    - ` fatorDeEncolhimentoDoItem * espaço restante`
- `flex-basis`:

  - Determina o tamanho inicial do item antes de qualquer coisa ser calculada.
  - É resolvida da mesma forma que `width`:
    - Por padrão, determina o tamanho da caixa de conteúdo
  
    - Porcentagens se referem ao container
  - Tem prioridade sobre `width`
  - Valores:
    - `auto`:
      - O tamanho base será como o valor da propriedade do tamanho principal ou caso seja auto também, será `content`. ou seja, podemos dizer que `width` é um fallback.
    - `content`:
      - em casos mais básicos e simples, será `max-content`
  - Exemplos de usos:
    - `flex-basis: 0`:
      - Se todos os elementos definidos com isso e com o mesmo `flex-grow >= 1`, o espaço restante no container será todo o container e assim este espaço será distribuído proporcionalmente.
- `flex`:

  - Shorthand para `flex-grow`, `flex-shrink` e `flex-basis`
  - Se `flex-grow` for omitido, é `1`
  - Se `flex-shrink` for omitido, é `1`
  - Se `flex-basis` for omitido, é `0`
  - Sintaxes:
    - Um valor:
      - No caso de um número, é interpretado como `flex: <numero> 1 0`
      - No caso de um valor válido para a propriedade `width`, é interpretado como `flex: 1 1 <width>`
      - `initial`: `flex: 0 1 auto` (valor padrão), ou seja:
        - os itens não poderão crescer
        - os itens poderão diminuir caso suas larguras ultrapassem a largura total do container
        - os itens possuem um tamanho inicial baseado em `width` ou no tamanho do conteúdo
      - `auto`: `flex: 1 1 auto`, ou seja:
        - mesma coisa que o valor initial, assim os itens poderão encolher e ter seu tamanho inicial definido, além disso, poderão crescer para preencher o container.
      - `none`:
        - itens inflexíveis
        - a `flex-basis` é auto
      - `<numero positivo>`:
        - os itens podem encolher e diminuir a partir de uma `flex-basis` de 0
    - Dois valores:
      - 1º: `<number> -> flex-grow`
      - 2º: `<number> -> flex-shrink (~> flex-basis = 0) || <width> -> flex-basis (~> flex-shrink = 1)`
    - Três valores:
      - `flex-grow flex-shrink flex-basis`



### Diferença entre flex-basis e width

- O que `flex-basis` irá se aplicar depende do `flex-direction`:
  - Se for `row`, controla a largura
  - Se for `column`, controla a altura
- Diferenças principais:

| flex-basis                                                   | width                          |
| ------------------------------------------------------------ | ------------------------------ |
| Se aplica apenas à itens flexíveis                           | Se aplica a todos os elementos |
| Funciona apenas no eixo principal, ou seja, não é possível controlar a largura de um elemento com o container `flex-direction: column` | Funciona em todos os eixos     |
| Não tem efeitos em itens flexíveis absolutamente posicionados | Possui efeito                  |

- Semelhanças:


| flex-basis e width                                             |
| ------------------------------------------------------------ |
| Não tem diferença em termos de como são *renderizados*, a menos que `flex-basis` seja `auto` ou `content` |
| `flex-basis` e `width` são *resolvidos* de forma idêntica, a menos que `flex-basis` seja `auto` ou `content`, nestes casos pode usar a largura do conteúdo (onde a largura também usaria) |
| `(flex-basis: x ||width: x ||height: x) && flex-shrink >= 1`, não significa necessariamente que a largura/altura renderizada, pois pode vim a encolher |
