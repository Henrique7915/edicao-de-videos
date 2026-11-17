# Projeto: Reels da noite de pagode no Boteco do Hudson

Este repositório é a memória da edição. Leia este arquivo e `projeto_video_boteco_do_hudson.md` antes de qualquer trabalho.

## Contexto

- Bar pequeno, fechado, noturno, com neon e LED colorido, em Belo Horizonte. Instagram @botecodohudson.
- Entrega: um Reels vertical 9:16, 40 segundos, cerca de 45 cortes.
- O usuário **não vai gravar mais nada**. O material é só o que está na pasta de vídeos e, se faltar algum take, clipes gerados por IA no Google Flow (prompts na seção 5 do projeto).
- Editor: **Kdenlive** (código aberto, Windows). **O Claude faz a edição inteira**, escrevendo o projeto `.kdenlive` (XML do MLT) e renderizando com `melt`. O usuário só assiste aos rascunhos e pede ajustes em texto; abrir o projeto no Kdenlive é opcional.
- Ferramentas necessárias no computador: Kdenlive (traz o `melt`) e ffmpeg.
- Idioma: português do Brasil.

## Arquivos

- Vídeos (fora do repositório, no computador do usuário): `C:\Users\massa\Desktop\Edição vídeo\vídeos_`
  - 29 vídeos do iPhone (IMG_1349 a IMG_1381) e 3 fotos (IMG_1354, IMG_1371, IMG_1372).
  - `521834886_1794872741157857.MP4` pode não ser do evento; confirmar com o usuário.
  - IMG_1358 e IMG_1376 não estão na pasta.
- `projeto_video_boteco_do_hudson.md`: conceito, estrutura de edição segundo a segundo, lista de takes, título de abertura e prompts para o Flow.
- `relatorio_referencias_boteco_do_hudson.md` e `dados_skill/`: pesquisa das referências (ritmo, enquadramento).
- `edicao/`: tudo o que for gerado na edição (inventário, timeline, exports). Criar se não existir.

## Decisões já tomadas

- Abertura: 2 clipes fortes, depois o título **WELCOME / TO / BOTECO DO HUDSON**, uma palavra por vez, trocando na batida (seção 2.1 do projeto).
- Ritmo em rajada e respiro, não constante. Uma câmera lenta só, no "rosto da noite".
- Uma música por baixo, sem narração. Corte seco, sem transições de efeito.
- Texto só no título de abertura e no fechamento (logo e chamada).
- Cor: neon saturado, pele quente, sombras escuras mantidas.
- Efeitos com moderação: flash branco curto em 2 ou 3 cortes de rajada, zoom "soco" no título, câmera lenta só no rosto da noite, brilho leve no neon. Nada de transição de efeito entre clipes.

## Fluxo de trabalho

1. **Inventário:** para cada clipe, extrair frames com ffmpeg, olhar as imagens, identificar o take (códigos A1 a E3 do projeto), medir duração e brilho, marcar se está tremido ou desfocado. Salvar em `edicao/inventario.md`.
2. **Grupos de luz:** agrupar clipes com luz parecida e definir uma correção por grupo (Lift/Gamma/Gain, balanço de branco, curvas e redução de ruído), aplicada no projeto do Kdenlive.
3. **Takes que faltam:** listar e preparar os prompts do Flow para eles.
4. **Montagem:** escrever `edicao/boteco_do_hudson.kdenlive` com os clipes cortados nos pontos certos, o título, a cor de cada grupo e os efeitos. Perfil 1080x1920, 30 fps.
5. **Render:** gerar `edicao/rascunho_vNN.mp4` com `melt` (ou ffmpeg) para o usuário assistir. Numerar cada versão e nunca sobrescrever a anterior.
6. **Ajustes:** a cada pedido do usuário, alterar o projeto, renderizar uma nova versão e registrar a mudança na seção "Histórico" abaixo.

Antes de entregar uma versão, abra alguns frames do render (início, título, meio, fim) e confira se o corte, o texto e a cor estão certos.

Não altere nem apague os vídeos originais. Trabalhe com cópias ou referências.

## Histórico de alterações

- Projeto, lista de takes e prompts do Flow criados.
- Título "Welcome / To / Boteco do Hudson" adicionado na abertura.
- Editor trocado de DaVinci Resolve para Kdenlive, com o Claude fazendo a edição inteira.
