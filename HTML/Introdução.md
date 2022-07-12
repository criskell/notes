# Introdução

- HTML é uma linguagem de marcação utilizada para definir a estrutura do conteúdo de uma página web.
- Consiste numa série de elementos utilizados para delimitar partes do conteúdo para que tenha um determinado significado, aparência e/ou comportamento.

## Anatomia de um elemento HTML

```
<p class="editor-note">My cat is very grumpy</p>
```

- A **tag de abertura** `<p>` que define o começo de um elemento.
- **A tag de fechamento** `</p>` que define o fim do elemento.
- O **conteúdo**. Neste caso é apenas texto.
- O elemento é a tag de abertura, o conteúdo e a tag de fechamento.
- Elementos podem ter atributos e estes atributos aparecem na tag de abertura.
- Os atributos definem **informações extras** do elemento.
- `Tag de abertura (+atributos) + conteúdo + tag de de fechamento = Elemento`

## Aninhamento de elementos HTML

- Aninhamento é colocar um elemento dentro de outro elemento.

## Elementos vazio

- Não possuem conteúdo e nem tag de fechamento.
- Exemplo: `<br>`

## Elemento x tag

- Elemento é uma parte de uma página web e fazem parte do DOM; tag é utilizada para marcar o início ou fim de um elemento no código.

## Anatomia de um documento HTML

```html
<!doctype html>
<html>
    <head>
    	<title>Página</title>
        <meta charset="utf-8">
    </head>
    <body>
    	Conteúdo
    </body>
</html>
```

- `<!doctype html>`: Garante que o documento se comporte corretamente.
- `html`: Elemento raiz da página. Vai abranger todos os elementos.
- `head`: Elemento que abrange tudo que **não é conteúdo**.
- `body`: Elemento que abrange tudo que **é conteúdo**.

## Listas

- Listas ordenadas: A ordem **importa**.
- Listas não ordenadas. A ordem **não importa**.

## Categorias de um elemento HTML

- Podemos dividir os elementos do HTML em (obs.: o HTML5 redefiniu as categorias de elemento):
  - Elementos em bloco (block): Formam um bloco visível na página, precedido e seguido por uma nova linha.
  - Elementos em linha (inline): Envolvem apenas **pequenas partes** do conteúdo e não cria novas linhas.

## Atributos booleanos

- Atributos booleanos podem ter apenas dois estados: verdadeiro ou falso.
- O único valor que um atributo booleano pode ter é, geralmente, o nome do próprio atributo. Por exemplo: `disabled="disabled"`. Neste caso, isto significaria um estado verdadeiro. Podemos emitir também o valor, deixando apenas o nome: `disabled`.
- A ausência do atributo significaria um estado falso.

## Espaços em branco

- O analisador HTML reduz espaços em branco (quebras de linha, caracteres de espaço e etc.) para um único espaço.

## Referências de entidades

- Também chamadas de entidades e referências de caracteres
- Referências de entidades representam um caractere.
- Começa com `&` e termina com `;`.
- Podemos ter um número, `&#xNUMERO`;
- Exemplo: `&nbsp;`
- Casos de uso:
  - Exibir caracteres reservados
  - Mostrar caracteres difíceis de digitar 

- Algumas:
  - `&nbsp`: Espaço sem quebra. Pode ser utilizado para juntar 2 palavras que sempre ficam juntas, exemplo: `R$&nbsp;35`
  - `&amp`: para `&`


## Questões

1. O que é o HTML
2. Qual é a anatomia de um elemento?
3. O que é um elemento?
4. Qual é a anatomia de uma página web?
5. Quando usar listas ordenadas e não ordenadas?
6. O que são referências de entidades?