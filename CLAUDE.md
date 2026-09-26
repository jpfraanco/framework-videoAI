# framework-videoAI

Base de conhecimento de vídeo com IA do JP. O documento principal é `FRAMEWORK.md`.

## Ao receber material novo

- Salvar o bruto em `fontes/` (URL e data de captura no topo; texto limpo, sem links de imagem).
- Integrar o aprendizado no `FRAMEWORK.md`, na seção que já trata do assunto. Não criar seção nova se uma existente cobre. Citar a origem entre parênteses.
- Se o material contradiz algo do framework, manter os dois com a data e marcar em "16. Em aberto".
- Prompt testado que funcionou vira arquivo em `exemplos/`.
- Atualizar a data no topo do `FRAMEWORK.md` e a tabela da seção 17.

## Regras de escrita

- Texto em português do Brasil, didático, siglas abertas na primeira vez, exemplos concretos.
- Sem travessão (em dash) nem meia-risca em texto nosso: usar dois-pontos, vírgula ou ·. Material em `fontes/` e `skills/` fica verbatim.
- Prompts de imagem e vídeo sempre em inglês.

## Ao escrever prompts para o JP

- Ler primeiro as seções 1 (leis), 5 ou 6 (anatomia) e 13 (diagnóstico) do `FRAMEWORK.md`.
- Higgsfield CLI: conferir parâmetros com `higgsfield model get <modelo>` antes de montar o comando; não gerar nada que gaste crédito sem o JP pedir.
