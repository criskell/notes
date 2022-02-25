# Funções, módulos e tipos
- Função é uma sequência nomeada de instruções que executa uma operação de computação.

## Chamada de funções
- `funcao(argumento1, argumento2, ...argumentoN)`

## Conversões entre tipos
- `int()` converte um valor, se possível, para inteiro. Se passar um `float`, irá remover a parte fracionária.
- `float` converte um valor para o tipo float.
- `str` converte um valor para o tipo string.

### Coerção de tipos
- Quando o Python converte automaticamente um tipo para outro em determinadas situações.
- Se em um operador matemático um operando for do tipo float, o outro é convertido para float.

## Módulos
- Um módulo é um arquivo que contém uma coleção de definições de funções, classes e etc.
- Para utilizar um módulo primeiro precisamos importar com um comando que possui a sintaxe `import <modulo>`.
- Depois para utilizar uma função deste módulo utilizamos a notação de ponto: `<modulo>.<ponto>(argumento1, argumento2, ...argumentoN)`.

## Definição de funções
- A sintaxe para a definição de funções é:
```
def <nome-da-funcao>(<parametros>):
    <instrucoes>
```
- As instruções precisam estar indentadas a partir da margem esquerda.

## Vantagens na criação de funções
- Colocar um nome em um grupo de comandos e assim esconder a complexidade do código.
- Reutilização de código.

## Fluxo de execução
- Fluxo de execução é a ordem que os comandos são executados.
- Chamadas de funções causam um desvio no fluxo de execução.

## Parâmetros
- Variáveis locais que recebem argumentos.

## Traceback
- Lista de funções que estão em execução.