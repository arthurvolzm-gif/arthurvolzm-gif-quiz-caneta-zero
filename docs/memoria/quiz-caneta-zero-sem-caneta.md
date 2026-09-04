---
name: quiz-caneta-zero-sem-caneta
description: "Variante do quiz Caneta Zero para quem NÃO usa canetinha — arquivo, ângulo do criativo, o que muda e o que ficou pendente"
metadata: 
  node_type: memory
  type: project
  originSessionId: 450c5fe7-c00c-4c07-9639-a4c0b88ac56d
  modified: 2026-09-02T19:47:20.932Z
---

Funil paralelo criado em 02/09/2026, duplicando `quiz-caneta-zero.html` para um público novo:
**quem não usa canetinha e quer emagrecer**. Arquivo: `quiz-caneta-zero-sem-caneta.html`
(raiz do projeto, ainda não publicado). O quiz original continua servindo só quem usa ou já
usou a caneta — são dois quizzes, não um com bifurcação.

**Ângulo do criativo que alimenta este quiz:** não é só a canetinha que produz GLP-1, o corpo
dela já produz esse hormônio, só que sem estar potencializado. A pessoa chega querendo
descobrir o nível de GLP-1 que ela própria produz, e a intro já promete que existe um método
para potencializar isso.

**Mesmo produto, mesma oferta, mesmo checkout** (R$29,90, Ticto, `O49D90BBF`) e mesmo pop-up
de saída (R$19,90). O nome "Método Caneta Zero" foi mantido de propósito: para este público
ele lê como "emagrecer com zero caneta", o que é ainda mais direto.

**O que mudou em relação ao quiz da caneta:**
- 21 perguntas (o original tem 22). Saíram dose, canetinha, tempo de uso, quilos já
  eliminados, gasto mensal, colaterais e as duas de concordância sobre a aplicação.
- Entraram: `caneta` (usa/já pensou/nunca — a P1 espelha o criativo), `tempo_luta`,
  `tentativas`, `sanfona`, `sinais` (sinais de saciedade baixa), `concorda_remedio`.
- `dor` mudou de dores do tratamento para dores de quem tenta emagrecer sozinha (fome o dia
  inteiro, balança travada, o peso sempre volta, barriga, ataque de doce). **As opções da
  `dor` são chave de `beneficioPorDor()`** — mexeu nelas, sincroniza a função.
- BREAK 2 continua devolvendo literalmente as respostas de `fome` e `prato`, mas agora o
  ponto é "você estava cortando comida em vez de religar a produção de saciedade".
- Diagnóstico: o ponto 2 reaproveita os 82% do SURMOUNT-4 com enquadramento novo — serve para
  provar que o atalho da caneta não resolve, e o texto se personaliza pela resposta da P1.
- FAQ, "quanto custa o atalho", decisão e antes/depois reescritos.

**Índice de GLP-1 Natural recalibrado.** Os pesos do quiz da caneta jogavam quase todo perfil
no piso (clamp 11). Testado no Chrome headless com 4 perfis: pesado extremo 11, pesado típico
16, médio 39, leve 58 (o teto do clamp continua 58, para o diagnóstico nunca sair tranquilo).

**Pendências de entregável (o quiz promete, o produto ainda não entrega assim):**
- Módulo 3 é anunciado como **"Blindagem Antissanfona"**, mas o ebook existente é
  `Modulo-3-Reducao-Sem-Efeito-Rebote.html`, que fala em reduzir dose. Precisa de uma versão
  reescrita para quem não usa caneta.
- O 3º bônus virou **Método Blackout** (sono e fome noturna, já existe em
  `Bonus-1-Metodo-Blackout-Sono.html`) no lugar do Guia Anti Efeitos Colaterais, que não faz
  sentido para este público.

Ver [[quiz-caneta-zero-estrutura]], [[funil-caneta-zero]], [[oferta-caneta-zero]],
[[regras-prova-caneta-zero]].
