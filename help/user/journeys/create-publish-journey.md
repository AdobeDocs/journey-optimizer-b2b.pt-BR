---
title: Criar e publicar uma Jornada
description: Crie jornadas de conta e pessoa na tela visual, adicione nós de ação e evento, configure o agendamento e publique para orquestração em tempo real no Journey Optimizer B2B Edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
autotag-review: 2026-03-30T23:14:46.843Z
TQID: 'https://experienceleague.adobe.com/-emMaxlrae40JXP0tThacD3xA27d5OzO8tX6o-mOnfg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 9d5641659907d61be992ed218088a023a5211c56
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 5%
---
# Criar e publicar uma jornada

Para iniciar uma nova jornada, crie a jornada e construa os nós e o fluxo da jornada no mapa de jornadas.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Criar uma jornada

Em **[!UICONTROL Gerenciamento de Jornadas]**, na navegação à esquerda, selecione o tipo de jornada que deseja criar:

* **[!UICONTROL jornadas da conta]**
* **[!UICONTROL jornadas de pessoas]**

_Para adicionar uma nova jornada :_

+++Jornada de conta

1. Clique em **[!UICONTROL Criar Jornada de Conta]** na parte superior direita da página.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

   ![Caixa de diálogo Criar Jornada de Conta](./assets/account-journey-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

+++

+++Jornada da pessoa

1. Clique em **[!UICONTROL Criar Jornada]** na parte superior direita da página.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

   ![Caixa de diálogo Criar Jornada](./assets/person-journey-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

+++

## Componentes para design de jornada

O _mapa de jornadas_ é a zona central no espaço de trabalho de jornada. É nessa zona que você pode adicionar nós de jornada e configurá-los. Clique em um nó para abrir o painel de propriedades à direita da tela e defina-o de acordo com seu design. Uma jornada sempre começa com um nó de público-alvo, em que você pode definir a entrada da jornada:

* [Nó de público-alvo da conta](./account-audience-nodes.md)
* [Nó de público-alvo de pessoa](./person-audience-nodes.md)

Depois de criar uma jornada de conta e adicionar o público-alvo, crie a jornada usando nós. O mapa de jornadas fornece uma tela, onde você pode criar seus casos de uso de marketing B2B em várias etapas usando os seguintes tipos de nó para criar uma jornada de conta:

* [Realizar uma ação](./action-nodes.md)
* [Acompanhar um evento](./listen-for-event-nodes.md)
* [Dividir caminhos](./split-merge-paths-nodes.md)
* [Caminhos divididos da variante](./variant-split-paths-nodes.md)
* [Próximo caminho recomendado](./next-best-path-node.md)
* [Aguardar](./wait-nodes.md)
* [Mesclar caminhos](./split-merge-paths-nodes.md)

## Medidas de proteção

Para ajudar você a criar uma jornada sem encontrar erros, as seguintes medidas de proteção estão em vigor:

* _Excluindo um nó de caminho Split_: a exclusão de um nó requer a exclusão de todos os nós subsequentes em cada caminho.
* _Excluindo um nó de mesclagem_: um nó de mesclagem só pode ser excluído quando há um caminho conectado a ele. Para excluir um nó de mesclagem, deixe apenas um caminho selecionado.
* _Alternância entre contas e pessoas_: alterar a seleção de contas para pessoas exclui todos os nós subsequentes em cada caminho.

## Adicionar um nó

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) no caminho e escolha o tipo de nó.

   ![Clique em + e escolha o tipo para adicionar o nó do jornada ao caminho](./assets/node-add-menu.png){width="400" zoomable="no"}

   Os tipos de nó disponíveis dependem do tipo de jornada e do contexto do caminho. Consulte [_Jornada nós_](./journey-nodes.md) para obter mais informações.

1. Defina as propriedades do nó à direita.

   As propriedades dependem do tipo de nó.

## Rotular um nó {#label-a-node}

Em [!DNL Adobe Journey Optimizer B2B Edition], cada nó no mapa de jornadas exibe seu nome padrão, como _Aguardar_ ou _Enviar email_. Adicione rótulos de exibição para distinguir nós do mesmo tipo e identificar a finalidade de cada etapa. Por exemplo, use o _controle de 48 horas_ ou o _email de boas-vindas_.

Você pode adicionar um rótulo de exibição a qualquer nó em uma jornada de conta ou em uma jornada de pessoa.

1. No mapa de jornadas, selecione o nó que deseja rotular.

1. Nas propriedades do nó, insira o texto no campo **[!UICONTROL Rótulo de exibição]**.

   O rótulo pode incluir até 255 caracteres.

1. Clique fora do campo para aplicar o rótulo.

   ![Adicionar um rótulo de exibição para distinguir o nó na jornada](./assets/node-display-label.png){width="500" zoomable="no"}

   O rótulo substitui o nome padrão no nó no mapa de jornadas.

Para restaurar o nome padrão, desmarque o campo **[!UICONTROL Exibir rótulo]** e clique fora do campo.

Ao publicar a jornada, o rótulo de exibição de cada nó é salvo com a jornada publicada.

>[!NOTE]
>
>Os rótulos de exibição não estão disponíveis para nós em jornadas que foram criadas antes da disponibilização desse recurso.

Os rótulos de nó estão disponíveis no esquema `AJOB2B - 1.5.4 - journey node` e no conjunto de dados `AJOB2B-1_5_4-journey_node`. Você pode consultar rótulos em [!DNL Adobe Experience Platform] e usá-los para relatórios em [!DNL Adobe Customer Journey Analytics]. Para obter mais informações sobre como consultar os dados exportados, revise os [pré-requisitos da consulta do conjunto de dados](../data/aep-query-examples.md#prerequisites).

## Excluir um nó

1. Navegue até o mapa de jornadas.

1. Nas propriedades do nó à direita, clique no ícone _Excluir_ ( ![Ícone Excluir](../assets/do-not-localize/icon-delete.svg) ).

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

## Adicionar e excluir um caminho

1. No mapa de jornadas, clique no ícone de adição ( **+** ) no caminho e adicione o [nó do caminho dividido](./split-merge-paths-nodes.md#split-paths).

1. Nas propriedades do nó à direita, selecione **[!UICONTROL Conta]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]**.

   Para cada caminho criado na jornada, um novo cartão de caminho aparece nas propriedades.

1. Navegue até um dos caminhos na jornada e adicione os nós [ação](./action-nodes.md) ou [evento](./listen-for-event-nodes.md) a esse caminho usando o ícone de adição.

1. Selecione o nó [caminho dividido](./split-merge-paths-nodes.md) para abrir as propriedades à direita.

   Os caminhos que contêm nós não podem ser excluídos.

1. Para excluir um caminho, primeiro você deve excluir todos os nós nesse caminho.

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

## Publicar uma jornada

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

1. Clique em **[!UICONTROL Next]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Publicar]**.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
