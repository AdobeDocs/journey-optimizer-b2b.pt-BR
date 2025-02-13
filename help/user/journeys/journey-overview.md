---
title: Jornadas da conta
description: Saiba mais sobre jornadas de conta e como criá-las e gerenciá-las.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---


# Jornadas da conta

Crie e execute jornadas personalizadas para cada grupo de compra e membro do grupo de compra usando o envolvimento automatizado por email, SMS, eventos e muito mais. Com as jornadas de conta, você pode dinamizar a geração de demanda e a qualificação do grupo de compras, além de impulsionar a demanda mais qualificada para seus programas de aquisição, venda adicional/venda cruzada e retenção.

Defina um envolvimento orientado a vendas que inclua email, SMS e muito mais jornadas de conta interna para coordenar o marketing de entrada com atividades de vendas de saída para cada membro do grupo de compras.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Acessar e procurar jornadas da conta

1. Na página inicial do Adobe Experience Platform, clique em Adobe Journey Optimizer B2B edition.

1. Na navegação à esquerda, clique em **[!UICONTROL jornadas da conta]**.

   ![Acessar jornadas da conta](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   A página jornadas exibida inclui as seguintes colunas:

   * [!UICONTROL Nome] (clique no nome para abrir a jornada de conta para edição)
   * [!UICONTROL Status]
   * [!UICONTROL Descrição]
   * [!UICONTROL Criado por]
   * [!UICONTROL Última atualização às]
   * [!UICONTROL Última atualização por]
   * [!UICONTROL Publicado em]
   * [!UICONTROL Publicado por]

Esta tabela inclui a capacidade de pesquisar por Nome e Criado por. A classificação não está disponível no momento.

Você pode personalizar a tabela exibida ao clicar no ícone _Colunas_ no canto superior direito e marcar ou desmarcar as caixas de seleção.

![Escolha as colunas a serem exibidas na lista de jornadas da conta](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomia de uma jornada de conta

Clique no nome (exibido como um link) na lista _[!UICONTROL jornadas da conta]_ para examinar os detalhes, fazer alterações e realizar ações.

![Espaço de trabalho de jornada de conta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

O cabeçalho do editor de cada jornada de conta inclui:

* Nome da jornada
* Capacidade de editar o nome (_ícone Editar_)
* Status da jornada

As seguintes ações estão disponíveis no cabeçalho:

* **Publicar** - Você pode publicar uma jornada se não houver erros de bloqueador. Quando publicado, o status da jornada muda para _Live_. Se a jornada tiver erros, o botão ficará esmaecido com informações de conteúdo: `Resolve errors before publishing`.
* **Duplicar** - Esta ação é semelhante a uma função de clone, mas a jornada duplicada não inclui nenhum ativo.
* **Fechar para novas entradas** - Se você fechar uma jornada, as contas que estão atualmente na jornada continuarão seu caminho na jornada e não poderá ocorrer mais nenhuma entrada na jornada. Uma jornada fechada não pode ser reiniciada. É possível duplicar uma jornada fechada.
* **Abortar** - Se você parar uma jornada, as contas na jornada pararão imediatamente seu progresso e não poderá ocorrer mais nenhuma entrada na jornada. Uma jornada interrompida não pode ser reiniciada. Se você bloquear novas entradas sem interromper o progresso das pessoas, considere fechar a jornada.
* **Excluir** - Esta ação exclui permanentemente a jornada.

O status de uma Jornada muda com base nas ações que você aplica. Com base no status de uma jornada, determinadas ações não estão disponíveis no cabeçalho.

| Status | Descrição | Ações disponíveis |
| ------ | ----------- | ----------------- |
| _**Rascunho**_ | Uma jornada não publicada que é editável. | <ul><li>Publicar</li><li>Duplicar </li><li>Excluir </li></ul> |
| _**Ao vivo**_ | O status da jornada muda de Rascunho para Em tempo real quando uma jornada é publicada. Nesse estado, ele não é mais editável. | <ul><li>Duplicar </li><li>Fechar para novas entradas </li><li>Anular </li></ul> |
| _**Fechadas para novas entradas**_ | O status da jornada muda de _Ativo_ para _Fechado para novas entradas_ quando você clica em [!UICONTROL Fechar para novas entradas] na navegação superior. | <ul><li>Duplicar </li><li>Anular </li></ul> |
| _**Anulado**_ | O status da jornada muda de _Ativo_ ou _Fechado para novas entradas_ quando você anula uma jornada. Uma jornada anulada não pode ser reiniciada. | <ul><li>Duplicar </li><li>Excluir </li></ul> |
| _**Concluído**_ | Quando todas as contas em uma jornada concluem a jornada, o status muda de Ativo ou Fechado para novas entradas e muda para Concluído. | <ul><li>Duplicar </li><li>Excluir </li></ul> |

## Introdução a uma jornada

Para começar a usar jornadas de conta:

1. [Criar uma jornada](./create-publish-journey.md#create-an-account-journey).
1. [Adicione os nós](./create-publish-journey.md#add-a-node) e [defina o fluxo de jornadas](./create-publish-journey.md#add-and-delete-a-path) no mapa de jornadas.
1. [Publicar a jornada](./create-publish-journey.md#publish-an-account-journey).

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
