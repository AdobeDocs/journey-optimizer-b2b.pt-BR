---
title: '[!DNL Adobe Target] Públicos-alvo externos'
description: Ativar públicos externos para  [!DNL Adobe Target] por meio de jornadas de conta. Personalize as experiências da Web B2B e mantenha a consistência entre plataformas.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target] públicos externos

Você pode ativar e personalizar experiências para públicos externos no [!DNL Adobe Target] por meio de jornadas de conta. Use esta integração para obter uma personalização avançada e personalizada que aumente o engajamento e para manter a consistência entre plataformas no [!DNL Target] e [!DNL Journey Optimizer B2B Edition]. Essa consistência garante que as equipes alinhem e personalizem canais da Web para grupos de compra em toda a jornada de compradores B2B.

É um fluxo de trabalho de duas etapas para ativar um público-alvo externo por meio do Adobe Target:

1. [Adicionar ao público-alvo de cliente externo](#add-to-customer-external-audience-from-a-journey) a partir de uma jornada.
2. [Ative o público externo](#activate-the-external-audience-to-target-as-a-destination) para [!DNL Target] como destino no Experience Platform.

## Adicionar ao público externo do cliente a partir de uma jornada

Na sua jornada, [adicione um nó _Realizar uma ação_](../journeys/action-nodes.md) para executar a ação _[!UICONTROL Adicionar ao público-alvo externo]_. As ações normalmente são o que você deseja que aconteça como resultado de algum tipo de acionador, como um evento ou uma ação anterior. A jornada executa a ação quando uma conta qualificada com perfis de pessoa chega ao nó.

>[!NOTE]
>
>Quando uma conta qualificada com perfis de pessoa atinge o nó _Adicionar ao público-alvo externo de cliente_ em uma jornada publicada, pode levar até 48 horas para que esses perfis sejam preenchidos no público-alvo externo.

1. Com o nó _Realizar uma ação_ selecionado na tela de jornada, escolha a opção _[!UICONTROL Ação em]_ **[!UICONTROL Pessoas]**.

1. Para _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Adicionar ao público-alvo externo]**.

   ![Nó do Jornada - executar uma ação nas pessoas - adicionar ao público-alvo externo do cliente](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. Nas propriedades do nó à direita, defina o público-alvo externo.

   * Se um ou mais públicos-alvo externos já tiverem sido criados, você poderá escolher **[!UICONTROL Selecionar existente]** e [selecionar o público-alvo que deseja usar](#choose-an-external-audience).

   * Se você deseja [criar um público-alvo](#create-an-external-audience) para usar no nó, escolha **[!UICONTROL Criar novo]**.

### Criar um público-alvo externo

1. Depois de escolher a opção **[!UICONTROL Criar novo]** nas propriedades do nó, clique em **[!UICONTROL Criar público-alvo externo]**.

   ![Realizar uma ação sobre pessoas - adicionar a público-alvo de cliente externo - criar nova opção](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) para o novo público-alvo.

   ![Caixa de diálogo Criar público-alvo de cliente externo](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

   O sistema cria o novo público-alvo e exibe uma mensagem de confirmação. Em seguida, você pode continuar a usá-lo como um público-alvo existente para a ação do nó.

### Selecionar um público-alvo externo

1. Depois de escolher a opção **[!UICONTROL Selecionar existente]** nas propriedades do nó, clique em **[!UICONTROL Selecionar público-alvo externo do cliente]**.

   ![Realizar uma ação sobre pessoas - adicionar a público-alvo de cliente externo - selecionar opção existente](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. Na caixa de diálogo _[!UICONTROL Adicionar público-alvo]_, selecione o público-alvo que deseja usar.

   Você pode inserir texto no campo _Pesquisa_ para filtrar os itens exibidos para uma correspondência do nome do público-alvo.

   ![Executar uma ação sobre pessoas - adicionar a público-alvo de cliente externo - adicionar caixa de diálogo de público-alvo](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar audiência]**.

## Ativar o público externo para o Target como destino

A ativação do público externo para o Adobe Target exige que você tenha configurado o [!DNL Adobe Target] como destino no [!DNL Real-time Customer Data Platform (RTCDP)]. Para obter informações adicionais sobre essa configuração, consulte a [documentação do RTCDP](https://experienceleague.adobe.com/pt-br/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>Usar a ativação por meio de uma jornada exige que sua implementação do RTCDP use o Endereço de email como uma identidade.

O processo de ativação exige que você adicione [!DNL Adobe Target] como público-alvo externo ou destino externo. Você começa criando um público-alvo de [!DNL Target] no construtor de públicos-alvo. Você também pode criar um público-alvo para espaço reservado e adicionar o recurso de público-alvo externo.

>[!BEGINSHADEBOX]

![Ícone de Permissões do AEP](../../assets/do-not-localize/icon_permissions-outline.svg) Essas etapas exigem as seguintes permissões para sua função de usuário atribuída:

* **[!UICONTROL Experience Platform]** - Para o recurso _[!UICONTROL Destinos]_: `Activate Destinations`, `Manage and Activate Dataset Destination` e `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. No Experience Platform, vá para **[!UICONTROL Conexões]** > **[!UICONTROL Destinos]** na navegação à esquerda.

1. Selecione a guia **[!UICONTROL Navegar]**.

1. Localize a conexão de destino que você deseja usar para ativar seus segmentos, clique no ícone _Mais menu_ ( **...** ) ao lado do nome e escolha **[!UICONTROL Ativar públicos-alvo]**.

   Digite texto no campo _[!UICONTROL Pesquisa]_ para filtrar os destinos exibidos para uma correspondência por nome.

   ![Experience Platform - destinos - procurar destinos do Target - menu Mais](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Na lista _[!UICONTROL Públicos-alvo disponíveis]_, selecione seu público-alvo externo e clique em **[!UICONTROL Avançar]**.

   ![Experience Platform - destinos - procurar destinos do Target - menu Mais](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Execute qualquer mapeamento de campo adicional para o destino (opcional) e clique em **[!UICONTROL Avançar]**.

1. Revise os novos parâmetros de público e clique em **[!UICONTROL Concluir]**.

   ![Experience Platform - destinos - ativar destino - analisar](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Após a ativação, você pode ver o público-alvo em [públicos-alvo da Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} e usá-los em atividades do Adobe Target.

