# Padrões de tela

O catálogo vem de `[pós: M13: Aumentando o repertório com tipos de telas, 12.0–12.9]`. As colunas "Pergunte" e o checklist de estados são `[prática]`.

## Catálogo, por categoria
| Categoria | Padrões | Pergunte |
|---|---|---|
| **Celebração** | conquistas, conclusão, dark mode | o fim do fluxo é um "pico" positivo? (pico-fim) |
| **Dados** | gráficos, barras de progresso (gestão de expectativa), dashboards, guia de tamanhos, coleções, favoritos, offline, playlist, lixeira | dado operacional ou analítico? Que decisão o dado apoia? |
| **Conteúdo** | home, discovery/explorer, feed, lista de itens, e-mail e mensagens, artigo, vídeo, podcast, receita, nota, metas, post, stories, chat, evento, quiz, jogo, aula, produto, realidade aumentada | qual conteúdo é o principal? |
| **Social** | conquistas, notificações, adicionar amigos, comentários, feed, seguidores, ranking, perfil, reviews, comunidades | tem moderação, privacidade e denúncia? |
| **Comunicação** | sobre, opções de ação, **sucesso**, **erro**, **confirmação**, **permissões**, **estado vazio**, **loading**, pull to refresh, coach marks, novidades (gestão de mudança), configurações, ajuda, feedback, privacidade, termos, sugestões | cada estado da tela tem a sua comunicação? |
| **Ações comuns** | adicionar, editar, excluir, upload/download, seleção, mover, reordenar, desenhar, salvar, cancelar, agendar, votar, seguir, compartilhar, denunciar, bloquear, filtrar e ordenar, pesquisar, transferir dinheiro | a ação é reversível? tem desfazer ou confirmação? |
| **E-commerce** | produto, carrinho, checkout | o que o usuário precisa saber antes de pagar? |
| **Onboarding** | telas iniciais | o usuário chega ao valor rápido? dá para pular? |
| **Outros** | timeline, calendário, data e hora, timer, lembrete, endereço, mapa, browser in-app, chatbot, players, gravador, editor de mídia, câmera e scanner, filtros, ligação | — |

**Repertório visual:** Mobbin; o DS da empresa; Material Design 3 e Apple HIG `[pós: M13]`.

**Projetando para exibir dados** `[pós: M13]`: separe **dados operacionais** (acompanhar o agora e agir) de **dados analíticos** (entender tendência e decidir). Para escolher o gráfico, veja `research-evidence/references/qual-grafico.md`.

## Checklist por camada, do macro para o micro `[prática, a partir do usuário]`
Use uma camada por vez. Só passe para a próxima quando a anterior estiver resolvida.

**1. Escopo**
- [ ] Que problema o fluxo resolve e onde ele termina

**2. Caminho principal (golden path)**
- [ ] O fluxo funciona de ponta a ponta no cenário mais comum

**3. Casos de borda**
- [ ] **Primeira vez / vazio:** explica o que vai aparecer e qual o primeiro passo
- [ ] **Erro:** diz o que houve e como resolver (heurística 9)
- [ ] **Parcial:** poucos itens, dados incompletos
- [ ] **Sem permissão / bloqueado:** diz como obter acesso
- [ ] **Offline / sem conexão**, se o produto tem uso móvel
- [ ] **Conteúdo extremo:** texto muito longo, nome grande, número alto, sem imagem

**4. Feedback do sistema**
- [ ] **Carregando:** skeleton ou indicador; acima de 5–10 s, explica a espera `[pós: M13]`
- [ ] **Sucesso:** confirma o que aconteceu (toast ou tela de sucesso)

**5. Refinamento**
- [ ] Motion e microinterações, só onde agregam
- [ ] **Dark mode** e **responsivo**, conforme o DS e as plataformas
