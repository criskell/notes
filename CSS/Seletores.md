# Seletores

- Seletores são padrões que correspondem com elementos HTML.
- Podemos dividir os seletores nos seguintes tipos:
  - Seletores de tipo, classe e ID
  - Seletores de atributos
  - Pseudoclasses e pseudoelementos
  - Combinadores

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
- Combinador **descendente** (` ` - espaço): Corresponde aos elementos correspondentes ao **segundo seletor** que possui um **ancestral** correspondente ao **primeiro seletor**.
- Combinador **filho** (`>`): Corresponde aos elementos correspondentes ao **segundo seletor** que são filhos **diretos** dos elementos correspondidos ao **primeiro seletor**.
- Combinador **irmão adjacente** (`+`): Corresponde ao elemento correspondente ao **segundo seletor** que é o **próximo irmão** dos elementos correspondentes ao **primeiro seletor**.
- Combinador **irmão geral** (`~`): Corresponde aos elementos correspondentes ao **segundo seletor** que são os *-**próximos irmãos** dos elementos correspondentes ao **primeiro seletor**.