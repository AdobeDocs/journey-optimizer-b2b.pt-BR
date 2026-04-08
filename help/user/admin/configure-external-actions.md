---
title: Configuração de ações externas
description: Saiba como desenvolvedores, administradores e profissionais de marketing trabalham juntos para implementar, configurar e usar ações externas que conectam o Journey Optimizer B2B edition a serviços externos em jornadas de conta.
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Configuração de ações externas

As ações externas permitem que as jornadas de conta no Journey Optimizer B2B edition se conectem a sistemas externos diretamente da tela de jornada. Quando um público-alvo de conta atinge um nó de ação externa, o sistema faz uma chamada de saída assíncrona para um serviço externo configurado, transmitindo dados de atributos de público-alvo para contas, pessoas ou ambos. O serviço externo processa os dados e responde usando um retorno de chamada, retornando os dados e os metadados do público-alvo que podem ser usados para orientar a execução da jornada.

Esse recurso oferece suporte a dois tipos de nó do jornada:

* **Ação externa** - Chama um serviço externo e continua ao longo de um único caminho de saída. Ideal para _disparar e esquecer_ integrações, como a atualização de um registro CRM ou o acionamento de uma notificação downstream.
* **Caminhos divididos externos** - Chama um serviço externo e avalia a resposta para rotear contas ao longo de um dos vários caminhos definidos.

>[!NOTE]
>
>Os serviços de ação externa são compatíveis somente com jornadas de conta. Esses tipos de nó não estão disponíveis para jornadas de pessoas.

## Visão geral da implementação

A criação de ações externas exige coordenação entre três funções em sequência:

