---
name: ui-accessibility
description: Lente de acessibilidade, usada nas fases 4 a 6. Checa WCAG 2.2 nível AA (e a ABNT NBR 17225) em telas, fluxos e handoff — contraste de texto e não-texto, uso de cor (daltonismo), alvos de toque e zona do polegar, foco e teclado, rótulos e erros de formulário, leitores de tela, movimento, zoom e dark mode — e manda achados críticos para o topo. Use quando alguém disser "acessibilidade", "a11y", "WCAG", "ABNT 17225", "contraste", "leitor de tela", "inclusivo", "daltonismo", "tamanho de toque", "dark mode legível", e em toda revisão de tela.
---

# Acessibilidade

> **Pendente para o ambiente da empresa:** provavelmente conflita com a skill de acessibilidade do design system. Na integração, deixar as regras gerais (contraste, foco, semântica, texto alternativo) num lugar só e manter aqui apenas o que for específico, para não ter duas fontes da verdade.

> Acessibilidade não é só para pessoas com deficiência: é tornar a interface utilizável por mais pessoas, de diferentes níveis sociais e culturas — e um diferencial competitivo `[pós: M13]`. Não basta um leitor de tela se o conteúdo não for compreensível `[pós: M13]`.

**Origem:** `[pós: módulo]` material da pós · `[artigo: …]` texto referenciado pela pós · `[externo: WCAG 2.2]` critério oficial do W3C (consultado via Guia WCAG) · `[prática]` recomendação do pacote. Links em `references/fontes.md`.

## Território
- **É seu:** conformidade WCAG 2.2 AA / ABNT NBR 17225 e inclusão — percepção, operação, compreensão, robustez.
- **Não é seu:** usabilidade geral (`ui-heuristics`), escolha estética de cor e tipografia (`ui-craft` — você só verifica se a escolha é acessível), implementação de código (se houver skill de código como `better-accessibility`, delegue a ela).

## Regras
1. **Exclusão é CRÍTICO** `[prática]`: se alguém não consegue perceber, operar ou entender a tarefa principal, o achado vai para o topo do relatório — independentemente do resto.
2. **Meta padrão: nível AA** `[pós: M13]` `[prática]`. Níveis: **A** (mínimo), **AA** (intermediário, inclui A), **AAA** (mais alto, inclui A e AA). Se a empresa tiver exigência legal ou contratual diferente, siga `context-company`.
3. **Cor nunca sozinha** `[pós: M13]` `[externo: WCAG 2.2 – 1.4.1]`: ~8% dos homens e ~1% das mulheres têm daltonismo; erro só com borda vermelha some para quem tem protanopia → **ícone + mensagem em texto**.
4. **Ferramenta ajuda, olho decide** `[pós: M13]`: plugins de contraste (Able no Figma, Whocanuse, Color Review) dão o número, mas "nem sempre o que parece bom para o plugin é bom de verdade" — siga observando e ajustando.
5. **Acessibilidade é de todos** `[artigo: Guia WCAG]`: cada critério tem uma área primária (UI, UX, conteúdo, desenvolvimento), mas a responsabilidade quase sempre é compartilhada. Diga em cada achado **quem** corrige.

## Os 4 princípios (POUR) `[pós: M13]`
**Perceptível** (a informação não pode ser invisível em nenhum aspecto) · **Operável** (toda ação operável por qualquer usuário) · **Compreensível** · **Robusto**.

## Valores exatos para checar `[externo: WCAG 2.2]` `[pós: M13]`
| O quê | Mínimo AA | Critério |
|---|---|---|
| Contraste de texto normal | **4.5:1** | 1.4.3 |
| Contraste de texto grande (≥ 24px, ou ≥ 18,66px em negrito) | **3:1** | 1.4.3 |
| Contraste de elementos não-texto (bordas de input, ícones de ação, foco, gráficos) | **3:1** | 1.4.11 |
| Alvo de toque/clique | **24×24 px** (ou espaçamento equivalente) | 2.5.8 |
| Zoom de texto sem perda | **200%** | 1.4.4 |
| Realinhar (sem rolagem horizontal) | largura de **320 px** CSS | 1.4.10 |
| Dark mode: fundo × texto branco | fundo escuro o bastante para **≥ 15,8:1**, garantindo **4.5:1** na superfície mais elevada (24dp) | `[pós: M13]` via Material |

Recomendação `[prática]`: para alvos principais em mobile, mire em 44×44 px e na **zona do polegar** `[pós: M13]` (ações principais ao alcance do polegar, como faz o Uber).

## Fluxo
1. Identifique a tarefa principal e os estados (padrão, foco, erro, desabilitado, carregando, dark mode) `[prática]`.
2. Rode `references/checklist.md` por componente presente na tela.
3. Para cada falha: critério WCAG + nível + item ABNT quando souber + quem corrige.
4. O que não dá para verificar em imagem estática (ordem de foco, leitor de tela, teclado) → liste como **Não verificado** e diga como testar.

## Saída
```
| Severidade | Onde | Problema | Critério (nível) | Recomendação | Quem corrige | Como verificar |
| CRÍTICO | Formulário › CPF | Erro indicado só pela borda vermelha | 1.4.1 Uso de cores (A); 3.3.1 Identificação do erro (A) | Ícone + texto "CPF incompleto: faltam 2 dígitos" junto ao campo | UI + conteúdo | simulador de protanopia; leitor de tela anuncia o erro |
Não verificado: <ordem de foco, leitor de tela, teclado> → como testar: <…>
```

## Referências
- `references/checklist.md` — por componente, com critério e nível
- `references/fontes.md`
