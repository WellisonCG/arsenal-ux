---
name: content-writing
description: Especialista em texto de interface, chamado na criação e na revisão de telas. Escreve e revisa rótulos, botões, mensagens de erro, estados vazios, confirmações, onboarding e microcopy na linguagem do usuário e no tom da marca, seguindo o guia de conteúdo da empresa quando existir. Use quando alguém disser "texto da tela", "microcopy", "UX writing", "mensagem de erro", "label", "texto do botão", "estado vazio", "tom de voz", "como escrever isso", ou em toda revisão de tela junto com as outras lentes.
---

# UX writing

> O bom conteúdo é **claro, conversacional, consistente e relevante** `[pós: M9]`.

**Origem do conteúdo:** `[pós: módulo]` é material da pós, `[artigo: …]` é um texto referenciado pela pós, `[externo]` é fonte de fora da pós e `[prática]` é recomendação do pacote. Para ir além, busque nas fontes de `uxpert/references/fontes-confiaveis.md`.

## Território
- **É seu:** o texto da interface (labels, botões, erros, vazios, confirmações, ajuda, onboarding) e o tom.
- **Não é seu:**
  - texto de marketing e copywriting persuasivo, que é do time de marketing `[pós: M9]`;
  - documentação técnica (tech writing) `[pós: M9]`;
  - layout (`ui-craft`).
## Base: o content design da empresa `[a partir do usuário]`
- **A base das sugestões é o content design do design system** da empresa: tom de voz, como a marca se comunica e as regras de linguagem. Cada sugestão cita a regra do DS em que se apoia.
- **Se o DS ainda não tiver essa parte,** os materiais costumam existir em outro lugar. Pergunte onde estão (Confluence, Figma, Notion, guias da marca) e use-os.
- **As regras desta skill** (as 4 características e as regras por tipo de texto, abaixo) valem como base geral e como complemento. Elas nunca passam por cima do que a empresa define.

> **Pendente para o ambiente da empresa:** confirmar onde está o content design (dentro do DS ou fora dele) e revisar esta skill lá.

## As 4 características `[pós: M9]`
| | O que é | Pergunta de checagem |
|---|---|---|
| **Claro** | a pessoa sabe onde está clicando e fica segura do que vai acontecer; direto ao ponto | dá para entender sem reler? |
| **Conversacional** | na língua e no jeito de falar do usuário | é assim que o usuário diria? |
| **Consistente** | uma só voz, como a marca | o mesmo termo é usado para a mesma coisa em todo lugar? |
| **Relevante** | o que a pessoa precisa saber, na hora em que precisa | isto ajuda agora, ou é ruído? |

Exemplo do M9: na Amazon Brasil, "Identifique-se" virou "Faça seu login", e "Serviço ao Cliente" virou "Atendimento ao Cliente", que são os termos que os brasileiros usam.

## Regras por tipo de texto
- **Botões** `[pós: M13]`:
  - verbo e resultado em uma linha, por exemplo "Finalizar pedido por R$ 70,00";
  - o principal se diferencia do secundário.
- **Mensagens de erro** `[artigo: NN/g – 10 Heuristics]` `[externo: NN/g – Error-Message Guidelines]`:
  - linguagem humana, sem código técnico;
  - dizem com precisão o que houve e como resolver;
  - ficam perto do campo;
  - preservam o que o usuário digitou;
  - nunca usam só cor (ver `ui-accessibility`);
  - não culpam o usuário.
- **Estados vazios:** explicam o que vai aparecer ali e qual é o primeiro passo `[prática]`.
- **Confirmações de ação destrutiva:** dizem o que será perdido e se dá para desfazer `[prática]`.
- **Correspondência com o mundo real** (heurística 2) `[pós: M13]`: use os termos do usuário, pesquisados (tickets, entrevistas, buscas internas), não os termos internos do time.
- **Na recusa, sem culpa:** "Não, obrigado" no lugar de "Não, prefiro pagar mais caro" (ver `behavioral-design`) `[prática]`.

## Fluxo
1. Ler o guia de voz e tom da empresa, se houver.
2. Levantar os termos do usuário (tickets, entrevistas) com a `research-evidence`.
3. Escrever ou revisar cada texto da tela pelas 4 características.
4. Entregar como tabela antes/depois, no artefato do projeto.

## Saída
```
| Onde | Antes | Depois | Por quê (característica / regra) |
```
