---
layout: post
title: Programando PONG com HTML5 e Javascript
date: 1970-01-16 19:31:31.000000000 -03:00
---

Esta é mais uma série de posts nova no blog para ser um complemento da “Como ser um programador de jogos”. Lá eu escrevo sobre vários aspectos, muitos teóricos, sobre a formação e aprendizagem para se tornar um programador de jogos. Aqui vou mostrar programação de jogos, mas sempre com o jogo PONG.

Por que sempre o PONG? A ideia é mostrar desenvolvimento de jogos com diversas tecnologias e em várias plataformas, por isso sempre irei mostrar como programar o mesmo jogo, assim ficará mais clara a complexidade de uma determinada tecnologia em relação a outra. Outro motivo também é que o PONG é um jogo relativamente simples de programar, e todo mundo conhece!

Neste primeiro post vou mostrar como programar o PONG utilizando o canvas do HTML5 e código em Javascript. Todo o código comentado (que não é muito grande) está disponível no link no final do post. Aqui vou destacar apenas algumas partes mais importantes em relação ao canvas do HTML5 e algumas partes mais complexas do Javascript. Na conclusão deste post irei falar minha opinião sobre usar esta tecnologia para desenvolver jogos.


# Introdução

O HTML5 surgiu há alguns anos com a proposta de adicionar mais interatividade à páginas web, querendo inclusive substituir o Flash como recurso multimedia. O HTML5 é um padrão que ainda está sendo implementado pelos navegadores, então alguns recursos podem ter funcionamento diferente em cada navegador, mas o básico já tem em todos.

Existem muitas bibliotecas javascript para desenvolver jogos, aplicativos e sites com HTML5 em javascript, mas neste post vou mostrar como fazer um PONG apenas utilizando recursos do HTML5 e Javascript “puro”, sem nada externo.

Para desenvolver com HTML5 e Javascript você precisa apenas de um aplicativo de bloco de notas e navegadores. Eu recomendo o [Sublime Text 2](http://www.sublimetext.com/2 "Sublime") para programar (tem versões para Windows e MacOSX) e pelo menos alguns navegadores mais usados para testar (Internet Explorer, Chrome, Firefox, Safari e Opera). Não precisa ter todos, mas pelo menos mais de um é recomendado.


# PONG

![](http://gamedeveloper.com.br/blog/wp-content/uploads/2013/08/Screen-Shot-2013-08-21-at-10.51.33.png "PONG")

O código do jogo é bem simples, para começar precisamos definir o nosso canvas do HTML5. O tamanho está definido para termos uma área fixa, assim fica mais fácil fazer este exemplo, caso contrário o código ficaria bem mais complexo para fazer o jogo ser adaptável a qualquer tamanho.

<canvas id="canvas" width="600" height="480"></canvas>

Com isso já podemos começar a brincar com o Javascript. Não vou adicionar todo o código aqui, como a inicialização das variáveis, mas você poderá ver o código completo no link no final do post. Uma parte importante da inicialização é adicionar os eventos para receber uma notificação quando uma tecla for pressionada e quando for solta. Este exemplo é baseado nas teclados de seta pra cima e para baixo do teclado. Outro evento importante é o setInterval, que executará uma função de game loop a cada 30 frames.

document.addEventListener('keyup', keyUp, false); document.addEventListener('keydown', keyDown, false); setInterval(gameLoop, 30);

Existem três partes principais no game loop relacionados a lógica do jogo: Jogador, Oponente e a Bola. Vamos primeiro ao jogador, que é mais simples, ele se move com o movimento das teclas.

if (jogadorParaCima) { if (jogadorPosY > 0) { jogadorPosY -= velocidadeJogador; } } else { if (jogadorPosY < (canvas.height - barraHeight)) { jogadorPosY += velocidadeJogador; } }

O comportamento do oponente é praticamente o mesmo, a única diferença é que o seu movimento é constante, e não depende das teclas pressionadas para se deslocar para cima e para baixo, respeitando os limites da tela.

if (oponenteParaCima) { oponentePosY -= velocidadeOponente; if (oponentePosY = canvas.height - barraHeight) { oponenteParaCima = true; } }

Por fim temos a bola, que é um pouco mais complexa pois existe a verificação da colisão dos jogadores com ela, e isso faz seu deslocamento ser invertido. Este código é maior, porém suas verificações são simples para determinar se alguém encostou na bola. Se a posição da bola estiver contida na posição do jogar, a movimentação da bola é invertida, e também é aplicada uma transformação matemática aleatória para que o seu angulo ao ser rebatida seja variado.

if ((bolaPosX - 10) jogadorPosY) && (bolaPosY - 10 < jogadorPosY + barraHeight)) { bolaParaDireita = true; if (jogadorParaCima) { bolaAngulo = Math.floor(Math.random() * 10) - 9; } else { bolaAngulo = Math.floor((Math.random() * 10)); } } } else if ((bolaPosX - 10) > (oponentePosX - barraWidth)) { if ((bolaPosY + 10 > oponentePosY) && (bolaPosY - 10 < oponentePosY + barraHeight)) { bolaParaDireita = false; if (oponenteParaCima) { bolaAngulo = Math.floor(Math.random() * 10) - 9; } else { bolaAngulo = Math.floor((Math.random() * 10)); } } } if ((bolaPosY - 10 canvas.height)) { bolaAngulo = bolaAngulo * -1; } bolaPosY += bolaAngulo; if (bolaParaDireita) { bolaPosX += velocidadeBola; } else { bolaPosX -= velocidadeBola; }

A lógica do PONG é bem simples, e será sempre parecida em todos os posts desta série, sendo a única diferença a tecnologia utilizada. Outro detalhe importante neste post é que não existem imagens para os jogadores e a bolinha, tudo foi desenhado no próprio código Javascript utilizando recursos do canvas do HTML5, como demonstrado abaixo.

`// Jogador e Oponente 
context.fillRect(jogadorPosX, jogadorPosY, barraWidth, barraHeight); context.fillRect(oponentePosX, oponentePosY, barraWidth, barraHeight); 
// Bola 
context.beginPath(); 
context.arc(bolaPosX, bolaPosY, bolaDiametro, 0, Math.PI * 2, true); context.closePath(); 
context.fill();`

Por fim, temos mais pedaços de código responsáveis por exibir o placar, desenhar as linhas e os jogadores, contar a pontuação (basicamente é só verificar se a posição da bolinha está fora do canvas), entre outros detalhes que estão comentados no código completo no link abaixo.

[Clique aqui para baixar o código completo!](https://github.com/GameDevBlog/game-html5-pong "PONG")

Conclusão

Pode parecer que a única novidade é a marcação <canvas>, mas por trás disso o HTML5 implementa muitas melhorias de desempenho e gráficas, além de definir melhor o padrão para desenvolvimento web. Existem bibliotecas que podem reduzir muito o código aqui mostrado, mas a ideia era mostrar como fazer apensa utilizando o que já está disponível por padrão nos navegadores.

A vantagem de fazer exemplos e testes com os recursos do HTML5 é que você acaba aprendendo mais do que usando direto uma biblioteca, que vai ocultar muitas dessas coisas para simplificar o seu trabalho.

Outra vantagem é que, por ser HTML, você pode rodar isso em qualquer coisa que tenha um navegador (PC, celulares, tablets, video games, etc). Existem muitos aplicativos mobile que são, na verdade, uma “casca” com um código que executa um HTML dentro do aplicativo.

Espero que tenham gostado! Estou ansioso para o próximo post desta série!


