---
layout: post
title: Revisão de código
date: 1970-01-18 00:01:20.000000000 -03:00
---
Esta é uma prática muito comum em empresas de médio e grande porte, mas na minha opinião poderia ser algo que muitas empresas pequenas deveriam tentar adicionar ao seu processo de desenvolvimento. Existem algumas maneiras formais de fazer revisão de código, mas neste post quero comentar da minha experiência em revisão de código. 

Na primeira vez que conheci este processo na prática foi quando trabalhei na [Electronic Arts](http://ea.com). Em projetos que estão em desenvolvimento existe uma exigência muito grande por parte dos líderes de que todo código seja revisado antes de fazer o merge das alterações para o branch principal do projeto.

Para a revisão funcionar é necessário que a equipe trabalhe com o conceito de branches. Isto pode ser facilmente feito em ferramentas de versionamento como [git](https://git-scm.com/) e [perforce](https://www.perforce.com/) (este é o que a EA usa). Cada feature ou bug fix deve ser feita em um branch separado, e quando terminada o merge é feito para o branch principal de desenvolvimento. É neste ponto que a revisão de código acontece.

A revisão do código, sempre feita por outro programador que não trabalhou no branch, pode ser algo mais leve como só verificar se existe algo que pode ser melhorado ou algo mais exigente, como verificar se o código está escrito no padrão do projeto (nomes de variáveis e métodos, espaçamento, quebras de linha, entre outros). No início, para um programador novo na equipe, é normal que o código necessite alterações, mas com o tempo tudo fica mais natural. Caso o revisor aprove o código, ele pode ser mergeado no branch de desenvolvimento. Caso contrário, o revisor enviará uma lista de alterações e até sugestões para melhorar o código.

Um dos benefícios da revisão de código não é só garantir que os padrões de desenvolvimento do projeto estejam sendo seguidos, mas também ajuda a evitar que novos códigos sejam adicionados em lugares errados ou que algo que já exista seja escrito novamente. A revisão de código ensina o programador a ter mais cuidado com o código que está escrevendo.

É importante lembrar que a revisão do código não é um teste unitário e muito menos gerar uma build e testar. Os testes de código provavelmente serão executados no momento de gerar uma build para algum QA testar ou após o merge do código no branch de desenvolvimento. A revisão do código busca a qualidade do código escrito e o padrão de desenvolvimento do projeto.

Outro ponto para se lembrar é que a revisão de código só funciona se todos programadores da equipe tiverem o bom senso de seguir os padrões do projeto. Não adianta introduzir algo que não será seguido por que alguém acha que é besteira ou perda de tempo, e prefere escrever o código de qualquer jeito só para terminar suas tarefas antes do prazo. Escrever código com qualidade nunca é perda de tempo, e qualquer processo que possa garantir a qualidade do código é útil em projetos com muita gente trabalhando ao mesmo tempo. 

Imagem da capa: [Programmer working](http://www.shutterstock.com/pic-395220502/stock-photo-programmer-working-on-laptop-at-office-focus-on-programming-code.html) do Shutterstock.






