# Como escolher a métrica

**Origem do conteúdo:**
- **Da pós** `[pós: M4]`: a ordem para decidir e o exemplo completo.
- **Do pacote** `[prática]`: a tabela "KPIs comuns" e as "Armadilhas" (exceto "medir tudo", que é `[pós: M4]`).
- **Externo** `[externo]`: o HEART.

## Ordem para decidir
1. **Objetivo primeiro.** Sem objetivo, nenhuma métrica faz sentido (M4).
2. **Entre as métricas disponíveis, qual mede melhor esse objetivo?** Essa vira o KPI.
3. **Uma métrica de guarda**: o que não pode piorar.
4. **Micro conversões** para diagnosticar onde a mudança age.

## Exemplo completo (M4)
**Problema:** é difícil abrir um chamado no site, e quem consegue acha o atendimento demorado. As reclamações no Reclame Aqui aumentaram.

| Objetivo | KPI | Ferramenta |
|---|---|---|
| Reduzir o tempo para abrir chamado | duração da sessão de quem concluiu a abertura | analytics, segmentado |
| Entender onde as pessoas se perdem | gravações de sessão | Hotjar ou similar |
| Reduzir abandono na jornada | taxa de saída por página da jornada | analytics |
| Reduzir reclamações | volume no Reclame Aqui | monitoramento |
| Aumentar chamados abertos pelo site | taxa de abertura (macro conversão) | analytics |

## KPIs comuns por tipo de objetivo
| Objetivo | KPI típico | Guarda típica |
|---|---|---|
| Ativação / onboarding | % que completa a primeira ação de valor em N dias | tempo até a primeira ação |
| Conversão de fluxo | taxa de conclusão do fluxo · saída por etapa | erros, tickets do fluxo |
| Engajamento | frequência de uso da feature por usuário ativo | retenção geral |
| Retenção | % ativo em D30 / M3 · churn | receita, NPS |
| Eficiência da tarefa | tempo mediano · taxa de sucesso | taxa de erro |
| Satisfação | CSAT da tarefa · tema do comentário | — |
| Suporte | tickets por 1.000 usuários sobre o tema | satisfação |

## HEART (referência externa: framework do Google)
Use quando precisar de uma lista ampla para não esquecer dimensões:
- **H**appiness: satisfação
- **E**ngagement: profundidade de uso
- **A**doption: novos usuários de algo
- **R**etention: volta
- **T**ask success: sucesso, tempo e erro

Para cada dimensão escolhida, defina **objetivo → sinal → métrica**.

## Armadilhas
- **Métrica de vaidade.** Pageviews e downloads crescem sem dizer se o problema foi resolvido.
- **Medir tudo.** "Quem mensura tudo não mensura nada" (M4).
- **Métrica sem segmento.** A média esconde segmentos opostos.
- **Mudar a definição no meio.** A linha de base e o resultado precisam medir a mesma coisa.
