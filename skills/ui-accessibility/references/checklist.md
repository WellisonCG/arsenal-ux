# Checklist de acessibilidade por componente

Critérios: `[externo: WCAG 2.2]`, com nomes da tradução oficial pt-BR usados pelo Guia WCAG `[artigo: Guia WCAG]`. Para a correspondência com a **ABNT NBR 17225**, use o próprio Guia WCAG (ele mostra os itens ABNT de cada critério) ou o checklist ABNT da Academia de Acessibilidade. Exemplos e dicas marcados `[pós: M13]`; resto `[prática]`.

## Texto e cor
- [ ] Contraste de texto ≥ 4.5:1 (grande ≥ 3:1) — **1.4.3 (AA)**
- [ ] Informação não transmitida só por cor (erro, status, legenda de gráfico, link no meio do texto) — **1.4.1 (A)** · erro com ícone + texto `[pós: M13]`
- [ ] Texto ampliável a 200% sem perda — **1.4.4 (AA)**
- [ ] Espaçamento de texto ajustável sem quebrar layout — **1.4.12 (AA)**
- [ ] Sem texto em imagem quando dá para ser texto — **1.4.5 (AA)**
- [ ] Dark mode: cores dessaturadas (ex.: primária 200 em vez de 600) e contraste 4.5:1 na superfície mais alta `[pós: M13]`

## Elementos não-texto
- [ ] Ícones de ação, bordas de input, indicador de foco e partes essenciais de gráficos ≥ 3:1 — **1.4.11 (AA)**
- [ ] Imagens de conteúdo com texto alternativo; decorativas ignoráveis; funcionais descrevem a função — **1.1.1 (A)**

## Botões, links e controles
- [ ] Alvo ≥ 24×24 px ou espaçamento suficiente — **2.5.8 (AA)** · mobile: ações principais na zona do polegar `[pós: M13]`
- [ ] Propósito do link claro pelo texto (nada de "clique aqui" solto) — **2.4.4 (A)**
- [ ] Nome acessível contém o rótulo visível — **2.5.3 (A)**
- [ ] Nome, função e estado expostos (toggle, expandido, selecionado) — **4.1.2 (A)**
- [ ] Ação de arrastar tem alternativa sem arrastar — **2.5.7 (AA)**

## Teclado e foco
- [ ] Tudo operável por teclado — **2.1.1 (A)**; sem armadilha de foco — **2.1.2 (A)**
- [ ] Ordem de foco lógica — **2.4.3 (A)**
- [ ] Foco visível — **2.4.7 (AA)**; foco não escondido por cabeçalho fixo, banner de cookies etc. — **2.4.11 (AA)**
- [ ] Link para pular blocos repetidos — **2.4.1 (A)**

## Formulários
- [ ] Rótulo visível ou instrução em todo campo — **3.3.2 (A)** (placeholder não é rótulo `[prática]`)
- [ ] Erro identificado em texto — **3.3.1 (A)**; com sugestão de correção — **3.3.3 (AA)**
- [ ] Propósito do campo identificável (autocompletar nome, e-mail, endereço) — **1.3.5 (AA)** · casa com "evite usar a memória" `[pós: M13]`
- [ ] Não pedir de novo informação já dada no mesmo processo — **3.3.7 (A)**
- [ ] Autenticação sem teste cognitivo obrigatório (permitir colar senha, gerenciador, OTP copiável) — **3.3.8 (AA)**
- [ ] Mudar um campo não muda o contexto sem aviso — **3.2.2 (A)**
- [ ] Transações jurídicas/financeiras reversíveis, verificadas ou confirmadas — **3.3.4 (AA)**

## Estrutura e leitores de tela
- [ ] Títulos e rótulos descrevem o conteúdo — **2.4.6 (AA)**; hierarquia de títulos real — **1.3.1 (A)**
- [ ] Idioma da página definido — **3.1.1 (A)**
- [ ] Mensagens de status (toast, "salvo", "3 resultados") anunciadas sem mover o foco — **4.1.3 (AA)**
- [ ] Tabelas com cabeçalhos associados — **1.3.1 (A)**

## Overlays, movimento e tempo
- [ ] Conteúdo que aparece no hover/foco (tooltip) é dispensável, persistente e alcançável — **1.4.13 (AA)**
- [ ] Carrossel/animação automática com pausar/parar — **2.2.2 (A)**
- [ ] Nada pisca mais de 3 vezes por segundo — **2.3.1 (A)**
- [ ] Limite de tempo ajustável ou extensível — **2.2.1 (A)**
- [ ] Respeitar preferência de movimento reduzido `[prática]` (critério 2.3.3 é AAA)

## Layout
- [ ] Sem rolagem horizontal a 320 px — **1.4.10 (AA)**
- [ ] Orientação não travada (retrato/paisagem) — **1.3.4 (AA)**

## Ferramentas citadas no curso `[pós: M13]`
- **Able** (plugin Figma) — contraste entre camadas
- **Whocanuse** — como o contraste afeta diferentes condições de visão
- **Color Review** — teste de contraste
- **Guia WCAG** (guia-wcag.com) — consulta rápida em pt-BR, com filtros por nível, área responsável e ABNT
- **VPAT** — modelo de relatório de conformidade (ex.: relatórios do Google) para documentar o status do produto
