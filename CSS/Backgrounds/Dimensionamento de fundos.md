# Dimensionamento

- A propriedade `background-size` especifica como um plano de fundo deve ser dimensionado em seu container.
- A cor de fundo ficará preencherá lugares que não possuem imagem de fundo e aparecerá por trás de imagens com transparência ou translucidez.
- Sintaxes:
  - Palavra-chave
  - Um valor, apenas para largura e a altura fica `auto`
  - Dois valores, para largura e altura.
- Valores:
  - `auto`:
    - Dimensiona a imagem
    - Proporções intrínsecas são mantidas 
  - `cover`:
    - Dimensiona a imagem para o menor tamanho possível para caber completamente em seu container
    - Preserva a proporção
    - Se a proporção do plano de fundo for diferente do container, a imagem será cortada verticalmente e/ou horizontalmente.
  - `contain`:
    - Dimensiona a imagem para ter o maior tamanho possível.
    - Se as proporções forem diferentes, o plano de fundo não aparecerá completamente no container.
    - Preserva a proporção
  - valor do tipo `<length>`:
    - Estica a imagem
  - valor em porcentagem
    - se refere à área de posicionamento do plano de fundo, determinada pela propriedade `background-origin`, sendo o padrão a *padding box*
    - se `background-attachment == fixed` então `area = viewport`

## Dimensões e proporções intrínsecas

- Dimensões intrínsecas = largura e altura
- Proporções intrínsecas = relação largura/altura

## Exercícios

1. O que acontece se passar apenas um valor?
2. Ao que as porcentagens se referem?
3. Como funciona o valor `auto`?