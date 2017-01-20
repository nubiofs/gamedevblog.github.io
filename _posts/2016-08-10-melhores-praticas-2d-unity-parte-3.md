---
layout: post
title: Melhores práticas para 2D na Unity - Parte 3
---

Na [parte 1](http://gamedeveloper.com.br/melhores-praticas-2d-unity-parte-1) falei sobre dicas para reduzir o tamanho das imagens e melhores resoluções para dispositivos móveis, e na [parte 2](http://gamedeveloper.com.br/melhores-praticas-2d-unity-parte-2) o foco foi o plugin [NGUI](https://www.assetstore.unity3d.com/en/#!/content/2413) (mas as dicas também se aplicam ao UI da Unity) e ao uso de sprite sheets. Desta vez o foco serão melhores práticas de programação para jogos 2D na Unity.

Apesar de ter o foco em 2D, boa parte do conteúdo deste post abrange jogos em 3D na Unity também. No site da Unity existe uma categoria de [Melhores Práticas](http://unity3d.com/pt/learn/tutorials/topics/best-practices) excelente, falando de física, assets e UI.

**O Update**

Quando criamos um novo script na Unity, por padrão os métodos `Start()` e `Update()` são adicionados ao código. O maior problema é não dar atenção a este detalhe, pois muitos programadores deixam estes métodos mesmo vazios no script, e isto pode fazer diferença no desempenho do jogo dependendo da quantidade de scripts sendo usados.

Internamente a Unity executa todos os `Update()` que encontra nos scripts ativos na cena do jogo, mesmo eles estando vazios. Este [artigo](http://blogs.unity3d.com/2015/12/23/1k-update-calls) publicado no blog da Unity explica este problema em maiores detalhes. Se você não for utilizar o método, simplesmente remova do seu código. O `Start()` não faz muita diferença, mas o `Update()` pode reduzir o seu frame rate significativamente, principalmente em dispositivos móveis.

Imagens e sprite sheets de jogos 2D podem ocupar mais espaço em disco e memória do que modelos 3D com textura, o que pode exigir um processamento extra do hardware que pode ser adquirido seguindo boas práticas como esta mencionada acima.

**A Física**

A Unity possui uma versão 2D para praticamente todo componente disponível no 3D, e mesmo sendo otimizado pode exigir bastante processamento do hardware se existirem muitos objetos na cena. Se eu não me engano, mesmo que o objeto não esteja sendo desenhado na tela, sua física continua ativa para verificações de colisão fora da tela. Se no seu jogo existem muitos objetos colidindo ao mesmo tempo em uma cena podemos desabilitar a física (ou mesmo o objeto inteiro) quando ele estiver fora da tela.

Por exemplo, em um jogo de estratégia como StarCraft podemos "ligar" a física dos objetos quando as unidades do jogador estiverem em uma área próxima das unidades do imigo. Para evitar verificações em cada update (e poder ter o problema do tópico anterior), você pode deixar a física habilitada no líder do grupo, e fazer ele habilitar a física nos depois com um callback quando chegar na área do inimigo. É apenas uma ideia, provavelmente existe maneiras ainda melhores pra isso, mas o ponto é que muitos objetos com física ativada podem causar problemas de desempenho.

A [Defold](http://www.defold.com), uma game engine desenvolvida pela King para jogos 2D, limita o número de objetos com colisão por nível. Tive este problema quando estava desenvolvendo o jogo [Metaforce](http://gamejolt.com/games/metaforce/141821) para o [Ludum Dare #35](http://gamedeveloper.com.br/ludum-dare-35/), montei o mapa inteiro com colisão para o personagem não atravessar as paredes, mas o limite da engine (que eu não sabia) me fez mudar a maneira de verificar a colisão com o cenário.

**O Loading**

Isto depende muito do jogo, mas geralmente temos duas maneiras de carregar as imagens do cenário: tudo de uma vez ou aos poucos. A vantagem de carregar tudo de uma vez é que o jogo flui sem a necessidade de fazer o load de imagens do disco para a memória durante o jogo, mas a desvantagem é que em alguns hardwares isto pode fazer o jogo usar toda memória disponível e quebrar, ou pode ser que o loading seja muito longo em aparelhos com hardware fraco.

Carregar aos poucos, ou [Lazy Loading](https://en.wikipedia.org/wiki/Lazy_loading) como é conhecido, é você carregar as imagens apenas quando for necessário. Por exemplo, você não precisa carregar a arte do chefão sem saber se o jogador vai chegar no final da fase para enfrentá-lo, ou carregar todas as imagens de achievements do jogo, mesmo sendo difícil de conseguir todos na mesma fase. A vantagem disso é que você usa apenas a memória necessária para carregar as imagens que precisa no momento, e assim o loading inicial fica mais rápido e com um risco menor de quebrar o jogo em aparelhos com hardware fraco. A desvantagem é que você vai precisar escrever o código para gerenciar o loading de recursos do jogo para que sejam carregados apenas quando necessários.

Ah, e não se esqueça de ter uma tela de loading ou um feedback para que o jogar saiba o que está acontecendo. Isto é mais Game Design do que Programação, mas vale a pena sempre pensar neste detalhes durante o desenvolvimento.

Esta foi a terceira e última parte sobre melhores práticas para fazer um jogo em 2D na Unity. A ideia inicial era ter publicar estes posts em sequencia, porém demorei mais de 1 ano para publicá-los. Se você quiser saber mais sobre desenvolvimento de jogos com Unity acompanhe o desenvolvimento do meu jogo [Final Frontier](http://gamedeveloper.com.br/tag/final-frontier/), estou escrevendo um post sobre o progresso do jogo a cada 2 semanas.
