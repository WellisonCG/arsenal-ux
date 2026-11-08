---
name: research-benchmark
description: Especialista em benchmark de UX/UI, chamado em qualquer fase (investigar, criar, validar). Pesquisa como concorrentes diretos e produtos análogos de outros nichos resolvem o mesmo problema, prioriza plataformas consolidadas, registra padrões com prints e links, e entrega um quadro comparativo com o que copiar, o que evitar e os padrões que viram variações. Use quando alguém disser "benchmark", "como os concorrentes fazem", "referências", "repertório", "inspiração", "análise competitiva", "como outros produtos resolvem", ou antes de montar variações de tela.
---

# Benchmark

> O benchmark mostra **soluções**, não prova que elas funcionam `[prática]`. Ele serve de repertório e de argumento: "é assim que os concorrentes fazem", "é o padrão que a Amazon usa".

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós e `[prática]` é recomendação do pacote. As fontes de busca estão em `uxpert/references/fontes-confiaveis.md`.

## Território
- **É seu:** buscar, registrar e comparar soluções de terceiros para o problema da demanda.
- **Não é seu:**
  - criar as variações (`ui-craft`, que usa o seu quadro);
  - avaliar a usabilidade da nossa tela (`ui-heuristics`);
  - pesquisa com usuários (`research-studies`).

## As duas frentes `[prática, a partir do usuário]`
1. **Concorrentes diretos do nicho.** Exemplo: se o produto é um CRM, outros CRMs.
2. **Análogos em outros nichos que resolvem um problema parecido.** Exemplo: criar uma campanha de e-mail se parece com criar um card no Jira ou uma tarefa no Todoist, inclusive na validação dos campos. Pergunte: qual é a tarefa essencial, e onde mais ela aparece?

Os exemplos ilustram o raciocínio; escolha as referências pelo caso real.

## Fluxo
1. **Definir a tarefa** a comparar, com a pergunta e o recorte (a criação do item, a validação, o estado vazio…).
2. **Escolher as referências:** de 3 a 6 por frente, priorizando plataformas consolidadas que seguem bons padrões de design. Consulte o `context-company` para saber quem são os concorrentes.
3. **Buscar**, nesta ordem:
   - navegando o produto ao vivo, quando possível;
   - nos materiais do próprio sistema analisado (telas, central de ajuda, documentação, blog de produto). Exemplo: para um fluxo da Amazon, nos materiais da Amazon;
   - em benchmarks públicos que já existem sobre aquele fluxo (estudos do Baymard, análises publicadas, case studies). Não refaça o que já foi feito;
   - em repositórios: Mobbin `[pós: M13]`, Page Flows, Baymard `[externo]`;
   - nas diretrizes da plataforma: Material Design, Apple HIG `[pós: M13]`.
   Registre o link e a data de cada print.
4. **Registrar cada referência:** quem é, o padrão usado, o que copiar, o que evitar, o print e o link.
5. **Comparar:**
   - os padrões que se repetem (são a convenção, pela Lei de Jakob `[pós: M13]`);
   - as soluções diferentes (são candidatas a variação);
   - as lacunas (oportunidades).
6. **Entregar** o quadro no artefato do projeto. Ele vira insumo da `ui-craft`.

## Saída
```
Tarefa comparada: <…>
| Referência | Frente | Padrão | Copiar | Evitar | Link/print |
Padrões recorrentes (convenção): <…>
Abordagens distintas → candidatas a variação: A <…> · B <…> · C <…>
Lacunas / oportunidades: <…>
```

## Cuidados `[prática]`
- **Não copie o contexto junto com a tela.** O que funciona para um público e um modelo de negócio pode não funcionar para o nosso.
- **Conta a convenção do mercado, não só um líder.** Um produto famoso não é prova de padrão.
- **O benchmark pode embasar dark patterns.** Passe o resultado pela `behavioral-design`.
