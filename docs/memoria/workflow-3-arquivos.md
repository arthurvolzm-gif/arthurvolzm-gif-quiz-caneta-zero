---
name: workflow-3-arquivos
description: Toda edição do quiz precisa ser sincronizada em 3 arquivos e depois publicada no Vercel
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 826f865a-cff5-449f-a58d-cba521f5d8ad
  modified: 2026-08-07T23:23:02.215Z
---

Ao editar o quiz do Destrave, SEMPRE sincronizar a mudança em **3 arquivos** (são cópias, não estão linkados):
1. `c:\Users\marlo\Documents\Site_Kelly\quiz-destrave-metabolico-sem-vsl-sem-landing.html` (arquivo de trabalho — onde edito)
2. `c:\Users\marlo\Documents\Site_Kelly\netlify-deploy\index.html`
3. `c:\Users\marlo\Documents\quiz-destrave-vercel\index.html` (é a pasta que sobe pro Vercel via GitHub)

**Como aplicar:** edito o arquivo de trabalho e depois copio para os outros dois com `cp`, e confirmo com `diff -q` que os 3 ficaram idênticos. Ex.:
`cp quiz-...-sem-landing.html netlify-deploy/index.html && cp quiz-...-sem-landing.html /c/Users/marlo/Documents/quiz-destrave-vercel/index.html`

**Why:** o site em produção é o do Vercel, que lê de `quiz-destrave-vercel`. Se eu editar só o arquivo de trabalho, a mudança não vai pro ar.

Ao terminar, SEMPRE dar ao usuário os comandos de publicação (ele roda no terminal do VS Code):
```
cd C:\Users\marlo\Documents\quiz-destrave-vercel
git add -A && git commit -m "..." && git push
```
O Vercel republica sozinho a cada push. Se adicionar imagem nova, copiar o arquivo da imagem também para `netlify-deploy` e `quiz-destrave-vercel`. Ver [[deploy-vercel-netlify]].
