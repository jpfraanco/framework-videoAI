# Selva urbana · roteiro decupado em 20 frames (exercício Human Academy)

Resposta ao pedido 2 do curso: "gerar 20 imagens desse roteiro, cena a cena, usando a CLI do Higgsfield, Seedream 5.0 2K". Roteiro original em [fontes/human-academy-curso.md](../fontes/human-academy-curso.md).

Teoria por trás: [FRAMEWORK.md, seções 5 e 11](../FRAMEWORK.md#11-o-método-human-academy-lido-prompt-a-prompt).

## Decisões de decupagem

- **7 atos, 20 frames.** Cada parágrafo do roteiro é um ato. Quase todo ato ganha 3 frames: onde estamos (aberto), o que ela sente (rosto), o que importa (detalhe).
- **Contraste no ato 1.** A casa e a manhã são comuns, sem nenhuma planta. É o "antes" que faz o portão tomado pela selva ter impacto.
- **A luz é o relógio.** O roteiro comprime um dia: manhã clara (atos 1 e 2), sol alto e sombra dura (atos 3 a 5), fim de tarde dourado (ato 6), pôr do sol (ato 7). A cidade vai ficando mais verde junto com a luz.
- **Planos variados em sequência.** Nunca dois frames seguidos com o mesmo tamanho de plano e o mesmo ângulo. Isso já deixa a sequência "montável" quando virar vídeo.
- **Frame 5 é o keyframe do curso**, adaptado para luz de manhã.
- **Cada prompt é independente.** O modelo de imagem não lembra do frame anterior, então todo prompt leva o mesmo sufixo com a âncora da personagem e o estilo.

## Referências

| Arquivo | O que é | Entra em |
|---|---|---|
| `refs/girl_sheet.png` | Folha B da [character sheet](character-sheet-street-girl.md) (um rosto só) | Todos os frames com ela (Image 1) |
| `refs/cidade.png` | O [asset ultra wide](cidade-engolida-ultrawide.md) | Frames 16, 19 e 20 (Image 2) |

## Sufixo (vai no fim de todo frame)

Salve como `sufixo.txt`:

```
CHARACTER (Image 1): the same young East Asian woman in every frame, identical face, very long straight jet-black hair, slouchy heather-grey chunky-knit beanie, black sleeveless tank top with a twisted knot at the chest, oversized black cargo bermuda shorts with a relaxed low drape, black slouchy knee-high leather boots, navy pinstripe canvas tote bag, chunky silver chain bracelets and silver rings.

STYLE: cinematic editorial film still from a contemporary fashion-thriller short film, photorealistic, hyper-detailed. Shot on 35mm film, Kodak Portra 400 grain, natural skin texture with visible pores, rich deep greens against black, white and concrete grey, subtle halation, soft atmospheric haze, natural motivated light only. 16:9. No text, no readable signage, no logos, no other people.
```

## Os 20 frames

| # | Ato | Plano | Luz |
|---|---|---|---|
| 01 | 1 · Manhã comum | Aberto, 35mm, altura dos olhos | Manhã clara |
| 02 | 1 | Close por cima do ombro, no espelho, 85mm | Manhã clara |
| 03 | 1 | Insert de cima, 100mm macro | Manhã clara |
| 04 | 2 · O portão | Médio por trás do ombro, 35mm | Manhã, contraluz |
| 05 | 2 | Worm's eye extremo, 24mm (keyframe do curso) | Manhã, contraluz |
| 06 | 2 | Close, 85mm, folha desfocada na frente | Manhã, verde rebatido |
| 07 | 3 · A rua racha | Aberto e baixo, 24mm | Sol alto |
| 08 | 3 | Rente ao chão, lente sonda 24mm | Sol alto |
| 09 | 3 | Médio, 50mm, instante congelado | Sol alto |
| 10 | 4 · A fuga | Lateral acompanhando, 50mm | Sol alto |
| 11 | 4 | Close frontal, 85mm | Sol alto, contraluz |
| 12 | 4 | Plongée alto e aberto, 35mm | Sol alto |
| 13 | 5 · A escada | Contra-plongée aberto, 24mm | Início da tarde |
| 14 | 5 | Insert da mão, 85mm | Início da tarde |
| 15 | 6 · O topo | Médio, 35mm | Fim de tarde dourado |
| 16 | 6 | Por trás do ombro, aberto, 24mm (com a cidade) | Fim de tarde dourado |
| 17 | 6 | Médio, 50mm, altura dela sentada | Fim de tarde dourado |
| 18 | 7 · Paz | De cima (top-down), 35mm | Pôr do sol |
| 19 | 7 | Rente ao chão, 24mm, botas contra o céu | Pôr do sol |
| 20 | 7 | Extremo aberto, 24mm, plano final | Pôr do sol |

Salve cada bloco abaixo como `frames/fNN.txt`.

### Ato 1 · Manhã comum

**f01**
```
Wide shot, 35mm, eye level. A small tidy city apartment bedroom on a clear, silent morning. She stands in front of a tall floor mirror leaning against a white wall, finishing getting ready, seen both from behind and in the mirror reflection. Soft cool morning light through a window with sheer curtains, pale dust in the air, a neatly made bed, a wooden chair with a jacket. An ordinary day: no plants anywhere in the room.
```

**f02**
```
Close-up over her shoulder into the mirror, 85mm, shallow depth of field. Her hands calmly adjust the slouchy grey beanie, fingertips tugging the knit back into place; in the reflection her face is relaxed and neutral, eyes on herself. Silver chain bracelets catch the soft window light. Cool clear morning tones, no plants anywhere.
```

**f03**
```
Top-down insert, 100mm macro. On a small wooden entryway table, her hands hold the navy pinstripe tote bag open, checking that a worn paperback book is inside; a set of keys and a ceramic dish beside it. Silver rings and chain bracelets in sharp focus, the book's cream pages softly lit by morning light from the side. Calm, routine gesture.
```

### Ato 2 · O portão

**f04**
```
Medium shot from behind her right shoulder, 35mm. She pushes open a tall black ornate wrought-iron gate in a white-painted brick gatehouse and freezes mid-step, one boot lifted. Beyond her hand, the walls, the ceiling and the iron bars are completely overtaken by thick twisting vines, roots and giant tropical leaves that were not there yesterday. Morning backlight streams through the opening, haze glowing, leaves backlit translucent green.
```

**f05**
```
Extreme low-angle worm's-eye shot, 24mm wide lens. She stands in the open doorway of the white-painted brick gatehouse, tall black wrought-iron gates swung open. Her lips are parted, eyes glancing sideways off-frame, alert, sensing danger. Vegetation completely dominates the scene: massive dense ivy, thick twisting vines and giant tropical leaves (monstera, banana leaves, ferns) swallow the walls and the gates, wrapping around the iron bars, hanging from the ceiling, creeping over the frame edges. Roots crack the white bricks, moss covers the surfaces, foreground leaves out of focus framing the lens. Lush, overwhelming, alive, slightly menacing overgrowth. Clear morning backlight through the opening, cool rim light on her hair, green bounce light on skin, soft haze, shallow depth of field on the foreground leaves.
```

**f06**
```
Close-up, 85mm, eye level, a blurred monstera leaf edge in the foreground. Her face turned three-quarters, eyes darting sideways, suspicious, jaw tight, shoulders raised, body on alert. A thin vine tendril curls from the wall toward her shoulder, just out of her sight. Green bounce light on her skin, cool morning rim light on her hair, soft haze.
```

### Ato 3 · A rua racha

**f07**
```
Wide low-angle shot, 24mm, camera near the ground in the middle of an empty city street lined with parked cars and low apartment buildings. The asphalt is splitting open in long jagged cracks running toward the camera, thick roots and green shoots bursting up through the fissures, chunks of tar and dust lifting into the air. She stands small on the sidewalk at the far edge of frame, just out of the overgrown gate, staring at the ground. Bright high sun, short hard shadows, dust glowing.
```

**f08**
```
Ground-level macro, 24mm probe lens skimming the asphalt. A thick gnarled root tears up through a fresh crack in the street, green shoots uncurling from it, fragments of black asphalt and grit suspended in mid-air, sharp detail on the torn tar edge. In the soft-focus background, her black knee-high boot takes a hesitant step back. Hard midday sun, crisp texture.
```

**f09**
```
Medium shot, 50mm, frozen instant, high shutter speed. A parked silver hatchback a few meters ahead on the empty street, its interior packed with dense vegetation pressing against every window. The side window bursts outward in an explosion of glass shards and leaves overflowing through the frame, vines spilling down the door. She is visible soft in the background, flinching, one arm raised. Hard midday sun, glittering glass particles.
```

### Ato 4 · A fuga

**f10**
```
Tracking side-profile shot, 50mm, lateral dolly at running speed, background streaked with motion blur. She sprints flat-out along the cracked street from right to left, long black hair flying, tote bag bouncing against her hip, boots pounding the broken asphalt. Behind her, a wall of jungle surges down the street, trees and vines swallowing lampposts and cars. Hard midday sun, dust and flying leaves.
```

**f11**
```
Frontal close-up, 85mm, handheld feel, shallow depth of field. She looks back over her shoulder while running, scared and breathless, mouth open mid-gasp, strands of black hair stuck across her face, a light sheen of sweat, beanie slipping. Behind her, out of focus, a dark green mass of foliage fills the street. Hard sun from behind rimming her hair.
```

**f12**
```
High-angle wide shot, 35mm, from a third-floor window looking down the street. She is small in the frame, running toward the bottom of the image; behind her, the jungle front advances down the street like a green wave, trees rising out of the asphalt, vines climbing the facades, a car already disappearing under leaves. Clear line between the untouched grey street ahead of her and the green chaos behind. Hard midday sun, long straight shadows of lampposts.
```

### Ato 5 · A escada

**f13**
```
Low-angle wide shot, 24mm, looking up the side of a five-story red-brick building. A black metal exterior staircase zigzags upward; she climbs as fast as she can, two steps at a time, halfway up, hair whipping. Vines race up the lower flights right behind her, wrapping the steps and railings. Early afternoon sun, bright sky above the roofline.
```

**f14**
```
Insert, 85mm, shallow depth of field. Her hand with chunky silver chain bracelets grips the metal railing, already covered with fresh leaves and curling tendrils. Just below, vines coil up the grated steps toward her black boot as it lifts to the next step. Early afternoon sun, sharp shadows through the metal grating.
```

### Ato 6 · O topo

**f15**
```
Medium shot, 35mm, eye level. On a concrete rooftop terrace, she stops and bends over with her hands on her knees, catching her breath, cheeks flushed, hair stuck to her face, beanie askew, chest heaving. Moss and small plants are starting to creep over the edges of the rooftop around her. Warm golden late-afternoon light from the side, long shadows, haze in the air.
```

**f16**
```
Wide shot over her shoulder, 24mm, from behind her. She stands at the edge of the rooftop, small against the view, looking out at the entire city turning into a forest, exactly like the city in Image 2: skyscrapers wrapped in vines, trees bursting from windows, streets turned into green canyons, the transformation still spreading. Warm late-afternoon sun, backlit leaves glowing, atmospheric haze fading the distant towers. Awe and stillness.
```

**f17**
```
Medium shot, 50mm, camera at her seated eye level. Instead of running, she sits cross-legged on the rooftop floor, calmly opens the navy pinstripe tote and pulls out the worn paperback book, a faint relieved smile. Behind her, out of focus, the green skyline glows. Warm golden late-afternoon light on her face, a few leaves drifting through the frame.
```

### Ato 7 · Paz

**f18**
```
Top-down overhead shot, 35mm, camera directly above. She lies on her back on the rooftop floor, legs crossed with knees up and boots in the air, holding the open paperback above her face, reading, peaceful. Moss, small ferns and leaves have crept over the concrete around her like a carpet. Warm sunset light raking across the surface, long soft shadows, amber and magenta tones mixing with deep greens.
```

**f19**
```
Ground-level low angle, 24mm, camera on the rooftop floor at her boots. In the foreground, her crossed black knee-high boots point up against a deep orange and magenta sunset sky; beyond them, the skyline of towers disappears under the jungle, as in Image 2. Her hand holding the book is just visible at the edge of frame. Sun touching the horizon, golden halation.
```

**f20**
```
Extreme wide final shot, 24mm, from a slightly higher neighboring rooftop. Her tiny figure lies reading on the rooftop terrace in the lower third of the frame, boots up. All around, the entire city has become nature, as in Image 2: towers reduced to green silhouettes, the forest stretching to the horizon, birds crossing the sky. Deep orange sunset turning to blue hour, calm, silent, at peace. The city turned into nature, and she found peace.
```

## Gerando na CLI

Teste primeiro os dois frames mais difíceis (f05, que tem o nível de detalhe do curso, e f16, que junta personagem e cidade) em qualidade básica. Se a personagem e o look estiverem certos, rode o resto em alta.

```bash
mkdir -p out && for f in frames/f*.txt; do n=$(basename "$f" .txt); refs="--image refs/girl_sheet.png"; case $n in f16|f19|f20) refs="$refs --image refs/cidade.png";; esac; higgsfield generate create seedream_v5_lite --prompt "$(cat "$f") $(cat sufixo.txt)" $refs --aspect_ratio 16:9 --quality high --wait --json > "out/$n.json"; done
```

Notas:

- "Seedream 5.0 2K" do curso = `seedream_v5_lite` com `--quality high` na CLI (confirmar com `higgsfield model get seedream_v5_lite`, ver [seção 16 do FRAMEWORK](../FRAMEWORK.md#16-em-aberto-a-validar)).
- Se um frame errar a personagem, não reescreva o prompt inteiro: confira se a referência foi junto e se o frame pede algo que a folha não mostra.
- Para virar vídeo, cada frame é o **frame de partida** de um clipe, no ângulo do primeiro corte.
