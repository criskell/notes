# Estruturação de testes

## AAA

- Todo teste unitário deve seguir o padrão AAA:
  - Arrange: Preparamos o ambiente necessário para o teste, inicializamos variávei, criamos test doubles e etc.
  - Act: Rodamos o teste, colocando o SUT à prova.
  - Assert: Afirmamos o resultado esperado da operação anterior.

## GWT

- Given (dado) pré-condições necessárias para o teste rodar
- When (quando) executo o SUT
- Then (então) pós-condições devem serem atendidas