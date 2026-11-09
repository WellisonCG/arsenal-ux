# Notas de atualização

## 0.1.1 (2026-11-09): auditoria das fontes

Cruzamos os 28 comentários da revisão no canvas com o texto das skills. Quase tudo já estava aplicado; a correção ficou nas fontes.

### Corrigido
- **behavioral-design:** o Coglode (indicação do usuário) e o Growth.Design entraram na seção "De onde vem o conhecimento", como fontes de aplicação no design. Elas mostram como aplicar o viés; o estudo original prova o efeito. Antes, as duas só apareciam no `uxpert/references/fontes-confiaveis.md`.
- **behavioral-design/references/fontes.md:** nova tabela "Fontes de busca fora da pós", com Coglode, Growth.Design e The Decision Lab, todos com link.

### Novo
- **research-benchmark/references/fontes.md**, com:
  - onde buscar, em ordem de força: o produto ao vivo, os materiais do próprio sistema analisado (por exemplo, os da Amazon para um fluxo da Amazon), os benchmarks públicos que já existem, os repositórios (Mobbin, Page Flows, Baymard, Built for Mars) e as diretrizes de plataforma;
  - as duas frentes: concorrentes diretos e análogos de outros nichos;
  - o lembrete de que benchmark é ponto de partida, não validação.
- **research-synthesis/references/fontes.md:** os módulos da pós usados (M1, M2, M3, Disc. 09) e onde buscar métodos de síntese que não estão na skill.
- **content-writing/references/fontes.md:** o content design do DS como base principal (pendente de confirmar onde está), o material do M9 e do M13 e os links da NN/g.
- As três skills agora listam o `fontes.md` na seção "Referências".

### Ajustado
- **CLAUDE.md:** o texto dizia que toda skill tem um `fontes.md`, o que não vale para a `context-company`, que só tem templates, nem para o `uxpert`, que usa o `fontes-confiaveis.md`. Agora diz isso.

### Conferido e já aplicado (sem mudança)
- rollout pelo tamanho e risco;
- perguntas sem limite fixo;
- três caminhos para hipótese de baixa confiança;
- timebox transversal, com alta fidelidade como padrão;
- pesquisa caso a caso, sem meta por cohort, com Pareto e loop de revisão do roteiro;
- três níveis de dark pattern;
- regras visuais vindas do DS, templates e acesso de teste;
- do macro para o micro, começando pelo golden path;
- variações com origem, prós e contras e recomendação, passando pelas lentes;
- content design do DS como base;
- `projeto.md` local;
- respostas sucintas, com o entregável no lugar do textão;
- pendências de handoff, acessibilidade e context-company.

### Ficou de fora de propósito
- As 8 regras de ouro de Shneiderman e o livro *Rápido e Devagar*, de Kahneman, como fontes de busca. Foram sugestões do Claude, sem aprovação explícita.

## 0.1.0 (2026-11-08): primeira versão
16 skills no padrão `área-especialidade`, com o `uxpert` como condutor, mais os comandos `/nova-demanda`, `/plano-pesquisa`, `/revisar-tela` e `/handoff`. O histórico das revisões v1 a v5 está no `PLANO.md`.
