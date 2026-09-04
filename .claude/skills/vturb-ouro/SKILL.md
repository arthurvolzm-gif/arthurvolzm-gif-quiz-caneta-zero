---
name: vturb-ouro
description: >-
  Playbook de marketing de resposta direta destilado de 165 entrevistas (440h) da
  VTurb com operadores de 7, 8 e 9 dígitos: métricas de VSL e de funil, estrutura
  de VSL, copy, ads e criativos, tráfego, ofertas, upsells, recuperação, escala e
  operação. Use SEMPRE que for escrever ou revisar copy, VSL, anúncios, upsells,
  downsell, order bump; montar ou diagnosticar funil de vendas; definir mecanismo,
  oferta, preço ou esteira de ascensão; ler métricas/benchmarks; ou planejar como
  escalar tráfego e operação. Referência de mesa do usuário (funil Destrave Metabólico
  e outros).
---

# VTurb Ouro — Playbook de Resposta Direta

Engenharia reversa de 165 entrevistas (440h, 201 operadores e copywriters) do canal VTurb
(Segredos da Escala / Scaling Secrets). Critério de "padrão": 3+ operadores independentes
dizendo o mesmo. Compilado em agosto de 2026.

**Como usar esta skill:** os padrões abaixo são a referência rápida. Quando precisar de
detalhe, benchmark exato, tática específica ("arsenal") ou de uma divergência entre
operadores, consulte `references/ouro-vturb-completo.txt` (texto integral, ~17,5 mil linhas;
use Grep pelo tema ou pelo número do padrão). Ao ajudar o usuário, **sempre** relacione a
recomendação ao princípio correspondente e ao número/benchmark quando existir.

> Nota de leitura: o texto integral tem `�` no lugar de letras acentuadas (falha de fonte na
> extração do PDF). O conteúdo continua legível. Este SKILL.md reescreve o essencial limpo.

---

## Os 13 números que se sabe de cor

| Métrica | Régua | Leitura |
|---|---|---|
| Conversão de VSL em tráfego frio | 1% a 2% | 2% abriu muito bem; acima de 3% é raro; 1% já escala se o tráfego for barato |
| Retenção no primeiro minuto | 60% a 70% | Abaixo de 50% a lead está morta, por melhor que seja o resto |
| Retenção até o pitch | 20% a 30% | Régua central; encolhe conforme a VSL cresce |
| Play rate | 60% a 70% (piso) | Headline sobre o player e thumbnail são as alavancas |
| Posição do pitch | ~2/3 do vídeo | Nunca compare posição entre durações diferentes |
| Leads testadas por VSL | 3 a 8+ | Lead não se escreve, se testa em lote |
| ROAS de operação escalada | 1,8 a 2,0 | Cai conforme a escala sobe, e isso é o esperado |
| Participação do upsell no faturamento | 30% a 35% | O pós-pitch é longo; close é a 2ª maior alavanca depois da lead |
| Order bump | 30% a 40% | Taxa boa; a "regra do 1/3 do ticket" não existe na prática |
| Recuperação de vendas | +15% a +40% | Lucro puro sobre tráfego já pago, o dinheiro mais barato |
| Margem líquida saudável | ~30% no Brasil | Nutra na gringa roda 10-20% e ganha no volume |
| Reembolso + chargeback | 3-5% BR / 15-20% EUA | É a métrica que quebra operação americana de brasileiro despreparado |
| Taxa de acerto de oferta/VSL | 10% a 30% | O jogo não é acertar mais, é validar barato e ter a próxima na fila |

---

## As 12 leis (atravessam todos os capítulos)

