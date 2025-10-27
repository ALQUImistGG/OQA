Pacote textual único organizado para entrega ao time de design/animação e engenharia

Arquivos listados abaixo com nomes sugeridos e conteúdo pronto para copy/paste. Copie cada bloco para o arquivo correspondente (por ex.: Intro_Description.txt, Gameplay_Description.txt, Stinger_Description.txt, Variants_Description.txt, obs_stinger.json, README_Project_Package.txt, CHECKLIST_QA.txt). Todos os parâmetros técnicos, timings e instruções de implementação estão incluídos.

Intro_Description.txt

Título: Overlay Quintessencial — Mockup 1 Intro (8–10s)

Resumo curto: Cena de abertura 8–10s, identidade ALQUImist central, loopable para OBS (WEBM alpha primário; MP4 greenkey fallback).

Descrição completa:



Objetivo: cena de abertura 8–10s com logotipo ALQUImist central, diamante com padrão yin‑yang, halo pulsante, feixe turquesa conectando o “A” ao diamante, partículas suaves em parallax e agrupamento de botões de controle.

Composição visual: safe area 10%; background gradiente Preto Obsidiana #060608 → Púrpura Profundo #3A176E; símbolos alquímicos em pentágono com parallax, opacidade 10–15%; diamante central com padrão yin‑yang; halo pulsante ±4% escala, opacidade 10–25%.

Feixe: inicia no “A”, percorre até o diamante; cor turquesa #00E5D4; glow 12px; animação contínua em loop.

Partículas: turquesa, 3–5px, blur leve, cobertura 3–6%, movimento suave e aleatório.

Texto: “Iniciando transmissão...” em âmbar #FFB000; “Agradecemos por aguardar” em turquesa #00E5D4; fonte limpa e legível.

Controles de jogo (base, agrupados): PlayStation (esquerda) ▵ #7CFC00; ◻ #FF69B4; ○ #FF0000; ✕ #4169E1. Xbox/Nintendo (direita) Y #FFFF00; A #00FF00; B #FF0000; X #0000FF. Botões: círculos com borda glow 2px, opacidade 25–30%, pulso sutil sincronizado com halo.

Animação timeline: fade‑in 0–2s; loop do feixe e respiração do halo ~0.6Hz (±0.1Hz); botões entram sequencialmente (PlayStation primeiro), iluminam ao serem tocados pelo feixe.

Entregáveis ao final: PSD/AI/SVG com camadas nomeadas (background, símbolos, logo vetor, diamante vetor, halo, feixe, partículas); protótipo animado 60fps loopable; WEBM VP9 alpha; MP4 H.264 greenkey fallback; versão low‑perf (partículas/blur reduzidos).

Parâmetros técnicos (resumo):



Master: 2560×1440; exportar 1920×1080 e 1080×1920.

Formato: WEBM (VP9) alpha primário; MP4 H.264 + chroma key #00FF00 fallback.

Framerate: 60 fps.

Bitrate: WEBM 10–12 Mbps; MP4 8–10 Mbps.

Keyframe interval: 2 s.

Alpha: 8‑bit pre‑multiplied se possível.

Notas: separar partículas e feixe em layers para permitir LOD/culling no OBS.

Gameplay_Description.txt

Título: Overlay Quintessencial — Mockup 2 Gameplay (principal)

Resumo curto: overlay modular e discreto para gameplay, escalável entre 2560×1440 e 1920×1080, com branding reduzido e animações reativas.

Descrição completa:



Objetivo: overlay funcional para gameplay com baixa distração e alto contraste para o conteúdo do jogo.

