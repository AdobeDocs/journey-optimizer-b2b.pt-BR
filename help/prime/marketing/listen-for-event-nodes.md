---
title: Ouvir um nó de evento
description: Configurar o Listen para nós de evento no Journey Optimizer B2B edition Prime - definir acionadores de evento, aplicar filtros opcionais e avançar as pessoas quando ocorrerem atividades ou alterações de dados.
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d0031543-532c-4a26-8f90-01af2b91e6d0
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# Ouvir um nó de evento

Adicione o nó _Ouvir um evento_ para mover o público-alvo para a próxima etapa da jornada quando ocorrer um evento.

## Acionadores de eventos {#event-triggers}

Obter lista do PM

## Filtros de evento {#event-filters}

Obter lista atualizada do PM

| Filtros | Descrição |
| ------- | ----------- |
| Histórico de atividades > Email | Atividades de email com base nas condições avaliadas usando uma ou mais mensagens de email selecionadas: <li>Clicou em um link no email <li>Email aberto |
| Histórico de atividades > Valor de dados alterado | Para um atributo de pessoa selecionado, ocorreu uma alteração de valor. Esses tipos de alterações incluem: <li>Novo valor <li>Valor anterior <li>Motivo <li>Fonte <li>Data da atividade <li> Número número de vezes |

## Adicionar um nó de evento {#add-event-node}

1. Navegue até a tela de jornada.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

   ![Clique em adicionar ícone no caminho da jornada](./assets/person-journey-canvas-add-node.png){width="200"}

1. Nas propriedades do nó à direita, clique em **[!UICONTROL Adicionar critério de evento]**.

1. Na caixa de diálogo _[!UICONTROL Editar evento]_, adicione os eventos a serem acionados.

   ![Editar evento - acionadores de evento](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** na caixa de diálogo e adicione critérios de filtragem para os acionadores.

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

   ![Editar evento - filtragem de eventos](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>No momento, a funcionalidade de tempo limite do Listen para um nó de evento não funciona. Está planejado para uma versão posterior.
