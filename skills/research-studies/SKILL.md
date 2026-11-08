---
name: research-studies
description: Especialista transversal em pesquisa, chamado em qualquer fase. Domina os métodos validados de research (entrevista, survey, testes, benchmark, mapa de empatia, jornada do usuário, service blueprint, personas, JTBD, diário e outros), sabe quando cada um serve e recomenda o de menor esforço para o resultado esperado, considerando os dados que já existem. Escolhe o método pela pergunta, prazo e custo (survey, entrevista em profundidade ou semiestruturada, teste de usabilidade moderado ou não moderado, guerrilha, card sorting, tree test, first-click, teste de 5 segundos, diário, pesquisa contextual), recruta por cohort a partir de dados, define tamanho de amostra, gera roteiro, termo de consentimento e template de síntese, e evita os vieses do pesquisador. Use quando alguém disser "pesquisa", "entrevista", "teste de usabilidade", "com quem eu falo", "recrutar", "roteiro", "formulário", "survey", "questionário", "não tenho tempo pra pesquisa", "sintetizar entrevistas", "quantas pessoas".
---

# Pesquisar

> Zero usuários dão zero insights. Um pouco de dado já muda muito `[artigo: NN/g – Why You Only Need to Test with 5 Users]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. Os links estão em `references/fontes.md`.

## Território
- **É seu:** gerar dado novo com usuários: escolher o método, recrutar, definir a amostra, escrever e revisar o roteiro e o consentimento, e conduzir.
- **Outras skills:** a síntese e os mapas são da `research-synthesis`; o benchmark é da `research-benchmark`. Rode-as em paralelo quando fizer sentido.
- **Não é seu:**
  - dados que já existem (`research-evidence`);
  - avaliação por especialista sem usuário (`ui-heuristics`, `ui-accessibility`);
  - medição pós-lançamento (`delivery-metrics`).

## Fluxo

### 1. Separar pergunta de pesquisa de pergunta ao usuário `[pós: M3]`
- **Pergunta de pesquisa** é o que o time quer aprender. Exemplo: "Como as pessoas decidiram usar o produto?". Ela **não** é feita ao usuário.
- **Perguntas ao usuário** vêm depois e servem para responder a pergunta de pesquisa.
- Comece pelas perguntas da fase 1 e pelas lacunas da fase 2 (`projeto.md`).

### 1b. Partir do que já sabemos e das restrições reais `[prática, a partir do usuário]`
- **Dados prévios:** o que a fase 2 já trouxe. Foque no que ainda é mais dúvida do que certeza.
- **Restrições reais:** quanto tempo existe (`strategy-timebox`) e quantas pessoas dá para acessar. Pode ser 10, 5, 1 ou nenhuma. Alguma pesquisa é melhor que nenhuma `[artigo: NN/g – 5 Users]`.
- **Menor esforço que tira mais dúvidas:** aplique Pareto e a navalha de Occam `[pós: M13]`. Qual é a coleta mais simples que resolve as maiores dúvidas?

Não existe meta fixa de participantes por cohort: decida caso a caso, com o designer.

### 1c. Dominar os métodos, não só os da lista
- **O domínio esperado:** a skill deve conhecer os métodos validados de research, saber o esforço de cada um, saber quando cada um serve e recomendar o de menor esforço para o resultado esperado.
- **Base e busca:** `references/metodos.md` é a base. Para métodos que não estão nela, busque nas fontes de `uxpert/references/fontes-confiaveis.md` (NN/g como principal), cite o link e aplique.
- **Exemplos não são o limite:** os métodos citados nas tabelas são exemplos, não a lista completa.

### 2. Escolher o método
Escolha pelo que precisa ser respondido, pelo prazo, pelo custo e pela confiança necessária. Ofereça 2 ou 3 opções e marque a recomendada `[prática]`. Use a matriz de `references/metodos.md`.

As três dimensões para decidir `[artigo: NN/g – Which UX Research Methods]`:
1. **Atitudinal × comportamental:** o que as pessoas **dizem** ou o que elas **fazem**?
2. **Qualitativo × quantitativo:** **por que** e **como** resolver, ou **quantos** e **quanto**?
3. **Momento:**
   - **generativa**, para escolher a direção (fase 2);
   - **formativa**, para melhorar o design (fase 5);
   - **somativa**, para medir o resultado (fase 6).

Regras de bolso:
- **Survey** serve para escala e parâmetros: feedback, priorização, percepção, dados objetivos. **Não serve** para causa raiz, dores profundas ou linguagem corporal; para isso, use entrevista (os 5 porquês) `[pós: M2]`.
- **Sem conhecimento nenhum do segmento,** comece por um survey para levantar hipóteses e depois aprofunde com entrevistas. Se as entrevistas trouxerem algo, um survey pode checar em escala. Isso é pesquisa com **métodos mistos** `[pós: M2]`.
- **Entrevista em profundidade** responde como a pessoa se sente, por que pensa assim e o que motivou uma decisão. **Não** responde "é fácil de usar?" nem "quantos usam?" `[pós: M3]`.
- **Teste de usabilidade** é a observação sistemática de alguém tentando completar uma tarefa numa interface. A interface pode ser um protótipo, o produto ou um concorrente `[pós: M2]`.

### 3. Definir quem e quantos
Use `references/recrutamento.md`.

- **Perfilamento** `[pós: M3]`:
  - parta das hipóteses e escolha 2 características **fundamentais**, mais as **interessantes**;
  - recrute por **comportamento** quando a pergunta é de comportamento (por exemplo, compra), e por demografia só quando ela importa (por exemplo, faixa etária).
  - A amostra precisa ser **válida** (representa a população) e **viável** (dá para recrutar).
- **Recrutamento por cohort** `[prática]`, quando houver acesso a usuários:
  1. segmente pelo comportamento visto nos dados;
  2. liste candidatos por cohort, mais do que o necessário, porque nem todos aceitam;
  3. decida com o designer quantas conversas cabem, pelo prazo e pelo acesso, sem meta fixa;
  4. diga de onde saiu cada lista (C2).
- **Quantos** `[artigo: NN/g – Why You Only Need to Test with 5 Users]`:
  - teste de usabilidade com público homogêneo: **5**;
  - com 2 grupos distintos: **3 a 4 por grupo**;
  - com 3 grupos ou mais: **3 por grupo**, que é o mínimo para ver a diversidade do comportamento;
  - teste quantitativo de usabilidade: **20**;
  - card sorting: **15**.
  - Prefira **vários testes pequenos** a um grande: teste, ajuste e teste de novo.
  - Esses números são referência de qualidade, não exigência. Se o acesso for menor, faça com o que der e diga o limite da leitura `[prática]`.
- **Quanto menor a amostra, mais rigoroso o critério de quem entra** `[pós: M2]`.
- **No espaço do problema** `[artigo: Caliari – Triple Track]`: recrute também quem tenta resolver o mesmo problema sem ser nosso usuário, e pessoas que agiram sobre o problema há 1 a 3 meses.

### 4. Preparar
- **Roteiro:** use `references/roteiros.md` (entrevista e teste de usabilidade) `[pós: M2, M3, Roteiro de Teste de Usabilidade]`.
- **Consentimento e dados:** use `references/etica-e-dados.md` `[pós: M2, M10]`. Peça autorização para gravar, explique o uso e lembre que a participação é voluntária. Fale com o jurídico.
- **Plano de uma página** `[artigo: Smashing – UX Research Plan]`: título, autor e stakeholders, data, contexto, objetivos (no máximo 3 ou 4), perguntas de pesquisa, método, participantes, cronograma e roteiro. Se o plano não cabe numa página, provavelmente ainda não está claro.
- **Piloto:** teste o roteiro com uma pessoa antes, para cronometrar as tarefas `[pós: M2]`.
- **Loop de revisão do roteiro** `[prática, a partir do usuário]`: antes de entregar, faça de 2 a 3 voltas de montar, revisar e ajustar. Em cada volta, confira:
  - as perguntas são abertas?
  - alguma é indutiva ou enviesada?
  - há perguntas compostas?
  - há termos difíceis ou jargão?
  - a ordem cria efeito de posição?
  - as tarefas repetem as palavras da tela (priming)?
  - o resto da tabela do passo 5 está atendido?
  Depois das voltas, entregue o roteiro ao **designer para a revisão final**.

### 5. Conduzir sem enviesar `[pós: M1, M3]` `[artigo: Qualtrics – Acquiescence Bias]`
| Evite | Por quê | Faça |
|---|---|---|
| Pergunta fechada ("Você já usou?") | dá pouca informação | pergunta aberta e exploratória ("Me conta a última vez que…") |
| Pergunta indutiva ("Não gostou dessa tela, né?") | viés de confirmação | pergunta neutra ("O que você achou?") |
| Pergunta julgadora | constrange | descrição neutra |
| Pergunta composta | a resposta fica ambígua | uma ideia por pergunta |
| Pedir para concordar ou discordar, sim ou não | **viés de aquiescência**: a tendência a concordar | pergunte sobre fatos e comportamentos, ofereça opções equilibradas |
| Futuro do pretérito ("Você pagaria?") | quem diz que pagaria não pagou | ancore em fato passado ("Quanto você pagou da última vez?") `[pós: M2]` |
| Dar dica durante a tarefa | efeito Clever Hans: o participante lê os sinais do moderador | silêncio, e "O que você faria se eu não estivesse aqui?" |

Também atrapalham `[pós: M1]`:
- **ancoragem e enquadramento** na formulação;
- **efeito de posição**: a ordem das perguntas e das opções influencia a resposta;
- **viés implícito** do pesquisador.

Vale também o **efeito Hawthorne** `[pós: M12]`: o participante muda o comportamento porque sabe que está sendo observado.

### 6. Sintetizar
Passe para a skill `research-synthesis`, que cuida do debriefing, da codificação, dos mapas e dos insights. Ela pode rodar em paralelo, sessão a sessão.

### 7. Devolver ao projeto
- Atualize o `projeto.md`: as evidências novas com nível `[pesquisa]` e o status das hipóteses.
- Diga o que a pesquisa **não** respondeu.

## Saída
```
Pergunta de pesquisa: <…>
Método: <recomendado> · alternativas: <…> (o que responde · tempo · custo)
Participantes: <critérios fundamentais> · <n por cohort> · fonte da lista: [fonte: …]
Roteiro: <anexo> · Consentimento: <ok / pendente com jurídico>
Cronograma: <recrutar · campo · síntese>
Resultado: <insights, com o nível [pesquisa]> · Hipóteses: <status> · Não respondido: <…>
```

## Referências
- `references/metodos.md`: matriz de métodos (pergunta × prazo × custo)
- `references/recrutamento.md`: perfilamento, cohorts, quantos, onde achar
- `references/roteiros.md`: entrevista semiestruturada e teste de usabilidade
- `references/etica-e-dados.md`: LGPD, consentimento, retenção
- `references/fontes.md`
