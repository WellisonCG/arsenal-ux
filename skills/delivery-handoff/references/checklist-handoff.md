# Checklist de handoff

## 1. Fluxo e estados `[pós: M13]` `[prática]`
- [ ] Fluxo completo, sem pontas soltas `[pós: M8]`
- [ ] Estados de tela: vazio, carregando, sucesso, erro, parcial, sem permissão, offline (ver `ui-craft/references/padroes-de-tela.md`)
- [ ] Estados de componente: padrão, hover, foco, pressionado, desativado, carregando `[pós: M9, M13]`
- [ ] Edge cases: texto longo, nome grande, número alto, lista vazia ou enorme, imagem ausente
- [ ] Mensagens de erro e de espera escritas, sem placeholder `[pós: M8]`
- [ ] Responsivo nas plataformas do produto

## 2. Consistência visual `[pós: M9]`
- [ ] Cores conforme as especificações da marca e do DS
- [ ] Ícones seguem as regras de aplicação
- [ ] Tipografia conforme a especificação
- [ ] Tom e voz da marca presentes no conteúdo
- [ ] Imagens e assets no mesmo padrão visual

## 3. Consistência comportamental `[pós: M9]`
- [ ] Estados de interação padronizados (active, hover, focus…)
- [ ] Animações claras e com significado ("motion is meaning", do Material Design)
- [ ] O mesmo componente se comporta igual em toda a interface (heurística 4)

## 4. Qualidade pelas heurísticas `[pós: M9]`
O M9 usa as 10 heurísticas como parâmetro de qualidade da entrega. Confirme que a `ui-heuristics` rodou na fase 5 e que os achados ALTO e CRÍTICO foram resolvidos ou aceitos com trade-off registrado.

## 5. Conteúdo `[pós: M9]`
- [ ] **Claro:** a pessoa sabe onde está clicando e o que vai acontecer
- [ ] **Conversacional:** na língua do usuário
- [ ] **Consistente:** uma voz só
- [ ] **Relevante:** o que a pessoa precisa saber, na hora em que precisa

## 6. Acessibilidade `[prática]`
- [ ] A `ui-accessibility` rodou e não há achado CRÍTICO aberto
- [ ] Anotações para o dev: ordem de foco, rótulos acessíveis, textos alternativos, mensagens de status

## 7. Entrega `[pós: M13]` `[pós: M8]`
- [ ] Arquivos organizados, no padrão de entrega da empresa (`context-company`)
- [ ] Assets exportados: imagens, ícones, fontes
- [ ] Specs no próprio arquivo de design (tokens do DS, espaçamentos, comportamentos)
- [ ] Handoff feito **com** o time de dev, em conversa e não só por link
- [ ] Canal de suporte durante a sprint definido
- [ ] Plano de mensuração anexado (ver `plano-de-medicao.md`)
