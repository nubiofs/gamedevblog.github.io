---
layout: post
title: Hello World no Nintendo DS
date: 1970-01-15 08:45:23.000000000 -03:00
---

Há pouco tempo comecei a pesquisar e estudar o **desenvolvimento de jogos para o Nintendo DS**. Poucos estúdios de games têm a licença e o kit oficial para desenvolver jogos comerciais para o Nintendo DS, mas existe uma outra maneira para desenvolver jogos não comerciais, apenas para estudo, também conhecido como **homebrew**.

A maneira que encontrei foi usar a biblioteca libnds e o compilador **devkitARM**, disponíveis no [devkitPro](http://www.devkitpro.org/ "devkitPro"), que foram desenvolvidos por uma comunidade dedicada ao desenvolvimento de homebrews para DS e algumas outras plataformas. Com esta [ferramenta](http://www.coderjoe.net/archive/2007/07/23/nintendo-ds-homebrew-tools-of-the-trade/ "Ferramenta") podemos desenvolver homebrews e rodar no próprio **Nintendo DS** (com R4 ou equivalente) ou em um emulador no PC.

Antes de sair programando, é necessário entender algumas **particularidades do Nintendo DS**. Assim como um celular, o Nintendo DS possui um hardware limitado, porém muito poderoso e com uma [arquitetura](http://dev-scene.com/NDS/Tutorials_Day_2 "Arquitetura DS") incrível, além de muitos recursos para criar diferentes tipos de gameplay. O diagrama abaixo parece complexo, mas não é muito. Entendendo como este hardware funciona, dúvidas e problemas podem ser resolvidos simplesmente olhando para o diagrama, como estouro de memória gráfica, por exemplo.

<figure class="wp-caption aligncenter" id="attachment_120" style="width: 495px">[![Arquitetura do Hardware do Nintendo DS](http://gamedeveloper.com.br/blog/wp-content/uploads/2009/09/dov_ds_memorymap.png "Dov_DS_MemoryMap")](http://dev-scene.com/NDS/Tutorials_Day_2)<figcaption class="wp-caption-text">Arquitetura do Hardware do Nintendo DS</figcaption></figure>A linguagem de programação utilizada é C/C++. Ao baixar e instalar o devkitPro, ele também irá instalar uma IDE para programação, o Programmer’s Notepad, que é praticamente um bloco de notas colorido que compila. Nada contra desenvolver utilizando este software, mas eu prefiro utilizar o Microsoft Visual Studio 2005/2008.

Neste [tutorial](http://www.coderjoe.net/archive/2007/07/30/using-devkitarm-and-libnds-with-visual-studio-2005/ "Visual Studio") é demonstrado como configurar um projeto no Visual Studio 2005 e utilizar o compilador devkitARM – também funciona no Visual Studio 2008. Para completar o ambiente de desenvolvimento, você irá precisar de um emulador de Nintendo DS, pois a configuração deste tutorial permite que ao executar um programa no Visual Studio (F5), além de gerar um arquivo .NDS, este arquivo é carregado em um emulador para testar, incrível não?

**Configuração do meu ambiente de desenvolvimento:**  
 – OS: Windows XP SP3  
 – IDE: [Visual Studio 2005/2008](http://msdn.microsoft.com/pt-br/vstudio/default.aspx "Visual Studio")  
 – Compilador: [devkitARM](http://www.devkitpro.org/downloads/ "devkitPro")  
 – Biblioteca: [libnds](http://libnds.devkitpro.org/ "libnds")  
 – Emulador: [DeSmuMe](http://www.desmume.com/ "DeSmuMe")

Para testar no meu Nintendo DS estou usando o [R4](http://www.r4ds.com/ "R4"). Você só precisa compilar o programa para gerar o .NDS e colocar na micro SD do R4 para funcionar no Nintendo DS. É tão simples quando utilizar um emulador.

É sempre bom **testar **no emulador e no Nintendo DS, pois a emulação do Nintendo DS no computador não é real. Como o emulador esta rodando em cima de uma arquitetura diferente da real, os limites do hardware do Nintendo DS geralmente não são levados em conta.

A libnds possui muitas funções para interagir com o hardware do DS, e todas estão muito bem explicadas e com exemplos neste [link](http://libnds.devkitpro.org "libnds"). Após configurar meu ambiente de desenvolvimento, estudei os exemplos deste link e li os tutoriais abaixo, antes de começar a brincar:

[http://patater.com/files/projects/manual/manual.html](http://patater.com/files/projects/manual/manual.html "Tutorial 1")  
[http://ndsbr.blogspot.com](http://ndsbr.blogspot.com "Tutorial 2")  
[http://dev-scene.com/NDS/Tutorials_Day_1](http://dev-scene.com/NDS/Tutorials_Day_1 "Tutorial 3")  
[http://www.double.co.nz/nintendo_ds](http://www.double.co.nz/nintendo_ds "Tutorial 4")

Para começar a brincadeira, fiz uma programa onde na tela superior do DS aparece um texto e na inferior (touch) existe um quadrado que pode ser controlado com os direcionais ou arrastado utilizando touch. Não é nada muito complexo, estudando os links acima é possível fazer muitas coisas legais, inclusive algum jogo curto ou demo.

<figure class="wp-caption aligncenter" id="attachment_122" style="width: 265px">![Executando no emulador DeSmuMe](http://gamedeveloper.com.br/blog/wp-content/uploads/2009/09/ds_emulador1.jpg "DS_emulador")<figcaption class="wp-caption-text">Executando no emulador DeSmuMe</figcaption></figure><figure class="wp-caption aligncenter" id="attachment_123" style="width: 495px">![Executando no Nintendo DS com R4](../content/images/2009/09/photo0021.jpg "Photo0021")<figcaption class="wp-caption-text">Executando no Nintendo DS com R4</figcaption></figure>[**Clique aqui para baixar o .NDS do meu “Hello World”.**](http://www.gamedeveloper.com.br/cicanci/games/testnds.zip "TestNDS")

No momento estou estudando JME por causa de uma matéria na pós-graduação de Jogos para Celular, e preciso terminar um jogo (que irei postar aqui logo). Quando terminar este projeto pretendo me dedicar um pouco mais à “brincar” com o Nintendo DS. Qualquer dúvida sobre a configuração do ambiente ou sobre a programação para o Nintendo DS é só postar que eu tentarei ajudar!


