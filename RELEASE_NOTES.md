# Versão 0.2 beta (MCassador)

Segunda versão pública do Super Mario Galaxy 2 VR, sobre o **Dolphin VR Redux de iChris4** (https://github.com/iChris4/dolphinXR).

## Arquivos do release

- **`SuperMarioGalaxy2-VR-v0.2-completo-com-Dolphin.zip`**: Dolphin VR Redux em modo portátil + o mod + as configurações do autor (controles do Quest, gráficos, códigos, cheats). Extrair e rodar `Jogar-SMG2-VR.bat`.
- **`SuperMarioGalaxy2-VR-v0.2.zip`**: só o mod, com instalador (`instalar-smg2-vr.bat`), para quem já tem o Dolphin VR Redux.

## Novidades da 0.2

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

- Quadros por segundo: **60** (velocidade normal do jogo).
- Giro do analógico direito: 45°.
- Altura extra no Yoshi: +30.
- Resolução interna do Dolphin: 6× (a do autor; baixe se a sua placa sofrer).

## Instalação

Veja [INSTALL.md](INSTALL.md).