| | Função | Tarefa |
| ---- | ---- | ---- |
| 1 | Desenvolvedor | [Implementar e publicar o serviço externo](#implement-service) |
| 2 | Administrador | [Configurar a ação no Journey Optimizer B2B edition](#configure-action) |
| 3 | Profissional de marketing | [Adicionar um nó externo a uma jornada de conta](#add-journey-node) |

## Implementar o serviço externo {#implement-service}

O desenvolvedor deve criar e publicar um serviço Web voltado para o público que esteja em conformidade com a [Interface do Provedor de Serviços de Ações Externas do Adobe Journey Optimizer B2B edition](https://developer.adobe.com/journey-optimizer-b2b-apis/).

>[!NOTE]
>
>A função de retorno de chamada requer um token de portador. Recupere configurando as [credenciais de Servidor para Servidor do OAuth na Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) para sua Organização IMS.

Depois que o serviço estiver ativo, forneça o URL para a especificação OpenAPI e as credenciais de autenticação ao administrador do produto responsável pela configuração da ação.

## Configurar a ação {#configure-action}

Uma ação deve ser configurada e ativada antes que os profissionais de marketing possam usá-la em uma jornada. As ações são criadas no estado _Rascunho_ e suas alterações são salvas automaticamente. Permanece como rascunho até que você o ative.

>[!PREREQUISITES]
>
>Obtenha o URL para a especificação OpenAPI e as credenciais de autenticação do desenvolvedor antes de adicionar a configuração.
>
>Para definir e ativar uma ação externa, você deve ter a _[!UICONTROL Gerenciar configurações de administrador B2B]_ [permissão de produto](./user-management.md#b2b-product-permissions).

1. Vá para **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.

1. Clique em **[!UICONTROL Ações Externas]** no painel intermediário.

   ![Acessar o espaço de configuração de Ações Externas](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Clique em **[!UICONTROL Criar ação]** na parte superior direita.

1. Insira a URL para a especificação OpenAPI do seu serviço externo e clique em **[!UICONTROL Criar]**.

   ![Insira a URL do serviço](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >Seu serviço externo deve estar ativo e acessível para que esta etapa seja bem-sucedida.

1. Quando a URL for resolvida com êxito, revise os **[!UICONTROL Detalhes do serviço]**.

   Os detalhes do serviço são lidos diretamente da especificação OpenAPI quando a ação é criada. Não é possível alterar essas propriedades na configuração após a criação.

   | Propriedade | Descrição | Propriedade de especificação OpenAPI |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Nome] | Nome da ação | `info.title` |
   | [!UICONTROL Descrição] | Descrição da ação | `info.description` |
   | [!UICONTROL URL] | URL da especificação OpenAPI que define o serviço externo | `servers.url` |

1. Insira as credenciais de **[!UICONTROL Autenticação]** para o serviço externo (`components.securitySchemes`).

   >[!NOTE]
   >
   >Os campos de credencial exibidos dependem do mecanismo de autenticação definido no serviço externo. Os tipos compatíveis são Chave de API, OAuth2 e Autenticação básica de HTTP.

   ![Adicionar as credenciais de autenticação](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   Você pode alterar as credenciais conforme necessário quando a ação configurada estiver no status _Rascunho_ ou _Ativo_.

1. Clique em **[!UICONTROL Next]**.

1. Defina as propriedades **[!UICONTROL Configurações]** para definir como a ação troca dados com o serviço externo.

   >[!NOTE]
   >
   >As propriedades marcadas como _Estáticas_ não são atualizáveis no momento da configuração e se baseiam na definição do serviço.

   * **[!UICONTROL Tipo de ação]** (_Estática_) - O tipo de nó de jornada com suporte:

      * [!UICONTROL Ação externa] (`enableSplitPath` = falso)
      * [!UICONTROL Caminho dividido da ação externa] (`enableSplitPath` = verdadeiro)

     Não é possível alterar o tipo de ação após criar a configuração da ação.

   * **[!UICONTROL Acessadores]** (_Estático_) - (Somente caminho dividido de ação externa) As variáveis retornadas pelo serviço externo para estarem disponíveis como condições de caminho em um nó de caminho dividido externo. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Contexto de Jornada]** (_Estático_) - O escopo dos dados de público enviados na solicitação (`supportedEntityType`):

      * [!UICONTROL Conta] - Envia somente contas

      * [!UICONTROL Pessoas] - Envia somente pessoas

      * [!UICONTROL Pessoas na Conta] - Envia contas e pessoas relacionadas à conta

   * **[!UICONTROL Campos de Saída]** - Mapeie cada campo da tabela para um [campo XDM](../admin/xdm-field-management.md). Esses campos são enviados no corpo da solicitação para o serviço externo. Propriedades de definição de serviço: `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields`.

   ![Mapear campos de saída de ação externa](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Campos de Entrada]** - Mapeie cada campo da tabela para um [campo XDM atualizável](../admin/xdm-field-management.md#updatable-fields). Esses campos são preenchidos a partir da resposta do serviço externo. Propriedades de definição de serviço: `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields`. Atualizável após a criação.

   * **[!UICONTROL Parâmetros de cabeçalho]** - Insira um valor para cada linha a ser transmitida como um cabeçalho HTTP na solicitação. Propriedade de definição de serviço: `invocationPayloadDef.headers`.

   * **[!UICONTROL Tempo limite]** - Insira o número de minutos para aguardar o serviço externo invocar o retorno de chamada antes que a solicitação seja considerada com falha. Propriedade de definição de serviço: `timeout`.

   * **[!UICONTROL Atributos globais]** - Insira um valor para cada linha a ser incluída como um campo estático no corpo da solicitação. Propriedade de definição de serviço: `invocationPayloadDef.globalAttributes`.

   ![Parâmetros de cabeçalho de ação externa, tempo limite e atributos globais](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Clique na _Seta para trás_ para retornar à lista e manter a ação no estado _Rascunho_.

   Ou clique em **[!UICONTROL Ativar]** para alterar a configuração da ação para o estado _Ativo_. A ação externa configurada deve estar ativa para torná-la disponível para uso nas jornadas da conta.

## Adicionar um nó externo a uma jornada {#add-journey-node}

Após a ativação de uma ação, os profissionais de marketing podem adicionar um nó _[!UICONTROL Ação externa]_ ou _[!UICONTROL Caminho dividido externo]_ a qualquer jornada de conta. Para obter informações sobre como adicionar e usar esses nós na tela de jornada da conta, consulte [Nós externos](../journeys/external-nodes.md).
