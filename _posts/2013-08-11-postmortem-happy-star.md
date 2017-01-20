---
layout: post
title: 'Postmortem: Happy Star Adventures'
date: 1970-01-16 19:18:31.000000000 -03:00
---

Este é o segundo postmortem de um jogo brasileiro que recebo para postar aqui no blog, desta vez é um jogo para o publico infantil desenvolvido com a Unity pelo Andre Dantas e publicado para Android. Confira os desafios que o Andre enfrentou em publicar seu primeiro jogo abaixo. Se você também fez um jogo e publicou em algum lugar, e quer publicar um postmortem aqui, entre em contato!

> Happy Star Adventures é um jogo casual, direcionado para crianças, mas também é divertido para pessoas de todas as idades. Trata-se das aventuras de uma estrelinha que deve acumular pontos e fugir dos perigos entre céu, terra e mar.
> 
> Para vencer a aventura o jogador deve alcançar 1000 pontos em menos de 3 minutos ajudando a estrelinha a coletar itens e fugir dos vilões. Para guiar a estrela é preciso apenas deslizar o dedo pela tela do dispositivo, ou tocar no local onde deseja que a estrela se desloque.
> 
> Boa aventura!
> 
> **SOBRE**
> 
> Este é o primeiro jogo para plataformas móveis, desenvolvido por mim. A primeira versão foi desenvolvida em dez dias, logo após o nascimento da minha filha. Desde então, o jogo já recebeu cinco atualizações, e novas aventuras foram adicionadas. O game está disponível para Android e, em breve, para iOS.
> 
> Quem estiver interessado em jogar o jogo, antes de ler o Post Mortem abaixo, é só acessar os links:  
> [https://play.google.com/store/apps/details?id=com.TOPgames.Happy_Star_Adventures](https://play.google.com/store/apps/details?id=com.TOPgames.Happy_Star_Adventures)  
> [http://happystar-adventures.tumblr.com/](http://happystar-adventures.tumblr.com/)
> 
> **CONCEITO**
> 
> A idéia do jogo veio durante os meus estudos de Unity, para desenvolvimento de jogos para celulares. Eu havia ativado a licença grátis do Android para o Unity3d (versão 3.5) para publicar os jogos para esta plataforma. Os meus jogos anteriores haviam sido desenvolvidos para WEB (Heli Escape e Pale Blue) então eu não sabia se seria tão fácil desenvolver jogos para Android, já que várias funções são específicas das plataformas móveis.
> 
> Decidi fazer um cubo seguir o meu toque. Onde eu tocasse, o cubo deveria ir. Parece ser uma tarefa fácil, mas como o Unity trabalha com um espaço 3D, e as diferentes resoluções e proporções de tamanho de tela (Aspect Ratio) devem ser consideradas, demorei algumas horas para resolver este problema.
> 
> Com este problema resolvido, comecei a imaginar um jogo, onde pudesse utilizar esta funcionalidade. No fim, pensei num jogo onde as pessoas devessem deslizar o dedo pela tela, coletando alguns itens e evitando tocar em outros.
> 
> No desenvolvimento do Happy Star Adventures, encontrei algumas dificuldades e aprendi algumas lições, que irei compartilhar aqui.
> 
> **PROBLEMAS/DIFICULDADES**
> 
> 1) Iniciar o jogo sem um Game Design Document (GDD)
> 
> Como parti de uma ideia não muito concreta, terminei por desenvolver um jogo completamente sem projeto/planejamento. Agora, aprendi que isto um erro grave, pois se o desenvolvedor não tem ideia do que pretende fazer, não saberá quando acabou e durante o andamento do projeto, terá inúmeras ideias que poderão ser difíceis de incluir durante o projeto já iniciado.  
>  Por exemplo, a minha ideia inicial era de fazer apenas uma fase, sem inimigos. Apenas uma estrela passeando enquanto coisas se moviam no background, e os itens para coleta não davam pontos para o jogador. Mostrando aos amigos e familiares, todos sentiram falta de um sistema de pontuação e de algum tipo de perigo a ser evitado. Para implementar estas sugestões, desenvolvi um sistema de pontuação e perigos que, quando tocavam na estrela, subtraíam pontos do jogador. Consequentemente, precisei desenvolver algo que mostrasse se o jogador venceu ou não a partida. Então, limitei o jogo a 3 minutos, no quais o jogador deveria atingir 1000 pontos, ou perderia a partida.
> 
> Nada destas funções estavam previstas incialmente e me tomou um bom tempo para inserir tudo isso num projeto em andamento.
> 
> 2) “Fracasso” de Público
> 
> Apesar deste item não ter sido um erro técnico, adicionei ele neste Post Mortem, pois impacta diretamente no sucesso de um jogo.
> 
> No começo do projeto, pesquisei em alguns fóruns e vi que o retorno financeiro de jogos grátis, utilizando propagandas internas ao jogo, chegaria a US$1000 facilmente, mesmo em jogos mais simples. Porém, para chegar a esse valor, a quantidade de downloads do jogo deve ultrapassar 10.000 (estimativa).
> 
> Dei continuidade ao projeto, e após o lançamento… a frustração. Após 2 meses, apenas 100 pessoas baixaram o meu jogo e a receita das propagandas somavam US$1,33.
> 
> Apesar de eu ter feito este projeto como aprendizado, sem expectativas grandes de ganhar dinheiro com isso, eu não achava que o resultado seria tão ruim assim. Comecei a questionar se deveria continuar desenvolvendo jogos ou não.
> 
> Um ponto importante para este problema é que o jogo é direcionado para o público infantil. Mas esse problema eu não poderia resolver mais neste jogo, então precisei procurar outra solução.
> 
> Vamos lá. Cada fracasso gera uma nova oportunidade. Não desanimei e comecei a pesquisar mais sobre como fazer um jogo ter uma maior quantidade de downloads. Aprendi que a coisa não é tão fácil quanto me diziam. É extremamente importante planejar uma estratégia de marketing antes mesmo de começar a desenvolver um jogo. Monte o seu site/blog, entre em contato com outros desenvolvedores para opinarem, escreva sobre o andamento do seu projeto, coloque versões Betas para todos verem, mande press releases para sites especializados em jogos… Tudo isto tem que ser feito para aumentar as suas chances de sucesso após o lançamento.
> 
> Antes de começar a colocar esta estratégia em prática, achei que um dos problemas para a falta de popularidade do jogo é que ele possuía apenas uma fase (no Espaço) e resolvi desenvolver uma nova fase (no Campo), lançada 2 meses depois da data de lançamento do jogo.
> 
> Estranhamente, 10 dias antes do lançamento da nova fase, a quantidade de downloads começou a aumentar ligeiramente e logo depois, disparou rapidamente, atingindo uma média do último mês de aproximadamente 35 downloads por dia. As instalações totais, que demoraram 2 meses para chegar a 100, em mais 2 meses, atingiram 1800. As receitas com propagandas já atingem US$61,76.
> 
> A criação da terceira fase (no fundo do mar) já não elevou a quantidade de downloads consideravelmente, como ocorreu no lançamento da segunda fase.
> 
> A minha expectativa inicial ainda não foi atingida, mas pelo menos o resultado já não é tão frustrante quanto no início.
> 
> 3) Falta de Fluidez no Jogo
> 
> Depois de um tempo notei que, mesmo em dispositivos mais poderosos, o jogo ficava travando rapidamente, prejudicando a fluidez nos movimentos da estrela.
> 
> Pesquisando sobre o assunto, achei duas possíveis causas para isto: Excesso de uso do Instantiate (Criação de um objeto durante o jogo) e o uso de planos com múltiplas faces no mesh, para as texturas.
> 
> Para resolver o problema do Instantiate, mudei a estratégia de CRIAR e depois DESTRUIR os objetos de jogo várias vezes, para fazer apenas o reposicionamento deles. Quando um objeto sair da tela, ele volta à posição inicial, sem precisar ser destruído e depois recriado. Esta estratégia melhorou a fluidez parcialmente.
> 
> Em relação aos planos, utilizei um plano criado no Blender, com apenas 1 face (2 triângulos) para substituir o plano nativo do Unity, com 100 faces (200 triângulos). Com isso, reduzi a quantidade de triângulos de aproximadamente 40 mil para 400, otimizando o processamento e melhorando mais ainda a fluidez do jogo.
> 
> 4) Diferenças nas Telas dos Dispositivos
> 
> Este problema tirou o meu sono várias vezes. Mesmo já tendo chegado a uma solução, sempre que eu tentava fazer ajustes, os objetos ficavam desproporcionais dependendo do Aspect Ratio utilizado, e eu tive dificuldades para entender totalmente como o Unity tratava estas mudanças.
> 
> Inicialmente, por meio de programação, fazia cálculos baseado no comprimento (x) e altura (y) da tela. Descobri uma constante que deveria ser aplicado ao tamanho dos objetos, e multiplicava este valor pelo tamanho atual do objeto, fazendo todos os elementos do jogo aumentarem ou diminuírem, dependendo do Aspect Ratio utilizado. Que loucura!
> 
> Após a segunda atualização do jogo, decidi estudar mais este problema. Descobri que o Unity ajusta automaticamente o tamanho da câmera do jogo, dependendo do tamanho da tela em Pixels. Mas se o Aspect Ratio for diferente o tamanho da câmera deve ser ajustado via programação. Assim, descobri qual a fórmula que deveria ser utilizada para ajustar o tamanho da câmera e não precisei mais alterar o tamanho dos objetos. Ficou perfeito para o meu caso, mas esta solução apenas funciona para uma câmera em modo Ortográfico, modo comum em jogos 2D.
> 
> **SUCESSOS/APRENDIZADO**
> 
> 1) Unity e Playmaker
> 
> Sem a game engine Unity, eu acho que não teria condições de fazer este jogo, já que eu não tenho muitas habilidades de programação e o Unity permite que muitas funções sejam realizadas por funções já pré-programadas na engine. Sua capacidade de exportar um mesmo jogo para várias plataformas diferentes, praticamente sem configuração extra, torna o desenvolvimento ainda mais fácil. E o melhor, a licença Indie para o Unity é gratuita.
> 
> Como não sei programar muito bem, o Playmaker foi indispensável para que eu conseguisse programar o jogo. O Playmaker é um plugin que permite que a programação seja realizada por meio de diagramas de blocos, substituindo a necessidade de programar diretamente nas linguagens do Unity (Javascript ou C#). O Happy Star Adventures foi totalmente desenvolvido com o Playmaker, sem a necessidade de digitar uma linha de código. Foram os US$45 mais bem gastos da minha vida!
> 
> 2) Arte Vetorial
> 
> As minhas habilidades artísticas deixariam uma criança de 6 meses com inveja. Por isso, decidi me aprimorar tecnicamente, aprendendo a utilizar um programa de desenho vetorial (Inkscape) e usar figuras como modelos para fazer as texturas do jogo. Desta forma, não precisei desenvolver minhas habilidades artísticas, mantendo a arte simples o suficiente para não fazer a minha incompetência aparecer.
> 
> Apesar de saber que um artista de verdade faria algo muito melhor, estou satisfeito com o resultado final. Ficou bem melhor do que eu esperava.
> 
> 3) Dinheiro!
> 
> Como já falei, estou recebendo bem menos do que esperava, mas já foi o suficiente para aprender algumas coisas sobre como ganhar dinheiro com aplicativos e jogos grátis.
> 
> Eu utilizo o AdMob (do Google) para colocar as propagandas no meu jogo e o AdMob me paga por cada clique que algum usuário dá nestas propagandas.
> 
> Depois que a quantidade de usuários dos Estados Unidos, Canadá e Austrália começaram a baixar mais o meu jogo, descobri uma coisa interessante. O valor pago pelo AdMob por clique nestes países chega a ser 6,3 vezes maior que o que me pagam por clique de brasileiros. Então, definitivamente, façam seus jogos também em inglês e se preocupem em divulgar seus jogos em sites e blogs estrangeiros.
> 
> Outra coisa que aprendi é que, se o jogo for curto, as pessoas não terão tempo suficiente para clicar nas propagandas. Por isso é importante planejar o jogo desde o início para que ele dure o máximo possível para ser terminado.
> 
> 4) Rapidez e Simplicidade
> 
> Por ter mantido o jogo simples desde o início, consegui terminar a primeira versão em apenas 10 dias e já publicá-lo no Google Play.
> 
> Se o jogo levar muito tempo para ser desenvolvido, principalmente se for o seu primeiro, vai dar a você muita dor de cabeça e o fará querer desistir várias vezes durante o processo. Você ainda estará aprendendo a usar as ferramentas e se encontrar um desafio maior, após tanto ter batalhado para chegar aonde chegou, pode colocar tudo a perder, achando que nunca poderá fazer um jogo do início ao fim.
> 
> Felizmente, não senti esta pressão neste jogo e pude, logo após o lançamento da primeira versão, aprender rapidamente onde havia errado e já partir para encontrar as soluções necessárias.
> 
> Algumas pessoas não acreditam, mas quem nunca fez um jogo do início ao fim, não tem muita ideia de como é difícil fazer um jogo sozinho. Terminar este primeiro jogo te dará moral para conseguir um emprego na área ou para conseguir se unir a uma equipe maior e começar a fazer jogos ainda melhores.
> 
> **CONCLUSÃO**
> 
> Cada vez que começo um projeto deste tipo, me impressiono com a quantidade e complexidade de ferramentas e habilidades que temos que dominar do início ao fim, sem perder o foco. Ao fim, no entanto, a satisfação de ver o seu jogo disponível para todo o mundo é maior do que jogar todos os jogos de uma vez só.
> 
> Mas para que isso aconteça, se prepare, seja humilde, aprenda com os erros dos outros e se dedique ao máximo.
> 
> Caso alguém tenha algum questionamento adicional, pode me contatar pelo e-mail localizado no final do site: [http://happystar-adventures.tumblr.com/](http://happystar-adventures.tumblr.com/)
> 
> Para finalizar, gostaria de agradecer a todos os que me apoiaram durante o desenvolvimento deste jogo, e ao Bruno Cicanci por publicar este Post Mortem em seu blog.
> 
> Abraços para todos.


