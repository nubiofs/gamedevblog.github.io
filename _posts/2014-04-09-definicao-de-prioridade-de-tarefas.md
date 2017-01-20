---
layout: post
title: 'Como ser um programador de jogos: Definição de prioridade de tarefas'
date: 1970-01-17 01:04:44.000000000 -03:00
---

Assim como em qualquer projeto, existem tarefas e elas necessitam de prioridade para você saber quais são mais importantes e urgentes. No desenvolvimento de um jogo, muitas vezes as tarefas podem ter dependência com outras áreas, como arte ou som, porém mesmo com dependências podemos definir prioridades nas tarefas.

Podemos olhar para elas pensando exclusivamente na programação, assim você saberá o que deve ser programado primeiro. Por exemplo, não adianta fazer a programação do movimento de um personagem sem antes ter um personagem na tela. Algumas tarefas podem ser difíceis de priorizar, pois muitas podem ter a mesma dependência básica. Por exemplo, com o personagem na tela você pode fazer ele andar, atacar, pular, correr, etc, mas essas tarefas podem não dizer claramente quais são as mais importantes.

Para saber o que é mais importante na hora de programar, devemos olhar para o nosso objetivo. Se queremos fazer o personagem lutar, fazer ele se movimentar é mais importante do que fazer ele interagir com portas, por exemplo. Por isso, muitas vezes as tarefas são derivadas de uma tarefa maior, que na verdade é um requisito do jogo, uma mecânica, uma jogabilidade, uma feature, entre outras coisas. É importante também manter o foco, pois se o objetivo é ver o personagem lutar, não é necessário criar todo o nível nestas tarefa, pois o foco dela é jogabilidade.

A seguir está um exemplo de uma tarefa quebrada em outras menores, e (ordenado por prioridade sempre que possível). Através do exemplo abaixo, podemos ter uma idéia de por que uma tarefa tem mais prioridade do que a outra. Se ajudar, você podem também adicionar números nas tarefas e marcar o nome de qual tarefa é dependente dela, mas isso não é necessário se um objetivo tiver mais ou menos o mesmo tamanho que o exemplo. Se for muito maior do que isso, ele precisa ser quebrado em menores antes de definir as tarefas.

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td valign="top" width="85">**Objetivo**</td><td valign="top" width="567">**Movimentar o personagem através de um controle de touch na tela**</td></tr><tr><td valign="top" width="85">Tarefas</td><td valign="top" width="567">- Desenhar jogador na tela (apenas uma imagem)
- Desenhar botões na tela (cima, baixo, esquerda e direita)
- Capturar o input do jogador nos botões
- Mover o personagem de acordo com o input
- Definir uma velocidade de movimento
- Substituir a imagem do jogador por animações para todas direções
- Alterar a imagem dos botões quando ele for pressionado
- Testar a jogabilidade e refinar até ficar boa e constante

</td></tr></tbody></table>Uma boa dica é utilizar ferramentas como o [Trello](http://trello.com "Trello") para organizar as tarefas. [Este post](http://gamedeveloper.com.br/blog/2014/01/22/gerenciamento-do-seu-tempo/ "Gerenciamento de Tempo") é legal para saber mais sobre o Trello e outras ferramentas e técnicas para organização do tempo, que podem ser úteis na organização das tarefas do projeto.


