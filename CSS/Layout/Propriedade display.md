# Propriedade display

- A propriedade `display` especifica como a caixa do elemento deve ser exibida.

- A menos que altere o valor da propriedade `display`, os elementos são exibidos em fluxo normal (são exibidos como elementos inline ou block) e sempre que possível voltam para este fluxo.

- Especifica dois valores:

  - *Outer display type*:
    - Participação no *flow layout* (bloco/inline)
    - Como o elemento se comporta ao lado de elementos irmãos.
  - *Inner display type*:
    - Como os filhos serão dispostos.

- Sintaxes:

  - ```css
    /* Valores pré-compostos/Sintaxe de valor único */
    display: block;
    display: flex;
    display: inline-flex;
    display: inline-block;
    
    /* Sintaxe de dois valores */
    display: block flow;
    display: block flex;
    display: inline flex;
    display: inline flow-root;
    ```

# Categorias de valores
- `<display-outside>`:
	- *outer display type*
	- Valores:
	  - Em navegadores que utilizam a sintaxe de dois valores, se definir apenas o `outer display type`, o `inner display type = flow`. Isto permite que os valores desta categoria sejam utilizados **unicamente** para **fins legados** ou junto com os valores `<display-inside>`.
	  - `block`:
	    - Gera uma caixa block-level.
	    - Cria uma caixa como um bloco.
	    - Criam novas linhas.
	    - Se expandem na dimensão de bloco em bloco e na dimensão inline.
	    - Suas margens e paddings são respeitados.
	  - `inline`:
	    - Gera uma caixa inline-level
	    - Cria a caixa na mesma linha
	    - Se comportam como palavras em uma frase. Não criam novas linhas e ficam lado a lado na direção inline.
	    - Suas margens e paddings não são respeitados.
	    - O seu dimensionamento é intrínsico, se expandindo na dimensão inline.
	    - Altura e largura não são respeitadas.
	    - Se comportam como palavras.
- `<display-inside>`:
	- *inner display type*.
	- Em navegadores que utilizam a sintaxe de dois valores, se definir apenas o *inner display type*, `outer display type = block`. Isto permite que os valores desta categoria sejam utilizados **unicamente** para **fins legados** ou juntamente com os valores de `<display-outside>`.
	- Valores:
	  - `flow`:
	    - Exibe o conteúdo da caixa com o *flow layout*.
	    - Se a caixa for inline-level ou `run-in` e estiver participando em um FC, gerará uma caixa **inline**. Caso contrário gerará uma **block container box**.
	    - Os seus filhos participarão de seu próprio FC ou estabelecerá um novo BFC (dependendo de algmas propriedades).
	  - `flow-root`:
	    - Gera uma `block container box` e dispõe os conteúdos segundo o `flow layout`
	    - Gera um novo BFC e define o `FC root`
- `<display-box>`:
	- Especifica se o elemento deve exibir caixas.
	- Valores:
	  - `contents`: As filhas de uma caixa são exibidas como se fossem diretamente filhas do pai da caixa.
	  - `none`: Desativa a exibição da caixa e das caixas filhas.
- `<display-legacy>`:
	- São valores únicos que foram definidos antes do nível 3 desta propriedade, variantes apenas no `outer display type` para um mesmo modo de layout.
	- Valores:
	  - `inline-block`:
      - `block + inline`
      - este valor único é mapeado para o valor `inline flow-root`
      - Fica na mesma linha
	    - Pode ter width e height
	    - Se comporta como palavras

## flow-root vs inline-block
- `flow-root`:
  - Da mesma forma que *flex* ou *grid* cria um novo FC, cria uma caixa de bloco que estabelece um BFC que contém tudo dentro do *flow root*.
- `inline-block`: Cria uma caixa em linha que estabelece um BFC.

## Sintaxe de dois valores e os valores antigos

- No nível 3 da especificação, foi criada uma nova sintaxe (sintaxe de dois valores) que permite especificar dois valores na propriedade, um valor externo e interno. Mas também permite especificar somente um valor único (ex.: block, inline).
- Há um valor externo padrão e um valor interno padrão, o que permite compatibilidade com os valores antigos da propriedade `display` se apenas um valor interno ou externo for especificado.
- Além disso, define valores legados **pré-compostos de nível em linha** (ex.: inline-block e inline-flex) que mapeia para valores com a sintaxe de dois valores.
- Tudo isso permite um mapeamento entre valores curtos e legados para valores com nova sintaxe.

## Exercícios



1. O que é a propriedade `display`? Quais tipos de display define, de acordo com a spec 3?
2. Quais são as categorias de valor para a propriedade `display`?
3. Como a especificação de nível 3 manipula valores antigos da propriedade `display` como `inline-block` e `block`?
4. Como funciona a nova sintaxe para a propriedade `display`?