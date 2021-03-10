# PGWebLibTest 

## 1. Descrição

Este programa é uma demonstração bem reduzida da integração com a PGWebLib em linux.
Trata-se de um console de testes que permite testar a interface da biblioteca, além de implementar fluxos básicos de transações.

## 2. Compilação

A aplicação é compilada a partir de makefile e tem quatro configurações diferentes:

- Release
- Release64
- Debug
- Debug64

Para buildar o projeto, basta executar no terminal:
> $ make <configuração>

## 3. Operação

Para executar a aplicação, basta rodar o executável compilado em uma pasta que contenha a PGWebLib.so.

Destaca-se que ambos os aplicativos devem ser compatíveis para que seja possível a execução (por exemplo, ambos compilados como 64 bits).
Além disso, a biblioteca necessita que esteja instalado open ssl, versão 1.1.1 para o correto funcionamento. Para conferir a versão no seu sistema, basta executar no terminal:

> $ openssl version

![imagem openssl](./Imagens/openssl.PNG)

Para executar o aplicativo, basta executá-lo pelo terminal da pasta onde o executável se encontra:

> $ ./PGWebLibTest.exe

Assim que executado, é exibido uma tela com todas as funções disponíveis:

![imagem  Init](./Imagens/Operacoes.PNG )

Seguindo o fluxo da dll, primeiro deve-se chamar PW_iInit, informando um diretório que a aplicação tenha permissões para leitura/escrita.

Após isso, é necessário efetuar uma operação de instalação para habilitar o ponto de captura para transacionar com o Pay&Go Web. Para efetuá-la, pode-se selecionar a operação:
> x - Teste de instalacao

Após isso, o ponto de captura está habilitado para efetuar as demais operações. Estas podem ser efetuadas pelas funções que abstraem os fluxos: 


![imagem  abstração](./Imagens/abstracoes.PNG )


Ou chamando as funções da API da biblioteca diretamente:

![imagem  API](./Imagens/API.PNG )

Para detalhamento do fluxos de operação, consultar o documento:

[Especificação de integração](./Especificacaov124.pdf)

## 4. Considerações adicionais

Caso sua ide apresente os fontes com caracteres ilegíveis, trocar o formato de exibição para ANSI/Windows 1252
