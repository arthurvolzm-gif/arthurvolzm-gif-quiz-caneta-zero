---
name: oferta-destrave
description: "Detalhes da oferta, mecanismo, persona e configs do produto Destrave Metabólico"
metadata: 
  node_type: memory
  type: project
  originSessionId: 826f865a-cff5-449f-a58d-cba521f5d8ad
  modified: 2026-08-07T23:24:12.878Z
---

**Produto:** Método Destrave Metabólico (Nutri Kelly, nutricionista). Ebook/protocolo de 14 dias + app + comunidade.

**Mecanismo central:** as **5 travas metabólicas** que travam a queima de gordura (analogia recorrente: "freio de mão puxado" e "5 cadeados"). As 5 travas = **sono, proteína, carboidrato, hidratação, gasto calórico**.

**Persona:** mulheres ~35-55 que usam ou usaram a caneta (Mounjaro/Ozempic/Wegovy), emagreceram e travaram. Dores: balança travada, medo de engordar de novo, gasto alto com a caneta, flacidez, fome desregulada, autoestima baixa, evita fotos/espelho. Desejo: emagrecer sem passar fome, sem aumentar a dose e se libertar da caneta.

**Preço/oferta:** R$29,90 à vista (ou 5x de R$6,63), ancoragem "De R$ 93,52". Garantia de 7 dias.

**Entregáveis:** protocolo 14 dias; módulos das 5 travas; 20 Receitas Light (bônus); **Aplicativo Destrave** (monitora sono, meta de hidratação, macros/calorias, frases de motivação diárias); comunidade. Ebooks estão em `Site_Kelly\Entregaveis\` (ex.: `Ebook-Destrave-Metabolico.html`, `Ebook-Exercicios-Anti-Flacidez.html`, `Ebook-Guia-Anti-Efeitos-Colaterais.html`).

**Configs técnicas no quiz:**
- Checkout Ticto: `https://checkout.ticto.app/O12A4116D` (constante `CHECKOUT_URL`). Preço tem que estar igual na Ticto também.
- Meta Pixel ID: `1012929151722018`. Eventos: PageView, QuizIniciado, Lead, OfertaRevelada, ViewContent, InitiateCheckout (helper `px()`). Purchase é configurado na Ticto.
- Verificação de domínio Meta (metatag): content `1ghqwe79k59bfxj5rarqsz5i6aoug4`.

**Upsells/downsell planejados:** Upsell 1 = Comunidade VIP WhatsApp; Upsell 2 = contato direto com a expert (Nutri Kelly); Downsell = plano mensal da comunidade. Ver [[copy-vsl-funil]].
