---
name: variante-copia-sem-caneta
description: Variante COPIA do quiz Destrave, pivô para público que NÃO usa caneta (sem grana pra remédio)
metadata:
  type: project
---

Desde ~ago/2026 estou construindo uma **segunda variante do quiz Destrave** num arquivo duplicado, para um **público diferente**.

**Arquivo da variante (edito por padrão):**
`c:\Users\marlo\Documents\Site_Kelly\quiz-destrave-metabolico-sem-vsl-sem-landing-COPIA.html`
Foi duplicado de `quiz-destrave-metabolico-sem-vsl-sem-landing.html` (o original continua mirando o público antigo, da caneta).

**Público novo da COPIA:** mulheres que **NÃO usam nenhum medicamento/caneta** (Ozempic/Mounjaro), muitas vezes **por falta de dinheiro**, e mesmo assim querem emagrecer. Dores centrais mudam: em vez de "gasto alto com a caneta / travou", o foco é dor de espelho e frustração (pneuzinhos, barriga, papada, rosto inchado, celulite, flacidez, braços/costas) e medo de nunca conseguir sem remédio caro.

**Regra de sincronização desta fase (importante):**
- **Copy do novo público** (perguntas, dores, depoimentos) fica **SÓ na COPIA**.
- **Mudanças de UI/estrutura** (ex.: botão da múltipla escolha aparecer sem rolar, cronômetro na intro, tela "Analisando") o usuário pede pra **replicar também no original** ("altere no quiz original também"). Só replicar no original quando ele pedir explicitamente.
- (Isto substitui, nesta fase, o [[workflow-3-arquivos]]; o Netlify/`netlify-deploy/index.html` NÃO está sendo sincronizado, só toco nele se ele pedir.)

**Estado atual da COPIA:**
- Quiz agora tem **15 perguntas** (removida a pergunta `medo`, "o que mais te preocupa"; as seguintes foram renumeradas 10-15 pra barra de progresso não estourar).
- Perguntas 3-6 refeitas sem foco na caneta: P3 tentativa, P4 barreira ("Você usa a caneta ou remédios...? Se não usa, por qual motivo?", 1ª opção = preço), P5 perdeu, **P6 `dor` = dores de espelho** (pneuzinhos/papada/celulite/braços).
- **Atenção técnica:** as opções da P6 (`dor`) são **chave** do mapa `PROFILES` (depoimento personalizado do diagnóstico) e do texto/fallback da oferta. Se mudar as opções da P6, tem que sincronizar as chaves do PROFILES e os fallbacks (linhas ~986 e ~1071), senão a personalização quebra.
- Intro: CTA com cronômetro "⏱ Disponível por: 09:47" (classe `.reserva`, estilo inline compacto/claro), sem a antiga linha da data.
- Tela "Analisando suas respostas..." com 4 itens + rótulo "Liberando seu diagnóstico personalizado...".

**Pendente (próximos passos):** o RESTO da COPIA ainda é "pró-caneta" e precisa de um pivô completo pra fechar a coerência: título da intro ("sem gastar com a caneta"), âncora de preço ("menos que 3 dias de caneta"), FAQ, carta da Nutri Kelly e a lista da oferta final (~linha 1248). Recomendei ao usuário fazer uma **pesquisa curta desse novo público** antes do pivô completo (o material atual em [[oferta-destrave]] é do público da caneta). Decisão dele.

Ver [[projeto-quiz-destrave]], [[oferta-destrave]], [[preferencias-edicao-copy]].
