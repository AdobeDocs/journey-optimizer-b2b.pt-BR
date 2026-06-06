---
title: Nós de público-alvo da conta
description: Configure nós de público-alvo de conta com públicos-alvo de conta ou listas de conta para definir pontos de entrada de jornada para a orquestração direcionada no Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 3%

---


# Nós de jornada de público-alvo da conta

O nó de público-alvo da conta especifica quais contas entram na jornada. Quando você [cria uma jornada de conta](./create-publish-journey.md#create-a-journey), a jornada sempre começa com um nó de público-alvo de conta que define sua entrada.

Use uma das seguintes opções de entrada para este nó do jornada:

* **[Público-alvo da conta](../audiences/account-audience-overview.md)** — O público-alvo da conta representa o público-alvo básico que é sincronizado a partir do Serviço de Segmentação da Experience Platform.
* **[Lista de contas](../accounts/account-lists.md)** — a lista de contas é uma coleção de contas nomeadas que você usa para a orquestração de jornadas direcionadas. Uma lista de contas é direcionada a contas nomeadas usando critérios definidos, como setor, local ou tamanho da empresa.

## Definir o público-alvo para o nó de público-alvo da conta

1. Clique no nó **[!UICONTROL Público-alvo da conta]**. Essa ação exibe as propriedades do nó no painel direito.

   ![Nó de jornada de público-alvo da conta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Escolha o tipo de entrada para contas que entram na jornada:

   * **[!UICONTROL Público-alvo da conta]**

     Escolha a opção de público-alvo da conta. Clique em **[!UICONTROL Adicionar público-alvo da conta]**.

     Na caixa de diálogo _[!UICONTROL Adicionar público-alvo]_, selecione um segmento de público-alvo criado anteriormente. Clique em **[!UICONTROL Adicionar público-alvo]**.

     ![Selecione um segmento de público-alvo para o nó](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Lista de contas]**

     Escolha a opção de lista de contas. Clique em **[!UICONTROL Adicionar lista de contas]**.

     Na caixa de diálogo _[!UICONTROL Selecionar lista de contas ativas]_, selecione uma lista de contas publicadas. Em seguida, clique em **[!UICONTROL Salvar]**.

     ![Selecione uma lista de contas ativas para o nó](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Para obter mais informações sobre como criar e publicar listas de contas, consulte [Listas de contas](../accounts/account-lists.md).

## Criar um segmento de público-alvo

1. Na navegação à esquerda, selecione **[!UICONTROL Contas]** > **[!UICONTROL Públicos]**.

1. Clique em **[!UICONTROL Criar público-alvo]** no canto superior direito.

   ![Criar um segmento de público-alvo](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Siga as etapas no [guia do Serviço de segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.
