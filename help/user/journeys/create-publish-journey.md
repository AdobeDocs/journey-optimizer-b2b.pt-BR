---
title: Criar e publicar uma Jornada de conta
description: Crie jornadas de conta na tela visual, adicione nós de ação e evento, configure o agendamento e publique para orquestração em tempo real no Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
source-git-commit: a8c2e8e96c5a70032ceba3f0630d1f6c5ae01726
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 4%

---

# Criar e publicar uma jornada de conta

Para começar a usar uma jornada de conta, crie a jornada e construa os nós e o fluxo de jornada no mapa de jornadas.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Criar uma jornada de conta

1. Na navegação à esquerda, clique em **[!UICONTROL Jornadas da conta]**.

1. Clique em **[!UICONTROL Criar Jornada de Conta]** na parte superior direita da página.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

   ![Caixa de diálogo Criar Jornada de Conta](./assets/account-journey-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

## Blocos de construção de uma jornada

O _mapa de jornadas_ é a zona central no espaço de trabalho de jornada. É nessa zona que você pode adicionar nós de jornada e configurá-los. Clique em um nó para abrir o painel de propriedades à direita da tela e defina-o de acordo com seu design. Uma jornada de conta sempre começa com um [nó de Público-alvo de Conta](./account-audience-nodes.md), onde é possível adicionar entrada à jornada.

Depois de criar uma jornada de conta e adicionar o público-alvo, crie a jornada usando nós. O mapa de jornadas fornece uma tela, onde você pode criar seus casos de uso de marketing B2B em várias etapas usando os seguintes tipos de nó para criar uma jornada de conta:

* [Realizar uma ação](./action-nodes.md)
* [Acompanhar um evento](./listen-for-event-nodes.md)
* [Dividir caminhos](./split-merge-paths-nodes.md)
* [Aguardar](./wait-nodes.md)
* [Mesclar caminhos](./split-merge-paths-nodes.md)

## Medidas de proteção

Para ajudar você a criar uma jornada sem encontrar erros, os seguintes painéis de proteção estão em vigor:

* _Excluindo um nó de caminho Split_: a exclusão de um nó requer a exclusão de todos os nós subsequentes em cada caminho.
* _Excluindo um nó de mesclagem_: um nó de mesclagem só pode ser excluído quando há um caminho conectado a ele. Para excluir um nó de mesclagem, deixe apenas um caminho selecionado.
* _Alternância entre conta e pessoas_: alterar a seleção de contas para pessoas exclui todos os nós subsequentes em cada caminho.

## Adicionar um nó

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) no caminho e selecione o tipo de nó.

1. Defina as propriedades do nó à direita.

## Excluir um nó

1. Navegue até o mapa de jornadas.

1. Nas propriedades do nó à direita, clique no ícone _Excluir_ ( ![Ícone Excluir](../assets/do-not-localize/icon-delete.svg) ).

1. Na caixa de diálogo de conformação, clique em **[!UICONTROL Excluir]**.

## Adicionar e excluir um caminho

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) no caminho e adicione o [nó do caminho dividido](./split-merge-paths-nodes.md#split-paths).

1. Nas propriedades do nó à direita, selecione **[!UICONTROL Conta]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]**.

   A cada caminho criado na jornada, um novo cartão de caminho é exibido nas propriedades.

1. Navegue até um dos caminhos na jornada e adicione os nós [ação](./action-nodes.md) ou [evento](./listen-for-event-nodes.md) a esse caminho usando o ícone de adição.

1. Selecione o nó [caminho dividido](./split-merge-paths-nodes.md) para abrir as propriedades à direita.

   Os caminhos que contêm nós não podem ser excluídos.

1. Para excluir esses caminhos, primeiro você deve excluir todos os nós nesse caminho.

## Agendar uma jornada

Ao publicar uma jornada, ela pode começar imediatamente ou em uma data futura programada. A data final pode ser um máximo de três anos a partir da data inicial. Depois que uma jornada for publicada (status _Ao vivo_), você poderá atualizar a data de término da jornada, mas não a data de início.

1. Navegue até o mapa de jornadas.

1. Agende sua jornada clicando em **[!UICONTROL configurações da Jornada]** no cabeçalho.

1. Na caixa de diálogo do, defina as opções de agendamento:

   * Escolha um tipo de agendamento.

     Para ativar a jornada no momento da publicação, escolha **[!UICONTROL Imediatamente]**.

     Para ativar a jornada em uma data futura, escolha **[!UICONTROL Em uma data específica]** e clique no ícone _Calendário_ para selecionar a data.

     ![caixa de diálogo de configurações do Jornada](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Especifique a **[!UICONTROL Data final]** para a jornada. Pode ser um máximo de três anos a partir da data de início (esse campo é necessário para publicar).

1. Clique em **[!UICONTROL Salvar]**.

   Quando estiver pronto para publicar sua jornada, você poderá rever essas configurações quando clicar em _[!UICONTROL Publicar]_.

## Publicar uma jornada de conta

Você pode publicar uma jornada se não houver erros de bloqueador. Quando publicado, o status da jornada muda para _Ativo_. Se a jornada tiver erros, o botão _[!UICONTROL Publicar]_ ficará esmaecido com as informações de conteúdo: `Resolve errors before publishing`.

>[!NOTE]
>
>Após a publicação de uma jornada de conta, ocorre um atraso de até 24 horas para que as contas qualificadas entrem na jornada.

1. Na parte superior direita do mapa de jornadas, clique em **[!UICONTROL Publicar]**.

1. Na caixa de diálogo _[!UICONTROL Revisar configurações da jornada]_, defina as opções de início da jornada.

   Se você já definiu as configurações do jornada para definir um agendamento, revise as configurações.

   Se precisar definir a ativação do jornada, escolha um tipo de agendamento:

   * Para ativar a jornada no momento da publicação, escolha **[!UICONTROL Imediatamente]**.

   * Para ativar a jornada em uma data futura, escolha **[!UICONTROL Em uma data específica]** e clique no ícone _Calendário_ para selecionar a data.

1. Se necessário, especifique a **[!UICONTROL Data final]** para a jornada.

   ![caixa de diálogo de configurações do Jornada](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Pode ser um máximo de três anos a partir da data de início (esse campo é necessário para publicar).

1. Clique em **[!UICONTROL Avançar]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Publicar]**.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
