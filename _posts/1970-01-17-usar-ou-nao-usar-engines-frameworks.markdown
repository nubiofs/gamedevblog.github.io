---
layout: post
title: Usar ou não usar game engines ou frameworks?
date: 1970-01-17 10:00:19.000000000 -03:00
---

Quando começamos a desenvolver jogos é mais fácil e prático utilizar soluções prontas para desenvolver jogos, porém grandes empresas da indústria de games criam seus próprios frameworks e engines. Mas, hoje em dia, não são apenas as empresas grandes que estão optando por criar suas próprias soluções.

Além das game engines famosas (que inclusive já contam com fanboys para defenderem as tecnologias, muitas vezes sem testarem outras soluções), existem muitas outras que ficam famosas após algum jogo ser lançado e ficar famoso. A mesma coisa acontecem com frameworks. [Neste post da revista Develop](http://www.develop-online.net/tools-and-tech/12-alternative-game-engines/0205547 "Develop") é possível conhecer 12 game engines e frameworks que são alternativas ao invés de utilizar sempre Unity (ou Unreal) nos projetos de jogos.

É muito comum grandes empresas criarem as próprias tecnologias para ter mais controle sobre tudo. Desta maneira engines como a [Frostbite](http://en.wikipedia.org/wiki/Frostbite_(game_engine) "Frostbite") da DICE ficaram famosas e são utilizadas por vários jogos da empresa. Quando trabalhei na EA todos jogos novos estavam sendo desenvolvidos utilizando um framework mobile recém criado internamente, chamado EAMT (Electronic Arts Mobile Technology). Este framework funcionou muito bem, e por ser modular outros frameworks podiam ser facilmente adicionados. A EA tem um departamento só para desenvolver novas tecnologias, chamado EA Tech, o que facilita muito o trabalho dos desenvolvedores.

Porém, não é necessário ter um departamento inteiro para desenvolver sua própria tecnologia. Apesar de atrasar um pouco o desenvolvimento de um jogo, é possível criar sua própria solução e reutilizar em todos projetos do estúdios. Muitos estúdios estão adotando esta prática, cada um por um motivo próprio porém com o mesmo objetivo: ter sua própria tecnologia que atende as suas necessidades. [Neste outro post da revista Develop](http://www.develop-online.net/tools-and-tech/why-a-plucky-band-of-developers-build-their-own-game-engines/0205448 "Develop") alguns desenvolvedores comentam por que decidiram seguir este caminho.

Eu acho isto algo incrível, pois muitas vezes não é necessário mais do que juntar alguns frameworks de física e gráfico (entre outros) para criar sua própria solução. É claro que é algo trabalhoso, mas o aprendizado é muito grande durante este processo. Outro detalhe legal é que se utilizar C/C++ para fazer o jogo (e definir bem a arquitetura do jogo), é possível trocar de framework e manter o jogo funcionando. Meu primeiro projeto na EA foi justamente isso, substituir o [Marmalade](https://www.madewithmarmalade.com/ "Marmalade") utilizado em um jogo pelo novo framework EAMT, e praticamente nenhuma alteração no código principal do jogo foi necessária.

Se você está começando um jogo com muito tempo disponível ou sem pressa para lançar, eu recomendo a abordagem de criar o próprio framework para fins de estudo. É claro que não é só juntar frameworks como peças de LEGO e esperar que tudo funcione, mas existem livros muito bons sobre este assunto, com o [Game Engine Architecture](http://www.amazon.com/Engine-Architecture-Second-Jason-Gregory-ebook/dp/B00MMOJ076/ref=sr_1_1?s=books&ie=UTF8&qid=1429219288&sr=1-1&keywords=game+engine "Amazon"). Só lembrando que engines e frameworks prontos possuem diversas pessoas trabalhando para que eles sejam bons e estáveis, mas que esta abordagem de criar sua própria tecnologia ensina muito mais do que apenas utiliza-los.

Imagem da capa: [Flat Modern Design](http://www.shutterstock.com/pic-211247059/stock-vector-flat-modern-design-vector-illustration-concept-of-creative-office-room-interior-workspace.html?src=0vXV1I7QZT1OQ65QVUoYfg-1-3 "Shutterstock") do Shutterstock.


