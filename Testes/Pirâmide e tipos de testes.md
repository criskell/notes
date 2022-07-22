# Pirâmide de testes

- Auxilia no TDD
- Consiste em camadas:
  - UI: Testes de interface/aceitação
  - Serviços: Testes de integração + teste de sanidade
  - Unidade: Base da pirâmide
- Funcionamento:
  - Se os testes de unidades passarem, devemos criar testes de integrações entre components
  - Se as integrações passarem, testamos um sistema como um todo com testes de aceitação
  - Se algum teste falhar numa camada, todas as camadas acima não precisam ser executadas
- Os testes de unidades devem estar em maior número e formar a base da pirâmide

## Tipos de testes

- Teste de aceitação:
  - Verifica se todo o projeto funciona como um todo
  - Testar os componentes numa UI
- Testes de integração:
  - Componentes são combinados e testados coletivamente
  - Antes dos testes de aceitação e depois dos testes unitários
- Testes de sanidade:
  - Se a aplicação está respondendo ou não.
- Testes de unidade:
  - Testa a menor parte testável chamada de unidade (geralmente um método)
  - Testa a unidade isoladamente de outras dependências geralmente através de simulações destas
  - Devem serem independentes de outros testes e executarem rápidos