1. **O front compra cliente; o lucro mora no backend.** A 1ª venda existe para pagar o tráfego. Upsell, order bump, esteira, recuperação e campanha interna são onde se ganha dinheiro.
2. **Quem paga mais caro pelo cliente ganha o leilão.** Subir o ticket médio compra permissão para gastar mais em tráfego, e é isso que permite escalar. Ticket alto vence ticket baixo com a mesma copy.
3. **A lead é o 80/20 da VSL, e a microlead é o 80/20 da lead.** A maior queda de retenção é no começo. Trocar as primeiras 100-500 palavras já dobrou conversão. Testa-se microlead antes de lead nova, e lead nova antes do corpo.
4. **Trocar formato dá saltos maiores que melhorar copy (2x a 3x).** Call center, podcast, entrevista, booklet, superprodução com rosto, vertical vs horizontal. Vale igual para criativo: formato > ângulo > copy.
5. **Congruência ponta a ponta ou o funil vaza.** Criativo, lead, VSL, página e produto contando a mesma história, na mesma linguagem, com o mesmo rosto.
6. **O criativo é o público.** Pós-iOS 14/Andrômeda, segmentação virou detalhe: quem qualifica o tráfego é o anúncio. Orçamento vai para esteira de criativos; leitura por criativo, não por conjunto.
7. **Valide por venda, nunca por métrica secundária.** Retenção alta ≠ conversão alta (há lead de 13% batendo a de 21%). CTR, CPC, nota do pixel servem para diagnosticar, não para aprovar. Decide: venda, ROI, lucro.
8. **Modele o validado; não invente do zero.** Mecanismo, estrutura, formato e oferta se modelam do que já escala no nicho. A inovação fica no gancho e no ângulo. Espionagem é processo formal.
9. **A taxa de acerto é baixa; o jogo é portfólio e cadência.** 10-30% das ofertas e das VSLs dão certo. Valide mais barato, mate rápido o mediano, tenha a próxima na fila.
10. **Volume de teste com proporção fixa entre validado e novo.** Oxigena-se o vencedor mudando uma variável por vez até secar; a fila de conceitos novos nunca para.
11. **O anúncio não pode parecer anúncio.** O criativo vende o clique, não o produto; a VSL disfarça a mensagem de vendas em conteúdo. Vencem: orgânico viral reaproveitado, criativo feio/cru de celular, advertorial, quiz, call center.
12. **Pesquisa é o trabalho; escrever é o final.** Copy de alto nível é mineração (comentários de YouTube, Reddit, grupos, avaliações da Amazon, biblioteca de anúncios) até ter a língua literal do público. Monta-se de trás para frente: oferta e mecanismo primeiro, lead por último.

---

## Índice de padrões por capítulo

Cada linha é um princípio acionável. Para o desenvolvimento, busque o número do padrão no
`references/ouro-vturb-completo.txt`.

### I. Métricas de VSL
1. Conversão em tráfego frio vive entre 1% e 2%, e é assim que se escala.
2. Retenção até o pitch: régua central 20-30%, encolhe conforme a VSL cresce.
3. Primeiro minuto: 60-70% de retenção é o piso de uma lead saudável.
4. A lead é o 80/20 da VSL; a microlead é o 80/20 da lead.
5. Lead não se escreve, se testa em lote: 3 a 8+ variações por VSL.
6. Retenção não é conversão: a métrica que decide é venda/ROI.
7. O player é alavanca de dois dígitos: headline, autoplay, fundo do vídeo e velocidade.
8. Trocar FORMATO gera saltos maiores que melhorar copy: 2x a 3x.
9. Rosto humano na tela dobra a conversão (expert real bate cinematografia).
10. Vertical/mobile ganha quase sempre: +51% a +100%.
11. Pitch aos ~2/3 do vídeo; pós-pitch longo; close é a 2ª maior alavanca depois da lead.
12. Duração é função de ticket e consciência: modele comprimento por quem escala no nicho.
13. Encurtar antes de validar perde; cortar gordura depois de validar ganha.
14. Delay de botão sincronizado ao pitch + recuperação por desconto dentro do player.
15. Retenção por criativo (origem de tráfego) é a régua de corte e escala.
16. Taxa de acerto de VSL: ~30% no topo, 10-20% na média; o jogo é cadência.
17. Play rate: 60-70% é o piso; headline, thumbnail e aviso prévio de vídeo são as alavancas.
18. Métricas se leem em ordem e no momento certo: pré-escala, nunca no teste de criativo.
19. Miniganchos/fascinations nos pontos de queda do gráfico de retenção.
20. Pre-sell/quiz antes da VSL: perde tráfego de propósito, ganha retenção e conversão.

