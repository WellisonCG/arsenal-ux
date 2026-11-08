---
name: strategy-framing
description: Fase 1 do processo de design. Transforma um pedido em problema bem definido, com perguntas socráticas, separação entre problema e solução pedida (solutioneering), stakeholders, mapa de certezas, problem statement, objetivo de discovery, prazo e restrições. Use quando chegar uma demanda nova, um pedido vago ou um pedido que já vem com a solução ("faz uma tela de X", "redesenha o onboarding", "o chefe quer uma central de notificações"), ou quando alguém disser "por onde começo", "briefing", "kickoff", "entender o problema", "problem statement", "entrevista com stakeholder", "JTBD", "inception".
---

# Entender a demanda

> "A descoberta não é sobre explorar um problema, é sobre tomar uma decisão sobre o que fazer a seguir." (Pete Herlihy, citado por Will Myddelton) `[pós: M1]` `[artigo: Myddelton]`

**Origem do conteúdo.** Cada bloco indica de onde veio: `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote, sem fonte específica. Os links estão em `references/fontes.md`.

## Território
- **É seu:** separar o problema da solução pedida, perguntas de enquadramento, stakeholders, mapa de certezas, problem statement, objetivo de discovery, prazo e restrições.
- **Não é seu:** buscar dados (`research-evidence`), hipóteses e métrica (`strategy-hypotheses`), distribuir o prazo (`strategy-timebox`), entrevistar usuários (`research-studies`). Entrevista com **stakeholder** é sua; com **usuário** é da `research-studies`.

## Modo de trabalho: você monta, o designer valida
Não peça ao designer para preencher problem statement, mapa de certezas, matriz CSD ou impacto × esforço. Você coleta, monta um rascunho e ele confirma, corrige ou completa.

1. **Peça as fontes, não as respostas.** Pergunte curto onde está o contexto:
   - threads e canais do Slack;
   - transcrições de reunião;
   - a origem da demanda: Pendo, feedbacks, NPS, pedidos de churn, pedido da marca ou do cliente;
   - tickets e dados que já existam.
2. **Leia tudo o que vier** e, com `context-company`, busque o que for acessível sem pedir.
3. **Devolva um rascunho preenchido** com o problem statement, o mapa de certezas e o objetivo de discovery, cada afirmação com a sua fonte.
4. **Marque as lacunas** onde faltar evidência e peça o material específico que as resolveria ("tem a gravação da call com a marca X?").
5. **Pergunte só o que não dá para descobrir**, priorizando o que mais muda a resposta. Não há limite fixo de perguntas: algumas demandas pedem mais. Prefira ir em etapas, conforme as respostas chegam, a mandar um questionário longo.
6. **Feche a fase perguntando o prazo.** É o gatilho do `strategy-timebox`.

Os passos do fluxo abaixo descrevem **o que você monta**, não o que o designer preenche.

## Quando precisa de discovery `[artigo: NN/g – Discovery: Definition]`
Precisa quando há **muitas incógnitas** que travam o time, ou quando **o time não está alinhado** sobre o que quer alcançar. Seguir só com suposições arrisca resolver um problema que não importa. Se a demanda é pequena, conhecida e alinhada, esta fase cabe em poucas perguntas.

## Fluxo

### 1. Detectar solutioneering `[pós: M1]` `[pós: M8]`
*Solutioneering* é chegar com a solução antes de entender a causa do problema. Sinais `[prática]`:
- o pedido tem um substantivo de interface: "tela", "botão", "central", "modal", "dashboard";
- o pedido é um verbo de execução: "faz", "coloca", "redesenha";
- não há nenhum "porque" no pedido.

Se aparecer algum sinal, **não recuse**. Reescreva o pedido como problema e pergunte o que motivou:

> Pedido: "Precisamos de uma central de notificações."
> Reescrita: "Que resultado esperamos com ela? Que problema o usuário tem hoje por não ter onde ver as notificações?"

O Lean UX troca o **entregável** por **resultado** (M8). Resultado vale mais que feature entregue: *outcomes* em vez de *outputs* `[artigo: PM3 – Continuous Discovery]`.

### 2. Perguntar o que falta `[pós: M1]` `[artigo: NN/g – Problem Statements]`
Use o 5W1H como checklist **interno**, não como questionário. Pergunte só o que estiver faltando, no máximo 5 perguntas, começando pelas que mais mudam a resposta `[prática]`:

| Ordem | Pergunta | Por que vem primeiro |
|---|---|---|
| 1 | **Por que** isso importa agora? Qual resultado de negócio ou do usuário está em jogo? | Define se é para fazer e qual métrica medir |
| 2 | **Quem** é afetado? Todos ou um segmento? Algum time interno, como o suporte? | Muda o recorte de dados e o recrutamento |
| 3 | **O quê** acontece hoje, e como sabemos? | Separa fato de percepção e alimenta a fase 2 |
| 4 | **Quando e onde** acontece? Em qual etapa, plataforma ou momento? | Localiza o problema na jornada |
| 5 | **Qual o prazo** e o que acontece se não resolvermos? | Alimenta o `strategy-timebox` |
| + | Já tentaram resolver antes? O que aconteceu? | Evita repetir erro (Guia de Stakeholders) |

Se a resposta vier vaga, aprofunde com uma *probing question* (veja `references/banco-de-perguntas.md`).

### 3. Mapear stakeholders `[pós: Guia de Entrevistas com Stakeholders]`
- Liste quem **decide**, quem é **afetado** e quem **sabe** (dados, suporte, vendas) `[prática]`.
- Para cada um que ainda não foi ouvido, proponha um papo 1:1 de 30 minutos com o roteiro de `references/entrevista-stakeholders.md`.
- O roteiro busca três coisas:
  1. objetivos de negócio e métricas;
  2. dados e insights que eles já têm;
  3. soluções tentadas e as limitações delas.
- Envolva **PM, design e engenharia** desde já. Um problema comum de discovery é não ter as pessoas certas no time, e quem não participa tende a pular direto para soluções `[artigo: NN/g – How Well Discovery Phases Are Performed]`.

### 4. Separar o que sabemos do que achamos `[artigo: Myddelton]`
Antes de escrever o problema, organize o que surgiu nas conversas. Pode ser num workshop curto de inception, de 60 a 90 minutos com o time, ou sozinho a partir das respostas. Use estas categorias:

| Categoria | O que entra | Para onde vai |
|---|---|---|
| **Objetivos** | o que queremos alcançar | objetivo de discovery |
| **Achismos** ("reckons") | o que **achamos** que já sabemos | fase 2: verificar com dado. Se não houver dado, vira hipótese |
| **A descobrir** | o que gostaríamos de saber | perguntas da fase 2 |
| **Armadilhas** ("rabbit holes") | o que consumiria muito tempo sem ajudar a decidir | fora do escopo, registrado |
| **Escopo / Isso não é** | o que faremos e o que parece relacionado mas não é | seção 1 do `projeto.md` |
| **Para depois** | ideias de solução que surgiram | guardadas para a fase 4 |

Essa separação é o antídoto do **falso consenso**: achar que o usuário pensa como nós `[artigo: NN/g – You Are Not the User]`. Todo achismo é tratado como hipótese até ter evidência.

### 5. Escrever o problem statement e o objetivo de discovery `[pós: M1]` `[artigo: NN/g – Problem Statements]`
- Use o modelo de `references/problem-statement.md`: no máximo 5 frases e **sem solução**. Ele tem três partes:
  1. **contexto** do problema;
  2. **pessoas afetadas** e como são afetadas (inclusive times internos, como o suporte);
  3. **impacto para a organização**, quantificado se possível.
- O problema pode ser uma **oportunidade**: a distância entre o estado atual e o desejado.
- Transforme o problema em **objetivo de discovery**, a decisão que esta demanda precisa tomar: "Decidir como vamos ajudar X a fazer Y" `[artigo: Myddelton]`. Desdobre em 2 a 4 perguntas para a fase 2.
- Evite as duas armadilhas (M1):
  - **Amplo demais**, como "melhorar a experiência".
  - **Prescritivo demais**, como "o formulário precisa ter menos campos".
- Um resultado legítimo do discovery é **decidir não seguir**, por exemplo quando não há necessidade real do usuário `[artigo: NN/g – Discovery: Definition]`.

### 6. Avaliar a clareza para o timebox `[pós: M1]`
Classifique e passe para o `strategy-timebox`:
- **Problema claro:** sabemos quem, onde e por quê, com evidência.
- **Problema obscuro:** falta pelo menos um desses três, ou só temos achismos.

Os fatores que pesam são três: **extensão do problema** (quantas pessoas, causas e serviços), **quanto já sabemos** e **escopo**. Uma oportunidade nova leva mais tempo que uma melhoria.

## Postura
- **Foque na causa, não no sintoma** `[pós: M1]`. "O usuário não clica no botão" é sintoma. Pergunte por quê.
- **Problema de usuário vem antes de problema de equipe** `[pós: M1]`.
- **Não seja rígido com o processo** `[pós: M1]`. Se a demanda é pequena e clara, 2 perguntas bastam.
- **Você não é o usuário** `[artigo: NN/g – You Are Not the User]`. Nem você, nem o stakeholder, nem os colegas. Na dúvida, investigue em vez de "validar".
- **JTBD quando o "porquê" for nebuloso** `[pós: M1]`. Pergunte qual progresso a pessoa tenta fazer, em que circunstância, e considere as dimensões funcional, social e emocional.

## Saída
Preencha a seção 1 do `projeto.md`:

```
Pedido original: <como chegou>
Problema: <statement, até 5 frases: contexto · afetados · impacto>
Objetivo de discovery: Decidir <...>
Perguntas para a fase 2: 1) … 2) … 3) …
Achismos a verificar: <lista>
Fora do escopo: <armadilhas e "isso não é">
Para quem: <segmentos>
Stakeholders: <decide · afetado · sabe>
Prazo e restrições: <…>
Clareza: claro | obscuro (motivo)
```

## Referências
- `references/banco-de-perguntas.md`: perguntas por tipo de demanda, probing questions, JTBD
- `references/entrevista-stakeholders.md`: roteiro de 30 minutos
- `references/problem-statement.md`: modelo, exemplos e checagem
- `references/fontes.md`: material da pós e artigos lidos para esta skill
