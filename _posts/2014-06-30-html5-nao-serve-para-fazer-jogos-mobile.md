---
layout: post
title: HTML5 não serve para fazer jogos mobile
---

Desde o seu surgimento, muita gente diz que o HTML5 seria o substituto do Flash para jogos, principalmente por ter um canvas 2D. Antes eu apoiava esta ideia, mas hoje já não acredito mais nisso em plataformas móveis.

Antes de começar a falar sobre o assunto do post, quero esclarecer algo que muitos se confundem: o HTML5 é apenas um padrão para marcações de HTML, e você não usa tudo desse padrão para fazer jogos, apenas a tag <canvas>. A programação do jogo é feita com Javascript, portanto, o jogo não é “desenvolvido com HTML5”, mas sim com Javascript.

O HTML5 é muitas vezes vendido como uma solução “perfeita” para o desenvolvimento de jogos e apps, pois você pode tornar o produto acessível através de um navegador (desktop, mobile e até consoles). Além disso, em plataformas móveis, existe a possibilidade de colocar o projeto dentro de um wrapper (como [PhoneGap](http://phonegap.com/ "PhoneGap") ou [Titanium](http://www.appcelerator.com/titanium/ "Titanium")) e lançar o jogo ou app nas stores.

Parece um mundo perfeito, sem Flash (nada contra rs) e com uma solução que “funciona” em qualquer plataforma, certo? Bom, por mais que vendam isso, esta utopia não existe.

Na empresa que trabalho atualmente tive a oportunidade de participar do desenvolvimento de um jogo muito parecido com o [SongPop](http://www.songpop.net/ "SongPop"), do seu início ao fim. Ele possui perguntas, interação social, partidas por turno e muitas outras coisas, então existe uma integração de front-end e back-end.

Foi possível desenvolver o jogo sem grandes problemas, e ele funciona bem nas plataformas desktop e mobile, porém o uso de HTML5 deixou o que deveria ser simples mais complicado de fazer: a interface. A integração com redes sociais e com o próprio servidor do jogo foi muito fácil se comparado com o trabalho de montar a interface do jogo, que é apenas telas com botões de ação.

O que era mais simples no Flash se torna a maior dificuldade em utilizar HTML5 para jogos, não existe uma solução visual boa para auxiliar o desenvolvimento. Mesmo soluções como o [Construct 2](https://www.scirra.com/ "Construct 2") são fracas e limitadas, pois facilitam a parte visual mas atrapalham a programação forçando o programador a utilizar tudo no padrão deles.

Outro fator que me fez não gostar do HTML5 para jogos mobile é o desempenho. O navegador do smartphone e tablets é um aplicativo que roda no sistema operacional, e o jogo roda dentro desse aplicativo. Por isso, muitas coisas são extremamente limitadas, como a memória disponível e o controle do contexto do jogo.

O carregamento de algumas músicas pode fazer aparelhos bons, como o iPhone 4S, não aguentarem e fecham o navegador. Pelos testes que fiz, estes navegadores aguentam no máximo algo perto de 10MB de imagens e sons na memória, mais do que isso faz o desempenho do jogo cair muito e o navegador fechar.

Para o desenvolvimento do jogo em questão, utilizei a suite de frameworks [CreateJS](http://www.createjs.com/#!/CreateJS "CreateJS"), um conjunto de bibliotecas Javascript muito bom para desenvolvimento de aplicações web interativas, como jogos ou aplicativos. Utilizei o [EaselJS](http://www.createjs.com/#!/EaselJS "EaselJS"), para o canvas, [PreloadJS](http://www.createjs.com/#!/PreloadJS "PreloadJS"), para fazer o carregamento dos recursos, e [SoundJS](http://www.createjs.com/#!/SoundJS "SoundJS"), para gerenciamento do som.

Este framework é muito bom para desenvolvimento web com Javascript, um dos melhores e mais estáveis do mercado. Porém, HTML5 não foi feito para jogos em navegadores. Enquanto que para desktop não há problemas, para mobile o navegador dos aparelhos coloca um limite sem sentido para jogos.

Mesmo utilizando wrappers, como os dois citados no começo do post, isso não quer dizer que os problemas foram resolvidos. Embora dentro de um wrapper o jogo possa usar mais memória, pois roda como um aplicativo, ainda assim existem limites. Quem já desenvolveu utilizando wrappers para conteúdo com HTML5 sabe o quanto é complicado fazer muitas coisas que depende do hardware funcionarem, isso sem falar em problemas de layout que sempre acontecem devido a limitação também presente nestes wrappers.

Enquanto não existir uma solução visual boa para o desenvolvimento de jogos com HTML5, mesmo seu uso em desktop será sempre limitado e de difícil utilização. Existem muitas outras opções melhores hoje, com a [Unity](http://unity3d.com/ "Unity"). É estranho ter tantos frameworks e tanta gente incentivando o uso de HTML5, porém não existem ferramentas de qualidade para auxiliar o desenvolvimento.

Para desktop, eu acredito que o uso de HTML5 para jogos só vai crescer quando houver mais ferramentas que auxiliem o desenvolvimento, e não estou falando de frameworks, e sim de softwares. Grandes jogos não são feitos apenas de frameworks, mas sim diversas ferramentas que auxiliam o desenvolvimento.

Para mobile, o melhor é não usar. Mesmo para o desenvolvimento de apps, o HTML5 é extremamente fraco. Nada é melhor do que fazer um aplicativo utilizando os recursos presentes no [Android SDK](http://developer.android.com/ "Android") e [iOS SDK](https://developer.apple.com/ "iOS"). Acredite: o trabalho de fazer dois apps com códigos diferentes é menor do que fazer um app com HTML5 e esperar que funcionem em ambos, e você ainda ganha mais desempenho no app.

Apps grandes como Facebook, Twitter, WhatsApp, entre muitos outros, são feitos em projetos separados para cada sistema operacional mobile, pois eles precisam de performance e flexibilidade, coisas que o HTML5 está muito longe de oferecer. Se os grandes fazem assim, por que insistir em um padrão fraco? Muitas vezes os programadores preferem utilizar o HTML5 por preguiça de fazer mais de um projeto, e no fim acabam com uma solução mobile ruim ou tendo que fazer projetos para cada wrapper (que também é ruim).

Com tantas opções hoje para desenvolvimento de jogos (e apps) mobile, não há razão para utilizar o HTML5. Eu tive todo tipo de experiência em jogos e aplicativos, ambos utilizando engines e frameworks bons e ruins, e tenho muito certeza quando digo que o momento é de abandonar o uso de HTML5 para jogos e aplicativos mobile. Ah, não confunda aplicativo com site, existe uma grande diferença entre prestar um serviço e mostrar informações.

Desculpe o texto longo em forma de desabafo, seu objetivo é deixar claro que o HTML5 não é a solução de todos os problemas, não tem ferramentas boas para desenvolvimento, e não tem bons motivos para ser usado em jogos e aplicativos mobile. Deixe seu comentário abaixo para continuarmos esta discussão.

**UPDATE**

Se você quiser ver uma longa explicação técnica de por que HTML5 não serve pra mobile, leia estes dois excelentes artigos (em Inglês):

[Mobile web apps are slow](http://sealedabstract.com/rants/mobile-web-apps-are-slow/)

[Why mobile web apps are slow](http://sealedabstract.com/rants/why-mobile-web-apps-are-slow/)
