# Super Mario Galaxy 2 VR

**Versão 0.3 (beta)** · Windows x64 · Dolphin VR Redux · OpenXR · Meta Quest 3 (Virtual Desktop)

O **Super Mario Galaxy 2** (versão americana, SB4E01) em realidade virtual, dentro do **Dolphin VR Redux**:
primeira pessoa com o corpo, os braços e as luvas do Mario nos seus controles, três câmeras e um
menu dentro do óculos.

[Instalação](INSTALL.md) · [Problemas conhecidos](KNOWN-ISSUES.md) · [Créditos](CREDITS.md) · [Notas da versão](RELEASE_NOTES.md)

## Dolphin VR Redux (créditos)

Tudo isto só existe por causa do **Dolphin VR Redux** (DolphinXR), o Dolphin com suporte a VR via OpenXR feito por **iChris4 (Christophe)**:
**https://github.com/iChris4/dolphinXR** (baixe as versões oficiais na [página de releases](https://github.com/iChris4/dolphinXR/releases)).
O Dolphin é um software livre (GPLv2 ou posterior) do Dolphin Emulator Project. O mod daqui é uma camada à parte, feita por MCassador, que roda **em cima** dele.

## Duas formas de baixar (na página de releases)

| Arquivo | Para quem |
| --- | --- |
| **`SuperMarioGalaxy2-VR-v0.3-completo-com-Dolphin.zip`** | Quem quer só extrair e jogar. Já vem com o **Dolphin VR Redux** pronto (modo portátil) e **todas as configurações do autor**: mapeamento dos controles do Quest, gráficos, códigos do jogo e o mod. Você só aponta para o seu jogo. |
| **`SuperMarioGalaxy2-VR-v0.3.zip`** | Quem já tem o Dolphin VR Redux instalado e quer só o mod (instalador automático). |

> **Nenhum dos dois contém o jogo.** Você precisa da sua própria cópia do Super Mario Galaxy 2 (versão americana).
>
> É a versão **beta**: foi feita e testada por uma pessoa só, e várias partes (formas do Mario, voos, cenas) ainda estão em ajuste.
> Veja [KNOWN-ISSUES.md](KNOWN-ISSUES.md).

## As três câmeras

Clique no analógico direito (R3) para trocar, sempre nesta ordem:

| Câmera | Como é |
| --- | --- |
| **Primeira pessoa** | Você vê pelos olhos do Mario. As luvas e os braços seguem os seus controles. |
| **Câmera 200** | Câmera atrás do Mario, horizonte reto, distância ajustável com o analógico direito. |
| **Terceira pessoa** | Segue a câmera do jogo, nivelada, com suavidade ajustável. |

O mapa de mundos e os menus do jogo ficam sempre na câmera original.

## O que o mod faz (por MCassador)

