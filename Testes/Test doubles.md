# Test doubles

- Test double é um objeto que substitui uma dependência real de um outro objeto para fins de testes
- Fakes:
  - Testar como o código reage a grande quantidade de dados
  - São objetos muito próximos ao de produção
  - São test doubles que não possuem implementação real
  - Não possuem uma lógica
  - Retorna sempre o que foi estipulado
  - Usam algum atalho que torna inviável para produção
- Mocks:
  - Simulam interações de saída (chamadas que o teste realiza para alterar seu estado) com as dependências externas
  - Possuem expectativas sobre como devem ser chamados e se não forem chamados da forma correta, falham
  - Controla e inspeciona as chamadas para essa falsa dependência:
    - quais argumentos foram passados
    - quantas vezes o método foi chamado
  - Quando usar:
    - Para testar se um método de uma dependência externa foi chamado corretamente, quantas vezes e com quais parâmetros
  - Quando não usar:
    - Para testar o retorno de funções
    - Para testar o comportamento de funções
- Spy:
  - É uma combinação entre mock e stub, ou seja, permite testar interações de chegada e de entrada
  - Grava as chamadas para o método espionado
  - Quando utilizar:
    - Armazenar as chamadas para o método espionado e controlar o que ele retorna
  - Espia a implementação real
  - Registram informações com base em como foram chamados
  - Diferentemente do mock, o spy sempre chama a implementação real, a não ser que substituímos o que deve retornar
- Stubs:
  - Simulam interações de chegada de alguma dependência externa com o SUT
  - São objetos com respostas prontas
  - Não sabem quantas vezes um método de uma dependência foi chamado, com quais parâmetros
  - Quando utilizar:
    - Testar retornos de uma dependência externa
    - Testar o comportamento do SUT com as diferentes respostas da dependência externa
  - Semelhante aos spies e fakes
  - Altera seu comportamento com base na maneira como foi chamado
- Dummies:
  - São dados que substituem dados reais, mas não são utilizados
  - Servem para satisfazer parâmetros