---
layout: post
title: 'Final Frontier: Algumas mudanças no projeto'
tags:
- final-frontier
cover: content/images/2016/12/capa-ff-camera-big.jpg
---

Faz um mês que não escrevo sobre o andamento deste projeto por que ele está parado no momento, mas por alguns bons motivos. Agora está mais claro pra mim onde quero chegar com este projeto, e também como quero fazer isso.

**O novo rumo do projeto**

No [primeiro post](http://gamedeveloper.com.br/inicio-do-projeto-final-frontier/) sobre este projeto eu falei de algumas referências que tinha para este projeto, e também que não sabia ao certo o que este jogo seria. Agora as coisas estão mais clara pra mim, e agora vou começar a escrever um [GDD](https://github.com/cicanci/game-unity-ff/wiki/GDD) com tudo que planejo fazer para uma primeira versão e organizar as [tarefas](https://github.com/cicanci/game-unity-ff/projects/1?fullscreen=true).

Encontrei uma referência que é o gameplay que tenho em mente para este jogo, o [Galaxy On Fire 3 - Manticore](http://www.gof3manticore.com/release/) (vídeo abaixo). Os controles em um dispositivo móvel são muito bons, e o gameplay tem muitos elementos que eu quero colocar no meu jogo. Provavelmente esta será minha maior referência para o gameplay, assim como o [Destiny](https://www.destinythegame.com/) é para a interface do jogo. Pretendo fazer este jogo com as plataformas mobile e desktop em mente, então os controles precisam ser bons em qualquer lugar.

<iframe width="560" height="315" src="https://www.youtube.com/embed/xdTP3zVbLog" frameborder="0" allowfullscreen></iframe>

**O desenvolvimento na Unity**

Agora que eu tenho uma noção melhor do que o jogo será, não faz muito sentindo continuar com a ideia de descobrir uma mecânica em um playground. Por isso boa parte dos scripts de teste serão removidos do projeto, e tudo será refeito como um protótipo. Neste caso, não será um protótipo totalmente com um código que pode ser jogado fora, pois muitas coisas podem ser feitas de uma maneira melhor para agilizar a implementação do jogo na Unity (como utilizar prefabs sempre que possível).

O protótipo será algo jogável e próximo de um jogo final, porém provavelmente não terá integrações com backend, redes sociais, multiplayer, e qualquer outra coisa que tire o foco do gameplay single player. A ideia é ter algo que não precise de conexão para ser jogado, e que seja divertido por um bom tempo.

Quero implementar algumas coisas mais avançadas na arquitetura do jogo e explicar como estas coisas funcionam em um projeto Unity. Um exemplo disso é algo chamado dependency injection que foi utilizado no Pokemon Go através do framework [Zenject](https://www.assetstore.unity3d.com/en/#!/content/17758), como pode ser visto na palestra abaixo do Unite deste ano. Outro exemplo é o padrão de troca de mensagens e busca de serviços utilizando o framework [Frictionless](https://github.com/Claytonious/Frictionless), que já está em uso no projeto.

<iframe width="560" height="315" src="https://www.youtube.com/embed/8hru629dkRY" frameborder="0" allowfullscreen></iframe>

**Conclusão**

Este post foi mais um update do projeto e um pouco sobre seu rumo em 2017. Pretendo focar mais em seu desenvolvimento e tentar definir todo trabalho que será realizado para que eu possa ter uma data de término. O que vai acontecer depois eu não faço ideia, mas primeiro preciso chegar lá.

O andamento do projeto pode ser conferido no [GitHub](https://github.com/cicanci/game-unity-ff). Todos os posts desta série sobre meu projeto podem ser vistos na tag [Final Frontier](http://gamedeveloper.com.br/tag/final-frontier/), e como sempre qualquer sugestão ou opinião é bem vinda!
