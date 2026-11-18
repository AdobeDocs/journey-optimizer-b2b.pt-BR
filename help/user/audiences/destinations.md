---
title: Destinos
description: Saiba mais sobre destinos compatíveis do Experience Platform e como conectar um destino para ativar listas de pessoas estáticas no Journey Optimizer B2B Edition.
feature: Audiences, Integrations
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 4%
---

# Destinos

Os destinos são integrações pré-criadas que permitem enviar [membros estáticos da lista de pessoas](./people-lists-static.md) e públicos-alvo de jornada de conta para plataformas sociais. Ativar uma lista estática para um destino mantém a associação em sincronia. À medida que as pessoas são adicionadas ou removidas da lista, elas são correspondentemente adicionadas ou removidas do público-alvo de destino e, por extensão, de qualquer campanha que o público-alvo alimente.

Há três maneiras de ativar pessoas para um destino conectado:

* **De uma lista estática** - Ative uma lista estática existente diretamente da guia **_[!UICONTROL Listas de pessoas]_**. Consulte [_Ativar para um destino_](./people-lists-static.md#static-list-activate).
* **De uma jornada de conta** - Adicione um nó de ação **_[!UICONTROL Ativar para destino]_** a um caminho de jornada para que as contas qualificadas sejam ativadas para o destino quando chegarem a esse nó. Consulte [_Ativar para ou desativar de um destino_](../journeys/action-nodes.md#activate-deactivate-destination).
* **De um grupo de compras** - Para preencher funções vazias em seus grupos de compras, você pode ativar um Público Correspondente do LinkedIn para direcionar os clientes potenciais que correspondem aos parâmetros do grupo de compras. Consulte [_Conta do LinkedIn correspondente a audience_s](../data/linkedin-account-matched-audiences.md#activate-buying-group).

>[!BEGINSHADEBOX]

## Permissões necessárias {#required-permissions}

O recurso de destino completo requer as seguintes [!DNL Adobe Experience Platform] permissões.

| Categoria | Permissão |
|--- |--- |--- |
| Sandboxes | Acesso à sandbox |
| Painéis | Ver Painéis de Controle Padrão |
| Painéis | Gerenciar painéis padrão |
| Destinos | Exibir destinos |
| Destinos | Gerenciar destinos |
| Destinos | Ativar destinos |
| Destinos | Ativar segmento sem mapeamento |
| Destinos | Gerenciar e ativar destino do conjunto de dados |
| Destinos | Criação de destino |
| Governança de dados | Exibir políticas de uso de dados |
| Governança de dados | Gerenciar políticas de uso de dados |
| Ingestão de dados | Exibir fontes |
| Ingestão de dados | Gerenciar fontes |
| Gerenciamento de perfil | Exibir configurações do perfil |
| Gerenciamento de perfil | Gerenciar configurações do perfil |

>[!ENDSHADEBOX]

## Destinos compatíveis {#supported-destinations}

Antes de ativar uma lista estática, um destino deve existir no catálogo de destinos. Na navegação à esquerda, expanda **[!UICONTROL Conexões]** e selecione **[!UICONTROL Destinos]**. Atualmente, [!DNL Journey Optimizer B2B Edition] oferece suporte ao **[!UICONTROL Destino (Social) de Audience]** Correspondente do LinkedIn. Consulte [_Públicos-alvo correspondentes da conta do LinkedIn_](../data/linkedin-account-matched-audiences.md) para

<!-- 
the following destinations:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Facebook Custom Audience]** (Social)
* **[!UICONTROL LinkedIn Matched Audience]** (Social)

![Access the available connector types](./assets/destinations-catalog.png){width="800" zoomable="yes"}

-->

>[!NOTE]
>
>O catálogo exibido não é o catálogo completo de destinos [!DNL Adobe Experience Platform]. Se você acessar destinos diretamente do [!DNL Experience Platform], verá um catálogo maior, mas apenas esses destinos estarão disponíveis no momento para ativação no [!DNL Journey Optimizer B2B Edition]. Destinos adicionais estão planejados para versões futuras.

## Configurar um destino {#set-up-destination}

Cada cartão de destino suportado mostra **[!UICONTROL Configurar novo destino]**. Configurar um destino é um pré-requisito para a ativação.

1. Na placa do conector, clique em **[!UICONTROL Configurar novo destino]**.

   ![Configurar um novo destino](./assets/destinations-configure-new.png){width="500"}

1. Selecione **[!UICONTROL Conta existente]** ou **[!UICONTROL Nova conta]** e insira os detalhes da conta, como o nome e a descrição da conta.

1. Clique em **[!UICONTROL Conectar ao destino]**.

   Um fluxo OAuth permite fazer logon na conta correspondente: LinkedIn, Google ou Facebook.

   >[!IMPORTANT]
   >
   >Neste ponto, não insira os _[!UICONTROL Detalhes do destino]_. Somente a conexão é necessária.

1. Preencha qualquer mapeamento de campo obrigatório entre os atributos de pessoas e os campos exigidos pelo destino.

1. Revise as configurações de governança de dados e ação de marketing e clique em **[!UICONTROL Salvar]**.

Para obter as etapas de instalação completas, consulte [Criar uma nova conexão de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} na documentação de [!DNL Experience Platform].

Quando configurado, o destino estará disponível para ativação em todos os locais que você puder selecionar um destino em [!DNL Journey Optimizer B2B Edition].

## Ativação e sincronização {#activation-sync}

A ativação é orientada por associação de lista estática, com uma sincronização bidirecional entre a lista e o público-alvo de destino:

* Adicionar uma pessoa à lista estática ativa-a no destino em 24 horas, adicionando-a ao público-alvo de destino e, subsequentemente, a qualquer campanha que o público-alvo alimente.
* Remover uma pessoa da lista estática desativa-a do destino. Eles são removidos do público-alvo de destino e de qualquer campanha conectada.
* A mesma lista pode ser ativada para vários destinos de uma só vez. A associação é sincronizada com todas elas.

>[!TIP]
>
>Para executar uma campanha do LinkedIn em relação a um segmento, ative a lista estática dessas pessoas para o destino do público-alvo correspondente do LinkedIn. Todos na lista são adicionados ao público-alvo correspondente no LinkedIn, onde uma campanha pode direcioná-los, e o público-alvo se mantém atualizado automaticamente à medida que a lista muda.
