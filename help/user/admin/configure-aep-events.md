---
title: Selecionar eventos de experiência e campos
description: Selecione eventos e campos do Experience Platform para acionar a decisão em tempo real nas jornadas com base no comportamento do cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Este recurso está atualmente em uma versão beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: cefd98099bf6524d1d559a47d502990852de1468
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 9%

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
>Na versão beta, não é possível remover eventos da lista. Certifique-se de que cada evento adicionado seja aquele que sua organização pretende usar.

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

## Eventos e campos

Para [!DNL Journey Optimizer B2B Edition], determinadas atividades no nível de pessoas são capturadas como [!DNL Experience Platform] Eventos de experiência. Esses eventos são armazenados em um conjunto de dados do sistema que usa o esquema de Evento de experiência XDM e inclui grupos de campos específicos da jornada. Você pode usar esses eventos no [!UICONTROL Journey Optimizer B2B edition] como qualquer outro Evento de Experiência.

Cada evento expõe um conjunto definido de campos que podem ser usados nos nós _Ouvir um evento_ da jornada (decisões baseadas em eventos). Revise os tipos de evento disponíveis e seus campos para determinar qual evento e campos usar nesses nós de jornada:

### E-mail enviado

Esse evento rastreia quando um email de marketing foi enviado a uma pessoa.

Tipo de evento: `directMarketing.emailSent`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID de origem do email | `directMarketing.emailSent.mailingKey.sourceID` |
| Tipo de origem do email | `directMarketing.emailSent.mailingKey.sourceType` |
| ID da instância de origem de email | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| Chave de origem do email | `directMailing.emailSent.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.emailSent.mailingName` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail enviado

Esse evento rastreia quando um email foi entregue com êxito ao serviço de email de uma pessoa.

Tipo de evento: `directMarketing.emailDelivered `

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail aberto

Esse evento rastreia quando uma pessoa abriu um email de marketing.

Tipo de evento: `directMarketing.emailOpened`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| É um dispositivo móvel | `device.isMobileDevice` |
| Modelo do dispositivo | `device.model` |
| Agente do usuário | `environment.browserDetails.userAgent` |
| Sistema operacional | `environment.operatingSystem` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Email clicado

Esse evento é rastreado quando uma pessoa clica em um link em um email de marketing.

Tipo de evento: `directMarketing.emailClicked`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| URL do link | `directMarketing.linkURL` |
| É um dispositivo móvel | `device.isMobileDevice` |
| Modelo | `device.model` |
| Agente do usuário | `environment.browserDetails.userAgent` |
| Sistema operacional | `environment.operatingSystem` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Email devolvido

Esse evento rastreia quando um email para uma pessoa é rejeitado.

Tipo de evento: `directMarketing.emailBounced`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| Email | `directMarketing.email` |
| Código de email rejeitado | `directMarketing.emailBouncedCode` |
| Detalhes do email rejeitado | `directMarketing.emailBouncedDetails` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Rejeição temporária de email

Esse evento rastreia quando um email para uma pessoa é rejeitado temporariamente.

Tipo de evento: `directMarketing.emailBouncedSoft`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| Email | `directMarketing.email` |
| Código de email rejeitado | `directMarketing.emailBouncedCode` |
| Detalhes do email rejeitado | `directMarketing.emailBouncedDetails` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Email cancelado

Esse evento é rastreado quando uma pessoa cancela a assinatura de um email de marketing.

Tipo de evento: `directMarketing.emailUnsubscribed `

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID da origem de mala direta | `directMarketing.mailingKey.sourceID` |
| Tipo de origem de mala direta | `directMarketing.mailingKey.sourceType` |
| ID da instância de origem de mala direta | `directMarketing.mailingKey.sourceInstanceID` |
| Chave de origem da mala direta | `directMarketing.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.mailingName` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Visitar página da Web

Esse tipo de evento é o método padrão para marcar a ocorrência como uma exibição de página.

Tipo de evento: `web.webpagedetails.pageViews`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID de origem da página da Web | `web.webPageDetails.webPageKey.sourceID` |
| Tipo de origem da página da Web | `web.webPageDetails.webPageKey.sourceType` |
| ID da instância de origem da página da Web | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Chave de origem da página da Web | `web.webPageDetails.webPageKey.sourceKey` |
| Nome da página da Web | `web.webPageDetails.name` |
| URL da página da Web | `web.webPageDetails.URL` |
| Parâmetros de consulta da página da Web | `web.webPageDetails.queryParameters` |
| ID da página da Web | `web.webPageDetails.webPageID` |
| Agente do usuário | `environment.browserDetails.userAgent` |
| URL do responsável pela indicação | `web.webReferrer.URL` |

+++

### Formulário preenchido

Esse evento rastreia quando uma pessoa preenche um formulário em uma página da Web.

Tipo de evento: `web.formFilledOut`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID de origem do formulário web | `web.fillOutForm.webFormKey.sourceID` |
| Tipo de origem do formulário web | `web.fillOutForm.webFormKey.sourceType` |
| ID da instância de origem do formulário web | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Chave de origem do formulário web | `web.fillOutForm.webFormKey.sourceKey` |
| ID do formulário web | `web.fillOutForm.webFormID` |
| Nome do formulário web | `web.fillOutForm.webFormName` |
| Parâmetros de consulta da página da Web | `web.webPageDetails.queryParameters` |
| ID da página da Web | `web.webPageDetails.webPageID` |
| Agente do usuário | `environment.browserDetails.userAgent` |
| URL do responsável pela indicação | `web.webReferrer.URL` |

+++

### Link da Web clicado

O evento sinaliza que o Web SDK registrou automaticamente um clique de link.

Tipo de evento: `web.webinteraction.linkClicks`

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| ID de origem da interação na Web | `web.webInteraction.webInteractionKey.sourceID` |
| Tipo de origem de interação com a Web | `web.webInteraction.webInteractionKey.sourceType` |
| ID da instância de origem da interação na Web | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Chave de origem da interação na Web | `web.webInteraction.webInteractionKey.sourceKey` |
| ID do link de interação na Web | `web.webInteraction.linkID` |
| URL do link de interação na Web | `web.webInteraction.linkURL` |
| Parâmetros de consulta da página da Web | `web.webPageDetails.queryParameters` |
| ID da página da Web | `web.webPageDetails.webPageID` |
| Agente do usuário | `environment.browserDetails.userAgent` |
| URL do responsável pela indicação | `web.webReferrer.URL` |

+++

### Momento interessante

Este evento rastreia quando um momento interessante foi gravado para uma pessoa.

Tipo de evento: `leadOperation.interestingMoment `

+++Campos

| Nome de exibição | Caminho |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Carimbo de data e hora | `timestamp` |
| ID da pessoa | `personID` |
| ID de origem da pessoa | `personKey.sourceID` |
| Tipo de origem da pessoa | `personKey.sourceType` |
| ID da instância de origem da pessoa | `personKey.sourceInstanceID` |
| Chave de origem da pessoa | `personKey.sourceKey` |
| Data do momento | `leadOperation.interestingMoment.date` |
| Descrição do momento | `leadOperation.interestingMoment.description` |
| Origem do momento | `leadOperation.interestingMoment.source` |
| Tipo de momento | `leadOperation.interestingMoment.type` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448688/?captions=por_br&learn=on) -->