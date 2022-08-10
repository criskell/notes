# Caixas de linha

- Uma caixa de linha armazena conteúdo **inline**.
- Utilizado pelo navegador para saber como dispor elementos **inline**.
- Os conteúdos fluem na direção **inline**.
- Por padrão, a caixa de linha ocupa toda a largura do container e sua altura é ajustada para a altura do maior conteúdo **inline**.
- Se um elemento não caber numa caixa de linha, irá ser criada uma nova caixa. O navegador tentará dividir o elemento num espaço em branco localizado dentro dele, e uma nova caixa de linha será adicionada, com parte do conteúdo do conteúdo continuando na nova caixa. Se não tiver um espaço em branco, ocorrerá um overflow com o elemento indo para fora da caixa (junto com a caixa de linha).

## Propriedades

- `line-height`:
  - Define a altura mínima da linha.
  - Valores:
    - Absolutos como `10px`
    - Relativos como `10em`, porcentagens ou números sem unidades
    - A porcentagem e os números sem unidades será resolvida com base no tamanho da fonte do elemento.
- `vertical-align`:
  - Define o alinhamento vertical de um elemento em relação a caixa de linha.
  - Valores:
    - `baseline`: Alinha a linha de base do elemento com a linha de base do elemento pai.
    - `middle`: Alinha o conteúdo no meio da fonte.