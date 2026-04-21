---
title: Ativar o Marketo Engage para oferecer suporte a ações de Jornada
description: Ative as conexões do Marketo Engage para oferecer suporte a ações do jornada, para que os profissionais de marketing possam coordenar campanhas entre o Marketo Engage e o Journey Optimizer B2B edition.
feature: Setup, Integrations
role: Admin
exl-id: e324a11b-1025-4850-865f-ef8886a6b2bb
source-git-commit: 5607ad407ffba007d174f4427e82b0ca6c162c24
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 92%

---

# Ativar conexões do Marketo Engage para ações de suporte

As ações do Marketo Engage são ações _com base em pessoas_ que permitem coordenar sua orquestração de marketing _com base em conta_ entre o Journey Optimizer B2B edition e seus esforços de marketing _com base em clientes potenciais_ no Marketo Engage. Use essas ações para orquestrar a associação de listas estáticas e colocar pessoas em campanhas.

Para usar as ações de jornada do Marketo Engage, um administrador cria primeiro um [serviço personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} no Marketo Engage, que fornece as credenciais necessárias para autenticação. Em seguida, um administrador de produto do Journey Optimizer B2B edition usa as credenciais para criar uma conexão com o Marketo Engage. Os usuários do Journey Optimizer B2B Edition podem então fazer referência à conexão para configurar as ações do Marketo Engage nas jornadas de pessoa e conta:

* [!UICONTROL Adicionar à lista do Marketo]
* [!UICONTROL Remover da lista do Marketo]
* [!UICONTROL Adicionar à campanha de solicitação do Marketo]

## Configurar uma conexão do Marketo Engage {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Conexões externas do Marketo Engage"
>abstract="Admins de produtos podem configurar conexões com instâncias externas do Marketo Engage, tornando-as disponíveis para ações de jornada."

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
   >Uma pessoa/lead continua pela jornada independentemente de uma correspondência, exceto quando ocorre um erro. Uma ação de jornada não cria um novo registro de pessoa no Marketo Engage quando um registro correspondente não existe.

1. Insira a Munchkin ID, a ID do cliente e o Segredo do cliente para o serviço criado na instância externa do Marketo Engage.
1. Clique em **[!UICONTROL Conectar ao Marketo]**.
1. Clique em **[!UICONTROL Criar]**.

## Usar a conexão em uma ação de jornada

Quando um profissional de marketing usa uma ação do Marketo Engage em uma jornada, é possível configurar o nó usando o nome da conexão.

>[!NOTE]
>
>As ações do Marketo Engage executadas a partir de uma jornada não se aplicam aos limites da API REST para a instância conectada do Marketo Engage.

Com a integração concluída, as ações do Marketo Engage estão disponíveis em **Ações em:** nas propriedades do nó.

![lista de ações do Marketo](assets/marketo-actions-list.png){width="800" zoomable="yes"}
