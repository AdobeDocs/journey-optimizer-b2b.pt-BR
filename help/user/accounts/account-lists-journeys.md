---
title: Usar listas de contas no Jornada
description: Use listas de contas na orquestração do jornada e adicione/remova contas dinamicamente no Journey Optimizer B2B edition.
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e935834c-48b7-43d8-b754-a815196a1b05
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: 2026-03-27T22:29:03.719Z
TQID: https://experienceleague.adobe.com/FokJGxTj7abTN01WCcrVLDEuNLW0oI-i-8z0j-rFBO4
source-git-commit: aa6547c60d1b4c570601b5540d193eff57ec6b86
workflow-type: tm+mt
source-wordcount: 417
ht-degree: 0%

---

# Usar listas de contas no jornada

Há várias maneiras de incorporar listas de contas Ativas (publicadas) nas jornadas de conta.

## Nó de público-alvo da conta

Todas as jornadas de conta começam com um nó [_Audiência da conta_](../journeys/account-audience-nodes.md). Quando você define este nó para usar uma lista de contas, as contas do membro se movem pela jornada quando ela fica ativa (publicada).

1. Selecione a opção **[!UICONTROL Lista de contas]** para o nó _Público-alvo da conta_ inicial.

   ![Selecione a opção de lista de contas para o nó de público-alvo da conta](../journeys/assets/node-audience-account-list.png){width="500"}

1. Clique em **[!UICONTROL Adicionar lista de contas]**.

1. Marque a caixa de seleção da lista de contas e clique em **[!UICONTROL Salvar]**.

   ![Selecione a opção de lista de contas para o nó de público-alvo da conta](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## Executar um nó de ação - Adicionar à conta

**_Somente listas de contas estáticas_**

Em uma jornada de conta, adicione contas a uma lista de contas estática usando o nó [a _Realizar uma Ação_](../journeys/action-nodes.md).

Por exemplo, você tem um caminho de jornada para enviar um email e algumas contas realizam várias ações como resposta. Você considera essa atividade um ponto de qualificação na jornada. Com a qualificação, você deseja adicioná-las a uma lista de contas usada como público-alvo para outra jornada com um fluxo diferente para contas qualificadas.

>[!NOTE]
>
>Se uma conta já estiver na lista quando o nó for executado, a ação será ignorada.

1. Selecione a opção _[!UICONTROL Ação em]_ **[!UICONTROL Contas]**.

1. Para _[!UICONTROL Ação nas contas]_, escolha **[!UICONTROL Adicionar à lista de contas]**.

   ![Selecione Adicionar à lista de contas](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. Para **[!UICONTROL Selecionar lista de contas estáticas em tempo real]**, escolha a lista de contas à qual deseja adicionar contas.

   ![Selecione Adicionar à lista de contas](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## Executar um nó de ação - Remover da conta

**_Somente listas de contas estáticas_**

Em uma jornada de conta, remova contas de uma lista de contas estáticas usando o nó [a _Realizar uma Ação_](../journeys/action-nodes.md).

Por exemplo, você tem um caminho de jornada para enviar um email e algumas contas realizam várias ações como resposta. Você considera essa atividade um ponto de qualificação na jornada. Com essa qualificação, você deseja removê-los de uma lista de contas. Essa lista é usada como público-alvo de outra jornada que envia emails adicionais para que você não duplique suas comunicações de qualificação.

>[!NOTE]
>
>Se uma conta não estiver na lista onde está agendada para remoção, a ação será ignorada.

1. Selecione a opção _[!UICONTROL Ação em]_ **[!UICONTROL Contas]**.

1. Para _[!UICONTROL Ação em contas]_, escolha **[!UICONTROL Remover da lista de contas]**.

   ![Selecione Remover da lista de contas](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. Para **[!UICONTROL Selecionar lista de contas estáticas em tempo real]**, escolha a lista de contas para a qual deseja remover as contas.

   ![Selecione Remover da lista de contas](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}
