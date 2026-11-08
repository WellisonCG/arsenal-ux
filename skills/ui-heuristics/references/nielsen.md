# As 10 heurísticas de Nielsen

**Origem do conteúdo:**
- **Definições e dicas:** `[artigo: NN/g – 10 Usability Heuristics]`.
- **Exemplos:** `[pós: M13]`.
- **Colunas "Sinais de violação" e "Correção típica":** `[prática]`, salvo quando marcadas de outra forma.

| # | Heurística | Ideia | Sinais de violação | Correção típica | Exemplo (M13) |
|---|---|---|---|---|---|
| 1 | **Visibilidade do estado do sistema** | manter o usuário informado com feedback em tempo razoável; onde está, de onde veio, para onde vai | etapas sem indicador; ação sem feedback; carregamento sem sinal | indicador "2 de 4", loading, confirmação de sucesso, skeleton | lista de vídeos do YouTube mostra qual está tocando |
| 2 | **Correspondência com o mundo real** | falar a língua do usuário, com conceitos familiares | jargão interno, termos técnicos, ícone sem convenção | UX writing com o vocabulário do usuário (pesquise os termos) | ação destrutiva em vermelho, por associação a perigo |
| 3 | **Controle e liberdade** | uma "saída de emergência" clara; desfazer e refazer | sem cancelar ou voltar; ação irreversível sem desfazer | Undo/Redo, Cancelar visível, editar no lugar | desfazer o envio no Gmail; mudar quantidade no carrinho da Amazon |
| 4 | **Consistência e padrões** | aprender uma vez; seguir as convenções da plataforma e do produto | mesmo componente com comportamentos diferentes; ícones de estilos misturados; nomes diferentes para a mesma coisa | usar o DS; seguir as convenções da plataforma (Jakob) | ícones e menus que mudam de forma a cada uso |
| 5 | **Prevenção de erros** | eliminar condições de erro ou confirmar antes de ações críticas | campo livre onde caberia uma escolha; ação destrutiva sem confirmação; formato não aceito | restrições e bons padrões contra **lapsos**; remover peso da memória e oferecer desfazer contra **enganos**. Prevenir primeiro os erros caros `[artigo: NN/g]` | pop-up de confirmação do Instagram |
| 6 | **Reconhecimento em vez de memorização** | deixar visíveis elementos, ações e opções | usuário precisa lembrar um código ou informação de outra tela; menus escondidos; campos sem exemplo | autocompletar, sugestões, recentes, dicas no hover | autocompletar do Google; OTP copiado pelo próprio iOS |
| 7 | **Flexibilidade e eficiência** | atalhos para quem é experiente sem atrapalhar quem é novato; personalização | caminho único e longo para tarefa frequente | atalhos, ações em massa, favoritos, personalização | feed do Instagram por interesse |
| 8 | **Estética e design minimalista** | foco no essencial do momento; cada elemento extra compete com o relevante | tudo com o mesmo peso; informação secundária disputando atenção | hierarquia; esconder o secundário; o Pareto das funções (20% resolvem 80%) | — |
| 9 | **Reconhecer, diagnosticar e recuperar de erros** | mensagem em linguagem simples, sem código, que diz o problema e sugere a solução | "Erro 500"; mensagem genérica; erro longe do campo | dizer o que houve e como resolver, junto ao campo, com destaque visual | 404 do Mailchimp com caminho de volta; "Você quis dizer" do Google |
| 10 | **Ajuda e documentação** | ajuda pontual, no contexto e fácil de seguir | ajuda só numa central externa; instrução longa | dica contextual no momento da dúvida | ajuda do CVV no Uber |

## Lapso × engano (heurística 5) `[artigo: NN/g – 10 Usability Heuristics]`
- **Lapso (slip):** erro inconsciente, por desatenção. Previna com restrições e padrões.
- **Engano (mistake):** erro consciente, quando o modelo mental do usuário não bate com o design. Previna tirando peso da memória, oferecendo desfazer e avisando.

## Reconhecimento × memorização (heurística 6) `[artigo: NN/g – Recognition and Recall]`
Reconhecer é mais fácil que lembrar do zero, porque o contexto ajuda a recuperar a informação da memória. Para favorecer o reconhecimento, deixe visíveis e acessíveis tanto a **interface** (botões, navegação) quanto o **conteúdo** de que o usuário precisa.

## Consistência ou heurística? `[pós: M13]`
Quando a marca ou o DS contradizem uma heurística (o botão de apagar verde do Spotify), aponte:
1. o risco;
2. como reduzi-lo (ícone de lixeira, confirmação, texto claro);
3. que a decisão é do time.
