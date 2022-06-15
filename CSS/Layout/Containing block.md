# Containing block
- O tamanho e posição de um elemento é frequentemente influenciado pelo seu containing block.
- Na maioria das vezes, é a área de conteúdo do ancestral de nível de bloco mais próximo.
- Quando o navegador apresenta um documento, uma caixa é gerada para cada elemento. Cada caixa possui 4 áreas:
	- Área de conteúdo
	- Área de preenchimento
	- Área de borda
	- Área de margem
- Efeitos do containing block:
	- O tamanho e posição são calculados frequentemente com base no containing block.
	- Valores em porcentagens das propriedades width, height, margin e padding são calculados com base no containing block.
- Identificando o containing block:
	- O containing block do elemento raiz é o initial containing block. O initial containing block é um retângulo que possui as dimensões da viewport.
	- Caso contrário, o processo depende do valor da propriedade position do elemento:
		- Se for static, relative ou sticky, o containing block é formado pelo perímetro da caixa de conteúdo do ancestral mais próximo que é um block container (por exemplo, elementos block) ou estabelece um FC.
		- Se for absolute, é formado pela edge da caixa de preenchimento do elemento ancrestral mais próximo que está posicionado (ex.: position relative, sticky, absolute, etc.)
		- Se for fixed, é formado pela viewport (no caso de mídia contínua)
		- Se for absolute ou fixed, o containing block também pode ser formado pela edge da caixa de preenchimento de um elemento ancrestral mais próximo que tiver algumas propriedades especiais definidas.
- Calculando valores em porcentagens a partir do contaning block:
	- Algumas propriedades possuem o computed value baseado no containing block. Propriedades que funcionam assim são as propriedadesdo box-model e de deslocamento:
		- height, top, bottom são calculados com base no height do containing block.
		- width, left, right, margin e padding são calculados com base no width do containing block.

## Exercícios

1. Escreva um algoritmo que identifique o containing block de uma caixa numa estrutura imaginária.
2. O que é o containing block?
3. Como as porcentagens das propriedades do box model, `width` e height, e as propriedades de offset são calculadas?