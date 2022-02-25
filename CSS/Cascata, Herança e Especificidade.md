# Cascata, especificidade e herança

## Cascata

- Cascata é um algoritmo que o CSS utiliza para resolver conflitos de declarações.
- A cascata resolve os conflitos por meio de etapas, onde o algoritmo irá passar para a próxima se houver "empate" entre declarações.
- **Valor em cascata** é o resultado.
- "[Figurado] Série de acontecimentos sucessivos".
- Etapas:
  - Origem e importância;
  - Especificidade da declaração;
  - Ordem da origem e da declaração;

### Origem e importância

- Esta etapa analisa a combinação de origem e importância (ter ou não `!important`).
- `!important` substitui as declarações normais.
- Ordem de precedência, de maior para menor:
  1. Transições
  2. Navegador, `!important`
  3. Usuário, `!important`
  4. Autor, `!important`
  5. Animação
  6. Autor
  7. Usuário
  8. Navegador

### Especificidade da declaração

- Declarações com mais especificidade vence nesta etapa.
- Especificidade é a medida de quão específico é um seletor.
- Estilos inline sempre vencem nesta etapa.

### Ordem de origem

- Declarações que vem por último na ordem de origem vence. No mesmo arquivo ou em arquivos diferentes.

## Especificidade

- É uma medida de quão específico um seletor é.
- A especificidade de uma declaração é a mesma da sua regra.
- Níveis de especificidade em ordem decrescente:
  - Inline
  - ID
  - Classes, pseudoclasses e atributos
  - Elementos e pseudoelementos
- Para comparar a especificidade entre seletores, contamos cada ocorrência de cada nível. O seletor com mais ocorrências no maior nível vence. Se houver empate, descemos o nível.

### Calculando a especificidade

- Contamos a quantidade de ocorrências em cada nível de especificidade e separamos por vírgulas.
- `.a .b e`: 0, 0, 2, 1
- `#x #p .oi::first-line`: 0, 2, 1, 1

## Herança

- Herança é a propagação de valores de propriedades de elementos pais para propriedades com valores não declarados pelos filhos.
- Uma propriedade não herdada é uma propriedade que não herda de seu pai e obtém por padrão o valor inicial.
- Uma propriedade herdada é uma propriedade que obtém de seu pai.
- Apenas valores computados são passados.
- Valores universais:
  - `initial`
  - `inherit`
  - `unset`: Retorna a propriedade para seu valor natural. Herdada ou valor inicial.
  - `revert`: Reverte a propriedade como se ela não fosse declarada.

## Processamento de valores

- Etapas para obter o valor final de uma propriedade:
  1. Valor declarado em declarações de regras.
  2. Valor em cascata.
  3. Valor especificado: Valor que o autor deseja numa folha de estilos. Pode vim de:
     - Cascata
     - Herança ou valor inicial (processo de **defaulting**)
  4. Valor computado: Aplicação de cálculos no valor especificado de acordo com o que a propriedade deseja.
  5. Valor usado: Aplicação dos cálculos restantes no valor computado durante a renderização do documento. `width: auto`, auto é o valor computado (não dá para calcular sem renderizar o documento) e um valor absoluto é o valor usado. Há valor usado somente se a propriedade **se aplica** ao elemento.
  6. Valor atual: O valor usado é aproximado de acordo com as limitações do computador.