---
layout: post
title: 'Postmortem: Come On Rio'
date: 1970-01-16 18:09:22.000000000 -03:00
---

As vezes recebo emails de desenvolvedores independentes brasileiros mostrando seus jogos recém lançados, e as vezes perguntam se eu posso divulgar. Como este blog é sobre desenvolvimento de jogos, e também meu portfólio, sempre respondi falando exatamente isso. Até que um dia recebi mais um emails desses, do Bernardo Dias, e dessa vez tive uma ideia diferente, que seria interessante para o blog, e também uma forma de divulgar o jogo: pedi para ele me enviar um postmortem do jogo.

Um postmortem é um documento muito importante de pós-produção, ou seja, é feito após o jogo ter sido lançado. O principal objetivo desse documento é contar as coisas que deram certo e errado, para que todos da equipe possam aprender e melhorar para próximos projetos.

Por ser um documento que tem como objetivo ensinar, e não é “confidencial” como um documento de game design, muitas empresas divulgam esses documentos após o término do projeto. No site [Gamasutra](http://www.gamasutra.com/view/feature/193695/postmortem__sony_santa_monicas_.php "Gamasutra") existem muitos publicados, de empresas gigantes e grupos independentes pequenos. Este é o documento mais incrível que podemos conhecer sobre um jogo, pois nele podemos aprender tudo que foi feito para o jogo ser um sucesso, e tudo que não deu certo.

Para iniciar essa nova categoria aqui no blog, convidei o Bernardo para escrever um postmortem do seu primeiro jogo lançado para Android e iOS, o Come On Rio. O texto abaixo foi escrito por ele, contanto suas experiências e, até mais do que isso, a realização pessoal de fazer um jogo.

> Olá, sou Bernardo Dias, criador de Come On Rio para iOS e Android, um jogo de lógica que tem como tema a cidade do Rio de Janeiro. Estou escrevendo esse artigo para mostrar um pouco do meu primeiro projeto de jogo, como também partilhar um pouco da experiência que pude adquirir e apontar alguns pontos que deram certo e outros que deram errado.
> 
> Primeiramente, acho importante mencionar que se você pretende desenvolver um jogo de maneira independente, esteja preparado para enfrentar dificuldades que se originam em questões completamente divergentes uma da outra, ou seja, o que quero dizer é que, por exemplo, quando a questão financeira estiver te atrapalhando, aparecerá outro problema diferente, como uma parte da programação que não está funcionando como você desejaria, etc.
> 
> É possível pensar depois de ler o parágrafo anterior: “isso é normal e acontece em qualquer tipo de projeto”, ok, mas já parou para pensar em todos esses problemas caindo apenas sobre uma cabeça: a sua, ou então, no máximo na cabeça de cinco ou seis pessoas? É bem complicado… imagina ter que pensar em todo o design do jogo (enredo, GDD, etc), criar toda a arte visual e sonora, a arquitetura e a usabilidade, programar o jogo, corrigir bugs, entre outros, e ainda ter todos esses problemas a sua volta? Isso sem citar os problemas que enfrentamos na vida, no trabalho…
> 
> Outro fator que quero citar é a mudança que o projeto vai sofrer conforme o mesmo for se desenvolvendo, claro que ele não ficará completamente diferente do conceito aplicado inicialmente, porém você terá um projeto bem modificado devido a diversos fatores, como otimização por exemplo. Mas acredite, isso é muito bom porque se trata de um fator essencial no refinamento do projeto, fazendo com que no final você perceba que algumas de suas idéias iniciais eram simplesmente bizarras.
> 
> Para aproveitar o fator das mudanças, citarei algumas que aconteceram na minha experiência de desenvolvimento em Come On Rio através de algumas coisas que deram certo e outras que não foram tão bem assim.
> 
> **• Coisas que deram certo:**
> 
> 1. A realização de um sonho.  
>  Independente do dinheiro ou do sucesso que seu jogo poderá adquirir, acho que nada mais gratificante e importante que você ter uma ideia, trabalhar em cima dela, enfrentar diversos obstáculos para no final, aleluia, você ver o seu jogo disponível para download em todos os continentes do mundo e para milhares de pessoas. Nada mais prazeroso do que estar num local, olhar para o lado e ver uma criança que você não conhece, jogando o seu jogo! Acredito que no final; para o seu primeiro projeto, aquele que vai te colocar dentro do sonho de criar um jogo; não importa se você não ficou milionário com ele ou se ele não fez sucesso mundial, seu jogo não foi um fracasso e sim um vitória! Ele é seu primeiro projeto concluído com êxito que te dará experiência e força para outros futuros projetos.
> 
> 2. Sem qualquer tipo de censura.  
>  Diante de tantos jogos que abordam tiros, sangue, violência ou zumbis, como escolha pessoal, queria que meu primeiro projeto pudesse abordar um tema que não houvesse qualquer tipo de censura, que pudesse ser jogado desde uma criança de sete anos, até uma senhora de sessenta anos sem qualquer tipo de preconceito. No final das contas, percebi que essa ideia principal seguiu ao meu lado até o fim.
> 
> 3. Tema único e originado de uma maneira diferente.  
>  Por vontade própria, eu não queria fazer um jogo clichê de corrida, zumbi ou de arma (apesar de gostar muito de todos esses). Penso que a ideia de um jogo que se passa nos principais pontos turísticos da cidade, presente em Come On Rio, nunca foi utilizada antes. Engraçado que tudo surgiu naquele dia abençoado em que num simples passeio de carro pela cidade, olhando para o maravilhoso Pão de Açúcar à minha esquerda, houve o momento em que uma pessoa que estava comigo definiu a cidade do Rio de Janeiro da melhor maneira que eu já escutei: “o Rio é a cidade mais linda do mundo, pois em nenhum outro lugar há uma harmonia tão grande entre o urbano e a natureza como há nela”. Bem, uniu a vontade de criar um jogo com uma ideia originada a partir de uma definição perfeita para mim: a harmonia entre o urbano e a natureza presente no Rio de Janeiro.
> 
> 4. Se divertir e aprender ao mesmo tempo.  
>  Engajando no ponto citado anteriormente, com o surgimento da ideia de um jogo sobre o Rio de Janeiro, acho que consegui completar outro objetivo que eu tinha para o projeto após a definição do tema. Penso que foi possível fazer as pessoas se divertirem aprendendo, foi possível passar um pouco de cultura e um pouco da cidade de uma maneira diferente.
> 
> **• Coisas que deram errado**
> 
> 1. Vários jogos em um só.  
>  Pois é, a princípio a minha ideia era em que cada ponto turístico que a pessoa acessasse, fosse possível jogar um jogo diferente. Bem, isso era simplesmente inviável por causa de diversos problemas como o tamanho final do jogo, otimização e tempo que o projeto levaria, sem contar o fato de fazer todos esses diversos jogos com atenção e cuidado total. Por isso no final, optei por fazer apenas um e poder dar total atenção, cuidado, vontade, etc a ele.
> 
> 2. Terminar o projeto em meses.  
>  Quando finalmente coloquei a mão para trabalhar em Come On Rio, pretendia termina-lo em alguns meses, porém só consegui finaliza-lo depois de um pouco mais de um ano. Acredite, o seu projeto vai demorar muito mais do que você espera. Você não tem 100% do seu tempo para se dedicar ao jogo pois tem que trabalhar ou estudar, como também você não tem milhões de reais para investir em uma equipe e em uma estrutura que vá acelerar o andamento do projeto.
> 
> 3. Criar o jogo exatamente igual em todas as plataformas em que eu lançasse.  
>  Apesar de não afetar a parte do jogo em si e sim a parte mais informativa de Come On Rio, não foi possível (pelo menos por enquanto) disponibilizar as fotos dos pontos turísticos para o projeto no Android, como é disponibilizado no iOS. Por querer atingir o máximo número de dispositivos Android possíveis, por questão de otimização, foi necessário retirar a parte informativa que mostrava lindas fotos do Rio de Janeiro.
> 
> 4. Ficar rico  
>  Pois é, pelo menos por enquanto eu não fiquei rsrsrsrs. Realmente é extremamente difícil no primeiro projeto, com pouquíssimos recursos, você conseguir captar muito dinheiro com ele. Você não tem fundos para investir em propagandas em diversos lugares e a única coisa que te resta é trabalhar muito, mas muito mesmo, para tornar o seu jogo famoso.
> 
> Como dito no início do artigo, se você conseguir ter uma ideia, trabalhar em cima dela e no final você ver essa sua ideia obtendo êxito, parabéns, você é um vitorioso! Você conseguiu superar todos os obstáculos e está iniciando seu caminho onde você sempre sonhou caminhar: desenvolvendo jogos. Uma vez li um artigo sobre desenvolvimento de jogos onde Chet Faliszek (roteirista de Half-Life 2, Portal e Left 4 Dead) deu a sugestão para quem quer trabalhar com jogos: apenas faça um. Lembro de ter lido que para ele não tem mistério, basta criar um jogo, todo dia que chegar em casa após o seu trabalho, continue o seu projeto, faça isso até que ele fique pronto e depois coloque-o disponível para venda. Eu fiz isso durante meu projeto e acredito realmente que esse seja o segredo e então sigo-o totalmente todos os dias da minha vida.
> 
> Esse foi o meu primeiro projeto onde foi possível adquirir bastante experiência no desenvolvimento de um jogo para em breve começar a lançar uns projetos em 3D usando a Unity ou outra engine que eu venha a me adaptar melhor. Só para concluir, acredite em uma coisa, você não conseguirá criar um projeto totalmente sozinho. Apesar de ter sido eu a colocar toda a mão na massa para criar tudo em Come On Rio, tive ajudas essenciais para o sucesso do mesmo, primeiramente Deus por me dar forças e recuperar minhas energias todos os dias, um grande amigo que me ajudou criando algumas artes e idéias, uma irmã que simplesmente fez um trabalho fenomenal em passar o jogo todo para inglês,familiares apoiando, e outros grandes amigos que foram beta testers por diversas vezes, inclusive alguns da faculdade que paravam de fazer o que estavam fazendo para me ajudar.
> 
> Bem, espero que esse artigo seja útil para quem quer desenvolver um jogo, e que minhas palavras tenham ajudado de alguma maneira. Obrigado a todos e principalmente ao Bruno Cicanci que me deu a excelente ideia de criar esse artigo.
> 
> Quem se interessar em ver como é o jogo, basta baixa-lo gratuitamente nos links abaixo:
> 
> Android: [https://play.google.com/store/apps/details?id=com.brevo.comeonrio](https://play.google.com/store/apps/details?id=com.brevo.comeonrio "Come On Rio")  
>  iPhone/iPod/iPad: [https://itunes.apple.com/br/app/come-on-rio/id595551098?l=pt&ls=1&mt=8](https://itunes.apple.com/br/app/come-on-rio/id595551098?l=pt&ls=1&mt=8 "Come On Rio")
> 
> Página do jogo: [http://www.comeonrio.com](http://www.comeonrio.com "Come On Rio")  
>  Página do facebook: [http://www.facebook.com/comeonrio](http://www.facebook.com/comeonrio "Come On Rio")
> 
> Abraços,  
>  Bernardo Dias

Eu gostei bastante do texto, e o jogo é divertido. Clique nos links acima para baixar, e confira o trailer abaixo. Bernardo, muito obrigado por compartilhar suas experiências e boa sorte nos seus próximos projetos.

<span class="embed-youtube" style="text-align:center; display: block;"><iframe allowfullscreen="true" class="youtube-player" frameborder="0" height="402" src="http://www.youtube.com/embed/wBuJiUFqDS4?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent" type="text/html" width="660"></iframe></span>

A partir de agora, sempre que eu receber algum email de sobre jogos, vou sugerir de fazer um postmortem para ser publicado aqui desta mesma forma. Se você, leitor, tem algum jogo publicado e quer compartilhar suas experiências contanto o que deu certo e errado n seu projeto, envie um email para mim (está em Contato).


