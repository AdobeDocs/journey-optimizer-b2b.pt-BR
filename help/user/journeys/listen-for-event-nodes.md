---
title: Ouvir um evento
description: 'Configure nós de eventos para acionadores de conta e de pessoas: acompanhe alterações de grupo de compras, cliques de email, preenchimentos de formulário e eventos do Experience Platform no Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: 2026-03-30T23:08:46.228Z
TQID: https://experienceleague.adobe.com/f9N-ZeBXK-ON-gWtJHgFwvr9DCXRQyZRj9O7Jz9qeyo
source-git-commit: 0b4e657df254a072d5703f13e956275e58554f9a
workflow-type: tm+mt
source-wordcount: 1897
ht-degree: 5%

---

# Acompanhar um evento

Para mover o público-alvo para a próxima etapa da sua [jornada](./journeys-overview.md) quando ocorrer um evento, adicione o nó _Ouvir um evento_. Dependendo do tipo de jornada, você pode usar esse nó para acionar o próximo nó na jornada de acordo com pessoas ou eventos de conta.

<!--
![Video](../../assets/do-not-localize/icon-video.svg){width="30", vertical-align="middle"} [Watch the overview video](#overview-video)
-->

## Jornadas da conta {#account-journeys}

>[!NOTE]
>
>Para uma jornada de conta, não é possível adicionar o tipo de nó _[!UICONTROL Escutar um evento]_ em um caminho dividido por pessoas.

1. Abra a tela de jornada da conta.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

   ![Adicionar nó de jornada a uma jornada de conta - Ouvir um evento](./assets/node-listen-event-account-journey.png){width="400"}

1. Nas propriedades do nó à direita, use o seletor _Tipo de evento_ para escolher entre **[!UICONTROL Contas]** e **[!UICONTROL Pessoas]**.

1. Selecione um evento na lista.

   * Para o tipo de evento _Pessoas_, escolha o [evento de pessoas](#people-events) que você deseja usar para o gatilho.

     ![Nó do Jornada - ouvir eventos em pessoas](./assets/node-listen-events-people.png){width="500" zoomable="yes"}

   * Para o tipo de evento _Contas_, escolha o [evento de conta](#account-events) que deseja usar para o gatilho.

     ![Nó de Jornada - escutar eventos na conta](./assets/node-listen-events-account.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

   Dependendo do tipo de evento e do evento selecionados, defina os critérios de correspondência do evento.

   * [Eventos de pessoas](#people-events)
   * [Eventos de conta](#account-events)

   Você também pode incluir [filtros](#filters-people-event) para o evento.

1. Clique em **[!UICONTROL Concluído]**.

   As definições de evento e filtro são exibidas no nó e nas propriedades do nó.

   ![Nó de jornada de Conta - Ouvir eventos - Evento e filtros](./assets/node-listen-events-account-complete.png){width="500"}

### Eventos de pessoas para jornadas de conta {#people-events}

Em uma jornada de conta, você pode acompanhar um evento com base em pessoas quando quiser mover a conta para frente na jornada, de acordo com os eventos acionados pela atividade de pessoas. Você também pode filtrar eventos de acordo com o histórico de eventos e atributos de pessoas.

>[!TIP]
>
>Eventos de experiência podem ocorrer _antes_ de as pessoas entrarem na jornada (como um clique de email ou uma interação na web anterior). Para rotear pessoas com base nesses eventos, use o filtro [!UICONTROL Histórico de eventos] em um nó [Dividir caminhos por pessoas](./split-merge-paths-nodes.md#experience-event-history-filtering).

#### Eventos B2B do Journey Optimizer {#events-account-people}

| Evento | Restrições |
| ----- | ----------- |
| [!UICONTROL Atribuído ao Grupo de Compras] | Interesse da solução (obrigatório)<br/><br/>Restrições adicionais (opcional): <li>Função</li><li>Data da atividade</li><br/>Tempo limite (opcional) |
| [!UICONTROL Alterações no perfil da pessoa] | Atributo (obrigatório)<br/>Data da atividade (opcional)<br/>Novo valor (opcional)<br/>Valor anterior (opcional)<br/>Motivo (opcional)<br/>Source (opcional) |
| [!UICONTROL Removido do Grupo de Compras] | Interesse da solução (obrigatório)<br/>Data da atividade (opcional)<br/>Tempo limite (opcional) |

1. Defina o valor necessário para corresponder ao evento.

   Se necessário, defina o operador para a avaliação.

1. Para cada restrição opcional que você deseja incluir na correspondência de eventos, clique em **[!UICONTROL Adicionar restrição]** e selecione uma restrição na lista.

   ![Caixa de diálogo Editar evento para um evento de pessoas B2B do Journey Optimizer em uma jornada de conta](./assets/node-listen-events-account-people-edit-event.png){width="700" zoomable="yes"}

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** para [adicionar filtros para o evento](#filters-people-event).

1. Clique em **[!UICONTROL Concluído]**.

#### Eventos de experiência {#experience-events-account-people}

>[!PREREQUISITES]
>
>Os administradores configuram os [Eventos de experiência do Adobe Experience Platform (AEP)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}, que permitem aos profissionais de marketing criar jornadas de conta e pessoa que reagem aos eventos em tempo quase real.
>
>Para disponibilizar Eventos de Experiência para jornada, um administrador de produto deve primeiro [adicionar os tipos de evento e campos de interesse](../admin/configure-aep-events.md#add-an-event) em [!DNL Journey Optimizer B2B Edition].

1. Clique em **[!UICONTROL Adicionar restrição]** e escolha o campo que deseja usar para a restrição.

   As restrições disponíveis são definidas como campos gerenciados para a configuração do evento.

1. Conclua a condição da restrição.

   Você pode usar o operador padrão **[!UICONTROL is]** para corresponder a um ou mais valores de campo. Ou você pode usar o operador **[!UICONTROL is not]** para corresponder em todos os valores com a exclusão de um ou mais valores especificados.

   ![Caixa de diálogo Editar evento para um Evento de Experiência em uma jornada de conta](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** para [adicionar filtros para o evento](#filters-people-event).

1. Clique em **[!UICONTROL Concluído]**.

### Eventos de conta {#account-events}

Em uma jornada de conta, você pode acompanhar um evento com base na conta quando quiser mover a conta para frente na jornada, de acordo com eventos acionados pela atividade da conta.

| Evento | Restrições |
| ----- | ----------- |
| [!UICONTROL A conta teve um momento interessante] | Tipo (Email, Marco ou Web)<br/>Restrições adicionais (opcional): <li>Descrição</li><li>Origem</li><li>Data da atividade</li> <br/>Tempo limite (opcional) |
| [!UICONTROL Alteração no valor dos dados da conta] | Atributo<br/>Restrições adicionais (opcional): <li>Novo valor</li><li>Valor anterior</li><li>Data da atividade</li> <br/>Tempo limite (opcional) |
| [!UICONTROL Alteração no Estágio de Grupo de Compras] | Interesse da solução<br/>Restrições adicionais (opcional): <li>Novo estágio</li><li>Fase anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| [!UICONTROL Alteração no Status do Grupo de Compras] | Interesse da solução<br/>Restrições adicionais (opcional): <li>Novo status</li><li>Status anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| [!UICONTROL Alteração na Pontuação de Integridade] | Interesse da solução<br/>Restrições adicionais (opcional): <li>Nova pontuação</li><li>Pontuação anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| [!UICONTROL Alteração na Pontuação de engajamento] | Interesse da solução<br/>Restrições adicionais (opcional): <li>Nova pontuação</li><li>Pontuação anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |

1. Defina a restrição necessária para corresponder ao evento.

1. Para cada restrição opcional que você deseja incluir para correspondência de eventos, clique em **[!UICONTROL Adicionar restrição]** e selecione o campo.

   ![jornada de Conta - Ouvir um evento de conta](./assets/node-listen-events-account-edit-event.png){width="700" zoomable="yes"}

   Defina o operador e o valor da avaliação.

1. Clique em **[!UICONTROL Concluído]**.

<!--

Removed from AJO B2B people events 

| [!UICONTROL Clicks link in email] | Email<br/><br/>Additional constraints (optional): <li>Link</li><li>Link ID</li><li>Is mobile device</li><li>Device</li><li>Platform</li><li>Browser</li><li>Is predictive content</li><li>Is bot activity</li><li>Bot activity pattern</li><li>Browser</li><li>Date of activity</li><li>Min. number of times</li><br/>Timeout (optional) |
| [!UICONTROL Clicks link in SMS] | Email<br/><br/>Additional constraints (optional): <li>Link</li><li>Device</li><li>Platform</li><li>Date of activity</li><li>Min. number of times</li><br/>Timeout (optional) |
| [!UICONTROL Data value changes] | Person attribute<br/><br/>Additional constraints (optional): <li>New value</li><li>Previous value</li><li>Reason</li><li>Source</li><li>Date of activity</li><li>Min. number of times</li><br/>Timeout (optional) |
| [!UICONTROL Opens email] | Email<br/><br/>Additional constraints (optional): <li>Link</li><li>Link ID</li><li>Is mobile device</li><li>Device</li><li>Platform</li><li>Browser</li><li>Is predictive content</li><li>Is bot activity</li><li>Bot activity pattern</li><li>Browser</li><li>Date of activity</li><li>Min. number of times</li><br/>Timeout (optional) |
| [!UICONTROL Score is changed] | Score name<br/><br/>Additional constraints (optional):<li>Change</li><li>New score</li><li>Urgency</li><li>Priority</li><li>Relative score</li><li>Relative urgency</li><li>Date of activity</li><li>Min. number of times</li><br/>Timeout (optional) |
| [!UICONTROL SMS Bounces]| SMS message<br/><br/>Additional constraints (optional): <li>Date of activity</li><li>Min number of times</li><br/>Timeout (optional) |


### Listen for a Marketo Engage event {#listen-for-marketo-engage-event}

| Marketo Engage | [!UICONTROL Visits Web Page] | Web page <br/> Select one or more Marketo Engage pages to match. <br/><br/>Additional constraints (optional): <li>Querystring</li><li>Client IP address</li><li>Referrer</li><li>User Agent</li><li>Search engine</li><li>Search query</li><li>Token</li><li>Browser</li><li>Platform</li><li>Device</li><li>Date of activity</li> |
| | [!UICONTROL Fills out form] | Form <br/> Select one or more Marketo Engage forms to match. <br/><br/>Additional constraints (optional): <li>Date of activity</li><li>Querystring</li><li>Client IP address</li><li>Referrer</li><li>User agent</li><li>Platform</li><li>Device</li><br/>Timeout (optional) |
| Adobe Experience Platform | [!UICONTROL Event definition] | Event type <br/><br/>Additional constraints (optional): <li>Fields</li> <br/>Additional constraints (not supported): <li>Date of activity</li><li>Min. number of times</li><br/> Timeout (optional) |

If you have web pages in your connected Marketo Engage instance, you can trigger an event based on a visit/no visit to these web pages, as well as Marketo Engage forms that were/were not filled. 

1. Use the **[!UICONTROL Select people event]** selector and scroll the menu to the **[!UICONTROL Marketo Engage]** section.

1. Select a Marketo Engage activity type:

   * **[!UICONTROL Visits Web Page]**.
   * **[!UICONTROL Fills Out Form]**

   ![Listen for an experience event](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Edit event]** and define one or more web pages to match and any additional constraints for the event.

   * (Required) In the _[!UICONTROL Edit event]_ dialog, define the **[!UICONTROL Web page]** or **[!UICONTROL Fills out form]** constraint. Use **[!UICONTROL is]** (default) to match on one or more selected pages or forms. Use **[!UICONTROL is not]** to match on all page visits/forms with the exclusion of one or more selected pages/forms. Or, use the **[!UICONTROL is any]** operator to match on any Marketo Engage web page visit or filled form.

   * (Optional) Click **[!UICONTROL Add constraint]** and choose the field that you want to use for the constraint. Set the operator and the value for the field.

     ![Listen for an experience event](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     To include additional field constraints as needed, repeat this action.

   * If needed, select the **[!UICONTROL Filters]** tab to [add filters for the event](#add-a-filter-to-the-people-event).

   * When the constraints and filters are defined, click **[!UICONTROL Done]**.

1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event (see [Add a timeout to an event node](#add-a-timeout-to-an-event-node)). 

1. In the journey canvas, add the next node to execute when the event occurs.

-->

## Jornadas de pessoas {#person-journeys}

1. Abra a tela de jornada de pessoa.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

   ![Adicionar nó de jornada a uma jornada de pessoa - Ouvir um evento](./assets/node-listen-event-person-journey.png){width="350"}

1. Nas propriedades do nó à direita, clique em **[!UICONTROL Adicionar critério de evento]**.

   ![Nó de Jornada - Ouvir propriedades de eventos - adicionar critérios de evento](./assets/node-listen-events-person-journey.png){width="450"}

1. Adicione um evento e defina as restrições que deseja corresponder ao acionador.

   Você pode usar [Eventos de experiência](#experience-events-person) e [Alterações de perfil de pessoa](#person-profile-changes) para definir o acionador do evento.

   Arraste e solte o acionador de evento no espaço do construtor e defina a definição. Clique em **[!UICONTROL Adicionar restrição]** para cada restrição que você deseja usar para refinar a correspondência de eventos.

   É possível adicionar vários eventos para corresponder. O primeiro evento de qualificação avança o perfil da pessoa na jornada.

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** para [adicionar filtros para o evento](#filters-people-event).

1. Clique em **[!UICONTROL Concluído]**.

   As definições de evento e filtro são exibidas no nó e nas propriedades do nó.

   ![Nó de Jornada - Ouvir eventos - Evento e filtros](./assets/node-listen-events-person-complete.png){width="450"}

### Eventos de experiência para jornadas de pessoas {#experience-events-person}

>[!PREREQUISITES]
>
>Os administradores configuram os [Eventos de experiência do Adobe Experience Platform (AEP)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}, que permitem aos profissionais de marketing criar jornadas de conta e pessoa que reagem aos eventos em tempo quase real.
>
>Para disponibilizar Eventos de Experiência para jornada, um administrador de produto deve primeiro [adicionar os tipos de evento e campos de interesse](../admin/configure-aep-events.md#add-an-event) em [!DNL Journey Optimizer B2B Edition].

Você pode usar Eventos de Experiência para acionar o nó em jornadas pessoais na caixa de diálogo _[!UICONTROL Editar evento]_.

1. Expanda **[!UICONTROL Eventos do AEP Sapphire]** na lista _[!UICONTROL Triggers]_ à esquerda.

1. Arraste e solte o Evento de experiência no espaço do construtor de eventos correspondente.

   Você pode usar o campo _Pesquisa_ para filtrar por uma palavra-chave no nome do evento, como `email`.

1. Clique em **[!UICONTROL Adicionar restrição]** e escolha o campo que deseja usar para refinar a correspondência do evento.

   As restrições disponíveis são definidas como campos gerenciados para a configuração do evento.

   ![Editar caixa de diálogo de evento para um Evento de Experiência em uma jornada de pessoa](./assets/node-listen-events-person-journey-edit-event-aep-event.png){width="700" zoomable="yes"}

1. Defina o operador e os valores para corresponder ao campo de evento.

1. (Opcional) Adicione outro evento de Experiência ou uma [alteração no perfil da pessoa](#person-profile-changes).

   Ao adicionar vários eventos para corresponder. O primeiro evento de qualificação avança o perfil da pessoa na jornada.

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** para [adicionar filtros para o evento](#filters-people-event).

1. Clique em **[!UICONTROL Concluído]**.

### Alterações no perfil da pessoa {#person-profile-changes}

Você pode usar uma alteração nos atributos de perfil da pessoa B2B para acionar o nó nas jornadas da pessoa na caixa de diálogo _[!UICONTROL Editar evento]_.

1. Arraste e solte **[!UICONTROL Alteração no perfil da pessoa]**&#x200B;s da lista _[!UICONTROL Acionadores]_ no espaço do construtor de eventos correspondente.

1. Clique em **[!UICONTROL Adicionar restrição]** e selecione a alteração de atributo que você deseja usar para o disparador de evento.

   Defina o valor do campo de acordo com a alteração que você deseja corresponder.

   ![jornada de pessoa - Ouvir um evento de alteração de perfil de pessoa](./assets/node-listen-event-person-edit-event.png){width="700" zoomable="yes"}

1. (Opcional) Adicione outro atributo _Alteração de perfil de pessoa_ que você deseja usar como um disparador de evento ou um [Evento de experiência](#experience-events-person).

   Ao adicionar vários eventos para corresponder. O primeiro evento de qualificação avança o perfil da pessoa na jornada.

1. (Opcional) Selecione a guia **[!UICONTROL Filtros]** para [adicionar filtros para o evento](#filters-people-event).

1. Clique em **[!UICONTROL Concluído]**.

## Filtros para eventos {#filters-people-event}

Ao definir um evento de [pessoas em uma jornada de conta](#people-events) ou um evento [em uma jornada de pessoa](#person-journeys), você pode incluir a filtragem para limitar disparadores de eventos correspondentes com base em vários critérios:

| Filtros | Descrição |
| ------------ | ----------- |
| [!UICONTROL Histórico de eventos] | Eventos de experiência configurados por um administrador. Consulte _[Selecionar eventos de experiência e campos](../admin/configure-aep-events.md)_. |
| [!UICONTROL Atributos da pessoa] | Atributos do perfil de pessoa B2B, incluindo: <li>Cidade <li>País <li>Data de nascimento <li>Endereço de e-mail <li>Email inválido <li>Email suspenso <li>Nome <li>Região inferida<li>Nome do cargo <li>Sobrenome <li>Número do celular <li>Pontuação de engajamento de pessoa <li>Número de telefone <li>Código postal <li>Estado <li>Inscrição cancelada <li>Motivo do cancelamento de inscrição |
| [!UICONTROL Atributos da pessoa] | (Somente jornadas de pessoa) Valor do atributo |
| [!UICONTROL Filtros especiais] > [!UICONTROL Membro do Grupo de Compras] | A pessoa é ou não é um membro do grupo de compra avaliado em relação a um ou mais dos seguintes critérios: <li>Interesse da solução</li><li>Status do Grupo de Compras</li><li>Pontuação de integridade</li><li>Pontuação de engajamento</li><li>Foi Removido</li><li>Função</li> |

<!--
| [!UICONTROL Special filters] > [!UICONTROL Member of List] | The person is or is not a member of one or more Marketo Engage lists. |
| [!UICONTROL Special filters] > [!UICONTROL Member of Program] | The person is or is not a member of one or more Marketo Engage programs. |
-->

1. Depois de definir o acionador de evento, selecione a guia **[!UICONTROL Filtros]** na caixa de diálogo _[!UICONTROL Editar evento]_.

   ![Ouvir o nó Evento por pessoas - guia Selecionar Filtros para editar o evento](./assets/node-listen-event-people-edit-event-filters.png){width="700" zoomable="yes"}

1. Para filtrar correspondências para o evento, adicione um ou mais critérios de filtro.

   * Arraste e solte qualquer um dos filtros da navegação à esquerda e conclua a definição de correspondência.

     >[!NOTE]
     >
     >Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta no Experience Platform, esses campos também estarão disponíveis em **[!UICONTROL Atributos]** para serem usados como atributos de pessoa em filtros.

   * Refine sua filtragem aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você pode optar por corresponder todos os filtros ou qualquer filtro.

     ![Filtros de pessoa usados em uma definição de evento](./assets/node-listen-events-filter-logic.png){width="600" zoomable="yes"}

1. Quando as definições de evento e filtro estiverem concluídas, clique em **[!UICONTROL Concluído]**.


## Adicionar um tempo limite a um nó de evento {#timeouts}

Se necessário, defina a quantidade de tempo que a jornada aguarda pelo evento. A jornada termina após um tempo limite, a menos que você defina um caminho de tempo limite, em que é possível adicionar outros nós.

Habilite a opção **[!UICONTROL Timeout]** nas propriedades do nó para especificar um tempo limite para o nó _Escutar evento_.

1. Com as opções habilitadas, escolha o _Tipo_ e especifique os parâmetros para o tempo limite:

   * **[!UICONTROL Duração]** - Use esse tipo para especificar um período de tempo para o disparador de evento. Se o evento não for acionado dentro desse período, a pessoa ou a conta não continuará na jornada.

     Selecione a duração pela qual a jornada aguarda a ocorrência de um evento antes de atingir o tempo limite. Especifique o número de minutos, horas, dias, semanas ou meses.

     ![Ouvir o nó do evento - Duração do tempo limite](./assets/node-listen-events-timeout-duration.png){width="500" zoomable="yes"}

     Se quiser que o período termine em um dia da semana específico, habilite a opção **[!UICONTROL Deve terminar em]**. **[!UICONTROL Qualquer dia]** é selecionado por padrão, com todos os dias selecionados. Desmarque a caixa de seleção e selecione um ou mais dias para uma data final. Em seguida, selecione **Hora** e **[!UICONTROL Fuso horário]**.

     ![Ouvir nó de evento - Duração do tempo limite - Deve terminar em](./assets/node-listen-events-timeout-duration-must-end-on.png){width="300"}

   * **[!UICONTROL Data]** - Use esse tipo para definir uma data de expiração para o nó. Se o evento não for acionado até a data/hora especificada, a pessoa ou a conta não continuará na jornada.

     Clique no ícone _Calendário_ para definir a data e a hora do tempo limite.

     ![Ouvir o nó do evento - Data do tempo limite](./assets/node-listen-events-timeout-date.png){width="500" zoomable="yes"}

1. Defina o caminho de tempo limite.

   A opção **[!UICONTROL Definir caminho de tempo limite]** está selecionada por padrão. Você pode usar esse caminho para definir o que acontecerá se o nó Escutar evento atingir o tempo limite. Você pode adicionar ações alternativas e eventos que se aplicam a perfis de pessoas quando o evento não ocorre.

   ![Nó de evento de Jornada - definir caminho de tempo limite](./assets/node-event-timeout-set-path.png){width="600" zoomable="yes"}

   Se não quiser definir o caminho, desmarque a caixa de seleção _[!UICONTROL Definir caminho de tempo limite]_.

<!--
 ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3443239/?captions=por_br&learn=on) 
-->
