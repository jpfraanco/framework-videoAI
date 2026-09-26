# Aprendizados · vídeo com IA (comercial BORA)

Método que saiu do teste da cena do metrô. Imagens no ChatGPT, vídeo no Dreamina (Seedance 2.0), 16:9.

## 1. A regra de ouro: o frame manda, o prompt só sugere

O Seedance copia com fidelidade **só o primeiro frame**. Tudo que não está nele, o modelo inventa: cartão, validador, direção da catraca, tamanho do sensor. O prompt ajuda, mas não segura detalhe.

Por isso, **gere muitos frames no ChatGPT** antes de gastar crédito de vídeo:

- **Um frame para cada detalhe crítico.** Se o que importa é o cartão encostando na seta do validador, o frame é esse plano fechado (exemplo: `f2a_cartao.png`). A pessoa entra depois pela referência dela.
- **O frame no ângulo exato do primeiro corte.** Se o corte 1 é um insert de 85mm, o frame é um insert de 85mm. Quando frame e corte batem, o vídeo começa pronto.
- **O frame um instante antes da ação.** Cartão a poucos centímetros do leitor, tela ainda azul. A mudança (seta e tela vermelhas) acontece no vídeo, não na imagem.
- **Detalhe que não pode errar vai para a imagem, não para o texto.** Quando um vídeo sai errado, primeiro pergunte: esse erro estava no frame? Se o elemento não aparecia, corrija criando um frame novo, não reescrevendo o prompt.
- **Refazer imagem é barato, refazer vídeo é caro.** Itere no ChatGPT até o frame estar certo e só depois vá para o Dreamina.

## 2. Referências reais antes de tudo

- **Fotografe ou recorte o objeto real.** O cartão (estética Riocard Mais), o validador amarelo do poste e as catracas do MetrôRio vieram de fotos reais, salvas em `refs/`. Descrição em texto sozinha gerou cartão de crédito e validador errado.
- **Diga o que copiar de cada imagem.** Por exemplo: "exact look of the third image", "black face, yellow side frame, blue screen, round reader with an arrow".
- **Tire logos e textos.** Peça "all text soft and unreadable". Mostrar marca real (MetrôRio, Riocard) falhando num comercial pode dar problema de marca.
- **Ignore o que não é o objeto.** Se a referência tem fundo verde ou texto, diga para ignorar.

## 3. Ordem de produção das imagens

1. **Folha de produto** (`01_produto/`): o device ou a catraca com o sensor, de vários ângulos. O packshot valida que o produto sai certo.
2. **Personagens** (`02_personagens/`): uma imagem limpa de cada, com rosto, cabelo e figurino.
3. **Locações em dupla** (`03_locacoes/`): versão A (o problema, sem BORA) e versão B (com BORA), com a mesma câmera e a mesma arquitetura. Se precisar, faça um **mapa de layout** para segurar posição de catracas, filas e câmera.
4. **Frames** (`04_frames/`): locação + personagem + produto + objetos de referência, no ângulo do primeiro corte.
5. **Vídeos** (`05_videos/`).

## 4. Geografia e física: o que a IA erra sozinha

- **Direção de movimento.** Defina sempre: todo mundo entra na estação, rumo às escadas rolantes. Nas vistas laterais, a entrada fica à esquerda do quadro. Sem isso, a primeira locação saiu invertida (lado de saída).
- **Luz coerente com o lugar.** Metrô subterrâneo tem só luz fluorescente fria. Sem essa instrução, saiu com sol.
- **Escala do produto.** O sensor da catraca tem cerca de 8 cm, embutido e rente ao tampo. Sem número, ele sai enorme.
- **Orientação do produto.** A cabeça do sensor fica nivelada, paralela ao chão. Sem isso, sai torta.
- **Física do tripé da catraca.** O braço fica parado enquanto travado. Depois de liberado, só gira quando a pessoa empurra com o corpo, um terço de volta por pessoa, nunca sozinho. Sem essa regra, a roleta "alucina".
- **A mão.** Palma aberta virada para baixo, paralela ao sensor, pairando a 5 cm, sem encostar. Cinco dedos, anatomia correta.
- **O scan.** A linha violeta atravessa a palma, e as veias aparecem só na parte já escaneada, abaixo da linha. Veias estilizadas, nunca biometria real (LGPD).
- **O produto certo no lugar certo.** No metrô não entra maquininha (POS), só o sensor embutido na catraca.

## 5. Seedance 2.0 no Dreamina

- **Limite de 4000 caracteres por prompt.** Use um prefixo de estilo curto (cerca de 700 caracteres) e âncoras enxutas. A imagem de referência carrega o resto.
- **As tags usam o nome do arquivo sem extensão:** `@f2a_cartao`, `@luana`, `@metro_B`. Não é `@Image1`.
- **Nomes únicos.** Dois arquivos chamados `f2a` viram tags ambíguas. Frame novo ganha nome novo (`f2a_cartao`), e o antigo não é sobrescrito.
- **Ordem de upload:** primeiro o frame inicial, depois personagem, objetos e locação. O prompt traz um bloco "References:" com o papel de cada tag.
- **Confira a tag depois do upload.** Se o Dreamina renomear o arquivo, troque a tag no prompt.

## 6. Duração e cortes

- **Cerca de 2 a 3 segundos por momento.**

| Momentos no clipe | Duração |
|---|---|
| 1 | 4 a 5s |
| 2 | 6s |
| 3 | 8s |

- **Poucos momentos por clipe.** Com duração curta demais, o modelo pula ações (a busca na bolsa, a catraca girando).
- **Termine o clipe onde o próximo começa.** O 2a acaba com ela fechando a bolsa e corta para o vídeo seguinte. Juntar problema e solução num clipe só complicou o resultado.

## 7. Economia de crédito

- **Comece pelo clipe mais difícil.** Se ele funcionar, o método está validado para o resto.
- **Um take por vez,** na menor duração que cabe a ação.
- **Antes de gerar, confira o frame, as tags e a contagem de caracteres.**
- **Quando falhar, diagnostique por segundo.** Por exemplo: "o segundo 1 errou o cartão, do segundo 2 em diante está ótimo". Corrija só o trecho que errou, de preferência no frame.

## 8. Onde fica cada coisa

- **`shotlist.html`:** o comercial inteiro. **`metro_teste.html`:** só a cena do metrô.
- **Cada card** traz as imagens a subir, as tags e o prompt com a contagem de caracteres.
- **Os geradores:** `_gera.py` (cenas e prompts), `_passos.py` (passos de imagem), `_render_passos.py` (vídeos e referências) e `_metro.py` (página do metrô). Para refazer, rode `python _metro.py` e `python _gera.py`.
