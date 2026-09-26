# framework-videoAI

Base de conhecimento do JP (unflat) sobre geração de imagem e vídeo com IA: Higgsfield, Seedance, Seedream, Dreamina, ChatGPT imagem e o método da Human Academy.

**Comece pelo [FRAMEWORK.md](FRAMEWORK.md).** É o documento principal, com as leis, o pipeline, a anatomia dos prompts, a CLI do Higgsfield e o diagnóstico de erros.

## Estrutura

| Pasta / arquivo | O que tem |
|---|---|
| [FRAMEWORK.md](FRAMEWORK.md) | O documento grande: tudo o que se sabe, organizado |
| [exemplos/](exemplos/) | Prompts completos prontos para usar (character sheet, locação ultra wide, roteiro em 20 frames, fashion film de 30 s) |
| [fontes/](fontes/) | Material bruto: posts e guias da Higgsfield, docs da CLI, prompts do curso, aprendizados do comercial BORA |
| [skills/](skills/) | A skill `seedance-shotlist-director` da Higgsfield (o `.skill` para subir no Claude e o `SKILL.md` aberto) |

## Como alimentar

1. Material novo (aula, post, teste, projeto) vai em `fontes/`, com a URL e a data no topo.
2. O que ele ensina entra no `FRAMEWORK.md`, na seção certa, com a origem entre parênteses.
3. Prompt que funcionou vira arquivo em `exemplos/`.
4. Atualize a data no topo do `FRAMEWORK.md` e a tabela de fontes (seção 17).

Com o Claude Code aberto nesta pasta, basta colar o material e pedir "integra no framework".
