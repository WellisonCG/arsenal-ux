---
name: delivery-handoff
description: Especialista em entrega do design para o desenvolvimento. Confere se o design está pronto (definition of done), organiza estados, edge cases, consistência visual e comportamental, conteúdo e assets, faz o handoff com o time de dev e dá suporte durante a sprint. Use quando alguém disser "handoff", "tá pronto pro dev?", "entregar", "specs", "definition of done", "documentar para o dev". Roda em paralelo com a delivery-metrics antes do lançamento.
---

# Handoff

> **Pendente para o ambiente da empresa:** não mexer até integrar com a skill de handoff que o usuário já usa no trabalho. Ela separa a entrega por histórias e documenta os casos de uso para devs e designers. Na integração, decidir:
> - se o tracking entra como seção dentro dela (hoje está na `delivery-metrics`);
> - onde fica a checagem de estados (hoje está na `ui-craft`);
> - quais outras skills do trabalho se encaixam aqui.

**Origem do conteúdo:** `[pós: módulo]` é material da pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:** o pacote de entrega, o definition of done de design, o handoff com o dev e o suporte na sprint.
- **Não é seu:**
  - medição e eventos (`delivery-metrics`, em paralelo);
  - auditoria de acessibilidade (`ui-accessibility`);
  - texto final (`content-writing`).

## 1. Definition of done de design `[pós: M8]`
Combine com o time quando um incremento está pronto e transforme isso num checklist para o dev e o PM:
- passou por revisão de design?
- está de acordo com o layout?
- há pontas soltas no fluxo?

Para o discovery, confira também:
- resolve a dor do usuário?
- está alinhado ao OKR?
- atende às heurísticas?

## 2. Checklist do pacote
Use `references/checklist-handoff.md`. Ele cobre:
- **estados e edge cases** `[pós: M13]`; aqui você só confirma que existem, porque a `ui-craft` já os resolveu;
- **consistência visual e comportamental** `[pós: M9]`;
- **conteúdo** `[pós: M9]`;
- **acessibilidade**;
- **assets** `[pós: M13, M8]`.

## 3. Entregar e acompanhar `[pós: M13]` `[pós: M8]`
- **O handoff é feito com o time de dev,** no formato padrão da empresa (`context-company`).
- **Na sprint de delivery,** o designer:
  - dá suporte e resolve os casos de exceção descobertos no desenvolvimento;
  - ajusta quando algo não é viável;
  - escreve as mensagens de erro e de espera;
  - entrega os assets.

## Saída
```
DoD: ✓/✗ por item · Estados: confirmados / pendentes · A11y: ok / achados · Assets: <onde> · Suporte: <quem, canal>
```