- Corpo, braços e luvas do próprio Mario seguindo os controles (e escolhendo a pose da luva pelos dedos, quando o óculos rastreia as mãos). Funciona no Mario normal e nas formas Abelha e Pedra.
- Menu dentro do óculos: **segure B + Y**. Câmeras, mãos, luvas, giro do analógico direito, quadros por segundo, tamanho do HUD, altura extra no Yoshi e mais.
- Sem os reflexos e a refração de tela que quebram em VR, sem as faixas pretas de cinema nos diálogos e cenas e sem o borrão de velocidade.
- **Altura da câmera estável**: ela fica sempre na mesma posição ao andar, correr e pular. Só muda onde precisa acompanhar o corpo (cipó e barra de balanço, Yoshi, casco, águia).
- **Room scale automático**: se você virar o corpo ou sair do lugar, a câmera volta para o corpo do Mario depois de um instante (opção *Centralizar sozinho* do menu). Se você senta ou levanta e fica ali, a **altura** também se ajusta (menos com *Agachar de verdade* ligado).
- **Seções 2D** (as paredes da Honeybloom e outras): o analógico esquerdo anda ao longo do plano em relação a para onde você olha, e o analógico direito gira a visão em passos (45° por padrão, ajustável).
- **Yoshi**: a câmera sobe um pouco (*Altura extra no Yoshi*) e acompanha a cabeça dele nos pulos e curvas.
- **Braços sempre braços**: o braço não estica mais como um tubo quando a mão fica longe do corpo (a luva pode parar um pouco antes do controle em poses extremas), e nas cenas em que o Mario fica a vários metros da câmera o mod usa os **braços do próprio jogo**, sem o "cone" esticado do peito dele até a sua luva.
- **Livro do prólogo**: a página branca do livro de figuras, que ficava flutuando na frente da vista no prólogo e nas primeiras fases, fica escondida (menu → aba **Jogo** → *Livro do prólogo*; o texto da história continua).
- **Corte de objetos**: só é desenhado o que está na direção para onde você olha (cone de 170°) e, dentro dele, o que está mais perto que **80 m** (menu → aba **Jogo** → *Corte de objetos* e *Corte por distância*: Longe 300 m, Médio 150 m, Perto 80 m ou Desligado). Dá mais FPS nas fases pesadas, inclusive na câmera original do jogo. Se algo distante sumir que não devia, suba para *Longe* ou desligue.
- **Mario Nuvem**: corpo, braços e luvas como o Mario normal; as nuvens do chapéu ficam fora da vista em primeira pessoa e a troca de câmera não faz nada piscar.
- **Casco de tartaruga** (nado debaixo d'água): o casco vira para onde a sua cabeça olha; o **grip direito** atira.
- **Fluzzard (a águia)**: a câmera acompanha a direção do voo, sem o corpo da ave entrar na sua cabeça.
- **Balanço, cipó e barras**: a câmera acompanha o corpo balançando.
- **Cenas e conversas** continuam em primeira pessoa, e a visão gira para onde a cena acontece. A caixa de diálogo fica mais baixa e dá para conversar de mais longe.
- Nado guiado pela cabeça ou pelo controle, patinação no gelo e Mario de Fogo ajustados para primeira pessoa.
- Pausa com um toque no botão Menu do controle esquerdo.
- Dá para desligar o som dos fragmentos de estrela e das Lumas no menu.
- Tela de abertura própria (`smgvr-splash.bmp`, você pode trocar a imagem).

## Dica importante: FPS e velocidade do jogo

O Galaxy conta o tempo em quadros: sozinho, a 90 FPS ele ficaria 50% mais rápido. O mod evita isso: a lógica do jogo fica em **60 passos por segundo** e só o desenho segue a taxa de quadros que o seu PC e o seu óculos entregam (a cabeça é acompanhada a cada quadro). O mod mede a taxa real e se ajusta, então o jogo fica em velocidade normal mesmo quando o FPS oscila (nos testes do autor, 59 a 61 passos por segundo com a tela entre 65 e 72 quadros).
Para escolher a taxa: menu do mod (B + Y) → aba **Jogo** → **Quadros/s** (**60, 72, 90, 100 ou 120**; vale ao reabrir o jogo). O que você de fato recebe depende do óculos e do PC: com o óculos em 72 Hz, por exemplo, o jogo não passa de uns 72 quadros por segundo; 90 ou 120 só ajudam se você subir o Hz do óculos (Virtual Desktop) e a placa de vídeo aguentar.
A opção **Velocidade do jogo em FPS alto** (mesma aba) permite voltar ao comportamento antigo: *Acelera com o FPS* (72 = 1,2×, 90 = 1,5×, 100 = 1,7×, 120 = 2×).
Limite: entre 61 e 119 quadros o mundo repete um quadro de vez em quando (a 60 e a 120 não há esse tranco); a cabeça, as mãos e a imagem continuam suaves. Se o FPS cair abaixo de 60, o jogo fica em câmera lenta, como sempre foi.

## Controles (Quest)

| Wii | Quest |
| --- | --- |
| Analógico (Nunchuk) | analógico esquerdo |
| A | botão A (direito) |
| B | gatilho direito |
| Z / C | gatilho esquerdo / grip esquerdo |
| Trocar de câmera | clique do analógico direito |
| Pausa (+) | botão Menu (esquerdo), toque rápido |
| Giro do Mario | movimento do controle |
| Nado e voo | virar: controle direito ou cabeça (menu); analógico esquerdo: subir e descer |
| Atirar o casco | grip direito |
| Agachar | gatilho esquerdo, ou abaixe a cabeça de verdade |
| Menu do mod | segurar B + Y |

Feito por **MCassador** sobre o Dolphin VR Redux de **iChris4**. Projeto de fã, sem fins lucrativos e sem relação com a Nintendo.
