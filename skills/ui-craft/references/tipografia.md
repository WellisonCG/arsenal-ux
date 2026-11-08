# Tipografia

Todo o conteúdo vem de `[pós: M13: Tipografia – Princípios; Aplicações em produtos]`. As exceções estão marcadas.

## Escala de tipos
- O Material Design define uma **type scale** de 13 estilos reutilizáveis, cada um com uma aplicação e um significado.
- Defina **antes** os tamanhos de título, subtítulo, parágrafo e botão. Assim, ao criar uma funcionalidade nova, ninguém decide fonte, tamanho ou estilo na hora, e a consistência fica garantida.
- **Se houver DS, use a escala dele** `[prática]`.

## Padrões de leitura
- **Padrão F:** o usuário lê o início das primeiras linhas e varre a lateral esquerda. Coloque a informação-chave no começo das linhas e dos títulos.
- **Padrão Z:** em telas com pouco texto, o olho percorre um Z. Use para landing pages e telas de ação.

## Legibilidade e leiturabilidade
| Aspecto | Recomendação |
|---|---|
| **Comprimento de linha** (corpo) | **40 a 60 caracteres**. Linhas curtas: 20 a 40. Em áreas largas, aumente a fonte |
| **Espaço entre parágrafos** | **0,75× a 1,25×** o tamanho da fonte |
| **Alinhamento** | à **esquerda** na maioria dos casos; centralizado só para citações e textos curtos; à direita em casos muito específicos; evite justificado |
| **Peso** | crie hierarquia com o peso, não só com o tamanho |
| **Monoespaçada** | para código e dados alinhados |

## Combinação de fontes
- Combine **duas** fontes. Ferramenta: fontpair.
- **Regra do M13:** títulos e subtítulos sem serifa; textos corridos com serifa, para fluidez de leitura.
- Em produto digital é comum usar **uma família sem serifa** com vários pesos `[prática]`.
- Typeface é a família; fonte é a variação (peso, estilo).

## Tamanhos de corpo
- **O M13 recomenda** cerca de **16 px** em desktop e laptop e **12 px** em smartphone, mas avisa: "Teste antes, não é uma regra", porque o tamanho percebido varia por typeface.
- **Atenção** `[externo]`: as diretrizes de plataforma recomendam corpo **maior** no mobile. Na Apple, o corpo padrão é de 17 pt; no Material, o corpo vai de 14 a 16 sp.
- **Recomendação do pacote** `[prática]`: no mobile, **corpo ≥ 16 px** e 12 px só para legendas e metadados. Verifique legibilidade e zoom com a `ui-accessibility`.
