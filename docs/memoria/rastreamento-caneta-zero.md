---
name: rastreamento-caneta-zero
description: "Pixel, verificação de domínio, eventos da Ticto e otimização de imagens do site Caneta Zero"
metadata: 
  node_type: memory
  type: project
  originSessionId: 9d7aa670-f739-42e1-894e-3ea2c63b4260
  modified: 2026-08-29T20:09:26.650Z
---

**Pixel da Meta:** `1021851947333727`, instalado no `<head>` da landing e do quiz. Eventos da própria página: `PageView`, `ExitOffer` (pop-up abre) e `ExitOfferClick` (clique no botão do pop-up).

**Na Ticto** devem ficar ligados: PageView, InitiateCheckout, AddPaymentInfo, **Purchase** e a **API de Conversões**. AddToCart desligado, porque dispara junto com o InitiateCheckout e duplica. O `InitiateCheckout` é responsabilidade da Ticto, não da landing — por isso o botão do pop-up manda evento customizado.

**Verificação de domínio no Meta:** código `65cbytnwqvx1m7apmthd12m9ilvjfy`, disponível pelos dois métodos — meta-tag no `<head>` e o arquivo `65cbytnwqvx1m7apmthd12m9ilvjfy.html` na raiz. Só conclui com domínio próprio; `.vercel.app` é domínio da plataforma.

**Deploy bloqueado na Vercel:** aconteceu em 26/08 porque os commits estavam assinados como `LeoVolz <leo.bertolli227@gmail.com>` e o plano Hobby não aceita colaborador externo em repositório privado. **O repositório está configurado para commitar como `arthurvolzm-gif <226346454+arthurvolzm-gif@users.noreply.github.com>`** — manter essa identidade, senão o deploy trava de novo.

**Imagens:** otimizadas em 29/08 de 17,6 MB para 0,7 MB. Sem ferramenta de compressão nesta máquina — o caminho que funciona é PowerShell com `System.Drawing`, redimensionando para o dobro do tamanho exibido e salvando JPEG qualidade 82. Todas as imagens do site são 24bpp, sem transparência. A landing usa `loading="lazy"` e `background-attachment: scroll` no mobile.

Ver [[projeto-caneta-zero]].
