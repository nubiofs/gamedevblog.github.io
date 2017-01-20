---
layout: post
title: Modelo de desenvolvimento com GIT usando branches
date: 1970-01-17 05:54:04.000000000 -03:00
---

Durante minha carreira já usei muitos controles de versão, mas nos últimos anos o que mais tenho usado é o GIT. Além das suas features que vou comentar neste post, a possibilidade de ter seu repositório na nuvem em sites como Github e Bitbucket sem pagar nada está fazendo cada vez mais programadores escolherem o GIT.

O primeiro controle de versão que utilizei foi o [SVN](http://tortoisesvn.net/ "SVN") quando era estagiário na Level Up! Games. Naquela época achava que o SVN servia apenas para compartilhar o código e ver o histórico das alterações no arquivo, não sentia muita vontade de usar isso em projetos pessoais.

Quando comecei a trabalhar como analista de sistemas e com .Net, utilizei muito o [SourceSafe](http://msdn.microsoft.com/en-US/library/3h0544kx(v=vs.80).aspx "SourceSafe") da Microsoft. Assim como o SVN, ele tinha o conceito de dar checkout em arquivo para trabalhar, e depois dar checkin para subir as alterações no repositório. Eu achava interessante esse conceito de bloquear um arquivo para edição, mas em equipes com mais de 3 pessoas este tipo de recurso era um problema, pois não permitia mais de um programador trabalhar no mesmo arquivo.

Na Electronic Arts eu utilizava o [Perforce](http://www.perforce.com/ "Perforce"), um controle de versão muito bom e com recursos semelhantes ao do [GIT](http://git-scm.com/ "GIT") que permitiam mais de uma pessoa trabalhar no mesmo arquivo sem grandes problema e criar branches para os projetos. Mesmo sendo muito bom, ainda assim não era como o GIT.

Cheguei a usar o SourceSafe no meu TCC da graduação, mas só quando comecei a pós-graduação que eu conheci o GIT. No início foi um grande choque sair de um modelo centralizado em arquivos para um outro onde cada um poderia trabalhar em qualquer arquivo e juntar tudo na hora de publicar no repositório. O uso de branches era bem interessante, mas como não conseguia ver para que poderia usar, sempre mantive as alterações no “master”. Aos poucos fui perdendo o medo de fazer branches e entendendo suas vantagens, mas só agora estou realmente usando tudo que o GIT oferece para os programadores.

[![GIT Model](../content/images/2014/09/git-model@2x-772x1024.png)](../content/images/2014/09/git-model@2x.png)

Um programador russo que trabalhou em um projeto comigo há algum tempo me mandou [este link](http://nvie.com/posts/a-successful-git-branching-model/ "GIT branching model"), que falava sobre um modelo de uso do GIT com branches e me disse que era muito bom. Li o texto e comecei a trabalhar assim, e em pouco tempo comecei a ver as vantagens desse modelo (e realmente usar as features do GIT).

A ideia desse modelo é bem simples: use um branch “develop” para o desenvolvimento e faça as releases no “master”. O grande diferencial do modelo está no desenvolvimento das features, pois cada feature deve ser desenvolvida no seu próprio branch. Este branch, por sua vez, deverá ser aplicado no brach “develop” usando o comando “git merge”. Pode parecer um pouco confuso, mas depois de começar a usar este modelo tudo fica mais claro. Além das features, podemos também ter branches separados para bug fixes, sempre sendo criados a partir do branch “develop”.

Existem muitas vantagens em utilizar um branch por feature, como por exemplo pode voltar a trabalhar em algo ou verificar alguma feature a qualquer hora. Como o merge é feito apenas no final da feature, o risco de ter vários conflitos é bem reduzido, pois você só precisará lidar com isso uma vez ao invés de lidar a cada commit quando utilizamos o mesmo branch “master” para tudo.

O código do projeto fica muito bem organizado, e fica mais fácil de associar uma feature a uma parte do código. Eu, pessoalmente, acho muito mais organizado do que usar tags (apesar de serem úteis para marcar commits). Eu expliquei bem por cima por que eu acho mais interessante ler a explicação completa no site do [Vincent clicando aqui](http://nvie.com/posts/a-successful-git-branching-model/ "Git").

E você, usa o qual repositório em seus projetos? Lembrando que dropbox não conta! rs

Fonte: [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/ "Fonte")