### II. Métricas de Funil
1. O lucro mora no backend: o front existe pra comprar cliente.
2. Quem paga mais caro pelo cliente ganha o leilão: suba o ticket médio.
3. Upsell se mede por contribuição no ticket médio, NUNCA por taxa de conversão.
4. Upsell responde por ~30-35% do faturamento (e fatia bem maior do lucro).
5. Recuperação de vendas é lucro puro sobre tráfego já pago (+15% a +40%).
6. O ROAS de escala converge para 1,8-2,0 e cai conforme a escala sobe.
7. Jogo do lucro > jogo do ROI: escala é aceitar ROI achatado com lucro absoluto maior.
8. Esteira de ascensão multi-degrau: front → upsell → programa → high ticket.
9. Webinário/live perpétua para a BASE de compradores é máquina de lucro recorrente.
10. Meteórico/raspagem de base: ROAS ~10 com teto baixo.
11. Order bump: 30-40% é a taxa boa; a "regra do 1/3 do ticket" não existe.
12. Pix mata o upsell one-click; ticket que puxa cartão destrava o funil.
13. Tickets validados por formato de funil.
14. Taxa de acerto de ofertas 10-30%: valide barato, mate rápido, conte com o portfólio.
15. Reembolso + chargeback quebra operação nos EUA (15-20% vs 3-5% no Brasil).
16. Margem líquida: ~30% é o teto saudável no Brasil; nutra gringa roda 10-20%.
17. CPA não se otimiza olhando CPA: planilha de KPIs, métricas antecedentes, caminho reverso.
18. O gerenciador mente: 25-60% das conversões se perdem sem trackeamento.
19. Lançamento puro em decadência; o perpétuo vira a base que paga o lançamento.
20. Recorrência anual > mensal: o mensal quebra o caixa e o cliente.

### III. Estrutura de VSL
1. Macroestrutura canônica: LEAD → HISTÓRIA → MECANISMO → OFERTA.
2. A lead é o bloco mais valioso (e onde mora a maior perda).
3. Múltiplas leads por VSL desde o dia 1 (3 a 5+, cada uma isolando um ângulo).
4. Ordem de escrita ≠ ordem do vídeo: mecanismo/oferta primeiro, lead por último.
5. Microlead: o anúncio validado colado no início da VSL.
6. Congruência ponta a ponta (criativo → lead → página → produto).
7. A venda escondida: disfarçar a mensagem de vendas em conteúdo.
8. Formato é rei: mudar o formato dá o maior salto de conversão.
9. Superprodução com rosto virou o padrão brasileiro ("Brazilian Wave").
10. Mecanismo: modelar o validado, nunca partir do zero.
11. Tese central / one belief: uma única crença, empilhada em logic points com prova.
12. Prova empilhada por tipo; prova demonstrativa é o elemento mais forte da VSL.
13. Quiz: o funil da vez, sempre com mini VSLs dentro e 20+ etapas.
14. Bloco de oferta templatizado: a parte mais racional (e mais negligenciada) da copy.
15. Product buildup: a transição obrigatória entre mecanismo e oferta.
16. Pós-pitch é venda também: FAQ, segunda rodada de CTA e recuperação no player.
17. No pitch, a página abre embaixo do player (o primeiro botão é o que converte).
18. História: função é credibilidade + conexão, enredos intercambiáveis (o bloco que ninguém testa).
19. Multiplicar personagens multiplica prova (o interlocutor tira o expert do papel de vendedor).
20. Esteira industrial de VSL: ciclos curtos, revisão diária, copy autor como revisor final da edição.
21. Validação em degraus: uma variável não-validada por vez, funil mínimo primeiro.
22. O player como estrutura: autoplay, headline, thumb de recuperação e botões são parte da VSL.
23. Front enxuto que fabrica a próxima venda (nunca criar "produto canibal").

