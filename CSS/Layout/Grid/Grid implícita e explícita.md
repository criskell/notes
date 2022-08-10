# Grid implícita

- A grid implícita é criado automaticamente devido à necessidade, como posicionar um elemento fora da grade explícita.
- Itens que não são posicionados explicitamente irão preencher a grid implícita automaticamente de acordo.

### Propriedades

- `grid-auto-[rows|columns]`:
  - Define o tamanho da faixa implícita.
  - Se não definido, o padrão é `auto`
    - colunas dividem o espaço disponível igualmente
    - linhas implícitas sem conteúdo possuem uma altura 0
- `grid-auto-flow`:
  - Define como o posicionamento automático irá se comportar.
  - `row`: O fluxo é em linhas.
  - `column`: O fluxo é em colunas.


## Grid explícita

- A grid explícita é criada com as propriedades `grid-template-[areas|columns|rows]`