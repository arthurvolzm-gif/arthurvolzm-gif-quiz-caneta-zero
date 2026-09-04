---
name: quiz-caneta-zero-estrutura
description: "Como o quiz Caneta Zero foi desenhado — ordem das perguntas, gimmick do diagnóstico e por quê"
metadata: 
  node_type: memory
  type: project
  originSessionId: ff61e82c-b1c3-42d9-8c63-d186d919bdbd
  modified: 2026-09-02T19:47:34.796Z
---

Decisões de arquitetura do `quiz-caneta-zero.html`, construído em agosto de 2026 modelando
5 funis de concorrentes (MetaFit/Dr Márcio, Renascer Magra, Protocolo Caneta, Me Seca, QH3X) e
reaproveitando a engine de `quiz-destrave-metabolico-sem-vsl-sem-landing.html`.

**Gimmick central:** "Índice de GLP-1 Natural" (0 a 100), calculado de verdade a partir de
tempo de uso, falta de fome, o que entra no prato, colaterais, flacidez, dose e objetivo.
Equivale à "Idade Metabólica" dos concorrentes, mas congruente com o mecanismo da oferta.

**Ordem das perguntas e o porquê:**
- 1 dose · 2 canetinha · 3 objetivo — a 1 espelha a grade do criativo, para o toque do anúncio
  continuar na primeira tela. Nome só na 4, depois de 3 micro-compromissos.
- **Atualizado em 02/09/2026:** a faixa de idade saiu da lista de perguntas e virou parte da
  própria intro (`IDADE_OPTS` + `selectIdade()`), então a tela de abertura já é a primeira
  pergunta. Sobraram 22 perguntas no array e a BREAK 1 passou a disparar depois do `nome`.
- 12 quanto consegue comer · 13 o que entra no prato — existem só para armar a BREAK 2, que
  devolve essas respostas literalmente ("você acabou de responder que come X").
- 20 tempo disponível · 21 tem nutricionista? — a 21 abre a lacuna que o produto preenche.
- 22 compromisso, com benefício personalizado pela dor da pergunta 9 (função `beneficioPorDor`).
- 23 ponte para o diagnóstico, com as duas opções sendo "sim".

**Fluxo:** intro → Q1-5 → BREAK 1 → Q6-13 → BREAK 2 (mecanismo) → Q14-19 → META (prova social)
→ Q20-23 → Analisando → Diagnóstico → Landing final.

**O que foi descartado das referências:** avatares 3D de corpo, "onde sente dores", captura de
WhatsApp/email, antes e depois, planos mensal/trimestral, VSL, idade metabólica.

**O público deste arquivo é só quem usa ou já usou a canetinha.** Todas as opções para quem vai
começar foram removidas de propósito, porque o diagnóstico não faz sentido para quem nunca
aplicou. ~~Se for atender esse público, é funil paralelo com outro diagnóstico~~ — o funil
paralelo foi criado em 02/09/2026: `quiz-caneta-zero-sem-caneta.html`, ver
[[quiz-caneta-zero-sem-caneta]]. Continua valendo a regra de não misturar os dois públicos
dentro de um quiz só.

Contexto da oferta em [[funil-caneta-zero]].
