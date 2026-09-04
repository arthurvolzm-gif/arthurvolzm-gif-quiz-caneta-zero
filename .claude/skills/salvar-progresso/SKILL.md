---
name: salvar-progresso
description: Atualiza a memória do projeto com o que mudou na conversa, para a próxima sessão já abrir com contexto. Use quando o usuário pedir para salvar o progresso/contexto, ao encerrar uma sessão de trabalho, ou depois de mudanças relevantes em preço, oferta, arquivos, deploy ou configuração.
---

# Salvar progresso do projeto

Objetivo: manter a memória em `C:\Users\marlo\.claude\projects\c--Users-marlo-Documents-Site-Kelly\memory\` fiel ao estado real do projeto, para que a próxima conversa não comece do zero nem com informação vencida.

## Como fazer

**1. Levante o que mudou nesta sessão.** Considere apenas fatos duráveis:

- preço, ancoragem, entregáveis, bônus, order bumps
- links de checkout, pixel, domínio, deploy
- arquivos criados, renomeados ou que deixaram de ser a fonte oficial
- decisões do usuário que valem para o futuro (nomes de produto, o que saiu do funil)
- armadilhas técnicas resolvidas, com a causa — vale mais que a solução

Ignore o que é só desta conversa: rascunhos, tentativas, prompts de imagem, textos que o usuário ainda está decidindo.

**2. Leia a memória existente antes de escrever.** Comece por `MEMORY.md` e abra os arquivos relacionados. A maioria das atualizações é **corrigir um arquivo existente**, não criar outro. Duplicar memória é pior que não salvar: a próxima sessão passa a ler duas versões do mesmo fato.

**3. Corrija o que venceu.** Este é o passo mais importante e o mais esquecido. Se um preço mudou, um arquivo foi renomeado ou uma pendência foi resolvida, edite a linha antiga. Memória desatualizada faz a próxima sessão trabalhar com dados errados e com confiança.

Para pendências resolvidas, o formato que funciona é riscar e datar:
`- ~~pendência antiga~~ resolvido em DD/MM/AAAA`

**4. Só crie arquivo novo** quando o assunto não couber em nenhum existente. Formato:

```markdown
---
name: <slug-em-kebab-case>
description: <uma linha, usada para decidir relevância na recall>
metadata:
  type: user | feedback | project | reference
---

<o fato, direto. Datas sempre absolutas: "23/08/2026", nunca "semana passada".
Ligue aos relacionados com [[nome-do-arquivo]].>
```

**5. Registre o pointer** em `MEMORY.md`: `- [Título](arquivo.md) — gancho curto`.

## Critério de qualidade

Escreva pensando em quem abrir a próxima sessão sem ter visto esta. A pergunta é sempre: *isso me faria errar se eu não soubesse?* Caminho de arquivo publicado, identidade de commit que destrava o deploy, motivo de um bug que já custou uma hora — tudo isso passa. "Conversamos sobre a headline" não passa.

## Ao terminar

Diga em uma linha o que foi salvo e o que foi corrigido. Não reproduza o conteúdo dos arquivos.
