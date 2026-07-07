---
title: Selecionar eventos de experiência e campos
description: Selecione eventos e campos do Experience Platform para acionar a decisão em tempo real nas jornadas com base no comportamento do cliente.
feature: Setup, Integrations
role: Admin
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: adf04a6a-050f-44bc-a52c-db79ccb22ebf
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: 2026-03-27T22:58:08.848Z
TQID: https://experienceleague.adobe.com/vmRXmmc19LjpJf6EQ0BipW8oXn5GdKT3r-boHLd-XmQ
source-git-commit: 0006aa457b010f30226ac9b0fd8d7c52fd9187e9
workflow-type: tm+mt
source-wordcount: 1632
ht-degree: 11%

---

# Selecionar eventos de experiência e campos

Os administradores podem selecionar [Eventos de experiência](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} do Adobe Experience Platform (AEP) específicos e seus campos associados no esquema de união do Evento de experiência. Após a seleção, os usuários podem configurar regras de decisão para ouvir esses Eventos de experiência e ativar ações de campanha dinâmicas e direcionadas com base em dados de eventos quase em tempo real.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->

>[!PREREQUISITES]
>
>O uso de eventos e campos de experiência no Journey Optimizer B2B edition requer esquemas de evento de experiência habilitados para perfil. Para obter mais informações, consulte [Habilitar perfis de clientes em tempo real](https://experienceleague.adobe.com/en/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/enable-profiles){target="_blank"} nos tutoriais do Experience Platform.

O uso de Eventos de experiência do AEP no jornada é um processo de duas etapas:

1. Um administrador [adiciona eventos e campos da AEP Experience](#add-an-event) nas configurações do Journey Optimizer B2B edition.

1. Em uma jornada, um profissional de marketing usa os eventos configurados de uma das duas formas a seguir:

   * Adiciona um nó _Ouvir um evento_ e [seleciona um Evento de Experiência](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event) para disparar a progressão da jornada com base na atividade de evento em tempo real durante a jornada.
   * Adiciona um nó _Dividir caminhos por pessoas_ e configura um caminho para [filtrar em um evento](../journeys/split-merge-paths-nodes.md#experience-event-history-filtering) da pasta **[!UICONTROL Histórico de eventos]**.

>[!BEGINSHADEBOX]

## Diretrizes e limitações {#guidelines-and-limitations}

Ao selecionar eventos para atender às suas metas organizacionais, considere o seguinte:

* É possível selecionar até 50 eventos e até 100 campos por evento.

* O Jornada pode ouvir eventos de experiência que são assimilados usando os recursos de transmissão do Experience Platform, como o Web SDK ou a API HTTP.

* Os dados históricos do evento de experiência começam a ser acumulados para uma pessoa quando o evento existe no banco de dados do Journey Optimizer B2B edition. Para pessoas que já existem quando um tipo de evento é configurado pela primeira vez, o preenchimento retroativo começa no momento da configuração. Para novas pessoas, o acúmulo começa quando a pessoa é adicionada pela primeira vez (seu histórico anterior não está disponível retroativamente).

* No momento, não há nenhum mecanismo de exclusão para o histórico de eventos acumulados. A política de retenção de longo prazo está sujeita a alterações.

* Ao usar um Evento de experiência e publicar a jornada, você pode adicionar mais campos, mas não pode remover campos que foram selecionados anteriormente.

* Você pode referenciar um Evento de experiência em várias jornadas ou usá-lo mais de uma vez na mesma jornada.

>[!NOTE]
>
>Ao selecionar campos XDM para _[!UICONTROL Padrão]_, _[!UICONTROL Relacional]_ ou _[!UICONTROL Eventos]_, somente os tipos de dados básicos são suportados (cadeia de caracteres, inteiro, duplo e Booleano). Matrizes e objetos não são permitidos.

>[!ENDSHADEBOX]

## Gerenciar eventos de experiência {#manage-experience-events}

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.

1. Clique em **[!UICONTROL Configurações XDM]** no painel intermediário e, em seguida, clique na guia **[!UICONTROL Eventos]** para exibir a lista de eventos disponíveis.

   ![Acessar os Eventos de Experiência selecionados](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   A lista é exibida de acordo com a coluna _[!UICONTROL Última atualização]_, com os eventos atualizados mais recentes no topo por padrão.

   Nesta página, você pode [selecionar](#add-an-event) e [editar](#edit-an-event) eventos para usar no jornada.

   Para acessar os detalhes de um evento selecionado, clique no nome do evento.

### Filtrar a lista de eventos {#filter-the-event-list}

Digite texto no campo _[!UICONTROL Pesquisa]_ para filtrar os eventos exibidos para uma correspondência do nome do evento.

![Filtrar a lista de eventos selecionados por nome](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Adicionar um evento {#add-an-event}

Para disponibilizar um Evento de Experiência para um nó _Ouvir um evento_ em uma jornada, selecione o evento e os campos com suporte.

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

A lista na guia _[!UICONTROL Eventos]_ exibe o evento salvo.

### Editar um evento {#edit-an-event}

Para alterar os campos, edite os detalhes do evento.

1. Clique no nome do evento ou clique no ícone _Mais menu_ ( **...** ) e escolha **[!UICONTROL Editar]**.

   ![Clique no ícone do menu Mais](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Editar campos]** para abrir a caixa de diálogo _[!UICONTROL Selecionar campos]_ e adicionar mais campos.

   Não é possível remover campos que foram selecionados anteriormente depois que uma jornada que usa esse evento é publicada.

1. Clique em **[!UICONTROL Selecionar]** para salvar suas seleções.

### Remover um evento {#remove-an-event}

Para impedir que um Evento de Experiência seja usado em um nó _Ouvir um evento_ em uma jornada, remova o evento. Não é possível remover um evento se uma jornada no status _Agendado_, _Em tempo real_ ou _Concluído_ o utilizar.

1. Clique no ícone _Mais menu_ ( **...** ) ao lado do nome do evento e escolha **[!UICONTROL Remover]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Remover]**.

   ![Confirmar a remoção do evento](./assets/configurations-xdm-events-remove.png){width="500" zoomable="yes"}

## Eventos e campos {#events-and-fields}

Para [!DNL Journey Optimizer B2B Edition], determinadas atividades no nível de pessoas são capturadas como [!DNL Experience Platform] Eventos de experiência. Esses eventos são armazenados em um conjunto de dados do sistema que usa o esquema de Evento de experiência XDM e inclui grupos de campos específicos da jornada. Você pode usar esses eventos no [!UICONTROL Journey Optimizer B2B edition] como qualquer outro Evento de Experiência.

Cada evento expõe um conjunto definido de campos que podem ser usados nos nós _Ouvir um evento_ da jornada (decisões baseadas em eventos). Para determinar qual evento e campos usar nesses nós de jornada, revise os tipos de evento disponíveis e seus campos:

### E-mail enviado {#email-sent}

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
| ID da instância de origem de email | `directMarketing.emailSent.mailingKey.sourceInstanceID` |
| Chave de origem do email | `directMarketing.emailSent.mailingKey.sourceKey` |
| Nome da mala direta | `directMarketing.emailSent.mailingName` |
| ID DA JORNADA | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID do nó | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail enviado {#email-delivered}

Esse evento rastreia quando um email foi entregue com êxito ao serviço de email de uma pessoa.

Tipo de evento: `directMarketing.emailDelivered`

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

### E-mail aberto {#email-opened}

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

### Email clicado {#email-clicked}

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

### Email devolvido {#email-bounced}

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

### Rejeição temporária de email {#email-bounced-soft}

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

### Email cancelado {#email-unsubscribed}

Esse evento é rastreado quando uma pessoa cancela a assinatura de um email de marketing.

Tipo de evento: `directMarketing.emailUnsubscribed`

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

### Visitar página da Web {#visit-web-page}

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

### Formulário preenchido {#form-filled-out}

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

### Link da Web clicado {#web-link-clicked}

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

### Momento interessante {#interesting-moment}

Este evento rastreia quando um momento interessante foi gravado para uma pessoa.

Tipo de evento: `leadOperation.interestingMoment`

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

<!--
 ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) 
-->