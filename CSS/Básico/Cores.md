# Cores

- Temos diversas formas de adicionar cores numa página em qualquer propriedade que aceite o tipo `<color>`:

## Cores numéricas

### Cores hexadecimais

- A notação hexadecimal especifica a cor na forma RGB utilizando dígitos hexadecimais, ou seja, atribui intensidades numéricas (0-255) para vermelho, verde e azul.
- Para converter um número hexadecimal de 2 dígitos para um número decimal, devemos multiplicar o primeiro dígito por 16 e somar com o segundo dígito, por ex.: `BF (base 16) = 11 * 16 + 15 = 191`
- Códigos hexadecimais podem ter dois dígitos a mais, especificando um valor alfa, ou seja, um valor para transparência, de 0 a 255. Ex.: `#FF00FF55 => alfa = 0x55 = 85 = 33.3333333333% de transparência (255)`
- Abreviações:
  - `#xyz -> #xxyyzz`
  - `#wxyz -> #wwxxyyzz`

### RGB

- Podemos especificar cores utilizando a função `rgb(red, green, blue)` onde `red`, `green` e `blue` equivalem aos canais vermelho, verde e azul. Podem ser números entre 0 ou 255 ou porcentagens de 255.
- Podemos especificar na forma também de `rgb(red green blue[ / alpha])` onde:
  - `alpha` pode ser um número decimal entre 0 e 1 ou uma porcentagem para transparência. Podemos utilizar RGB com alfa de forma mais compatível com outros navegadores utilizando a função `rgba`.

### HSL

- `hsl(hue, saturation, luminosity)`:
  - Matiz (ou tonalidade), saturação, luminosidade (ou leveza)
  - O alfa é adicionado da mesma forma que a função `rgb`. Exemplo: `(hsl(h s l / 0%) || hsla(h, s, l, 0)), hsl(h s l / 0.5), hsla(h, s, l, 0.20%)`
  - Formas:
    - `hsl(h, s, l)`
    - `hsl(h s l)`
  - `hue`:
    - Valor na roda de cores, na faixa de 0 a 360. Um ângulo.
    - Pode ser um número ou um valor do tipo ângulo (ex.: `0deg` ou apenas `0`).
  - `saturation`:
    - Porcentagem de quão vibrante o tom é. Quando mais saturada, menos cinza e quanto menos saturada, mais cinza.
  - `luminosity`:
    - Porcentagem de quão leve a cor é.
    - Descreve a escala do preto ao branco na cor. `100%` é totalmente branco.

### Palavra-chaves

- Podemos utilizar cores com palavra-chaves, exemplo: `pink, blue, yellow`.
- Palavras-chaves especiais:
  - `transparent`: Cor totalmente transparente.
  - `currentColor`: Valor computado da propriedade `color` do elemento.

## Questões de revisão

1. Como expressar cores nos formatos hexadecimal, `rgb + rgba` e `hsl + hsla`? Descreva cada parâmetro das funções e suas formas.
2. Quais são as palavras-chaves especiais para descrever cores?