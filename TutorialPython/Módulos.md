# Módulos

- Um módulo é um **arquivo** que contém **definições** e **instruções**.
- O nome de um módulo é o nome do arquivo sem a extensão `.py`.
- Cada módulo possui uma **tabela de símbolos privada e global** e as definições desta tabela podem serem acessadas com a sintaxe `nomedomodulo.definicao`.

## Importação

- A instrução `import` coloca o **nome do módulo** na **tabela de símbolos atual** e com este nome é possível acessar as definições do módulo utilizando a **notação de ponto**.
- A **variação** desta instrução, `from <modulo> import nome1, nome2, nomeN`, permite importar **definições específicas** deste módulo para a **tabela de símbolos atual**.
- Ao importar um módulo, as instruções no topo são executadas somente **uma vez **.

## Execução de módulos como scripts

- É possível executar um módulo **como um script** utilizando o comando `python <nome-do-modulo>.py <argumentos>`.
- Neste módulo, a variável global `__name__` é alterada para `__main__`.

## Caminho de busca dos módulos

- Ao importar um módulo (ou pacote), caso este módulo exista **built-in** no interpretador, o interpretador carrega. Caso contrário ele procura por este mesmo módulo na lista de diretórios em `sys.path`.
- A variável `sys.path` é inicializada com:
  - O diretório do **script de entrada** (caso não haja, uma **string vazia** denotando o **diretório de trabalho atual** será adicionada).
  - A variável `PYTHONPATH`.
  - Uma lista de diretórios que **depende da instalação**.

## Pacotes

- Os pacotes permitem estruturar de forma **hierárquica** o espaço de nomes dos módulos utilizando **nome de módulo com pontos**.

- **Alternativa 1**: Podemos importar submódulos de pacotes com a instrução `import`:

  ```python
  import pacote.modulo
  ```

- Utilização de nomes: `pacote.modulo.nome`.

- **Alternativa 2**: A cláusula `from` na instrução, onde importamos de um pacote um módulo:

  ```python
  from pacote import modulo
  ```

- Ao importar um **nome** (submódulo, subpacote, função, variável e classe) de um pacote com a cláusula `from`, primeiro o interpretador verifica se este nome está **definido no pacote**, caso contrário irá tentar **carregar** um módulo com este nome.

- Nesta variação, não informamos o **prefixo do pacote**, por exemplo: `modulo.funcao()`.

- **Alternativa 3**: Podemos importar diretamente itens individuais de um submódulo em um pacote:

  ```python
  from pacote.modulo import funcao
  ```

### Importando * de um pacote

- A variável `__all__` é utilizada para fornecer um índice dos submódulos para serem importados na instrução `from <pacote> import *`.
- A variável `__all__`, **não sendo definida**, faz com que a instrução `from <pacote> import *` importe todos os **nomes definidos no pacote**. O que inclui os nomes no arquivo `__init__.py` (junto com os **módulos carregados** neste arquivo) e os submódulos do pacote carregados **anteriormente por outras instruções import**.

## Imports relativos

- Imports relativos utilizam pontos para representar o pacote pai de um módulo.
- São resolvidos com base no **nome do módulo atual**.
- `.` = pacote pai
