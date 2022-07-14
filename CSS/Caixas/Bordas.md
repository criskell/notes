# Bordas

- Cada borda de uma caixa irá ter:
  - estilo (estilo do traço)
  - largura (espessura do traço)
  - cor

## Largura

- É a espessura do traço
- O padrão é `medium`
- `border-color` ou da mesma coisa que os estilos

## Estilo

- Especificamos o estilo com a propriedade `border-style`
- Ou `border-top-style`, `border-right-style`, `border-bottom-style`, `border-left-style`
- Para a borda aparecer, devemos especificar um estilo

## Cor

- A cor padrão é `currentColor`
- `border-color` ou da mesma coisa que os estilos

## Shorthand

- `border: largura estilo cor`

## Arredondamento de cantos

- Arredondamos cantos da caixa com `border-radius`
- Sintaxe:
- ```css
border-radius: <todos-os-cantos>;
border-radius: <top-left + bottom-right> <top-right + bottom-left>;
border-radius: <top-left> <bottom-left + top-right> <bottom-right>;
border-radius: <top-left> <top-right> <bottom-right> <bottom-left>;
```
- Podemos especificar cantos específicos com `border-<canto>-radius`
- Cada canto irá admitir 2 valores, um para o raio no sentido horizontal e para o outro no sentido vertical. Na `border-radius` especificamos com `/`.

## Bordas customizadas
- `border-image`