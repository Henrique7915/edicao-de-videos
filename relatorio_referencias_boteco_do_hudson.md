# Relatório: referências de edição de pagode / roda de samba para o Boteco do Hudson

## Tarefa para o agente que receber esta pasta

Use este relatório como base de pesquisa para ajudar o dono do projeto a gravar e editar um Reels (vertical 9:16, 30 a 45 s) de um evento de pagode no **Boteco do Hudson** (bar pequeno, fechado, noturno, pouca luz, sem drone). Entregue, a partir das seções 5 a 9: (1) um roteiro de gravação com lista de takes a capturar, (2) um plano de edição segundo a segundo, e (3) ajustes se o dono trouxer novos vídeos. Não invente números: use só o que está marcado como MEDIDO ou VISTO, e trate OPINIÃO como sugestão.

## Conteúdo da pasta

- `relatorio_referencias_boteco_do_hudson.md`: este arquivo (resumo, medições, padrões, ranking de takes, roteiro e modelo de edição).
- `dados_skill/<vídeo>/VIDEO.md` e `dados_skill/<vídeo>/video/*.md`: saída em texto da ferramenta rea-video, um conjunto por vídeo: `yt_Qfo-QbzT10s` (A Grande Roda de Samba), `yt_zSSROrafgH8` (Folks), `yt_B3Kb6elfv6c` (Tiee), `ig_ciri_DeE7AGovHfQ` (Ciri), `ig_oboe_Dexa_NwylQS` (Oboé). Para ver cada corte com horário, abra `video/timeline.md`; para som, `video/sound.md`; para enquadramento e edição, `video/look.md`.
- **Atenção nesses arquivos:** os campos de "como foi feito" (`made~`, "AI-generated", "3D render"), os veredictos de origem da música e as seções de remake estão errados ou sem base para estes vídeos (a compressão das plataformas apaga os sinais). Ignore-os. Confie só em número de cortes, duração dos takes, BPM, loudness e enquadramento.
- Imagens, áudio e vídeos não estão incluídos. Você não precisa deles: tudo o que importa está descrito em texto.

Data da pesquisa: 2026-11-16. Idioma: português do Brasil.
Leitor previsto: um agente que **não consegue ver vídeo nem imagem**. Por isso tudo abaixo está em texto: números, descrições de quadro e regras. Cada afirmação é marcada como **[MEDIDO]** (calculado por ferramenta no arquivo de vídeo), **[VISTO]** (descrito por quem olhou quadros do vídeo) ou **[OPINIÃO]** (recomendação, não vem dos vídeos). **[NÃO CONFIRMADO]** = não deu para verificar.

---

## 0. Resumo executivo (leia só isto se tiver pouco tempo)

1. Os melhores vídeos de aftermovie de pagode/samba em formato vertical têm **cortes muito rápidos: 0,86 a 1,01 s por take** em 4 dos 5 vídeos medidos (Roda do Rio 0,86, Tiee 0,88, Ciri ~0,9, Oboé 1,01) **[MEDIDO]**; o mais simples (Folks) tem cerca de 2 s **[MEDIDO]**.
2. A maioria **não corta na batida da música**: entre 14% e 27% dos cortes caem na batida em 3 vídeos (o acaso seria ~17% a 31%) **[MEDIDO]**. Ciri chega a 48% (acaso ~40%) e Folks a 40% (acaso ~28%), uma vantagem pequena. Não precisa sincronizar na batida para ficar bom.
3. A receita mais repetida **[VISTO]**: planos médios e close (rosto do público cantando, artista, instrumento) em movimento de câmera constante, uma trilha única por baixo, sem narração, e uma marca/logo no começo ou no fim.
4. **O local:** Boteco do Hudson é pequeno, de teto baixo, com palco quase no nível do público e iluminação de neon e LED colorido **[VISTO]**. Isso favorece planos próximos (close e médio), que são os que mais aparecem nos vídeos de referência.
5. Referências com drone ou palco enorme devem ser descartadas ou usadas só como inspiração de cor (o usuário não tem drone e o espaço é pequeno).

---

