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
    /* Sintaxe de dois valores */
    display: <a> <b>;
    ```

# Categorias de valores:
- `<display-outside>`:
	- Define o outer display type.
	- Valores:
	  - `block`: Gera uma caixa bloco.
	  - `inline`: Gera uma caixa inline.
- `<display-inside>`:
	- Define o *inner display type*, que define o contexto de formatação dos descendentes da caixa.
	- Valores:
	  - `flow`:
	    - Exibe o conteúdo da caixa com o *flow layout*.
- `<display-box>`:
	- Especifica se a caixa deve exibir caixas.
	- Valores:
	  - `contents`: As filhas de uma caixa são exibidas como se fossem diretamente filhas do pai da caixa.
- `<display-legacy>`:
	- São valores únicos que foram definidos antes do nível 3 desta propriedade.
	- Valores:
	  - `block`:
        - Cria uma caixa como um bloco.
        - Criam novas linhas.
        - Se expandem na dimensão de bloco em bloco e na dimensão inline.
	      - Suas margens e paddings são respeitados.
	  - `inline`:
        - Cria a caixa na mesma linha
        - Se comportam como palavras em uma frase. Não criam novas linhas e ficam lado a lado na direção inline.
        - Suas margens e paddings não são respeitados.
        - O seu dimensionamento é intrínsico, se expandindo na dimensão inline.
        - Altura e largura não são respeitadas.
	      - Se comportam como palavras.
	  - `inline-block`:
	    - `block + inline`
	    - Fica na mesma linha
	    - Pode ter width e height
	    - Se comporta como palavras

## flow-root vs inline-block
- `flow-root`: Cria uma caixa de bloco que estabelece um BFC.
- `inline-block`: Cria uma caixa em linha que estabelece um BFC.