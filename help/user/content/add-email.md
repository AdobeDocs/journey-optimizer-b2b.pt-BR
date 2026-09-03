---
title: Adicionar um email à sua Jornada
description: Para um nó de ação de envio de email em uma jornada, crie novos emails ou duplique os existentes para usar em comunicações direcionadas no Journey Optimizer B2B edition.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
autotag-review: 2026-03-30T22:38:56.688Z
TQID: https://experienceleague.adobe.com/8poXn9D7fkr-5yQBUn3dAxV0izKGfW-U8Qf0gG4aRWw
source-git-commit: f67a6703d32e133be7c3422e1d5ceb6099da849e
workflow-type: tm+mt
source-wordcount: 1042
ht-degree: 0%

---

# Adicionar um email à sua jornada

Use o Adobe Journey Optimizer B2B edition para enviar mensagens de email aos seus clientes por meio de jornadas de conta. Você pode optar por criar, personalizar e visualizar mensagens no espaço de design de email. Depois que os emails estiverem no jornada, monitore o envio, a entrega e o envolvimento no [Relatório de desempenho de email](../dashboards/email-performance-dashboard.md).

>[!NOTE]
>
>Se estiver enviando um email pela primeira vez, verifique se o canal de email está configurado. Para saber mais, consulte [Protocolos de rastreamento e entrega de email](../start/email-protocols.md).
>
>Para obter detalhes sobre como as preferências de consentimento de email são avaliadas no momento da entrega, consulte [Preferências de consentimento](./channels-consent-preferences.md).

## Adicionar um nó de ação de envio de email {#send-email-node}

Você pode configurar entregas de email em uma jornada ao [adicionar um nó _[!UICONTROL Executar uma ação]_](../journeys/action-nodes.md) e fazer o seguinte:

1. _(Somente jornadas de Conta)_ Para a _[!UICONTROL Ação em]_ destino, escolha **[!UICONTROL Pessoas]**.

1. Para a ação, escolha **[!UICONTROL Enviar email]**.

1. Clique em **[!UICONTROL Criar email]**.

   ![Realizar uma ação - enviar um email](assets/journey-node-send-email.png){width="500"}

