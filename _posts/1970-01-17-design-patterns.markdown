---
layout: post
title: 'Como ser um programador de jogos: Design Patterns'
date: 1970-01-17 09:25:50.000000000 -03:00
---

Este é um assunto complicado até para quem decorou todos [design patterns](http://en.wikipedia.org/wiki/Software_design_pattern "Design Patterns") possíveis e imagináveis em programação. Por mais que existem muitos por ai, poucos são utilizados no dia-a-dia, e muitas vezes por falta de conhecimento.

Antes de começar a trabalhar com jogos eu imaginava que muitos design patterns eram utilizados nos jogos, afinal são programas bem complexos e grandes. Porém, o que eu aprendi é que nem sempre é necessário utilizar todas as técnicas possíveis só para dizer que utilizou.

Em praticamente todos jogos que trabalhei na [Glu](http://glu.com "Glu") e na [EA](http://ea.com "EA") o design pattern mais utilizado era sempre o [Singleton](http://en.wikipedia.org/wiki/Singleton_pattern "Singleton"). Praticamente todas as classes que não eram objectos ou entidades tinham este padrão implementado que tem como objetivo expor uma variável estática para acessar todo conteúdo da classe.

É claro que aqui e ali se via alguns outros design patterns, como [Factory](http://en.wikipedia.org/wiki/Factory_method_pattern "Factory") e [Prototype](http://en.wikipedia.org/wiki/Prototype_pattern "Prototype"), mas o mais utilizado sem dúvidas era o Singleton, por que funciona muito bem quando você precisa acessar conteúdos de outras classes. É importante conhecer alguns design patterns mais utilizados, mas também saber onde e quando utilizar.

Não adianta implementar todos design patterns só para falar que utilizou todos se os demais programadores da equipe (ou futuros programadores) não vão manter tudo funcionando, principalmente por falta de conhecimento. Por isso é muito importante conhecer bem os mais utilizados e pelo menos saber onde utilizar. Para estudar mais sobre design patterns eu recomendo os 3 livros abaixo:

- [Game Programming Patterns](http://www.amazon.com/Game-Programming-Patterns-Robert-Nystrom/dp/0990582906/ref=sr_1_1?ie=UTF8&qid=1427148769&sr=8-1&keywords=game+design+patterns "Amazon")*
- [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/ref=sr_1_1?ie=UTF8&qid=1427149751&sr=8-1&keywords=design+patterns "Amazon")
- [Code Complete: A Practical Handbook of Software Construction](http://www.amazon.com/Code-Complete-Practical-Handbook-Construction/dp/0735619670/ref=sr_1_1?ie=UTF8&qid=1427149756&sr=8-1&keywords=code+complete "Amazon")

* Este livro possui uma [Game Programming Patterns](http://gameprogrammingpatterns.com/contents.html) (o autor começou o link na internet e depois publico a versão impressa). Obrigado Gabriel Sussumu por lembrar deste link nos comentários!

**UPDATE 1:** Links de mais conteúdo de Design Patterns em jogos enviado pelo leitor Fernando Mondo:

- [FSM (Máquina de Estados) em jogos RTS](https://sofiaia.wordpress.com/2008/07/11/maquina-de-estados/)
- [Composite em jogos RPG](http://gamedevelopment.tutsplus.com/tutorials/using-the-composite-design-pattern-for-an-rpg-attributes-system--gamedev-243)
- [Site Universidade da Pennsylvania](http://www.cse.lehigh.edu/~munoz/CSE348/classes/)

**UPDATE 2:** Reescrevi algumas partes do texto para tentar expressar melhor minha opinião.


