---
title: Configurações de SMS
description: Saiba como configurar conexões com provedores de SMS compatíveis para uso por mensagens SMS do Journey Optimizer B2B edition.
feature: Setup
source-git-commit: c3352db2235af08e31ba7e4d8690bc9e330dd41f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Configurações de SMS

O Adobe Journey Optimizer B2B edition envia mensagens de texto por meio de provedores de serviços SMS (ou provedores de gateway SMS). Antes de criar a mensagem SMS, configure o provedor de serviços nas configurações do _Administrador_.

## Provedores de serviços de gateway de SMS

Atualmente, o Adobe Journey Optimizer B2B edition está integrado a provedores de terceiros que oferecem serviços de mensagens de texto de forma independente. Os provedores de mensagens de texto compatíveis são Sinch, Twilio e Infobip.

Antes de configurar um canal SMS no Adobe Journey Optimizer B2B edition, você deve criar uma conta com um desses provedores para obter o token da API e a ID do serviço. Essas credenciais são necessárias para configurar a conexão entre o Adobe Journey Optimizer B2B edition e o provedor aplicável.

>[!IMPORTANT]
>
>O uso dos serviços de mensagens de texto está sujeito a termos e condições adicionais do provedor aplicável. Como soluções de terceiros, o Sinch, o Twilio e o Infobip estão disponíveis para usuários do Adobe Journey Optimizer B2B edition por meio de uma integração. A Adobe não controla e não é responsável por produtos de terceiros. Em caso de problemas ou solicitações de assistência relacionados aos serviços de mensagens de texto (SMS), entre em contato com seu provedor.

## Verificar uma configuração de API de SMS existente

>[!NOTE]
>
>As configurações descritas podem ser acessadas somente pelos usuários com privilégios de administrador de SMS.

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Canais]**.

   ![Acessar a configuração de credenciais de API de SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. No painel de navegação, selecione **[!UICONTROL Credenciais da API]**.

   A página lista as configurações de API disponíveis para sua instância.

1. Se necessário, clique no ícone _Filtro_ ( ![Ícone Mostrar ou ocultar filtros](../assets/do-not-localize/icon-filter.svg) ) e selecione opções para exibir a lista de credenciais de API configuradas pelo provedor de serviços SMS ou criador.

   ![Clique no ícone Filtro para refinar a lista de credenciais de API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Criar novas credenciais de API para um provedor de serviços SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Para configurar o Sinch como seu provedor de SMS com o Adobe Journey Optimizer B2B edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Sinch](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Sinch` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a credencial da API.

   * **[!UICONTROL ID de Serviço]** e **[!UICONTROL Token de API]** - Acesse a página de APIs da sua conta Sinch (você pode encontrar suas credenciais na guia SMS).

   Para obter mais informações sobre como encontrar essas informações para sua conta Sinch, consulte a [documentação do desenvolvedor da Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Clique em **[!UICONTROL Enviar]** quando os detalhes de configuração das suas credenciais de API estiverem concluídos.

>[!TAB Twilio]

_Para configurar o Twilio como seu provedor de SMS com o Adobe Journey Optimizer B2B edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Twilio` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a definição de credencial de API.

   * **[!UICONTROL SID da Conta]** e **[!UICONTROL Token de Autenticação]** - Acesse o painel _Informações da Conta_ da página Painel do Console do Twilio para encontrar suas credenciais.

   Para obter mais informações sobre como encontrar essas informações para sua conta do Twilio, consulte a [Central de Ajuda do Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Clique em **[!UICONTROL Enviar]** no canto superior direito da página quando os detalhes de configuração das suas credenciais de API forem concluídos.

>[!TAB Infobip]

_Para configurar o Infobip como seu provedor de SMS com o Adobe Journey Optimizer B2B edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Infobip` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a definição de credencial de API.

   * **[!UICONTROL URL de base de API]** e **[!UICONTROL chave de API]** - Acesse a página inicial da interface da Web ou a página de gerenciamento de chaves de API da sua conta Infobip para encontrar suas credenciais.

   Para obter mais informações sobre como encontrar essas informações para sua conta Infobip, consulte a [documentação do Infobip](https://www.infobip.com/docs/api/_blank).

1. Clique em **[!UICONTROL Enviar]** no canto superior direito da página quando os detalhes de configuração das suas credenciais de API forem concluídos.

>[!ENDTABS]

Ao clicar em _[!UICONTROL Enviar]_, as credenciais são imediatamente validadas e salvas, redirecionando você para a página de listagem _[!UICONTROL credenciais de API]_. Se as credenciais enviadas forem inválidas, o sistema exibirá uma mensagem de erro na página de listagem. Nesse caso, você pode optar por cancelar a configuração ou atualizá-la e enviar novamente.
