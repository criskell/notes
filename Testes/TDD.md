# TDD

- Desenvolvimento orientado a testes
- Testes antes do código
- Influenciado pelo movimento ágil
- Os testes unitários são a base do TDD, pois são rápidos e devem ser de maior número
- Consiste num ciclo:
  - Red:
     - Crie testes que testa um código ainda não implementado.
  - Green:
    - Implemente o código da maneira mais simples possível
  - Refactor:
    - Eliminar códigos redudantes
    - Deixar o código mais legível e manutenível
    - Remover acoplamentos
- Vantagens do TDD:
  - Reduzir o tempo em bugs
    - Possibilidade de reproduzir o erro sem executar a aplicação.
  - Diminuição de código desnecessário
    - Fazer o suficiente para os testes passarem.
  - Auxiliar testes de regressão
    - Reduz os efeitos colaterais de alterações no código, pois um teste irá falhar se você corrigir um bug e quebrar outro pedaço do sistema
  - Documentação
  - Qualidade
  - Refatoração

## Dicas

- Legibilidade nos testes
- Responsabilidade única nos testes
- Siga o ciclo
- Evitar acoplamento em testes
- Testar uma coisa por vez