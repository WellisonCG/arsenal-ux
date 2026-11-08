---
name: ui-heuristics
description: Lente de avaliação, usada nas fases 4 e 5. Faz avaliação heurística de telas e fluxos com as 10 heurísticas de Nielsen, as 20 Leis de UX, Gestalt, hierarquia visual, atenção, memória, familiaridade e efeito estético, e devolve achados priorizados com trade-off e "como medir". Use quando alguém disser "revisa essa tela", "avaliação heurística", "Nielsen", "leis de UX", "tá bom?", "o que melhorar", "usabilidade", "critica esse layout", "Gestalt", "hierarquia visual", "carga cognitiva".
---

# Heurísticas

> As heurísticas são regras gerais, não diretrizes específicas `[artigo: NN/g – 10 Usability Heuristics]`. Elas aumentam a chance de uma boa experiência, mas não a garantem `[pós: M13]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós, `[prática]` é recomendação do pacote e `[externo]` é fonte de fora da pós. Os links estão em `references/fontes.md`.

## Território
- **É seu:** usabilidade avaliada por especialista. Inclui Nielsen, Leis de UX, Gestalt e hierarquia visual, encontrabilidade e descobribilidade, atenção, memória, familiaridade, efeito estético e a escolha entre padrão e inovação.
- **Não é seu:**
  - WCAG, contraste e foco (`ui-accessibility`);
  - vieses aplicados e dark patterns (`behavioral-design`; as leis com nome de viés, como pico-fim e Zeigarnik, aparecem aqui só como usabilidade e a checagem ética fica lá);
  - teste com usuário (`research-studies`);
  - cor, tipografia e componentes como ofício (`ui-craft`).
- **Avaliação heurística não substitui teste com usuário** `[artigo: NN/g – You Are Not the User]`. Ela acha problemas prováveis; o teste confirma.

## Princípios da revisão
1. **Contexto antes de regra** `[prática]`. Pergunte uma vez, se não estiver claro, qual tarefa a tela atende e para quem. Uma tela administrativa usada todo dia aguenta densidade que um checkout não aguenta `[pós: M13]`.
2. **Trade-off é válido** `[pós: M13]`. O botão de apagar do Spotify é verde, a cor da marca, em vez de vermelho. Isso fere a heurística 2, mas foi uma decisão de negócio. Aponte o risco, sugira como reduzi-lo e não trate como erro automático (C7).
3. **O DS da empresa vence** `[prática]`. Uma convenção deliberada do design system é preferência, não achado. O mesmo detalhe feito de dois jeitos dentro do produto, sim, é achado (heurística 4).
4. **Padrão antes de inovação** `[pós: M13]`. Inove só quando a inovação ajudar a tarefa a ficar mais fácil ou rápida. Inovar só pelo visual (neomorfismo, por exemplo, em que sombras se confundem com botões) prejudica o reconhecimento. "Os usuários passam a maior parte do tempo em outros sites" (Lei de Jakob).
5. **Bonito não é usável** `[pós: M13]`. O efeito estético faz usuários tolerarem pequenos problemas e pode **mascarar** problemas no teste. Não deixe a estética esconder um achado.

## Fluxo
1. **Entender a tarefa principal** da tela e o perfil de quem usa `[prática]`.
2. **Percorrer o fluxo** como o usuário, estado por estado: vazio, carregando, erro, sucesso, primeira vez, recorrente `[prática]`.
3. **Aplicar as lentes, nesta ordem** `[prática]`:
   1. **As 10 heurísticas de Nielsen**, com sinais e correções em `references/nielsen.md`.
   2. **Percepção e hierarquia**: Gestalt, contraste, tamanho, posição, espaço em branco, encontrabilidade, descobribilidade e cegueira à mudança. Veja `references/percepcao-e-memoria.md`.
   3. **Carga cognitiva e memória**: reconhecimento em vez de memorização, Hick, Miller, familiaridade, curva de aprendizado em redesign.
   4. **Leis de UX** que se apliquem, em `references/leis-de-ux.md`. Use só as que explicam um achado; não liste as 20.
4. **Registrar cada achado** no formato abaixo, com severidade, trade-off e "como medir".
5. **Consolidar**: um achado por causa raiz, com todos os lugares onde aparece. O mais severo vem primeiro.
6. **Dizer o que não foi verificado** (por exemplo: "estado de erro não estava no protótipo").

## Severidade `[prática]`
| Nível | Quando | Equivalente na escala de Nielsen (0–4) `[externo]` |
|---|---|---|
| **CRÍTICO** | impede a tarefa, causa perda de dados ou dinheiro, ou não tem saída | 4 (catástrofe) |
| **ALTO** | atrapalha muito a tarefa principal ou gera erro frequente | 3 (grave) |
| **MÉDIO** | atrito evitável, inconsistência visível | 2 (menor) |
| **BAIXO** | refinamento | 1 (cosmético) |

Para graduar, considere três coisas: **frequência** (quantos encontram o problema), **impacto** (quanto atrapalha) e **persistência** (se o problema se repete toda vez) `[externo]`.

## Saída
```
Tela/fluxo: <…> · Tarefa principal: <…> · Público: <…>

| Severidade | Onde | Problema | Recomendação | Princípio | Trade-off | Como medir |
| ALTO | Checkout › etapa 2 | Não mostra em que etapa está nem quantas faltam | Indicador "2 de 4" | H1 Visibilidade do estado; Efeito do objetivo gradiente | — | taxa de saída da etapa 2; teste: "quantas etapas faltam?" |

Não verificado: <estados ausentes, fluxos não vistos>
Recomendação de teste: <o que só um teste com usuário confirma → pesquisar>
```

A coluna "Como medir" diz que dado ou teste confirmaria o problema e qual métrica deve melhorar com a correção. É ela que liga a heurística aos dados.

## Referências
- `references/nielsen.md`: as 10 heurísticas, com sinais de violação, correções e exemplos
- `references/leis-de-ux.md`: as 20 leis e o que fazer com cada uma
- `references/percepcao-e-memoria.md`: Gestalt, hierarquia, atenção, memória, familiaridade, estética
- `references/fontes.md`
