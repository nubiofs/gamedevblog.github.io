---
layout: post
title: 'Final Frontier: Câmera e controle'
---

No último [post](http://gamedeveloper.com.br/final-frontier-skybox-e-mais-destruicao/) deste série sobre o desenvolvimento do meu jogo [Final Frontier](http://gamedeveloper.com.br/tag/final-frontier/) falei sobre o novo skybox e melhorei a destruição da caixa que representa um asteroide. Desta vez trabalhei em melhorias para a câmera e o controle da nave, além de alterar novamente o skybox e adicionar um planeta.

**Um planeta na galáxia**

Um skybox adiciona detalhes incríveis ao jogo, e muitas vezes o jogador não repara na arte que está acima de suas cabeças. O mapa da Lua no jogo [Destiny](https://www.destinythegame.com/) tem um skybox incrível, com a Terra e a ISS destruída em destaque no céu.

Eu decidi mudar o skybox para outra opção do mesmo asset pack, desta vez com uma névoa verde que adiciona mais detalhes. Também adicionei um novo asset pack gratuito chamado [Vast Outer Space](https://www.assetstore.unity3d.com/en/#!/content/38913), que contém modelos de planetas, asteroides e algumas partículas. Adicionei o planeta abaixo, ele parece próximo mas está bem longe e aumentei o modelo 1000 vezes. Também alterei o `Clipping Planes` da câmera, aumentando o `Far` para 10000, assim o planeta aparece ao fundo mesmo estando bem longe.

![](/content/images/2016/08/planeta-novo.jpg)

**Pilotando a nave**

Até então o controle da nave era algo temporário, até mesmo para um quase protótipo. Decidi pesquisar como eu gostaria que o controle da minha nave fosse, e usei como referência alguns jogos que gostava de jogar no Nintendo 64 e Playstation 2. Estava em dúvida entre: [Star Fox 64](https://www.youtube.com/watch?v=GhQp8le67Xo), onde a a câmera fica fixa seguindo a nave; [Star Wars Rogue Squadron](https://www.youtube.com/watch?v=V0zjmj4rf3U), onde o jogador tem mais liberdade porém com variação de zoom na nave; Star Wars Starfighter (video abaixo), onde encontrei a melhor referência para o que eu quero fazer no Final Frontier.

<iframe width="640" height="360" src="https://www.youtube.com/embed/fv4e_vvwY6c" frameborder="0" allowfullscreen></iframe>

Eu poderia modificar o código que fiz para a movimentação da nave, adicionando ainda mais linhas de código, mas decidi pesquisar outras maneiras de controlar a nave. Mesmo sendo um código temporário, muitas linhas de código podem dificultar implementar novas features, portanto decidi melhorar esta parte do código. Usei como referência o video abaixo, que ensina a fazer um jogo simples de pilotar aviões.

<iframe width="640" height="360" src="https://www.youtube.com/embed/lCulq9J0Y9E" frameborder="0" allowfullscreen></iframe>

O resultado final, que foi uma mistura do que eu tinha feito com novas coisas do video acima, ficou bem melhor do que eu esperava. Além dos direcionais do teclado agora também é possível controlar usando um controle conectado ao computador, testei com o Xbox 360 Controller for Windows e o Steam Controller. Para deixar o tiro mais simples e reduzir uma verificação no código adicionei o botão `space` como um trigger para o botão `Fire1` no `Input Manager` (Edit > Project Settings > Input).

![](/content/images/2016/08/input-manager.jpg)

**Câmera**

Na versão anterior do controle da nave a câmera estava dentro do prefab da nave, o que dava a impressão de uma câmera dura seguindo a nave. Como alterei o controle, foi natural também adaptar a câmera para esta nova situação. Decidi tentar usar o [LookAt](https://docs.unity3d.com/ScriptReference/Transform.LookAt.html) como é mostrado no video acima, mas não funcionou muito bem no meu caso, pois quando a nave dava um loop a câmera girava e ficava de cabeça para baixo.

![](/content/images/2016/08/nave-erro-camera.jpg)

Meu erro foi assumir que tudo do video acima funcionaria no meu caso, porém a câmera tem um comportamento diferente, então removi o `LookAt` e fiz a rotação da câmera ser a mesma da nave, o que ficou exatamente como eu queria. Ajustei a distância da câmera adicionando um offset no script, assim ela ficou um pouco mais afastada, além de dar um efeito legal ao rodar o jogo (a nave sai de trás da câmera e vai para o local do offset).

![](/content/images/2016/08/ff-camera.jpg)

**Próximos passos**

Agora que a movimentação da nave está melhor vou começar a trabalhar em uma mira na tela, para o jogador saber onde está atirando, e vou substituir a caixa branca por um modelo de asteroide. Provavelmente vou dar uma pesquisada em algum efeito de partícula para a nave e os tiros, substituindo as bolas brancas por algo que faça mais sentido ser atirado por uma nave no espaço.

O andamento do projeto pode ser conferido no [GitHub](https://github.com/cicanci/game-unity-ff) e neste [link](https://github.com/cicanci/game-unity-ff/tree/3e8ab71d0ae3410b50dac9e7873c48aa0e0e0b4a) você pode ver as alterações no projeto até este post. Todos os posts desta série sobre meu projeto podem ser vistos na tag [Final Frontier](http://gamedeveloper.com.br/tag/final-frontier/), e como sempre qualquer sugestão ou opinião é bem vinda!
