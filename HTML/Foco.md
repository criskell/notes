# Foco

## Atributo tabindex

- `tabindex`: posição de um elemento na navegação sequencial via teclado (por ex.: tab)
- Usos:
  - Alterar quais elementos são e não são focalizáveis
  - Alterar a ordem em que os elementos focalizáveis são navegados

- Valores:
  - `-1`:
    - não pode ser acessado via tab
    - é possível o foco programático via JS
  - `0`:
    - O elemento pode ser focalizado após elementos com `tabindex > 0`, através do teclado ou de forma programática
    - A ordem é a ordem de origem do documento
  - `x > 0`:
    - O elemento pode ser focalizado, através do teclado ou de forma programática
    - A ordem é definida por `x`, de forma crescente
    - Se vários tiverem o mesmo `x`, a ordem é pelo DOM
    - não é recomendado utilizar
- Valor padrão:
  - Alguns elementos são focalizáveis por padrão e recebem `0`
  - O resto recebe `-1`
- Boas práticas:
  - É interativo, faz parte da navegação e deve ser focável?

## Elemento focalizável

- Deve ter um `tabindex` (ou ser focalizável via teclado por padrão)
- Estar renderizado
- Não ser inerte
- Não estar desabilitado