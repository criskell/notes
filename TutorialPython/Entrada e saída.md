# Entrada e saída

## Formatação de strings

- Formatar é organizar ou colocar num determinado formato.
- A função `str` converte um valor em uma string que é **mais legível para humanos** e a função `repr` converte um valor em uma string que pode ser **lida e analisada pelo interpretador**.

### Strings literais formatadas (f-strings)

- Permitem inserir expressões dentro de strings.

- A string pode ter zero ou mais campos de substituição com a gramática:

  ```python
  campoDeSubstituicao ::= "{" expressao ["="] ["!" conversao] [":" especificadorDeFormato] "}"
  ```

- `conversao` age como os conversores do método format.

- `especificadorDeFormato` especifica como cada **valor individual** deve ser **formatado**. Cada tipo define uma forma de interpretação deste especificador.

- **Especificadores de formato de nível superior** podem ter um **campo de substituição aninhado** mas não é permitido um **aninhamento mais profundo que 1 nível**, por exemplo:

  ```python
  f"Olá, {10 ** 20 + 5000!s:.{10 * 2}}"
  """
  ** Explicação:
  
  10 ** 20 + 5000 é avaliado para o valor 100000000000000005000.
  O inteiro é convertido para uma string por causa do conversor !s que
  se utiliza da função str().
  O especificador de formato ":.{10 * 2}" é interpretado como ":.20".
  Este especificador de formato ":.20" vai dizer como a string "100000000000000005000" deve ser formatada. Ou seja, a string irá ser limitada a 20 caracteres de *precisão*.
  """
  ```

  

### Método format

- O método format executa uma **operação de formatação**.

- O texto passado como argumento pode conter texto literal e **campos de substituição**.

- Os **campos de substituição** são delimitados por chaves e **substítuidos** pelos valores passados via argumentos posicionais ou nomeados. Exemplo de campo de substituição: `{meucampo}`.

- A sintaxe do **campo de substituição** é mais ou menos a seguinte, onde:

  ```python
  {[nome-do-campo][!conversao]:[especificador-de-formato]}
  ```

  - `nome-do-campo`: Especifica qual valor deve ser formatado e inserido naquela posição. Pode ser seguido por expressões de índice `[indice]` ou expressões de atributos `.atributo`.

  - `conversao`: Indica que o valor deve ser formatado como uma string. Para isso, o valor é convertido para uma string.
    - `!s`: A função `str` é utilizada para converter o valor para uma string.
    - `!r`: A função `repr` é utilizada para converter o valor para uma string.
    - `!ascii`: A função `ascii` é utilizada para converter o valor para uma string.

  - `especificador-de-formato`: Pode um **campo de substituição aninhado**, mas somente um nível de aninhamento é permitido.

- Exemplo:

  ```python
  "isto é um texto {campo-de-formatacao} literal"
  ```


### Especificador de formato

- Define como valores individuais são formatados.

- Sintaxe:

  ```
  [[preenchimento]alinhamento][sinal][#][0][tamanho][_ | ,][.precisao][tipo]
  ```

- Onde:

  - `tipo`: Determina como os dados devem serem apresentados. Por exemplo, se os dados forem do tipo inteiro, o tipo `b` apresenta o número na base 2.

### Alguns métodos de formatação em strings

- Método `rjust(w)`: Alinha a string à direita, retornando uma string de comprimento `w`.
- Método `ljust(w)`: Alinha a string à esquerda, retornando uma string de comprimento `w`.
- Método `center(w)`: Centraliza a string, retornando uma string de comprimento `w`.
- Método `zfill(w)`: Preenche uma string numérica com zeros à esquerda para retornar uma string de comprimento `w`.

### Formatação antiga de strings

- O operador `%` é utilizada para formatar uma string com uma tupla de valores.
- Esta string é formada por texto literal e **especificadores de formato**.
- Exemplo: `"Olá, %s" % ("Mundo")`
- O segundo operando pode ser um único valor, uma tupla ou um mapeamento (como dicionários).
- Ao passar um mapeamento podemos nos referir a uma chave no especificador de formato utilizando parênteses, por exemplo: `"Oi, %(name)s" % {'name': 'Cris'}`.

## IO

- A função `open(n, m)` retorna um objeto arquivo de um arquivo com nome `n` e com o modo `m`.
- `m` é uma string que descreve o modo de **como** o arquivo deverá ser **aberto**. Possíveis caracteres:
  - `r` abre para leitura;
  - `w` escreve e limpa. Caso o arquivo não exista, ele será criado;
  - `a` abre para escrita e **escreve no final do arquivo** caso ele exista. O arquivo é criado caso não exista.
  - `x` abre para escrita e para **exclusivamente criação de arquivos** (sem atualizar).
  - `+` abre também para leitura caso não seja utilizado a opção `r`, e para escrita também caso não seja utilizado a opção `w` ou `a`.
  - `b` especifica o modo binário de leitura e escrita
  - `t` especifica o modo texto de leitura e escrita (padrão)
- Modo texto é um modo de arquivos em que strings de *caracteres* são escritas e lidas de arquivos.
- Modo binário é um modo de arquivos em que strings de *bytes* são escritas e lidas de arquivos.
- No modo texto, na leitura, o terminador de linha da plataforma é convertido para `\n` e, na escrita, `\n` é convertido para o terminador de linha da plataforma.
- O arquivo deverá ser fechado para que as todas alterações sejam enviadas para o disco.
- Podemos iterar o arquivo no modo texto com `for` retornando todas as linhas do arquivo.

### Métodos de arquivos

- `write()`: Aceita uma string de bytes ou caracteres e escreve.
- `read(s)`: Se `s` for informado, `s` caracteres ou bytes serão lidos e retornados. Uma string vazia significa que o fim foi atingido.
- `readline()`: Ler uma única linha do arquivo e retorna com `\n` no final se houver (caso não seja uma linha em branco). Uma string vazia significa que o fim foi atingido.
- `readlines()`: Ler todas as linhas restantes do arquivo.
- `tell()`: Posição atual. **Número de bytes** desde o ínicio do arquivo, no modo binário. E um número **opaco** no modo texto.
- `seek(d, p)`: Modifica a posição atual no arquivo com base no deslocamento (`d`) relativo a um ponto de referência (`p`).
  - Os pontos de referência `p` podem serem:
    - 0: Início do arquivo.
    - 1: Posição atual.
    - 2: Fim do arquivo.
  - No modo texto, não é permitido `d != 0` quando `p != 0`. `d` quando `p == 0`, `d` precisa ser **zero** ou o número retornado por `tell()`, se for diferente disso, o comportamento é **indefinido**.