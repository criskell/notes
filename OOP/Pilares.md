# Pilares

## Abstração

- Abstrair é omitir detalhes num conjunto de conceitos e preservar somente o essencial, retirando as diferenças, resultando numa abstração.
- Abstração é ocultar coisas desnecessárias no nível do design.
- Nível de design se refere a estrutura, quais são os métodos e atributos.
- Nível da implementação se refere ao funcionamento, como funcionam seus atributos e métodos.

## Encapsulamento

- Esconder os dados de um objeto para esconder a implementação e do comportamento de classes que depende de determinadas variáveis corretas.
- Objetos são ditos encapsulados quando seu estado é privado e há métodos públicos para acessar-los.
- Proteger contra mudanças no estado do objeto que desrespeita as normas impostas pelos métodos e ocultar detalhes desnecessários para o cliente no nível de implementação.
- Esconder todas as informações que não são necessárias para usar a classe.
- Exemplo: O controle de uma TV possui uma cápsula com botões, portanto está encapsulado.

## Herança

- Uma classe herda características e comportamentos de outra classe.
- Herança direta: Quando uma classe X herda diretamente Y. (dizemos que X é Y).
- Herança indireta: Quando uma classe X herda Y que herda Z, herdando indiretamente Z. (dizemos que X é Y, Y é Z e Y por ser Z, X também é Z)
- Devemos manter a regra do ser/estar: Exemplo: Carro e Bicicletas são Veículos.
- Generalização: Tomamos características comuns a classes em uma classe base.
- Especialização: Tomamos características singulares que dão o valor de subtipo numa classe derivada.

## Polimorfismo

- Polimorfismo consiste em uma estrutura polimórfica assumir diferentes formas em certas circustâncias.
- Polimorfismo é a capacidade de apresentar a mesma interface para diferentes formas subjacentes (**implícitas, ocultas**).
- Polimorfismo é a capacidade de um objeto responder a diferentes mensagens idênticas a cada um a sua maneira.
- Pode acontecer de diversas formas como sobrescrita de métodos.