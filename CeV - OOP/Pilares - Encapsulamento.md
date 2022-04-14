# Encapsulamento

- Proteção contra eu e a cápsula e vice-versa;

- Padronizar uma interface;

- Esconder o funcionamento;

- Encapsular:

  - Ocultar partes independentes da implementação, permitindo construir partes invisíveis ao mundo exterior.
    - Como funciona não importa.
    - O programa não precisa saber como o objeto foi feito.
  - Encapsular é tornar o objeto uma cápsula, com uma **interface**, de modo que **esconda sua implementação**, fazendo que não nos preocupemos com o funcionamento do objeto.

- Comunicamos com objetos através de mensagens.

- Interface: Lista de serviços fornecidos por um componente. É o contato com o mundo exterior que define o que pode ser feito com este objeto.

- Vantagens

  - Mudanças invisíveis
  - Reutilização
  - Redução de efeitos colaterais

- Diagrama de interface:

  ```markdown
  +----------------------------+
  |     <<interface>>          |
  |    Controlador             |
  +----------------------------+
  | + ligar()                  |
  +----------------------------+
                                    
  ^
  |
  | (uma seta significa implementa)
  |
  
  +----------------------------+
  |    ControleRemoto          |
  +----------------------------+
  | + ligar()                  |
  +----------------------------+
  ```

- Os métodos numa interface são chamado de métodos abstratos, ou seja, não possuem implementação (não importa).

- Implementar uma interface é adicionar cada funcionamento de cada método.

- Quando encapsulamos, nós tornamos todos os atributos privados, geralmente.