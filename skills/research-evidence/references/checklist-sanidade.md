# Checklist de sanidade do dado

Rode antes de tirar uma conclusão. Se algum item falhar, registre o limite e rebaixe a confiança, em vez de descartar o dado `[prática]`.

## 1. O dado é real?
- [ ] **Tracking** `[prática]`: o evento dispara certo? Pico ou queda súbita coincidem com release, mudança de evento ou migração de ferramenta?
- [ ] **O que o evento capta** `[artigo: Métricas Boss – Evento GA]`: se ninguém documentou o evento, descubra o que ele mede de fato antes de usá-lo. No GA: veja em quais páginas dispara; no GTM: copie o gatilho e procure o elemento na página. Depois **documente**. Isso é para casos esporádicos; o certo é ter tudo documentado no plano de mensuração.
- [ ] **Definição** `[prática]`: o nome da métrica significa o que achamos? "Sessão" e "usuário" são coisas diferentes, e "taxa de saída" é diferente de "rejeição".
- [ ] **Filtros** `[prática]`: bots, contas internas e ambientes de teste foram excluídos?

## 2. O recorte é certo?
- [ ] **População × amostra** `[pós: M4]` `[artigo: Scribbr – Population vs. Sample]`: a população é o grupo inteiro sobre o qual queremos concluir; a amostra é de quem temos dado. A amostra representa a população-alvo? Um erro comum é estudar pessoas sem interesse na categoria do produto `[pós: M4]`.
- [ ] **Segmentos misturados** `[prática]`: a média geral pode esconder um segmento que vai bem e outro que vai mal. Quebre por segmento, canal ou plataforma.
- [ ] **Viés de sobrevivência** `[pós: M12]`: estamos olhando só quem ficou, converteu ou respondeu? Onde estão os que saíram?

## 3. O tamanho basta?
- [ ] **Amostra** `[pós: M4]`: quanto menor a amostra, maior a variação possível. O erro amostral é proporcional a 1/√n: para reduzir o erro pela metade, é preciso **4×** a amostra.
- [ ] **Proporções pequenas** `[prática]`: "50% dos usuários", quando são 2 de 4, não é um achado. Mostre sempre o n.
- [ ] **Probabilística ou não?** `[pós: M4]` `[artigo: Scribbr]`: uma amostra não probabilística (quem respondeu, quem reclamou) é mais barata, mas qualquer inferência sobre a população fica **mais fraca**. Use para gerar hipótese, não para estimar.

## 4. A comparação é justa?
- [ ] **Período equivalente** `[pós: M4]`: se há sazonalidade, compare o mesmo período do ano anterior.
- [ ] **Mesma definição** nos dois períodos `[prática]`.
- [ ] **Meta** `[pós: M4]`: existe meta para comparar? Sem ela, diga que não há referência.

## 5. A conclusão se sustenta?
- [ ] **Correlação × causalidade** `[pós: M4]`: a relação foi observada ou provocada? Só um experimento testa causa. O resto estima relação.
- [ ] **Diferença real ou ruído?** `[artigo: Netflix – Interpreting A/B Test Results]`: mesmo sem mudança nenhuma, os números oscilam. Numa moeda honesta, 55 caras em 100 jogadas não provam nada (p ≈ 0,32). Antes de dizer que algo "subiu", pergunte se a variação é maior que a oscilação normal daquela métrica.
- [ ] **Média × mediana** `[pós: M4]` `[prática]`: em dados enviesados, como tempo de tarefa, renda ou número de pedidos, a média engana. Use a mediana ou mostre a distribuição.
- [ ] **Ordem de grandeza** `[prática]`: o número bate com o que se esperaria? Se parecer bom ou ruim demais, desconfie primeiro do dado.
- [ ] **Explicação alternativa** `[prática]`: algo mais pode explicar o efeito, como campanha, preço, feriado, concorrente ou mudança de público?

## Como registrar
`Limite: <item> · <o que isso muda na leitura>`. Exemplo: "Limite: o evento da etapa 3 mudou em 15/09, então comparamos só out/26 com out/25."
