---
name: context-company
description: Ponte entre o pacote Arsenal UX e a empresa. Lê a pasta contexto/ do workspace (empresa, produto, fontes de dados, design system, stakeholders, pesquisas) e diz às outras skills o que existe e o que tem precedência. Use quando o arsenal carregar contexto; quando alguém perguntar "que dados temos", "onde vejo X", "qual componente do DS", "quem decide"; ou para montar o contexto da empresa pela primeira vez ("monta o contexto", "configurar o pacote", "setup").
---

# Contexto da empresa

> **Pendente para o ambiente da empresa:** só dá para validar rodando no computador da empresa. Antes de qualquer coisa, levantar o que as skills existentes lá já cobrem e deixar aqui apenas a ligação com elas, sem duplicar conteúdo.

**Origem do conteúdo:** esta skill inteira é `[prática]`, a estrutura de portabilidade do pacote. A ideia de que a convenção deliberada do projeto vence a regra genérica vem do padrão da família better-ui (jakubkrehel/skills), que é referência externa do pacote e não da pós.

## Território
- **É seu:** ler e manter `contexto/`, responder o que existe (fontes de dados, DS, métricas, stakeholders, pesquisas anteriores) e aplicar a precedência.
- **Não é seu:** analisar os dados (`research-evidence`) e desenhar com o DS (`ui-craft`). Você só diz **onde** está cada coisa e **quem** a usa.

## Precedência
1. **Skills e convenções do design system da empresa**: tokens, componentes, padrões.
2. **`contexto/`**: negócio, métricas oficiais, restrições.
3. **Skills genéricas do Arsenal UX.**

Uma convenção deliberada e consistente da empresa (por exemplo, "não usamos sombras") é preferência, não erro. Nenhuma skill do pacote aponta como problema algo que o DS define assim.

## Ao carregar
1. Leia os arquivos existentes em `contexto/`. Não invente o que estiver vazio.
2. Devolva às outras skills um resumo curto:
   - fontes de dados acessíveis e o modo de acesso de cada uma;
   - as skills do DS e quando chamar cada uma;
   - as métricas oficiais;
   - as restrições que mudam recomendações.
3. Se uma fonte de `fontes-de-dados.md` tiver acesso direto (MCP, API, consulta), avise `research-evidence` de que pode buscar sem pedir.
4. Se o acesso for "pedir para alguém", diga a quem pedir e qual pergunta fazer.

## Setup pela primeira vez
1. Copie os modelos de `templates/` (nesta pasta da skill) para `contexto/` na raiz do workspace.
2. Preencha por entrevista, com no máximo 5 perguntas por arquivo. Comece por `fontes-de-dados.md` e `design-system.md`, que destravam mais coisas.
3. Se houver ferramentas conectadas (analytics, suporte, Figma), liste o que elas expõem e preencha a partir disso. Mostre o resultado para a pessoa conferir.

## Sem `contexto/`
O pacote funciona mesmo assim. As outras skills perguntam ao designer o que precisarem. Sugira o setup **uma vez**, no fim da primeira resposta, sem insistir.
