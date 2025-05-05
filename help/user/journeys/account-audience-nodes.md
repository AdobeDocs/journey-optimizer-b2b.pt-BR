---
title: Nós de público-alvo da conta
description: Saiba mais sobre o tipo de nó de público-alvo da conta que você pode usar para definir a entrada das suas jornadas de conta no Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 5ed7e58b7a069c8b436d0d2f7b338072259768be
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Nós de jornada de público-alvo da conta

O nó Account audience define as contas de entrada para a jornada. Quando você [cria uma jornada de conta](./journey-overview.md#create-an-account-journey), ela sempre começa com um nó _Público-alvo de conta_ que define a entrada para a jornada.

Há dois tipos de entrada que você pode usar para esse nó:

* **[Público-alvo da conta](../audiences/account-audience-overview.md)** - É o público-alvo básico que é sincronizado do Serviço de Segmentação da Experience Platform.
* **[Lista de contas](../accounts/account-lists.md)** - esta é uma coleção de contas nomeadas que você pode usar para a orquestração de jornadas direcionadas. Uma lista de contas é direcionada a contas nomeadas de acordo com os critérios definidos, como setor, local ou tamanho da empresa.

_Para definir a audiência do nó:_

1. Clique no nó **[!UICONTROL Account audience]** para exibir as propriedades do nó à direita.

   ![Nó de público-alvo da conta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Escolha o tipo de entrada para as contas a serem informadas na jornada:

   * **[!UICONTROL Público-alvo da conta]**

     Escolha esse tipo e clique em **[!UICONTROL Adicionar público-alvo da conta]**.

     Na caixa de diálogo _[!UICONTROL Adicionar público-alvo]_, selecione um segmento de público-alvo criado anteriormente e clique em **[!UICONTROL Adicionar público-alvo]**.

     ![Selecione um segmento de público-alvo para o nó](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Lista de contas]**

     Escolha este tipo e clique em **[!UICONTROL Adicionar lista de contas]**.

     Na caixa de diálogo _[!UICONTROL Selecionar lista de contas ativas]_, selecione uma lista de contas publicada anteriormente e clique em **[!UICONTROL Salvar]**.

     ![Selecione uma lista de contas ativas para o nó](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Vá para [Listas de Contas](../accounts/account-lists.md) para obter informações detalhadas sobre como criar e publicar listas de contas.

_Para criar um segmento de público-alvo:_

1. Na navegação à esquerda, escolha **[!UICONTROL Contas]** > **[!UICONTROL Públicos-alvo]**.

1. Clique em **[!UICONTROL Criar público-alvo]** na parte superior direita.

   ![Criar um segmento de público-alvo](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Siga as etapas descritas no [guia do Serviço de Segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.
