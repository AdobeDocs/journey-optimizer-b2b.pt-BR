---
title: Jornada reentrada
description: Controla quando e com que frequência contas ou pessoas podem entrar novamente na mesma jornada de conta ou pessoa.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
autotag-review: '2026-08-14T19:11:15.391Z'
TQID: 'https://experienceleague.adobe.com/BabVdaLaAwER8tEQLOAjChwyy4WI2Cle19-Uu-varIc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 07717d3ba2d67a61e3dcfa4693e2ee2e151e78da
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 1%
---
# Jornada reentrada

Quando você ativa a reentrada para uma jornada, pode controlar quando e com que frequência uma conta ou pessoa pode entrar novamente na mesma jornada. Use as configurações de reentrada para definir critérios, limites e tempos de espera para que as contas ou pessoas se requalifiquem para a jornada de forma controlada.

Uma conta ou pessoa pode se requalificar para uma jornada quando os seguintes itens forem verdadeiros:

* A conta ou pessoa está dentro do número de reentradas permitidas para a jornada.
* A conta ou pessoa atingiu o limite de tempo de espera (o tempo mínimo de espera antes da requalificação).
* A conta ou pessoa não está na jornada.

## Ativar reentrada para uma jornada

Você pode habilitar a reentrada e alterar as configurações de reentrada quando a jornada estiver com o status _Rascunho_.

>[!BEGINTABS]

>[!TAB jornada na conta]

1. Abra a jornada da conta de rascunho.

1. Clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Reinserir]**.

   ![Clique em Mais na parte superior direita de uma jornada de conta](./assets/account-journey-draft-more-menu.png){width="450"}

1. Na caixa de diálogo _[!UICONTROL Reentrada de Jornada]_, alterne a opção **[!UICONTROL Habilitar reentrada]**.

   Quando o recurso está ativado, as opções de tempo, atraso e limites são exibidas.

   ![Caixa de diálogo de reentrada de Jornada para uma jornada de conta com recurso habilitado](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Para **[!UICONTROL Tempo de reentrada]**, escolha como a espera é calculada:

   * **[!UICONTROL Aguardar do fim da jornada]** - O período de espera começa quando a conta sai ou conclui a jornada. Por exemplo, &quot;30 dias depois que a conta concluir a jornada, ela poderá inserir novamente&quot;.

   * **[!UICONTROL Aguardar desde o início da jornada]** - O período de espera se baseia em quando a conta entrou pela primeira vez na jornada. Por exemplo, &quot;30 dias a partir de quando a conta iniciou a jornada, ela pode inserir novamente&quot;.

1. Defina o **[!UICONTROL Atraso de reentrada]**, que é a duração da espera em horas ou dias.

   Essa configuração determina quanto tempo uma conta deve esperar após sair ou iniciar a jornada antes de entrar novamente.

1. Para definir o número máximo de vezes que uma conta pode entrar na jornada, defina o **[!UICONTROL Limite de entradas]**.

   Quando uma conta atinge o limite, ela não se qualifica mais para entrada até que o limite seja redefinido ou a jornada seja republicada com um novo limite.

   Esse limite se aplica por conta para essa jornada.

1. Clique em **[!UICONTROL Salvar]**.

>[!TAB jornada de pessoa]

1. Abra a jornada de pessoa de rascunho.

1. Clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Reinserir configurações]**.

   ![Clique em Mais na parte superior direita de uma jornada de pessoa](./assets/person-journey-draft-more-menu.png){width="450"}

1. Na caixa de diálogo _[!UICONTROL Reentrada de Jornada]_, alterne a opção **[!UICONTROL Habilitar reentrada]**.

   Quando o recurso está ativado, as opções de tempo, atraso e limites são exibidas.

   ![Caixa de diálogo de reentrada de Jornada para uma jornada de pessoa com recurso habilitado](./assets/person-journey-re-entry-dialog.png){width="450"}

1. Para **[!UICONTROL Tempo de reentrada]**, escolha como a espera é calculada:

   * **[!UICONTROL Aguardar desde o fim da jornada]** - O período de espera começa quando a pessoa sai ou conclui a jornada. Por exemplo, &quot;30 dias depois que a pessoa conclui a jornada, ela pode entrar novamente&quot;.

   * **[!UICONTROL Aguardar desde o início da jornada]** - O período de espera se baseia em quando a pessoa entrou na jornada pela primeira vez. Por exemplo, &quot;30 dias a partir de quando a pessoa iniciou a jornada, ela pode entrar novamente&quot;.

1. Defina o **[!UICONTROL Atraso de reentrada]**, que é a duração da espera em horas ou dias.

   Essa configuração determina quanto tempo uma pessoa deve esperar após sair ou iniciar a jornada antes de entrar novamente.

1. Para definir o número máximo de vezes que uma pessoa pode entrar na jornada, defina o **[!UICONTROL Limite de entradas]**.

   Quando uma pessoa atinge o limite, ela não se qualifica mais para entrada até que o limite seja redefinido ou a jornada seja republicada com um novo limite.

   Esse limite se aplica por pessoa para essa jornada.

1. Clique em **[!UICONTROL Salvar]**.

>[!ENDTABS]

## Progressão e atividade

Para uma jornada de conta ou pessoa publicada, a tela de jornada exibe [progressão](./journeys-overview.md#review-account-progression) para os nós de jornada. Cada nó exibe o número de contas ou pessoas que acessam esse nó e, para jornadas ativas, o número atual nesse nó. Cada vez que uma conta ou pessoa entra novamente em uma jornada, ela é contada como uma entrada distinta.

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
