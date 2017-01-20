---
layout: post
title: Organização de um projeto de jogo (parte 5)
date: 1970-01-16 08:58:44.000000000 -03:00
---

Esta é a última parte da série de posts com dicas sobre como organizar seu projeto de jogo. Neste último post farei um comparativo sobre o uso dos serviços na nuvem, apresentados nos posts anteriores, e o que vale a pena manter offline. Confiram aqui a [parte 1](http://gamedeveloper.com.br/blog/2012/06/04/organizacao-projeto-jogo-parte-1/ "Parte 1"), [parte 2](http://gamedeveloper.com.br/blog/2012/06/05/organizacao-projeto-jogo-parte-2/ "Parte 2"), [parte 3](http://gamedeveloper.com.br/blog/2012/06/06/organizacao-projeto-jogo-parte-3/ "Parte 3") e [parte 4](http://gamedeveloper.com.br/blog/2012/06/07/organizacao-projeto-jogo-parte-4/ "Parte 4").

**Online vs Offline**

Tudo que foi apresentado até aqui visa manter todas as informações do projeto na nuvem da internet, para que todos os membros tenham fácil acesso a qualquer hora, através de qualquer computador ou dispositivo móvel. Pelos motivos apresentados, como compartilhar sempre arquivos atualizados e facilitar a organização do projeto, todos estes serviços online são incrivelmente úteis.

Porém, existem coisas que podem funcionar melhor localmente. Por exemplo, para armazenamento da arte do jogo, que muitas vezes pode ter vários gigas, o [DropBox](http://dropbox.com "DropBox") pode ser pequeno e lento demais. Neste caso, é recomendado a utilização de um servidor local com dois HDs grandes em RAID 1, para garantir que os dados não sejam perdidos, além de backups de segurança em algum HD externo ou PC. Isso pode parecer exagero, ou um pouco demais para um simples projeto, mas acredite: é melhor ser organizado e prevenido do que perder dias, semanas ou meses de trabalho.

Além da arte, os arquivos de som podem ser grandes demais para serem armazenados no DropBox, por isso vale a pena guardar apenas documentos do projeto lá. O código-fonte sempre deverá ficar em um local seguro e de fácil acesso, como o [GitHub](http://github.com "GitHub") ou [BitBucket](http://bitbucket.org "BitBucket"). Para não peder muito tempo com os arquivos de arte e som, eu recomendo armazenar junto com o código-fonte apenas os arquivos finais, como um arquivo PNG, e armazenar os fontes em algum lugar como foi sugerido no parágrafo anterior, como um arquivo PSD que gerou o PNG.

É sempre bom ter alguns backups locais, em caso de precisar acessar rapidamente os arquivos mesmo sem conexão com a internet, mas lembre-se de que se algo acontecer com o seu computador, seu trabalho poderá ser perdido se não estiver em um local seguro. Por esse motivo, eu utilizo o DropBox para arquivos, BitBucket para código-fonte, e todo o resto deixo em um HD externo. Pouca coisa fica apenas no meu computador, o que é bom pois eu posso acessar qualquer coisa ao mesmo tempo em qualquer computador, sem precisar de um pendrive ou compartilhar na rede.

Espero que vocês tenham gostado desta série, nunca é tarde para organizar um projeto! Não importante o tamanho do seu projeto, na verdade nem importa se é um jogo, o importante é cuidar bem e organizar tudo que foi desenvolvido durante o projeto.


