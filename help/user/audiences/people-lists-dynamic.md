---
title: Listas Dinâmicas De Pessoas
description: Defina regras de associação e duplique listas dinâmicas de pessoas no Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%
---

# Listas dinâmicas de pessoas

Uma [lista de pessoas](./people-lists.md) dinâmica é uma coleção de perfis de pessoas definida por regras (filtros). A associação de lista dinâmica é definida usando filtros simples que fazem referência a atributos e atividades de pessoas. A associação é mantida automaticamente à medida que os perfis são qualificados e desqualificados de acordo com a lógica do filtro.

Não é possível adicionar ou remover pessoas individuais de uma lista dinâmica. Para alterar a associação da lista, atualize suas regras. Se você precisar gerenciar a associação manualmente ou por meio de uma jornada, use uma [lista estática](./people-lists-static.md).

## Definir regras de associação {#set-membership-rules}

>[!NOTE]
>
>Uma lista dinâmica sem regras não tem membros. Para preencher a lista, adicione pelo menos um filtro.

1. Abra a lista dinâmica e selecione a guia **[!UICONTROL Regras]**.

1. Clique em **[!UICONTROL Editar regras]**.

   ![Regras de acesso para criar uma lista dinâmica de pessoas](./assets/people-list-dynamic-rules-edit.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Editar regras]_, defina as regras para perfis qualificados arrastando os filtros do painel esquerdo.

   Qualificar perfis para a lista usando qualquer combinação de:

   * Histórico de atividades
   * [!DNL Experience Platform] campos de pessoa habilitados
   * Campos personalizados
   * Dados de intenção
   * Atributos da pessoa
   * Filtros especiais, como associação de jornada

   Para cada filtro adicionado, clique em **[!UICONTROL Adicionar restrições]** para refinar os critérios de correspondência. Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você pode optar por corresponder todas as condições, qualquer condição ou definir a lógica avançada.

   ![Adicionar filtros com restrições para popular a lista dinâmica](./assets/people-list-dynamic-rules-edit-filter.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Concluído]** para salvar suas alterações.

   A guia **[!UICONTROL Regras]** exibe os filtros e a lógica de filtro da lista, e a guia **[!UICONTROL Membros]** é atualizada para refletir a associação atualizada. Para encontrar as qualificações de público mais atualizadas, use **[!UICONTROL Atualizar membros]** no menu **[!UICONTROL Mais]**.

1. Selecione a guia **[!UICONTROL Membros]**.

   Os membros qualificados aparecem na lista após um breve atraso.

   ![Membros gerados para uma lista dinâmica de pessoas](./assets/people-list-dynamic-members.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Para alterar as regras da lista a qualquer momento, repita essas etapas. A lista de associação é atualizada com base nos filtros salvos.

<!--

## Duplicate a dynamic list {#duplicate-dynamic-list}

Duplicating a dynamic list replicates its membership filtering so that you can reuse it in a different context.

1. In the _[!UICONTROL Dynamic lists]_ tab, click the _More menu_ ( **...** ) icon next to the list and choose **[!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Name]** (required) and a **[!UICONTROL Description]** (optional).

   By default, the dialog appends `_copy` to the name of the originating list. Enter a different unique name as needed.

   ![Duplicate list dialog](./assets/people-list-duplicate-dialog.png){width="375"}

1. Click **[!UICONTROL Duplicate]**.
-->
