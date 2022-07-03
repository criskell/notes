# Seletores

- Seletores são padrões que correspondem com elementos HTML.
- Representam estruturas HTML e podem serem utilizados para condições ou uma descrição desta estrutura.
- Seletor **simples** é uma condição única (simples/atômica) para corresponder elementos.
- Seletor **composto** é uma sequência de seletores simples, portanto representa várias condições.
- Seletor **complexo** é uma sequência de seletores **compostos** separados por combinadores.
  - Um pseudoelemento pode ser adicionado no último seletor composto.

- Podemos dividir os seletores nas seguintes categorias:
  - Seletores de tipo, classe e ID
  - Seletores de atributos
  - Pseudoclasses e pseudoelementos

## Listas de seletores

- Listas de seletores são listas separadas por vírgulas de seletores individuais onde a regra CSS será aplicada para todos os seletores.
- Se um seletor for inválido na lista (ex.: `..oi`), toda a regra será ignorada. 
- Sintaxe: `<seletor1>, <seletor2, ...seletorN>`

## Seletor de tipo, classe e ID

### Seletor de tipo

- Seletor de tipo seleciona elementos de um tipo. Exemplo: `h1`

### Seletor universal

- Seleciona todos os elementos.

### Seletor de classe

- Seletor de classe seleciona elementos de uma classe.

### Seletor de ID

- Seletor de ID seleciona um elemento com um id.

## Seletor de atributos

- Este tipo de seletores seleciona elementos com base no atributo.
- Podemos utilizar o sinalizador (flag) `i` para correspondência entre valores de atributos ser **case-insensitive**. Se não informado, as correspondências será **case-sensitive**. Podemos utilizar o sinalizador `s` para a correspondência entre valores de atributos ser case-sensitive.

#### Seletores de presença e valor

- Selecionando um elemento com um atributo presente: `[href]`.
- Selecionando um elemento com um atributo **exatamente** igual a outro valor: `[href=valor]`.
- Selecionando um elemento com um atributo que é **exatamente** igual a um outro *valor* ou que possui um *valor* numa **lista separada por espaços**: `[attr~=valor]`
- Selecionando um elemento com um atributo que é **exatamente** igual a outro *valor* ou que **começa** com o ***valor* seguido por um hífen**: `[attr|=valor]`

#### Seletores de correspondência de substrings

- Este grupo permite outras correspondências mais avançadas de substrings.
- Selecionando elementos cujo valor do atributo `attr` começa com `value`: `[attr^=value]`
- Selecionando elementos cujo valor do atributo `attr` termina com `value`: `[attr$=value]`
- Selecionando elementos cujo valor do atributo `attr` possui `value` em qualquer posição: `[attr*=value]`

## Pseudoclasses e pseudoelementos

### Pseudoclasses

- Pseudoclasses são seletores que selecionam elementos em um certo estado.
- Agem como se fossem classes adicionadas manualmente por isso são chamadas de pseudoclasses.
- Algumas pseudoclasses:
  - `:first-child`: Seleciona um elemento que é o primeiro filho.

### Pseudoelementos

- Pseudoelementos agem como se fossem elementos reais para **partes** específicas de um elemento selecionado.
- Podemos especificar pseudoelementos utilizando a sintaxe `::pseudoelemento` no seletor.

## Combinadores

- Um combinador **combina** dois seletores de forma que eles **expressam um relacionamento**.
- `X Y`: Combinador **descendente** ( - espaço):
  - Corresponde aos elementos correspondentes ao **segundo seletor** (`Y`) que possui um **ancestral** correspondente ao **primeiro seletor** (`X`). Outra explicação:
  - Corresponde ao elemento `Y` que seja descendente de `X`. Outra explicação:
  - Elemento `Y` está contido no elemento `X`.
- `X > Y`: Combinador **filho** (`>`):
  - Corresponde aos elementos correspondentes ao **segundo seletor** que são filhos **diretos** dos elementos correspondidos ao **primeiro seletor**. Outra explicação:
  - Corresponde ao elemento `Y` que seja filho imediato de `X`. 
- `X + Y`: Combinador **irmão adjacente** (`+`):
  - Corresponde ao elemento correspondente ao **segundo seletor** que é o **próximo irmão** dos elementos correspondentes ao **primeiro seletor**. Outra explicação:
  - Corresponde ao elemento `Y` que seja irmão imediato de `X`, ou seja, `X` e `Y` possui o mesmo pai e `X` precede imediatamente `X`. Outra explicação:
  - Elemento `Y` que é **imediatamente** precedido por `X`.
- `X ~ Y`: Combinador **irmão geral** (`~`):
  - Corresponde aos elementos correspondentes ao **segundo seletor** que são os **próximos irmãos** dos elementos correspondentes ao **primeiro seletor**.  Outra explicação:
  - Corresponde ao elemento `Y` quando é precedido por `X`.  Outra explicação:
  - Elementos `Y` que vem depois de `X`.