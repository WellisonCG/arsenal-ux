---
name: behavioral-design
description: Especialista transversal em vieses cognitivos e economia comportamental, chamado em qualquer fase (entender, pesquisa, hipóteses, UI). Tem três usos. Aplicar vieses a favor do usuário (efeito padrão, ancoragem, enquadramento, prova social, escolha limitada, pico-fim, Zeigarnik, blocamento). Auditar se uma tela explora vieses e vira dark pattern (padrão pré-marcado enganoso, escassez falsa, reatância). Apontar vieses do próprio time e da pesquisa (confirmação, disponibilidade, maldição do conhecimento, sobrevivente, Hawthorne). Inclui o Framework CBB e um roteiro de experimento comportamental. Use quando alguém disser "viés", "psicologia", "persuasão", "nudge", "dark pattern", "economia comportamental", "como aumentar conversão", "escassez", "urgência", "prova social", "efeito padrão", "Framework CBB", "arquitetura de escolha".
---

# Vieses cognitivos

> Vieses **descrevem** comportamento; eles não o **causam** `[artigo: Behavioral Scientist – More Than Biases]`. Mais do que decorar os mais de 200 vieses mapeados, importa entender os princípios por trás deles `[pós: M12]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:**
  - vieses no produto, tanto a favor quanto contra o usuário;
  - a checagem ética (dark patterns);
  - os vieses do time e da pesquisa;
  - experimentos comportamentais (CBB).
- **Não é seu:**
  - usabilidade geral (`ui-heuristics`); as Leis de UX que também são vieses ficam lá como usabilidade e vêm para cá quando usadas para **persuadir**;
  - a condução da pesquisa (`research-studies`), que recebe daqui os alertas de viés;
  - a métrica e a leitura do experimento (`strategy-hypotheses`).

## Onde atua
Esta skill é **transversal**. Ela embasa todas as fases, não só a UI:
- **Entender:** que vieses aparecem no pedido e nos stakeholders (confirmação, autoridade)?
- **Pesquisa:** o roteiro e a amostra estão enviesados?
- **Hipóteses:** que viés explica o comportamento observado, e que viés do time pode estar distorcendo a leitura?
- **UI:** aplicar a favor do usuário e auditar a ética.

## De onde vem o conhecimento
- **Base curada:** `references/catalogo.md`, com os vieses do curso (M12) `[pós]`.
- **Além da base:** existem mais de 200 vieses mapeados `[pós: M12]`. Busque nas fontes de `uxpert/references/fontes-confiaveis.md`:
  - **principal:** The Decision Lab;
  - **apoio:** Behavioral Scientist e o estudo original no Google Acadêmico;
  - **para achar o termo:** a Wikipedia e o Codex, só como índice.
- **Sempre:** cite o link, marque `[externo]` e avise quando um viés tiver problema de replicação.

## Princípio-guia `[pós: M12]`
O design **sempre** influencia o comportamento, de forma intencional ou não, então é melhor fazer isso de propósito e com ética. O ambiente molda o comportamento: no teste do marshmallow, o contexto muda a escolha. Mudar um comportamento é diferente de criar um hábito.

## Os 4 problemas que os vieses resolvem `[pós: M12]`
O cérebro toma mais de 35 mil decisões por dia e usa atalhos para dar conta de quatro problemas:

| Pilar | Problema | O cérebro preenche com… | Vieses do curso |
|---|---|---|---|
| **Informação** | informação demais | mudanças, bizarrices, repetição, confirmação | disponibilidade, confirmação, ancoragem, mera exposição, enquadramento, escolha limitada, contraste, apoio à escolha |
| **Ambiguidade** | falta de significado | padrões, generalizações, problemas mais fáceis | prova social, maldição do conhecimento, sobrevivente, autoridade, mão quente, história, atalho metafórico, efeito padrão |
| **Tempo / ação** | necessidade de agir rápido | "você está certo", "o mais perto é melhor", "o mais fácil é melhor" | Hawthorne, IKEA, aversão ao risco, reatância, escassez |
| **Memória** | o que lembrar | memórias existentes, generalização, memória externa | posição serial, Zeigarnik, blocamento, curiosidade, pico-fim |

Detalhes de cada viés, com uso ético e risco, estão em `references/catalogo.md`.

## Uso 1: aplicar a favor do usuário
1. **Comece pelo comportamento, não pelo viés** `[pós: M12]`. Qual ação queremos que aconteça? Quais barreiras impedem? Use o Framework CBB (`references/frameworks.md`).
2. **Escolha o princípio que remove a barreira.** Por exemplo:
   - se a barreira é excesso de opções, use **escolha limitada** e um **padrão** recomendado;
   - se é falta de confiança, use **prova social**;
   - se é esforço, use **blocamento** (dividir em partes) e **objetivo gradiente**.
3. **Teste.** Vieses são tendências amplas, não traços fixos. A mesma intervenção pode não ter efeito ou sair pela culatra dependendo do contexto `[artigo: Behavioral Scientist – More Than Biases]`. Os padrões, por exemplo, funcionam muito em média (a opção pré-selecionada é escolhida cerca de 27% mais vezes), mas variam bastante de estudo para estudo `[artigo: Behavioral Scientist – Defaults]`. Nunca aplique sem medir: chame a `strategy-hypotheses`.

## Uso 2: auditar (checagem ética)
Rode `references/etica.md` sempre que uma tela usar intencionalmente padrão, escassez, urgência, prova social, ancoragem de preço ou enquadramento. A pergunta central `[prática]`:

> **O usuário faria a mesma escolha se entendesse o mecanismo, e consegue desfazer com facilidade?**

A linha entre persuasão e dark pattern é fina. O pacote preza por conversão e pelos objetivos de negócio, então **não descarte boas opções por excesso de rigor**. Classifique em três níveis `[prática, a partir do usuário]`:

| Nível | Quando | O que fazer |
|---|---|---|
| **Persuasão legítima** | ajuda o usuário a completar o objetivo dele e o do negócio: plano recomendado em destaque, prova social real, urgência verdadeira, padrão que favorece o usuário | segue |
| **Zona cinzenta** | funciona, mas pode ser lido como pressão ou esconde algo em parte | **segue na mesa**, com um alerta ao designer: o risco, uma alternativa mais transparente e a métrica de guarda para acompanhar |
| **Dark pattern** | só funciona se o usuário não perceber: custo escondido, cancelamento labiríntico, culpa na recusa, urgência ou escassez falsa, opt-in pré-marcado para algo que ele não pediu | **CRÍTICO** |

Teste: sabendo exatamente o que está acontecendo, o usuário ainda escolheria aquilo? Se sim, é persuasão. Se depende de ele não perceber, é dark pattern.

Exemplo do curso: deixar pré-marcadas as opções que o negócio quer que sejam aceitas é uso enganoso do efeito padrão `[pós: M12]`. O mesmo vale para a compra recorrente pré-selecionada `[pós: M13]`. Pressão demais também falha por si só: pela **reatância**, o usuário faz o oposto e desiste `[pós: M12]`.

## Uso 3: autocrítica do time e da pesquisa
Antes de concluir algo, pergunte `[pós: M1, M12]`:
- **Confirmação:** estamos buscando só o que confirma nossa ideia?
- **Disponibilidade:** estamos dando peso demais ao caso mais recente ou mais lembrado, como o último ticket irritado?
- **Maldição do conhecimento:** o que é óbvio para nós é óbvio para o usuário? Use metáforas e linguagem do usuário.
- **Sobrevivente:** olhamos só quem ficou ou converteu?
- **Mão quente e autoridade:** estamos aceitando a ideia por causa de quem a deu?
- **Hawthorne:** o comportamento no teste mudou por estar sendo observado?
- **Priming na pesquisa:** a tarefa usou as mesmas palavras da interface e entregou a resposta? `[artigo: NN/g – Priming]`

## Saída
**Aplicar:**
```
Comportamento-chave: <…> · Barreira principal: <…> · Princípio: <viés> · Hipótese: Se <…>, então <…>, porque <…>
Checagem ética: legítimo / ajustar (como) · Como medir: <KPI + guarda>
```

**Auditar** (mesmo formato de achado das lentes):
```
| Severidade | Onde | Viés usado | Problema | Recomendação | Trade-off | Como medir |
```

## Referências
- `references/catalogo.md`: vieses do curso por pilar, com uso ético, risco e exemplo
- `references/etica.md`: checagem ética e dark patterns
- `references/frameworks.md`: Framework CBB, roteiro de experimento em 8 etapas, dissecação de produtos
- `references/fontes.md`
