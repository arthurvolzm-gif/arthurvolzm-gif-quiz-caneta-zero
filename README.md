# Quiz Caneta Zero

Funil-quiz do Método Caneta Zero (Nutri Kelly Firbida): diagnóstico do Índice de GLP-1
Natural para quem usa canetinha (Mounjaro, Ozempic, Wegovy, Saxenda), terminando na
oferta do protocolo de 14 dias.

## Rodar

Abra `quiz-caneta-zero.html` no navegador. Não há build nem dependências — é um arquivo
único com HTML, CSS e JS.

Para testar o rastreamento e o pop-up de saída, publique em qualquer host estático
(Vercel, Netlify): abrindo como `file://` o analytics não registra nada.

## Estrutura

```
quiz-caneta-zero.html     o quiz inteiro
*.jpg / *.jpeg / *.png    imagens usadas pelo quiz
CLAUDE.md                 contexto do projeto para o Claude Code
.claude/skills/           skills do projeto (vturb-ouro, salvar-progresso)
docs/memoria/             notas das sessões anteriores (oferta, preços, decisões)
```

## Antes de publicar

- Colar o ID do GA4 na variável `GA_ID`, no topo do arquivo.
- Conferir os links de checkout da Ticto.
