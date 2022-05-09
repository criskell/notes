# Capítulo 13

## Psicologia das cores

- Psicologia das cores é um estudo sobre as emoções que as cores proporcionam.
- As cores passam emoções para o subconsciente das pessoas, influenciando em suas escolhas.

## Círculo cromático

- Uma representação gráfica simplificada de várias cores na forma de um círculo.
- Uma das funções do círculo é obter **harmonia de cores**.
- **Simetria**, **cores** e **fontes** são algumas das técnicas para deixar algo agradável.
- Podemos dividir em 12 vezes o círculo, onde cada divisão é uma **cor**. 3 cores são primárias, 3 cores são secundárias e 6 cores são terciárias.

### Tipos de cores

- Cores primárias: Não se dividem. O vermelho, amarelo e azul são cores primárias.
- Cores secundárias: Formadas adicionando uma cor primária em outra cor primária. Laranja, violeta e verde são cores secundárias.
- Cores terciárias: Formadas adicionando cores primárias e secundárias. No círculo estão **entre** uma cor primária e uma secundária.

## Cores nas CSS

- Formas de representar:
  - Hexadecimal: Por exemplo, `#6a5c9a` é 0x6a de vermelho, 0x5c de verde e 0x9a de azul. Podemos adicionar opacidade adicionando mais dois dígitos: `#6a5c9a05` ou seja, 0x05 de opacidade.
  - RGB
  - HSL: hsl (sem opacidade) e hsla (com opacidade). HSL: Hue (Matiz), Saturation (Saturação) e Luminosity (Luminosidade)
- Nas telas, cada cor possui uma quantidade de vermelho, verde e azul.

## Temperatura

- Classificamos as cores do círculo cromático em quentes ou frias.
- Cores quentes dão uma sensação de **calor** e **proximidade**.
- Cores frias dão uma sensação de **calma**, **frescor** e **tranquilidade**.

## Paleta de cores

- Escolhemos uma paleta de cores de 3 a 5 cores.

### Cores complementares
- Uma cor complementar a outra é uma cor que está no extremo oposto do círculo cromático.
- Caracterizadas por serem de alto contraste.

### Cores análogas
- Uma cor análoga a outra é uma cor que é "vizinha" a ela, ou seja, está bem próxima.
- Tem nenhum ou pouco contraste.

### Cores análogas e uma complementar
- Também chamada de **dividir e complementar**.
- São obtidas obtendo primeiramente 2 cores análogas e uma complementar a alguma cor.
- A complementar será de alto contraste, certamente.

### Cores análogas relacionadas
- Cores análogas relacionadas são obtidas pegando primeiramente 2 cores análogas e, no sentido horário ou anti-horário, pular uma cor e selecionar uma terceira cor.
- No total serão 3 cores e a terceira não será de alto contraste e irá possuir uma similaridade.

### Cores intercaladas
- São cores intercaladas por `n` cores.
- Para obter cores intercaladas, pegamos uma primeira cor, pulamos `n` cores, pegamos a segunda cor, pulamos `n` cores e assim sucessivamente.
- Cores intercaladas geralmente tem mais contraste e menos similaridade.

### Cores triádicas
- São cores intercaladas por **três** cores.
- Curiosidade: As cores primárias e secundárias são cores triádicas.

### Cores em quadrado
- São cores intercaladas por **duas** cores.
- **Devem** formar um quadrado.
- São cores fortes e bem balanceadas.

### Cores tetrádicas
- Formada por dois pares de cores complementares.
- Forma um retângulo.
- Podem ter cores análogas, mas não necessariamente.

### Monocromia
- É uma técnica que consiste atingir harmonia utilizando apenas **uma** (mono) cor e várias tons dela.
- Pegamos uma cor e aumentamos ou diminuimos a **saturação** e **brilho**.

## Gerando paletas
- Podemos gerar paletas com as ferramentas: Adobe Color, Paletton e Coolors.
- Funções do Adobe Color:
  - Extrair um tema e degradê de uma imagem.
    - Gerar temas a partir de logotipo do cliente.

- Funções do Paletton:
  - Gerar paletas e pré-visualizar como ficaria num site.

- Funções do Coolors:
  - Gerar paletas de cores.
  - Tem uma função que permite bloquear uma cor e ao apertar espaço, ele vai gerando cores harmonicas com a escolhida.


## Degrâde nas CSS

- Podemos criar degrâde nas CSS utilizando as funções `linear-gradient` e `radial-gradient`.

- A função `linear-gradient` cria um degradê linear e aceita os seguintes argumentos:

  - Para onde vai o degradê (1º argumento): Pode ser tipo `to top` e em graus.

  - Uma lista variável de cores, junto com a porcetagem de aparecimento.

  - Exemplo:

    ```css
    header {
        /**
         * Cria um gradiente de 50 na ordem:
         * #95A31C (30% de presença) -> #B5C4A8 (20% de presença) -> #5c4a9a (50% de presença)
         */
        background: linear-gradient(50deg, #95A31C 30%, #B5C4A8 20%, #5c4a9a 50%);
    }
    ```

- A função `radial-gradient` cria um gradiente **radial** e aceita os argumentos:

  - 1º argumento: `circle` é utilizada para criar um **gradiente radiano circular**.
  - nº argumento: Cores do gradiente que podem possuir uma porcentagem.
