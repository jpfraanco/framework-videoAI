# Prompt para o ChatGPT · roteiros Heineken Ultimate e Jack Daniel's

Brief completo para pedir os dois comerciais de 15 s ao ChatGPT, levando junto o método do [FRAMEWORK.md](../FRAMEWORK.md). Copie tudo o que está dentro do bloco.

- Preencha o `[contexto de uso]` antes de colar.
- O último bloco ("Direções que já exploramos") é opcional: mantenha para o ChatGPT propor ideias diferentes das nossas, apague para comparar sem influência.
- O pedido vem em duas etapas (conceitos primeiro, roteiro completo depois) para a resposta não ficar rasa por falta de espaço.

````text
# PAPEL
Você é diretor(a) de criação e diretor(a) de cena de comerciais feitos com IA generativa (imagem + vídeo). Pense como cineasta, não como quem resume roteiro: decida bloqueio, lente, luz, ritmo e som.

# A DEMANDA
Quero dois comerciais DINÂMICOS de 15 segundos:
1. Heineken® Ultimate
2. Jack Daniel's® Old No. 7

- Contexto de uso: [preencher: pitch para a marca / portfólio da unflat, estúdio de tecnologia criativa / job]. São peças-conceito, não campanhas oficiais.
- Produção: imagens de referência no ChatGPT (GPT Image) e no Seedream; vídeo no Seedance 2.5 pelo Higgsfield, numa geração só de 15 s com vários planos (multi-shot), 1080p, usando imagem de partida + imagens de referência (produto, personagens, locação).
- Formato: 16:9, com a ação importante no terço central para recortar em 9:16 depois.
- O vídeo gerado não tem fala nem locução, só som diegético. Música, cartela e packshot real entram na edição.

# FATOS DOS PRODUTOS
Use só estes. Qualquer outro dado, marque [confirmar com a marca].

Heineken® Ultimate:
- Lager puro malte, 3,5% de álcool, sem glúten, 30% menos calorias que a Heineken regular (97 kcal a garrafa; 29 kcal por 100 ml).
- Mesmas leveduras da marca, produzida em tanques horizontais; o desafio foi manter o sabor fiel à Heineken regular.
- Lançamento global com o Brasil como primeiro mercado (maio de 2026).
- Posicionamento oficial: "equilíbrio, moderação e novas formas de socialização". Público: quem quer continuar com álcool, num produto mais equilibrado.
- Assinatura oficial: "30% menos caloria. Sem glúten. Sem dúvida, Heineken®."

Jack Daniel's® Old No. 7 (confirmar cada item com o guia da marca):
- Tennessee Whiskey, destilaria em Lynchburg, Tennessee.
- Água de nascente de caverna de calcário.
- Filtragem gota a gota em carvão de bordo (sugar maple) antes do barril ("Lincoln County Process").
- Barris novos de carvalho branco, queimados por dentro.
- Garrafa quadrada, rótulo preto.

Embalagens: vou mandar fotos reais das garrafas. Não invente o visual do rótulo.

# ESTILO QUE QUEREMOS (referências que já estudamos)
1. "Cinematic Headphones", comercial da Higgsfield feito com Seedance: um herói com o produto travado por referência numa situação cômica que escala até o desfecho (ele acalma o chefe furioso colocando os fones nele). Tem uma montagem de café em cortes secos "estilo comercial de carro" (pó, chama, café saindo, gole, cada ação na batida), um plano com a câmera presa ao corpo do ator travada no produto enquanto o mundo passa borrado, câmera no chão com o ator correndo por cima da lente, super teleobjetiva de transmissão esportiva, e um match cut entre cenas pelo mesmo gesto (o toque no fone).
2. Fones rosa no parque (guia do Seedance 2.5): um efeito surreal com UMA regra física só (cada passo dela espalha uma onda de cor e todo mundo congela), fechando numa piada visual (a avó congelada e o cachorro dela, vivo, latindo).
3. Nosso comercial do BORA: 8K IMAX commercial, lente anamórfica, luz motivada, a cor da marca como única fonte saturada do quadro.

"Dinâmico" para nós = lente e movimento diferentes a cada plano, cortes secos na batida, pelo menos um momento de câmera lenta de verdade (120 fps tocado a 24 fps) e um fechamento limpo de produto. Humor e surpresa são bem-vindos, sem virar pastelão.