## 1. Contexto do pedido

- Quem vai gravar: o próprio usuário, sozinho. Destino: Instagram Reels, vertical 9:16, 30 a 45 s.
- Local: **Boteco do Hudson**, Instagram [@botecodohudson](https://www.instagram.com/botecodohudson/). Ambiente fechado, pequeno, à noite, pouca luz.
- Restrição do usuário: **sem drone**. Descartar qualquer referência dependente de drone.
- Dados públicos do perfil **[VISTO]**: 87 posts, 32,2 mil seguidores, bio "Aqui só entra boa energia", abre domingo das 17h às 00h e segunda das 19h às 01h, Belo Horizonte (bairro das Indústrias II).

---

## 2. Como a análise foi feita (e o que NÃO foi possível)

- **Quem analisou:** um agente com navegador. Ele extraiu 14 quadros espaçados de cada vídeo (a cada ~1 s nos vídeos de 15 s, ~4 s nos de 60 s) e descreveu o que viu.
- **Ferramenta rea-video** ([JuneYaooo/rea-video](https://github.com/JuneYaooo/rea-video)) rodada em 3 Shorts do YouTube. Ela mede número de cortes, duração de take, BPM, loudness e enquadramento.
- **Problema conhecido da ferramenta:** ela tenta dizer se o vídeo é "filmado, IA ou 3D". Nos 3 vídeos YouTube ela errou (disse ~83% IA no primeiro). Motivo: a compressão do YouTube apaga os sinais que ela usa e eu não configurei o modelo de visão dela. **Ignore os veredictos "IA / 3D / código"**. Use só as medições de corte, BPM e enquadramento.
- **Não ouvi áudio.** O que se sabe do som é só o que a ferramenta mediu (BPM, loudness, presença de voz). Não sei dizer se o som é do evento ou música colocada depois; a ferramenta apenas inclina "provável trilha de biblioteca" sem confirmar.
- **Não foi analisado:** TikTok (não pesquisei). Os vídeos do Instagram foram vistos por quadros, mas a ferramenta rea-video **não rodou neles** (precisa de arquivo .mp4; o usuário vai baixar os que quiser). Cada vídeo foi visto uma vez, não duas.
- **Números de alcance:** o Instagram não mostra visualizações nessas páginas. Para Instagram usei **curtidas**. No YouTube, visualizações (e curtidas quando visíveis). Tamanho do perfil dos criadores: **[NÃO CONFIRMADO]**. Os números são pequenos em geral (o maior vídeo tem ~2,5 mil views).
- **Contagem de cortes em vídeos não medidos pela ferramenta** é estimativa a partir de quadros.

---

## 3. Medições da ferramenta (3 Shorts do YouTube) [MEDIDO]

| Vídeo | Duração | Cortes | Cortes/min | Duração média do take | BPM | Cortes na batida | Voz |
|---|---|---|---|---|---|---|---|
| [A Grande Roda de Samba](https://www.youtube.com/shorts/Qfo-QbzT10s) (@lanceevents) | 60 s | 70 | 68,9 | 0,86 s | 110 | 23% (acaso ~25%) | nenhuma |
| [Tiee em Curitiba](https://www.youtube.com/shorts/B3Kb6elfv6c) (@cwbbrasil.eventos) | 59 s | 71 | 71,2 | 0,88 s | 136 | 27% (acaso ~31%) | nenhuma |
| [Folks Pub Sertanejo](https://www.youtube.com/shorts/zSSROrafgH8) (@FolksPubSertanejo) | 35 s | 21 | 34,2 | ~2,0 s (os takes de filme) | 129 | 40% (acaso ~28%) | 53% do tempo (música cantada; veredito "TTS" da ferramenta é duvidoso, ignore) |
| [5 anos de Pagode (Ciri)](https://www.instagram.com/p/DeE7AGovHfQ/), arquivo baixado do Instagram | 30,4 s | 34 | 65,2 | ~0,9 s (30,4 s ÷ 34 takes; a ferramenta cita 0,36 s só para os takes que ela classifica como filmagem, ignore) | 178 (pode ser 89 em meio tempo) | 48% (acaso ~40%) | a ferramenta marca voz, sem confirmar a origem; música em 95% do tempo |
| [Oboé Salvador 3 anos](https://www.instagram.com/p/Dexa_NwylQS/), arquivo baixado do Instagram | 60,6 s | 60 | 58,4 | 1,01 s | 129 | 14% (acaso ~17%) | nenhuma; música em 59% do tempo, termina antes do fim do vídeo |

Outros pontos medidos:
- Ciri: enquadramento close 48%, médio-close 33%, médio 20% (medido pelo rosto); 5 locais ou posições de câmera diferentes; a música termina junto com o vídeo.
- Oboé: enquadramento médio-close 59%, médio 22%, close extremo 12% (estimado); cor muito saturada e quente.
- Roda do Rio: enquadramento médio-close em 83% dos takes, close em 6%, médio em 10%; câmera em movimento em 100% dos takes; um efeito sonoro "ding" aos 0,1 s quando o texto "SAMBA" aparece; música cortada de forma seca no fim.
- Tiee: enquadramento médio em 100% (estimado); música termina antes do fim do vídeo.
- Folks: o último trecho é um cartão com logo (~5 s) que a ferramenta conta como inserção.
- **Observação:** os quadros confirmam que os 70 e 71 cortes são takes de fato diferentes (pessoa ou ângulo muda a cada ~1 s). A contagem não é erro de detecção.

---

## 4. Vídeos analisados por quadros [VISTO]

### 4.1 Referências de aftermovie (YouTube e Instagram)

| # | Vídeo e perfil | Duração | Alcance | Abertura (0–3 s) | Estilo e luz | Texto e fim |
|---|---|---|---|---|---|---|
| 1 | [A Grande Roda de Samba](https://www.youtube.com/shorts/Qfo-QbzT10s) | 60 s | 149 views, 1 curtida | Logo da roda no cenário em close; depois brinde de duas latas | Rostos de mulheres cantando e dançando, banda, abertos da plateia. Luz de palco azul, roxa e magenta, pele quente | Logo no cenário (não é texto sobreposto). Termina em close do vocalista |
| 2 | [Folks Pub Sertanejo](https://www.youtube.com/shorts/zSSROrafgH8) | 35 s | 899 views, 7 curtidas | Neon "FOLKS" em ângulo diagonal; depois selfie de duas mulheres | Lâmpadas de filamento quentes com bokeh, fundo azul. Dois takes desfocados em movimento | Cartão final com logo "Não tem erro!" por ~5 s |
| 3 | [Tiee em Curitiba](https://www.youtube.com/shorts/B3Kb6elfv6c) | 59 s | 2,2 mil views, 31 curtidas | Mulher com copo dentro de moldura vintage; título "TIEE · 29 de julho de 2023 · by KLEVFILMS" aos 4,5 s | Azul e teal, contraste alto. Cantor, pandeiro em close, rostos, planos abertos do palco com repetição em espelho | Título de abertura. Termina em close do cantor |
| 4 | [5 anos de Pagode (Ciri)](https://www.instagram.com/p/DeE7AGovHfQ/) | 30 s | 102 curtidas | Cantor de camiseta branca em plano médio; depois artista de costas com o braço estendido | **34 cortes medidos (~0,9 s por take)**; nos quadros apareceram: sax, cavaquinho, baterista, rosto de mulher cantando, tela dividida aos 6,8 s. Luz de lâmpadas e contraluz quente | Créditos "UM FILME POR: @eaiciri" aos ~26 s. Termina em plano médio do cantor |
| 5 | [Quintal da Villa (Batucada Dez)](https://www.instagram.com/p/DQK-knBj4v_/) | 52 s | 146 curtidas | Logo animado sobre fundo preto; depois logo grande sobre mulher | Luz vermelha forte e lâmpadas penduradas, bar fechado à noite; rostos cantando em close, cantor visto de baixo, banjo em close | Logo no início; marca do videomaker aos 11 s. Termina em grupo dançando |
| 6 | [Oboé Salvador 3 anos](https://www.instagram.com/p/Dexa_NwylQS/) | 61 s | 315 curtidas | Luzes de palco; depois letreiro | Festival grande: fogos, chamas, retratos de rosto com legendas pequenas, P&B aos 35 s, rastro de luz aos 26 s. Cor muito saturada | Legendas poéticas pequenas. Usar só como inspiração de cor e ritmo (evento grande) |

Outros 7 vídeos analisados e descartados como referência principal: Samba SJ (um take quase contínuo, muito escuro), Boteco do Boss, Thiaguinho/Camarote Aju (um take só de palco grande), Madax (DJ/eletrônica), Turma do Pagode Campinas (palco grande), Mixing Night (balada), Pagode do Gla (de dia, ao ar livre). Também descartados por drone: Pagode no Supra e Roda de Samba do Bem.

### 4.2 Vídeos gravados no próprio Boteco do Hudson [VISTO]

| # | Vídeo e perfil | Duração | Curtidas | O que aparece |
|---|---|---|---|---|
| H1 | [Reel do próprio Hudson](https://www.instagram.com/p/DZ5k584uYII/) | 52 s | 511 | **Calçada** com mesas de madeira dobráveis e grade metálica ao fundo, luz de dia/entardecer. Pessoas de camisa amarela do Brasil. Legenda palavra por palavra na parte de baixo (a palavra atual em amarelo). Um garçom serve, homem fala para a câmera. Câmera na altura do rosto, quase fixa |
| H2 | [Resenha do Edgar](https://www.instagram.com/p/DYjoeamBIkx/) | 40 s | 401 | **Interior lotado** à noite. Palco baixo na altura do público, banda com baixo e percussão sentada ao redor de mesas com baldes de gelo e garrafas. Texto fixo no topo "ESSA É NOSSA HEIM !!!" com 3 corações, o vídeo todo. Câmera sempre perto, em movimento leve, de dentro da plateia. Poucos cortes: a cena é quase contínua com aproximações a instrumentos |
| H3 | [Portfoliuz (videomaker mobile)](https://www.instagram.com/p/DcOJENPx1jp/) | 75 s | 43 | Noite de piseiro com chapéu de vaqueiro. Muitos takes curtos de pessoas: cantor, casais, brindes, mulher dançando, mesa com balde de gelo. **Neon nas paredes** (letreiros em amarelo, verde com forma de violão, caneca de chope laranja) e luz rosa/laranja/azul. Feito por videomaker que grava no celular |
| H4 | [Sementes do Samba](https://www.instagram.com/p/DcgVauQxZJX/) | 39 s | 799 | Um homem dançando sozinho, câmera quase parada na mesma posição o vídeo todo (um take longo). Luz de feixes coloridos (vermelho, azul, magenta) que passam no corpo dele. Fundo: mesas redondas de madeira, banquetas altas, pessoas em pé. Resolução baixa (480p) |

**O que dá para concluir sobre o espaço (H2, H3, H4):**
- Teto baixo e paredes próximas: planos abertos são curtos. O melhor "aberto" que se consegue é de dentro da plateia, olhando para o palco baixo.
- A luz do ambiente é neon e LED colorido (magenta, azul, verde, laranja). Cores quentes nas paredes.
- Mesas redondas com balde de gelo, garrafas e copos plásticos laranja: bons detalhes de bebida.
- Palco quase no chão: o artista é filmado de frente à altura do rosto, não "de baixo para cima".
- Lotado no horário de pico: planos próximos de rosto e instrumento são mais fáceis do que planos abertos.
- Calçada com mesas dobráveis: boa para o "antes de abrir" e para entrevistas curtas, mas é de dia/entardecer e fica fora do clima de noite.

---

## 5. Padrões que mais se repetem (contagem em 15 vídeos de 15 criadores)

(9 do YouTube Shorts e 6 do Instagram, vistos por quadros; os 4 vídeos do Hudson não entram nessa contagem.)

- **14 de 15:** têm plano aberto do salão ou palco.
- **13 de 15:** têm artista ou DJ em plano médio ou close.
- **12 de 15:** têm close ou médio de rosto do público cantando ou rindo.
- **9 de 15:** usam texto ou logo sobreposto em algum ponto.
- **7 de 15:** abrem (0–3 s) com placa, logo ou letreiro do local.
- **7 de 15:** têm instrumento em close. **7 de 15:** têm mãos para cima ou dança.
- **6 de 15:** têm detalhe de bebida.
- **5 de 15:** terminam em marca, créditos ou cartão final.
- **Efeitos:** flash ou flare em 4. P&B pontual em 3. Tela dividida em 1.
- **Ritmo:** os melhores usam take de ~0,9 a 1 s (Tiee, Roda do Rio, Ciri, Oboé) ou ~2 s (Folks). Isso corrige uma estimativa anterior, que dava ~2 s para o Ciri a partir de quadros espaçados; a medição mostrou 34 cortes em 30 s. Os vídeos de um take só (Samba SJ, Thiaguinho, Sementes do Samba) têm menos variedade.

**O que os vídeos mais fracos fazem diferente [OPINIÃO baseada no que se viu]:**
- Um take só, sem corte, sem abertura e sem fechamento.
- Escuro e granulado sem luz de apoio.
- Efeitos fortes sem pessoas conversando ou ambiente (Madax).
- Engajamento (curtidas) **não** separou qualidade: perfis pequenos ficam com poucas curtidas mesmo com imagem boa.

---

## 6. Ranking dos 10 takes mais usados e como gravar no Hudson [OPINIÃO]

| # | Take | Em quantos | Como gravar em espaço pequeno e escuro |
|---|---|---|---|
| 1 | Plano aberto do salão | 14 | De dentro da plateia ou da porta, olhando para o palco baixo. Inclua neon ou lâmpada no quadro para dar profundidade. |
| 2 | Artista médio ou close | 13 | De frente, na altura do rosto, perto do palco (ele está quase no chão). Foco e exposição travados no rosto. |
| 3 | Rosto do público cantando | 12 | A ~1 m, altura do olho, no pico da música. Peça autorização ou faça um sinal de "pode?". |
| 4 | Placa, letreiro, neon do bar | 7 | Grave antes de encher, com tudo aceso. Use o neon "Boteco do Hudson" como abertura. |
| 5 | Instrumento em close | 7 | Pandeiro, cavaquinho, tantã, baixo, de lado ou de cima. O movimento já está no instrumento. |
| 6 | Mãos para cima, dança | 7 | Médio pela cintura, de lado, para não precisar de espaço. |
| 7 | Detalhe de bebida | 6 | Balde de gelo, brinde, copo laranja, a 20 a 30 cm, com neon ao fundo para o desfoque brilhar. |
| 8 | Câmera por cima do ombro, celulares no ar | 5 | Atrás de alguém, mostrando a roda. |
| 9 | Câmera atrás do artista, olhando a plateia | 5 | Só se der para ficar atrás. Mostra a reação. |
| 10 | Pan rápido ou desfoque de movimento | 4 | Gire o celular rápido de uma pessoa para uma luz. Serve de transição. |

**Luz:** nos vídeos de bar fechado (Ciri, Quintal da Villa, Folks, Hudson H2/H3) a luz principal é a do próprio ambiente (lâmpadas, neon, gel vermelho, LED colorido). Não consegui confirmar se usaram luz de LED na câmera **[NÃO CONFIRMADO]**. **[OPINIÃO]** Use a luz do bar como luz principal e proteja os pontos brilhantes (letreiros) com exposição levemente menor.

---

## 7. Roteiro de gravação para a noite (ordem cronológica) [OPINIÃO]

Gravar **80 a 120 clipes de 3 a 6 s**, em vertical, com câmera em movimento leve (a maioria dos vídeos usa câmera sempre em movimento).

1. **Antes de abrir (30 a 45 min antes):** neon e fachada, mesas e copos, instrumentos montados, passagem de som, balde de gelo, plano aberto do salão vazio com tudo aceso. Se der, uma cena na calçada com a luz do fim de tarde. Teste foco e exposição travados.
2. **Casa enchendo:** pessoas entrando, brindes, selfies, garçom servindo, rostos chegando. Takes de 2 a 3 s.
3. **Auge:** vocalista em médio e close, cada instrumento, mãos para cima, rostos cantando, 2 ou 3 pans rápidos, um aberto da plateia. Grave 5 a 8 s por take.
4. **Final:** brinde ou abraço, banda agradecendo, o neon do bar de novo para fechar.

---

## 8. Modelo de edição para um Reels de 30 a 45 s [OPINIÃO baseada nos números da seção 3]

Meta de ritmo: **~35 a 45 cortes em 40 s** (≈1 s por take), com 3 ou 4 takes mais longos (2 a 3 s) em momentos de destaque. O Ciri (o mais parecido com um boteco) fez 34 cortes em 30 s; para 40 s, isso dá cerca de 45 cortes. Cortar na batida é **opcional** (nos medidos, só Ciri e Folks passam do acaso, e por pouco).

| Segundo | Conteúdo |
|---|---|
| 0–3 | Neon ou letreiro do Boteco do Hudson **ou** um rosto cantando em close. Título curto (nome do evento e data). |
| 3–8 | Casa enchendo: 4 a 6 takes de ~1 s (pessoas entrando, brinde, copo). |
| 8–20 | Artista, instrumento, rosto cantando, bebida: takes de ~1 s, alternando médio e close. |
| 20–32 | Auge: mãos para cima, dança, pan rápido, um aberto da plateia cheia. |
| 32–38 | O rosto mais emocionado da noite, em um take de 2 a 3 s. |
| 38–45 | Último plano com a marca do local e uma chamada ("Quer o próximo? Chama"). |

Trilha: uma música única por baixo, sem narração. Os 3 vídeos medidos têm 110, 129 e 136 BPM e a música termina de forma seca. Som real do evento (ou música colocada depois): **[NÃO CONFIRMADO]**.

---

## 9. Os 5 melhores como referência (priorizando o que se parece com o Hudson)

1. **[5 anos de Pagode (Ciri)](https://www.instagram.com/p/DeE7AGovHfQ/)** — pub com lâmpadas, takes de ~2 s, variedade de instrumentos, créditos no final. É o mais parecido com um boteco.
2. **[Quintal da Villa (Batucada Dez)](https://www.instagram.com/p/DQK-knBj4v_/)** — bar fechado e noturno com luz vermelha. Bom para rostos e banjo em close.
3. **[A Grande Roda de Samba](https://www.youtube.com/shorts/Qfo-QbzT10s)** — melhor equilíbrio de rostos, banda e luz. É a referência de ritmo (70 cortes em 60 s).
4. **[Folks Pub Sertanejo](https://www.youtube.com/shorts/zSSROrafgH8)** — pub com luz quente e bokeh, fechamento de marca.
5. **[Portfoliuz no Hudson (H3)](https://www.instagram.com/p/DcOJENPx1jp/)** — gravado no próprio local, mostra o neon e as cores reais do espaço, feito no celular. É a melhor prova de como o Hudson fica na câmera.

---

## 10. Pendências

- **TikTok:** não pesquisado.
- **Instagram:** rodei a ferramenta nos arquivos de Ciri e Oboé (baixados pelo usuário). Faltam, se o usuário quiser: Quintal da Villa (só veio a capa .jpg, sem vídeo) e Portfoliuz (H3), que é o gravado no Hudson.
- A identificação dos 2 arquivos foi feita pela duração (60,6 s = Oboé; ~30,4 s = Ciri). Os nomes originais dos arquivos eram códigos sem pistas.
- **Áudio:** nenhuma análise de som real foi feita (nem origem, nem quando a plateia canta, nem sincronia fina com a batida). Para isso é preciso uma pessoa ou um modelo que escute.
- **Alcance relativo ao tamanho do perfil:** não confirmado para nenhum criador.
- **Arquivos de apoio:** estão nesta pasta, em `dados_skill/` (só os textos da ferramenta). Os vídeos originais, imagens e áudio ficaram no computador do agente que fez a pesquisa e não foram copiados.
