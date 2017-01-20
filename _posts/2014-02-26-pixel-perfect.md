---
layout: post
title: 'Como ser um programador de jogos: Pixel Perfect'
---

Uma das dúvidas mais comuns no desenvolvimento de jogos para dispositivos móveis é qual a melhor maneira para que o jogo se adapte em várias resoluções, e uma das técnicas mais usadas é a chamada Pixel Perfect, que consiste em utilizar a PPI do aparelho como base para isto.

Neste post vou explicar como está técnica funciona usando como base os aparelhos da Apple com iOS. No Android e Windows Phone é a mesma coisa, porém eles possuem mais variações de PPI, por isso dá um pouco mais de trabalho. Aqui não vou explicar como identificar a DPI de um aparelho, e sim o uso da técnica. Lembrando que isto funciona apenas para jogos em 2D, pois em 3D é outra história.

PPI significa Pixels Per Inch, ou seja, é o número de pixels por polegada. Isto é literalmente o número de pixels que são exibidos em uma polegada da tela, quanto maior mais detalhes se o tamanho da tela for grande também. Algumas pessoas chama isso também de DPI, que significa Dots Per Inch, ou seja, pontos por polegada. Esta atribuição é incorreta quando falamos de aparelhos digitais, pois esta medida é usada em impressões. Porém, é bem comum chamar PPI de DPI, o próprio Google chama esta medida de DPI no Android, então acostume-se a ouvir ambos.

Primeiro, vamos analizar a resolução e o PPI dos aparelhos da Apple. No Android a DPI é classificada como MDPI, HDPI, XHDPI, entre outros. Não vou entrar nos detalhes de classificação, pois o importante neste técnica é o valor da PPI/DPI. No caso do Android, você pode encontrar [mais detalhes aqui](http://developer.android.com/guide/practices/screens_support.html "DPI").

iPhone 3G/3GS 320x480 163 ppi iPhone 4/4S 640×960 326 ppi iPhone 5/5C/5S 640×1136 326 ppi

A PPI do iPhone 3, assim como a resolução da sua tela, é exatamente a metade da PPI do iPhone 4 e de sua tela também. Por ser exatamente metade, isto significa que se você usar uma imagem do tamanho do iPhone 4 com resize no iPhone 3, ela ficará “perfeita”, e dai vem o termo Pixel Perfect. Isto só funciona quando a PPI (ou DPI) possui esta proporção de ser metade, então nestes casos você pode usar uma imagem maior com resize para um tamanho menor sem perder a qualidade e definição.

No caso do iPhone 5 temos um problema, embora sua PPI seja a mesma do iPhone 4, o tamanho da sua tela é diferente e não é proporcional, pois a largura é a mesma e a altura é diferente. Uma imagem no tamanho do iPhone 5 ficará cortada no iPhone 4, pois apesar da mesma DPI não é possível fazer o resize sem perder qualidade. Isto se aplica ao iPhone 3 também, que também tem a metade da PPI do iPhone 5, mas não tem a metade da resolução. Assim, a imagem ficará distorcida.

Estes são dois exemplos levando em conta apenas imagens com o tamanho da tela do aparelho, sendo que funciona do iPhone 4 para o iPhone 3, mas não funciona do iPhone 5 para os demais. Neste caso, muitos desenvolvedores criam uma imagem para o iPhone 5 e uma para o iPhone 4, que é usada também no iPhone 3.

Porém, para imagens que não ocupam a tela inteira como botões ou sprites, a mesma imagem usada no iPhone 5 pode ser usada no iPhone 4 sem resize, e usada no iPhone 3 com resize mas sem perder a qualidade e definição graças a PPI. Basicamente, a regra geral é esta:

> Para imagens com o tamanho da tela:  
>  – Resize só funciona sem perder a qualidade se os aparelhos tiverem a PPI/DPI e o tamanho da tela proporcionais.
>
> Para imagens menores:  
>  – Resize funciona baseado apenas na PPI/DPI, o tamanho da tela pode influenciar apenas o posicionamento dos itens na tela.

Já utilizei esta técnica algumas vezes quando trabalhei na [Glu Mobile](http://glu.com "Glu") e na [Electronic Arts](http://ea.com "EA"). O jogo que mais usei isto foi o [Scrabble](http://www.ea.com/scrabble-paid-ipad?intcmp=EACom_scrabbleipad_update_0313 "Scrabble"), para [Android](https://play.google.com/store/apps/details?id=com.ea.game.scrabblemattel_bv "Android") e [iOS](https://itunes.apple.com/br/app/scrabble/id311691366?mt=8 "iOS"). Todo seu layout é baseado na PPI/DPI do aparelho, e as imagens são usadas de acordo com esta classificação. Neste jogo o layout do tablet é diferente do smartphone, então não tivemos problemas com a PPI/DPI e resolução destes aparelhos, o que ajudou bastante no resultado final.

Espero ter conseguido explicar direito esta técnica, ela é bem simples de usar e um pouco complicada de explicar. Lembre-se que este exemplo foi feito para os modelos de iPhone, que é o mais simples de todos. Aparelhos Android geralmente dão mais problemas por causa da fragmentação e falta de padrões por parte dos fabricantes, mas não é impossível fazer uso do Pixel Perfect da mesma maneira. Qualquer dúvida, fique a vontade para perguntar nos comentários abaixo!
