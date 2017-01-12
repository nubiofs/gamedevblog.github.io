---
layout: post
title: 'Como ser um programador de jogos: Delta Time'
date: 1970-01-16 21:22:19.000000000 -03:00
---

Muitas engines e frameworks possuem um controle do tempo de cada game loop internamente, mas expõem esta informação caso você precise. E, acredite, você precisa!

Primeiro, vamos falar de algumas definições. Game loop é looping principal do jogo, aquele método update() que é executado a cada frame, e pode ser internamente ([Cocos2d-x](http://www.cocos2d-x.org/ "Cocos2d-x"), [Corona](http://www.coronalabs.com/ "Corona"), [Unity](http://unity3d.com/ "Unity")) ou você tem que definir ([SDL](http://www.libsdl.org/ "SDL"), [DirectX](http://www.microsoft.com/en-us/download/details.aspx?id=6812 "DirectX")). Cada vez que um frame do jogo é executado, quem executa é o game loop. Assim, se o seu jogo está rodando a 30 frames por segundo, o game loop é executando 30 vezes em um único segundo, por isso é importante que ele seja bem controlado.

A diferença entre o tempo que o game loop inicia e termina sua execução é o nosso Delta Time! Esta diferença, geralmente em segundos ou mili-segundos, é um tempo inconstante que cada frame do jogo leva para ser feito. Basicamente, durante um frame acontecem coisas como verificar o input do jogador, atualizar a lógica do jogo e desenhar na tela tudo que aconteceu. Tudo isso feito várias vezes por segundo! Já da pra imaginar que quando o jogo está lento ou com lag o problema está por aqui, né?

![](http://gamedeveloper.com.br/blog/wp-content/uploads/2013/11/2005-07-21-gameloop.gif "Game loop")

E por que é tão importante o Delta Time? Para controlar os frames por segundo do seu jogo. As engines e frameworks possuem um controle bem básico internamente, mas cabe ao programador estendê-lo para se adequar ao seu jogo. Existem algumas técnicas para controlar o tempo do game loop envolvendo o Delta Time, e a mais usada chama-se Fixed Rate, que consiste em garantir que game loop será executado naquele tempo.

No caso do Fixed Rate, basicamente, temos um valor fixo para cada game loop. Por exemplo, eu quero que cada game loop seja executado em 0,03 segundos (1 segundo / 30 frames), só que o tempo está rápido demais. Neste caso, após a execução do game loop, verificamos se o Delta Time é menor do que 0,03 segundos, e em caso positivo fazemos o game loop “esperar” 0,03 segundos – Delta Time, utilizando recursos como Thread Sleep (isso depende da tecnologia usada). Abaixo um exemplo implementado em C++ no framework SDL, que possui métodos para pegar o número de “ticks” e aguardar um número específico. Neste caso, o SDL não usa segundos, e sim um valor que corresponde ao número de “ticks” por frame.

Uint32 Scene::Wait(Uint32 t0) { Uint32 t1 = SDL_GetTicks(); if ((t1 - t0) < 75) SDL_Delay(75 - (t1 - t0)); return t1; }

Isto funciona se o jogo estiver rápido demais, mas se estiver lento demais? Se estiver muito lento, o jeito é reduzir o número de frames por segundo. Quando trabalhei no [FIFA 12 para Android](http://gamedeveloper.com.br/blog/2013/10/02/vi-uma-pessoa-jogando-um-jogo-que-fiz-na-ea/ "FIFA 12"), na [Electronic Arts](http://www.ea.com "EA"), usamos isso para baixar o FPS (frame por segundo) do jogo em aparelhos com hardware mais fraco, e assim reduzir ou eliminar o lag. Lembrando que reduzir o FPS não deixa o seu jogo lento, ele apenas faz menos updates por segundo, e para o olho humano as coisas só ficam perceptivelmente lentas abaixo de 17 FPS. O vídeo abaixo explica isso, e também diz quais são as diferenças entre 30 e 60 frames por segundo.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/n00qUDL0Cxg?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Para saber mais detalhes sobre o game loop e fixed rate, dêem uma olhada [neste post que fiz faz alguns anos explicando melhor este dois conceitos](http://gamedeveloper.com.br/blog/2010/03/01/programacao-de-jogos-main-loop/ "Game loop"). Como o objetivo deste post é o Delta Time, vou falar um pouco mais sobre outros usos dele. Por exemplo, as vezes você precisa esperar um tempo determinado para uma ação, como esperar 10 segundos para exibir um banner em um jogo mobile. Neste caso, você usa o Delta Time para acumular o tempo passado até que chegue no seu valor desejado. O exemplo abaixo é uma implementação em C# na game engine Unity, e mostra como pegar o Delta Time, acumular e esperar um tempo determinado.

private float mDelay; void Update () { // se passou 10 segundos... if (mDelay > 10.0f) { // faz alguma coisa e zera o contado mDelay = 0; } else { // se não, vai acumulando mDelay += Time.deltaTime; } }

Controlar o game loop e fazer contagem de tempo são duas das principais utilizações do Delta Time em um jogo, e é claro que existem outros. O importante é sempre utilizar este tipo de recurso para estas tarefas, e lembre-se sempre de verificar na tecnologia que você está usando como este controle pode ser feito.

**UPDATE**: Tinha esquecido de adicionar o video, obrigado por avisar Thales!


