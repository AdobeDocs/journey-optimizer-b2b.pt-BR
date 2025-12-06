---
title: Ativar o Marketo Engage para oferecer suporte a ações de Jornada
description: Ative as conexões do Marketo Engage para oferecer suporte a ações do jornada, para que os profissionais de marketing possam coordenar campanhas entre o Marketo Engage e o Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Ativar instâncias do Marketo Engage para dar suporte a ações

As ações do Marketo Engage são ações _com base em pessoas_ que permitem coordenar sua orquestração de marketing _com base em conta_ entre o Journey Optimizer B2B edition e seus esforços de marketing _com base em clientes potenciais_ no Marketo Engage. Use essas ações para orquestrar a associação de listas estáticas e colocar pessoas em campanhas.

Para usar as ações de jornada do Marketo Engage, um administrador cria primeiro um [serviço personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} no Marketo Engage, que fornece as credenciais necessárias para autenticação. Em seguida, um administrador de produto do Journey Optimizer B2B edition usa as credenciais para criar uma conexão com o Marketo Engage. Os usuários do Journey Optimizer B2B edition podem fazer referência à conexão para configurar ações do Marketo Engage em <!-- person and -->jornadas de conta, como adicionar ou remover pessoas de listas do Marketo Engage ou adicioná-las a campanhas de solicitação.

## Configurar uma conexão do Marketo Engage {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Conexões externas do Marketo Engage"
>abstract="Os administradores de produtos podem configurar conexões com instâncias externas do Marketo Engage, o que as torna disponíveis para ações de jornada."

Conclua as tarefas a seguir para configurar uma instância externa do Marketo Engage para uso com ações de jornada.

### Criar o serviço personalizado do Marketo Engage

1. Faça logon no Marketo Engage como administrador e [crie um serviço personalizado](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Copie os seguintes valores para usar na conexão do Journey Optimizer B2B edition:

   * ID do Munchkin
   * ID do cliente
   * Segredo do cliente

A visibilidade do espaço de trabalho do Marketo Engage para ativos, como listas e campanhas, é regida pelas [permissões de função atribuídas no serviço personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Os profissionais de marketing podem usar a mesma conexão várias vezes em uma jornada e usar diferentes conexões do Marketo Engage na mesma jornada.

### Adicionar a integração

![Adicionar detalhes da integração](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. No Journey Optimizer B2B edition, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.
1. Selecione para a guia **[!UICONTROL Integrações]**.
1. Clique em **[!UICONTROL Criar uma conexão]**.
1. Insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).
1. Selecione a política de atualização usada para aplicar uma ação a um registro de pessoa correspondente.

   Quando uma ação é executada para a instância conectada do Marketo Engage, a _política de atualização_ selecionada determina os registros de pessoa no Marketo Engage para selecionar se existem vários identificadores no perfil de pessoa unificado.

   * **[!UICONTROL Atualizar todos os registros correspondentes]**
   * **[!UICONTROL Atualizar somente o registro correspondente mais antigo]**
   * **[!UICONTROL Atualizar somente o registro correspondente mais recente]**

   >[!NOTE]
   >
   >As pessoas continuam pela jornada independentemente de uma correspondência, exceto quando ocorre um erro.

1. Insira a Munchkin ID, a ID do cliente e o Segredo do cliente para o serviço criado na instância externa do Marketo Engage.
1. Clique em **[!UICONTROL Conectar ao Marketo]**.
1. Clique em **[!UICONTROL Criar]**.

## Usar a conexão em uma ação de jornada

Quando um profissional de marketing usa uma ação do Marketo Engage em uma jornada, é possível configurar o nó usando o nome da conexão.

Com a integração concluída, as ações do Marketo Engage estão disponíveis em **Ações em:** nas propriedades do nó.

![lista de ações do Marketo](assets/marketo-actions-list.png){width="800" zoomable="yes"}