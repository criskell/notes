# Condicionais e recursividade

## Tipo booleano
- Verdadeiro (`True`) ou Falso (`False`).

## Operadores de comparação
- `==, !=, >, <, <=, >=`

## Operadores lógicos
- E (`and`), OU (`or`) e NÃO (`não`).
- Os operandos de operadores lógicos não precisam ser booleanos pois Python não é muito rigoroso.
- Qualquer número diferente de zero é verdadeiro.

## Execução condicional
- Estruturas condicionais permitem mudar o comportamento do código de acordo com determinadas condições.

## Estrutura if
- `if` é uma estrutura condicional composta que permite alterar o fluxo de execução a partir de uma condição booleana. A sintaxe da estrutura `if` é a seguinte:
```py
if condicao:
    # corpo (novo ramo)
```
- Estrutura completa:
```py
if condicao:
    # corpo (novo ramo)
elif outraCondicao:
    # corpo (novo ramo)
else:
    # corpo (novo ramo)
```

## Instrução return
- A instrução `return` termina a execução de uma função com um resultado.

## Frames
- Cada vez que o interpretador chamada uma função, é criado um novo quadro para armazenar as variáveis locais desta função e este quadro é colocado numa pilha (stackframe).