1. Na caixa de diálogo _Criar novo email_, opte por criar um novo ativo de conteúdo de email ou duplicar um ativo de conteúdo de email existente.

   * Escolha a opção **[!UICONTROL Novo email]** quando quiser criar um email usando uma tela vazia ou um modelo de email.

     ![Caixa de diálogo Criar novo email - novo email](assets/create-new-email.png){width="400"}

     * Insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

     * Clique em **[!UICONTROL Criar]**.

   * Escolha a opção **[!UICONTROL Duplicar email existente]** quando quiser criar um email usando um email existente da jornada atual ou de outra jornada.

     Você pode fazer alterações no email duplicado de acordo com seu objetivo para o nó de jornada.

     * Para duplicar o email **[!UICONTROL existente]**, clique no ícone _Seleção_ ( ![Ícone Seleção](../assets/do-not-localize/icon-email-select.svg) ) e selecione o email que deseja duplicar e usar para o nó de jornada.

       Você pode filtrar a lista de emails inserindo uma cadeia de texto no campo de pesquisa para corresponder ao nome do email. Marque a caixa de seleção do email que você deseja duplicar e clique em **[!UICONTROL Selecionar]**.

       ![Selecionar email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

     * Insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

       ![Caixa de diálogo Criar novo email - duplicar email existente](assets/create-new-email-duplicate.png){width="400"}

     * Clique em **[!UICONTROL Criar]**.

1. Clique em **[!UICONTROL Editar email]** para definir as [configurações](#email-settings) e o [conteúdo](./email-authoring.md) do email.

   ![Nó de jornada de email de envio - editar email](assets/journey-node-send-email-edit-email.png){width="500"}

## Definir as configurações de email {#email-settings}

Com a guia **[!UICONTROL Detalhes]** selecionada no painel _Resumo_ à direita, role até o final para exibir e definir as configurações de email.

![Configurações de email](./assets/email-summary-details-settings.png){width="700" zoomable="yes"}

| Opção | Descrição |
| ------ | ----------- |
| [!UICONTROL De nome] | O nome do remetente usado no cabeçalho do email. Insira o nome do remetente como deseja que ele apareça para o destinatário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Do email] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido nas [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Endereço para resposta] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido a partir das [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Do Rótulo]). Insira o endereço de email que você deseja preencher se o recipient usar a função de resposta (pode ser diferente ou igual ao endereço do remetente). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Linha de assunto] | O texto exibido no campo de assunto do email. O valor padrão é preenchido com base no texto inserido na caixa de diálogo _[!UICONTROL Criar novo email]_. Você pode alterar o texto, se necessário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Domínio de marca] | Se você tiver mais de um [domínio de identidade visual](../admin/configure-channels-emails.md#branding-domains) definido no sistema, selecione o domínio de identidade visual a ser usado para enviar o email. Use um domínio de marca específico para enviar emails que parecem vir da sua marca, em vez da empresa como um todo. Ele cria confiança com a marca, personaliza a experiência de email e aumenta as taxas de abertura e resposta. |
| [!UICONTROL Email operacional] | Marque a caixa de seleção se desejar designar o email como operacional. Os emails operacionais são excluídos das listas de recusa/cancelamento de inscrição e dos limites de comunicação. Selecione essa opção somente quando o recipient não puder considerar a mensagem de email como uma mensagem comercial não solicitada (SPAM). |
| [!UICONTROL Incluir exibição como página da Web] | Marque a caixa de seleção para incluir um link para uma página da Web gerada a partir do conteúdo da mensagem de email. As mensagens de email têm recursos mais limitados do que as páginas da Web, portanto, são úteis para o JavaScript, CSS estendido e formulários. O texto usado para gerar o link está configurado nas [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Exibir como página da Web do HTML] e [!UICONTROL Exibir como texto da página da Web]). |
| [!UICONTROL Desabilitar o rastreamento de aberturas] | Marque a caixa de seleção quando não quiser rastrear a atividade de abertura de emails. Com a função desativada, as contagens de atividades de email abertas são aumentadas somente quando uma pessoa única abre o email. Você pode [gerenciar o rastreamento de link do conteúdo de email](./email-authoring.md#edit-linked-url-tracking) ao criar o conteúdo do corpo do email. |
| [!UICONTROL Pré-cabeçalho] | Marque a caixa de seleção para incluir um pré-cabeçalho. Um pré-cabeçalho é o texto curto de resumo exibido após a linha de assunto em alguns clientes de email. Normalmente, fornece um breve resumo do email e geralmente é uma frase única. Insira o texto de resumo no campo <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |

<!-- 
Removed, but may reappear elsewhere
| [!UICONTROL Dedicated IP] | If you have more than one dedicated IP addresses defined, select a dedicated IP address to use for sending the email. When you use a specific dedicated IP for your programs, you can track and monitor deliverability more closely and respond quickly to any changes in your delivery metrics. For more information about adding a dedicated IP for the connected Marketo Engage instance, refer to the [Marketo Engage documentation](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/use-your-dedicated-ip-addresses-to-send-emails){target="_blank"}.|
| [!UICONTROL Fields used as CC addresses] | If available, select up to 25 Lead or Company fields that are set up in Marketo Engage using the `Email` type.  |
-->

## Verificar alertas {#check-alerts}

À medida que você define as configurações e o conteúdo de email, os alertas são exibidos na interface (canto superior direito da página) quando as configurações principais estão ausentes. Se você não vir esse botão, não há problemas detectados.

![Alertas de email](./assets/email-alerts.png){width="600" zoomable="yes"}

Há dois tipos de alertas:

* **_Avisos_** que se referem a recomendações e práticas recomendadas, como:

  * `The opt-out link is not present in the email body`: adicionar um link para cancelar inscrição ao corpo do email é uma prática recomendada.

    >[!NOTE]
    >
    >As mensagens de email de estilo de marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais.

  * `Text version of HTML is empty`: defina uma versão de texto do corpo do email, que é usada quando o conteúdo do HTML não pode ser exibido.

  * `Empty link is present in email body`: verifique se todos os links no seu email estão corretos.

  * `Email size has exceeded the limit of 100KB`: Para uma entrega ideal, certifique-se de que o tamanho do seu email não exceda 100KB.

* **_Erros_** que impedem que você teste ou ative a jornada/campanha enquanto não forem resolvidos, como:

  * `From name is empty`: O campo _De_ do email (obrigatório) não está definido.

  * `The subject line is missing`: A linha de assunto do email (obrigatória) não está definida.

  * `The email version of the message is empty`: O conteúdo do email não está definido.
