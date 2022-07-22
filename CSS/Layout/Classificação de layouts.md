# Classificação de layouts

## Layout fixo

- Dimensões expressas em pixels
- Características:
  - Não se adaptam as resoluções/tamanhos de tela
  - Se for muito pequena, aparecerá uma barra de rolagem lateral
  - Possui um wrapper de largura fixa e os componentes dentro do wrapper possui larguras em porcentagens ou fixa
- Prós:
  - Fica mais fácil a vida do desenvolvedor
  - A largura é a mesma, portanto há menos problemas para conteúdos de largura fixa como imagens
  - Com compatibilidade com uma pequena resolução (ex. 800 x 600), o layout vai ser legível em resoluções maiores 
- Contras:
  - Falta de usabilidade
  - Pode aparecer barras de rolagens horizontais ou criar bastante espaço em branco
  - Diversidade de resoluções

## Layout fluído ou líquido

- Dimensões expressas em unidades de porcentagens da viewport
- Características:
  - Textos e imagens mantém seu tamanho
  - As dimensões do layout se alteram com a mudança do tamanho do navegador
- Prós:
  - Compatibilidade com telas menores
  - Não aparecer barra de rolagem, se bem definido
  - O espaço em branco é semelhante entre diferentes resoluções
- Contras:
  - O designer tem menos controle do design
  - Conteúdos de largura definida podem precisar serem definidos em várias larguras para diferentes resoluções
  - Em telas maiores, o excesso de espaço em branco pode ser grande
- Técnicas para lidar com layouts fluídos:
  - Definir largura mínima e máxima para usabilidade:
    - Assim, quando o usuário estiver fora destas larguras, o layout passa a ser fixo
    - E portanto, pode aparecer barras de rolagens
    - Já em telas maiores, fica mais legível

## Layout elástico

- Uma mistura entre layout fixo e fluído
- Larguras expressas em `em`
- O layout muda quando o tamanho da fonte muda
- Prós:
  - Dimensiona de acordo com as preferências do usuário
- Contras:
  - Difícil de implementar

## Layout híbrido

- Combina o layout fixo, fluído e elástico.
- Por exemplo, dimensionar um elemento em pixeis e o resto dos elementos em unidades `em` ou `%`

## Layout adaptável

- Um layout fixo em várias versões
- "Salta" entre versões
- No breakpoint, ele se comporta como um layout fixo

## Layout responsivo

- Combina o layout fluído e o layout adaptativo
- As imagens se adaptam
- Muda muito nos breakpoints
- Entre os breakpoints, se estende como um layout fluído