### IV. Copy
1. Pesquisa é o trabalho; escrever é só o final.
2. Minas de pesquisa: comentários de YouTube, Reddit, grupos fechados, Ads Library, livros da Amazon escritos pelo próprio avatar.
3. Falar a língua literal do público; autoridade = descrever o problema melhor que a própria pessoa.
4. One Belief: a frase única que, aceita, torna a compra óbvia.
5. Pontos lógicos: cadeia de "sims" que parte do que a pessoa já acredita.
6. O mecanismo é o coração e nasce de crença que o público JÁ tem.
7. Nome chiclete, gimmick e pergunta paradoxal.
8. Prova é o alfa e o ômega: calibrada pelo tamanho da claim, com demonstração no topo.
9. Copy é montada, não escrita: estrutura invisível, swipe e Frankenstein.
10. Escreve-se de trás pra frente: oferta e mecanismo primeiro, lead por último.
11. Lead = promessa + prova + curiosidade; os começos são o gargalo de tudo.
12. Otimização: troca-se lead, gancho e formato; o mecanismo validado não se toca.
13. Congruência anúncio → lead → VSL.
14. A venda disfarçada: anúncio não pode parecer anúncio.
15. Benefícios em 3 camadas e emoção dominante por nicho.
16. Simplicidade radical: dona Maria, criança de 6ª série, teto da sofisticação.
17. Revisão é onde a copy é escrita.
18. Formação por imersão: ler, transcrever e escrever copy em volume todos os dias.
19. IA é executora com julgamento humano: bloco a bloco, nunca a VSL inteira.
20. Sofisticação importa mais que consciência; identificar, não escolher.

### V. Ads e Criativos
1. O anúncio não pode parecer anúncio: vende o clique, não o produto.
2. Formato é a maior alavanca do criativo (formato > ângulo > copy).
3. O orgânico viral é a fonte nº 1 de criativo pago.
4. Anatomia hook + body: criativo é combinação, não peça única.
5. Os primeiros 3-15 segundos: alavanca mais barata de renovação e função de derrubar CPC.
6. Empilhamento de ganchos (gancho + gancho + corpo, sem precisar de coesão).
7. Avatar: a microvariação mais poderosa (e a congruência que ninguém pode errar).
8. Volume industrial com proporção fixa entre validado e novo.
9. Lateralização/oxigenação: um vencedor vira dezenas de variações, uma variável por vez.
10. Criativo feio, cru e lo-fi vence a superprodução.
11. Hook visual e "clickbait contextualizado": atenção que qualifica.
12. Espionagem como processo formal (e o perfil fake que simula o lead).
13. Métricas granulares: hook rate, hold rate, e o que fazer com cada uma.
14. Criativo é ativo documentado: nomenclatura, banco de estruturas, swipe organizado.
15. O copy é diretor: briefing de gravação e edição fazem parte da copy.
16. Continuidade criativo → VSL: o anúncio é "a lead da lead".
17. Teste a mensagem barato antes de produzir caro.
18. A volta das imagens estáticas (com teto de escala).
19. Rejeição e aprovação são rotina operacional, não acidente.
20. IA na esteira: avatar próprio licenciado, locução em blocos e mistura com real.

### VI. Tráfego
1. Pós-Andrômeda/iOS 14: o criativo é o público; segmentação morreu.
2. Validação é por venda/ROI; métrica secundária não valida nada.
3. Custo por initiate checkout é a métrica intermediária rainha.
4. Orçamento de teste medido em tickets/CPAs (1 ticket por criativo é o número mágico).
5. A conta de anúncio é a variável mais imprevisível: teste em 2+ contas sempre.
6. Não existe estrutura universal: teste de estrutura por conta e por oferta.
7. Escala vertical fracionada com leitura da janela pós-aumento; choque de orçamento mata.
8. Reduzir antes de matar: campanha/criativo em queda leva corte de verba, não pausa.
9. Escala horizontal/lateralização é o caminho dos grandes (campanhas, contas, páginas, países).
10. Day trade de horário: orçamento baixo na largada, subir antes do pico, meia-noite como largada.
11. Calendário: fim de semana é ouro; criativo se testa no pior dia, oferta no melhor.
12. Nunca uma fonte só: diversificação é seguro de vida.
13. Cada fonte pede criativo, copy e funil próprios (dopamina vs educação vs congelado).
14. Google/YouTube funcionam por inteligência acumulada: não duplique, aqueça, espere.
15. Fundo de funil no Google (branded search) é camada obrigatória e porta de entrada.
16. Contingência: qualidade do ativo (BM/conta com gasto white recente) define o tráfego.
17. Tracking: o gerenciador mente, a UTM/tracker decide; pixel vale pouco no DR.
18. Jogo de spy dos dois lados: esconder os próprios criativos e ler sinais nos alheios.
19. Internacionalização da oferta validada: traduzir e multiplicar países é a escala mais barata.
20. Remarketing é camada de lucro com teto (e regras próprias).
21. Esteira industrial de criativos e "nunca pare de testar".
22. Diagnóstico de trás pra frente; o tráfego termina no clique.

