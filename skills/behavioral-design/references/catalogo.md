# Catálogo de vieses do curso

**Origem do conteúdo:**
- **Definições:** `[pós: M12]`. O M12 cita estudos para cada viés; eles foram referenciados pelo material, mas não lidos diretamente.
- **Colunas "Use a favor" e "Risco / dark pattern":** `[prática]`, salvo quando marcadas de outra forma.

## Informação: excesso de informação
| Viés | O que é | Use a favor | Risco / dark pattern |
|---|---|---|---|
| **Disponibilidade** | julgamos pelo que vem à mente com facilidade | traga o dado relevante para perto da decisão | na pesquisa: superestimar o último caso lembrado |
| **Confirmação** | absorvemos o que confirma nossas crenças | — (é um viés do time) | testar só para confirmar; "validar" em vez de investigar |
| **Ancoragem** | a primeira informação pesa no julgamento seguinte, mesmo sem relação | mostrar o preço de referência ou o plano recomendado primeiro | preço "de" inflado; âncora falsa |
| **Mera exposição** | a familiaridade aumenta a aceitação | apresentar mudanças aos poucos ("deixe as pessoas se acostumarem") | — |
| **Enquadramento** | o mesmo fato, apresentado de outro jeito, muda a decisão | apresentar benefícios em termos que o usuário valoriza | enquadrar para esconder custo ou risco |
| **Escolha limitada** | escolher é mais fácil com poucas opções (o paradoxo da escolha, o estudo das geleias) | poucas opções e uma destacada como padrão | esconder a opção que o usuário quer |
| **Contraste (Von Restorff)** | lembramos do que se destaca | destacar só a ação-chave | destacar a opção cara e apagar a "Não, obrigado" |
| **Apoio à escolha** | depois de decidir, valorizamos os pontos positivos da escolha | reforçar a escolha com sentimentos positivos (por exemplo, a confirmação) | — |

## Ambiguidade: falta de significado
| Viés | O que é | Use a favor | Risco / dark pattern |
|---|---|---|---|
| **Prova social** | seguimos o que os outros fazem. Tipos no M12: descritiva, aspiracional, subjetiva, dinâmica | avaliações reais, "mais escolhido" | números inventados ou sem contexto; reviews falsos |
| **Maldição do conhecimento** | quem sabe não consegue imaginar não saber | use boas metáforas e a linguagem do usuário; teste com novatos | — (é um viés do time) |
| **Sobrevivente** | focamos em quem passou pelo filtro e esquecemos o resto | pesquisar também quem saiu ou desistiu | conclusões tiradas só de quem ficou |
| **Autoridade** | obedecemos a figuras de autoridade (o estudo do uniforme) | selos e especialistas **reais** | autoridade falsa; selo inventado |
| **Falácia da mão quente** | quem teve sucesso parece que sempre terá | — | "deu certo na empresa X, vai dar aqui" |
| **Viés da história** | confiamos em quem conta histórias, e histórias fixam na memória | storytelling em onboarding e cases | história que distorce o fato |
| **Atalho metafórico** | metáforas fazem entender mais rápido (o desktop da Xerox) | ícones e metáforas familiares | metáfora que promete o que o produto não faz |
| **Efeito padrão** | tendemos a aceitar o que já vem selecionado | o padrão = a melhor opção **para o usuário**; padrões que criam bons hábitos | **pré-marcar** o que o negócio quer. Exemplo do M12; ver `etica.md` |

## Tempo / ação: necessidade de agir
| Viés | O que é | Use a favor | Risco / dark pattern |
|---|---|---|---|
| **Hawthorne** | mudamos o comportamento quando nos sabemos observados | — | na pesquisa, o comportamento no teste não é o real |
| **Efeito IKEA** | valorizamos mais o que ajudamos a construir | personalização, configuração guiada | esforço artificial que só serve para prender o usuário |
| **Aversão ao risco** | evitamos o risco e a perda | garantia, teste grátis, devolução fácil | medo exagerado para forçar a compra |
| **Reatância** | sob pressão excessiva, fazemos o oposto | reduzir a pressão; dar controle | excesso de urgência (o Booking é o exemplo do M12) **afasta** o usuário |
| **Escassez** | o escasso parece mais valioso. Tipos: **quantidade**, **tempo**, **acesso**, **meio de pagamento** | só escassez **real**, com informação útil (por exemplo, "último posto em 80 km") | estoque ou contador falsos |

## Memória: o que lembrar
| Viés | O que é | Use a favor | Risco |
|---|---|---|---|
| **Posição serial** | lembramos do primeiro e do último | o importante no início e no fim. Na pesquisa, alterne a ordem das opções | esconder no meio o que o usuário precisa saber |
| **Zeigarnik** | lembramos do que ficou incompleto | checklist e progresso no onboarding | notificações de "incompleto" para gerar ansiedade |
| **Blocamento (chunking)** | informação em blocos é mais bem processada. Agrupe para clarificar, converter e memorizar | agrupar campos, números, etapas | — |
| **Curiosidade** | quatro tipos: perceptiva, específica, epistemológica, diversa | dar indícios de conteúdo a explorar | clickbait |
| **Pico-fim** | julgamos a experiência pelo pico e pelo fim | cuidar do pior momento e do final. Responder a um review ruim é um "ponto de oportunidade" | — |

## Priming `[artigo: NN/g – Priming]`
Uma exposição anterior influencia a resposta seguinte.
- **Na interface:** imagens e palavras preparam a interpretação.
- **Na pesquisa:** usar na tarefa os termos da interface induz o participante a procurá-los. Escreva as tarefas com as palavras do usuário, não com as da tela.
