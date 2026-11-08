# Componentes

Todo o conteúdo vem de `[pós: M13: Botões; Formulários – Princípios e Aplicações; Componentes – Elementos de controle, Imagens, Overlays, Itens de visualização]`, apoiado no Material Design e na Apple HIG. As exceções estão marcadas.

## Botões
**Estados:** padrão, hover, foco, pressionado, desativado, carregando. Todos fazem parte do guia de estilos.

| Faça | Por quê |
|---|---|
| Texto numa só linha | ler e escanear mais rápido |
| Diferencie **principal** e **secundário** | menos carga cognitiva; ação assertiva |
| Texto que diz o que acontece, por exemplo "Finalizar pedido por R$ 70,00" | o usuário sabe o resultado e o custo |
| Tamanho adequado à largura do dispositivo | alvo de toque (ver `ui-accessibility`) |
| Posição que o usuário espera (Lei de Jakob) | ninguém procura |
| Ações diferentes com cores diferentes | evita ação errada |
| Indicador de atividade no próprio botão quando a ação demora | feedback sem gastar espaço |
| Texto extra abaixo do rótulo só se for útil | não poluir |

## Formulários
**Por que melhorar:** economiza tempo, aumenta a conversão (cada campo a mais aumenta o abandono) e cumpre o objetivo de negócio, pedindo **só o necessário, no momento certo**.

**"O melhor formulário é nenhum formulário"**
- Use o que já se sabe: autocompletar, OTP copiado automaticamente, dados do dispositivo.
- Adie o cadastro (o botão de US$ 300 milhões da Amazon).

**Princípios dos campos (Material)**
- **Descobrível:** o campo parece um campo, sem precisar de explicação.
- **Claro:** os estados são bem distintos.
- **Eficiente:** facilita entender o que se pede e corrigir erros.
- O campo pode ser contornado ou preenchido; o importante é mostrar a dimensão do que se espera.

**Tipos**
| Tipo | Quando |
|---|---|
| **Linear** | sequência lógica de campos. Se for longo, divida em etapas |
| **Por etapas** | mostra os campos aos poucos. **Exiba o progresso** para gerenciar a expectativa |
| **Que não parece formulário** | frases com lacunas, seleção visual (o antigo site da Gol) |

**Dicas**
- Peça só o que vai usar. CPF e RG apenas com respaldo jurídico (ver `research-studies/etica-e-dados.md`).
- Rótulo visível; erro junto ao campo, com texto e ícone; formato flexível (Lei de Postel) `[prática]`.

## Overlays
| Componente | Use para | Cuidado |
|---|---|---|
| **Caixa de diálogo** | pergunta que precisa de resposta imediata, com fundo escurecido | não interromper sem necessidade; ações claras |
| **Tooltip** | ajuda pontual no hover ou foco | não esconder informação essencial nele |
| **Toast / snackbar** | feedback rápido, sem interromper o fluxo | não usar para erro que exige ação |
| **Action sheet** (iOS) / menus (Android) | ações sobre um item | seguir a convenção da plataforma |

## Itens de visualização
- Badges, tags e chips; pins de mapa; tabelas; divisores, intermediários e com subcabeçalho; listas; cards; galeria; acordeão; banner; carrossel.
- **Skeleton:** para carregamento gradual. Se a espera passar de **5 a 10 segundos**, use um indicador animado que explique a demora.

## Imagens
- **Hero, thumbnail, avatar:** defina a proporção e o comportamento de corte no DS `[prática]`.
- Texto alternativo segue a `ui-accessibility`.

## Animações (tendências)
- Evite excesso de repetição; não mostre a mesma animação várias vezes ao mesmo usuário (inclusive no scroll); use a velocidade certa.
- **Personalizar:** o sistema faz o esforço pelo usuário ("Não me faça pensar", de Steve Krug).
- **Customizar:** o usuário ajusta.
