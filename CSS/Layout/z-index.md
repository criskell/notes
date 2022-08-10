# z-index

- Especifica a posição de um elemento na ordem de empilhamento

## Eixo Z

- É a profundidade em um plano 3D
- Cada caixa tem 3 posições: horizontal e vertical, além disso, elas ficam ao longo de um eixo Z. São colocadas uma em cima da outra.

## Ordem de empilhamento

- A ordem de empilhamento dita qual elemento se empilha na frente de outros elementos.

### Simplificação

- Sem nenhum `z-index` e `position`, a ordem de empilhamento, de forma simplificada, é a mesma ordem de aparência no HTML.
- Já com `position` e sem `z-index`, irá aparecer na frente de elementos não posicionados.
- Já com `position` e `z-index` irá aparecer na frente de valores `z-index` mais baixos no mesmo contexto de empilhamento.
- Entre elementos com `z-index`, o que fica na frente é sempre o que tiver o valor mais alto e os valores são iguais a ordem é ditada pela ordem de aparecimento no HTML.

### Ordem num contexto de empilhamento

- Num contexto de empilhamento, a ordem de empilhamento de camadas é:
  1. Bordas e fundos do elemento que estabelece o contexto de empilhamento
  2. Elementos posicionados com `z-index < 0`, em ordem de aparecimento
  3. Elementos em nível de bloco não posicionados e não flutuantes, na ordem do HTML
  4. Elementos flutuantes não posicionados, em ordem de aparição
  5. Elementos em linha, em ordem de aparição
  6. Elementos posicionados, na ordem do código fonte
  7. Elementos posicionados com `z-index > 0`

## Contexto de empilhamento

- Um contexto de empilhamento são grupos de elementos que se movem juntos ao longo da ordem de empilhamento

- Ao definir `z-index` devemos pensar que não muda apenas a ordem, mas também cria um grupo em torno dos elementos filhos.

- O `z-index` de um elemento é comparado somente com elementos no mesmo contexto de empilhamento e nunca com elementos em outros contextos.

- Regras de um contexto de empilhamento:

  - Num contexto de empilhamento, o empilhamento segue as regras de empilhamento com os descendentes apenas.

  - Ao empilhar os elementos num contexto filho, todo o elemento (+ filhos) é considerado no contexto de empilhamento pai.
  - Os contextos filhos são tratados atomicamente como uma única unidade no contexto pai

  - Os valores `z-index` de contextos filhos só tem algum significado no contexto pai

- Casos em que é criado:
  - Quando o posicionamento é absoluto ou relativo e z-index é diferente de `auto`
  - Quando o posicionamento é fixo ou esticado (sticky).

## Exercícios

1. O que é z-index?
2. O que são contextos de empilhamento?
3. Um contexto de empilhamento é sempre criado em elementos *posicionados*?
4. Qual é a ordem de empilhamento em contextos de empilhamento?