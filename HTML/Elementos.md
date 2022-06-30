# Elementos

- Um elemento é um pedaço da página web, como parágrafos, títulos, etc.
- O HTML consiste numa série de elementos utilizados para delimitar partes do conteúdo para que tenha um determinado significado, aparência e/ou comportamento.

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

## Empty elements x void elements e self-closing tags

- *Empty elements* não possuem conteúdo.
- *Void elements* **não podem** ter conteúdo e tag de fechamento.
- As vezes *empty elements* são chamados de *void elements*
- A `/` no final da tag de abertura de *void elements* são opcionais e não possuem efeito. As tags que terminam com `/` são chamadas de *self-closing tags*, ou seja, que não tem uma tag de fechamento.
- Exemplo: `<br>`

## Elemento x tag

- Elemento é uma parte de uma página web e fazem parte do DOM; tag é utilizada para marcar o início ou fim de um elemento no código.