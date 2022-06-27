# Textos



- Categorias de propriedades para manipular textos:

  - Font styles: Manipula a fonte
  - Text layout styles: Manipula o layout do texto

  

  ## Fontes

  - O texto é exibido na context box
  - Começa no canto superior esquerdo e vai até o final da linha
  - Ao chegar no final, o texto desce pra uma nova linha
  - Isso até o conteúdo ser exibido totalmente na caixa
  - Shorthand:
    - `font`
    - `font-style font-variant font-weight font-stretch font-size line-height font-family`
    - font-style > font-weight > font-size > [line-height] > font-family
    - deve haver uma barra entre `font-size` e `line-height`

### Cores

- `color`: Aplica uma cor ao foreground (ex.: textos, text-decoration, etc.) do conteúdo da caixa

### Famílias de fontes

- `font-family`:
  - Configura qual fonte exibir
  - Se não for possível localizar qualquer fonte, usa uma fonte padrão do navegador
  - Pode receber uma pilha de fontes, em que cada uma é testada
- Fontes **seguras**:
  - são fontes que são disponíveis na maioria dos dispositivos
  - Arial:
    - Melhor usar Helvetica, pois tem uma forma mais *agradável*, quando possível
- Fontes padrões/genéricas:
  - são fontes *muito genéricas*, onde o navegador tenta escolher uma fonte mais *apropriada*
  - `serif`: Fontes com serifa (traços)
  - `sans-serif`: Sem serifa
  - `monospace`: Largura de cada caractere é o mesmo
  - `cursive`: caligrafia
  - `fantasy`: decorativa

## Tamanho da fonte

- `font-size`
- valores medidos em unidades `<length>` ou porcentagens
- principais unidades utilizadas (**para dimensionar texto**):
  - `em`: 1 em = tamanho da fonte no elemento pai (mais especificadamente a largura da letra M em caixa alta no elemento pai)
  - `px`:
    - define a altura da fonte em **pixeis**
    - é uma unidade absoluta, portanto o valor computado vai o mesmo na maior parte das vezes
  - `rem`: 1 rem = tamanho da fonte do elemento raiz 
- é recomendado evitar alterar o tamanho da fonte em containers
- utilizar `rem` na medida do possível para ficar tudo mais simples

## Estilo, peso, transformação e decoração

- `font-style`: estilo da fonte (itálico ou não)
  - `normal`: fonte normal
  - `italic`: tentará usar a variante itálica da fonte; caso contrário usará `oblique`
  - `oblique`: simula uma fonte itálica criada inclinando a fonte normal
- `font-weight`: grossura da fonte (negrito)
  - `normal`: fonte normal
  - `bold`: negrito
  - `lighter`: a fonte vai ficar *um passo* mais **leve** que a fonte do elemento pai.
  - `bolder`: a fonte vai ficar *um passo* mais **pesada** que a fonte do elemento pai.
  - `100-900`: permite um controle mais apurado do negrito
- `text-transform`: transformação da fonte (capitalização e o tipo de caixa)
  - `none`: nenhuma transformação
  - `capitalize`: Cada Palavra Assim
  - `uppercase`: ASSIM
  - `lowercase`: assim
  - `full-width`: cada glifo vai estar dentro de uma **quadrado** de **mesma largura**
    - permite um alinhamento entre caracteres latinos/caracteres asiáticos
    - não é bastante suportado
- `text-decoration`: decoração da fonte
  - `none`: desativa
  - `underline`: sublinhado
  - `overline`: linha encima do texto
  - `line-through`: um riscado
  - aceita vários valores ao mesmo tempo (ex. `underline overline`)
  - shorthand para as props. `text-decoration-color`, `text-decoration-style`, `text-decoration-line`
  - `text-decoration-line`: tipo de decoração (ex.: `underline, overline, etc`)
  - `text-decoration-style`: estilo da decoração
  - `text-decoration-color`: cor

## Sombras de texto	

- `text-shadow`:

  - Aplica uma **sombra** ao texto

  - Aceita 4 valores:

    1. deslocamento horizontal: positivo vai para a direita e negativo para a esquerda

    2. deslocamento vertical: negativo vai para cima e positivo para baixo

    3. blur (desfoque/raio de espalhamento):

       - quanto mais alto o valor é, mais amplamente espalhada a sombra fica

       - o padrão é 0: não há desfoque

    4. cor

  - Podemos aplicar várias sombas/valores, separando por vírgulas



## Layout do texto

- Propriedades que afetam o layout do texto
- `text-align`:
  - Alinha o texto na caixa de conteúdo do elemento
  - `left`: justifica o texto à esquerda
  - `right`: justifica o texto à direita
  - `center`: centraliza o texto
  - `justify`:
    - o texto será espalhado horizontalmente, através da variação de espaços entre as palavras
    - cuidado com palavras longas
