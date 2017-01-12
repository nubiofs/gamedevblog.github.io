---
layout: post
title: A tecnologia por trás de Minecraft
date: 1970-01-16 04:12:18.000000000 -03:00
---

Eu conheci o jogo indie [Minecraft](http://www.minecraft.net "Minecraft") em dezembro de 2010. Na época, seu desenvolvimento tinha passado da fase alpha para a fase beta. Duas coisas me deixaram muito curioso: (1) era um jogo que dependia da criatividade do jogador, lembrava [Lego](http://www.lego.com "Lego"), e também tinha monstros que apareciam a noite e em cavernas que o jogador poderia explorar; e (2) o seu modelo de comercialização, onde o jogo era vendido inacabado durante sua fase de produção.

[![](http://gamedeveloper.com.br/blog/wp-content/uploads/2011/11/minecraft_titulo.jpg "Minecraft")](http://www.minecraft.net/)

**Um começo com pé direito**

O [desenvolvimento de Minecraft](http://www.minecraft.net/game "Minecraft") foi iniciado oficialmente em 10 de maio de 2009, por [Markus “Notch” Persson](http://notch.tumblr.com/ "Notch"). Notch largou seu emprego de desenvolvedor de jogos para tornar-se um desenvolvedor independente, já que acreditava muito na sua ideia. Desde o seu início, o jogo foi oferecido como uma prévia para ser[ jogado no navegador](http://www.minecraft.net/classic/play "Minecraft") ou uma versão para jogar no computador com mais algumas coisas, e essa versão era paga. Mas como assim, comprar por um jogo que ainda estava em desenvolvimento?

<figure class="wp-caption aligncenter" id="attachment_905" style="width: 550px">[![](http://gamedeveloper.com.br/blog/wp-content/uploads/2011/11/minecraft_notch.jpg "Notch")](http://notch.tumblr.com/)<figcaption class="wp-caption-text">Markus "Notch" Persson</figcaption></figure>Em um primeiro momento achei estranho, quem compraria um jogo em fase alpha, com poucas features e com risco de não ser finalizado? Bom, eu como muitas outras pessoas acreditas no jogo por que achamos divertido, e também havia a promessa de que quem comprasse antes teria acesso a todos updates do jogo e pagaria menos pela sua cópia. Durante a fase alpha o jogo foi comercializado a €10, depois na fase beta por €15, e agora está sendo vendido a €20.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/m_yqOoUMHPg?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Em pouco tempo o jogo de Notch ficou famoso, chegando a impressionantes [4 milhões de unidades vendidas](http://g1.globo.com/tecnologia/noticia/2011/11/game-independente-minecraft-passa-dos-4-milhoes-de-downloads.html "G1") antes do seu lançamento na sexta-feira passada durante a [MineCon](http://minecon.mojang.com/ "MineCon"). E, junto com o sucesso do jogo, nasceu uma cultura relacionada a marca Minecraft, que começou com [camisetas ](http://www.minecraft.net/store "Minecraft")e [papercrafts](http://www.minecraftforum.net/topic/18345-the-standardized-papercraft/ "Papercraft"), até um [documentário](http://www.kickstarter.com/projects/2pp/minecraft-the-story-of-mojang "Documentário") e seu próprio evento de dois dias realizado em Las Vegas. Notch conseguiu dinheiro mais do que suficiente para aumentar seu studio, Mojang, terminar Minecraft e poder produzir tranquilamente o jogo que quiser pelos próximos anos sem se preocupar com investidores.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/q_AMqCJSMMI?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Agora que eu falei um pouco do fenômeno Minecraft, vou analisar mais de perto alguns de seus aspectos técnicos. Pensei em dividir minha análise em duas partes, como um documento de post mortem: “O que deu certo?” e “O que deu errado?”. Como falar que algo deu errado em Minecraft não é algo muito lógico, vou chamar essa parte de “O que não deu tão certo?”.  Meu objetivo não é analisar o Game Design do jogo, mas sim toda sua parte técnica, como programação e distribuição.

**O que deu certo?**

Notch [desenvolveu seu jogo indie](http://www.minecraft.net/game/credits "Minecraft") utilizando a [linguagem de programação Java](http://www.java.com "Java"), pois ele queria que seu jogo fosse acessível para todos. Nisso ele conseguiu se dar bem, por que graças à [JVM ](http://pt.wikipedia.org/wiki/M%C3%A1quina_virtual_Java "JVM")(Java Virtual Machine) Minecraft pode rodar em [Windows, MacOS, Linux, Solaris](http://www.minecraft.net/download "Minecraft"), e qualquer outro sistema operacional com suporte a JVM. Para a programação foi utilizado também o [LWJGL ](http://www.lwjgl.org/ "LWJGL")(Lightweight Java Game Library), um framework gratuito para desenvolvimento de jogos com Java, além do [JOrbis ](http://www.jcraft.com/jorbis/ "JOrbis")(Ogg decoder) e [3D Sound System](http://www.paulscode.com/forum/index.php?topic=4.0 "3D Sound System") (som para ambientes tridimensionais).

<figure class="wp-caption aligncenter" id="attachment_906" style="width: 550px">[![](http://gamedeveloper.com.br/blog/wp-content/uploads/2011/11/minecraft_android.jpg "Minecraft")](https://market.android.com/details?id=com.mojang.minecraftpe&hl=pt_BR)<figcaption class="wp-caption-text">Minecraft - Pokect Edition para Android</figcaption></figure>Minecraft possui um modo de jogo Cliente-Servidor, onde os jogadores podem participar da mesma sessão no mesmo mundo, onde juntos podem construir mais coisas e mais rápido. Este modo multiplayer também foi desenvolvido utilizando Java e alguns pacotes nativos da linguagem com suporte  a rede. Embora seja uma linguagem de programação não muito utilizada para jogos, ainda assim ela possui muitos pacotes e frameworks gratuitos úteis para dar suporte ao desenvolvimento.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/jO-y5wzmK4E?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Escolher Java também ajudou muito na conversão do jogo para smarthphones e tablets com o [sistema operacional Android](https://market.android.com/details?id=com.mojang.minecraftpe&hl=pt_BR "Android Market"). Como o Android tem suporte a JVM, provavelmente foram necessários apenas ajustes relacionados ao hardware dos aparelhos, como optimizar consumo de memória e modificar os controles do jogo para touchscreen, por exemplo. O Java também permitiu a publicação de uma [versão web do jogo](http://www.minecraft.net/play "Minecraft"), disponível para jogar no site utilizando o mesmo save game que a versão desktop.

**O que não deu tão certo?**

Se por um lado Java foi muito bom para tornar o jogo acessível para todos, ele limitou um pouco as plataformas em que o jogo poderia ser distribuído. C/C++ é a tecnologia mais utilizada hoje para desenvolvimento de jogos, e um dos grandes benefícios é ser multiplataforma e não depender de uma máquina virtual, pois roda nativamente em qualquer sistema operacional, de qualquer plataforma.

<figure class="wp-caption aligncenter" id="attachment_908" style="width: 550px">[![](http://gamedeveloper.com.br/blog/wp-content/uploads/2011/11/minecraft_ios.jpg "Minecraft")](http://itunes.apple.com/pt/app/id479516143?mt=8)<figcaption class="wp-caption-text">Minecraft - Pocket Edition no iOS</figcaption></figure>Com C/C++, Minecraft poderia ter sido distribuído na [App Store da Apple](http://itunes.apple.com/pt/app/id479516143?mt=8 "App Store") há algum tempo, pois poderia ser facilmente convertido de uma versão desktop para iOS, da mesma maneira que foi feita a conversão da versão Java para Android. E, graças ao NDK, o mesmo código nativo também funcionaria no Android. C/C++ daria mais flexibilidade ao código, podendo ser convertido para distribuição nas redes de consoles Xbox Live, Playstation Network e Wii Ware.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/rfYuY3sv1Ro?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

Como o jogo foi lançado para iOS recentemente, e logo será lançado para Xbox Live, provavelmente houve uma conversão do código Java para C/C++. O tempo e o custo desta conversão poderia ter sido utilizados para melhorar ainda mais o jogo caso tivessem escolhido C/C++ desde o início, ao invés do Java. Mas, Notch teve um bom motivo para utilizar Java, provavelmente ela tinha um bom conhecimento prévio para começar um jogo indie utilizando Java ao invés de C/C++. Na minha opinião estes são pequenos detalhes que poderiam ser pensados desde o início do projeto.

**Ao infinito e além**

Notch pode não ter sido feliz na escolha da sua tecnologia para criar Minecraft, mas isso não importa muito, pois o jogo é um sucesso. Apensar de que as versões mobile são bem limitadas, a versão de desktop melhorou muito e está muito divertida, vale a pena conferir. Alias, diversão é algo que sempre preocupou Notch, e ele garante que se uma feature não é divertida, ele não incluirá no jogo.

<figure class="wp-caption aligncenter" id="attachment_901" style="width: 550px">[![](http://gamedeveloper.com.br/blog/wp-content/uploads/2011/11/minecraft_ingame.jpg "Minecraft")](http://www.minecraft.net/)<figcaption class="wp-caption-text">Minecraft para PC</figcaption></figure>Agora que a versão de desktop finalmente atingiu seu status Gold, a Mojang provavelmente irá focar no desenvolvimento de conteúdos extras para o Minecraft, conquistar novas plataformas e trabalhar em novos jogos, como o Scrolls, que foi anunciado este ano. E sabe qual é a parte mais legal disso tudo? Notch disse que no futuro, quando as vendas do Minecraft estiverem baixas, ele tornará o [código fonte do jogo público](http://www.minecraft.net/game "Minecraft") para que todos possam ver como o jogo foi feito. Porém, do jeito que este jogo está vendendo, talvez isso demore um pouco.

**Conclusão**

Através desta análise técnica eu tentei contar detalhes interessantes sobre o desenvolvimento do jogo indie milionário Minecraft, bem como analisar um pouco do que sei sobre as tecnologias e escolhas do seu desenvolvimento. Escrevi muita coisa baseada na minha opinião e experiência com desenvolvimento de jogos, espero que tenham gostado.

Esta foi uma análise mais técnica, porém existem diversos ângulos que podemos analisar Minecraft, como seu Game Design, seu impacto cultural, seu modelo de negócios, suas mecânicas, usabilidade, interface, entre vários outros. Este jogo é um ótimo caso para ser estudado em diversas áreas relacionadas ao desenvolvimento e a indústria de jogos, e podem ficar horas falando sobre seus detalhes.

Se você quiser saber mais sobre [Minecraft ](http://www.minecraft.net/ "Minecraft")visite o seu site oficial e o blog do [Notch](http://notch.tumblr.com/ "Notch"). Existem também uma [comunidade ](http://www.minecraft.net/community "Minecraft")muito ativa sobre o jogo, alguns conseguem criar coisas incríveis (e outras nem tanto) com os blocos de Minecraft. Para finalizar, um vídeo que demonstra que podemos até criar músicas dentro do jogo:

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/j4qQHWP0GXg?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

<div id="-chrome-auto-translate-plugin-dialog" style="opacity: 1 !important; background-image: initial !important; background-attachment: initial !important; background-origin: initial !important; background-clip: initial !important; background-color: transparent !important; position: absolute !important; top: 0px; left: 0px; overflow-x: visible !important; overflow-y: visible !important; z-index: 999999 !important; text-align: left !important; display: none; background-position: initial initial !important; background-repeat: initial initial !important; padding: 0px !important; margin: 0px !important;">![](http://www.google.com/uds/css/small-logo.png)

</div>
