---
name: deploy-vercel-netlify
description: Como o site do quiz é hospedado/publicado (Vercel + GitHub) e onde ficam os assets
metadata: 
  node_type: memory
  type: reference
  originSessionId: 826f865a-cff5-449f-a58d-cba521f5d8ad
  modified: 2026-08-07T23:24:34.631Z
---

**Site publicado no Vercel**, ligado ao GitHub. Repo: `https://github.com/arthurvolzm-gif/quiz-destrave-metabolico` (branch `main`).

Pasta local que sobe pro Vercel: `C:\Users\marlo\Documents\quiz-destrave-vercel\` (contém `index.html` + assets: `bg-vegetal.jpg` fundo, `logo-destrave.png` logo, `FotoKelly.jpg`, e imagens que ele salvar como `resultado-1.jpg`, `canetas-emagrecedoras.jpg`, etc.).

**Publicar (o usuário roda no terminal do VS Code):**
```
cd C:\Users\marlo\Documents\quiz-destrave-vercel
git add -A && git commit -m "..." && git push
```
Vercel republica sozinho a cada push.

Também existe `Site_Kelly\netlify-deploy\` (usado com Netlify antes; domínio `inspiring-zabaione-469a9b.netlify.app`). Mantemos os dois sincronizados por [[workflow-3-arquivos]], mas o principal em produção é o Vercel.

**Eu não consigo salvar arquivos de imagem** que o usuário manda no chat — quando ele quer uma imagem no site, eu deixo o `<img>` apontando pro nome do arquivo e ele salva a imagem com esse nome nas pastas. Para recortar margem transparente de imagem (ex.: fiz com a logo), uso PowerShell + System.Drawing (não há ImageMagick/Python/Node funcionando nesta máquina; Chrome existe para gerar PDF via headless).
