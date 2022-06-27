# Hiperlink

- *Hyperlinks* permitem vincular documentos à outros documentos ou recursos, vídeos, áudio e etc.
- É uma característica essencial da *web*.

## Anatomia de um hiperlink

- O conteúdo do hyperlink deve ser envolvido por um elemento `a` com os atributos:
  - `title`: Informações adicionais do hyperlink.
  - `href`:
    - Referência para hipertexto. É o destino do link.
    - Se o navegador não conseguir abrir o arquivo, tentará baixar ele.

## URLs

- URLs são strings que especifica como um recurso pode ser acessado
- O caminho é utilizado na URL para localizar um arquivo no sistema de arquivos
- Estrutura de diretórios:
  - **Raiz** é onde tudo reside.
- Tipos:
  - Absoluta:
    - Aponta para um recurso definido por sua posição absoluta
  - Relativo:
    - Aponta para um recurso relativo ao próprio documento que está vinculando

## Fragmentos de documentos

- São partes do documento em que vinculamos via um hiperlink.
- Para criar um, adicionamos um identificador e referenciamos na URL via `#`.

## Boas práticas

- Utilizar um texto claro, curto e acessível, por exemplo: `Baixe o TS` ao invés de `Clique aqui` pois:
  - SEO: Palavra-chave
  - Acessibilidade:
    - Leitores de telam pulam de link em link, sem ler o contexto do link
  - Os links destacados são atraídos pelos usuários
- Não colocar a URL no próprio texto do link
- Não dizer "link para" no texto do link
- Não criar links para outros lugares com o mesmo texto
- Indicar que está vinculando um recurso que não é HTML e adicionar palavras-chaves para reduzir confusões. Por exemplo: "Abrir documento Word (PDF, 10mb)"
- Utilizar o atributo `download` quando estiver vinculando arquivos que devem ser baixados

## Emails

- URLs com o esquema `mailto`.
- Exemplos:
  - `mailto:[endereco][?[cc=...]&[subject=...]]`

## Landing pages

- Páginas que são o ponto de entrada de um site ou seção de um site.

## Links para download

- Atributo `download`
- Indica o nome do arquivo ao salvar

## Exercícios

1. O que são hyperlinks e como representar no HTML
2. O que são URLs e caminhos. Quais os tipos de URLs
3. 5 boas práticas para criar links
4. O que são landing pages
5. O que são fragmentos
6. Quais são os atributos de links
7. Por que links são importantes