---
name: research-synthesis
description: Especialista em síntese e mapeamento, chamado em qualquer fase. Transforma material bruto (entrevistas, testes, tickets, reviews, transcrições, dados de benchmark) em insights e artefatos de síntese: debriefing, codificação, mapa de afinidade, mapa de empatia, jornada do usuário, service blueprint, personas, JTBD e matriz CSD. Escolhe o artefato que responde à pergunta com o menor esforço. Use quando alguém disser "sintetizar", "o que as entrevistas disseram", "insights", "mapa de afinidade", "mapa de empatia", "jornada", "service blueprint", "persona", "organizar o que descobrimos".
---

# Sintetizar

> O insight é o contraste entre o que imaginávamos nas hipóteses e o que encontramos `[pós: M3]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Para métodos que não estão aqui, busque nas fontes de `uxpert/references/fontes-confiaveis.md` (NN/g como principal).

## Território
- **É seu:** dar sentido ao material coletado e escolher o artefato de síntese.
- **Não é seu:**
  - coletar com usuários (`research-studies`);
  - buscar dados existentes (`research-evidence`);
  - transformar o resultado em hipóteses (`strategy-hypotheses`, que recebe os seus insights).

## Fluxo
1. **Juntar o material** com a origem de cada peça: sessão, ticket, transcrição, link.
2. **Debriefing logo após cada sessão** `[pós: M3]`, se for pesquisa própria: de 30 a 60 minutos, informal, para alinhar e calibrar. Pode rodar em paralelo à `research-studies`, sessão a sessão.
3. **Escolher o artefato** pela pergunta, com o menor esforço `[prática]`:

| Pergunta | Artefato |
|---|---|
| Que temas aparecem no material? | **Mapa de afinidade** `[pós: M3]` |
| O que sabemos, o que supomos, o que falta saber? | **Matriz CSD** `[pós: ref. Disc. 09]` |
| O que o usuário diz, pensa, faz e sente? | **Mapa de empatia** |
| Onde a experiência quebra ao longo do tempo? | **Jornada do usuário** |
| O problema atravessa áreas, sistemas ou operações? | **Service blueprint** |
| Há segmentos com necessidades distintas? | **Personas ou proto-personas** |
| Que progresso a pessoa está tentando fazer? | **JTBD** `[pós: M1]` |

Antes de aplicar um método, confira o passo a passo nas fontes confiáveis.

4. **Codificar e agrupar** os trechos em temas e contar a frequência (x de n) `[pós: M3]`.
5. **Escrever os insights:** o que encontramos, como contrasta com a hipótese, e a evidência (citação, clipe, número).
6. **Números de teste pequeno** servem para comparar e provocar reflexão; não têm significância estatística `[pós: M2]`.
7. **Anonimizar** os participantes ("P1", "P2"), por causa da LGPD `[pós: M2]`.
8. **Entregar** no artefato do projeto e atualizar o `projeto.md` com as evidências marcadas como `[pesquisa]`.

## Saída
```
Material: <n sessões / n tickets / fontes>
Artefato: <qual e por quê>
Insights: 1) <achado> · contraste com H<n> · evidência <x/n, citação>
Severidade (se for usabilidade): <CRÍTICO/ALTO/MÉDIO/BAIXO>
Não respondido: <…>
```

## Referências
- `references/sintese.md`: debriefing, documentação, análise, classificação, apresentação
- `references/fontes.md`
