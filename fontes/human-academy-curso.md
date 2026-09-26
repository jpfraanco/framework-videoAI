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
