---
title: Adicionar um email à sua Jornada
description: Saiba como adicionar, definir e otimizar ações de email no Adobe Journey Optimizer B2B. Aprimore suas jornadas de conta com comunicações direcionadas por email.
feature: Email Authoring, Content
source-git-commit: 6517a953692a56bd31c5b0f2fa5f15f40c6743b5
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Adicionar um email à sua jornada

Use o Adobe Journey Optimizer B2B edition para enviar mensagens de email aos seus clientes por meio de jornadas de conta. Você pode optar por criar, personalizar e visualizar mensagens no espaço de design de email. Como alternativa, você pode optar por enviar um email que já está definido na instância conectada do Marketo Engage.

>[!NOTE]
>
>Se estiver enviando um email pela primeira vez, verifique se o canal de email está configurado no Adobe Marketo Engage. Para saber mais, consulte [Protocolos de rastreamento e entrega de email](../start/email-protocols.md).

## Adicionar um nó de ação de email em uma jornada

Você pode configurar entregas de email em uma jornada ao [adicionar um nó _[!UICONTROL Executar uma ação]_](../journeys/action-nodes.md) e fazer o seguinte:

1. Para o destino _[!UICONTROL Ação em]_, escolha **[!UICONTROL Pessoas]**.

1. Para a _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Enviar email]**.

1. Para a _[!UICONTROL origem do email]_, escolha como você deseja originar o email a ser enviado.

   ![Realizar uma ação - enviar um email](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Escolha **[!UICONTROL Criar novo email]** para criar o email nativamente no Journey Optimizer B2B edition.

     Essa opção permite gerenciar o conteúdo de email nativamente no Journey Optimizer B2B edition. Clique em **[!UICONTROL Criar email]** para abrir o diálogo _Criar novo email_. Você pode criar um novo ativo de conteúdo de email<!-- or duplicate an existing email content asset-->.

     Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**, depois clique em **[!UICONTROL Criar]**.

     ![Caixa de diálogo Criar novo email - novo email](assets/create-new-email-no-duplicate.png){width="400"}

     Na seção _[!UICONTROL Propriedades de email]_ da página de conteúdo de email, os campos _[!UICONTROL Do email]_ e _[!UICONTROL Responder para endereço]_ já estão configurados. Você pode inserir valores para os campos _[!UICONTROL De nome]_ e _[!UICONTROL Descrição]_ (opcional).

     Defina as [configurações](#define-the-email-settings) do email e clique em **[!UICONTROL Editar conteúdo do email]** para [criar o conteúdo](./email-authoring.md).

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Escolha **[!UICONTROL Selecionar email do Adobe Marketo Engage]** para usar um dos emails pré-criados no Marketo Engage e enviá-lo como parte da jornada.

     ![Selecionar email do Marketo Engage](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Com essa opção, o nó é definido e o conteúdo do email não precisa de mais definição na jornada.

## Definir as configurações de email

Com a guia **[!UICONTROL Detalhes]** selecionada no painel _Resumo_ à direita, role até a parte inferior para exibir e definir as opções de email.

![Configurações de email](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Opção | Descrição |
| ------ | ----------- |
| [!UICONTROL De nome] | O nome do remetente usado no cabeçalho do email. Insira o nome do remetente como deseja que ele apareça para o destinatário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Do email] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido nas [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Endereço para resposta] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido a partir das [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Do Rótulo]). Insira o endereço de email que você deseja preencher se o recipient usar a função de resposta (pode ser diferente ou igual ao endereço do remetente). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Linha de assunto] | O texto exibido no campo de assunto do email. O valor padrão é preenchido com base no texto inserido na caixa de diálogo _[!UICONTROL Criar novo email]_. Você pode alterar o texto, se necessário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Email operacional] | Marque a caixa de seleção se desejar designar o email como operacional. Os emails operacionais são excluídos das listas de recusa/cancelamento de inscrição e dos limites de comunicação. Selecione essa opção somente quando o recipient não puder considerar a mensagem de email como uma mensagem comercial não solicitada (SPAM). |
| [!UICONTROL Incluir exibição como página da Web] | Marque a caixa de seleção para incluir um link para uma página da Web gerada a partir do conteúdo da mensagem de email. As mensagens de email têm recursos mais limitados do que as páginas da Web, portanto, são úteis para o JavaScript, CSS estendido e formulários. O texto usado para gerar o link está configurado nas [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Exibir como página da Web do HTML] e [!UICONTROL Exibir como texto da página da Web]). |
| [!UICONTROL Desabilitar o rastreamento de aberturas] | Marque a caixa de seleção quando não quiser rastrear a atividade de abertura de emails. Com a função desativada, as contagens de atividades de email abertas são aumentadas somente quando uma pessoa única abre o email. Você pode [gerenciar o rastreamento de links de conteúdo de email](./email-authoring.md#content-authoring---link-tracking) ao criar o conteúdo do corpo do email. |
| [!UICONTROL Pré-cabeçalho] | Marque a caixa de seleção para incluir um pré-cabeçalho. Um pré-cabeçalho é o texto curto de resumo exibido após a linha de assunto em alguns clientes de email. Normalmente, fornece um breve resumo do email e geralmente é uma frase única. Insira o texto de resumo no campo <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Campos usados como endereços CC] | Se disponível, selecione até 25 campos de Cliente Potencial ou Empresa configurados no Marketo Engage usando o tipo `Email`. |

## Verificar alertas

À medida que você cria o conteúdo da sua mensagem de email, os alertas são exibidos na interface (canto superior direito da página) quando as principais configurações estão ausentes. Se você não vir esse botão, não há problemas detectados.

![Alertas de email](./assets/email-alerts.png){width="600" zoomable="yes"}

Dois tipos de alertas podem ser detectados:

* **_Avisos_** que se referem a recomendações e práticas recomendadas, como:

   * `The opt-out link is not present in the email body`: adicionar um link de cancelamento de assinatura ao corpo do email é uma prática recomendada.

     >[!NOTE]
     >
     >As mensagens de email de estilo de marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais.

   * `Text version of HTML is empty`: não se esqueça de definir uma versão de texto do corpo do email, que é usada quando o conteúdo do HTML não pode ser exibido.

   * `Empty link is present in email body`: verifique se todos os links no seu email estão corretos.

   * `Email size has exceeded the limit of 100KB`: para uma entrega ideal, verifique se o tamanho do seu email não excede 100KB.

* **_Erros_** que impedem que você teste ou ative a jornada/campanha enquanto não forem resolvidos, como:

   * `The subject line is missing`: a linha de assunto do email é obrigatória.

   * `The email version of the message is empty`: este erro é exibido quando o conteúdo do email não foi configurado.
