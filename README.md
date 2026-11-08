# Arsenal UX

Pacote de skills de design. O **`uxpert`** é o especialista que conduz cada demanda e monta o time certo de skills, rodando em paralelo as que são independentes. O processo é fluido: as fases orientam, não são uma receita.

## As skills
| Tipo | Skill | Faz |
|---|---|---|
| Condutor | `uxpert` | conduz a demanda, escolhe e combina as skills, mantém o `projeto.md` |
| Fase 1 | `strategy-framing` | coleta o contexto e monta o problema; o designer valida |
| Fase 2 | `research-evidence` | busca os dados que já existem, com fonte |
| Fase 3 | `strategy-hypotheses` | transforma palpites em hipóteses e métricas |
| Fase 4 | `ui-craft` | variações em hi-fi com o DS, baseadas em benchmark |
| Fase 6 | `delivery-handoff` | entrega para o dev *(pendente: integrar com a skill da empresa)* |
| Fase 3 e 6 | `delivery-metrics` | plano de mensuração e leitura do resultado |
| Transversal | `strategy-timebox` | prazo real e o que cabe nele |
| Transversal | `research-studies` | método, recrutamento, roteiro e condução |
| Transversal | `research-synthesis` | insights e mapas (afinidade, empatia, jornada, blueprint…) |
| Transversal | `research-benchmark` | concorrentes e análogos |
| Transversal | `behavioral-design` | vieses em todas as fases, com checagem ética |
| Lente | `ui-heuristics` | Nielsen, Leis de UX, Gestalt |
| Lente | `ui-accessibility` | WCAG 2.2 AA e ABNT NBR 17225 *(pendente: conflito com o DS)* |
| Lente | `content-writing` | texto de interface |
| Ponte | `context-company` | fontes de dados, DS e métricas da empresa *(pendente: validar lá)* |

**Fontes:** os MDs são a base curada. Para ir além, as skills buscam nas fontes de `skills/uxpert/references/fontes-confiaveis.md` e citam o link.

## Instalar
```
/plugin marketplace add <caminho-ou-repo-deste-pacote>
/plugin install arsenal-ux@arsenal-ux
```

## Usar na sua empresa
1. Copie `skills/context-company/templates/` para a raiz do workspace como `contexto/` e preencha. Outra opção é pedir: "monta o contexto da empresa".
2. Em `contexto/design-system.md`, aponte as skills do seu DS.
3. Cada demanda ganha `projetos/<demanda>/projeto.md`, que é local, um por projeto.

**Precedência:** design system da empresa > `contexto/` > skills deste pacote.

## Comandos
- `/nova-demanda`: começa uma demanda nova
- `/plano-pesquisa`: monta pesquisa (método, recrutamento, roteiro)
- `/revisar-tela`: lentes em paralelo (heurísticas, acessibilidade, vieses, UX writing)
- `/handoff`: entrega e plano de medição, em paralelo

## Estrutura
```
.claude-plugin/   manifesto do plugin
skills/           16 skills (SKILL.md + references/)
  uxpert/templates/projeto.md          memória de cada demanda
  uxpert/references/fontes-confiaveis.md
  context-company/templates/           modelos do contexto/
commands/         atalhos
_fontes/          material da pós, só local (fora do git)
```
