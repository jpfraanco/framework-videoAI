# Asset de locação ultra wide · cidade engolida pela selva (exercício Human Academy)

Resposta ao meta-prompt 4 do curso ([fontes/human-academy-curso.md](../fontes/human-academy-curso.md)).

Teoria por trás: [FRAMEWORK.md, seção 4.4](../FRAMEWORK.md#44-locações).

## Decisões

- **Estrutura em blocos**, como o estádio do tutorial dos fones da Higgsfield: primeiro plano, cidade, escala, atmosfera, luz, cor, câmera e proibições.
- **Escala com objetos conhecidos**: faixa de pedestre, semáforo, ônibus, copas de árvore chegando ao 20º andar. Sem régua, a cidade vira maquete.
- **Transformação em andamento**: alguns prédios já viraram silhueta verde, outros ainda mostram vidro. É o que dá a sensação de "está acontecendo agora" e ameaça.
- **Beleza e ameaça ao mesmo tempo**: luz dourada e folhas translúcidas (bonito), silêncio, cidade parada e raízes rachando concreto (ameaçador).
- **Mesma estética do filme**: Kodak Portra 400, verdes profundos dominando, como no keyframe do portão.
- **Fim de tarde**: é o momento do roteiro em que ela chega ao topo do prédio e olha em volta. Assim o asset serve direto como frame da cena 6.
- **Primeiro plano do terraço**: amarra o asset ao ponto de vista dela.

## Prompt

```
Ultra-wide cinematic establishing shot of a modern metropolis completely swallowed by a forest, seen from the edge of a high rooftop terrace at late afternoon, as if the jungle devoured the entire city in a single night.

THE FOREGROUND: the edge of a concrete rooftop terrace cracked open by thick roots, a rusted railing wrapped in ivy, moss and ferns spilling over the ledge, giant monstera and banana leaves framing the lower corners slightly out of focus.

THE CITY: dozens of glass-and-steel skyscrapers and mid-rise apartment blocks stretching to the horizon, every facade wrapped in dense ivy and hanging curtains of vines; full-grown trees bursting out of broken windows and balconies; massive roots pouring down the sides of towers like frozen waterfalls, splitting the concrete; rooftop water tanks and antennas buried in foliage; a highway overpass sagging under a thick blanket of vines; the streets below turned into green canyons, cars half-buried in leaves. The transformation is still in progress: some towers are already solid green silhouettes, others still show patches of glass reflecting the sky.

SCALE: tiny empty streets far below, visible crosswalk stripes, a green-covered traffic light and a lone abandoned bus give the true scale; tree canopies reach the twentieth floor; the city runs uninterrupted to the horizon. No people anywhere.

ATMOSPHERE: beautiful, surreal and quietly menacing at the same time. Humid haze layered between the buildings, pollen and seeds drifting through shafts of light, a flock of birds circling a distant tower, the heavy silence of a city that stopped.

LIGHT & SKY: warm low late-afternoon sun from frame left, long shadows raking across the facades, backlit leaves glowing translucent green, atmospheric perspective fading the most distant towers into pale blue-green, towering cumulus clouds catching golden light.

COLOR GRADE: rich deep greens dominating, concrete greys and black steel as secondary, a small accent of warm golden sunlight; Kodak Portra 400 film grain, gentle halation around the sun, naturalistic and restrained saturation, not a fantasy painting.

CAMERA & LENS: large-format cinema camera, 24mm wide rectilinear lens, slightly elevated angle, deep focus from the rooftop leaves to the horizon, straight verticals, no fisheye distortion.

Photorealistic, hyper-detailed, ultra-wide 21:9 panorama. No text, no readable signage, no logos, no people, no animals in the foreground, no CGI or video-game look.
```

## Onde gerar

O Seedream V5 Lite não tem 21:9 na CLI. Opções:

```bash
higgsfield generate create soul_location --prompt "$(cat cidade.txt)" --aspect_ratio 21:9 --wait
```

```bash
higgsfield generate create cinematic_studio_2_5 --prompt "$(cat cidade.txt)" --aspect_ratio 21:9 --resolution 4k --wait
```

```bash
higgsfield generate create seedream_v4_5 --prompt "$(cat cidade.txt)" --aspect_ratio 21:9 --quality high --wait
```

Se quiser o mesmo look do Seedream 5, gere em 16:9 com `seedream_v5_lite` e estenda para os lados com `outpaint`.

## Variações úteis

- **Sem o terraço** (para ser fundo de qualquer cena): tire o bloco `THE FOREGROUND` e troque o ponto de vista por "seen from a drone high above the rooftops".
- **Versão "antes"**: mesma câmera, mesma cidade, sem nenhuma planta, "clear quiet morning". É o par A/B que dá impacto na montagem.
- **Pôr do sol** (cena final): troque `LIGHT & SKY` por "sun touching the horizon, deep orange and magenta sky, the jungle-covered skyline in near silhouette".