Layout e safe area: safe area 10%; área central para gameplay; webcam topo esquerdo (frame turquesa glow 3px, canto 8px); chat topo centro (fundo #060608 20% opacidade; texto #F3F6F7); alertas topo direito com borda âmbar #FFB000; status do jogo base esquerda; estatísticas base direita.

Branding reduzido: diamante ~50% do tamanho da Intro; logotipo compacto; símbolos alquímicos opacidade 5–12%; feixe mais sutil glow 6–8px; partículas cobertura 3–5%.

Componentes funcionais: webcam frame PNG 32‑bit; chat box PNG semi‑transparente; alert widget animations (WEBM alpha 5–8s); status widgets (PNG + optional animated accents).

Animações reativas (predefinidas): novo seguidor → feixe + halo expandem; doação → partículas douradas + flash âmbar; sub → animação completa do feixe + iluminação dos botões; raid → transição estilo portal (stinger variante).

Diretrizes UX: elementos funcionais não devem cobrir HUDs importantes do jogo; fornecer versões com padding adicional para streamers com overlays de HUDs nativos.

Entregáveis: PSD/AI com guias de safe area; frames em PNG 32‑bit; micro‑animações WEBM VP9 alpha (alertas 5–8s); versão low‑perf sem blur/partículas.

Parâmetros técnicos (resumo):



Resoluções: master 2560×1440; fallback 1920×1080.

Formatos: PNG 32‑bit para estáticos; WEBM VP9 alpha para micro‑animações.

Framerate: 60 fps para animações (widgets podem usar 30 fps para economia).

Bitrate: 8–10 Mbps para WEBM gameplay widgets; alertas curtos 6–8 Mbps.

Safe areas: 10% Márgen.

Stinger_Description.txt

Título: Overlay Quintessencial — Mockup 3 Transição Stinger (≈2.5s)

Resumo curto: stinger em 4 fases, ponto de corte configurável para OBS; WEBM alpha primário; MP4 greenkey fallback.

Descrição completa:



Objetivo: transição fluida e impactante de ~2.5s com white flash no corte, animada e otimizada para OBS transition_point_ms.

Estrutura e timings (total ~2.5s):

Carga 0.00–0.60s: partículas convergem ao centro; glow inicia no “A”.

Corte 0.60–1.70s: feixe percorre logotipo até o diamante; energia concentra.

Flash ~1.18s (ponto crítico): white flash curto recomendado 0.06s.

Dissipação 1.70–2.50s: feixe transforma‑se em púrpura; elementos assentam.

Visuals e efeitos: glow progressivo no “A”; cor do feixe turquesa → flash âmbar → dissipação púrpura; partículas convergentes e explosão suave no flash; halo responsivo.

Curvas de easing: carga ease‑out‑cubic; corte linear; dissipação ease‑in‑out‑sine.

Entregáveis: WEBM VP9 alpha com marker/nota do transition_point_ms; MP4 H.264 greenkey fallback; storyboard frame‑by‑frame; asset do white flash em camada separada (para ajuste no OBS).

Parâmetros técnicos (resumo):



Resolução entrega recomendada: 1920×1080 (fornecer escala 2560×1440 opcional).

Formato primário: WEBM VP9 alpha; fallback MP4 H.264 + chroma key #00FF00.

Framerate: 60 fps.

Bitrate: WEBM 10–12 Mbps; MP4 8–10 Mbps.

Keyframe interval: 2 s.

Ponto de transição recomendado: 1180 ms (faixa ajuste 1150–1220 ms).

White flash duration: 60 ms (0.06s) — intensidade 100% → 80% → 0% em 3 frames a 60 fps.

OBS JSON de referência incluído separadamente (obs_stinger.json).

Variants_Description.txt

Título: Overlay Quintessencial — Versões coloridas alternativas e presets

Variações propostas:



Nocturna (mais dark)

Paleta: Preto puro #000000; Púrpura escuro #1A0A3E; Turquesa profundo #00A89F; âmbar mantido #FFB000 para alertas.

Uso: streams com temática dark, cinematográficas; aumentar contraste do âmbar nos alertas.

Neon (mais vibrante)

Paleta: Turquesa saturado #00FFE1; Púrpura vibrante #5A2BFF; glow intenso para botões/partículas; partículas douradas mais saturadas.

Uso: streams com estética neon/futurista; elevar brilho dos guias e botões.

Minimal (baixo impacto)

Paleta: reduzir saturação turquesa/púrpura; aumentar opacidade de fundos; partículas quase inexistentes.

Uso: streamers que priorizam máxima legibilidade e desempenho.

Entregáveis por variante:



Arquivo de paleta ASE/ACO.

Mockups estáticos para aprovação.

Animações principais exportadas nas mesmas especificações (WEBM alpha / MP4 fallback).

Presets de cor no PSD/AI para troca rápida.

Regras rápidas de aplicação de paleta:



Texto principal: Branco‑Quintessência #F3F6F7.

Acentos/feixes: Turquesa variante conforme tema.

Alertas: sempre utilizar âmbar #FFB000 ou equivalente saturado para máxima visibilidade.

obs_stinger.json

Conteúdo (JSON):

{

"transition_point_ms": 1180,

"adjustment_range": "1150-1220",

"video_format": "webm_vp9_alpha",

"fallback_format": "mp4_h264_greenkey",

"resolution": "1920x1080",

"framerate": 60,

"bitrate": "10-12 Mbps (webm), 8-10 Mbps (mp4)",

"keyframe_interval": "2s",

"white_flash_duration_ms": 60,

"performance_notes": "testar em hardware mínimo: i5 + GTX 1060"

}

README_Project_Package.txt

Projeto: Overlay Quintessencial — Pacote de entrega textual

Conteúdo do pacote (arquivos textuais nesta entrega):



Intro_Description.txt — descrição, entregáveis e parâmetros técnicos da Intro.

Gameplay_Description.txt — descrição, entregáveis e parâmetros técnicos da cena Gameplay.

Stinger_Description.txt — descrição, entregáveis e parâmetros técnicos da transição stinger.

Variants_Description.txt — variações de cor e presets.

obs_stinger.json — JSON pronto para uso como referência de transition_point_ms no OBS.

CHECKLIST_QA.txt — checklist de validação e passos de QA.

Instruções de uso:



Copiar cada bloco para arquivo com o nome indicado e compartilhar com designer/animador/engenharia.

For animações: solicitar master em 60 fps, WEBM VP9 alpha como primeiro formato e MP4 H.264 com chroma key verde #00FF00 como fallback.

Fornecer versão “low‑perf” (sem blur/partículas) junto das versões full para testes de performance.

Testar stinger no OBS com transition_point_ms = 1180 e ajustar entre 1150–1220 conforme sensação.

CHECKLIST_QA.txt

Título: Checklist QA — Overlay Quintessencial

Validação visual



[ ] Logotipo legível em 70% / 100% / 130% escala.

[ ] Contraste validado em displays IPS/VA/TN.

[ ] Teste de exibição em ambiente claro e escuro.

[ ] Teste de acessibilidade para daltonismo (ferramenta de simulação).

Validação técnica / performance



[ ] WEBM VP9 alpha exportado e testado no OBS com alpha real.

[ ] MP4 H.264 greenkey fallback testado (chroma key #00FF00).

[ ] Bitrates validados (WEBM 10–12 Mbps; MP4 8–10 Mbps) e arquivos com tamanhos aceitáveis.

[ ] Verificar keyframe interval = 2s em ambos formatos.

[ ] Teste de CPU/GPU: baseline i5 + GTX 1060; medir impacto em uso real de streaming.

[ ] Fornecer e validar versão low‑perf (partículas/blur reduzidos).

Stinger / OBS



[ ] Stinger WEBM com marker de transition_point_ms embutido; JSON disponível.

[ ] Testar transition_point_ms = 1180; ajustar entre 1150–1220; comparar white flash 60ms vs 80ms.

[ ] Verificar sincronização de áudio (se aplicável) e visual no momento do corte.

Entrega e documentação



[ ] PSD/AI/SVG com camadas nomeadas e presets de cor.

[ ] Mockups estáticos para aprovação (Intro, Gameplay, Stinger).

[ ] Micro‑animações WEBM alpha (alertas) 5–8s.

[ ] Pacote de instalação e guia passo‑a‑passo para OBS/Streamlabs (incluir obs_stinger.json).

[ ] Material de marketing: screenshots e vídeo demo curto.

Checklist de testes com streamers



[ ] Rodada de testes com 3–5 streamers de hardware variado.

[ ] Coletar feedback sobre distração, legibilidade e performance.

[ ] Registrar correções/ajustes e priorizar.
