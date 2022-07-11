# Floats

- A propriedade `float` é utilizada para mover um elemento para a esquerda ou direita. Irá se deslocar até tocar um outro float ou a borda do containing block.
- Os textos e os elementos inline em fluxo normal depois deste elemento o envolvem, ficando lado a lado, e depois fica embaixo se não houve espaços.
- Elementos flutuantes não dão forma ao seu container pai.
- Elementos não flutuantes, não posicionados e de nível de bloco agem como se o float não estivesse lá, pois o float está fora de fluxo em relação a outros elementos.
- Geralmente, o dimensionamento de um float deve ser explícito.
- Casos de uso:
  - Páginas tableless


## Limpar floats

- A propriedade `clear` permite limpar floats do lado direito ou esquerdo de um elemento.
- Faz o conteúdo após o elemento flutuante ou o container dele renderizar abaixo dele.
- Isso permite resolver problemas de layout, por exemplo:
  - Elemento pai colapsado:
    - Ocorre quando um elemento pai não se expande totalmente para conter um float, mostrando pedaços do float na página.
    - Por que? Pois os floats estão fora de fluxo.
    - Soluções:
      - Elemento vazio: Criar um elemento vazio que limpe os floats. O pai se expandirá para conter ele e, consequentemente, conterá o float.
      - Flutuar o elemento pai / `overflow`: Isto irá criar um BFC que deve conter os floats.
      - `::after`: Limpar o float através do pseudo-elemento `after` em um elemento pai que contém floats, ao invés de adicionar um elemento não semântico como divs na marcação.
