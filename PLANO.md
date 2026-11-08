# Arsenal UX — Plano do pacote de skills

> v3 · 2026-11-08 · revisado com os 21 comentários do usuário no canvas de revisão (https://claude.ai/artifact/2W1ejZYmqhFbTmQLjTpxci).
> O condutor agora se chama `uxpert`, e as regras de comportamento atuais (C1 a C11) estão em `skills/uxpert/SKILL.md`. As seções 1 e 2 abaixo são da v2: valem como histórico.

## Mudanças da revisão (v3)
- **Condutor renomeado** de `parceiro-senior` para `uxpert` (trocadilho com expert): um especialista em todas as áreas de UX.
- **Propositivo em vez de questionário.** A skill coleta (Slack, transcrições, Pendo, NPS, churn) e monta rascunhos; o designer valida.
- **Sucinto, "sugerir e produzir".** Entrega materiais em vez de textão no chat. O formato sugerido é um artefato de design com pranchas, mas é opcional.
- **Postura:** processo fluido, não receita de bolo. O caminho mais rápido até o usuário, com a estratégia de lançamento escolhida conforme a demanda; os exemplos não são regra.
- **Fontes confiáveis, sempre com link.** Os MDs são a base curada, não o limite. Para ir além, a skill busca em fontes validadas por área (`skills/uxpert/references/fontes-confiaveis.md`), com uma principal e 1 ou 2 de apoio, e cita o link.
- **Especialistas transversais:** `behavioral-design` e `research-studies` podem ser chamados em qualquer fase.
- **Timebox transversal:** entra logo depois de entender a demanda e limita os métodos das outras skills.
- **Alta fidelidade com o DS é o padrão.** Baixa e média viram exceção.
- **Pesquisa:** sem meta por cohort, com decisão caso a caso, loop de revisão do roteiro em 2 a 3 voltas e benchmark padrão (concorrentes + análogos).
- **UI:** variações sempre baseadas em benchmark, com origem, prós e contras e uma recomendada; trabalho do macro para o micro em camadas; regras visuais vêm do DS.
- **Hipóteses:** com baixa confiança, três caminhos (descartar, assumir ou reduzir o risco), e quem decide é o designer.
- **Vieses:** três níveis (persuasão, zona cinzenta, dark pattern), sem descartar boas opções por excesso de rigor.

## Divisão em especialistas (v4, 2026-11-08)
Algumas skills faziam papel demais. Foram divididas para que o `uxpert` possa rodar várias em paralelo:

| Antes | Agora |
|---|---|
| `research-studies` fazia plano, condução, síntese, mapas e benchmark | `research-studies` (plano e condução) + `research-synthesis` (insights e mapas) + `research-benchmark` |
| `ui-craft` também escrevia os textos | `ui-craft` + `content-writing` |
| `entregar-e-medir` | `delivery-handoff` (pendente) + `delivery-metrics` |

São 16 skills no total. O `uxpert` ganhou a seção "Especialistas trabalhando juntos", com combinações comuns, que são exemplos, e regras para montar o time.

## Padrão de nomes (v5, 2026-11-08)
O formato é **`área-especialidade`**: nomes em inglês, conteúdo em português. A área funciona como o "cargo"; a especialidade mantém cada skill pequena e possível de rodar em paralelo.

| Área | Skills |
|---|---|
| Condutor | `uxpert` |
| Strategy | `strategy-framing` · `strategy-hypotheses` · `strategy-timebox` |
| Research | `research-evidence` · `research-studies` · `research-synthesis` · `research-benchmark` |
| Behavioral | `behavioral-design` |
| UI | `ui-craft` · `ui-heuristics` · `ui-accessibility` |
| Content | `content-writing` |
| Delivery | `delivery-handoff` · `delivery-metrics` |
| Context | `context-company` |

**Nomes antigos → novos:**
- entender-demanda → strategy-framing
- definir-hipoteses → strategy-hypotheses
- planejar-timebox → strategy-timebox
- investigar-evidencias → research-evidence
- pesquisar → research-studies
- sintetizar → research-synthesis
- benchmark → research-benchmark
- vieses-cognitivos → behavioral-design
- heuristicas → ui-heuristics
- acessibilidade → ui-accessibility
- ux-writing → content-writing
- handoff → delivery-handoff
- medir-resultado → delivery-metrics
- contexto-empresa → context-company

**Skill nova:** use uma área existente. Se nenhuma servir, crie uma área nova só quando ela tiver pelo menos duas skills.

## Pendências para o ambiente da empresa
| Skill | O que revisar lá |
|---|---|
| `delivery-handoff` | integrar com a skill de handoff do usuário (histórias, casos de uso); decidir se o tracking (hoje em `delivery-metrics`) entra nela |
| `ui-accessibility` | resolver o conflito com a skill do DS: uma fonte da verdade para as regras gerais |
| `ui-craft` | adaptar ao DS conectado, às skills de navegação na plataforma e ao arquivo de templates |
| `context-company` | validar rodando lá e ligar com as skills existentes, sem duplicar |
| `behavioral-design` | ampliar o catálogo além dos cerca de 30 vieses do M12, cada um com estudo e link |
| `content-writing` | confirmar onde está o content design (dentro do DS ou fora dele) e usar esse material como base |

## 1. A ideia central

Um **designer sênior sentado ao lado** de qualquer pessoa do time. Ele não segue cartilha: usa uma caixa de ferramentas.

### Regras de comportamento (valem para todas as skills)

| # | Regra |
|---|---|
| C1 | **Pergunta antes de responder** quando falta contexto crítico. No máximo 3–5 perguntas, começando pelas que mais mudam a resposta |
| C2 | **É propositivo com dados.** Busca sem esperar pedido e **sempre diz de onde tirou cada dado** (sistema, evento, período, link), para o designer conferir |
| C3 | **Proporcional ao tempo.** A recomendação cabe no prazo |
| C4 | **Caixa de ferramentas, não cartilha.** Oferece 2–3 opções com custo e tempo de cada uma, e marca a recomendada |
| C5 | **Nível de evidência explícito:** dado da empresa > pesquisa própria > estudo publicado > heurística > opinião |
| C6 | **Ensina o porquê**, dando nome à técnica para a pessoa conseguir repetir sozinha |
| C7 | **Imperfeição aceita.** Registra o trade-off em vez de bloquear |
| C8 | **Memória do projeto.** Tudo o que for decidido vai para o `projeto.md` da demanda |

## 2. O processo: 6 fases em duplo diamante

| Fase | Pergunta central | Skill dona | Apoio |
|---|---|---|---|
| **1 Entender** | Qual é o problema de verdade? | `strategy-framing` | — |
| **2 Investigar** | O que já sabemos? | `research-evidence` | `research-studies`, `behavioral-design`, `context-company` |
| **3 Definir** | O que vamos testar e como vamos medir? Como distribuímos o prazo? | `strategy-hypotheses` + `strategy-timebox` | `behavioral-design` |
| **4 Criar** | Como resolvemos? | `ui-craft` | `ui-heuristics`, `behavioral-design`, `ui-accessibility`, `context-company` |
| **5 Validar** | Funciona? | `research-studies` + `ui-heuristics` + `ui-accessibility` | `behavioral-design`, `ui-craft` |
| **6 Entregar e medir** | Está pronto para o dev? Deu certo depois do lançamento? | `entregar-e-medir` | `ui-accessibility`, `context-company` |

O **`uxpert`** conduz o fluxo todo: identifica em que fase a demanda está, avisa quando uma fase foi pulada, chama as skills e mantém o `projeto.md`.

O resultado medido na fase 6 vira evidência da próxima demanda e volta para a fase 2.

## 3. Os dados em três momentos (substitui o antigo "plano de dados")

| Momento | O que é | Skill |
|---|---|---|
| **O que já existe** (fase 2) | Analytics, funil, tickets, reviews, pesquisas anteriores, desk research, benchmark | `research-evidence` |
| **O que geramos** (fases 2 e 5) | Formulário quanti, entrevistas por cohort, teste de usabilidade, first-click… | `research-studies` |
| **Como saberemos se deu certo** (fases 3 e 6) | Métrica de sucesso e linha de base (fase 3), eventos instrumentados e leitura do resultado (fase 6) | `strategy-hypotheses`, `entregar-e-medir` |

## 4. As 12 skills

| Skill | Tipo | Faz | Fontes da pós |
|---|---|---|---|
| `uxpert` | condutor | Conduz o fluxo, mantém o `projeto.md`, aplica as regras C1–C8 | Times de UX de uma pessoa só (M7), Agile UX (M8), Design Ops |
| `strategy-framing` | processo | Perguntas socráticas, separação entre problema e solução pedida, stakeholders, prazo | Fundamentos (M1), Guia de Entrevistas com Stakeholders, Workshop Design Engineer |
| `research-evidence` | processo | Busca proativa de dados existentes, com a fonte citada, checagem de sanidade e tabela de evidências | UX Analytics e Estatística (M4, M5), dataviz |
| `strategy-hypotheses` | processo | Hipótese testável + sinal de erro, métrica de sucesso e linha de base, priorização | Workshop Design Engineer (hipóteses), M4 |
| `strategy-timebox` | processo | Perfil do projeto (problema claro ou obscuro × solução conhecida ou nova), distribuição do tempo, checkpoints | Agile UX (M8), M7 |
| `ui-craft` | processo | Fidelidade, padrões de tela, componentes, cor e tipografia; delega a execução para o DS | UI Estratégico (M13: 7–14) |
| `entregar-e-medir` | processo | Checklist de handoff, eventos a instrumentar, leitura do resultado, fechamento das hipóteses | M13 (15.1), Design Ops e Content Ops |
| `research-studies` | caixa de ferramentas | Escolha de método por pergunta × prazo, recrutamento por cohort, roteiros, síntese | UX Research Avançado (M2, M3), Research Ops (M10, M11), Práticas de UX com IA |
| `ui-heuristics` | lente | Nielsen com severidade, Leis de UX, Gestalt, atenção e memória | M13 (2–6) |
| `behavioral-design` | lente | Aplicar no produto, auditar dark patterns, apontar vieses do time e da pesquisa | Vieses Cognitivos (M12) |
| `ui-accessibility` | lente | WCAG 2.2 AA; achado crítico sempre sobe para o topo | M13 (7.1) + WCAG |
| `context-company` | ponte | Fontes de dados, DS, métricas oficiais, stakeholders; é a única skill que muda no trabalho | — |

**Comandos:** `/nova-demanda` (fases 1→3), `/plano-pesquisa`, `/revisar-tela` (fase 5), `/handoff` (fase 6).

**Fora do pacote de design:** Inteligência Emocional, Governança, FastClass, MicroSaaS, APIs de IA. Liderança e Persuasão pode entrar no `uxpert`, no ponto de *apresentar e defender decisões*.

## 5. Timebox (`strategy-timebox`)

| Perfil | Entender | Investigar | Definir | Criar | Validar | Entregar |
|---|---|---|---|---|---|---|
| Executar (claro · conhecida) | 5 | 5 | 5 | 55 | 15 | 15 |
| Explorar visual (claro · nova) | 5 | 10 | 5 | 45 | 25 | 10 |
| Investigar (obscuro · conhecida) | 15 | 35 | 10 | 20 | 10 | 10 |
| Descobrir (obscuro · nova) | 10 | 25 | 10 | 25 | 20 | 10 |

Valores em % do prazo. Checkpoints por prazo: **3 dias → 1**, **1 semana → 2**, **3 semanas → 3–4**. São um ponto de partida para você ajustar.

## 6. Onde mora o conhecimento

| Camada | O que fica |
|---|---|
| `SKILL.md` | Regras, fluxo, checklists. Enxuto, sempre carregado |
| `references/` | Síntese própria do material da pós (catálogos, matrizes, templates). Carregado sob demanda |
| `references/fontes.md` | Links públicos (NN/g, The Decision Lab, Laws of UX, WCAG), curados a partir dos 403 links das disciplinas |

Os PDFs ficam em `_fontes/` (local e fora do pacote via `.gitignore`), por três motivos: tamanho, direitos de uso e o fato de slide não ser instrução.

### Como cada skill é escrita
1. **Ler o material didático** da pós ligado à skill: os capítulos relevantes, não o PDF inteiro.
2. **Ler os artigos referenciados** pela disciplina que tratam do tema da skill. Se um link estiver bloqueado, tentar pelo navegador. Se não abrir, registrar como "não lido".
3. **Sintetizar com palavras próprias** em regras aplicáveis.
4. **Marcar a origem de cada bloco:** `[pós: M4]` · `[artigo: NN/g – …]` · `[prática]` (recomendação do pacote, sem fonte) · `[externo]` (fonte de fora da pós).
5. **Criar `references/fontes.md`** na skill, com o material da pós, os artigos lidos (link + data + onde cada um foi usado) e o que ficou sem ler.

## 7. Portabilidade para o trabalho

`contexto/` com `empresa.md`, `produto.md`, `fontes-de-dados.md` (a peça essencial para a fase 2), `design-system.md` (ponteiro para as skills do DS), `stakeholders.md` e `pesquisas.md`.

**Precedência:** DS da empresa > contexto > skills genéricas.

**Distribuição:** plugin do Claude Code.

## 8. Roadmap

0. ~~Validar o processo (`processo.html`)~~ ✓
1. ~~Esqueleto do plugin + `uxpert` + `projeto.md` + `contexto/`~~ ✓ (as outras 10 skills existem como rascunho, com território e gatilhos)
2. ~~Fases 1–3~~ ✓ `strategy-framing`, `research-evidence`, `strategy-hypotheses`, `strategy-timebox`, cada uma com `references/`, sintetizadas de M1, M4, M5, M7 e M8
3. ~~`research-studies` + lentes (`ui-heuristics`, `behavioral-design`, `ui-accessibility`)~~ ✓
4. ~~`ui-craft`, `entregar-e-medir`~~ ✓. Todas as 12 skills têm conteúdo, origem marcada e `fontes.md` (2026-11-08)
5. Revisão do usuário ← **próximo**
6. Testes com demandas reais (cenários S1–S9)
7. Exportar e adaptar no trabalho: `strategy-framing`, `research-evidence`, `strategy-hypotheses`, `strategy-timebox`
3. `research-studies` + lentes (`ui-heuristics`, `behavioral-design`, `ui-accessibility`)
4. `ui-craft`, `entregar-e-medir`, comandos
5. Testes com demandas reais
6. Exportar e adaptar no trabalho
