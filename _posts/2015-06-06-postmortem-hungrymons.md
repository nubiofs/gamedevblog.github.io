---
layout: post
title: 'Postmortem: Hungrymons'
---

Há alguns meses um amigo conversou comigo e disse que queria começar a desenvolver jogos. Hoje, algum tempo depois, ele e seu amigo formaram um estúdio de jogos independentes e lançaram seu primeiro jogo para dispositivos móveis.

Fico muito feliz por terem publicado o jogo e por contar neste postmortem um pouco sobre o projeto, o que deu errado e o que deu certo durante seu desenvolvimento.

> # POSTMORTEM HUNGRYMONS
>
> por Marcelo Vitoria e João Arthur Navarro
>
>
> ## 1) INTRODUÇÃO
>
> Hungrymons é um game casual para iOS e Android. Nele, um robô flutuante (HungryBot) arremessa comidas no ar em diferentes direções, e o jogador precisa mover os monstros (Hungrymons) na tela na direção das comidas para alimentá-los, ganhando pontos por isso. O objetivo é fazer a maior quantidade de pontos possível. O jogador perde quando ele fica sem monstros para alimentar, sendo contabilizada a pontuação final.
>
> O game foi desenvolvido por mim e por meu amigo e sócio João Arthur Navarro, sob a alcunha de CodeRogue Studio. Este é o nosso primeiro projeto, e o tempo total de desenvolvimento foi de 9 meses, entre Julho de 2014 e Março de 2015, tendo o game sido publicado nas app stores em Abril de 2015.
>
>
> ## 2) DETALHES DO GAMEPLAY
>
> O jogador só precisa tocar no monstro e mover horizontalmente na direção das comidas lançadas. Com o tempo, a quantidade de comidas vai aumentando, assim como a velocidade com que elas são arremessadas, além de serem introduzidos elementos que não podem ser ingeridos, como frascos de veneno, que impedem o monstro de comer, e bombas, que eliminam o monstro imediatamente. Além disso, é possível realizar combos que multiplicam a pontuação, e controlar dois monstros ao mesmo tempo.
>
>
> ## 3) PROPOSTA
>
> A idéia era fazer um game casual para plataformas mobile, com controles simples, objetivo claro, e que pudesse ser jogado em sessões curtas, de um a três minutos.
>
>
> ## 4) O QUE DEU CERTO?
>
> ### **4.1 Engine**
>
> Utilizamos o Corona SDK como plataforma de desenvolvimento, o que aumentou nossa produtividade e possibilitou que testássemos nossas decisões de design de forma rápida e objetiva. Além disso, o fato de podermos utilizar o mesmo código para ambos os SOs facilitou a escolha por esta engine, já que ela lida muito bem com as diferentes resoluções e tamanhos de tela (principalmente no Android).
>
> ### **4.2 Perfis dos desenvolvedores**
>
> No time tínhamos um programador e um designer, e essa divisão clara de responsabilidades e habilidades foi de grande valia durante todo o processo de desenvolvimento, e garantiu que cada um tivesse que se preocupar quase que única e exclusivamente com uma dessas duas tarefas. Isso ajudou a manter o foco, e fez com que o resultado final ficasse um pouco acima das nossas expectativas iniciais.
>
> ### **4.3 Comunicação**
>
> Como todos sabem, a comunicação eficiente, o debate e a rápida resolução de conflitos são pontos importantíssimos em qualquer equipe, de qualquer tamanho. Durante o processo de desenvolvimento, as dúvidas, idéias e problemas eram compartilhados, discutidos, e o consenso era alcançado sem desgaste. O fato de não termos um deadline para entrega, ou comprometimento com terceiros, contribuiu para a harmonia e a fácil comunicação.
>
>
> ## <span style="font-size: 35px; font-weight: bold; line-height: 1.2308;">5) O QUE DEU ERRADO?</span>
>
> ### **5.1 GDD (e a falta dele)**
>
> Mesmo sendo um game pequeno, com poucas mecânicas, controles e game design simples, houve momentos em que estávamos em um ponto avançado do desenvolvimento e nos deparamos com dúvidas e dilemas sobre algum aspecto do game que, se devidamente documentados, teria nos poupado tempo e evitado o desvio de foco.
>
> A falta de um GDD evidenciou que não tínhamos pensado como queríamos que tudo funcionasse, desde o inicio. Nós tínhamos um conceito inicial em mente, basicamente relacionado ao gameplay, e trabalhamos em torno disso para que todo o resto atendesse a ideia principal. Entendo que, mesmo que tivéssemos um documento, ele também seria alterado eventualmente, e evoluiria para o que se tornou o produto final, mas a presença dele serve de direção para o trabalho realizado, e te faz pensar em todos os aspectos do game antecipadamente, definindo um ponto de referência para futuras discussões.
>
> ### **5.2 Planejamento**
>
> O game foi desenvolvido inteiramente em nosso tempo livre, concorrendo com trabalho em tempo integral, relacionamento, família, etc. Nessas situações, é imprescindível que haja um planejamento das atividades de acordo com estimativas (mesmo que superficiais), e um controle rígido do tempo gasto no projeto. Nós não nos planejamos devidamente para o projeto em nenhum dos aspectos mencionados.
>
> Como não tínhamos um documento que guiasse o desenvolvimento, muitas vezes o trabalho era paralisado até que se pudesse discutir algum ponto importante ou tomar decisões sobre qual caminho seguir. Não tivemos um calendário definido de reuniões iniciais, e essas discussões muitas vezes causava retrabalho.
>
> O uso de ferramentas de controle de atividades, como Trello, minimizou o impacto na produtividade, mas entendo que, se tivesse havido um melhor planejamento, teríamos feito mais em menos tempo.
>
> ### **5.3 Poucas features**
>
> Sem dúvida, não conseguimos colocar no game tudo o que gostaríamos, como animações mais elaboradas, diferentes cenários, mini games, mais personagens, tutorial interativo, trilha sonora personalizada, e muito mais.
>
> A verdade é que o projeto demorou bem mais do que imaginávamos, e tivemos que deixar muitas coisas de lado para garantir que tivéssemos no resultado final os conceitos principais, e não estendêssemos ainda mais o tempo de desenvolvimento.
>
>
> ## 6) CONCLUSÃO
>
> Por ser nosso primeiro projeto, naturalmente enfrentamos muitas dificuldades durante o processo: falta de planejamento e documentação, curva de aprendizado da engine escolhida, dificuldade de conciliar as atividades do dia-a-dia com o tempo dedicado ao projeto, e diversas outras coisas.
>
> Olhando para o produto final, podemos dizer que ficamos satisfeitos com o resultado, que condiz com a proposta inicial, com um conceito aderente às plataformas escolhidas, e um nível de “polimento” razoável, que não faz frente à grandes estúdios do mercado, mas nos deixou orgulhosos por termos começado com o pé direito.
>
> Claro que gostaríamos de ter feito muito mais, mas conseguimos manter o foco no objetivo de fazer nosso primeiro game da melhor forma possível em um tempo aceitável. Muitos desenvolvedores cometem o “erro” de começar com projetos muito grandes, sem passar por experiências intermediarias que lhes dêem confiança e tempo para acumular as habilidades necessárias para criar games cada vez melhores. Felizmente, conseguimos fugir desse estigma e começar bem, com um sentimento de satisfação pessoal, e vontade de fazer muito mais!
>
>
> ## 7) DADOS
>
> **Desenvolvedor**:
>
> CodeRogue Studio ([http://www.coderoguestudio.com/](http://www.coderoguestudio.com/));
>
> **Plataformas**:
>
> - iOS:[ https://itun.es/i6Lh3sB](https://itun.es/i6Lh3sB)
> - Android:[ http://goo.gl/xX3GFu](http://goo.gl/xX3GFu)
>
> **Time**:
>
> - Marcelo Vitoria (@MarcVit [[https://twitter.com/marcvit](https://twitter.com/marcvit)]);
> - João Arthur Navarro (@Litsoh_Navarro [[https://twitter.com/litsoh_navarro](https://twitter.com/litsoh_navarro)]);
>
> **Tempo de desenvolvimento**:
>
> 9 meses;
>
> **Ferramentas e Linguagens**:
>
> - Corona SDK (Lua), utilizando Sublime Text;
> - Git e GitHub, controle de versão e repositório de código;
> - Photoshop;
> - Audacity, PremiumBeat.com, OpenGameArt.org;
> - Trello (task manager);

Siga o exemplo do [Marcelo](https://twitter.com/marcvit) e do [João](https://twitter.com/litsoh_navarro) e faça um jogo simples e publique. Pela experiência deles (e de outros desenvolvedores publicados [aqui](http://gamedeveloper.com.br/category/postmortem/)) fica claro que mesmo um jogo simples pode ser complexo de fazer por vários motivos. É muito legal comparar a experiência dos desenvolvedores e ver que as vezes algo que um acerta o outro erra, e isso é bem comum mesmo.

Muito obrigado ao Marcelo e ao João por terem dedicado um tempo em escrever e compartilhar a experiência deles, e parabéns pelo ótimo jogo que desenvolveram e publicaram! Se você já fez um jogo e publicou, e quer compartilhar sua experiência, é só entrar em contato comigo que eu publico seu texto neste seção do blog.
