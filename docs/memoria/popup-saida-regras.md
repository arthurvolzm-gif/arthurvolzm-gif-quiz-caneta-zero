---
name: popup-saida-regras
description: Regras técnicas do pop-up de saída (back redirect) que já custaram depuração — não repetir os erros
metadata: 
  node_type: memory
  type: reference
  originSessionId: 9d7aa670-f739-42e1-894e-3ea2c63b4260
  modified: 2026-08-29T20:07:26.611Z
---

O pop-up de saída existe na landing e no quiz do Caneta Zero, oferecendo 33% de desconto (De R$107,90 por R$19,90). Três regras aprendidas na marra:

**1. Só armar depois de um gesto real do usuário.** O Chrome tem a *history manipulation intervention*: entradas criadas por `pushState` sem interação são marcadas como puláveis e o botão Voltar as ignora, saindo da página. Vale `pointerdown`, `mousedown`, `click`, `touchstart`, `keydown` — **`scroll` não conta** como ativação.

**2. `pushState` sem passar URL.** Em página aberta via `file://` a origem é `null` e `history.pushState(state, '', location.href)` falha com SecurityError. Usar `history.pushState({...}, '')` dentro de try/catch.

**3. Uma camada só.** Depois de exibido, marcar em `sessionStorage` e deixar o Voltar funcionar normalmente. Re-empilhar vira armadilha e pesa na avaliação de experiência do Meta.

**Dois gatilhos:** o Voltar na própria página e o retorno do checkout — este último marca a ida ao clicar em link `payment.ticto.app` e reabre a oferta no evento `pageshow`, que é o único que dispara quando a página volta do bfcache.

**No quiz**, o pop-up só vale na tela final (`FLOW[state.idx].type === 'result'`), nunca durante as perguntas.

Ver [[projeto-caneta-zero]] e [[oferta-caneta-zero]].
