---
name: teste-trafego-caneta-zero
description: "Primeiro teste de tráfego pago do Caneta Zero: estrutura 1-1-3, orçamento, criativos, régua de leitura e pré-requisitos"
metadata:
  node_type: memory
  type: project
---

Plano fechado com o usuário em 30/08/2026 para o primeiro teste pago do
[[funil-caneta-zero]] no Meta. Antes disso o funil nunca tinha recebido tráfego.

**Estrutura decidida:** 1 campanha, 1 conjunto, 3 anúncios (1-1-3), ABO, público de segmento
aberto, R$25 por dia, destino `metodo-caneta-zero.vercel.app`.

O usuário chegou querendo 1-1-5. A régua do playbook (VI-4) é ~1 ticket de gasto por criativo
antes de decidir: com ticket de R$29,90, 5 criativos pedem ~R$150 no total, ou seja R$50 a
R$60 por dia. Com R$25 cada criativo pegaria meia dúzia de reais por dia e o Meta sufocaria
os perdedores antes de dar amostra. Daí o corte para 3.

**Os 3 criativos da onda 1** (um ângulo, um público e um formato cada):
- `CZ_A_dinheiro_comparativo_v1` — custo R$12.000 x R$0 por mês — quem usa há meses
- `CZ_B_platô_tipografico_v1` — "a caneta não parou de funcionar, seu corpo parou de responder" — quem travou na balança
- `CZ_C_rebote_whatsapp_v3` — conversa da amiga que parou e recuperou 7kg — quem já parou

O C tem 3 versões. **Sobe a v3** (com "Meu Deus amigaaa", "isso é pq vc parou de uma vez",
fecha em "te mando o link do site que me explicou isso" e leva a etiqueta única de CTA).
A v2, idêntica mas sem etiqueta, fica guardada como variação da onda seguinte.

**Régua de leitura:** o usuário decidiu escolher o vencedor por CTR maior e CPC menor, e
depois gerar 2 variações dele. Com esse orçamento não há amostra de venda mesmo, então está
coerente. O desempate acordado é **custo por Initiate Checkout** (VI-3): se dois empatam no
CTR, ganha o que gera checkout mais barato, porque trouxe clique de gente certa.

**Ao variar o vencedor: uma variável por vez.** Se o B ganhar, as variações são outras frases
no mesmo formato tipográfico, não um formato novo.

**Pré-requisitos que ficaram avisados antes de gastar:**
- **Domínio próprio.** `.vercel.app` é domínio de plataforma: não fecha verificação de domínio
  no Meta, não configura Aggregated Event Measurement e tem histórico de link flagado. Ver
  [[rastreamento-caneta-zero]].
- **Order bumps ligados na Ticto.** Ticket de R$29,90 puro limita o CPA máximo a ~R$25, o que
  é inviável em frio (Lei 2 do playbook). Bump a 30-40% leva o ticket médio para ~R$37.
- **Purchase e API de Conversões conferidos.**
- **1 conta só é risco de falso negativo** (VI-5): resultado ruim aqui não prova criativo ruim.

**Plano de ondas:** onda 1 descobre o ângulo; onda 2 testa formato contra o vencedor (recorte
real da reportagem do SURMOUNT-4, print de busca do Google, vídeo lo-fi da Kelly); onda 3
lateraliza o vencedor em avatares e entram os ângulos novos. Nunca subir a fila inteira de uma
vez: cabem 3 anúncios por onda com esse orçamento.

**Aviso registrado:** o ângulo "quem vai começar" pega um público que ainda não tem o problema
que o produto resolve. Pode ganhar no CTR e vender mal, e isso é falta de página para ele, não
defeito do criativo.

Criativos e regras de arte em [[criativos-caneta-zero]].
