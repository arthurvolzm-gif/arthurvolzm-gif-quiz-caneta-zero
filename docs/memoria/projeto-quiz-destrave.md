---
name: projeto-quiz-destrave
description: Projeto ativo — quiz/funil do Método Destrave Metabólico (arquivo principal e estrutura)
metadata: 
  node_type: memory
  type: project
  originSessionId: 826f865a-cff5-449f-a58d-cba521f5d8ad
  modified: 2026-08-14T01:34:02.636Z
---

Projeto ativo desde ~jul/2026: **funil de quiz do "Método Destrave Metabólico"** (produto de emagrecimento da Nutri Kelly, para mulheres que usam a caneta Mounjaro/Ozempic/Wegovy e travaram).

**Arquivo principal de trabalho (o que edito por padrão neste projeto):**
`c:\Users\marlo\Documents\Site_Kelly\quiz-destrave-metabolico-sem-vsl-sem-landing.html`
(É um quiz single-page: `FLOW` de etapas renderizado por JS. Substitui os arquivos antigos `quiz-destrave-metabolico*.html`.)

**Fluxo atual do quiz (16 perguntas):** intro → perguntas (nome, idade, medicação, gasto, perdeu, dor, sono, impacto, tentou → quebra "Você não está sozinha" → medo, peso, altura, tempo → página de prova social "meta" → beneficios[multi], futuro, garantia) → comprometimento (prepitch) → "analisando" (com contador de liberação 0-100%, ease-out, ~4s) → diagnóstico (gráfico "índice de gasto calórico" + caixa vermelha + solução) → oferta (offerLocked → offerPrice).

Detalhes importantes de UI já implementados: logo (`logo-destrave.png`, recortada) no cabeçalho; seta de voltar (`backBtn()`, `go(-1)`); multi-select (`type:'multi'`); imagem por pergunta (`img:` field); página de diagnóstico com gráfico SVG. Ver [[oferta-destrave]] e [[copy-vsl-funil]].

**Variante de teste (13/08/2026):** `quiz-destrave-metabolico-v2-vturb.html`, criada a partir do arquivo `-COPIA` e otimizada com o [[vturb-ouro-playbook]] (mecanismo das 5 travas dentro do quiz, diagnóstico personalizado com IMC e travas detectadas, pós-pitch completo na oferta, UTM repassada ao checkout, exit intent, CTA fixa, localStorage). Ainda NÃO está em produção, não entra no [[workflow-3-arquivos]] enquanto for variante.

**Variante público-sem-caneta (ago/2026):** arquivo `quiz-destrave-metabolico-sem-vsl-sem-landing-COPIA.html`, pivô do quiz para mulheres que NÃO usam caneta (sem grana pra remédio). É o arquivo que edito por padrão nessa frente. Ver [[variante-copia-sem-caneta]].

Sempre seguir [[workflow-3-arquivos]] e [[preferencias-edicao-copy]].