# MÉTODO QUE JÁ VALIDAMOS (siga à risca)
1. O frame manda, o prompt só sugere: o Seedance copia com fidelidade a imagem de partida; o que não está nela, ele inventa. Detalhe que não pode errar vai para a imagem, não para o texto.
2. Trave os assets antes de mover a câmera: produto, personagens, locação e objetos de cena viram imagens de referência com nome único (@tag), reaproveitadas em todos os planos.
3. Referência vence descrição. Uma referência por elemento; conjunto enxuto.
4. Um rosto por referência de personagem: folha com close do rosto + corpo inteiro de frente e de costas, fundo cinza, e o rosto apagado no painel de corpo inteiro.
5. Mudou o estado do personagem (molhado, suado), gera uma referência nova com nome próprio.
6. Posição que importa vai num mapa esquemático visto de cima, usado como referência.
7. Diga o que NÃO acontece: no music, no extra people, no readable text, no 3D, no CGI sheen.
8. Plano a plano: cada plano com tempo exato, enquadramento, lente (em mm e em graus de campo de visão), movimento, ação, terminando em "Hard cut."
9. Números em vez de adjetivos: tamanho em cm, distância em metros, segundo exato de cada ação, % do quadro.
10. Cerca de 2 a 3 segundos por momento. 15 s comportam 5 a 8 planos em ritmo de comercial. Curto demais, o modelo pula ação.
11. Efeito surreal = uma regra física só, repetível, com gatilho claro e hora para acabar.
12. Direção de gesto, não de adjetivo. Não "ela gosta", e sim "os olhos fecham meio segundo, os ombros descem, um canto da boca sobe". Dança ou coreografia, passo a passo.
13. Cortes caem na batida; match cut por gesto ou forma; cada plano termina onde o próximo começa.
14. Rótulo e texto saem desfocados ou ilegíveis no vídeo; o packshot real e a cartela entram na edição. No prompt, o produto é citado pela tag (@heineken_ultimate, @jd_bottle), nunca pelo nome da marca.
15. Líquido, espuma, gelo, condensação e fogo precisam de física descrita (velocidade, direção, como se comportam), senão viram plástico.
16. Imagem é barata, vídeo é caro: aponte o plano mais difícil para testarmos primeiro em 480p.

Lentes em graus (campo de visão diagonal, full frame): 12° ≈ 200 mm (detalhe em tele) · 18° ≈ 135 mm · 29° ≈ 85 mm (retrato) · 47° ≈ 50 mm (normal) · 63° ≈ 35 mm · 84° ≈ 24 mm (grande angular) · 107° ≈ 16 mm.

# REGRAS DE MARCA E DE PUBLICIDADE DE ÁLCOOL (Brasil)
- Todas as pessoas com 25 anos ou mais, e com aparência disso.
- Nada de direção de veículo, consumo excessivo ou embriaguez; nada de sugerir sucesso, sedução ou desempenho (esportivo, sexual, profissional) por causa da bebida.
- Heineken Ultimate: nunca sugerir que dá para beber mais por ser mais leve. Evitar academia, atleta e esporte de performance.
- Consumo, se aparecer, moderado: um gole, um brinde.
- Cartela final com advertência obrigatória ("Beba com moderação"; indique a frase exata exigida pelos anexos A e P do CONAR).
- Jack Daniel's é destilado: na TV aberta, só das 21h às 6h (Lei 9.294/96). Considere isso na proposta.
- Claims só os oficiais, com o texto exato.

# FORMATO DO PROMPT DE VÍDEO (Seedance 2.5, em inglês, um bloco contínuo com seções rotuladas)
```
GLOBAL STYLE: genre, look, film or digital, 60:30:10 palette, 16:9, 24fps and 180 degree shutter, speed ramps, what must NOT appear.
SCENE: one line: what happens, where, mood.
CHARACTERS: face, hair, build, wardrobe; or "identity and wardrobe exactly as in @tag".
PRODUCT: (@tag) identical to the reference in every shot, size in cm, label soft and unreadable.
LOCATION: the space and its props, separate from the people.
FIRST FRAME AND BLOCKING: exact starting positions, who faces where, at what distance.
FORMAT MODE: N shots, N-1 hard cuts, 15.0 seconds total.
Shot 1 (0.0s to X.Xs): [shot type, lens in degrees, camera move]. [action with exact timings]. Hard cut.
Shot 2 (...)
OPTICS: lens per shot type.
CAMERA: support and movement per shot.
PHYSICS: liquids, foam, ice, condensation, fire, fabric, hair; the single rule of the surreal effect, if any.
LIGHTING: motivated source, direction, how it falls on faces and on the product.
AUDIO: diegetic sounds with exact timings. No music, no dialogue, no subtitles.
POSITIVE LOCKS: what never changes (identity, product, positions, number of people).
```

