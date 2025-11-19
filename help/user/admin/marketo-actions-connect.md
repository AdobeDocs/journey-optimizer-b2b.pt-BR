---
title: Ativar o Marketo Engage para oferecer suporte a ações de Jornada
description: Ative as conexões do Marketo Engage para oferecer suporte a ações do jornada, para que os profissionais de marketing possam coordenar campanhas entre o Marketo Engage e o Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---


# Ativar instâncias do Marketo Engage para dar suporte a ações

As ações do Marketo Engage são ações _com base em pessoas_ que permitem coordenar sua orquestração de marketing _com base em conta_ entre o Journey Optimizer B2B edition e seus esforços de marketing _com base em clientes potenciais_ no Marketo Engage. Use essas ações para orquestrar a associação de listas estáticas e colocar pessoas em campanhas.

Para usar as ações do Marketo Engage, um administrador cria primeiro um [serviço personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#) no Marketo Engage, que fornece as credenciais necessárias para autenticação.
Em seguida, um administrador de produto do Journey Optimizer B2B edition cria uma conexão com o Marketo Engage inserindo as credenciais.
Os usuários do Journey Optimizer B2B edition podem fazer referência à conexão para configurar ações do Marketo Engage em <!-- Person and -->jornadas de conta, como adicionar ou remover pessoas de listas do Marketo Engage ou adicioná-las a campanhas de solicitação.

A visibilidade do espaço de trabalho do Marketo Engage para ativos, como listas e campanhas, é regida pelas permissões de função atribuídas no serviço personalizado.

A mesma conexão pode ser usada várias vezes em uma jornada, e diferentes conexões do Marketo Engage podem coexistir em uma única jornada.

Quando uma ação é executada, ela usa a Política de seleção para determinar quais registros de pessoa no Marketo Engage e selecionar se vários identificadores existem no perfil de pessoa unificado. As opções incluem escolher os registros Marketo Engage mais antigos, mais recentes ou todos correspondentes. As pessoas continuam pela jornada independentemente de uma correspondência, exceto quando ocorre um erro.

## Configurar uma conexão do Marketo Engage

Configure uma instância remota do Marketo Engage para usar com as ações de jornada do Marketo Engage.

### Criar o serviço personalizado do Marketo Engage

1. Faça logon no Marketo Engage como administrador e crie um serviço personalizado.
1. Registre os seguintes valores para usar na conexão:

   * ID do Munchkin
   * ID do cliente
   * Segredo do cliente

### Adicionar a integração

![Adicionar detalhes da integração](assets/integration-connection-details.png)

1. No Journey Optimizer B2B edition, navegue até **Administração** > **Configurações**.
1. Selecione para a guia **Integrações**.
1. Clique em **[!UICONTROL Criar uma conexão]**.
1. Insira um nome (obrigatório) e uma descrição (opcional).
1. Selecione uma **Política de seleção** para corresponder a registros de pessoas.
1. Insira sua Munchkin ID, ID do cliente e Segredo do cliente.
1. Clique em **[!UICONTROL Conectar ao Marketo]**.
1. Clique em **[!UICONTROL Criar]**.

Quando um profissional de marketing usa uma ação do Marketo Engage em uma jornada, é possível configurar o nó usando o nome da conexão.

Com a integração concluída, as ações do Marketo Engage estão disponíveis em **Ações em:** nas propriedades do nó.

![lista de ações do Marketo](assets/marketo-actions-list.png)