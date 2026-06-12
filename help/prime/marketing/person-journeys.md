---
title: Jornadas de pessoas
description: Página de espaço reservado para jornadas de pessoas.
autotag-review: '2026-06-12T23:03:17.139Z'
TQID: 'https://experienceleague.adobe.com/MhkAuypbebo-n9uwxFPUKbNgyHijaTnaVsqhs9-lXC0'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 683
ht-degree: 21%

---

# Jornadas de pessoas

No Journey Optimizer B2B edition Prime, as jornadas pessoais são planos de marketing automatizados com base em clientes potenciais em várias etapas, usando dados do Marketo Engage que orquestram experiências personalizadas em canais em resposta a engajamento, eventos comerciais ou campanhas programadas.

Para começar a usar a jornada em primeira pessoa:

1. Criar uma jornada de pessoa.
1. Adicione os nós e defina o fluxo da jornada no mapa de jornadas.
1. Publique a jornada.

## Acessar e procurar jornadas de pessoas

Na navegação à esquerda, expanda **[!UICONTROL Gerenciamento de marketing]** e selecione **[!UICONTROL jornadas de pessoa]**.

Você pode digitar texto na ferramenta _Pesquisa_ na parte superior da lista para filtrar a lista exibida por nome.

### Jornada colunas da lista

A página Lista de jornadas inclui as seguintes colunas:

Nome (clique no nome para abrir o mapa de jornadas para edição)
Status
Data de criação
Criado por
Última atualização
Última atualização por
Publicado em
Publicado por
Data inicial
Data final

Você pode classificar a lista por Status, Data de criação ou Última atualização clicando no cabeçalho da coluna.

Para personalizar (mostrar/ocultar) as colunas exibidas na tabela, clique no ícone Personalizar tabela ( ) no canto superior direito. Marque ou desmarque as caixas de seleção na caixa de diálogo e clique em Aplicar.

### Status da jornada

O status de uma jornada pode mudar com base nas ações que você aplica. Com base no status de uma jornada, certas ações estão/não estão disponíveis no lado direito do cabeçalho.

| Status | Descrição | Ações disponíveis |
| ------ | ----------- | ----------------- |
| Rascunho | Uma jornada não publicada que é editável. | <li>Publicar <li>Duplicar <li>Excluir |
| Ativo | O status da jornada muda de Rascunho para Em tempo real quando uma jornada é publicada. Nesse estado, ela não é mais editável. | <li>Duplicar |
| Concluído | Quando todos os membros do público-alvo de conta ou pessoa em uma jornada concluírem a jornada, o status mudará de Ativo ou Fechado para novas entradas e concluídas. | <li>Duplicar <li>Excluir |

## Criar uma jornada de pessoa

1. Clique em **[!UICONTROL Criar Jornada]** no canto superior direito da lista de jornadas.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

<!-- 
   ![Create Journey dialog](./assets/person-journey-create-dialog.png){width="400"}
-->

1. Clique em **[!UICONTROL Criar]**.

### Design da jornada

O _mapa de jornadas_ é a zona central no espaço de trabalho de jornada. É aqui que você pode adicionar nós de jornada e configurá-los. Clique em um nó para abrir suas propriedades no painel à direita do layout e defina-as de acordo com seu design. Uma jornada de pessoa sempre começa com um nó _[!UICONTROL Audiência de pessoa]_, onde é possível definir a entrada da jornada.

<!--
   ![Journey map for newly created journey](./assets/person-journey-create-dialog.png){width="400"}
-->

Depois de criar uma jornada de pessoa e adicionar o público-alvo de pessoa, crie a jornada usando nós. O mapa de jornada fornece uma tela, onde você pode criar seus casos de uso de marketing B2B em várias etapas usando os seguintes tipos de nó para criar a jornada:

* [Realizar uma ação](./action-nodes.md)
* [Acompanhar um evento](./listen-for-event-nodes.md)
* [Aguardar](./wait-nodes.md)
* [Dividir caminhos](./split-merge-paths-nodes.md)
* [Próximo caminho recomendado](./next-best-path.md)
* [Mesclar caminhos](./split-merge-paths-nodes.md)


## Gerenciamento de jornadas



## Mapa da jornada

Clique no nome (exibido como um link) na lista jornadas para revisar os detalhes, fazer alterações e realizar ações.

O cabeçalho de cada mapa de jornada inclui:

Nome da jornada
Editar ferramenta para o nome da jornada (ícone Editar)
Status da jornada
No mapa de jornadas, é possível Adicionar os nós e definir o fluxo de jornadas.

### Jornada ações

A página da lista de jornadas inclui todas as jornadas de conta ou pessoa na instância do Journey Optimizer B2B edition. Na página da lista, é possível aplicar várias ações a uma jornada.



#### Duplicar uma jornada

Uma ação duplicada é semelhante a uma função de clone, mas uma jornada duplicada não inclui nenhum ativo de conteúdo de jornada criado. Você pode duplicar os detalhes da jornada ou apenas um esqueleto simples da estrutura de fluxo e caminho.

NOTA

Clique no ícone More (...) ao lado do nome da jornada e escolha Duplicate.

Dependendo do status da jornada, você também pode acessar a ação duplicar nos detalhes da jornada ou no mapa de jornadas:

Para uma jornada de rascunho, clique no menu Mais... na parte superior direita e escolha Duplicar.
Para todos os outros status da jornada, clique em Duplicar na parte superior direita.
Na caixa de diálogo Duplicar Jornada, defina o Nome e a Descrição da nova jornada.
Por padrão, a caixa de diálogo usa o nome da jornada duplicada anexada com _copy. Insira outro nome exclusivo para a jornada, conforme necessário.

Escolha o Tipo de duplicação:
Duplicação parcial de conteúdo - use esse tipo para copiar tudo na jornada, excluindo emails ou mensagens SMS criados. Os nós que fazem referência a um email ou mensagem SMS do Marketo Engage estão totalmente intactos.
Duplicar sem detalhes - Use esse tipo para copiar somente a estrutura e os caminhos do nó. Todas as configurações de nó e condições de caminho são indefinidas (padrão), de modo que você pode reutilizar o fluxo básico com diferentes configurações de público-alvo, ações e segmentação de caminho. Todos os nós de espera usam o padrão de cinco dias.
Clique em Duplicate.
A jornada duplicada é aberta no mapa de jornadas, onde você pode definir os detalhes e criar conteúdo da jornada conforme necessário.

Excluir uma jornada

Use uma ação de exclusão para excluir uma jornada permanentemente. Não é possível excluir uma jornada ativa ou programada.

Clique no ícone Mais (...) ao lado do nome da jornada e escolha Excluir.
Dependendo do status da jornada, você também pode acessar a ação de exclusão nos detalhes da jornada ou no mapa de jornadas:

Para uma jornada de rascunho, clique no menu Mais... na parte superior direita e escolha Excluir.
Para outros status de jornada, como Concluído ou Abortado, clique em Excluir na parte superior direita.
Na caixa de diálogo de confirmação, clique em Excluir.






