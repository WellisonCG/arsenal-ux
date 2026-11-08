# Percepção, atenção e memória

Todo o conteúdo vem de `[pós: M13: Usabilidade e mente humana; Percepção visual e Gestalt; Atenção, memória, familiaridade e Aesthetic Usability Effect]`. As exceções estão marcadas.

## Simplicidade
- Simplifique ao máximo ou quebre o complexo em partes. Formulários extensos podem ser divididos em seções.
- **Exceção:** trabalho repetitivo, como formulários administrativos, pode juntar tudo num campo de visão.
- Formulários aumentam o custo de interagir. Exemplo: a Amazon trocou o botão "Cadastrar" por "Continuar" e deixou o cadastro para o fim, o que aumentou as vendas em 45% (cerca de US$ 300 milhões no primeiro ano).

## Encontrabilidade × descobribilidade
| Conceito | O que é | Depende de |
|---|---|---|
| **Encontrabilidade** (findability) | achar algo que você **sabe** que existe | foco, busca, navegação clara |
| **Descobribilidade** (discoverability) | perceber algo que você **não sabia** que existia | visão periférica, destaque, contexto |

- **Visão focal:** só focamos uma coisa por vez. No experimento do gorila, a maioria não o vê porque está concentrada em contar passes. Não espere que alguém veja o que está fora do foco da tarefa.
- **Cegueira à mudança (change blindness):** uma mudança não é percebida, por exemplo o número do carrinho que muda sem o usuário notar. Uma animação de feedback resolve, como os campos de senha que tremem no site da Apple.
- **Estímulos:**
  - **externos** (bottom-up): cor, peso, posição;
  - **internos** (top-down): o contexto e a expectativa do usuário.

## Gestalt
| Princípio | Use para |
|---|---|
| **Fechamento** | o cérebro completa formas incompletas; ícones e logos simples |
| **Proximidade** | o que está perto parece um grupo; espaçamento define grupos |
| **Região comum** | o que está dentro de uma borda ou fundo parece um grupo |
| **Similaridade** | o que é parecido parece relacionado |
| **Continuidade** | o olho segue linhas e curvas; alinhamento, carrosséis |
| **Destino comum** | o que se move junto parece um grupo |
| **Figura e fundo** | separar o foco do contexto; modais, sobreposições |

## Hierarquia visual: os 5 recursos
**Cor**, **tipografia**, **tamanho**, **posicionamento** e **espaço em branco**. Sinal de problema `[prática]`: tudo com o mesmo peso, ou mais de um elemento disputando ser o principal.

## Memória
- **Curto prazo:** limitada. Não peça para o usuário lembrar algo de uma tela para usar em outra.
- **Evite depender da memória:** autocompletar cupons, SMS, cartão e destinatários. O OTP do iOS é copiado automaticamente.
- **Comparações:** com mais de duas opções, destaque uma (por popularidade ou outro atributo). Isso se apoia na Lei de Hick.

## Familiaridade e curva de aprendizado
- Quanto mais familiar, mais intuitivo.
- **Em redesign,** quem estava acostumado com a versão antiga sente a mudança. Pela *power law of learning*, a nova interface começa lá embaixo na curva de aprendizado enquanto a antiga já estava no topo.
- **Mitigação:** mostre o nome antigo junto do novo durante a transição, como a Amazon fez em menus.
- **Como medir** `[prática]`: o tempo e a taxa de sucesso das tarefas principais logo após o redesign, comparados com as semanas seguintes.

## Pensar é difícil
- Tomamos milhares de decisões por dia, então usamos atalhos, e um deles é aceitar o padrão.
- Um padrão que favorece o negócio contra o usuário não é boa prática. Exemplo: compra recorrente pré-marcada. Passe esses casos para a `behavioral-design`.
- **Escolhas compensatórias × não compensatórias:**
  - **não compensatória:** descartar opções por um atributo negativo (por exemplo, nenhum carro com mais de 5 anos). Ofereça filtros.
  - **compensatória:** pesar os benefícios de cada opção (por exemplo, comparar planos). Ofereça uma comparação lado a lado.

## Efeito estético-usabilidade
- Produtos atraentes são **percebidos** como mais usáveis, e as pessoas toleram pequenos problemas neles.
- Vale investir em estética.
- Num teste, o entusiasmo com a aparência pode esconder problemas. Observe o comportamento, não só a opinião.
