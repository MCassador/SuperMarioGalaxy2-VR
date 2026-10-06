# Problemas conhecidos

- **Versão beta.** Foi testada por uma pessoa só; algumas fases e formas do Mario ainda não foram testadas ou estão em ajuste.
- **Gráficos do pacote completo:** a resolução interna vem em 6× (a do autor, em uma placa potente). Se o FPS ficar baixo, reduza em *Gráficos → Aprimoramentos → Resolução interna*.
- **Pacote completo = Dolphin portátil:** ele não importa as configurações do Dolphin que você já tem (de propósito); usa só a pasta `User` dele. Os seus jogos e saves antigos não aparecem lá até você adicionar a pasta do jogo e copiar o save, se quiser.
- **Programas de geração de quadros e outras camadas OpenXR de terceiros** (por exemplo o OFXR Bridge) podem derrubar o Dolphin ao iniciar o jogo (queda sem mensagem logo depois de "Requesting API version" no `dolphin.log`). Desligue o programa ou coloque `Dolphin.exe` na lista de processos excluídos dele.
- **Cópias antigas da camada** (as versões do Galaxy 1 anteriores a este pacote) não têm a trava contra duas cópias carregadas ao mesmo tempo. Se você tem uma delas registrada, o instalador deste pacote a retira do registro; evite reinstalar o zip antigo depois.
- **Só a versão americana** do jogo (SB4E01).
- **Velocidade do jogo = FPS.** O Galaxy avança um passo por quadro. Em 90 FPS ele roda 1,5× mais rápido e, se o FPS cai, fica em câmera lenta.
  O pacote vem em 60 quadros para ter velocidade normal. Se o seu PC não segurar 60, o jogo fica um pouco mais lento nos trechos pesados.
- **Formas do Mario:** Mario normal, Abelha e Pedra têm corpo e luvas em primeira pessoa. Nuvem, Fantasma/Boo, Mola, Fogo/Gelo e Tornado estão em ajuste: o corpo pode aparecer de um jeito estranho.
- **Câmera 200 e terceira pessoa** foram menos ajustadas que a primeira pessoa e têm menos FPS (o jogo desenha uma área maior).
- **Cinemáticas e vídeos** podem ter pequenos erros de enquadramento.
- **Voos e transformações** (águia, Yoshi, casco, patinação) já têm câmera própria, mas ainda podem ter momentos em que o corpo passa na frente da câmera; conte como foi enviando o `smgvr.log`.
- **Rastreamento de mãos** está no começo: o dedo escolhe a pose da luva (aberta, fechada, apontando...), mas os dedos ainda não se mexem um a um.
- **Room scale automático:** se você se inclinar mais de 25 cm e ficar parado ali, a câmera passa a considerar aquele lugar como o novo centro. Dá para desligar em *Centralizar sozinho*.
- **Mod em desenvolvimento.** Se encontrar algo, envie o `smgvr.log` e diga o que estava fazendo.
