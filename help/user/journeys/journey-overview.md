---
title: Jornadas da conta
description: Saiba mais sobre jornadas de conta e como criá-las e gerenciá-las.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---


# Jornadas da conta

Defina um envolvimento orientado a vendas que inclua email, SMS e muito mais jornadas de conta interna para coordenar o marketing de entrada com atividades de vendas de saída para cada membro do grupo de compras.

## Acessar e procurar jornadas da conta

1. Na página inicial do Adobe Experience Platform, clique em Adobe Journey Optimizer B2B Edition.

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

* **Publish** - Você pode publicar uma jornada se não houver erros de bloqueador. Quando publicado, um status de Jornada é alterado para _Live_. Se a jornada tiver erros, o botão ficará esmaecido com informações de conteúdo: `Resolve errors before publishing`.
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

Para começar a usar uma jornada de conta, crie a jornada e construa os nós e o fluxo da jornada no editor de jornadas.

### Criar uma jornada de conta

1. Na navegação à esquerda, clique em **[!UICONTROL jornadas da conta]**.

1. Clique em **[!UICONTROL Criar Jornada de Conta]** na parte superior direita da página.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

   ![Caixa de diálogo Criar Jornada de Conta](./assets/account-journey-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

### Adicionar o público-alvo da conta para a sua jornada

Uma jornada de conta sempre começa com o Público-alvo da conta, onde é possível adicionar entradas à jornada.

1. Clique no nó **[!UICONTROL Account audience]** para exibir as propriedades do nó à direita.

   ![Nó de público-alvo da conta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar público da conta]**.

   Você pode selecionar um segmento de público selecionado anteriormente clicando em _[!UICONTROL Adicionar públicos-alvo]_.

1. Para criar um novo segmento de público, selecione **[!UICONTROL Públicos-alvo da conta]** na navegação à esquerda.

1. Clique em **[!UICONTROL Criar público-alvo]** e siga as etapas descritas no [guia do Serviço de Segmentação](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.

### Blocos de construção de uma jornada

A _tela de jornada_ é a zona central no designer de jornada. É nessa zona que você pode adicionar nós de jornada e configurá-los. Clique em um nó para abrir o painel de propriedades à direita da tela e defina-o de acordo com seu design.

Você pode criar a jornada usando qualquer um destes tipos de nó:

* [Ouvir um evento](journey-nodes.md#listen-for-an-event)
* [Realizar uma ação](journey-nodes.md#take-an-action)
* [Dividir caminhos](journey-nodes.md#split-paths)
* [Aguardar](journey-nodes.md#wait)
* [Caminhos de mesclagem](journey-nodes.md#merge-paths)

### Trilhos de proteção

Para ajudar você a criar uma jornada sem encontrar erros, os seguintes painéis de proteção estão em vigor:

* _Excluindo um nó de caminho Split_: não é possível excluir um nó sem excluir todos os nós subsequentes em cada caminho.
* _Excluindo um nó de mesclagem_: um nó de mesclagem só pode ser excluído quando há um caminho conectado a ele. Para excluir um nó de mesclagem, deixe apenas um caminho selecionado.
* _Alternando entre conta e pessoas_: não é possível alterar a seleção de contas para pessoas sem excluir todos os nós subsequentes em cada caminho.

### Adicionar um nó

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) no caminho e selecione o tipo de nó.

1. Defina as propriedades do nó à direita.

### Excluir um nó

1. Navegue até o editor de jornadas.

1. Nas propriedades do nó à direita, clique no ícone _Excluir_ (lixeira).

1. Na caixa de diálogo de conformação, clique em **[!UICONTROL Excluir]**.

### Adicionar e excluir um caminho

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) no caminho e adicione o nó do caminho dividido.

1. Nas propriedades do nó à direita, selecione **[!UICONTROL Conta]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]**.

   A cada caminho criado na jornada, um novo cartão de caminho é exibido nas propriedades.

1. Navegue até um dos caminhos na jornada e adicione os nós de ação ou evento a esse caminho usando o ícone de adição.

1. Selecione o nó do caminho dividido para abrir as propriedades à direita.

   Observe que os caminhos que têm nós não podem ser excluídos.

1. Para excluir esses caminhos, primeiro você deve excluir todos os nós nesse caminho.

### Agendar uma jornada

Ao publicar uma jornada, ela pode começar imediatamente ou em uma data futura programada. A data final pode ser um máximo de três anos a partir da data inicial. Depois que uma jornada for publicada (status _Ao vivo_), você poderá atualizar a data de término da jornada, mas não a data de início.

1. Navegue até o editor de jornadas.

1. Agende sua jornada clicando em [!UICONTROL configurações da Jornada] no cabeçalho.

1. Na caixa de diálogo do, defina as opções de agendamento:

   * Escolha um tipo de cronograma.

     Para ativar a jornada no momento da publicação, escolha **[!UICONTROL Imediatamente]**.

     Para ativar a jornada em uma data futura, escolha **[!UICONTROL Em uma data específica]** e clique no ícone _Calendário_ para selecionar a data.

     ![caixa de diálogo de configurações do Jornada](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Especifique a **[!UICONTROL Data final]** para a jornada. Pode ser no máximo três anos a partir da data de início (este campo é obrigatório).

1. Clique em **[!UICONTROL Salvar]**.

   Quando estiver pronto para publicar sua jornada, você poderá rever essas configurações quando clicar em _[!UICONTROL Publish]_.
