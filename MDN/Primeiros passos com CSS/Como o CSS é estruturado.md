# Como o CSS é estruturado

## Aplicando CSS em HTML

- Podemos aplicar CSS no HTML com estilos externos, internos e inline.
- Estilos externos: São estilos que residem fora do documento HTML.
- Estilos internos: São estilos que residem dentro de um documento HTML no elemento `style`.
- Inline: São estilos que são aplicados a um único elemento no atributo `style`.

## Seletores

- Seletores selecionam elementos HTML.
- Cada regra CSS começa com um seletor (`exemplo`) ou uma lista de seletores (`exemplo, outroexemplo`).

## Especifidade e cascata

- Especifidade e cascata são regras que determinam como declarações conflitantes de uma mesma propriedade para um mesmo elemento são resolvidos.
- A regra da cascata diz que a última declaração num mesmo arquivo de CSS é prevalecida caso as declarações esteja na mesma regra ou caso estejam em regras diferentes com seletores de especifidades iguais.
- A regra da especifidade diz que quando as declarações estão em seletores distintos, mas para um mesmo elemento, irá prevalecer a declaração que está na regra com o seletor mais específico.

## Anatomia de uma regra

- Propriedades são **identificadores** que indicam **recursos estilísticos**.
- Cada propriedade tem **valores** que indica **como** deve modificar a propriedade.
- Juntando uma propriedade a um valor, temos uma declaração.
- Um bloco de declarações é delimitado por chaves e consiste em declarações separadas por ponto e vírgula.
- Uma regra (também chamada de conjunto de regras) consiste num seletor ou uma lista de seletores junto com um bloco de declarações.
- Portando, `<regra> ::= <seletor>|<lista-de-seletores> <bloco-declaracoes>`.

## Funções

- Valores podem assumir a forma de uma função com a sintaxe `funcao(argumento1, argumento2, ...argumentoN)`

## @rules

- @rules são instruções que definem como o CSS deve se **comportar**.

## Shorthands

- Algumas propriedades são shorthands para outras propriedades, ou seja, permitem atribuir vários valores para diferentes propriedades numa única declaração.