---
name: strategy-hypotheses
description: Fase 3 do processo de design. Transforma palpites e pedidos de feature em hipóteses testáveis, com métrica, linha de base e sinal de que estamos errados. Liga objetivo, KPI e estratégia, separa macro de micro conversão, define métrica de guarda, identifica o tipo de risco (valor, usabilidade, viabilidade técnica, viabilidade de negócio, ética) e prioriza. Use quando alguém disser "acho que é X", "minha hipótese", "como vamos medir", "métrica de sucesso", "KPI", "OKR", "o que priorizar", "o que testar primeiro", "como sei que deu certo", "teste A/B".
---

# Definir hipóteses

> Ao receber um briefing há uma certeza do que deve ser feito. Quando se trabalha com uma hipótese, você assume um risco e precisa provar se está certo `[pós: M8]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:** hipóteses, objetivo, KPI, métrica de guarda, linha de base, tipo de risco, priorização.
- **Não é seu:**
  - buscar a linha de base (`research-evidence` busca; você usa);
  - distribuir o prazo (`strategy-timebox`);
  - instrumentar e medir depois do lançamento (`delivery-metrics`).

## Fluxo

### 1. Do entregável ao resultado `[pós: M8]` `[artigo: PM3 – Continuous Discovery]`
Se a demanda é uma feature, reescreva como resultado:
- **Antes:** "Fazer uma central de notificações."
- **Depois:** "Aumentar a conversão de X fazendo o usuário ver as notificações sobre Y."

O time passa a responder pelo **resultado** (*outcome*), não pelo entregável (*output*). Trate tudo como experimento: "certeza" é uma palavra perigosa no discovery.

### 2. Ligar objetivo, KPI e estratégia `[pós: M4]`
| Conceito | O que é | Exemplo |
|---|---|---|
| **Objetivo** | o que queremos conquistar. Sem objetivo não há o que medir | Aumentar as aberturas de chamado pelo site |
| **Métrica** | tudo o que pode ser medido | sessões, cliques, tempo, saídas |
| **KPI** | a métrica que melhor diz se o objetivo está sendo atingido | taxa de conclusão da abertura de chamado |
| **Estratégia** | o que faremos para atingir o objetivo | simplificar as etapas e usar a linguagem do usuário |

Separe a **macro conversão**, que é o objetivo principal, das **micro conversões**, que são os passos até lá `[pós: M4]`.

### 3. Escrever as hipóteses
Use este formato. A estrutura vem do Lean UX `[pós: M8]`; os campos de linha de base, sinal de erro e guarda são `[prática]`:

> Acreditamos que **[mudança]** para **[público]** vai gerar **[efeito]**.
> Saberemos que funcionou quando **[KPI]** passar de **[linha de base + fonte]** para **[meta]** em **[prazo]**.
> Estaremos errados se **[sinal]**.
> Sem piorar: **[métrica de guarda]**.

Regras `[prática]`:
- **Linha de base tem fonte.** Se não houver, peça a `research-evidence` ou marque como "a medir antes do lançamento".
- **"Estaremos errados se…" é obrigatório.** Uma hipótese que não pode ser derrubada não é hipótese.
- **Métrica de guarda** é o que não pode piorar: suporte, cancelamento, tempo de tarefa, erros, receita.
- **Uma hipótese, uma mudança.** Se a mudança é um pacote, diga que não será possível saber qual parte funcionou.
- **Meta realista.** Use a meta do time (`contexto/produto.md`) ou proponha uma faixa e diga que é estimativa. Toda ação precisa de meta, porque sem meta qualquer número parece bom `[pós: M4]`.

Veja `references/metricas.md` para escolher o KPI.

### 4. Identificar o tipo de risco `[artigo: PM3 – Dual Track]` `[artigo: SVPG – Product Validation]`
Cada hipótese aposta contra um tipo de risco. Marty Cagan lista cinco:

| Risco | Pergunta | Quem ajuda | Como reduzir |
|---|---|---|---|
| **Valor** | O cliente vai comprar ou usar? | usuário, PM | entrevista, protótipo, teste de demanda |
| **Usabilidade** | O usuário consegue entender e usar? | designer, usuário | teste de usabilidade com protótipo |
| **Viabilidade técnica** | Conseguimos construir isso? | dev e tech lead | conversa técnica ou prova de conceito, **cedo** |
| **Viabilidade de negócio** | Funciona para o negócio (financeiro, jurídico, vendas, marca)? | stakeholders | entrevista com stakeholder |
| **Ética** | Devemos construir isso? | time + `behavioral-design` | checagem ética e de dark patterns |

A SVPG alerta para um erro comum: confiar demais na especificação e deixar o ajuste para depois do beta, quando mudanças grandes já são caras. Valide valor, usabilidade e viabilidade **antes** de entregar para construção.

### 5. Priorizar `[prática]`
- Pontue cada hipótese de 1 a 3 em **impacto**, **confiança** (quanta evidência existe) e **esforço**. Veja `references/priorizacao.md`.
- Comece pela de **maior impacto com menor confiança**: é a suposição mais arriscada. Testá-la cedo segue a lógica do discovery, que é atacar os riscos importantes o mais cedo possível `[artigo: PM3 – Dual Track]`.

### 6. Checar o próprio viés `[pós: M1, M12]` `[artigo: NN/g – You Are Not the User]`
Antes de fechar, pergunte ao time (com `behavioral-design`):
- **Confirmação:** estamos buscando só o que confirma a ideia de quem pediu?
- **Falso consenso:** estamos supondo que o usuário pensa como nós?
- **Sobrevivente:** a hipótese considera quem já saiu?

### 7. Confiança baixa: seguir, assumir ou reduzir o risco?
A confiança também decide **se vale seguir**, não só como testar. Com uma hipótese de baixa confiança, há três caminhos `[prática]`:

1. **Descartar ou adiar**, quando não faz sentido seguir agora.
2. **Assumir o risco conscientemente**, registrando a decisão e o motivo no `projeto.md`.
3. **Montar uma estratégia para reduzir o risco** até conseguir medir com confiança. Exemplos: piloto com um cliente, rollout faseado, feature flag, protótipo com usuários.

**Quem decide é o designer.** Você apresenta os três caminhos com prós e contras e uma recomendação, e monta a estratégia junto com ele.

### 8. Escolher como testar
Para cada hipótese, aponte a forma mais barata de testar dentro do prazo e passe para `strategy-timebox` e `research-studies` `[prática]`:

| Confiança atual | Como testar |
|---|---|
| Baixa, com mudança grande | se o designer decidir seguir: piloto ou rollout faseado com métrica e capacidade de recuar; teste com usuários quando errar for caro |
| Média | lançar para um segmento pequeno, ou teste rápido |
| Alta, com mudança pequena e reversível | lançar para todos e medir; A/B se houver tráfego |

Com IA, construir custa menos. Prefira execução controlada (flag, liberação gradual, métrica, recuo) a uma validação prévia longa, a menos que o erro seja caro ou irreversível `[prática, a partir do usuário]`.

**Sobre o A/B:**
- Ele é o único teste que mostra **causa** `[pós: M4]`.
- **Exige tráfego e tempo.** Sem os dois, combine teste qualitativo com medição antes e depois e diga que a leitura é mais fraca `[prática]`.
- **Pode errar nos dois sentidos** `[artigo: Netflix – Interpreting A/B Test Results]`:
  - **Falso positivo:** o teste mostra diferença que não existe. Por convenção, aceita-se 5% de chance, o "nível de significância de 5%".
  - **Falso negativo:** o teste não mostra uma diferença que existe.
  - Reduzir um aumenta o outro.
- **Defina antes de rodar:** a métrica de decisão, a significância e o tamanho de amostra.
- **"Nenhuma variante líder" é um resultado válido** `[pós: M4]`. Significa dados insuficientes, e não que a original ganhou.

## Saída
Preencha a seção 3 do `projeto.md`:

```
Objetivo: <…> · KPI: <…> · Guarda: <…>
| # | Hipótese | Risco | KPI | Linha de base (fonte) | Meta | Erramos se… | I/C/E | Teste | Status |
| H1 | Acreditamos que … | usabilidade | conclusão etapa 3 | 38% [fonte: Analytics › campaign_step · ago–out] | 48% | não subir ≥ 10 p.p. em 30 dias | 3/1/2 | protótipo + 6 marcas | aberta |
```

## Referências
- `references/metricas.md`: como escolher KPI, macro e micro, guarda, HEART
- `references/priorizacao.md`: matriz impacto × confiança × esforço
- `references/fontes.md`: material da pós e artigos lidos para esta skill
