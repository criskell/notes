# Múltiplas colunas
- Essa técnica de layout divide o conteúdo em várias colunas.

## Como ativar

- `column-count`:
	- Fragmenta o conteúdo em `n` colunas com larguras flexíveis
- `column-width`:
	- Fragmenta o conteúdo colunas o tanto possível utilizando uma largura ideal, mas não exata
	- Se houver espaço restante, será compartilhado

## Estilizando colunas
- `column-gap`:
	- Lacuna entre as colunas.
- `column-rule`:
	- Regras entre colunas.
	- É como a propriedade `border`, possui estilo, largura e cor
	- Fica dentro das colunas
- `column-span`:
	- `all`: Estende um elemento em todas as colunas. O conteúdo continuará após o elemento.

## Fragmentação
- O conteúdo de um layout multicol é fragmentado em várias colunas
- Para que fragmente, o conteúdo precisa quebrar
- Controlamos isso com a declaração `break-inside: avoid`, que permite que um elemento se comporte como uma única entidade inequebrável