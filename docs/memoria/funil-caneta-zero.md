---
name: funil-caneta-zero
description: "Funil ativo Método Caneta Zero — oferta, mecanismo, arquivos e estado do projeto"
metadata: 
  node_type: memory
  type: project
  originSessionId: ff61e82c-b1c3-42d9-8c63-d186d919bdbd
  modified: 2026-09-02T19:47:40.070Z
---

Funil principal em construção desde agosto de 2026. Substituiu o "Método da Caneta Saudável"
(mesma persona, mecanismo novo). Expert: Nutri Kelly Firbida, 41 anos, Paraná, 18 anos de
nutrição.

**Oferta:** ebook em PDF, **R$29,90 à vista ou 5x R$6,62**, ancoragem De R$97,90.
4 módulos + 3 bônus. Checkout Ticto.

**Mecanismo (One Belief):** o GLP-1 que a canetinha injeta é o mesmo hormônio que as células L
do intestino já fabricam. A caneta não ensina o corpo a produzir, ela substitui a produção;
meses comendo pouquíssimo deixam essa fábrica sem estímulo, e é por isso que a balança trava e
o peso volta. O "Gatilho GLP-1 Natural" tem 3 partes: proteína suficiente, fibra fermentável e
a ordem de comer.

**Módulos:** 1 Ativação do Gatilho GLP-1 Natural · 2 Blindagem da Massa Magra ·
3 Redução Sem Efeito Rebote · 4 Plano de 14 Dias.

**Arquivos (raiz do projeto):**
- `caneta-zero-site/index.html` (fora de Site_Kelly) — é a que está no ar em metodo-caneta-zero.vercel.app
- `quiz-caneta-zero.html` — quiz de quem usa caneta, engine copiada do quiz Destrave
- `quiz-caneta-zero-sem-caneta.html` — mesma oferta, público que NÃO usa caneta, criado em
  02/09/2026, ver [[quiz-caneta-zero-sem-caneta]]
- `advertorial-caneta-zero.html` — artigo assinado pela Kelly, destino do criativo de notícia
- `Ebooks-Caneta-Zero/` e `Entregaveis - Caneta Zero/` — entregáveis

**Fluxo:** criativo → quiz OU landing → checkout. O criativo de notícia vai para o advertorial,
que leva à landing. Ver [[criativos-caneta-zero]].

**Pendências conhecidas:**
- ~~CHECKOUT_URL do quiz apontando para o Destrave~~ corrigido em 27/08/2026
- advertorial diz "dois terços" onde landing e quiz dizem 82% (padronizar)
- ~~notificações de venda inventadas no quiz~~ removidas em 29/08/2026
- **o quiz continua sem publicar**; a landing já está no ar
- **o advertorial também não está publicado**: o repositório `caneta-zero-site` só tem `index.html`,
  então o criativo de manchete não tem destino (verificado em 30/08/2026)
- **domínio próprio ainda não comprado**, e é pré-requisito do tráfego pago

Plano do primeiro teste pago em [[teste-trafego-caneta-zero]].
Regras de prova e claims em [[regras-prova-caneta-zero]]. Preferências de escrita em
[[preferencias-edicao-copy]].
