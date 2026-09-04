---
name: ebooks-caneta-zero
description: "Pasta Ebooks-Caneta-Zero: os 9 entregáveis, padrão de estrutura, CSS e como gerar os PDFs"
metadata: 
  node_type: memory
  type: project
  originSessionId: de23c304-e371-4ba9-b492-394ee8709916
  modified: 2026-08-29T20:07:38.020Z
---

Entregáveis do [[projeto-caneta-zero]], em `Site_Kelly\Ebooks-Caneta-Zero\`. HTML editável na raiz da pasta, PDFs em `Ebooks-Caneta-Zero\PDF\`.

## Os 9 arquivos

| Ebook | Estado em 29/08/2026 |
|---|---|
| `Modulo-1-Ativacao-do-Gatilho-GLP1-Natural` | expandido, 21 pgs |
| `Modulo-2-Blindagem-da-Massa-Magra` | expandido, 20 pgs |
| `Bonus-3-Guia-Anti-Efeitos-Colaterais` | expandido, 20 pgs — virou **Bônus 3** em 23/08 |
| `Modulo-3-Reducao-Sem-Efeito-Rebote` | expandido, 21 pgs — renumerado de 4 para 3 |
| `Modulo-4-Plano-de-14-Dias` | expandido, 22 pgs — renumerado de 5 para 4 |
| `Bonus-2-Cardapio-Semanal-e-Lista-de-Compras` | versão curta, 11 pgs |
| `Bonus-3-Metodo-Blackout` | **fora do funil** desde 23/08, arquivo mantido na pasta |
| `Bump-Papada-Zero` | criado em 26/08, 9 pgs, fundo `fundo-bump-papada.jpg` |
| `Boas-Vindas-Acesso` | página única pós-compra, fundo preto, CSS próprio |
| `Bump-Metodo-Barriga-Negativa` | versão curta, 14 pgs |
| `Bump-Protocolo-Anti-Celulite` | versão curta, 13 pgs |

**Os 4 últimos ainda não foram expandidos** no padrão dos módulos.

## Padrão de estrutura (usado nos 5 módulos)

Capa → sumário numerado com subtítulos → **carta de abertura da Kelly** (abre por um desconforto real, não pela técnica) → capítulos numerados → erros mais comuns → perguntas frequentes → checklist → encerramento que costura com o módulo seguinte.

## CSS e capas

`estilo.css` compartilhado pelos 9. Classes: `.page`, `.cover`, `.parte` (divisórias), `.sumario`, `.carta`, `.faq-item`, `.erro`, `.mito`/`.verdade`, `.ref-rapida`, `.fim`, `.check`, `.passo`, `.card`.

**Capas e divisórias usam fundo claro:** foto com overlay **branco 78%** (esbranquiçada, tipo marca d'água), título em **verde escuro**, selo e etiqueta em verde. Overlay preto foi testado e reprovado, porque as fotos são de mármore e madeira clara e o texto branco sumia.

Fundos reaproveitados de `Entregáveis - Método da Caneta\`, copiados para a pasta como `fundo-mod1..5.jpg`, `fundo-bonus2.jpg`, `fundo-bonus3.jpg`, ligados por classes `.f-mod1` … `.f-bonus3`. **Faltam** `fundo-bump-barriga.jpg` e `fundo-bump-celulite.jpg`.

## Gerar os PDFs

Chrome headless, que preserva cor de fundo e fontes do Google:

```bash
cd "c:/Users/marlo/Documents/Site_Kelly/Ebooks-Caneta-Zero"
CHROME="/c/Program Files/Google/Chrome/Application/chrome.exe"
OUT="C:/Users/marlo/Documents/Site_Kelly/Ebooks-Caneta-Zero/PDF"
for f in *.html; do n="${f%.html}"; "$CHROME" --headless=new --disable-gpu \
  --no-pdf-header-footer --virtual-time-budget=20000 \
  --print-to-pdf="$OUT/$n.pdf" \
  "file:///C:/Users/marlo/Documents/Site_Kelly/Ebooks-Caneta-Zero/$f" >/dev/null 2>&1; done
```

Use **barras normais** no caminho de saída: `\\` antes de `$` quebra a expansão da variável no bash. Contar páginas: `grep -a -o '/Count [0-9]*' arquivo.pdf | sort -rn | head -1`.

## Decisão do usuário registrada

Em 23/08/2026 ele mandou **remover todos os disclaimers** dos ebooks ("este material é educativo, não substitui acompanhamento médico"). Foram removidos dos 9. **Os alertas clínicos foram mantidos** (procurar médico em caso de vômito persistente, dor irradiando para as costas, sinais de desidratação), porque são segurança de quem usa medicamento injetável, não texto jurídico. Se ele pedir de novo para tirar, avisar uma vez e cumprir.
