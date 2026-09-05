# Quiz Caneta Zero — contexto do projeto

Repositório dedicado ao **funil-quiz do Método Caneta Zero** (Nutri Kelly Firbida).
Foi separado do repositório antigo `Site_Kelly`, que misturava outros funis e tinha
100+ MB de histórico. Aqui fica só o que este funil precisa.

## O arquivo que importa

- **`quiz-caneta-zero.html`** — o quiz inteiro em arquivo único: HTML, CSS e JS.
  Não há build, não há dependências. Abrir no navegador já roda.
- Imagens usadas pelo quiz, todas na raiz: `FotoKelly.jpg`, `FotoSiteKelly.jpeg`,
  `Garantia7dias.png`, `pesquisa-mounjaro.jpeg`, `resultado-1.jpg`, `bg-vegetal.jpg`.

A landing do mesmo produto **não** está aqui: ela vive em
`arthurvolzm-gif/caneta-zero-site` (Vercel) e é a fonte oficial da página de vendas.

## Como o quiz está montado

Ordem das telas (o `FLOW` é montado a partir do array `QUESTIONS`):

1. **Abertura** — headline, a pergunta da idade já com as opções (2 por linha, cada uma
   com foto colada ao botão, cantos arredondados) e o texto "Faça o teste e receba um
   protocolo específico para seu corpo…". Não há botão de CTA: clicar na foto ou no botão
   de uma faixa de idade inicia o quiz e dispara `QuizIniciado`.
2. **Perguntas 1 a 11** — nome, objetivo, canetinha, dose, tempo de uso, dor principal,
   quilos eliminados, massa muscular, exercícios, fome, sintomas.
3. **Diagnóstico (versão curta)** — direto após `colaterais`, sem tela de análise antes.
   Não mostra o alerta, o Índice de GLP-1 nem o "3 pontos identificados": só os pontos
   1 e 2 (sem numerar o 2) e termina com um gancho de curiosidade pra continuar o teste.
4. **Perguntas 12 a 20** — projeção de futuro, concordâncias, peso, altura, meta,
   prova social, acompanhamento, compromisso, liberação.
5. **"O hormônio da caneta não vem só da caneta"** — a tela do mecanismo (break2).
6. **"Analisando suas respostas…"** (5 s, barra com curva *smootherstep*) + **Diagnóstico
   (versão completa)** — só aqui aparece o alerta, o Índice de GLP-1, o "3 pontos
   identificados", o ponto 3 e a frase original da solução ("potencializar o hormônio
   que produz o GLP-1").
7. **Landing final** (`renderResult`) — oferta, bônus, garantia, FAQ e checkout.

### Regras que o código já respeita

- **Numeração**: cada pergunta tem `num`, e a barra de progresso é `num/TOTAL_Q`.
  Ao inserir, remover ou reordenar perguntas, renumere — e lembre que as telas de
  conteúdo (diagnóstico, prova social, mecanismo) usam `pctAte('<id da pergunta>')`.
- **Gatilhos de tela** ficam no `FLOW.push`: o primeiro diagnóstico entra depois de
  `colaterais` (dentro do `QUESTIONS.forEach`), a prova social depois de `meta_kg`. Fora
  do forEach, na sequência final: `break2` (mecanismo) → `analyzing` → `diagnostico` (2ª
  vez) → `result`. `renderDiagnostico(full)` é a mesma função nas duas ocorrências: o
  `FLOW.push({type:'diagnostico'})` do meio chama sem `full` (versão curta), e o do fim
  usa `{type:'diagnostico', full:true}` (versão completa). Ao editar o texto do
  diagnóstico, veja se a mudança deve valer só numa versão (então entra dentro do
  `full ? ... : ...`) ou nas duas.
- **O Índice de GLP-1** (`calcIndiceGLP`) lê os *textos* das alternativas. Se você mudar
  o texto de uma opção, ajuste o `includes()` correspondente ou a pontuação some
  silenciosamente. Hoje ele usa: tempo de uso, fome, massa, colaterais, objetivo e dose.
- **Personalização**: várias telas montam frase a partir de `state.answers`. Ao remover
  uma pergunta, procure por `a.<id>` antes.