### VII. Hacks e Ofertas
1. Front é aquisição, backend é monetização: o lucro mora depois da 1ª venda.
2. "Respeite a conversão": achou oferta que converte, sugue o máximo no menor tempo.
3. Oferta que escala nasce boa; mate rápido as medianas e tenha a próxima na fila.
4. Ofertas e mecanismos são cíclicos: reviva, reembale, traduza.
5. Upsell tem fórmula: mesma promessa acelerada, "mais do mesmo", ou "feito pra você"; métrica é ticket médio, não conversão.
6. Recuperação é centro de lucro: multiplique pontos de contato e funis por evento.
7. Meteórico/campanha interna: monetize a base com CAC ~zero.
8. Valide antes de produzir: teste seco, MVP e campanha antes do produto.
9. Big nicho de dor urgente > nicho inexplorado ("se ninguém vende ali, é por um motivo").
10. Sofisticar o entregável (app + personalização) sobe conversão e valor percebido; venda o formato que o nicho já compra.
11. Todo produto resolve um problema e cria o próximo: esteira desenhada desde o front.
12. O próximo produto sai da boca da base: pesquisa como fábrica de oferta.
13. Escassez e ancoragem que funcionam são as VERDADEIRAS.
14. Reversão de risco agressiva, com trava de implementação.
15. Expert real vence ator; sociedade vence coprodução.
16. Espionagem é processo formal da empresa, não hobby.
17. Preço é a alavanca mais barata e menos testada.
18. Ordem 80/20 de montagem e diagnóstico de trás pra frente.
19. Gringa: entre como afiliado, vire produtor depois; Europa é o blue ocean da vez.
20. Networking fechado e eventos de bastidor são canal de inteligência (e de ofertas).

### VIII. Operação, Gestão e Mentalidade
1. "Mais > Melhor > Novo": o vício em iteração é o câncer do mercado.
2. A matemática da persistência: só perde quem desiste.
3. O gargalo é sempre o empreendedor (antídoto é founder mode, não ausência).
4. Contrate PSD e treine do zero; a pior contratação é a do meio.
5. Demissão previsível + densidade de talento.
6. Cultura é o que você tolera, é top-down, e só existe se virar ritual.
7. Meta é lucro/margem, nunca faturamento; transforme meta em variável controlável.
8. A cadência: daily / weekly / monthly, com pauta fixa e plano de ação.
9. Diagnóstico por gargalo: pergunte "por que meu negócio NÃO cresce".
10. Zona de genialidade, calculadora de delegação e a ordem certa de contratar.
11. Caixa compra o direito de errar; padrão de vida trava a escala.
12. Ambiente e círculo social definem o teto (projete o ambiente, não confie na disciplina).
13. Modo caverna calibrado: intensidade distorce o tempo, mas o limite é real.
14. Networking é o 80/20 do conhecimento, mas exige resultado e reciprocidade.
15. Mentoria individual e emprego batem curso; "obesidade mental" é o problema real.
16. Humildade operacional: entre um degrau abaixo, use a operação dos outros de escola.
17. Faixa branca não inova: modele primeiro, invente depois.
18. Timing e ciclos: formatos morrem, princípios ficam, e a janela fecha.
19. Separar funil de AQUISIÇÃO de funil de MONETIZAÇÃO: o lucro está no backend.
20. Processo só depois de validado; estrutura enxuta até o motor existir.
21. Efeito Lindy, fonte primária e inglês: onde os melhores estudam.
22. Skill composta: o full stack é o moat pessoal.

