---
name: ui-craft
description: Fase 4 do processo de design. Cria interfaces em alta fidelidade com o design system da empresa, partindo do fluxo que existe hoje em produção e dos templates do DS, e apresenta sempre 2 a 4 variações baseadas em benchmark (concorrentes e análogos), cada uma com origem, prós e contras e uma recomendada. Trabalha do macro para o micro: escopo, caminho principal, casos de borda, feedback do sistema e refinamento. Use quando alguém disser "desenha", "monta a tela", "layout", "protótipo", "variações", "componente", "qual padrão usar", "onboarding", "checkout", "formulário", "estado vazio", "benchmark de UI".
---

# UI craft

> Design de interfaces é um processo, não só a produção de telas `[pós: M1]`. Não faça algo bonito só por ser bonito: a apresentação precisa ter um propósito `[pós: M13]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós, `[externo]` é fonte de fora da pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

> **Pendente para o ambiente da empresa:** esta skill será adaptada quando estiver conectada ao design system e às outras skills do trabalho. Veja "Pendências" no PLANO.

## Território
- **É seu:**
  - escolher o padrão de tela;
  - montar as variações;
  - aplicar o DS;
  - cobrir as camadas do fluxo.
- **Não é seu:**
  - regras visuais: tipografia, cor, tamanhos, espaçamento e componentes vêm **do design system**, não se decidem aqui;
  - avaliar usabilidade (`ui-heuristics`);
  - contraste e foco (`ui-accessibility`);
  - os textos da tela (`content-writing`, em paralelo);
  - vieses (`behavioral-design`);
  - handoff (`delivery-handoff`).

## Regras
1. **O DS decide o visual** `[prática, a partir do usuário]`. Tokens, tipografia, cor, tamanhos e componentes saem das skills e dos arquivos do DS (via `context-company`). Esta skill nunca fixa valores. Os princípios em `references/cor.md` e `references/tipografia.md` servem só **sem DS** ou para justificar uma proposta de mudança ao DS.
2. **Parta do que existe** `[prática, a partir do usuário]`:
   - **Navegue no produto e no fluxo atual em produção.** Peça ao designer para fazer login num acesso de teste; não use credenciais reais.
   - **Use o arquivo de templates do DS** como ponto de partida para as telas principais, em vez de recriar do zero.
3. **Alta fidelidade é o padrão** `[prática, a partir do usuário]`. Com DS e IA, a alta fidelidade é rápida e já tem a cara do produto. Baixa ou média fidelidade só pontualmente, para tirar carga cognitiva de quem decide e focar em fluxo ou palavras (`references/fidelidade.md`).
4. **Sempre variações para decidir, baseadas em benchmark** `[prática, a partir do usuário]`:
   - Use o quadro da skill `research-benchmark` (concorrentes diretos + análogos de outros nichos), rodando em paralelo quando ainda não existir.
   - Apresente **2 a 4 variações**. O número depende de quantos padrões realmente distintos o benchmark revelar; não invente uma variação só para completar.
   - Cada variação traz **de onde vem** ("é como o concorrente X faz", "segue o padrão da Amazon"), **prós e contras** e **qual dado ou princípio** a sustenta.
   - **O benchmark é ponto de partida, não validação.** O concorrente fazer algo não prova que é bom. Antes de apresentar, rode em paralelo as lentes `ui-heuristics`, `behavioral-design`, `ui-accessibility` e `content-writing` sobre cada variação. Os prós e contras devem refletir o que elas encontraram, não só o que o benchmark mostrou.
   - Marque **uma recomendada**, com a justificativa em uma linha.
5. **Do macro para o micro, em camadas** `[prática, a partir do usuário]`. Ataque só a camada em que a pessoa está. Não puxe loading ou motion antes de o caminho principal estar resolvido:
   1. **Escopo:** que problema o fluxo resolve e onde ele termina.
   2. **Caminho principal (golden path):** o fluxo funcionando de ponta a ponta.
   3. **Casos de borda:** vazio, erro, sem permissão, dados extremos.
   4. **Feedback do sistema:** loading, skeleton, progresso, sucesso.
   5. **Refinamento:** motion e microinterações, só onde agregam.
6. **Padrão antes de inovação** `[pós: M13]`. Inove só quando a inovação facilitar a tarefa.
7. **Lentes rápidas** `[prática]`. Antes de entregar, passe pela `ui-heuristics` e pela `ui-accessibility` e, se houver persuasão, pela `behavioral-design`.

## Fluxo
1. Ler o problema, a hipótese e o prazo no `projeto.md`.
2. Ver o fluxo atual em produção e os templates do DS.
3. Pegar o quadro da `research-benchmark` (ou rodá-la em paralelo).
4. Montar as variações em hi-fi, na camada certa.
5. Passar as lentes rápidas.
6. Entregar no artefato do projeto, para o designer revisar.

## Saída (curta)
```
Camada: caminho principal · Base: fluxo atual + template "<nome>" do DS
A · como o concorrente X faz — prós: … · contras: …
B · padrão da Amazon (análogo) — prós: … · contras: …
C (recomendada) · porque <dado/princípio>
Próxima camada: casos de borda
```

## Referências
- `references/padroes-de-tela.md`: catálogo de padrões e checklist por camada
- `references/componentes.md`, `references/cor.md`, `references/tipografia.md`: princípios para quando não houver DS
- `references/fidelidade.md`
- `references/fontes.md`
