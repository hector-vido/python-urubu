---
title: Urubu
layout: page
content:
    - jenkins
    - python
    - mais
---

Urubu é um micro CMS de arquivos estáticos.
{.lead}

Isso significa...
=================

Isso significa nada de banco de dados ou configurações complexas, 
direto do git para o servidor!

Tudo o que precisamos é criar nossos arquivos `.md` e rodar o comando
`make` para que sejam convertidos para arquivos `.html`.

Isso é perfeito para você criar o seu próprio blog em python!

Arquivos de conteúdo
====================

Todos os arquivos de conteúdo começam com uma sesssão delimitada por três traços `---`
onde definimos o `title` e o `layout`.

Esta página por exemplo, começa assim:

```yml
---
title: Urubu
layout: page
content:
    - jenkins
    - python
    - mais
---
```

Depois disso basta escrever em markdown.

Layouts
=======

Todos os arquivos de conteúdo utilizam a variável `layout` para especificar o
desenho da página.

Existem alguns exemplos no diretório `_layout`, mas aqui vamos utilizar apenas
aquele chamado `page`.
