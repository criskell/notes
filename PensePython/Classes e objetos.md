# Classes e objetos

- Classe é um tipo personalizado.
- Objeto é uma instância de uma classe.
- Objeto e instância são intercambiáveis.
- Métodos semanticamente são iguais a funções mas o modo de definição é diferente e modo de invocação também.
- Sintaxe para classes:
```
class Classe:
    def metodo(objeto):
        pass
```
- Podemos invocar métodos em objetos utilizando a sintaxe de função que consiste em chamar a função diretamente na classe, passando o objeto e os argumentos do método:
```
Classe.metodo(objeto, ...argumentos)
```
- Ou chamar o método no objeto utilizando a sintaxe de método:
```
objeto.metodo(...argumentos)
```
- O objeto neste caso é chamado de sujeito.

## Métodos especiais
- `__init__`: Inicializa o objeto.
- `__str__`: Retorna uma representação do objeto como uma string.

## Sobrecarga de operadores
- Sobrecarga de operadores é alterar o comportamento de operadores em tipos personalizados.
- Por exemplo, ao definir o método `__add__` em uma classe estamos sobscrevendo o comportamento do operador de soma para o tipo em questão.

## Polimorfismo
- Funções que funcionam para vários tipos são chamadas de funções polimórficas.

## Atributos de classes x atributos de instância
- Atributos de instância estão associados com a instância da classe e atributos de classes estão associados com as classes.