## Medição do funil (instalada, falta ligar)

- `GA_ID` no topo do arquivo está **vazio de propósito**. Cole o ID `G-XXXXXXXXXX` da
  propriedade GA4 e o rastreamento liga sozinho; vazio, nada carrega.
- Três eventos vão ao mesmo tempo para GA4 e Meta Pixel:
  - `quiz_etapa` — cada tela, com `etapa`, `etapa_id`, `tipo`, `posicao`.
  - `quiz_resposta` — cada resposta, com `pergunta` e `resposta` (no nome grava só
    "preenchido", nunca o texto digitado).
  - `quiz_abandono` — no `pagehide`, com a última etapa vista.
- No GA4, registre `etapa`, `etapa_id`, `pergunta` e `resposta` como **dimensões
  personalizadas**, senão os relatórios não deixam quebrar por resposta.
- Analytics só coleta em URL publicada. Abrindo como `file://` não registra nada.

## Oferta e rastreamento

- Pixel Meta: `1021851947333727`; verificação de domínio no `<head>`.
- Checkout principal (R$29,90): `https://payment.ticto.app/O49D90BBF`.
- Checkout do pop-up de saída (R$19,90): `https://payment.ticto.app/O1376B6BC`.
- Pop-up de saída: só arma na tela final (`result`), depois de um gesto real do usuário,
  uma exibição por sessão (`sessionStorage.cz_saida`), e reabre para quem volta do
  checkout da Ticto.

## Preferências de trabalho do usuário

- **Manter o texto exato** que ele pedir. Se houver erro de português ou algo que
  atrapalhe a conversão, avisar — não corrigir por conta própria.
- **Sem travessão** na copy.
- **Compliance Meta**: nada de promessa de resultado garantido, "antes e depois"
  agressivo ou claim médico.
- **Prova**: o número de 82% tem fonte (reportagem sobre reganho pós-Mounjaro).
  Depoimento fabricado não entra — a tela de histórias foi removida por isso.
- **"Crie uma imagem"** significa escrever o prompt de geração, não montar HTML.
- Capas de e-book não levam assinatura "Método Caneta Zero · Nutri Kelly" dentro da arte.

## Ambiente

- Windows 11, PowerShell (e Bash via Git Bash). **Não há Python, ImageMagick nem gh CLI.**
- Para comprimir imagem: PowerShell com `System.Drawing`. Para gerar PDF: Chrome headless.
- Commits no repositório da landing (`caneta-zero-site`) precisam ser assinados como
  `arthurvolzm-gif <226346454+arthurvolzm-gif@users.noreply.github.com>`, senão a Vercel
  bloqueia o deploy no plano Hobby. Neste repositório do quiz isso não se aplica.

## Skills disponíveis

Ficam em `.claude/skills/` e são carregadas automaticamente pelo Claude Code:

- **`vturb-ouro`** — playbook de resposta direta destilado de 165 entrevistas da VTurb
  (métricas de VSL, estrutura de copy, anúncios, ofertas, upsells, escala). Usar sempre
  que for escrever ou revisar copy, montar funil, definir mecanismo/preço ou ler métricas.
  O material completo está em `references/ouro-vturb-completo.txt`.
- **`salvar-progresso`** — atualiza a memória do projeto ao fim de uma sessão em que algo
  durável mudou (preço, oferta, bônus, link, pixel, deploy, arquivo, decisão de nome, ou
  armadilha técnica resolvida). Invocar sem esperar o usuário pedir.

## Histórico e memória

`docs/memoria/` guarda as notas de contexto acumuladas nas sessões anteriores — oferta,
preços, criativos, regras de prova, decisões do quiz, deploy. `docs/memoria/MEMORY.md` é
o índice. Leia antes de propor mudanças de preço, oferta ou copy: várias decisões já
foram tomadas e testadas ali.

## Pendências conhecidas

- Colar o `GA_ID` e publicar para começar a medir o funil.
- O quiz ainda não está publicado (a landing está; o quiz não).
- A ancoragem do pop-up de saída diz "De R$ 107,90" enquanto a oferta principal do quiz
  é R$29,90 — decisão pendente do usuário.