---

## Guias rápidos de aplicação (quando o usuário pedir)

**Escrever/revisar uma VSL** → macroestrutura LEAD → HISTÓRIA → MECANISMO → OFERTA (III-1).
Escreva de trás pra frente (IV-10). A lead concentra o esforço (III-2); prepare 3-5 leads
isolando ângulos diferentes (III-3). Mecanismo modelado do que já escala no nicho (III-10),
nascido de crença que o público já tem (IV-6). Prova demonstrativa no topo (III-12). Bloco de
oferta templatizado com product buildup antes (III-14/15). Pós-pitch com FAQ + 2ª CTA (III-16).

**Escrever copy/lead** → pesquisa primeiro, linguagem literal do avatar (IV-1/2/3). One Belief
(IV-4) sustentada por pontos lógicos (IV-5). Lead = promessa + prova + curiosidade (IV-11).
Simplicidade radical (IV-16). Revisão é onde a copy é escrita (IV-17). Prova calibrada pela
claim (IV-8). Não invente o mecanismo do zero; modele (Lei 8).

**Criar anúncio/criativo** → não pode parecer anúncio (V-1). Formato > ângulo > copy (V-2).
Modele orgânico viral (V-3). Foque os primeiros 3-15s (V-5). Empilhe ganchos (V-6). Teste
avatar como variação (V-7). Criativo cru/lo-fi costuma vencer superprodução (V-10). Congruência
com a VSL: o anúncio é "a lead da lead" (V-16).

**Montar/otimizar o funil** → lucro no backend (Lei 1); suba o ticket médio (Lei 2). Order bump
(30-40%), upsell (mede-se por ticket médio, ~30-35% do faturamento), recuperação (+15-40%).
Esteira: front → upsell → programa → high ticket (II-8). No Brasil, atenção ao Pix vs cartão no
one-click (II-12). Quiz + mini VSLs é o funil da vez (III-13).

**Upsell / downsell** → fórmula: mesma promessa acelerada, "mais do mesmo", ou "feito pra você"
(VII-5). Mede por contribuição no ticket médio, nunca por conversão (II-3). Downsell tipicamente
= mesma oferta em condição menor (ex.: plano mensal no lugar do vitalício).

**Oferta / preço / mecanismo** → oferta que escala nasce boa; mate as medianas rápido (VII-3).
Escassez e ancoragem só as VERDADEIRAS (VII-13). Reversão de risco agressiva (VII-14). Preço é a
alavanca mais barata e menos testada (VII-17). Sofisticar entregável (app, personalização) sobe
valor percebido, mas venda o formato que o nicho já compra (VII-10).

**Ler métricas / diagnosticar** → valide por venda/ROI, não por métrica secundária (Lei 7).
Cheque contra a tabela dos 13 números. Custo por initiate checkout é a métrica intermediária
rainha (VI-3). Diagnóstico de trás pra frente, por gargalo (VIII-9). O gerenciador mente; confie
na UTM/tracker (VI-17 / II-18).

**Escalar** → paga mais caro pelo cliente quem tem backend (Lei 1/2). Escala vertical fracionada
sem choque de orçamento (VI-7); reduzir verba antes de pausar (VI-8); escala horizontal e
internacionalização da oferta validada (VI-9/19). Aceite ROI achatado com lucro absoluto maior
(II-7). Nunca uma fonte só de tráfego (VI-12).

---

## Regras ao usar este playbook com o usuário

- Combine com as preferências de escrita do usuário (sem hífen/travessão, texto exato, compliance Meta) e com o contexto do funil ativo (ex.: Destrave Metabólico).
- Nunca fabrique número ou estudo. Escassez e ancoragem sempre reais (VII-13).
- Modele o validado; a inovação fica no gancho/ângulo. Ao sugerir, cite o padrão que embasa.
- Quando faltar detalhe, busque no `references/ouro-vturb-completo.txt` antes de responder.