# STYLE PREFIX DE PARTIDA (em inglês; adapte para cada marca)
```
Style: 8K IMAX commercial. Photorealistic, 16:9 frame with anamorphic character (oval bokeh, subtle horizontal flares). No 3D render, no game engine, no CGI sheen.
Lighting: Motivated light only. [scene light]. The [brand accent color] is the only saturated color in frame.
Color: 60:30:10. 60 [dominant], 30 [secondary], 10 [brand accent], never more.
Camera: Physical cine lens. 180 degree shutter motion blur. Confident, fast commercial pacing.
Skin: Pore-level realism. Vellus hair, asymmetric moles, capillary flush.
Hands: Anatomically correct hands in every cut. Five fingers, natural knuckle creases. No extra fingers, no morphing.
Acting: Hollywood restraint. Micro-pauses before reactions, precise eye-line, living eyes with catch-lights. Nobody poses for camera.
Physics: Gravity and inertia respected. Real weight, correct contact shadows. Liquids, foam, ice and condensation behave physically.
Product: [product] geometry and colors identical to the reference in every cut. Label soft and unreadable. No invented text.
Composition: Rule of thirds. Every person moving from frame one.
Continuity: Characters, wardrobe, props and environment identical across every cut. No identity drift.
Technical: 24fps. No on-screen text, no subtitles, no watermarks, no real-world logos.
Audio: Environmental SFX only. No music. No dialogue.
```

# O QUE ENTREGAR
ETAPA 1 (agora), para cada marca:
1. Três conceitos bem diferentes entre si: nome, a ideia em 2 frases, por que conversa com a marca e com o posicionamento, e o risco técnico para a IA (baixo, médio, alto).
2. O conceito que você recomenda e por quê.
Pare aqui e espere eu escolher.

ETAPA 2 (depois que eu escolher), para cada conceito escolhido:
3. Roteiro em tabela, segundo a segundo, fechando em exatamente 15,0 s: tempo | plano (tipo, lente em mm e em graus, movimento) | ação | som.
4. Lista de assets com @tag e um prompt de imagem em inglês para cada: folha de produto a partir da foto real, folha de personagem, locação em 3/4, objetos de cena, mapa se precisar.
5. Prompt do frame de partida em inglês: no ângulo exato do Shot 1, um instante antes da ação.
6. Prompt de vídeo Seedance 2.5 completo, em inglês, no formato acima, com o Style Prefix adaptado à marca.
7. Três opções de cartela final em português, só com claims oficiais e a advertência.
8. Riscos: o que a IA tende a errar neste roteiro (líquido, espuma, mãos, rótulo, gelo, fogo) e como o prompt previne; qual plano testar primeiro em 480p.

# ESCRITA
- Explicações em português do Brasil, diretas, sem travessões (use dois-pontos, vírgula ou ponto).
- Prompts de imagem e de vídeo em inglês, cada um num bloco de código, pronto para copiar.
- Se faltar algo essencial, faça no máximo 3 perguntas antes de começar; se não, siga e declare suas suposições.

# DIREÇÕES QUE JÁ EXPLORAMOS (proponha conceitos diferentes destas)
- Heineken Ultimate, "Leve. Sem dúvida.": ao abrir a garrafa a gravidade fica mais fraca em volta dela (tampinha, gotas e cabelo flutuam); no primeiro gole a gravidade volta com um "tum", e a garrafa pousa sólida no balcão.
- Heineken Ultimate, "Double take": ela lê o rótulo novo, a câmera faz um chicote de ida e volta até a garrafa, os amigos congelam desconfiados, um gole, sem dúvida.
- Jack Daniel's, "Gota a gota": uma gota atravessa o processo (nascente, barril em chamas, carvão, anos no barril) até o gelo trincar no copo, ligada por match cuts.
- Jack Daniel's, "Ofício": o ofício de um luthier em paralelo com o da destilaria (o verniz vira o âmbar), terminando num copo com amigos.
````
