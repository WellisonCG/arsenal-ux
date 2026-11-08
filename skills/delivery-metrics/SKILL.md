---
name: delivery-metrics
description: Especialista em medição, chamado antes e depois do lançamento. Antes, monta o plano de mensuração (objetivos, KPIs, eventos e propriedades a instrumentar, linha de base, teste do tracking). Depois, lê o resultado como avaliação somativa, fecha cada hipótese como confirmada, derrubada ou inconclusiva e registra o aprendizado para as próximas demandas. Use quando alguém disser "instrumentar", "eventos de analytics", "plano de mensuração", "tracking", "lançou", "deu certo?", "medir resultado", "pós-lançamento", "ler o A/B", "rollout: como acompanhar".
---

# Medir resultado

> O plano de mensuração deve ser feito **antes** do lançamento: ele define o que medir e por quê, e só então vem a implementação `[pós: M4]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:** o plano de mensuração, os eventos, a leitura do resultado, o fechamento das hipóteses e o registro do aprendizado.
- **Não é seu:**
  - **definir a métrica:** é da `strategy-hypotheses`. Você mede o que foi definido lá; se nada foi definido, faça **uma** pergunta;
  - **analisar o dado com rigor:** é da `research-evidence`, que você chama para a leitura;
  - **entregar o design:** é da `delivery-handoff`, que roda em paralelo com esta skill antes do lançamento.

## Antes do lançamento: plano de mensuração `[pós: M4]` `[artigo: Métricas Boss]`
Monte com `references/plano-de-medicao.md`:
1. **Definir:** objetivos e KPIs, vindos da `strategy-hypotheses`.
2. **Documentar:** tipo de produto, como ele funciona e o que acontece quando o usuário interage.
3. **Planejar:**
   - quais métricas e dimensões importam?
   - quais relatórios respondem aos objetivos?
   - quais configurações são necessárias?
4. **Implementar** com dev e analytics.
5. **Testar e refinar** o tracking.

**Regras:**
- **Não meça tudo.** Medir demais gera *data obesity* `[artigo: Métricas Boss]`.
- **Toda hipótese aberta precisa de um evento ou de uma fonte de medição.** A linha de base fica registrada com a fonte antes do lançamento `[prática]`.
- **Combine a medição com a estratégia de lançamento** escolhida (todos, faseado, piloto, flag). Defina o que observar em cada etapa e o sinal para avançar ou recuar `[prática]`.

## Depois do lançamento: ler o resultado `[artigo: NN/g – Formative vs. Summative]` `[artigo: Netflix]`
1. **Na data marcada**, compare o antes e o depois com a `research-evidence`: período equivalente, segmento e tracking.
2. **No A/B, use a significância definida antes.** "Nenhuma variante líder" quer dizer dados insuficientes `[pós: M4]`.
3. **Feche cada hipótese:**
   - **confirmada:** atingiu a meta, e a guarda não piorou;
   - **derrubada:** bateu o sinal "erramos se…";
   - **inconclusiva:** registre o motivo.
4. **Registre o aprendizado** no `projeto.md` e em `contexto/pesquisas.md`. Ele vira evidência da próxima demanda `[prática]`.

## Saída
```
| Hipótese | KPI | Evento(s) + propriedades | Linha de base (fonte) | Meta | Guarda | Leitura em | Quem lê |
H1: <antes → depois> [fonte: … · período] · Guarda: ok/piorou · confirmada | derrubada | inconclusiva · Aprendizado: <…>
```

## Referências
- `references/plano-de-medicao.md`, `references/fontes.md`
