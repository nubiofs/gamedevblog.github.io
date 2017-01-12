---
layout: post
title: Monetização de jogos e aplicativos com RevMob
date: 1970-01-16 22:19:55.000000000 -03:00
---

A RevMob é uma empresa brasileira que trabalha com publicidade de jogos, aplicativos e sites em dispositivos móveis. Conheça os tipos de anúncios que você pode colocar em seu jogo e quais são as boas práticas para monetizar sem irritar o jogador.

Eu trabalho na [RevMob](http://www.revmobmobileadnetwork.com/ "RevMob") há alguns meses como Engenheiro de Software, entrei nesta empresa algum tempo depois que o estúdio da Electronic Arts fechou no Brasil. Atualmente sou o líder da equipe responsável pelo desenvolvimento dos SDKs que permitem os desenvolvedores integrarem o sistema de anúncios da RevMob em seus jogos e aplicativos.

Por trabalhar na parte técnica, vou focar este post em mostrar os diferentes tipos de anúncios e onde são os lugares mais indicados para usar. Para conhecer mais sobre a empresa e como funciona, acesso o site da [RevMob](http://www.revmobmobileadnetwork.com/ "RevMob"). Acesse também o [site do SDK](http://sdk.revmobmobileadnetwork.com/ "RevMob") e veja as opções disponíveis, como: iOS, Android, Corona, Unity, Adobe Air, PhoneGap, Titanium, Cocos2d-x, entre outros.


## Fullscreen

![](http://gamedeveloper.com.br/blog/wp-content/uploads/2013/12/fullscreen_ios.png "Fullscreen")

Este é o tipo de anúncio mais usado, e também o que possui maior retorno para o desenvolvedor, pois é um anúncio de tela cheia exibido por cima da tela do jogo. Porém, este também é o anúncio que mais irrita os jogadores quando usado em excesso. No jogo Combo Nuts que desenvolvi com a Aplay Studios tivemos muita reclamação em relação a frequência desde tipo de anúncio, e acabamos reduzindo no primeiro update do jogo.

O ideal é mostrar em momentos que o jogador não está imerso no gameplay. Muitos desenvolvedores exibem este anúncio quando o jogador chega na tela de menu principal, e sempre exibem caso ele volte para esta tela. Isto foi o que fizemos no Combo Nuts e irritou os jogadores, então reduzimos para mostrar apenas na primeira vez que o jogo é carregado, e não enquanto o jogador estiver navegando nos menus.

O melhor lugar para colocar, e que muitos jogos usam, é entre as partidas. Geralmente, todo jogo tem um momento em que o jogador morre ou termina uma fase, e neste momento de transição é um bom lugar que não irrita tanto o jogador. Claro que se você colocar em todas as transições, isso vai irritá-lo do mesmo jeito, por isso eu recomendo um contador para exibir o anúncios a cada 3 ou 5 partidas.


## Banner

![](../content/images/2013/12/banner_ios.png "Banner")

O banner já foi muito usado, porém hoje em dia não está sendo uma opção muito usada pelos desenvolvedores. Seu principal problema é que o desenvolvedor deve reservar uma área no jogo para exibir o banner, e isso implica em mudanças no layout e redução do espaço do jogo para mostrar uma propaganda. Por ficar o tempo todo presente, o seu retorno pode até ser bom, dependendo do local.

No jogo Scrabble, meu último projeto na EA, o banner era exibido apenas no menu principal e em algumas telas de configuração e informação, sempre na parte inferior da tela. Eu acredito que foi uma boa escolha, por não acho legal ser exibido durante o gameplay, como é o caso do Angry Birds, que exibe um banner na parte de cima da tela durante o jogo, e isto pode irritar por atrapalhar a visão do jogo.

Assim como no caso do fullscreen, e em qualquer outro tipo de anúncio, deve ser colocado nos lugares corretos e evitar o uso durante o gameplay.


## Link

O link é muito versátil, pois permite o desenvolvedor criar seu próprio anúncios e chamar uma URL para um anúncio real. Um exemplo de uso são botões adicionados na tela de menu do jogo com textos “Get More Games” ou algo semelhante que, ao ser tocado, leva o jogador a ao anúncios, que geralmente é um jogo.

Isto não irrita o jogador, pois se ele tocar neste botão é por que realmente quer saber o que é esta opção. Porém, isto irritará o jogador se usado para enganá-lo, iludindo-o com algum texto que o leve a acreditar que esta opção dará algo para ele relacionado ao jogo.


## PopUp

[![](../content/images/2013/12/popup_ios.png "PopUp")](../content/images/2013/12/popup_ios.png)

Esta opção pode ser menos irritante que o fullscreen para o jogador, e pode dar mais resultados que o banner e o link também. Ela consiste em exibir uma janela perguntando para o jogador se ele deseja baixar um jogo gratis, ou algo assim, e ele tem a opção de escolher sim ou não. Também deve ser usada com cautela, pois é muito fácil o jogador confundir este popup com uma mensagem do próprio jogo, e isso pode fazer ele entrar sem querer no anúncio.

Os melhores locais para exibir este anúncio são bem parecidos com os indicados para o fullscreen, mas sempre com pouca frequência.


## Conclusão

É muito fácil irritar um jogador com anúncios, por isso devem ser usados sempre com cautela. Outro coisa que deve ser evitada é usar todos os tipos de anúncios ao mesmo tempo, isso pode ser visto como spam pelo jogador. Um dos principais motivos que faz um jogador ficar irritado e até desinstalar um jogo é quando eles percebem a ganância do desenvolvedor em colocar muitos anúncios. Por isso, use o bom senso quando for adicionar anúncios. Quando colocados nos lugares corretos, e em uma frequência adequada, o resultado é melhor do que exibir o tempo todo.

Lembre-se também de fazer uma versão do jogo paga sem anúncios, ou dar uma opção para o jogador comprar algum item e remover os anúncios do jogo, isso funciona na maioria das vezes quando o jogador gosta do jogo. Existem outras empresas que fazem este mesmo trabalho que a [RevMob](http://www.revmobmobileadnetwork.com/ "RevMob"), oferecer SDKs para integração do seu serviço em jogos mobile, como a [Admob](http://www.google.com/ads/admob/ "Admob") e a [Chartboost](https://www.chartboost.com/ "Chartboost").


