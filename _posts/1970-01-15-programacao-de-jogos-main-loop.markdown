---
layout: post
title: 'Programação de jogos: main loop'
date: 1970-01-15 13:04:46.000000000 -03:00
---

Antes de começar a estudar desenvolvimentos de games ano passado eu não imaginava o que realmente era um jogo, do ponto de vista da programação. Quem está acostumado com a estrutura de um sistema, não consegue imaginar muito bem que tipo de programa é um jogo sem estudar sua estrutura básica.

Basicamente, **um jogo é um programa em *loop *infinito**. Fiquei surpreso nas primeiras aulas da pós-graduação quando percebi isso. Independente do tipo do jogo, todos têm isso em comum, chamado de *Main Loop* ou *Game Loop*, que é responsável por controlar tudo no jogo.

<figure class="wp-caption aligncenter" id="attachment_413" style="width: 422px">[![Game Loop](http://gamedeveloper.com.br/blog/wp-content/uploads/2010/03/2005-07-21-gameloop.gif "Game Loop")](http://www.ronkes.nl/blog/?2005-07-21-gameengine)<figcaption class="wp-caption-text">Fonte: http://www.ronkes.nl/blog/?2005-07-21-gameengine</figcaption></figure>A principal responsabilidade do Main Loop é receber entradas, atualizar o status do jogo e produzir saídas correspondentes, tudo isso em um ciclo contínuo, praticamente infinito. Neste ponto existe uma diferença entre o Main Loop de um jogo de PC e um jogo de console: no PC o Main Loop é finalizado quando o jogar fecha o jogo; em alguns Consoles o Main Loop é praticamente infinito, pois não existe um “sair do jogo”; em Consoles como o Nintendo Wii, é possível sair do jogo e voltar para a tela inicial do Wii, finalizando o Main Loop do jogo.

Outra responsabilidade do Main Loop, que muitos iniciantes esquecem, é o ***Frame Rate***. A taxa de quadros por segundo em que o jogo roda é importante por que sem este tipo de controle o jogo não fica sincronizado. Em alguns casos, o Frame Rate é escondido do programador e utiliza um valor default, como no XNA. Em outros, ele é obrigatório para o jogo rodar, como na SDL.

O Frame Rate pode ser definido com um número que o programa deve esperar até executar o Main Loop novamente. Porém, não é simplesmente fazendo isso que o programa irá executar aquele mesmo rate sempre. Dependendo do consumo de processamento e memória, um loop pode ser mais lento do que outro, e utilizando um número fixo, o rate sempre será diferente, provocando lags para o jogador.

Uma solução para este problema é descontar do Frame Rate o tempo em o Main Loop gastou em sua execução, assim, o jogo rodará sempre no mesmo frame. Por exemplo: se o Frame Rate é 30, e o Main Loop gastou 3, o programa deve aguardar 27 (30 – 3) para executar novamente o Main Loop. Sem este controle, o programa iria aguardar 33 (30 + 3) para ser executado novamente, lembrando que o tempo do Main Loop pode variar sempre e o Frame Rate é uma constante. O diagrama abaixo ilustra o funcionamento do Main Loop Fixed Rate:

<figure class="wp-caption aligncenter" id="attachment_416" style="width: 506px">![Main Loop Fixed Rate](http://gamedeveloper.com.br/blog/wp-content/uploads/2010/03/main_loop_fixed_rate.gif "Main Loop Fixed Rate")<figcaption class="wp-caption-text">Fixed Rate - Fonte: NAKAMURA, Ricardo. Técnicas de Programação de Games.</figcaption></figure>O que escrevi neste post é algo que considero bem básico para a programação de um game, e acho que pode ser **muito útil para iniciantes**. Apesar de ser básico, a partir disso é possível procurar mais informações na internet, ou perguntar aqui mesmo qualquer dúvida sobre o assunto.


