# Pseudo-classes

- Pseudo-classes permitem estilizar com base no estado e fatores externos de um elemento.

## Estados interativos

- `:hover`: quando um dispositivo que possui um ponteiro está sobre o elemento
- `:active`:
  - quando o elemento está interagindo ativamente, como um clique
  - ao clicar no botão, o botão estará no estado `:active:focus`, caso seja focalizável

- `:focus`:
  - quando o elemento está focado
  - o elemento está selecionado para receber entradas
  - por exemplo, ao utilizar a tecla:`tab`

- `:focus-within`: quando o elemento possui um filho que está em foco
- `:focus-visible`:
  - quando o elemento corresponde ao `:focus` e o navegador decide que a indicação de foco **deve** ser exibido (por exemplo, ao utilizar o teclado via tab)
  - por exemplo, por padrão, um `outline` é ativado ao receber um clique ou foco, e ao desativar isso, diminui a acessibilidade para usuários que estão acessando a web via o teclado, pois não há como saberem onde que o foco está atualmente

## Estados do histórico de navegação

- `:link`: links que possui um `href` e que não foram visitados.
- `:target`: quando o elemento possui um ID que corresponde ao fragmento de URL
- `:visited`:
  - links que possuem um `href` e que foram visitados.
  - há restrições nesta pseudo-classe por motivos de segurança.

### Ordem

- Para elementos com essas pseudo-classes e mesma especificidade, pode haver conflitos, pois uma pseudo-classe é construída sobre a outra
- por isso devemos usar a ordem LVHA ou LVFHA
  - Link
  - Visited
  - Focus
  - Hover
  - Active

## Estados de elementos de formulários

- `:valid`: Quando o campo é válido.
- `:invalid`: Quando o campo está inválido.
- `:checked`: Quando o checkbox ou radio button está marcado
- `:indeterminate`:
  - Quando está num estado intermediário, não está nem marcado nem desmarcado, está num estado indeterminado
  - Por exemplo:
    - Podemos colocar um checkbox no estado intermediário utilizando a propriedade `indeterminate` do JS.
- `:placeholder-shown`: Quando há um placeholder e não há nenhum valor
- `:disabled`: Quando o elemento está desativado
- `:enabled`: Elemento está ativado (padrão)
- `:in-range`: quando possui um valor que está dentro dos limites especificados pelos atributos `min` e `max`
- `:required`: quando o campo é obrigatório
- `:optional`: o campo é opcional, ou seja, não apresenta o atributo `required`

## Estruturais

- `nth-child(idx)`:
  - Seleciona um elemento de índice `idx`
- `:first-child`: Seleciona um elemento que é o primeiro filho de um pai
- `:last-child`: Seleciona um elemento que é o último filho de um pai
- `:first-of-type`: Seleciona o elemento que é o primeiro de seu tipo no elemento pai.
- `:last-of-type`: O mesmo acima, mas para o último.
- `:empty`:
  - Seleciona um elemento que está vazio.
  - Não possui textos, elementos nem espaço em branco.
- `:only-of-type`: O elemento é o único de seu tipo no grupo de irmãos.

## Funcionais

- `:is(listaDeSeletores)`: Seleciona um elemento que corresponde com algum seletor na lista.
- `:not(listaDeSeletores)`: Seleciona elementos que não correspondem com nenhum seletor da lista. 

## Pendente

- Explicar mais ainda o `:link` e `:visited`
- Se aprofundar nas pseudo-classes estruturais

## Exercícios

1. Crie um explicador de seletores CSS, que dado um seletor, retorne a explicação das pseudo-classes.