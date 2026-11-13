# Liderplac · Reforma de painel v3 → prompt Seedance 2.5

Cliente: **Liderplac** (placas/painéis de máquina, desde 1994, @liderplac1994).
Vídeo base: `liderplac_reforma_painel_v3.mov` — 1080x1920, 30 fps, ~30 s, sem áudio.
Objetivo: usar o vídeo como referência (video-to-video) e deixar os painéis
ultrarrealistas, com reflexo de luz, textura de material e profundidade.

## Como usar (importante)

1. **Gere sem os textos.** IA de vídeo deforma letras. Exporte uma versão do
   vídeo sem as legendas grandes ("ÓLEO", "PRECISA DE REFORMA...", CTA, logo) e
   recoloque tudo por cima depois, na edição. As gravações pequenas do painel
   (ROMI, I-30A, tabelas) a IA vai tentar manter — confira quadro a quadro.
2. **Corte por cena.** O Seedance segura melhor 5–10 s por geração. Use o
   prompt mestre + o bloco da cena correspondente, mesmo seed em todas.
3. **Força de referência média (~0.5–0.65).** Baixa demais muda o movimento;
   alta demais não ganha realismo.
4. Mande também um print nítido do painel limpo como imagem de referência,
   se a ferramenta aceitar.

## Prompt mestre (colar em todas as cenas)

```
Photorealistic product commercial, vertical 9:16, 1080x1920. Keep the exact
camera motion, timing, framing and composition of the reference video. Upgrade
only the realism of the industrial machine control panels.

The panels are real screen-printed aluminum plates, about 2 mm thick, with
visible beveled edges, small mounting holes with metal screws, crisp
silkscreened graphics and labels slightly raised on the surface, round cut-outs
for knobs showing the real thickness of the metal. White panels have a satin
enamel finish; black panels have a semi-matte anodized finish with fine
brushed-metal grain.

Lighting: high-end studio product photography. Large softbox key light from the
top left creating a soft gradient specular highlight that glides across the
panel surface as the camera moves, a thin bright rim light on the panel edges,
subtle reflections of the studio environment on the surface, physically
correct soft contact shadows on the background, gentle ambient occlusion around
the holes. Shallow depth of field on close-ups, slight lens bokeh, cinematic
color grading, deep blacks, clean whites, 8K detail, sharp micro texture,
ray-traced reflections, natural motion blur.

Preserve all printed text, numbers, logos and tables exactly as they are,
legible and undistorted. No new text, no extra objects, no people, no hands.
```

**Negative prompt:**

```
warped text, melted letters, gibberish typography, plastic look, CGI look,
flat lighting, cartoon, oversaturated, flicker, jitter, morphing shapes,
extra holes, bent panel, low resolution, blurry print, watermark
```

## Blocos por cena (somar ao mestre)

**Cena 1 · 0–3 s · Macro do painel gasto**
```
Extreme macro, low angle sliding across an old worn dark grey machine panel.
Real oil film with rainbow iridescent sheen, dried grease, scratched paint,
chipped print, dust in the light. A red light streak sweeps across the dark
background at the top. Moody, dark, high contrast, rack focus.
```

**Cena 2 · 3–8 s · Painel branco entra no estúdio**
```
A clean white ROMI I-30A panel slides in from the left and stops at the center,
floating in front of a seamless light grey studio backdrop with a soft
vignette. As it moves, a soft highlight sweeps across the enamel surface and
the edges catch a thin rim light. Soft shadow on the backdrop.
```

**Cena 3 · 8–14 s · O tempo destrói o painel**
```
Slow push-in on the panel while it ages in real time: brown oil stains spread
and soak into the paint, rust specks appear, fine tool scratches cut across
the print, the white turns yellowed and greasy, the gloss becomes dull and
uneven. Realistic grime physics, no cartoon effects.
```

**Cena 4 · 14–19 s · Camada por camada**
```
A precision restoration wipe: a fresh new layer slides down over the worn
panel, a machined edge with a thin red accent line moving top to bottom,
revealing pristine white enamel and sharp new print underneath. The new
surface catches a bright specular glint as it is revealed.
```

**Cena 5 · 19–21 s · Novo de novo**
```
The fully restored white panel, perfect and glossy, gentle hero rotation of a
few degrees, a light sweep glides across the surface from left to right.
```

**Cena 6 · 21–30 s · Final premium**
```
Dark charcoal studio background with diagonal red light streaks and soft red
haze. A black anodized ROMI S-30B panel in front of a white ROMI I-30A panel,
layered with real depth, slow parallax drift. Red rim light on the right edges,
cool white key light from the top left, glossy reflections sliding over both
panels, subtle reflection on a dark glossy floor. Leave clean empty space at
the bottom third for the call to action.
```

## Validação antes de entregar

- [ ] Textos gravados nos painéis (ROMI, I-30A, S-30B, tabelas) sem deformação
- [ ] Sem flicker entre quadros nem troca de formato dos furos
- [ ] Legendas e logo Liderplac recolocados na edição, ortografia conferida
- [ ] 1080x1920, terço inferior livre para o CTA

## Cortes enviados ao Drive (pasta "Liderplac · Reforma painel v3")

| Arquivo | Trecho | Bloco de prompt |
|---|---|---|
| cena1-macro-oleo.mp4 | 0–3,3 s | Cena 1 |
| cena2-painel-entra.mp4 | 3,3–9 s | Cena 2 |
| cena3-desgaste.mp4 | 9–14 s | Cena 3 |
| cena4-camada-por-camada.mp4 | 14–20 s | Cena 4 |
| cena5-novo-de-novo.mp4 | 20–25 s | Cena 5 + Cena 6 (vira para o fundo escuro no meio) |
| cena6-final-cta.mp4 | 25–30 s | Cena 6 |

MP4 H.264, 1080x1920, ~2,6 MB cada (limite do envio ao Drive por aqui é ~3 MB).
Na montagem final, juntar na ordem e recolocar legendas e logo.
