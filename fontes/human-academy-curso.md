# Human Academy · prompts usados no curso

Material bruto, do jeito que veio das aulas (colado pelo JP em 2026-09-26). A interpretação de cada um está no [FRAMEWORK.md](../FRAMEWORK.md#11-o-método-human-academy-lido-prompt-a-prompt).

## 1. Keyframe editorial (imagem)

```
Extreme low-angle worm's-eye shot, cinematic editorial photograph. A young East Asian woman with very long straight jet-black hair stands in the open doorway of a white-painted brick gatehouse with tall black ornate wrought-iron gates swung open. She wears a slouchy heather-grey knit beanie, a black sleeveless fitted tank top with a twisted knot detail at the chest, oversized black cargo bermuda shorts, black slouchy knee-high leather boots, a navy pinstripe tote bag on her shoulder, chunky silver chain bracelets and silver rings. Her lips are parted, eyes glancing sideways off-frame, alert, sensing danger.
Vegetation completely dominates the scene: massive dense ivy, thick twisting vines and giant tropical leaves (monstera, banana leaves, ferns) swallow the walls and the gates, wrapping around the iron bars, hanging from the ceiling, creeping over the frame edges. Roots crack the white bricks, moss covers the surfaces, foreground leaves out of focus framing the lens. Lush, overwhelming, alive, slightly menacing overgrowth.
Late-afternoon backlight through the opening, warm rim light on her hair, green bounce light on skin, soft haze. Shot on 24mm wide lens, shallow depth of field on foreground leaves, Kodak Portra 400 film grain, rich deep greens against black and white, high detail, 16:9.
```

## 2. Roteiro → 20 imagens (pedido ao agente)

```
gerar 20 imagens desse roteiro, cena a cena, usando a cli do higgsfield modelo sedream 5.0 2k

Numa manhã clara e silenciosa, ela termina de se arrumar diante do espelho. Ajeita o gorro com calma, pega a bolsa e confere se o livro está lá dentro. É um dia como outro qualquer.
Ela abre o portão para sair e para no meio do passo. As paredes, o teto e as grades estão tomados por cipós, raízes e folhas gigantes que não estavam ali ontem. Olha para o lado, desconfiada, com o corpo em alerta. Algo mudou.
Na rua, o asfalto começa a rachar. Raízes e brotos rompem o chão com força, abrindo fendas por toda a rua vazia. Um pouco adiante, um carro estacionado foi tomado por dentro pela vegetação. As plantas pressionam o vidro até ele estourar e as folhas transbordam pela janela.
Ela corre. Olha para trás, assustada e ofegante, com o cabelo no rosto, enquanto a selva avança atrás dela sem parar.
Ela encontra uma escada externa e sobe o mais rápido que consegue, com a mão no corrimão já coberto de folhas e os cipós subindo pelos degraus logo atrás. Precisa chegar ao ponto mais alto.
No topo do prédio, ela para e recupera o fôlego. Olha ao redor: a cidade inteira está virando floresta. E então, em vez de continuar fugindo, ela senta, abre a bolsa com calma e tira o livro.
O sol se põe e ela está deitada no chão do terraço, com as pernas cruzadas e as botas para o alto, lendo tranquila. Ao fundo, os prédios desaparecem sob a selva. A cidade virou natureza, e ela encontrou paz.
```

## 3. Meta-prompt: Character Sheet

```
Elabore um prompt para criar um Character Sheet. Quero uma Asian girl muito estilosa, com estética street fashion moderna, cool e contemporânea. Asian Girl, com gorro, cabelo longo, gorro, acessórios, botas e principalmente o caimento oversized e natural das roupas. Mostre ela de frente, 3/4, perfil e costas, além de expressões importantes para o filme, como neutra, assustada, ofegante e determinada. Inclua também alguns detalhes dos acessórios e peças do look, tudo em fundo neutro de estúdio, com acabamento fotográfico hiper-realista e aparência de material profissional de pré-produção de cinema.
```

## 4. Meta-prompt: asset de locação ultra wide

```
Quero o prompt para criar um asset (IMAGEM ULTRA WIDE) de uma cidade moderna completamente dominada pela natureza, com prédios cobertos por plantas gigantes, raízes, cipós e árvores, como se uma floresta tivesse engolido toda a cidade. Quero uma visão ampla que mostre bem a escala dessa transformação, com uma atmosfera ao mesmo tempo bonita, surreal e ameaçadora, mantendo a estética cinematográfica e hiper-realista do filme.
```

## 5. Pedido de animação (imagem → vídeo)

Anexo: foto de uma menina (a imagem de partida).

```
animar essa imagem no higgsfield cli usando o seedance 2.5 30 segundos, 1080, multishot

clipe publicitário cool, surreal e bem fashion, com movimentos de câmera dinâmicos, cortes criativos, pausas dramáticas e sensação hiper-realista. A menina brinca com uma maçã verde, joga ela para cima e, de forma surreal, ela se multiplica em centenas de maçãs flutuando pelo céu e como sensação de scroll escolhendo as maçãs passando para o lado, faz a seleção. Quero uma narrativa visual divertida, impactante e com estética de fashion film contemporâneo
```

## 6. Prompt de nova cobertura a partir de um vídeo (vídeo → mais vídeo)

Colado pelo JP em 2026-09-26.

```
BASE
Use the attached video as the primary reference and create 10 seconds of NEW shots that feel like additional footage from the exact same scene.

ANALYZE THE REFERENCE FIRST
Identify the visible subjects, their appearance, wardrobe, actions, important objects and the layout of the location.

Identify the reference's lighting direction, light quality, exposure, color palette, contrast, shadows, highlights, depth of field, lens character and image texture.

Use these observed characteristics as fixed continuity rules throughout the generated video. Infer them directly from the reference; do not require a written description.

PRESERVE THE ORIGINAL PHOTOGRAPHY
Match the reference's visual treatment in EVERY shot, including close-ups, wider views and fast inserts.

Keep the same apparent time of day and atmosphere. Do not automatically brighten, beautify or restyle the scene.

CREATE NEW COVERAGE
Show different camera angles, closer details and natural continuations of the action already happening in the video. Include relevant gestures, objects and environmental details from that same situation.

Preserve the subjects' identities, clothing and important object details. Keep the location spatially coherent. Avoid inventing unrelated people, props or activities.

EDITING AND CAMERA
Alternate held moving shots with bursts of three or four quick cuts, then return to a longer shot.

Begin with a new angle held for about two seconds. Follow with quick action details, a sustained lateral view, another short burst of inserts and a wider closing shot.

Use camera movements motivated by the action: gentle tracking, push-ins, pullbacks, low angles, high angles and short arcs. Let the camera follow the subjects' gestures.

Use real hard cuts between distinct shots. Do not morph one angle into another. Keep anatomy and motion natural.

REFERENCE IMAGES AND OUTPUT
If additional reference images are attached, use them to understand appearance, photography and the location. Do not reproduce them as static shots.

Generate new footage that belongs to the original scene. No added text, logos, dialogue or music.
```

## 7. Resultados do curso gerados no ChatGPT (filme da maçã verde)

O padrão de qualidade a perseguir. Imagens em [human-academy-imagens/](human-academy-imagens/).

- `maca_character_sheet_chatgpt.jpg`: character sheet da menina da maçã. Quatro vistas de corpo inteiro (frente, 3/4, perfil, costas) e dois closes de expressão sobrepostos embaixo (olhando para cima, boquiaberta; sorriso de canto), em fundo de papel cinza de estúdio com queda de luz e sombra no chão.
- `maca_still_fisheye_chatgpt.jpg`: still do filme. Olho de peixe de baixo para cima, sol duro, céu azul cobalto com nuvens, ela sentada numa cadeira azul de arquibancada segurando a maçã, joelhos enormes em primeiro plano e crocs menta com pins de maçã.

## 8. Previs no Blender (hero frame → animação em argila → Seedance 2.5)

Versão completa, do PDF enviado pelo JP em 2026-09-26 (substitui a colagem anterior, que chegou cortada). Original em [human-academy-imagens/PROMPT-BASE-BLENDER.pdf](human-academy-imagens/PROMPT-BASE-BLENDER.pdf).

```
You are my PREVIS DIRECTOR inside Blender.

The attached HERO FRAME is the approved visual reference. Reconstruct it as a simple,
editable 3D scene matching its composition, camera perspective, relative scale and major
objects.

The hero frame already defines the final appearance. Your job is to create the clearest
spatial simulation of the shot, not a beautiful 3D render.

We will use the Blender animation as a clay / white-model motion reference for Seedance
2.5, together with the original hero frame.

PRIORITIES

1. Camera 2. Composition 3. Blocking 4. Timing 5. Spatial relationships 6. Character/object
trajectories

Visual detail is NOT a priority.

BUILDING RULES

Use simple geometry whenever possible. Use primitive shapes for architecture and props
unless their real silhouette affects the composition.

Characters can be simple mannequins or low-detail proxies.

Use neutral matte clay materials. Avoid decorative textures, logos, text and unnecessary
detail.
Everything must remain editable.
Keep logical objects separated and clearly named.

CAMERA
Treat the camera as the most important object in the scene. Match the approved hero frame
as the starting composition before animating.
Define:
- starting camera position
- ending camera position
- camera height
- lens / field of view
- camera target
- path
- acceleration/deceleration
- framing at important beats
- foreground occlusion
- parallax
Do not use random camera movement.

ACTION
Break the performance into clear timed beats.

For each beat define:
- subject starting position
- subject ending position
- movement
- interaction
- screen direction
- camera relationship
Use simple animation cheats when they communicate the idea better than complex
animation.

PHYSICAL REALISM PASS
Review the entire animation as if you were a senior cinematographer, camera operator, stunt
animator and physics animator preparing this previs for live-action production.
The goal is NOT perfect mathematical motion.
The goal is motion that feels physically filmed in the real world.
Do not redesign the scene, composition or story.
 Preserve all approved beats, blocking and
final framing.
Your job is to remove anything that feels like:
 CG animation,
 robotic keyframes,
 perfect
spline motion,
 linear interpolation,
 floating objects,
 weightless movement,
 mechanical
camera motion,
 unnatural acceleration,
 or instant starts and stops.

1. CAMERA — MAKE IT FEEL PHYSICALLY OPERATED
First identify what kind of real camera system could physically create this shot:
handheld operator

shoulder camera
Steadicam / gimbal
dolly
crane / techno-crane
slider
vehicle-mounted camera
drone
robotic arm
combination of physically plausible systems
Choose the closest real-world camera logic and rebuild the motion around its physical
behavior.
The camera must have MASS and INERTIA.
Never allow the camera to instantly:
 start,
 stop,
 change direction,
 change height,
 or rotate.
Every major camera movement must contain believable:
anticipation → acceleration → travel → deceleration → settle.
Avoid generic Ease In / Ease Out.
Acceleration must respond to the distance being traveled, camera mass and intended
energy of the shot.
Inspect the animation curves manually.
Remove:
 perfectly symmetrical curves,
 linear-looking transitions,
 constant-speed CG gliding,

abrupt tangent changes,
 and unnecessary keyframes.
Favor continuous velocity and acceleration.

Avoid sudden changes in acceleration (“jerk”) unless motivated by an intentional physical
impact.

2. REMOVE THE “3D CAMERA” FEEL
The camera should never feel like a floating point moving through coordinates.
It should feel attached to a physical device occupying real space.

Introduce extremely subtle organic imperfections appropriate to the chosen camera
system.
Do NOT add random camera shake.
Imperfections must have physical causality.
For handheld:
 use subtle human body drift, breathing, small delayed corrections and
imperfect stabilization.
For Steadicam/gimbal:
 keep the shot smooth but allow tiny residual inertia, slight vertical drift
and delayed rotational correction.
For dolly:
 movement should be highly stable, with strong horizontal consistency and
extremely subtle start/stop inertia.
For crane:
 respect the arc and mechanical radius of the arm.
For drone:
 respect momentum, banking, acceleration limits and delayed directional
correction.
Avoid perfectly locked XYZ motion unless the actual camera rig would produce it.
3. PAN / TILT / ROTATION
Camera rotation and camera translation must not feel like independent sliders.
They should influence each other naturally.
When following a moving subject, allow the camera framing to react with a slight human
delay rather than mathematically tracking the subject perfectly.
Do not keep the subject unnaturally locked to exactly the same screen coordinate.
Allow tiny composition corrections.
For fast reframing:
 introduce a believable overshoot followed by a small correction when
appropriate.
For slow cinematic movements:
 prioritize stability, controlled inertia and smooth acceleration.
Never use artificial constant rotation.
4. LENS AND PARALLAX
Review whether the virtual lens matches the perceived camera movement.
Avoid changing focal length merely to fake camera movement.
Prefer real camera translation whenever possible.
Check foreground, midground and background parallax.
The amount of parallax must agree with:
 camera distance,
 lens choice,
 camera velocity,
 and
scene scale.
Make sure scale feels physically believable.
If the camera passes close to foreground objects, their screen-space velocity should
increase naturally.
Do not allow objects to feel like flat layers sliding independently.
5. CHARACTER AND OBJECT PHYSICS
Review every animated subject for:
mass,
 gravity,
 momentum,
 friction,
 contact,
 balance,

inertia,
 drag,
 collision,
 and follow-through.
Nothing should begin or stop moving instantly unless physically justified.

For living characters:
Movement should originate from shifts in center of mass.
Before major movement, create believable preparation or weight transfer.
Feet must make convincing contact with the floor.
No foot sliding.
Pelvis and torso should respond to locomotion.
Head movement should not be perfectly synchronized with the torso.
Arms and secondary body parts should contain natural follow-through.
After large movements, allow subtle stabilization.
Avoid symmetrical robotic motion.
6. OBJECT WEIGHT
Every object must visually communicate its mass.
Heavy objects:
accelerate more deliberately,
 take longer to stop,
 have stronger momentum,
 and create
more noticeable reaction during impacts.
Light objects:
 respond faster,
 are more affected by air resistance,
 and may oscillate or settle
differently.
Do not animate all objects with the same easing profile.
Use different acceleration, damping and settling behavior according to material and mass.
7. GRAVITY AND FALLING MOTION
Any unsupported object must respect gravity.
Review falling arcs and vertical acceleration.
Do not use visually linear falling motion.
Thrown objects must follow believable ballistic trajectories unless another force is acting on
them.
After impact:
 consider bounce,
 compression,
 sliding,
 rotation,
 friction,
 and settling.
Avoid exaggerated simulation unless the scene intentionally requires it.
8. COLLISIONS AND CONTACT
Inspect every moment where:
 feet touch floors,
 hands touch objects,
 characters sit,
objects land,
 objects collide,
 doors move,
 vehicles interact with surfaces,
 or subjects cross
close to environment geometry.
There must be no visible penetration, hovering or unexplained gap.
Contact should create an appropriate reaction.
When one object pushes another, motion must propagate through the interaction.
When a character touches something, their body should subtly react to the force.
9. SECONDARY MOTION
Add only secondary motion that strengthens realism.
Examples:
subtle body stabilization,
 hair lag,
 cloth follow-through,
 object vibration after impact,

suspension movement,
 small camera settling,
 environmental reaction,
 delayed movement in
loose components.
Secondary motion should FOLLOW the primary force.
It should never look like independent decorative animation.
10. TIMING
Review the scene at full playback speed.
Do not judge realism from isolated frames.
Identify any moment where the viewer would subconsciously feel:

“this moved too quickly”
 “this stopped too perfectly”
 “this feels weightless”
 “this feels
animated”
 “the camera feels like a computer”
 “the character feels like a mannequin”
Fix those moments.
Realistic timing is more important than preserving exact keyframe timestamps.

You may adjust timings slightly while preserving the approved narrative beats.
11. DO NOT OVER-SMOOTH
Realism does NOT mean making every curve smooth.
Real movement contains:
 changes of intention,
 micro-corrections,
 impact,
 hesitation,

momentum,
 and recovery.
Preserve motivated irregularity.
Remove mathematical perfection without introducing noise.
The final result should feel DIRECTED, not randomized.

12. FINAL CAMERA REALISM CHECK
Watch the animation once while ignoring the scene and looking only at the camera behavior.
Ask:
Could a real camera system physically perform this move?
Does the operator seem to anticipate the action?
Does the camera have inertia?
Does it accelerate and decelerate naturally?
Does framing breathe slightly instead of remaining mathematically perfect?
Does it feel like someone filmed this rather than a 3D viewport camera moving between
keyframes?
If not, revise it.
13. FINAL ACTION REALISM CHECK
Watch again while ignoring the camera.
For every moving subject ask:
Where is its weight?
What force started this motion?
What force stops it?
Where is the center of mass?
What is touching the ground?
What should continue moving after the main action stops?
Does gravity affect it?
Does the timing match its apparent mass?
Fix anything without a convincing physical answer.
14. FINAL DELIVERY
After the realism pass:
Preserve the original approved shot design.
Clean unnecessary keyframes.
Refine animation curves.
Correct physically implausible acceleration.
Add restrained secondary motion.
Verify contacts and collisions.
Verify camera inertia.
Verify real-world camera feasibility.
Generate a new real-time viewport playblast.

Show me:
full playblast
camera velocity over time
the main camera animation curves
frames at 0%, 25%, 50%, 75% and 100%
Do not proceed to final generation until the motion no longer feels like a Blender animation.
TARGET:
It should feel like a real camera recorded a real physical event, and Blender merely
reconstructed it.
```
