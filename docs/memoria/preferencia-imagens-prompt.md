---
name: preferencia-imagens-prompt
description: Ao pedir "crie uma imagem", o usuário quer o PROMPT de geração, não a imagem montada em HTML/render
metadata:
  type: feedback
---

Quando o usuário pede "crie uma imagem" (capas de bônus, criativos, logo), ele quer que eu **escreva o prompt de geração de imagem** em PT-BR (com versão em inglês opcional) para usar num gerador externo. Ele **não** quer que eu monte o card em HTML/CSS e renderize em PNG via Chrome headless.

**Why:** ele já tem o gerador de imagens que usa e mantém o padrão visual por lá; o render em HTML não reproduz as fontes e o acabamento das capas existentes.

**How to apply:** responder direto com o prompt (padrão dos bônus: estrutura do card, paleta com hex, tipografia, bullets, regras de acentuação PT-BR), sem criar arquivos nem rodar Chrome. Ver [[oferta-destrave]] e [[preferencias-edicao-copy]].
