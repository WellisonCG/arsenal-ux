# Plano de mensuração

Base: `[pós: M4: Plano de mensuração]` e `[artigo: Métricas Boss – Plano de Mensuração]` (Gustavo Esteves, que também é o autor do M4). As tabelas-modelo são `[prática]`.

## As 5 etapas
| Etapa | O que fazer | Saída |
|---|---|---|
| **1. Definir** | listar **todos** os objetivos da demanda (não só "vender") e o KPI de cada um | objetivos → KPIs (vindos da `strategy-hypotheses`) |
| **2. Documentar** | tipo de produto (e-commerce, app, PWA…), como funciona, o que acontece quando o usuário interage | mapa de interações relevantes |
| **3. Planejar a implementação** | responder: quais métricas e dimensões importam? que relatórios respondem aos objetivos? que configurações são necessárias? | lista de eventos e relatórios |
| **4. Implementar** | com dev e analytics (TI, marketing, produto), priorizando o que mapear | eventos no código |
| **5. Testar e refinar** | o dado está chegando certo? Corrija e crie uma rotina de checagem | tracking validado |

> "Quem mensura tudo não mensura nada." Medir tudo gera *data obesity*, custo (as ferramentas cobram por evento ou têm limite) e paralisia `[artigo: Métricas Boss]`.

## Modelo de especificação de evento `[prática]`
| Evento | Quando dispara | Propriedades | Hipótese / KPI | Responsável |
|---|---|---|---|---|
| `audience_estimate_viewed` | estimativa de alcance aparece na etapa 3 | `campaign_id`, `estimate_value`, `segment` | H1 · conclusão da etapa 3 | dev + analytics |
| `campaign_step_completed` | usuário avança uma etapa | `step`, `time_on_step` | H1 · micro conversão | dev |

**Regras do modelo:**
- **Nome do evento:** verbo no passado e objeto, num padrão único da empresa (`contexto/fontes-de-dados.md`).
- **Propriedades:** só as que permitem segmentar a leitura.
- **Documentação:** todo evento novo entra em `contexto/fontes-de-dados.md`, para não virar um "evento misterioso" depois `[artigo: Métricas Boss – Evento GA]`.

## Leitura do resultado `[prática]`, com base em `[artigo: NN/g – Formative vs. Summative]`
| Campo | Exemplo |
|---|---|
| Data de leitura | 30 dias após 100% do rollout |
| Comparação | mesmo período e mesmo segmento, antes × depois; ou controle × variante |
| Quem lê | designer + PM + analytics |
| Critério | meta da hipótese; sinal de "erramos se…"; guarda |
| Cuidados | checklist de sanidade (`research-evidence`); significância no A/B (`strategy-hypotheses`) |
