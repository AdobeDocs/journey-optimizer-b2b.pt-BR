---
title: Filtros de grupo de compra no Marketo Engage
description: Filtre leads comprando a associação de grupo nas Smart Lists do Marketo Engage com restrições como a pontuação de integridade para otimizar campanhas e a pontuação de lead.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---

# Filtros de grupo de compra no Market Engage

>[!IMPORTANT]
>
>**Descontinuação de recursos**</br></br>
>
>Com a [arquitetura simplificada](../simplified-architecture.md) para o Journey Optimizer B2B edition, os filtros de grupo de compra não estão mais disponíveis em uma instância conectada do Marketo Engage.</br></br>
>
>Como alternativa, você pode criar uma lista estática para cada interesse de solução e, em seguida, [usar a _ação Adicionar à lista do Marketo_](../journeys/action-nodes.md#marketo-engage-actions) de um nó de jornada. Essa ação adiciona membros do grupo de compra a uma lista estática específica em uma instância conectada do Marketo Engage. Em seguida, use a lista estática focada no interesse da solução para um filtro de lista inteligente.

Como profissional de marketing, talvez você queira suprimir campanhas no Marketo Engage para pessoas que fazem parte de grupos de compra no Journey Optimizer B2B edition. Você também pode informar os workflows de pontuação de clientes potenciais no Marketo Engage usando informações sobre os clientes potenciais associados aos grupos de compra. Por exemplo:

* Este cliente em potencial faz parte de um grupo de compras?
* O grupo de compras está completo e envolvido?

Se essas condições forem verdadeiras, você pode optar por pontuar em primeiro lugar. Caso contrário, você pode optar por não marcá-lo como um lead qualificado de marketing (MQL).

Na instância do Marketo Engage que está conectada ao Journey Optimizer B2B edition, você pode usar o filtro _[!UICONTROL Membro do Grupo de Compra]_ nas Smart Lists para identificar esses clientes em potencial de acordo com a estratégia de campanha.

1. Depois de [criar uma Smart List no Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"}, selecione a guia **[!UICONTROL Smart List]** para abrir o editor de filtro.

1. Na lista de filtros à direita, role para baixo na lista e expanda a pasta **[!UICONTROL Filtros especiais]**.

1. Clique no filtro **[!UICONTROL Membro do Grupo de Compras]** e arraste-o para a área de definição de filtro.

   ![Adicionar o filtro Membro do Grupo Comprador à Smart List](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Defina a opção _[!UICONTROL Membro do Grupo de Compras]_ como **[!UICONTROL true]** ou **[!UICONTROL false]**.

   Essa restrição é necessária para a definição.

1. (Opcional) Adicione outras restrições relacionadas ao grupo de compras ao filtro de acordo com como você deseja identificar clientes em potencial para a Smart List.

   * Clique em **[!UICONTROL Adicionar restrição]** na parte superior direita do cartão de filtro.

     ![Selecionar outra restrição](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Selecione a restrição que deseja adicionar, como _Pontuação da integridade_ ou _Interesse na solução_.

   * Defina a avaliação que deseja usar para uma correspondência. Para uma pontuação, você pode usar uma correspondência exata ou um intervalo que esteja acima ou abaixo do número inserido.

     Para um item discreto, como os interesses da solução definidos no Journey Optimizer B2B edition, é possível selecionar um ou mais itens para a lista.

     ![Selecione um valor para a restrição da lista](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Selecione o primeiro e clique no seletor novamente para abrir a caixa de diálogo _[!UICONTROL Seletor de Vários Valores]_.

     ![Selecionar vários valores para a restrição](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Mova qualquer um dos itens restantes para a direita e clique em **[!UICONTROL OK]** quando tiver a lista de itens que deseja usar para a restrição.

   * Repita essas ações para adicionar quantas restrições forem necessárias.

   ![Membro do Filtro de Grupo de Compra com várias restrições](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
