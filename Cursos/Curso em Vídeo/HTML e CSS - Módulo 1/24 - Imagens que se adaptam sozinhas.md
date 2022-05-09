# Imagens que se adaptam sozinhas

- Podemos selecionar uma determinada imagem de acordo com a tela do usuário.
- Podemos usar a tag `picture` ou os atributos `srcset` e `sizes` na tag `img`.

## Tag picture

- A tag picture é utilizada para mostrar **diferentes versões** de uma imagem de acordo com o dispositivo e tela do usuário.
- Possui zero ou mais tags `source` e uma única tag `img`.
- A tag `source` tem os atributos `srcset`, `media` e `type`.
- O atributo `media` possui uma media query.
- A tag `img` é utilizada como um **fallback **para o caso que nenhuma tag `source` é carregada ou caso a tag `picture` ou `source` não for suportada. Também é utilizada para outros atributos de imagem, como o atributo `alt`.
- Usos desta tag:
  - Direção de arte: Modificação de uma imagem para determinados dispositivos (exemplo: fornecer uma imagem mais simples num dispositivo pequeno).
  - Oferecer formatos de imagens alternativos para caso não seja suportado no navegador.
  - Diminuir o uso de dados selecionando uma imagem apropriada para o tamanho da tela.