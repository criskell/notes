# z-index

- Altera a posição no eixo Z de um elemento
- Cada caixa tem 3 posições: horizontal e vertical, além disso, elas ficam ao longo de um eixo Z. São colocadas uma em cima da outra.
- Cada caixa fica numa camada e podem ser configuradas para ficarem numa camada além da camada 0 (de renderização normal).
- Elementos com valores mais altos de `z-index` ficam na frente de elementos com valores mais baixos ao longo do eixo Z
- Geralmente funciona em apenas elementos posicionados, mas há exceções

## Eixo Z

- É a profundidade em um plano 3D
- Está de frente para a página

## Regras de empilhamento

- Quando nenhum elemento possui `z-index`, o empilhamento é feito na seguinte ordem, de baixo para cima:
  1. Bordas e fundos do elemento raiz
  2. Elementos de nível de bloco não posicionados, na ordem de aparição no documento
  3. Blocos flutuantes
  4. Elementos inline não posicionados
  5. Elementos posicionados, na ordem de aparição no documento
- Ao utilizar `z-index`:
  - Permite criar uma ordem de empilhamento de camadas personalizadas
  - Ao pensar no eixo Z, devemos pensar numa pilha de camadas ordenadas numericamente. As camadas com valores numéricos mais alto ficam acima das camadas de números menores.
  - Elementos sem `z-index` são renderizados na camada 0, a padrão
  - Se ambos elementos possuírem o mesmo `z-index` as regras aplicadas são, a partir de cima, em ordem: 1, 2 e 5 

## Contextos de empilhamento

- Contexto de empilhamento são grupos de elementos
- O `z-index` de um elemento é comparado somente com elementos no mesmo contexto de empilhamento e nunca com elementos em outros contextos
- Quando um elemento que forma um contexto de empilhamento é movido ao longo do eixo Z, todo o contexto é movido também
- Ao definir `z-index` devemos pensar que não muda apenas a ordem, mas também cria um grupo em torno dos elementos filhos.
- Aninhados
- Regras:
  - Independentes de irmãos: Num contexto de empilhamento, o empilhamento segue as regras de empilhamento com os descendentes apenas
  - Autocontidos:
    - Ao empilhar os elementos num contexto filho, todo o elemento (+ filhos) é considerado no contexto de empilhamento pai.
    - Os contextos filhos são tratados atomicamente como uma única unidade no contexto pai
  - Escopo: Os valores `z-index` de contextos filhos só tem algum significado no contexto pai
- Casos em que é criado:
  - Quando o posicionamento é absoluto ou relativo e z-index é diferente de `auto`
  - Quando o posicionamento é fixo ou esticado (sticky)