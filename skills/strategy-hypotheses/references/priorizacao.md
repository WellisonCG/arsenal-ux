# Priorizar hipóteses

`[prática]`. A pontuação é do pacote. A regra de começar pelo maior risco segue a lógica do discovery de atacar os riscos importantes cedo `[artigo: PM3 – Dual Track]`.

## Pontuação rápida (de 1 a 3)
| Critério | 1 | 2 | 3 |
|---|---|---|---|
| **Impacto**: quanto move o KPI se for verdade | pouco | moderado | muito |
| **Confiança**: quanta evidência já temos | só opinião | indícios (tickets, heurística) | dado da empresa + quali |
| **Esforço**: quanto custa testar ou construir | baixo | médio | alto |

## Como ler
| Impacto | Confiança | O que fazer |
|---|---|---|
| Alto | **Baixa** | **Testar primeiro.** É a suposição mais arriscada. Protótipo e teste antes de construir |
| Alto | Alta | Construir. Lançar pequeno e medir |
| Baixo | Baixa | Descartar ou guardar no backlog |
| Baixo | Alta | Fazer só se o esforço for baixo, como quick win |

O esforço desempata. Entre duas hipóteses no mesmo quadrante, comece pela mais barata.

## Mostrar ao time
Apresente a tabela com a recomendação e o porquê, em uma linha cada. Exemplo:

> "H2 primeiro: impacto alto e só 1 de confiança, que vem de 3 tickets. Se estiver errada, H1 e H3 perdem o sentido."
