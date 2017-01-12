---
layout: post
title: Melhores práticas para 2D na Unity - Parte 2
date: 1970-01-17 11:41:13.000000000 -03:00
---
Não esperava demorar praticamente 9 meses para escrever esta segunda parte, mas acabou ficando de lado por ser um conteúdo mais longo que o normal para o blog. Eu até prefiro escrever mais posts assim, e acredito que deve ajudar bastante, por isso vou tentar fazer algo assim pelo menos uma vez por mês (não só sobre a Unity). Se você ainda não viu, recomendo ler a [parte 1](http://gamedeveloper.com.br/melhores-praticas-2d-unity-parte-1/) antes de continuar neste post.

**Boas práticas usando NGUI**

Quando desenvolvi o jogo que mencionei na [parte 1](http://gamedeveloper.com.br/melhores-praticas-2d-unity-parte-1/) a GUI da Unity estava em beta, por isso acabamos comprando e usando o plugin [NGUI: Next-Gen UI](https://www.assetstore.unity3d.com/en/#!/content/2413). Este plugin ficou muito famoso pois tornou possível a criação de interface e até jogos 2D utilizando a Unity, que até então não tinha suporte para ambos nativamente.

Hoje o cenário é bem diferente, porém quase tudo que era feito na NGUI também se aplica aos recursos da Unity. A palavra "quase" é devido aos recursos disponíveis na classe NGUITools, que muitas vezes te ajudam demais no desenvolvimento. Eu particularmente utilizei muito os métodos `SetActive` e `AddChild`, junto com os componentes da NGUI.

Um dos grandes recursos da NGUI é fazer toda UI ter apenas um draw call, ou seja, ser desenhada em uma única chamada. Eu recomendo assistir aos videos desta [playlist](https://www.youtube.com/playlist?list=PLI_jd5nXafTbBrubTmgbodCtWY6BhVxtP) do criador da NGUI (em Inglês), ele fez tutoriais cobrindo todo básico necessário para utilizar o plugin seguindo as boas práticas e otimizando seu jogo. O vídeo abaixo é o número 2 de 5, e cobre o básico.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe width="560" height="315" src="https://www.youtube.com/embed/aWZaq1eLqyE" frameborder="0" allowfullscreen></iframe></span>

Eu tive um grande problema com este plugin: era praticamente impossível migrar o projeto da Unity 4 para Unity 5 sem ter que refazer boa parte da interface. Por este motivo decidimos continuar utilizando a Unity 4. Eu sei que outros desenvolvedores passaram pela mesma situação, e muitos utilizam Unity 4 até hoje por que não tiveram tempo de migrar a NGUI. Mas, ao mesmo tempo, conheço gente que não teve problemas em migrar para Unity 5. Mesmo com estes problemas eu acho que vale a pena utilizar NGUI, pois é um plugin incrível com muito conteúdo disponível. 

Se você está se perguntando se deveria comprar o plugin NGUI por $95 dólares ou utilizar os recursos da Unity minha sugestão é a seguinte: se você já comprou a NGUI, e tem experiência com ela, continue utilizando mas não deixe de estudar os recursos da Unity. Se você ainda não comprou, primeiro estude os recursos da Unity antes de tomar a decisão de comprar, pois isso pode te economizar $95 dólares. 

**Seu melhor amigo, o sprite sheet**

Um sprite é image imagem solitária, e seu jogo pode ter várias imagens assim. Quando você combina vários sprites em uma única imagem, isto é chamado sprite sheet. Existem tantos benefícios por utilizar isto que é praticamente uma boa prática obrigatória para jogos 2D. 

No primeiro video abaixo (em Inglês) podemos ver as vantagens relacionadas ao tamanho e redução de cores para deixar seus assets mais leves e reduzir o consumo de memória. O segundo video explica a importância de usar sprite sheets para otimizar o tempo do OpenGL para carregar e desenhar imagens na tela. 

<span class="embed-youtube" style="text-align:center; display: block;"><iframe width="560" height="315" src="https://www.youtube.com/embed/crrFUYabm6E" frameborder="0" allowfullscreen></iframe></span>

<span class="embed-youtube" style="text-align:center; display: block;"><iframe width="560" height="315" src="https://www.youtube.com/embed/_KyUqyS5MLA" frameborder="0" allowfullscreen></iframe></span>

Sem dúvidas é um ganho enorme se preocupar em organizar os assets do seu jogo em um único sprite sheet. Porém, devemos levar em conta as limitações de hardware das plataformas que estamos desenvolvendo. Em muitos aparelhos Android e iOS antigos o sprite sheet não deve ter mais do que 1024. O 2048 é um tamanho mais recomendado para que funcione na maioria dos aparelhos, mas 4096 funciona bem em praticamente todos hardwares mais recentes. Lembre-se que o sprite sheet deve sempre ter o tamanho em POT (power of two, ou potência de dois), pois se não for o OpenGL vai fazer sua imagem ser na hora que carregar na memória, o que consome mais espaço e recurso do processador.

Os dois videos foram feitos pelo autor do [TexturePacker](https://www.codeandweb.com/texturepacker), um excelente software para gerar sprite sheets e que é compatível com qualquer game engine ou framework com suporte 2D. O site também possui excelentes [tutoriais](https://www.codeandweb.com/texturepacker/tutorials) para as principais tecnologias, tudo em Inglês.

No caso da Unity é necessário utilizar o plugin gratuito chamado [TexturePacker Importer](https://www.assetstore.unity3d.com/en/#!/content/16641). Eu utilizei o TexturePacker e o plugin junto com a NGUI no projeto que mencionei na [parte 1](http://gamedeveloper.com.br/melhores-praticas-2d-unity-parte-1/), e os ganhos de consumo de memória e tamanho da build foram boa partes graças ao uso de sprite sheets, junto com as outras coisas mencionadas.

Internamente a Unity agrupa suas imagens em uma sprite sheet na hora que seu jogo compilado, então mesmo se você não quiser ter este trabalho de preparar tudo antes a Unity faz pra você. Porém, é bom ter o controle disso, pois muitas otimizações mencionadas aqui devem ser feitas manualmente para se ter um ganho de memória na Unity.

Esta foi a parte 2! Na próxima e, provavelmente, última parte vou comentar sobre melhores práticas relacionadas à programação na Unity em C#. O foco não será a linguagem de programação, mas sim sobre a utilização dos recursos de script engine. Qualquer dúvida ou sugestão deixe seu comentário abaixo!
