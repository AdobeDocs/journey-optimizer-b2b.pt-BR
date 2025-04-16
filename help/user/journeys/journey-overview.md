---
title: Jornadas da conta
description: Saiba mais sobre jornadas de conta e como criá-las e gerenciá-las.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 08c8684d138005d4560941c7d89d6771472bcd60
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 29%

---


# Jornadas de conta

Com as jornadas da conta, você pode dinamizar a geração de demanda e a qualificação do grupo de compra e impulsionar a demanda mais qualificada para seus programas de aquisição, venda adicional/venda cruzada e retenção. Personalize suas jornadas para cada grupo de compra e membro do grupo de compra usando o envolvimento automatizado em email, SMS, eventos e muito mais.

Defina um engajamento orientado a vendas que inclua email, SMS e mais jornadas de conta interna para coordenar o marketing de entrada com atividades de vendas de saída para cada membro do grupo de compra.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Introdução a uma jornada

Para começar a usar jornadas de conta:

1. [Crie uma jornada](./create-publish-journey.md#create-an-account-journey).
1. [Adicione os nós](./create-publish-journey.md#add-a-node) e [defina o fluxo da jornada](./create-publish-journey.md#add-and-delete-a-path) no mapa de jornada.
1. [Publique a jornada](./create-publish-journey.md#publish-an-account-journey).

## Acessar e procurar jornadas de conta

Na navegação à esquerda, clique em **[!UICONTROL Jornadas da conta]**.

![Acessar jornadas de conta](./assets/account-journey-browse.png){width="800" zoomable="yes"}

A página de jornadas exibida inclui as seguintes colunas:

* [!UICONTROL Nome] (clique no nome para abrir a jornada para edição)
* [!UICONTROL Status]
* [!UICONTROL Descrição]
* [!UICONTROL Criado por]
* [!UICONTROL Última atualização em]
* [!UICONTROL Última atualização por]
* [!UICONTROL Publicado em]
* [!UICONTROL Publicado por]

Use a ferramenta _Pesquisa_ na parte superior para localizar a jornada por nome. Você pode classificar a lista por _[!UICONTROL Status]_ clicando no cabeçalho da coluna.

Você pode personalizar as colunas exibidas na tabela clicando no ícone _Personalizar tabela_ ( ![Personalizar tabela](../assets/do-not-localize/icon-column-settings.svg) ) no canto superior direito. Marque ou desmarque as caixas de seleção na caixa de diálogo e clique em **[!UICONTROL Aplicar]**.

![Escolha as colunas a serem exibidas na lista de jornadas de conta](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomia de uma jornada de conta

Clique no nome (exibido como um link) na lista de _[!UICONTROL jornadas de conta]_ para consultar os detalhes, fazer alterações e realizar ações.

![Espaço de trabalho da jornada de conta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

O cabeçalho de cada mapa de jornada de conta inclui:

* Nome da jornada
* Acesso para editar o nome da jornada (ícone ![Editar](../assets/do-not-localize/icon-edit.svg) _Editar_)
* Status da jornada

O status de uma jornada pode ser alterado com base nas ações aplicadas. Com base no status de uma jornada, determinadas ações não estão disponíveis no lado direito do cabeçalho.

| Status | Descrição | Ações disponíveis |
| ------ | ----------- | ----------------- |
| _**Rascunho**_ | Uma jornada não publicada que é editável. | <ul><li>[Publicar](./create-publish-journey.md#publish-an-account-journey)</li><li>Duplicar </li><li>Excluir </li></ul> |
| _**Ativa**_ | O status da jornada muda de Rascunho para Ativa quando ela é publicada. Nesse estado, ela não é mais editável. | <ul><li>Duplicar </li><li>Fechar para novas entradas </li><li>Abortar </li></ul> |
| _**Fechada para novas entradas**_ | O status da jornada muda de _Ativa_ para _Fechada para novas entradas_ quando você clica em [!UICONTROL Fechar para novas entradas] na navegação superior. | <ul><li>Duplicar </li><li>Abortar </li></ul> |
| _**Abortada**_ | O status muda para _Ativa_ ou _Fechada para novas entradas_ quando você aborta uma jornada. Uma jornada abortada não pode ser reiniciada. | <ul><li>Duplicar </li><li>Excluir </li></ul> |
| _**Concluída**_ | Quando todas as contas em uma jornada concluem a jornada, o status muda de Ativa ou Fechada para novas entradas para Concluída. | <ul><li>Duplicar </li><li>Excluir </li></ul> |

## Gerenciar jornadas

A lista _Jornadas da conta_ inclui todas as jornadas da sua instância do Journey Optimizer B2B edition.

### Anular jornada

Se você abortar (interromper) uma jornada em tempo real ou programada, as contas na jornada interromperão imediatamente o progresso e não poderá ocorrer mais nenhuma entrada na jornada. Uma jornada abortada não pode ser reiniciada.

>[!IMPORTANT]
>
>Quando a jornada da conta é usada em outra jornada de um nó _Executar uma ação_ com a ação _Adicionar conta à (outra) Jornada_, a anulação da jornada bloqueia essa ação dessa jornada.

1. Clique no nome da jornada para abri-la.

1. Clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Anular]**.

   ![Clique em Mais no canto superior direito](./assets/account-journey-live-more-menu.png){width="450"}

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Abortar]**.

### Fechar para novas entradas

Se você fechar uma jornada em tempo real, as contas que estão atualmente na jornada continuarão seu caminho nessa jornada e nenhuma outra entrada de jornada poderá ocorrer. Uma jornada fechada não pode ser reiniciada. É possível duplicar uma jornada fechada.

>[!IMPORTANT]
>
>Quando a jornada de conta é usada em outra jornada de um nó _Executar uma ação_ com a ação _Adicionar conta à (outra) Jornada_, fechá-la em novas entradas bloqueia essa ação a partir dessa jornada.

1. Clique no nome da jornada para abri-la.

1. Clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Fechar para novas entradas]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Fechar para novas entradas]**.

### Duplicar jornada

Uma ação duplicada é semelhante a uma função de clone, mas uma jornada duplicada não inclui ativos de conteúdo de jornada criados. Você pode duplicar os detalhes da jornada da conta ou apenas um _esqueleto_ simples das estruturas de fluxo e caminho

1. Clique no ícone _Mais_ (**...**) ao lado do nome da jornada e escolha **[!UICONTROL Duplicar]**.

   ![Clique no ... ícone e escolha Duplicar](./assets/account-journeys-list-more-menu.png){width="450"}

   Dependendo do status da jornada da conta, você também pode acessar a ação duplicar nos detalhes da jornada ou no mapa de jornadas:

   * Para uma jornada de rascunho, clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Duplicar]**.

   * Para todos os outros status de jornada, clique em **[!UICONTROL Duplicar]** na parte superior direita.

     ![Clique em Duplicar na parte superior direita](./assets/account-journey-duplicate-button.png){width="450"}

1. Na caixa de diálogo _Duplicar Jornada_, defina o **[!UICONTROL Nome]** e a **[!UICONTROL Descrição]** para a nova jornada.

   Por padrão, a caixa de diálogo usa o nome da jornada duplicada anexada com __cópia_. Insira outro nome exclusivo para a jornada, conforme necessário.

   ![Caixa de diálogo de Jornada duplicada](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Escolha o **[!UICONTROL Tipo]** de duplicação:

   * **[!UICONTROL Duplicação parcial de conteúdo]** - Use esse tipo para copiar tudo na jornada, excluindo todos os emails ou mensagens SMS criados. Os nós que fazem referência a um email ou mensagem SMS do Marketo Engage estão totalmente intactos.

   * **[!UICONTROL Duplicar sem detalhes]** - Use esse tipo para copiar apenas a estrutura e os caminhos do nó. Todas as configurações de nó e condições de caminho são indefinidas (padrão), de modo que você pode reutilizar o fluxo básico com diferentes configurações de público-alvo, ações e segmentação de caminho. Todos os nós _Wait_ usam o padrão de cinco dias.

1. Clique em **[!UICONTROL Duplicar]**.

   A jornada de conta duplicada é aberta no mapa de jornadas, onde você pode definir os detalhes e criar conteúdo da jornada conforme necessário.

### Excluir jornada

Use uma ação de exclusão para excluir uma jornada permanentemente. Não é possível excluir uma jornada ativa ou programada.

1. Clique no ícone _Mais_ (**...**) ao lado do nome da jornada e escolha **[!UICONTROL Excluir]**.

   Dependendo do status da jornada da conta, você também pode acessar a ação de exclusão nos detalhes da jornada ou no mapa de jornada:

   * Para uma jornada de rascunho, clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Excluir]**.

   * Para outros status de jornada, como _Concluído_ ou _Anulado_, clique em **[!UICONTROL Excluir]** na parte superior direita.

1. No diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
