# Character sheet · garota street fashion (exercício Human Academy)

Resposta ao meta-prompt 3 do curso ([fontes/human-academy-curso.md](../fontes/human-academy-curso.md)). O figurino é o mesmo do keyframe do portão, para a personagem ser a mesma em todo o filme.

Teoria por trás: [FRAMEWORK.md, seção 4.3](../FRAMEWORK.md#43-folha-de-personagem-character-sheet).

## Decisões

- **Figurino herdado do keyframe do curso**: gorro cinza mescla, regata preta com nó torcido, bermuda cargo preta oversized, bota preta de cano alto molenga, tote azul-marinho risca de giz, correntes e anéis de prata.
- **Caimento como prioridade**: o pedido enfatiza o oversized natural, então o prompt descreve como cada peça cai (baixo no quadril, dobras no cano, tecido pesado).
- **Expressões tiradas do roteiro**: neutra (espelho), assustada (portão), ofegante (fuga e topo do prédio), determinada (escada).
- **Grade em 3 linhas**: vistas, expressões, detalhes. Ordem fixa ajuda o modelo a não misturar.
- **Um rosto por referência**: para o vídeo, recorte o painel de rosto e o de corpo inteiro em arquivos separados, ou gere a variante B.

## A. Prancha completa de pré-produção

Modelo sugerido: `gpt_image_2_5` (melhor com grade e muitos painéis) ou `seedream_v5_lite` (o do curso). Proporção 16:9, qualidade alta.

```
Professional film pre-production character reference sheet, hyper-realistic studio photography, landscape 16:9 layout on a plain seamless neutral light-grey background, clean three-row grid separated by thin vertical and horizontal divider lines. The same young woman in every panel: identical face, hair, proportions and wardrobe.

CHARACTER: a young East Asian woman in her early 20s, slim build, about 1.65 m tall, very long straight jet-black hair falling to mid-back with a few loose strands around the face, natural skin with visible pores and two tiny moles on the left cheek, straight dark brows, minimal makeup, cool and self-assured presence. Modern street-fashion look, cool and contemporary, every piece with a relaxed oversized natural drape:
- a slouchy heather-grey chunky-knit beanie worn loose and pushed back, extra fabric slumping at the back of the head;
- a black sleeveless fitted tank top with a twisted knot detail at the center of the chest;
- oversized black cotton-twill cargo bermuda shorts sitting low on the hips, wide legs ending just below the knee, deep side cargo pockets, soft heavy folds;
- black slouchy knee-high leather boots with a soft shaft that collapses into natural rings of folds around the calf, chunky rubber sole;
- a navy pinstripe canvas tote bag on the right shoulder, sagging with weight, a paperback book inside;
- chunky silver chain bracelets on both wrists, stacked silver rings, small silver hoop earrings.

TOP ROW, TURNAROUND: four full-body views head to toe, same scale, same relaxed neutral stance, arms hanging at her sides, 35mm lens, even soft studio light: front view; three-quarter view; side profile facing left; back view showing the back of the beanie, the full hair length, the bag strap, the rear of the shorts and the boots.

MIDDLE ROW, EXPRESSIONS FOR THE FILM: four head-and-shoulders close-ups, 85mm portrait lens, beanie and hair unchanged:
- neutral: calm, relaxed face, soft gaze straight into the lens;
- scared: eyes wide, glancing sideways off-frame, lips parted, shoulders slightly raised;
- breathless: mouth open mid-breath, flushed cheeks, a light sheen of sweat, strands of black hair stuck across her face;
- determined: jaw set, lips pressed, steady forward gaze, a slight frown.

BOTTOM ROW, WARDROBE DETAILS: six macro inserts in product-photo style: the chunky knit texture of the beanie; the twisted knot on the tank top; the cargo pocket and the heavy fold of the bermuda hem; the slouched boot shaft and the lug sole; the pinstripe tote with the paperback peeking out; her hand with silver chain bracelets and stacked rings.

LOOK: soft diffused key light with gentle fill, no harsh shadows, true-to-life skin tones, visible fabric textures (knit, cotton twill, leather, canvas, polished silver), fine detail, muted natural color grade, professional film costume and character bible. No text, no labels, no logos, no brand marks, no background scenery, no other people.
```

Na CLI:

```bash
higgsfield generate create gpt_image_2_5 --prompt "$(cat prancha_a.txt)" --aspect_ratio 16:9 --quality high --resolution 2k --wait
```

## B. Folha de travamento para o vídeo (modelo Higgsfield)

Um rosto grande de um lado, corpo inteiro de frente e costas do outro. É essa que sobe como `@girl` no Elements ou como referência no Seedance.

```
Cinematic character reference sheet, split-frame layout, photorealistic.
Left panel, facial close-up: the same young East Asian woman from the reference, the entire head fully inside the frame including the whole beanie and all the hair, nothing cropped, very long straight jet-black hair, real skin texture with subtle pores, calm neutral expression, looking straight into the lens. Shot on 85mm portrait lens, shallow depth of field, soft cinematic key light with gentle fill.
Right panel, full-body front and back views side by side: on the left a full-body front view facing the camera, on the right a full-body back view photographed from directly behind. In both she stands straight in a relaxed pose, arms at her sides, full height in frame head to toe, slim build about 1.65 m, same beanie, tank top, oversized cargo bermuda shorts, slouchy knee-high boots, navy pinstripe tote and silver jewelry. Both figures matched in framing, scale and lighting. Shot on 35mm lens, even full-length lighting.
Look: clean studio character sheet, plain solid grey background, consistent character across all views, soft diffused cinematic lighting, muted natural color grade, fine detail, true-to-life skin tones, vertical divider lines separating each view. No text, no logos.
```

Depois, uma edição para sobrar um rosto só:

```
Erase the face from the full-body front view on the right panel.
```

## C. Estados que o roteiro pede

Folhas derivadas, cada uma com nome próprio:

| Nome | Edição sobre a folha B |
|---|---|
| `@girl_run` | `same character sheet, after sprinting: flushed cheeks, light sweat on the face and neck, strands of hair stuck to the forehead, beanie pushed slightly askew.` |
| `@girl_dusk` | Não precisa de folha nova: a luz do pôr do sol vem do prompt da cena. Só crie folha quando o corpo ou a roupa mudam. |
