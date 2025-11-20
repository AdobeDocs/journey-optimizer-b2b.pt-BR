---
title: Selecionar eventos de experiência e campos
description: Selecione eventos e campos do Experience Platform para acionar a decisão em tempo real nas jornadas com base no comportamento do cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Este recurso está atualmente em uma versão beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Selecionar eventos de experiência e campos

Os administradores podem selecionar [Eventos de experiência do AEP](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} específicos e seus campos associados no esquema de união de Eventos de experiência. Após a seleção, os usuários podem configurar regras de decisão para ouvir esses Eventos de experiência e ativar ações de campanha dinâmicas e direcionadas com base em dados de eventos quase em tempo real.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
O uso de eventos de experiência do AEP no jornada é um processo de duas etapas:

1. Um administrador [adiciona eventos e campos de experiência do AEP](#add-an-event) nas configurações do Journey Optimizer B2B edition.

2. Em uma jornada, um profissional de marketing adiciona um nó _Ouvir um evento_ e [seleciona um Evento de experiência](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Seleciona o evento a ser usado no nó.
   * Seleciona os campos a serem usados como restrições.

>[!BEGINSHADEBOX]

## Diretrizes e limitações

Ao selecionar eventos para atender às suas metas organizacionais, lembre-se do seguinte:

* É possível selecionar até 50 eventos e até 100 campos por evento.

* O Jornada pode ouvir eventos de experiência que são assimilados usando os recursos de transmissão do Experience Platform, como o Web SDK ou a API HTTP.

* Você pode usar os Eventos de experiência para fins de decisão em uma jornada, mas eles não são retidos. Portanto, não é possível aproveitar um registro histórico de Eventos de experiência no Journey Optimizer B2B edition.

* Ao usar um Evento de experiência e publicar a jornada, você pode adicionar mais campos, mas não pode remover campos que foram selecionados anteriormente.

* Você pode fazer referência a um Evento de experiência em várias jornadas ou usar um mais de uma vez na mesma jornada.

>[!ENDSHADEBOX]

## Gerenciar eventos de experiência

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.

1. Clique em **[!UICONTROL Classes XDM]** no painel intermediário e, em seguida, clique na guia **[!UICONTROL Eventos]** para exibir a lista de eventos disponíveis.

   ![Acessar os Eventos de Experiência selecionados](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   A tabela é classificada pela coluna _[!UICONTROL Última atualização]_, com os eventos atualizados mais recentes no topo por padrão.

   Nesta página, você pode [selecionar](#add-an-event) e [editar](#edit-an-event) eventos para usar no jornada.

   Para acessar os detalhes de um evento selecionado, clique no nome do evento.

### Filtrar a lista de eventos

Digite texto no campo _[!UICONTROL Pesquisa]_ para filtrar os eventos exibidos para uma correspondência do nome do evento.

![Filtrar a lista de eventos selecionados por nome](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Adicionar um evento

Para disponibilizar um Evento de Experiência para um nó _Ouvir um evento_ em uma jornada, selecione o evento e os campos com suporte.

>[!NOTE]
>
>Na versão beta, não é possível remover eventos da lista. Certifique-se de que cada evento adicionado se destine ao uso por sua organização.

1. Clique em **[!UICONTROL Selecionar evento de experiência]** na parte superior direita.

   A página de detalhes do evento é exibida. Nessa página, é possível escolher o tipo de evento e os campos.

   ![Detalhes de evento para um novo evento](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Escolha o tipo de evento.

   * Clique em **[!UICONTROL Selecionar tipo de evento]**.

   * Na caixa de diálogo, escolha o tipo de evento.

     Use o campo _[!UICONTROL Pesquisa]_ para filtrar a lista exibida por nome. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar as seleções atuais.

     ![Caixa de diálogo Selecionar tipo de evento](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Clique em **[!UICONTROL Selecionar]**.

1. Escolha um ou mais campos para o tipo de evento.

   * Clique em **[!UICONTROL Selecionar campos]**.

   * Na caixa de diálogo, selecione os campos que deseja usar como restrições para eventos correspondentes.

     Use o campo _[!UICONTROL Pesquisa]_ para filtrar a lista exibida por nome. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar as seleções atuais.

     ![Caixa de diálogo Selecionar campos](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Clique em **[!UICONTROL Selecionar]**.

1. Na página de detalhes do evento, clique em **[!UICONTROL Salvar]**.

O evento salvo é exibido na lista da guia _[!UICONTROL Eventos]_.

### Editar um evento

Edite os detalhes do evento para alterar os campos.

1. Clique no nome do evento ou clique no ícone _Mais menu_ ( **...** ) e escolha **[!UICONTROL Editar]**.

   ![Clique no ícone do menu Mais](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Editar campos]** para adicionar mais campos ou remover seleções existentes na caixa de diálogo _[!UICONTROL Selecionar campos]_.

1. Clique em **[!UICONTROL Selecionar]** para salvar suas seleções.

### Remover um evento

>[!NOTE]
>
>Na versão Beta desse recurso, não é possível remover um evento da lista de eventos selecionados. A remoção do evento está planejada para a versão do GA.

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->