# Instalação

## O que você precisa

- Windows 10/11 x64 com uma boa placa de vídeo e o **Microsoft Visual C++ Redistributable 2015-2022 (x64)** (quase todo PC com jogos já tem).
- Meta Quest 3 com Virtual Desktop (ou outro óculos com runtime OpenXR; testado só no Quest 3 com Virtual Desktop).
- A **sua** cópia do Super Mario Galaxy 2, versão americana (SB4E01). As versões europeia e japonesa não funcionam.

Você pode escolher entre as duas formas abaixo.

## Opção A: pacote completo com o Dolphin (recomendado)

Arquivo: **`SuperMarioGalaxy2-VR-v0.7-completo-com-Dolphin.zip`**. Traz o **Dolphin VR Redux** (de [iChris4](https://github.com/iChris4/dolphinXR)) em modo portátil, já com as configurações do autor:
controles do Quest (`WiimoteNew.ini` e o perfil `Mario`), gráficos (`GFX.ini`, resolução interna, ajustes de VR do jogo), cheats ligados, os códigos do jogo e o mod.
Nada é instalado no seu Dolphin atual e as suas configurações atuais não são tocadas: o pacote usa só a pasta dele (`User`).

1. Extraia o zip em uma pasta **sem acentos nem espaços de preferência** (por exemplo `C:\Jogos\SMG2-VR`).
2. Conecte o Quest ao PC (Virtual Desktop, Air Link ou Link).
3. Dê dois cliques em **`Jogar-SMG2-VR.bat`**. É só isso: ele registra a camada VR para o seu usuário (sem pedir administrador), **abre uma janela para você escolher o arquivo do seu Super Mario Galaxy 2**
   (`.wbfs`, `.iso`, `.rvz`...; só na primeira vez) e abre o Dolphin já com o jogo. Das próximas vezes ele abre o mesmo jogo direto.
   Para trocar de jogo: apague o arquivo `User\jogo.txt` ou arraste outro arquivo de jogo em cima do `Jogar-SMG2-VR.bat`.
   **Deixe a janela do `Jogar-SMG2-VR` aberta enquanto joga.** A camada VR só fica ligada no Windows enquanto o Dolphin do pacote está aberto: quando você fecha o Dolphin, a janela desliga a camada, devolve o registro como estava e se fecha sozinha. Nada fica instalado.
   Se o Windows mostrar "O Windows protegeu o computador" (SmartScreen), clique em *Mais informações → Executar assim mesmo*: os arquivos vêm de um zip baixado da internet e não são assinados.

O pacote é **portátil**: pode ficar em qualquer pasta, e para desinstalar basta apagar a pasta (veja "Desinstalar").

## Opção B: só o mod (você já tem o Dolphin VR Redux)

Arquivo: **`SuperMarioGalaxy2-VR-v0.7.zip`**. Requer o **Dolphin VR Redux**, build com OpenXR (ramo *openxr-work*, [releases do iChris4](https://github.com/iChris4/dolphinXR/releases)).

1. Feche o Dolphin.
2. Extraia o pacote em **qualquer pasta**. Só se o seu Dolphin for **portátil** (existe um `portable.txt` ao lado do `Dolphin.exe`) é que o pacote deve ser extraído dentro da pasta do Dolphin.
3. Dê dois cliques em `instalar-smg2-vr.bat`. **Tudo é automático**, não pergunta nada. Ele:
   - acha sozinho a pasta de usuário do Dolphin (portátil, registro, Documentos ou AppData);
   - cria a pasta `Documentos\Dolphin Emulator\SMG-VR` e copia para lá a camada VR e a configuração;
   - registra a camada OpenXR (chave `HKCU\SOFTWARE\Khronos\OpenXR\1\ApiLayers\Implicit`);
   - instala os códigos do jogo (`GameSettings\SB4E01.ini`), os ajustes de VR (`GameSettingsVR\SB4E01.ini`) e os controles;
   - liga os cheats do Dolphin (sem isso os códigos não rodam);
   - guarda cópias de segurança do que substituiu na pasta `Backup` do Dolphin.
4. Conecte o Quest ao PC (Virtual Desktop, Air Link ou Link), abra o Dolphin e inicie o Super Mario Galaxy 2 (versão americana).

A mesma camada (`smgvr_layer.dll`) também serve para o Super Mario Galaxy 1, mas estes pacotes só instalam os códigos do **Galaxy 2**.
Se você já usa o mod do Galaxy 1, a instalação da opção B não mexe nos arquivos dele (`RMGE01`).
**Usando as duas opções no mesmo PC:** pode. A opção A desliga a cópia da opção B só durante o jogo e a devolve no fim. Já o instalador da opção B tira do registro a cópia do pacote da opção A (que se religa sozinha na próxima vez que você usar o `Jogar-SMG2-VR`), e nunca troca uma `smgvr_layer.dll` mais nova por uma mais antiga (por exemplo, ao instalar o zip do Galaxy 1 depois deste). Além disso, se por qualquer motivo duas cópias da camada forem carregadas juntas, só a mais nova funciona e a outra fica fora do caminho.

## Usando

- **Trocar de câmera:** clique do analógico direito (primeira pessoa → câmera 200 → terceira pessoa). A troca só responde depois que o jogo entrou na fase.
- **Menu do mod:** segure **B + Y**. Analógico para cima/baixo escolhe a linha, para os lados troca de aba, A muda o valor.
- **Quadros por segundo:** aba **Jogo** → **Quadros/s** (60, 72, 90, 100 ou 120). Vale ao reabrir o jogo. O jogo continua na velocidade normal (60 passos por segundo) em qualquer valor: a opção **Velocidade do jogo em FPS alto** (mesma aba) pode ser trocada para *Acelera com o FPS* (72 = 1,2×, 90 = 1,5×, 100 = 1,7×, 120 = 2×). O valor que você recebe depende do óculos (o Hz dele) e do PC.
- **Tela de abertura:** a imagem `smgvr-splash.bmp` na pasta `SMG-VR` aparece por alguns segundos ao iniciar. Apague ou troque o arquivo se quiser.
- As opções do mod ficam em `smgvr-menu-smg2.ini` (pasta `SMG-VR`; criado quando você mexe no menu).
- **Gráficos:** o pacote vem com a resolução interna do autor (6×). Se a sua placa de vídeo sofrer, baixe em *Gráficos → Aprimoramentos → Resolução interna*.

## Se algo der errado

Envie estes dois arquivos:

- `smgvr.log` (pasta `SMG-VR`: na opção A fica em `User\SMG-VR`, na B em `Documentos\Dolphin Emulator\SMG-VR`)
- `dolphin.log` (na pasta `Logs` da pasta de usuário do Dolphin: na opção A em `User\Logs`)

## Desinstalar

- **Opção A:** apague a pasta do pacote. Se você fechou a janela do `Jogar-SMG2-VR` à força durante o jogo, o registro pode ter ficado: `reg delete "HKCU\SOFTWARE\Khronos\OpenXR\1\ApiLayers\Implicit" /v "<pasta do pacote>\User\SMG-VR\smgvr_layer.json" /f`.
- **Opção B:** apague a pasta `Documentos\Dolphin Emulator\SMG-VR`, remova a chave de registro com `reg delete "HKCU\SOFTWARE\Khronos\OpenXR\1\ApiLayers\Implicit" /v "%USERPROFILE%\Documents\Dolphin Emulator\SMG-VR\smgvr_layer.json" /f` e, para voltar à configuração anterior, restaure os arquivos da pasta `Backup` da pasta de usuário do Dolphin.