- `line-height`:
  - Determina a altura das linhas de texto
  - Valores:
    - Valores do tipo `<length>`
    - Valores sem unidades: o valor especificado é multiplicado pelo `font-size`
- `text-indent`: especifica um espaço horizontal antes da primeira linha do texto

## Listas

### Espaçamento de listas

- Devemos dar um espaçamento vertical consistente entre os elementos ao redor para uma lista (chamado de **ritmo vertical**)
- E dar o mesmo espaçamento horizontal entre elas

## Estilização

- ```css
  /* Define o tipo de marcador */
  list-style-type: square;
  
  /* Define a posição do marcador */
  /* inside: dentro das listas */
  /* outside: fora das listas */
  list-style-position: inside;
  
  /* Define uma imagem para o marcador */
  /* Se não for possível carregar a imagem, */
  /* o marcador padrão será utilizado. */
  /* Não temos muito controles sobre o tamanho e posição do marcador */
  /* list-style-image: url(example.jpg); */
  /* list-style-image: linear-gradient(to left, blue, red); */
  
  /* Shorthand */
  list-style: inside upper-alpha ;
  ```

- `list-style-type`: tipo de marcador.

  - `disc`
  - `circle`
  - `square`
  - `none`
  - `upper-alpha` || `upper-latin` + `lower-alpha` || `lower-latin`
  - `upper-roman` + `lower-roman`

- `list-style-position`: onde o marcador deve estar. dentro (`inside`) ou fora (`outside`) da lista.

- `list-style-image`: permite especificar um marcador customizado através de uma imagem.

- `list-style`: shorthand, em qualquer ordem, 1-3 propriedades

## Estilizando links

- Cada link tem estados que podem ser selecionados a partir de pseudo-classes:
  - Link: Não foi visitado e possui um destino. `:link`
  - Visitado: Foi visitado pelo usuário. `:visited`
  - Focado: O link está em foco, por exemplo, ao pressionar tab. `:focus`
  - Hover: O ponteiro do mouse está sobre o link. `:hover`
  - Ativo: O link foi ativado, por exemplo, clicado. `:active`
- Devemos utilizar as pseudo-classes nesta ordem acima, caso contrário, ao estilizar uma mesma propriedade, pode haver conflitos, pois quando um link está num certo estado, também implica que esteja em outros estados.
- Ao estilizar links devemos manter o mais próximo do comportamento esperado pelos usuários de links na web, para não os confundir:
  - destaque o link, por exemplo, utilizando sublinhado
  - destaque o link quando estiver no estado de hover ou focado. Já para quando está ativado, destacar de uma forma diferente.

## Exercícios

1. Das propriedades de manipulação de texto nas CSS, podemos classificar em dois grandes grupos. Quais são?
2. Como funciona a propriedade de dimensionamento da fonte?
3. O que a propriedade `color` especifica?
4. Em relação à propriedade `font-family`, o que é uma pilha de fontes e fontes seguras?
5. Como funciona as propriedades `font-style`, `font-weight`, `text-decoration`, `text-transform`?
6. Como podemos aplicar sombras no texto? E mais de uma sombra?
7. Como aplicar o tamanho da fonte, estilo da fonte, altura da linha e família de fontes com apenas 1 declaração?
8. Crie uma regra que seleciona elementos do tipo `p` e estilize da seguinte forma, utilizando no máximo 2 declarações:
   - A fonte deve ser "Tatakae" e não possui uma versão itálica;
   - Caso a fonte não exista, a outra fonte deve ser *segura* e se não existir, a outra deve ser *genérica*;
   - Deve haver uma linha encima, no meio e embaixo do elemento;
   - A altura das linhas do texto deve ser de 1,5 vezes o tamanho da fonte do elemento;
   - Deve ter uma fonte relativamente um pouco menos grossa (leve) que o elemento pai;
   - O texto deve ter um estilo *itálico*;
   - Cada letra deve estar em letra maiúscula; 
   - O texto deve estar justificado;
   - O início da primeira linha do texto deve estar deslocado horizontalmente para a direita `50px`;
   - O texto deve ter uma sombra configurada da seguinte forma:
     - deslocada para a **esquerda**, 5px
     - deslocada para **baixo**, 5px
     - deve ter um espalhamento de 5px
     - a cor deve ser a do próprio elemento
9. O que são fontes seguras e genéricas? Cite 1 fonte segura e 5 fontes genéricas.
10. O que são pilhas de fontes?
11. Quais são os estados possíveis de um link? Como estilizar estes estados via CSS?
12. Qual é a ordem das pseudo-classes de links?