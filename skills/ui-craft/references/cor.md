# Cor

Todo o conteúdo vem de `[pós: M13: Cores – Princípios; Teoria e Acessibilidade; Aplicações em produtos]`, que segue o Material Design e o guia da Apple. As exceções estão marcadas.

## Os 3 princípios (Material Design)
- **Hierarquia:** o mais importante se destaca mais. A cor indica o que é interativo e o nível de destaque. Por exemplo, título em preto e subtítulo em cinza; CTA com uma cor que se diferencia do resto.
- **Legibilidade:** o texto e os elementos precisam ser legíveis sobre o fundo. Verifique com a `ui-accessibility`.
- **Expressividade:** a cor expressa a marca.

## Estrutura de um tema
Os papéis de cor são:
- primária e secundária;
- superfície, fundo e erro;
- as cores **"on"**, usadas em texto e ícones **sobre** cada uma das anteriores;
- os swatches, com as variações de tom.

Tenha um tema claro e um escuro.

## Distribuição
- **60-30-10:** 60% para a cor dominante, 30% para a secundária e 10% para o destaque. Não é uma regra rígida, mas ajuda.
- **No máximo 3 cores na paleta:** dominante, secundária e uma para a ação. Alertas e CTAs podem variar.
- **Contraste guia o olhar.** Use-o para tirar os elementos da similaridade.

## Dark theme
- **Escureça com cinza** (não com preto puro). Use cor só em detalhes. O dark theme economiza energia e ajuda pessoas com baixa visão.
- **Cores dessaturadas:** no fundo claro a primária fica no tom 600; no escuro, no tom 200. Cores saturadas "vibram" e não passam no contraste.
- **Contraste:** o fundo precisa ser escuro o bastante para dar **≥ 15,8:1** com o texto branco. Isso garante **4,5:1** na superfície mais elevada (24dp).
- **Elevação em dark:** superfícies mais altas ficam mais claras.
- **Estados** (desativado, foco, erro) também precisam ser testados no tema escuro.

## Significado e cultura
- **A mesma cor tem significados diferentes em cada cultura.** Exemplo: a cor do luto. Consulte o "Colours in Cultures" (Information is Beautiful).
- **O vermelho, conforme o contexto,** pode significar luxo, violência, perigo ou saúde.
- **Cores quentes** (vermelho, laranja, amarelo) passam calor e chamam a atenção. **Cores frias** (verde, roxo) passam calma. **Neutras** servem de base.
- **Ação destrutiva:** o vermelho é o esperado. Se a marca impõe outra cor (o exemplo do Spotify), compense com ícone, texto e confirmação.

## O "checklist secreto" das cores
1. Tudo bem usar as cores que o cliente quer, desde que passem a mensagem certa.
2. A mesma cor muda de sentido com a cultura.
3. Confira o significado do vermelho no contexto.
4. Distribua as cores (60-30-10).
5. Lembre da acessibilidade: cerca de 8,5% dos homens têm daltonismo, então a cor nunca vai sozinha. Reforce com texto e ícone.

## Harmonias e ferramentas
- **Harmonias:** triádica, complementar, complementar dividida, dupla complementar, quadrado, composta.
- **Modelos de cor:** HSB, HEX e RGB.
- **Ferramentas:**
  - para paletas: Adobe Color, Coolors, Colors.lol;
  - para inspiração: Mobbin, Evernote.design, Dribbble;
  - para contraste: Able, Whocanuse, Color Review.
- **Guias de referência:** Primer (GitHub), Atlassian, Adele (repositório de design systems), IBM.
