---
title: Nós de público-alvo de pessoa
description: Configure nós de público-alvo de pessoas com segmentos ou públicos-alvo baseados em eventos para definir pontos de entrada de jornada de pessoas para a orquestração direcionada no Journey Optimizer B2B edition.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Nós de jornada de público-alvo de pessoa

O nó _person audience_ especifica quais perfis de pessoa entram na jornada. Quando você [cria uma jornada de pessoa](./create-publish-journey.md#create-a-journey), a jornada sempre começa com um nó de público-alvo de pessoa que define sua entrada. O nó de público-alvo pessoa pode ter um dos dois tipos de entrada de público-alvo: segmentos de CDP ou associação baseada em eventos. As definições de segmento e público-alvo baseadas em eventos não podem ser combinadas.

Use uma das seguintes opções de entrada para o nó de jornada do público-alvo de pessoa:

* **Público-alvo do perfil** - Use públicos-alvo de segmento definidos em uma CDP. Todos os perfis qualificados para o público-alvo são adicionados como membros à jornada. Perfis recém-qualificados para o segmento são adicionados à jornada durante as tarefas diárias de [assimilação de perfis](#profile-ingestion). Se um perfil não se qualificar mais para o segmento, ele **_não_** será removido da jornada.

* **Público-alvo do evento** - Use eventos qualificados para definir o público-alvo. Esses eventos são definidos na configuração do nó e devem usar [eventos XDM definidos nas configurações de administração](../admin/configure-aep-events.md). Até 10 eventos são compatíveis com a associação de público-alvo com base em eventos. Um perfil é qualificado imediatamente para a jornada após o primeiro evento correspondente que seu perfil realiza.

  >[!NOTE]
  >
  >Eventos não podem ser combinados com atributos de perfil para restringir as definições de público. Melhorias para lidar com essa limitação estão planejadas para versões futuras.

## Ingestão de perfil

No Journey Optimizer B2B edition, uma tarefa de assimilação de público-alvo noturna mantém os perfis em sincronia com o Experience Platform. Embora as jornadas de pessoas baseadas em eventos possam qualificar perfis que não fazem parte de um perfil ou público-alvo de conta assimilado/em uso pelo Journey Optimizer B2B edition, elas resultam em perfis assimilados que permanecem obsoletos, a menos que façam parte de um público-alvo usado por uma jornada de pessoa, jornada de conta ou grupo de compras. Se um perfil for assimilado e posteriormente adicionado a um público-alvo, a compilação de perfil será executada e o perfil permanecerá sincronizado com o Experience Platform. As melhorias na sincronização de dados deste perfil estão planejadas para versões futuras.

Um perfil recém-criado assimilado por uma jornada de pessoa com base em eventos pode não ter as informações de perfil atualizadas no momento da assimilação. Por exemplo, se um perfil for criado por meio de um evento de preenchimento de formulário e uma jornada de pessoa os assimilar do evento de preenchimento de formulário qualificado, os dados enviados no formulário talvez ainda não sejam sincronizados com o perfil quando a jornada os assimilar. O resultado pode ser dados incompletos para personalização (como no conteúdo de email). As melhorias na sincronização de dados do evento deste perfil estão planejadas para versões futuras.

As jornadas de pessoas baseadas em eventos podem qualificar perfis que ainda são anônimos/sem endereços de email e que contêm apenas ECIDs. Isso acontece com mais frequência quando você tem lógica de qualificação para atividade de página da Web. Lógica de público-alvo baseada em eventos muito ampla pode resultar na ocorrência de 40 milhões de perfis no limite se muitos perfis forem qualificados. Limite o escopo possível do público-alvo para evitar esse cenário.

>[!IMPORTANT]
>
>Durante o programa beta atual, o uso ideal das jornadas de pessoas é qualificar apenas os perfis que você também está direcionando nas jornadas de conta e nas definições de grupo de compras. Esse uso garante um perfil completo que permanece sincronizado com o Experience Platform.

## Definir o público do nó de público-alvo pessoa

1. Clique no nó **[!UICONTROL Público-alvo de pessoa]**.

   Essa ação exibe as propriedades do nó à direita.

   ![Nó de jornada de público-alvo de pessoa](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Escolha o tipo de entrada para as pessoas que entram na jornada:

   * **[!UICONTROL Público-alvo do perfil]**

     Escolha a opção _[!UICONTROL Perfil de público-alvo]_. Em seguida, clique em **[!UICONTROL Adicionar público-alvo do perfil]**.

     Na caixa de diálogo _[!UICONTROL Adicionar público-alvo]_, selecione um segmento de público-alvo criado anteriormente. Clique em **[!UICONTROL Adicionar público-alvo]**.

     ![Selecione uma audiência de perfil para o nó](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Público-alvo do evento]**

     Escolha a opção _[!UICONTROL Audiência do evento]_. Em seguida, clique em **[!UICONTROL Adicionar critérios de evento]**.

     Na caixa de diálogo _[!UICONTROL Editar critérios de evento]_, adicione um ou mais eventos que você deseja usar para qualificação de membros de público-alvo. Para cada evento que você adicionar, clique em **[!UICONTROL Adicionar restrição]** para escolher um atributo de evento para uma correspondência. Defina a avaliação que deseja usar para uma correspondência. Você pode adicionar várias restrições para corresponder ao evento.

     ![Adicionar eventos e critérios de correspondência para qualificar um perfil de pessoa](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     Quando os critérios do evento forem definidos, clique em **[!UICONTROL Salvar]**.

     Para obter mais informações sobre a configuração de eventos compatíveis com o jornada, consulte [Gerenciar eventos de experiência](../admin/configure-aep-events.md#manage-experience-events).
