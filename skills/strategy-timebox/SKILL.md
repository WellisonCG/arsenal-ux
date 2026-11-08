---
name: strategy-timebox
description: Skill transversal, chamada logo depois de entender a demanda e sempre que o prazo mudar. Pergunta quanto tempo real existe, classifica o projeto (problema claro ou obscuro × solução conhecida ou nova), propõe com o designer como dividir o prazo, define quais métodos de pesquisa e validação cabem nesse tempo, marca os checkpoints e diz o que cortar se apertar. Use quando alguém disser "tenho 3 dias", "tenho uma semana", "quanto tempo leva", "cronograma", "timebox", "prazo", "onde gasto mais tempo", "dá tempo de pesquisar?", "sprint", "o prazo mudou".
---

# Planejar timebox

> Não existe fórmula mágica para o tempo de descoberta, por isso o timebox forçado: ele obriga a priorizar e evita que o trabalho se perca no tempo `[pós: M1]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Papel
É uma **restrição que alimenta as outras skills**, não uma fase isolada. O prazo muda a percepção de tudo: que método de pesquisa cabe, como validar a hipótese, quanto explorar.

- **Quando entra:** logo depois de `strategy-framing`, perguntando o prazo.
- **Quando volta:** só quando o prazo muda ou uma fase estoura o previsto, para replanejar.
- **Quem consulta:** `research-studies`, `strategy-hypotheses` e `ui-craft` olham este limite antes de propor qualquer coisa.

## Território
- **É seu:** o prazo real, o perfil do projeto, a divisão do tempo, o que cabe em cada fase, os checkpoints e o plano de corte.
- **Não é seu:** o método em si (`research-studies`) e o conteúdo de cada fase (as skills donas).

## O que a realidade mostra `[artigo: NN/g – How Well Discovery Phases Are Performed]`
- **58% dos discoveries duram até 2 semanas.**
- **O principal motivo para pular o discovery é a pressão por entregar.**

Esta skill não briga com o prazo: aceita o que existe e deixa explícito o que ficou sem saber.

## Fluxo

### 1. Perguntar o prazo, cedo `[prática]`
Pergunte em 1 ou 2 frases:
- "Para quando é a entrega, e é handoff ou lançamento?"
- "Quanto tempo real de dedicação temos?"
- "Tem marco no meio, como uma review com stakeholder?"

### 2. Classificar o perfil `[pós: M1]` `[prática]`
**O problema está claro?** Pesam a extensão do problema, o quanto já sabemos e o escopo `[pós: M1]`.
**A solução já é conhecida?** Já existe padrão no design system, no mercado ou no próprio produto?

| Perfil | Onde está o risco | O tempo vai para |
|---|---|---|
| **Executar** (claro · conhecida) | execução e detalhe | criar e entregar |
| **Explorar visual** (claro · nova) | usabilidade da solução nova | criar e validar |
| **Investigar** (obscuro · conhecida) | resolver o problema errado | investigar |
| **Descobrir** (obscuro · nova) | os dois | investigar e validar cedo |

Considere também o risco dominante que a `strategy-hypotheses` aponta (valor, usabilidade, viabilidade, negócio, ética) `[artigo: PM3 – Dual Track]`.

### 3. Propor a divisão do tempo, negociada `[prática]`
A tabela abaixo é **ponto de partida para conversar**, não regra. Proponha, explique em uma linha e ajuste com o designer.

| Perfil | Entender | Investigar | Definir | Criar | Validar | Entregar |
|---|---|---|---|---|---|---|
| Executar | 5% | 5% | 5% | 55% | 15% | 15% |
| Explorar visual | 5% | 10% | 5% | 45% | 25% | 10% |
| Investigar | 15% | 35% | 10% | 20% | 10% | 10% |
| Descobrir | 10% | 25% | 10% | 25% | 20% | 10% |

### 4. Dizer o que cabe no prazo `[prática]`
| Prazo | Pesquisa e validação que cabem |
|---|---|
| **Horas a 2 dias** | dados existentes, benchmark rápido, revisão heurística, guerrilha, lançar pequeno e medir |
| **1 semana** | os anteriores + teste não moderado ou 3 a 5 conversas rápidas, piloto |
| **2 semanas ou mais** | entrevistas, teste moderado, rollout faseado com leitura de métricas |

Repasse este limite à `research-studies` e à `strategy-hypotheses`.

### 5. Fidelidade padrão: alta, com o design system `[prática, a partir do usuário]`
Com design system e IA, a alta fidelidade sai rápido e já com a cara do produto, então **parta dela**. Baixa e média fidelidade ficam como exceção, para quando:
- o problema ainda precisa ser explorado; ou
- o visual está atrapalhando a decisão, e convém tirar a carga cognitiva para focar em fluxo e palavras.

### 6. Checkpoints `[prática]`
| Prazo | Checkpoints |
|---|---|
| Até 3 dias | 1: proposta em hi-fi com o stakeholder |
| 1 semana | 2: proposta com o stakeholder + validação com usuário ou piloto |
| 3 semanas | 3 a 4: enquadramento, proposta, validação, revisão com o dev |

**Leve o dev cedo.** "Se a primeira vez que seus desenvolvedores veem uma ideia é no planejamento de sprint, você falhou" (Marty Cagan) `[artigo: PM3 – Dual Track]` `[pós: M8]`.

### 7. Pesquisar antes ou lançar e medir? `[pós: M8]` `[artigo: SVPG]` `[prática]`
| Prefira lançar pequeno e medir quando | Prefira pesquisar antes quando |
|---|---|
| a mudança é reversível (flag, rollout por segmento) | errar é caro (dinheiro, dados, confiança, regulação) |
| o custo de errar é baixo | a mudança é difícil de desfazer |
| existe tráfego para ler o resultado | não há como medir depois |
| o prazo não cabe uma rodada de pesquisa | o risco dominante é valor ou viabilidade |

No Lean UX, colocar algo no ar também é pesquisa `[pós: M8]`. Registre a escolha em "Decisões".

### 8. Encaixar no ritmo do time `[pós: M8]` `[artigo: PM3]` `[artigo: Gothelf]` `[artigo: Caliari]`
- **Dual track:** discovery e delivery correm em paralelo. O design faz o discovery da próxima demanda enquanto a engenharia constrói a atual.
- **Triple track:** uma trilha contínua de pesquisa sobre o problema, fora das demandas, deixa a fase 2 adiantada. Se o time não tem, sugira uma vez.

### 9. Plano de corte `[prática]` `[pós: M7]`
Defina antes o que sai se o prazo apertar (`references/plano-de-corte.md`). Solução nova: corte escopo antes de cortar validação. Nunca corte a métrica nem o evento que a mede.

## Saída (curta)
```
Prazo: 5 dias úteis (handoff) · Perfil: Explorar visual · Risco: usabilidade
Divisão proposta: dia 1 entender/investigar/definir · dias 2–3 criar (hi-fi) · dia 4 validar · dia 5 entregar
Cabe: benchmark, revisão heurística, teste não moderado com 5 pessoas
Checkpoints: dia 2 com PM + tech lead · dia 4 com usuários
Se apertar: corta a 3ª variação, mantém a validação
```

## Referências
- `references/cronogramas.md`, `references/plano-de-corte.md`, `references/fontes.md`
