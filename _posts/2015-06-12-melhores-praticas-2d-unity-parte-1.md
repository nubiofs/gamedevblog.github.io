---
layout: post
title: Melhores práticas para 2D na Unity - Parte 1
---

Trabalhei em um projeto grande utilizando a [Unity](http://unity3d.com/), e aprendi tanta coisa útil sobre otimização para jogos 2D durante o desenvolvimento que vale a pena compartilhar por aqui.

Vou listar alguns tópicos abaixo com o que aprendi para melhorar o desempenho da Unity em jogos 2D. Para ter uma idéia, só o menu principal do jogo estava usando mais de 350MB de memória em um aparelho iOS e a build estava com pouco mais de 100MB. Após fazer as otimizações listadas abaixo, o consumo de memória caiu para 50MB no menu principal e a build ficou com pouco mais de 30MB.

Apenas como referência, neste projeto utilizei a Unity 4.5.5 e o NGUI como plugin para criar toda interface do jogo e menu. Embora eu esteja usando este plugin, muitas dicas abaixo podem ser usadas no 2D da Unity. Esta é a primeira parte de uma série de três.

**Reduzindo o peso das imagens**

A primeira coisa que devo avisar aqui é que não importa o quanto você consegue comprimir uma imagem, a Unity vai descomprimir e usar seu tamanho real na importação do editor, e recomprimir quando compilar o projeto.

Então por que devemos nos preocupar em reduzir o peso das imagens? Por que isso ajuda a reduzir muito o tamanho da build! Vou recomendar aqui dois programas gratuitos para Mac OS X que ajudam a comprimir imagens e otimizar seus dados.

[![ImageAlpha](../content/images/2015/03/screenshot-1.3.png)](../content/images/2015/03/screenshot-1.3.png)

[ImageAlpha](http://pngmini.com/): este programa reduz muito o tamanho de imagens PNG, principalmente com transparência. Ele faz um processamento na imagem que remove alguns bytes de cores não usadas e converte para outro formato PNG muito mais eficiente.

[![ImageOptim](../content/images/2015/03/ImageOptim-yosemite.png)](../content/images/2015/03/ImageOptim-yosemite.png)

[ImageOptim](https://imageoptim.com/): este programa deve ser utilizado após reduzir o tamanho da imagem com o ImageAlpha para ter um resultado melhor. Ele comprimi a imagem reduzindo o tamanho sem perder qualidade. Sua redução é menor do que o ImageAlpha, porém juntos funcionam muito bem. Um aviso: este software é muito lento, então tenha paciência e deixe seu computador processando as imagens enquanto você joga alguma coisa em seu console ou dispositivo móvel.

Esta dica não é algo exclusivo da Unity, eu já utilizei em projetos com Cocos2d-x e HTML5, funciona muito bem! Infelizmente só rodam em Mac OS X, mas pelo menos são gratuitas, open source e podem ser utilizadas pela linha de comando para processar muitas imagens de uma vez.

Um aviso: dependendo da imagem, as vezes pode acontecer de perder a qualidade por causa da redução do número de cores. Então fique atento quanto a isto e sempre prefira utilizar este recurso em imagens com pouca variação de cor.

**Resolução das imagens para dispositivos móveis**

Isto foi algo que deixei passar despercebido e só depois de alguns testes entendi o que estava fazendo de errado. Os dispositivos utilizam OpenGL ES para lidar com a parte gráfica dos jogos e aplicativos, por isso muitas coisas que a Unity faz internamente tem como objetivo otimizar o jogo para OpenGL quando a build for para dispositivos móveis (Android e iOS).

Toda imagem carregada na memória é convertida em um tamanho POT (Power Of Two, potência de 2) para fins de otimização do OpenGL. Sabendo disso, a Unity junta as imagens para formar POT internamente, porém isso pode deixar tudo mais pesado.

Eu pesquisei bastante sobre qual seria a melhor resolução para fazer um jogo mobile na Unity, e embora muitos digam que o melhor é partir da maior resolução, eu acho que aqui está um item chave para melhorar o jogo. A maior resolução recomendada é do iPad com retina 2048×1536. Porém, quando convertida para POT esta imagem vai ter o tamanho de aproximadamente 2048×2048 e muitos bytes transparentes.

Na parte 2 vou abordar as melhores práticas usando NGUI (que também servem para o 2D da Unity) e como utilizar sprite sheets no jogo. Na parte 3 vou dar algumas dicas para otimização de código. Se você tem alguma dúvida ou dica relacionada ao assunto é só comentar abaixo!
