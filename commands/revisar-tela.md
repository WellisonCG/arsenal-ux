---
description: Revisa uma tela ou fluxo pelas lentes de heurísticas, vieses, acessibilidade e UI e devolve um relatório priorizado
argument-hint: <print, link do Figma, arquivo ou descrição da tela>
---

Use a skill `uxpert` para revisar:

$ARGUMENTS

1. Se não estiver claro qual problema a tela resolve e para quem, faça **uma** pergunta e siga.
2. Rode em paralelo as lentes `ui-heuristics`, `ui-accessibility`, `behavioral-design` e `content-writing`, e junte os achados sem repetição. Respeite o DS da empresa via `context-company`.
3. Devolva um relatório único, com o achado mais severo primeiro, nas colunas:
   `Severidade | Onde | Problema | Recomendação | Princípio | Trade-off | Como medir`
4. Liste o que não foi possível verificar como "Não verificado".
