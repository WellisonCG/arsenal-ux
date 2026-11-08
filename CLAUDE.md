# Arsenal UX: contexto do projeto

Leia isto antes de mexer no pacote. Aqui está o que foi decidido, por quê, e o que falta fazer.

## O que é
Um pacote de skills de design para o Claude Code. O objetivo é **nivelar o time de design** no mesmo patamar de raciocínio que o dono do projeto usa com IA: dados, estratégia, pesquisa, vieses cognitivos, heurísticas, acessibilidade e UI.

O pacote foi construído de forma genérica, a partir do material de uma pós-graduação (MBA em Inovação Orientada à IA e UX), e agora vai ser **adaptado ao ambiente da empresa**: design system, skills que já existem lá e fontes de dados.

- **Condutor:** `uxpert` (trocadilho com expert). É o especialista que monta o time de skills certo para cada pedido e roda em paralelo as que são independentes.
- **16 skills**, no padrão `área-especialidade`, com nomes em inglês e conteúdo em português. A lista está no `README.md` e no `PLANO.md`, seção "Padrão de nomes".
- **Histórico completo:** `PLANO.md`, nas seções v1 a v5.

## Princípios do usuário (respeitar sempre)
1. **Processo fluido, não receita de bolo.** As fases são um mapa para se orientar. Os exemplos que o usuário dá são ilustrações, nunca regra.
2. **Especialista, não cartilha.** As skills têm contexto, várias ferramentas, e escolhem pelo caso real.
3. **Propositivo.** A skill coleta (Slack, transcrições, Pendo, NPS, churn), monta o material e o designer valida. Não pede para o designer preencher matrizes.
4. **Dado com fonte.** Busca sem esperar autorização, mas sempre diz de onde tirou cada dado.
5. **Fontes confiáveis, não só os MDs.** Os MDs são a base curada. Para ir além, a skill busca nas fontes de `skills/uxpert/references/fontes-confiaveis.md` (uma principal e 1 ou 2 de apoio), sempre com link. Nunca inventa.
6. **Sucinto.** Nada de textão no chat. A skill sugere, produz o entregável, e a revisão acontece no próprio entregável.
7. **Rápido na mão do usuário.** A estratégia de lançamento depende da demanda. Com IA, execução controlada no lugar de validação longa, quando o erro é reversível.
8. **Alta fidelidade com o DS é o padrão.** Baixa e média fidelidade são exceção.
9. **Skills pequenas e especialistas**, que o `uxpert` combina e roda em paralelo. Se uma skill faz papel demais, divida.
10. **O DS da empresa vence** o conteúdo genérico do pacote.

## Como o usuário gosta de trabalhar
- **Revisão:** num canvas de design (artefato do tipo Design), com uma prancha por assunto e comentários dentro dele.
- **Respostas:** ele **não lê as respostas nos comentários.** Depois que ele avisar que terminou de comentar, leia tudo, aplique as mudanças, marque os comentários como resolvidos e **resuma no chat** o que mudou e o que está pendente.
- **Enquanto ele comenta, não aja.** Espere o aviso.
- **Proposta sua** (não pedida por ele) deve aparecer marcada como tal, para ele revisar com mais atenção.

## Pendências para o ambiente da empresa ← começar por aqui
| Skill | O que fazer |
|---|---|
| `context-company` | Rodar no computador da empresa. Levantar o que as skills existentes já cobrem e deixar aqui só a ligação com elas, sem duplicar. Preencher `contexto/` (principalmente `fontes-de-dados.md` e `design-system.md`). |
| `delivery-handoff` | Integrar com a skill de handoff que o usuário já usa: ela separa por histórias e documenta casos de uso para devs e designers. Decidir se o tracking (hoje em `delivery-metrics`) entra nela. A checagem de estados fica na `ui-craft`. |
| `ui-accessibility` | Resolver o conflito com a skill de acessibilidade do DS: uma só fonte da verdade para as regras gerais. |
| `ui-craft` | Adaptar ao DS conectado, às skills de navegação na plataforma (acesso de teste) e ao arquivo de templates das telas principais. As regras visuais vêm do DS. |
| `content-writing` | Confirmar onde está o content design (tom de voz, regras), dentro do DS ou fora, e usar esse material como base. |
| `behavioral-design` | Ampliar o catálogo além dos cerca de 30 vieses do M12, com estudo e link de cada um. |
| todas | Cruzar com as skills que já existem na empresa: o que se sobrepõe, o que conflita, o que fica dentro do DS e o que fica fora. |

Depois disso: **testar com demandas reais** e ajustar.

## Artefatos (claude.ai, privados, da conta do usuário)
- **Canvas de revisão:** https://claude.ai/artifact/2W1ejZYmqhFbTmQLjTpxci
  - página "Revisão 1": a primeira revisão, com os nomes antigos;
  - página "Mudanças v3–v4": antes e agora, fontes confiáveis e padrão de nomes.
- **Mapa do processo** (versão antiga, já desatualizada): https://claude.ai/artifact/KDHzatLun7duKuJ9cBfRoi, cujo código está em `processo.html`.

## O que NÃO está no repositório
- **`_fontes/`**, o material da pós (PDFs, slides). Ele é licenciado para uso pessoal e fica só no computador de origem. As skills já trazem a síntese desse material, com a origem marcada em cada bloco: `[pós: M4]`, `[artigo: …]`, `[prática]` ou `[externo]`. Cada skill tem também um `references/fontes.md`.
- O histórico de conversa. O que importa dele está resumido neste arquivo e no `PLANO.md`.

## Convenções ao editar
- **Marque a origem de todo conteúdo novo:** `[pós: …]`, `[artigo: …]`, `[externo]`, `[prática]` ou `[a partir do usuário]`.
- **Skill nova:** use uma área existente (strategy, research, behavioral, ui, content, delivery, context). Crie uma área nova só quando ela tiver pelo menos duas skills.
- **Depois de mexer,** confira se o `name` de cada skill bate com o nome da pasta e se todo arquivo de `references/` citado existe.
