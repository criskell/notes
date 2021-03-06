# Pirâmide de testes

- A pirâmide de testes fornece uma orientação sobre como deve ser a estruturação do teste numa aplicação.
- Consiste em camadas:
  - UI: Testes de interface/aceitação
  - Serviços: Testes de integração + teste de sanidade
  - Unidade: Base da pirâmide
- Funcionamento:
  - Se os testes de unidades passarem, devemos criar testes de integrações entre components
  - Se as integrações passarem, testamos um sistema como um todo com testes de aceitação
  - Se algum teste falhar numa camada, todas as camadas acima não precisam ser executadas
- Os testes de unidades devem estar em maior número e formar a base da pirâmide

## Níveis de teste

- Teste de aceitação:
  - Verifica se todo o projeto funciona como um todo
  - Testar os componentes numa UI
- Teste de ponta a ponta:
  - Verificam se o sistema atende com requisitos.
  - Testa uma ponta à outra.
- Testes de integração:
  - Componentes são combinados e testados coletivamente
  - Antes dos testes de aceitação e depois dos testes unitários
  - Testar uma funcionalidade conjunta
- Testes de sanidade:
  - Se a aplicação está respondendo ou não.
- Testes de unidade:
  - Testa uma parte específica do sistema
  - Testa a unidade isoladamente de outras dependências, geralmente através de simulações destas
  - Devem serem independentes de outros testes e executarem rápidos