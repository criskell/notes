# Containing block
- O **tamanho** e **posição** de um elemento é frequentemente influenciado pelo seu containing block.
- é a content area do ancestral block-level mais próximo. (geralmente)
- Identificando o containing block:
	- elemento raiz -> initial containing block (dimensões da viewport). 
	- valor da prop. `position`:
		- `static || relative || sticky` -> é formado pela *edge* da content box do ancestral mais próximo que é: um block container (por exemplo, elementos block) || estabelece um FC.
		- `absolute` -> *edge* da *padding box* do ancestral mais próximo que está *posicionado* (!= `static`).
		- `fixed` -> *viewport*
		- `absolute || fixed` -> *edge* da *padding box* de um ancestral mais próximo que tiver algumas propriedades **especiais** definidas.
- Calculando valores em porcentagens a partir do contaning block:
	- propriedades de deslocamento e do box-model calculam o **computed value** a partir do containing block:
	  - **height**, **top**, **bottom** -> **height**.
	  - **width**, **left**, **right**, **margin** e **padding** -> **width**.

## Exercícios

1. Escreva um algoritmo que identifique o containing block de uma caixa numa estrutura imaginária.
2. O que é o containing block?
3. Como as porcentagens das propriedades do box model, `width` e height, e as propriedades de offset são calculadas?
4. O que é o initial containing block?