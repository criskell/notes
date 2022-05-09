# Como funciona a Web

## Conceitos básicos

- Conexão de internet: Permite enviar/receber dados.
- TCP/IP: Protocolos que transportam dados.
- DNS: Traduz domínios para IPs.
- HTTP: É o protocolo que cliente e servidor utilizam para se comunicarem.

## Acesso a um site

- Para requisitar um arquivo:
  1. O navegador traduz o domínio para um IP.
  2. Envia um pedido HTTP pro servidor com este IP através da conexão com a internet via TCP/IP.
  3. O servidor envia a resposta, em forma de pacotes de dados.
  4. O navegador junta esses pedaços numa página web.
- Em todo o processo, a comunicação se dá por envio e recebimento de pacotes de dados, com este pacote sendo enviado por várias rotas diferentes.

## Como o navegador carrega o HTML

1. Analisa o HTML e obtém todos os `<link>` de CSS e `<script>`
2. Pede pro servidor os scripts e estilos.
3. Constrói a árvore do DOM e o **CSSOM** do CSS, ao mesmo tempo que executa o JS.
4. A página é pintada na tela.