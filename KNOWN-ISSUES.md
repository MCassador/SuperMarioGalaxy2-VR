# Problemas conhecidos

- **Versão beta.** Foi testada por uma pessoa só; algumas fases e formas do Mario ainda não foram testadas ou estão em ajuste.
- **Gráficos do pacote completo:** a resolução interna vem em 6× (a do autor, em uma placa potente). Se o FPS ficar baixo, reduza em *Gráficos → Aprimoramentos → Resolução interna*.
- **Pacote completo = Dolphin portátil:** ele não importa as configurações do Dolphin que você já tem (de propósito); usa só a pasta `User` dele. Os seus jogos e saves antigos não aparecem lá até você adicionar a pasta do jogo e copiar o save, se quiser.
- **Programas de geração de quadros e outras camadas OpenXR de terceiros** (por exemplo o OFXR Bridge) podem derrubar o Dolphin ao iniciar o jogo (queda sem mensagem logo depois de "Requesting API version" no `dolphin.log`). Desligue o programa ou coloque `Dolphin.exe` na lista de processos excluídos dele.
- **Cópias antigas da camada** (as versões do Galaxy 1 anteriores a este pacote) não têm a trava contra duas cópias carregadas ao mesmo tempo. Se você tem uma delas registrada, o instalador deste pacote a retira do registro; evite reinstalar o zip antigo depois.
- **Só a versão americana** do jogo (SB4E01).
- **Velocidade do jogo e FPS.** O Galaxy avança um passo por quadro. O mod mantém o jogo em 60 passos por segundo em 72, 90, 100 e 120 quadros (opção *Velocidade do jogo em FPS alto*, padrão *Normal*), medindo a taxa real; entre 61 e 119 quadros o mundo repete um quadro de vez em quando (60 e 120 não têm esse tranco). Se o FPS cair abaixo de 60 o jogo fica em câmera lenta, e o óculos limita a taxa ao Hz dele (72 Hz = no máximo uns 72 quadros). Com *Acelera com o FPS* o jogo roda 1,2×, 1,5×, 1,7× ou 2× mais rápido.
  Testado só em 65 a 72 quadros por segundo; 90 e 120 de verdade ainda não foram testados.
- **Formas do Mario:** Mario normal, Abelha e Pedra têm corpo e luvas em primeira pessoa. Nuvem, Fantasma/Boo, Mola, Fogo/Gelo e Tornado estão em ajuste: o corpo pode aparecer de um jeito estranho.
- **Câmera 200 e terceira pessoa** foram menos ajustadas que a primeira pessoa e têm menos FPS (o jogo desenha uma área maior).
- **Cinemáticas e vídeos** podem ter pequenos erros de enquadramento.
- **Voos e transformações** (águia, Yoshi, casco, patinação) já têm câmera própria, mas ainda podem ter momentos em que o corpo passa na frente da câmera; conte como foi enviando o `smgvr.log`.
- **Rastreamento de mãos** está no começo: o dedo escolhe a pose da luva (aberta, fechada, apontando...), mas os dedos ainda não se mexem um a um.
- **Room scale automático:** se você se inclinar mais de 25 cm e ficar parado ali, a câmera passa a considerar aquele lugar como o novo centro. Dá para desligar em *Centralizar sozinho*.
- **Livro do prólogo escondido:** a caixa branca pode aparecer por uma fração de segundo quando o livro surge, antes de o mod achá-lo (até uns 0,2 s).
- **Braços em poses extremas:** com a mão muito esticada para longe do corpo a luva pode ficar um pouco antes do controle (até uns 15 a 35 cm); nas cenas com o Mario longe da câmera os braços são os do jogo e não seguem os controles.
- **Altura ao sentar e levantar:** o ajuste leva cerca de 1 s depois que você para; durante esse tempo a câmera fica mais baixa ou mais alta que o Mario.
- **Mod em desenvolvimento.** Se encontrar algo, envie o `smgvr.log` e diga o que estava fazendo.
