# Arquivos

- `open(caminho, modo)`
- Se o caminho não for absoluto, o Python irá entender como caminho relativo ao diretório corrente.

## Leitura
- O método `read` ler os dados de um arquivo.
- Ele recebe um argumento indicando quantos caracteres deseja ler. Se não for informado, ele ler todo o arquivo.
- Se não houver caracteres para ler, ele retorna uma string vazia.

## Escrita
- O método `write` escreve em um arquivo.

## Arquivo texto
- Um arquivo texto é um arquivo composto por caracteres imprimíveis e quebras de linha.
- O método `readline` ler uma linha de um arquivo junto com a quebra de linha.
- O método `readlines` retorna todas as linhas do arquivo.