---
title: Gerenciamento de jornadas
description: 'Simplifique a geração de demanda com o jornada: crie, publique e gerencie o envolvimento do grupo de compra por email, SMS e eventos no Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 44%

---


# Gerenciamento de jornadas

No Journey Optimizer B2B edition, as jornadas são planos de marketing automatizados, baseados em contas em várias etapas e clientes potenciais, que orquestram experiências personalizadas em todos os canais em resposta a engajamento, eventos comerciais ou campanhas programadas. Defina um envolvimento orientado a vendas que inclua email, SMS e muito mais para coordenar o marketing de entrada com atividades de vendas de saída para cada membro do grupo de compras.

O Journey Optimizer B2B edition é compatível com dois tipos de jornada:

* **jornadas da conta** - Simplifique a geração de demanda e a qualificação do grupo de compras e gere demanda mais qualificada para seus programas de aquisição, venda adicional/venda cruzada e retenção. Personalize suas jornadas para cada grupo de compra e membro do grupo de compra usando engajamento automatizado por email, SMS, eventos e muito mais.

  ![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral da jornada da conta](#overview-video)

* **jornadas de pessoas** - (Beta) Orquestrar o marketing com base em clientes potenciais usando públicos-alvo e dados da Experience Platform. Com jornadas pessoais, suas operações de marketing não dependem do Marketo Engage ou de soluções alternativas para cadeias de ferramentas Adobe Campaign/B2C para que possam trabalhar com casos de uso B2B.

  Quando usada em conjunto com jornadas de conta e grupos de compra, uma jornada de pessoa pode fornecer aos profissionais de marketing o poder de aplicar a orquestração completa à jornada de compra.

  +++Limitações atuais para jornadas de pessoas

  Existem limitações que podem bloquear certos casos de uso ou causar dificuldade para criar jornadas de pessoas. Muitos problemas são resultado da implementação inicial do programa beta, que deverá ser abordada no futuro.

   * Eventos não podem ser combinados com atributos de perfil para restringir as definições de público.
   * O contexto do evento que qualifica um perfil para uma jornada não pode ser usado para personalização ou orquestração.
   * No momento, o Jornada não pode ter um evento e um critério de entrada de segmento de perfil.
   * Os ouvintes de eventos não podem ouvir vários eventos.
   * No momento, os nós de espera não têm um conjunto completo de opções para os critérios de dia da semana ou hora do dia de saída.
   * O editor de email faz referência incorretamente a recursos e atributos que só estão disponíveis para Jornadas de conta
   * O suporte para tokens de jornada personalizados (_Meus tokens_) ainda não está disponível.
   * Adicionar e Remover dos nós de jornada de pessoa não está disponível atualmente em nenhum dos tipos de jornada.
   * O histórico de eventos não pode ser usado para orquestração ou personalização.
   * Objetos relacionados (como conta, grupo de compra, oportunidade e objetos personalizados) não podem ser usados para orquestração ou personalização.
   * No momento, não há suporte para canais de plataforma da Web, SMS e anúncio.

  +++

## Introdução a uma jornada

Para começar com sua primeira jornada:

1. [Crie uma jornada](./create-publish-journey.md#create-a-journey).
1. [Adicione os nós](./create-publish-journey.md#add-a-node) e [defina o fluxo da jornada](./create-publish-journey.md#add-and-delete-a-path) no mapa de jornada.
1. [Publique a jornada](./create-publish-journey.md#publish-a-journey).

## Acessar e navegar pelas jornadas

>[!BEGINTABS]

>[!TAB jornadas da conta]

Na navegação à esquerda, expanda **[!UICONTROL Gerenciamento de Jornadas]** e clique em **[!UICONTROL jornadas de Conta]**.

Insira texto na ferramenta de _pesquisa_ da parte superior da lista para filtrar a lista exibida por nome.

![Filtrar a lista de jornadas da conta](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB jornadas de pessoas (Beta)]

[!BADGE Beta]{type=Informative tooltip="Disponível como um recurso beta na arquitetura simplificada"}

Na navegação à esquerda, expanda **[!UICONTROL Gerenciamento de Jornadas]** e clique em **[!UICONTROL jornadas de pessoas]**.

Insira texto na ferramenta _Search_ na parte superior da lista para filtrar a lista exibida por nome.

![Filtrar a lista de jornadas da pessoa](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Jornada colunas da lista

A página Lista de jornadas inclui as seguintes colunas:

* [!UICONTROL Nome] (clique no nome para abrir a jornada para edição)
* [!UICONTROL Status]
* [!UICONTROL Data de criação]
* [!UICONTROL Criado por]
* [!UICONTROL Última atualização]
* [!UICONTROL Última atualização por]
* [!UICONTROL Publicado em]
* [!UICONTROL Publicado por]
* [!UICONTROL Data de início]
* [!UICONTROL Data final]

Você pode classificar a lista por _[!UICONTROL Status]_, _[!UICONTROL Data de criação]_ ou _[!UICONTROL Última atualização]_ clicando no cabeçalho da coluna.

Para personalizar (mostrar/ocultar) as colunas exibidas na tabela, clique no ícone _Personalizar tabela_ ( ![Personalizar tabela](../assets/do-not-localize/icon-column-settings.svg) ) no canto superior direito. Marque ou desmarque as caixas de seleção na caixa de diálogo e clique em **[!UICONTROL Aplicar]**.

![Escolha as colunas a serem exibidas na lista de jornadas](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Status da jornada

O status de uma jornada pode mudar com base nas ações que você aplica. Com base no status de uma jornada, certas ações estão/não estão disponíveis no lado direito do cabeçalho.

| Status | Descrição | Ações disponíveis |
| ------ | ----------- | ----------------- |
| _&#x200B;**Rascunho**&#x200B;_ | Uma jornada não publicada que é editável. | <li>[Publicar](./create-publish-journey.md#publish-a-journey)<li>[Duplicar](#duplicate-journey) <li>[Excluir](#delete-journey) |
| _&#x200B;**Ativa**&#x200B;_ | O status da jornada muda de _Rascunho_ para _Ao vivo_ quando uma jornada é publicada. Nesse estado, ela não é mais editável. | <li>[Duplicar](#duplicate-journey)<li>[Fechar para novas entradas](#close-to-new-entries) <li>[Abortar](#abort-journey) |
| _&#x200B;**Fechada para novas entradas**&#x200B;_ | O status da jornada muda de _Ativa_ para _Fechada para novas entradas_ quando você clica em [!UICONTROL Fechar para novas entradas] na navegação superior. | <li>[Duplicar](#duplicate-journey) <li>[Cancelar](#abort-journey) |
| _&#x200B;**Abortada**&#x200B;_ | O status muda para _Ativa_ ou _Fechada para novas entradas_ quando você aborta uma jornada. Uma jornada cancelada não pode ser reiniciada. | <li>[Duplicar](#duplicate-journey) <li>[Excluir](#delete-journey) |
| _&#x200B;**Concluída**&#x200B;_ | Quando todos os membros de conta ou público-alvo de pessoa em uma jornada concluírem a jornada, o status mudará de _Ativo_ ou _Fechado para novas entradas_ para _Concluído_. | <li>[Duplicar](#duplicate-journey) <li>[Excluir](#delete-journey) |

## Jornada mapas

Clique no nome (exibido como um link) na lista jornadas para revisar os detalhes, fazer alterações e realizar ações.

![Espaço de trabalho da jornada de conta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

O cabeçalho de cada mapa de jornada inclui:

* Nome da jornada
* Ferramenta de edição para o nome da jornada (![Ícone de edição](../assets/do-not-localize/icon-edit.svg) ícone _Editar_)
* [Status](#journey-status) da jornada

No mapa de jornadas, você pode [Adicionar os nós](./create-publish-journey.md#add-a-node) e [definir o fluxo de jornada](./create-publish-journey.md#add-and-delete-a-path).

## Jornada ações

A página da lista de jornadas inclui todas as jornadas de conta ou pessoa na instância do Journey Optimizer B2B edition. Na página da lista, é possível aplicar várias ações a uma jornada.

### Cancelar jornada

Se você abortar (interromper) uma jornada em tempo real ou programada, as contas ou as pessoas na jornada interromperão imediatamente seu progresso e nenhuma entrada adicional na jornada poderá ocorrer. Uma jornada cancelada não pode ser reiniciada.

>[!IMPORTANT]
>
>Quando a jornada é usada em outra jornada de um nó _Executar uma ação_ com a ação _[!UICONTROL Adicionar conta à (outra) Jornada]_, anular a jornada bloqueia essa ação nessa jornada.

1. Clique no nome da jornada para abri-la.

1. Clique no menu **[!UICONTROL Mais...]** no canto superior direito e escolha **[!UICONTROL Cancelar]**.

   ![Clique em “Mais” no canto superior direito](./assets/account-journey-live-more-menu.png){width="450"}

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Cancelar]**.

### Fechar para novas entradas

Se você fechar uma jornada ativa, as contas que estão atualmente na jornada continuarão seu caminho nessa jornada e nenhuma outra entrada de jornada poderá ocorrer. Uma jornada fechada não pode ser reiniciada. É possível duplicar uma jornada fechada.

>[!IMPORTANT]
>
>Quando a jornada é usada em outra jornada de um nó _Executar uma ação_ com a ação _[!UICONTROL Adicionar conta à (outra) Jornada]_, fechá-la em novas entradas bloqueia essa ação dessa jornada.

1. Clique no nome da jornada para abri-la.

1. Clique no menu **[!UICONTROL Mais...]** no canto superior direito e escolha **[!UICONTROL Fechar para novas entradas]**.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Fechar para novas entradas]**.

### Duplicar uma jornada

Uma ação duplicada é semelhante a uma função de clone, mas uma jornada duplicada não inclui nenhum ativo de conteúdo de jornada criado. Você pode duplicar os detalhes da jornada ou apenas um _esqueleto_ simples da estrutura de fluxo e caminho.

>[!NOTE]
>
>Esta ação não está disponível no momento para jornadas de pessoas.

1. Clique no ícone de _Mais_ (**...**) ao lado do nome da jornada e escolha **[!UICONTROL Duplicar]**.

   ![Clique no ícone ... e escolha Duplicar](./assets/account-journeys-list-more-menu.png){width="450"}

   Dependendo do status da jornada, você também pode acessar a ação duplicar nos detalhes da jornada ou no mapa de jornadas:

   * Para uma jornada de rascunho, clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Duplicar]**.

   * Para todos os outros status de jornada, clique em **[!UICONTROL Duplicar]** na parte superior direita.

     ![Clique em Duplicar na parte superior direita](./assets/account-journey-duplicate-button.png){width="450"}

1. Na caixa de diálogo _Duplicar jornada_, defina o **[!UICONTROL Nome]** e a **[!UICONTROL Descrição]** para a nova jornada.

   Por padrão, a caixa de diálogo usa o nome da jornada duplicada anexada com __cópia_. Insira outro nome exclusivo para a jornada, conforme necessário.

   ![Caixa de diálogo Duplicar jornada](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Selecione o **[!UICONTROL tipo]** de duplicação:

   * **[!UICONTROL Duplicação parcial de conteúdo]**: use este tipo para copiar tudo na jornada, excluindo emails ou mensagens SMS criados. Os nós que fazem referência a um email ou mensagem SMS do Marketo Engage ficam totalmente intactos.

   * **[!UICONTROL Duplicar sem detalhes]**: use esse tipo para copiar apenas a estrutura e os caminhos do nó. Todas as configurações de nó e condições de caminho ficam indefinidas (padrão), de modo que você pode reutilizar o fluxo básico com diferentes configurações de público-alvo, ações e segmentação de caminho. Todos os nós _Wait_ usam o padrão de cinco dias.

1. Clique em **[!UICONTROL Duplicar]**.

   A jornada duplicada é aberta no mapa de jornadas, onde você pode definir os detalhes e criar conteúdo da jornada conforme necessário.

### Excluir uma jornada

Use uma ação de exclusão para excluir uma jornada permanentemente. Não é possível excluir uma jornada ativa ou programada.

1. Clique no ícone _Mais_ (**...**) ao lado do nome da jornada e escolha **[!UICONTROL Excluir]**.

   Dependendo do status da jornada, você também pode acessar a ação de exclusão nos detalhes da jornada ou no mapa de jornadas:

   * Para um rascunho de jornada, clique no menu **[!UICONTROL Mais...]** no canto superior direito e escolha **[!UICONTROL Excluir]**.

   * Para outros status de jornada, como _Concluído_ ou _Cancelado_, clique em **[!UICONTROL Excluir]** no canto superior direito.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

## Revisar progressão da conta

Para uma jornada de conta publicada que esteja em um status _Ativo_, _Fechado para novas entradas_, _Abortado_ ou _Concluído_, você pode abrir o mapa de jornadas para examinar a progressão de conta para os nós de jornada. Cada nó no mapa exibe o número de contas para chegar a esse nó e, para jornadas ativas, o número de contas atualmente nesse nó.

![Informações sobre o progresso da conta do nó da jornada](./assets/node-account-progression-observability.png){width="400"}

Ao selecionar o nó, clique no número para visualizar uma lista de contas que entraram no nó ou que estão atualmente nessa etapa da jornada.

![Informações sobre o progresso da conta do nó da jornada](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Vídeo de visão geral da jornada de conta {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
