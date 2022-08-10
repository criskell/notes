# Variáveis

- Variáveis são *containers* para *valores*.

## Tipos de dados

- **n**umber
- **s**tring
- **o**bject: Um objeto é uma estrutura que traz uma "ideia" do "mundo real"
- **f**unction
- **b**oolean: Este tipo consiste em valores lógicos que representam verdadeiro ou falso.
- **u**ndefined

## Tipagem dinâmica

- Tipagem dinâmica é uma característica que quer dizer que uma variável podem assumir valores de qualquer tipo.

## Declaração de variáveis

- **Declarar** uma variável é **criar** uma variável, apenas isso.
- Uma variável pode ser declarada por:
  - `var <nome>`
  - `let <nome>`
- Na mesma instrução, podemos inicializar imediatamente com o operador de atribuição:
  - `var <nome> = <valor>`
  - `let <nome> = <nome>`

## Inicialização de variáveis

- Inicializar uma variável é atribuir um valor **inicial** para esta variável.
- Podemos fazer isso na mesma hora de declarar ou posteriormente (constantes não permitem isso)

## Reatribuição de variáveis

- Consiste em trocar o valor atual do container (variável) para outro valor.

### var vs let

Diferenças:

```js
// var:
// É permitido redeclarar mais de uma vez uma variável com `var`
var possoDeclararMaisDeUmaVez = false;
var possoDeclararMaisDeUmaVez = true; // ok
// Possui o mecanismo de hoisting
// não irá gerar um erro, pois variáveis não declaradas geram erro, mas ela já foi declarada via hoisting
console.log(hoisted);
var hoisted;
// Possui escopo global ou de função
{
    var x = 5;
}
console.log(x); // 5

// let
// Não é permitido redeclarar
let test1 = 5;
let test1 = 5; // erro
// Não possui um mecanismo de hoisting
console.log(test1); // não gerará um erro
let test1 = 20;
// Possui um escopo de bloco, função ou global
{
    let x = 10;
}
console.log(x); // erro
```

## Constantes

- Constantes são *containers* que sempre armazenam um **mesmo** *valor*

- Regras:

  - Uma constante declarada deve ser **imediatamente** inicializada:

    - ```js
      // Incorreto
      const x;
      ```

    - ```js
      // Correto
      const x = 50;
      ```

  - Uma constante não pode ser reatribuída a um novo valor:

    - ```js
      // Incorreto
      const x = 20;
      x = 30; // <--
      ```

    - ```js
      // Correto
      const x = 50;
      // sem reatribuição
      ```

## Exercícios

1. O que são variáveis.

2. Diferencie constantes de variáveis (o **conceito** e **manipulação**)

3. Qual é a diferença de `let` e `var`?

4. Diferencie declaração de inicialização de variáveis.

5. O JavaScript possui qual estilo de tipagem? Como se define tal tipagem?

6. Cite 6 tipos de dados do JavaScript.

7. Encontre os dois erros.

   ```js
   const x;
   x = 5;
   ```

   