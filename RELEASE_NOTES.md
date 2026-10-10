# Versão 0.9 beta (MCassador)

Nona versão pública do Super Mario Galaxy 2 VR, sobre o **Dolphin VR Redux de iChris4** (https://github.com/iChris4/dolphinXR).

## Arquivos do release

- **`SuperMarioGalaxy2-VR-v0.9-completo-com-Dolphin.zip`**: Dolphin VR Redux em modo portátil + o mod + as configurações do autor (controles do Quest, gráficos, códigos, cheats). Extrair e rodar `Jogar-SMG2-VR.bat`.
- **`SuperMarioGalaxy2-VR-v0.9.zip`**: só o mod, com instalador (`instalar-smg2-vr.bat`), para quem já tem o Dolphin VR Redux.

## Novidades da 0.9

- **O ponteiro agora acerta de qualquer direção.** A bolinha vermelha já seguia o controle direito para qualquer lado, mas o jogo só aceitava o que você apontava quando você estava de frente para o quadro da HUD. Virado de lado ou de costas, a bolinha ficava certinha em cima do alvo e nada acontecia: o Yoshi não comia o bicho nem a fruta, os fragmentos de estrela não eram pegos e os inimigos não paravam.
  - **Por que acontecia:** a cada quadro, depois que o mod entrega a posição do ponteiro, o jogo ainda pergunta ao Wiimote do Dolphin se ele está apontando para a tela. O Dolphin calcula isso contra a tela plana da HUD, que fica parada na frente da sala; com você virado para outro lado ele respondia "fora da tela", e o jogo desligava o ponteiro antes de testar qualquer alvo.
  - **O que mudou:** enquanto o mod controla o ponteiro, essa resposta do Dolphin é ignorada e o jogo continua usando a posição do mod, de qualquer ângulo. Onde volta o ponteiro normal do jogo (conversas, cenas, pausa, menus e escolhas de Sim/Não) nada muda, e a câmera que gira quando o ponteiro encosta na borda da tela continua como antes.
  - Vem dentro do código *Ponteiro do Yoshi (VR)*, que já vem ligado; não precisa ligar nada.
  - Detalhe técnico: no `updateDpdInfo` do `StarPointerController` (Galaxy 2 americano, SB4E01), o caminho "fora da tela" grava 0 no byte "na tela" do controle; a instrução que carrega esse 0 (`li r0,0` em `0x80499EEC`) passou a chamar uma rotina de 8 instruções que devolve 1 quando o mod está controlando o ponteiro do 1º controle. O resto do caminho mantém a posição do mod.
- Vale na 1ª pessoa e também no Yoshi na câmera 200 e na câmera do jogo.

## Novidades da 0.8 (já vinham antes)

- **Corpo e braços acompanham o seu corpo de verdade:** ao virar o corpo na vida real (até dar a volta inteira) ou esticar os braços, o peito do Mario vira para onde estão as suas mãos e cada braço sai do ombro do lado certo. Antes, de costas para a frente da sala, os braços cruzavam e torciam, e esticar piorava.
- **Room scale na hora:** ao andar, dar um passo ou virar o corpo, a câmera continua em cima do corpo do Mario no mesmo instante (sobra só uma folga de 5 cm para inclinar a cabeça). Antes ela esperava você ficar parado e, sem recentralizar o óculos, às vezes não voltava.
- Montado no Yoshi o corpo continua virado para o lado do Yoshi, como antes.
- **Ponteiro livre:** nas escolhas de Sim/Não volta o ponteiro normal do jogo.

## Novidades da 0.7 (já vinham antes)

- **Ponteiro de estrela livre na 1ª pessoa:** ele segue o controle direito para qualquer lado, também olhando para os lados, para cima ou para trás (antes parava na borda do quadro da HUD). O jogo procura o que você aponta na linha do controle, os fragmentos de estrela saem nessa direção e o mod desenha uma bolinha vermelha na ponta. Em conversas, cenas, pausa e menus volta o ponteiro normal do jogo.
- **HUD no pulso só na 1ª pessoa e só dentro da fase:** o painel não aparece mais nos menus; na câmera 200 e na câmera do jogo volta a HUD original.
- **Câmera 200 e câmera do jogo:** ao levantar, sentar ou dar um passo, a câmera volta para trás do Mario em cerca de um segundo (antes ficava deslocada).

## Novidades da 0.6 (já vinham antes)

- **HUD da fase** (menu do mod, aba **Jogo**): *Fixa (como o jogo)* (padrão), *Segue a cabeça* (vida, moedas, fragmentos e estrelas deslizam para onde você olha) ou *No pulso esquerdo*:
  - **1ª pessoa:** levante a mão esquerda como quem olha um relógio, com as costas da mão para você, e aparece um painel 3D no pulso, uma linha embaixo da outra: Vida, Estrelas, Moedas, Fragmentos e Mario (vidas). Abaixando a mão, ele some.
  - **Câmera 200 e 3ª pessoa:** o mesmo painel fica sempre visível, no canto de baixo à esquerda da visão.
  - Os ícones são os do jogo quando você tem o pacote de texturas HD instalado no Dolphin (`Load\Textures\<ID do jogo>`); sem ele, o painel usa formas simples.

## Novidades da 0.5 (já vinham antes)

- **Yoshi come o que você aponta com o controle direito.** Antes o ponteiro do jogo vinha de uma tela plana do Dolphin e não batia com o que o óculos mostra, então a bolinha vermelha não ficava no bicho.
  - **1ª pessoa:** o ponteiro do jogo segue a direção real do controle.
  - **Câmera 200 e câmera original:** o jogo procura o alvo exatamente na linha do controle, de qualquer ângulo (de lado, para cima, de costas), e o mod desenha a **própria bolinha vermelha** nessa linha, fora do quadrado da HUD. A bolinha do jogo fica escondida enquanto você está no Yoshi.
  - Novo código no jogo: *Ponteiro do Yoshi (VR)* (já vem ligado).
- **Pausa só no botão Menu do controle esquerdo:** na câmera original, empurrar o analógico direito para a esquerda (botão − do Wiimote) abria a pausa. O − não pausa mais.
- **Rastro do braço ao girar a visão:** ao girar com o analógico direito (em passos ou suave) o braço não deixa mais um "vulto" para o lado oposto por um ou dois quadros.

## Novidades da 0.4 (já vinham antes)

- **Giro suave do analógico direito (opcional):** em vez dos passos de 45°, a visão gira de forma contínua enquanto você segura o analógico. Menu, aba **Câmeras**: *Tipo de giro* e *Velocidade do giro suave* (de 45°/s a 180°/s). O padrão continua em passos.
- **Menu em português e inglês:** a primeira linha da aba **Câmeras** é *Idioma / Language*. No primeiro uso o menu segue o idioma do Windows.
- **Corte por distância pausa sozinho** em cenas, conversas e viagens rápidas (Estrela Lançadora, canhão): o planeta para onde você voa e o cenário mostrado nas cenas não somem mais. Fora disso, o corte continua como você configurou.
- **Menu zerado:** os ajustes de câmera (*frente / trás*, *acima / abaixo* e *à frente: andando/pulando*) agora começam em 0; os valores que o autor usava ficam como base por baixo deles. Esses três ajustes mudaram de nome no arquivo de configurações, então **os valores salvos da versão 0.3 não são lidos** e a câmera volta ao padrão do autor.
- **Velocidade do jogo em FPS alto:** o padrão agora é *Acelera com o FPS* (a 60 quadros não muda nada). Para manter 60 passos por segundo em 72, 90, 100 ou 120 quadros, escolha *Normal (60 passos/s)*.

## Novidades da 0.3 (já vinham antes)

- **Corte de objetos mais esperto:** o mod manda o jogo desenhar só o que está na direção para onde você olha (cone de 170°, ajustável em *Corte de objetos*) e, dentro dele, **não desenha o que está além de uma distância** (menu → aba **Jogo** → *Corte por distância*: Longe 300 m, Médio 150 m, **Perto 80 m (padrão)** ou Desligado). Nas fases grandes a maior parte dos objetos está longe da câmera, então isso tira trabalho do Dolphin.
- **Câmera original do jogo com mais FPS:** ela também passou a usar o corte pela cabeça (antes desenhava o cenário inteiro e ficava uns 10 FPS abaixo da primeira pessoa no mesmo lugar).
- **Trocar de câmera sem piscar:** a cabeça, o corpo e as nuvens do chapéu do Mario Nuvem não somem mais por instantes ao trocar de câmera (primeira pessoa, câmera 200, câmera do jogo).
- **Mario Nuvem:** corpo, braços e luvas como no Mario normal em primeira pessoa; as nuvenzinhas do chapéu ficam fora da frente da cabeça e voltam na hora ao sair da primeira pessoa.
- **Braços:** a manga não se torce mais quando você vira o pulso até o fim, e o braço não estica nem se deforma nas cenas em que a mão fica longe.
- **Velocidade do jogo em FPS alto:** o controle ficou mais preciso (acompanha a taxa real e não acumula erro); continua em 60 passos por segundo.
- **Menu novo:** mais largo e mais fácil de ler, com barras, rolagem e títulos de seção.

## Novidades da 0.2 (já vinham antes)

- **Velocidade normal em FPS alto:** a lógica do jogo fica em 60 passos por segundo mesmo com 72, 90, 100 ou 120 quadros (o mod mede a taxa real e se ajusta). A opção *Velocidade do jogo em FPS alto* do menu volta ao comportamento antigo (jogo acelerado).
- **Quadros por segundo:** agora com 60, 72, 90, 100 e 120 no menu (aba **Jogo**), e o menu grava no arquivo que o Dolphin realmente lê, então a escolha passa a valer ao reabrir o jogo.
- **Livro do prólogo:** a página branca do livro de figuras, que flutuava na vista no prólogo e nas primeiras fases, fica escondida (opção *Livro do prólogo*).
- **Braços:** não esticam mais como tubos; nas cenas com o Mario longe da câmera usam os braços do próprio jogo; a manga não "quebra" ao levantar a mão e virar o controle.
- **Room scale:** além de voltar ao corpo quando você vira ou sai do lugar, a **altura** também se ajusta quando você senta ou levanta.
- **Yoshi:** a câmera não desce mais por instantes enquanto você está montado.

## O que já vinha na 0.1

- Primeira pessoa com corpo, braços e luvas do Mario nos controles (Mario normal, Abelha e Pedra).
- Câmera 200 e terceira pessoa; troca pelo clique do analógico direito.
- Menu dentro do óculos (B + Y), com 60, 90 ou 120 quadros por segundo (vale ao reabrir o jogo).
- Sem reflexos e refração de tela, sem faixas pretas de cinema e sem borrão de velocidade.
- Altura da câmera estável e room scale automático (a câmera volta ao corpo quando você vira ou sai do lugar).
- Seções 2D com o analógico esquerdo relativo ao plano e giro do analógico direito em passos.
- Yoshi com a câmera mais alta e acompanhando a cabeça; casco de tartaruga guiado pela cabeça (grip direito atira); águia (Fluzzard) com a câmera acompanhando o voo.
- Balanço, cipó e barras com a câmera acompanhando o corpo.
- Cenas e conversas em primeira pessoa, olhando para onde a cena acontece.
- Nado guiado pela cabeça, patinação no gelo e Mario de Fogo ajustados.
- Pausa com um toque no botão Menu; sons de estrelas e Lumas opcionais.
- Tela de abertura própria.
- **Sem camadas duplicadas:** se duas cópias da camada VR forem carregadas juntas, só a mais nova funciona (antes elas duplicavam o menu e os ajustes da câmera). O `Jogar-SMG2-VR` liga a camada só enquanto o Dolphin está aberto e devolve o registro depois; o instalador nunca troca uma DLL mais nova por uma mais antiga.
- **Primeira vez mais fácil:** o `Jogar-SMG2-VR` abre uma janela para você escolher o seu jogo e depois abre o Dolphin já com ele.

## Padrões desta versão

- Quadros por segundo: **60**.
- Velocidade do jogo em FPS alto: **Acelera com o FPS** (só faz diferença acima de 60 quadros).
- Idioma do menu: o do Windows (português ou inglês).
- Giro do analógico direito: 45°.
- Altura extra no Yoshi: +30.
- Corte de objetos: **Leve (170°)**; corte por distância: **Perto (80 m)**.
- Resolução interna do Dolphin: 6× (a do autor; baixe se a sua placa sofrer).

## Instalação

Veja [INSTALL.md](INSTALL.md).
