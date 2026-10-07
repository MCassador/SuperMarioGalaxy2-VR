# Versão 0.4 beta (MCassador)

Quarta versão pública do Super Mario Galaxy 2 VR, sobre o **Dolphin VR Redux de iChris4** (https://github.com/iChris4/dolphinXR).

## Arquivos do release

- **`SuperMarioGalaxy2-VR-v0.4-completo-com-Dolphin.zip`**: Dolphin VR Redux em modo portátil + o mod + as configurações do autor (controles do Quest, gráficos, códigos, cheats). Extrair e rodar `Jogar-SMG2-VR.bat`.
- **`SuperMarioGalaxy2-VR-v0.4.zip`**: só o mod, com instalador (`instalar-smg2-vr.bat`), para quem já tem o Dolphin VR Redux.

## Novidades da 0.4

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
