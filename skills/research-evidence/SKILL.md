---
name: research-evidence
description: Fase 2 do processo de design. Busca de forma proativa o que já se sabe sobre um problema (analytics, funil, tickets, reviews, Reclame Aqui, pesquisas anteriores, desk research, benchmark, literatura), cita a fonte de cada dado, triangula fontes de tipos diferentes, coloca o número em contexto, checa se o dado faz sentido e monta a tabela de evidências com as lacunas. Use quando alguém disser "por que X acontece", "quero entender", "o que os dados dizem", "tem dado sobre isso?", "desk research", "benchmark", "analisar funil", "churn", "abandono", "conversão caiu", "taxa de rejeição".
---

# Investigar evidências

> Analytics responde **o que** está acontecendo. UX responde **por quê**. As duas juntas permitem decidir melhor `[pós: M4]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:** dados que **já existem**. Buscar, citar a fonte, triangular, contextualizar, checar a sanidade, interpretar, sugerir a visualização e apontar lacunas.
- **Não é seu:**
  - gerar dado novo com entrevista, formulário ou teste (`research-studies`);
  - definir a métrica de sucesso (`strategy-hypotheses`);
  - medir depois do lançamento (`delivery-metrics`).

## Regras
1. **Seja proativo** `[prática]`. Busque sem esperar pedido. Ao começar, avise numa linha o que vai olhar e por quê, e siga.
2. **Cite a fonte de todo dado** `[prática]` no formato `[fonte: sistema › objeto · período]`, com o nível de evidência ao lado (`[empresa]`, `[pesquisa]`, `[estudo]`, `[heurística]`, `[opinião]`). Dado sem fonte deve ser escrito como suposição.
3. **Interprete, não só leia** `[pós: M4]`. Um número sem contexto não permite conclusão.
4. **Não meça tudo** `[pós: M4]` `[artigo: Métricas Boss – Plano de Mensuração]`. "Quem mensura tudo não mensura nada." O excesso de dados (*data obesity*) deixa o time perdido. Busque o que responde às perguntas da fase 1.
5. **Triangule** `[artigo: NN/g – How Well Discovery Phases Are Performed]`. Pesquisa exploratória fica mais confiável quando os dados vêm de várias fontes e métodos. Nenhuma conclusão deve depender de uma fonte só.
6. **Investigue, não "valide"** `[artigo: NN/g – You Are Not the User]`. Procure o que pode **derrubar** a ideia, não só o que a confirma.

## Fluxo

### 1. Partir das perguntas da fase 1 `[pós: M1]` `[pós: M4]`
Pegue o objetivo de discovery, as perguntas e os **achismos** do `projeto.md`. Para cada um, defina que tipo de evidência o responderia:
- **Comportamento** (quanti): o que as pessoas fazem.
- **Motivo** (quali): por que fazem.

Se a fase 1 não aconteceu, pergunte uma vez qual decisão a investigação precisa apoiar.

### 2. Escolher as fontes
Siga a ordem abaixo `[prática]` e pare quando as perguntas estiverem respondidas:

| Ordem | Fonte | Responde | Exemplos |
|---|---|---|---|
| 1 | **Dados da empresa** (`contexto/fontes-de-dados.md`) | o quê | funil, eventos, taxa de saída, segmentos, receita |
| 2 | **Pesquisas anteriores** (`contexto/pesquisas.md`) | por quê | entrevistas, testes, NPS com comentário |
| 3 | **Voz do cliente** | por quê | tickets, chat, reviews nas lojas, Reclame Aqui, vendas e CS `[pós: M1, M4]` |
| 4 | **Comportamento observável** | como | gravação de sessão, mapa de calor `[pós: M4]` |
| 5 | **Benchmark** | como outros resolvem | concorrentes, produtos análogos `[pós: M1]` |
| 6 | **Literatura** | o que já se sabe em geral | NN/g, Google Acadêmico, Portal CAPES, ACM Digital Library `[pós: M4]` |

As fontes 3 a 6 são **pesquisa secundária**: dados de terceiros que aceleram o discovery `[pós: M1]`. Veja `references/fontes-desk-research.md`.

### 3. Colocar todo número em contexto `[pós: M4]`
Antes de apresentar um número, responda:
- **Qual o recorte?** Página, canal, segmento, plataforma. "87% de rejeição" não diz nada. "87% de rejeição na landing do curso vinda de Google Ads" já permite comparar com outros canais.
- **Comparado com o quê?**
  - um período equivalente (janeiro com janeiro, se houver sazonalidade);
  - a meta;
  - outro segmento.
- **Qual a meta?** Sem meta, qualquer número parece interessante.
- **Comparar com concorrente?** Só com cuidado. A métrica que importa para eles pode não importar para nós.

### 4. Checar a sanidade
Rode `references/checklist-sanidade.md` antes de concluir. Os itens que mais derrubam conclusões:
- tracking quebrado ou evento que mede outra coisa;
- amostra que não representa a população-alvo;
- correlação tratada como causa;
- período incomparável;
- viés de sobrevivência;
- média enganosa.

Se algum item falhar, **não descarte o dado**. Diga o limite e rebaixe a confiança `[prática]`.

### 5. Juntar o quê com o porquê `[pós: M4]`
- Para cada achado quanti, procure uma evidência quali que explique o motivo.
- Se não houver, o porquê vira **hipótese**, não conclusão. Exemplo do M4: "85% saem no cadastro. Na gravação de sessão, a saída acontece no campo Título de eleitor. Hipótese: as pessoas não têm o documento em mãos."

### 6. Fechar com evidências e lacunas `[prática]`
- Monte a tabela de evidências.
- Atualize os achismos: cada um vira **confirmado**, **derrubado** ou **hipótese**.
- Liste as lacunas e, para cada uma, sugira a coleta mais barata que cabe no prazo, chamando a `research-studies`.

## Saída
Preencha a seção 2 do `projeto.md`:

```
| Evidência | Fonte | Nível | Data |
| 62% param na etapa 3 do funil de campanha | [fonte: Analytics › campaign_step · 01/08–31/10] | empresa | 2026-11-08 |
| 18 de 40 tickets citam "não entendi o público" | [fonte: Zendesk › tag campanha · out/26] | empresa | 2026-11-08 |

Triangulação: <quais tipos de fonte sustentam cada conclusão>
Achismos: <confirmado / derrubado / virou hipótese>
Limites: <ex.: evento da etapa 3 mudou em 15/09, então comparar só depois dessa data>
Lacunas → pesquisar: <pergunta · coleta sugerida · tempo>
Leitura: <2 a 3 frases sobre o que as evidências dizem, sem extrapolar>
```

Se a pessoa pedir gráfico, use `references/qual-grafico.md`.

## Referências
- `references/checklist-sanidade.md`
- `references/fontes-desk-research.md`
- `references/qual-grafico.md`
- `references/fontes.md`: material da pós e artigos lidos para esta skill
