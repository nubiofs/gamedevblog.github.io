---
layout: post
title: SpaceShip 4042 - meu primeiro jogo para celular!
---

![SpaceShip 4042](http://gamedeveloper.com.br/blog/wp-content/uploads/2009/10/splash01.png "SpaceShip 4042")Este é o primeiro jogo que fiz para celulares, e também foi o primeiro projeto que terminei tudo o que eu planejava fazer. Fiz este jogo para a matéria de Jogos para Celular na pós-graduação utilizando **Java Mobile** (JME com CLDC 1.1/MIDP 2.0) e o [Netbeans 6.7.1](http://www.netbeans.org/downloads/index.html "Netbeans").

Como eu conheço Java, não tive problemas com a programação. A principal dificuldade inicial era entender como um jogo funciona em um celular, entender suas limitações e arquitetura. Por ser bem limitado, deve-se ter muita paciência e cuidado na programação para celular, para que o código não exija muito processamento e também para que as imagens fiquem “leves”.

**O Netbeans ajudou muito no desenvolvimento do jogo**, pois ele possui um tipo de arquivo chamado GameDesign, onde você importa imagens e cria sprites, cenários e cenas. Eu utilizei apenas para criar sprites do jogo, não precisei utilizar cenários e cenas.

Este projeto levou cerca de 2 meses para ficar pronto, porém não foram 2 meses de trabalho diário, eu programava um pouco por semana. Tive ajuda do David Felicino com as imagens das naves, tela de abertura, fundo do jogo e itens. Obrigado!

### <span style="color: #ff0000;">[**Clique aqui para baixar este jogo!**](http://www.gamedeveloper.com.br/cicanci/games/SpaceShip4042_20091012.zip "SpaceShip 4042")</span><span style="color: #ff0000;">**  
**</span>

**O objetivo do jogo é simples**: permanecer o maior tempo possível e pontuar destruindo os meteoros ou desviando deles. O jogo acaba quando os 3 pontos de vida da nave chegarem ao fim, devido a colisões com os meteoros. Os meteoros também têm 3 pontos de vida.

Existem dois itens: um para ganhar 1 ponto de vida e outro para transformar a nave em “nível 2”. Neste nível 2, o jogo dobra a velocidade e os meteoros são destruídos com apenas um tiro. Se for atingido pelo meteoro, neste modo, o jogador não perde vida, apenas o item e volta a ficar com a nave “nível 1”. A velocidade do jogo também dobra se acontecer uma determinada situação.

A maior pontuação do jogar é sempre armazenada e pode ser vista através do meu “High Score”. Existe também uma opção para ver os controles e os créditos. O menu foi legal de fazer, pois o JME não dá suporte para menus apenas com imagens, então criei o menu com sprites que são trocados ou selecionados através dos botões “para cima” e “para baixo” do celular.

Além dos controles tradicionais (direcionais e botão central do celular), **existe um suporte a eventos de toque na tela** (apenas o jogo, o menu ainda não). O video abaixo é uma demonstração no meu celular, um Samsung Star S5230:

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/oikX6uWwwxs?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

O jogo também possui uma verificação para **talvez **funcionar em um maior número de celulares sem precisar ser portado. A verificação é a seguinte: se a resolução da largura (width) da tela do jogo for inferior a 240, são desabilitados o som e a imagem de fundo e a imagem de abertura e os meteoros são imagens com um tamanho menor.

Este vídeo demonstra o jogo no emulador do Netbeans, em uma tela de 240 x 320:

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/4Il01HFR_Ts?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Este vídeo demonstra o jogo no emulador do Netbeans, em uma tela de 176 x 220:

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/5zd-GqKcj3U?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

No segundo vídeo é possível ver tudo que foi reduzido da versão normal (primeiro vídeo) . É claro que é ambição demais querer que este jogo realmente funcione em vários celulares diferentes, mas pelo menos tentei fazer com que isto seja possível de alguma forma.

Este jogo funcionou nos seguintes celulares: Samsung Star S5230, Motorola A1200, Motorola V9, Sony Ericsson W380 (reduzido) e Sony Ericsson K550i (reduzido). Não consegui instalar no Motorola V3, ocorre um erro após transferir por bluetooth.

Existem alguns bugs que estou corrigindo e muitas coisas para polir, mas o jogo já está em sua primeira versão jogável. O principal problema é que, as vezes, ao entrar no jogo pela primeira vez em celulares mais simples, aparece uma tela branca. Neste caso basta voltar para o menu e entrar novamente, porém isto não ocorre sempre. Estou trabalhando nesta e em outras coisas para deixar este jogo o mais perfeito possível.

Desenvolver este jogo foi muito interessante, pois aprendi bastante sobre a arquitetura de um celular, programação com JME, algumas técnicas para diminuir o consumo do processamento, aplicação de design patterns no Java, gravar e ler informações no celular, e, principalmente, alguns dos vários problemas que podem acontecer ao testar o jogo fora do simulador.

Espero que gostem do jogo, este é o primeiro de muitos que pretendo fazer! Comentários são bem-vindos, principalmente se forem sobre bugs! Até mais!
