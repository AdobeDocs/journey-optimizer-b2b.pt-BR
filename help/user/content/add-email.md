---
title: Adicionar um email à sua Jornada
description: Saiba como adicionar, definir e otimizar ações de email no Adobe Journey Optimizer B2B. Aprimore suas jornadas de conta com comunicações direcionadas por email.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 828419933a6552b09d05a8be2a14676a87046a26
workflow-type: tm+mt
source-wordcount: '1346'
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

     Essa opção permite gerenciar o conteúdo de email nativamente no Journey Optimizer B2B edition. Clique em **[!UICONTROL Criar email]** para abrir o diálogo _Criar novo email_. Você pode criar um novo ativo de conteúdo de email ou duplicar um ativo de conteúdo de email existente.

     +++Novo email

     Quando quiser criar um email usando uma tela vazia ou um modelo de email, use a opção _[!UICONTROL Novo email]_.

      1. Na caixa de diálogo, escolha **[!UICONTROL Novo email]**.

      1. Insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

         ![Caixa de diálogo Criar novo email - novo email](assets/create-new-email.png){width="400"}

      1. Clique em **[!UICONTROL Criar]**.

         Na seção _[!UICONTROL Propriedades de email]_ da página de conteúdo de email, os campos _[!UICONTROL Do email]_ e _[!UICONTROL Responder para endereço]_ já estão configurados. Você pode inserir valores para os campos _[!UICONTROL De nome]_ e _[!UICONTROL Descrição]_ (opcional).

      1. Clique em **[!UICONTROL Editar email]** para definir as [configurações](#define-the-email-settings) do email e criar o [conteúdo](./email-authoring.md).

     +++

     +++Duplicar email existente

     Quando quiser criar um email usando um email existente da jornada atual ou de outra jornada, use a opção _[!UICONTROL Duplicar email existente]_. Você pode fazer alterações no email duplicado de acordo com seu objetivo para o nó de jornada.

      1. Na caixa de diálogo _[!UICONTROL Criar novo email]_, escolha **[!UICONTROL Duplicar email existente]**.

      1. Para duplicar o email **[!UICONTROL existente]**, clique no ícone _Seleção_ ( ![Ícone Seleção](../assets/do-not-localize/icon-email-select.svg) ) e selecione o email que deseja duplicar e usar para o nó de jornada.

         Você pode filtrar a lista de emails inserindo uma cadeia de texto no campo de pesquisa para corresponder ao nome do email.

         ![Selecionar email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

         Marque a caixa de seleção do email que você deseja duplicar e clique em **[!UICONTROL Selecionar]**.

      1. Insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

         ![Caixa de diálogo Criar novo email - duplicar email existente](assets/create-new-email-duplicate.png){width="400"}

      1. Clique em **[!UICONTROL Criar]**.

         Na seção _[!UICONTROL Propriedades de email]_ da página de conteúdo de email, os campos _[!UICONTROL Do email]_ e _[!UICONTROL Responder para endereço]_ já estão configurados. Você pode inserir valores para os campos _[!UICONTROL De nome]_ e _[!UICONTROL Descrição]_ (opcional).

      1. Se necessário, clique em **[!UICONTROL Editar email]** para modificar as [configurações](#define-the-email-settings) e o [conteúdo](./email-authoring.md) do email.

     +++

   * Escolha **[!UICONTROL Selecionar email do Adobe Marketo Engage]** para usar um dos emails pré-criados no Marketo Engage e enviá-lo como parte da jornada.

     Se você tiver mais de um espaço de trabalho disponível na instância conectada do Market Engage, selecione o espaço de trabalho. Em seguida, selecione o email aprovado que deseja enviar para o nó do jornada.

     ![Selecionar email do Marketo Engage](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Com essa opção, o nó é definido e o conteúdo do email não precisa de mais definição na jornada.

## Definir as configurações de email

Com a guia **[!UICONTROL Detalhes]** selecionada no painel _Resumo_ à direita, role até o final para exibir e definir as configurações de email.

![Configurações de email](./assets/email-summary-details-settings.png){width="700" zoomable="yes"}

| Opção | Descrição |
| ------ | ----------- |
| [!UICONTROL De nome] | O nome do remetente usado no cabeçalho do email. Insira o nome do remetente como deseja que ele apareça para o destinatário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Do email] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido nas [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Endereço para resposta] | O endereço do remetente usado no cabeçalho do email. O valor padrão é preenchido a partir das [configurações de entrega de canal de email](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Do Rótulo]). Insira o endereço de email que você deseja preencher se o recipient usar a função de resposta (pode ser diferente ou igual ao endereço do remetente). Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo. |
| [!UICONTROL Linha de assunto] | O texto exibido no campo de assunto do email. O valor padrão é preenchido com base no texto inserido na caixa de diálogo _[!UICONTROL Criar novo email]_. Você pode alterar o texto, se necessário. Clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) para usar um token de personalização no campo.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Domínio de marca] | Se você tiver mais de um [domínio de identidade visual](../admin/configure-channels-emails.md#branding-domains) definido no sistema, selecione o domínio de identidade visual a ser usado para enviar o email. Use um domínio de marca específico para enviar emails que parecem vir da sua marca, em vez da empresa como um todo. Ele cria confiança com a marca, personaliza a experiência de email e aumenta as taxas de abertura e resposta. |
| [!UICONTROL IP dedicado] | Se tiver mais de um endereço IP dedicado definido, selecione um endereço IP dedicado para usar ao enviar o email. Ao usar um IP dedicado específico para seus programas, você pode rastrear e monitorar a capacidade de entrega com mais precisão e responder rapidamente a qualquer alteração em suas métricas de entrega. Para obter mais informações sobre como adicionar um IP dedicado para a instância conectada do Marketo Engage, consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/use-your-dedicated-ip-addresses-to-send-emails){target="_blank"}. |
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

   * `The opt-out link is not present in the email body`: Adicionar um link de cancelamento de assinatura ao corpo do email é uma prática recomendada.

     >[!NOTE]
     >
     >As mensagens de email de estilo de marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais.

   * `Text version of HTML is empty`: não se esqueça de definir uma versão de texto do corpo do email, que é usada quando o conteúdo do HTML não pode ser exibido.

   * `Empty link is present in email body`: verifique se todos os links no seu email estão corretos.

   * `Email size has exceeded the limit of 100KB`: Para uma entrega ideal, certifique-se de que o tamanho do seu email não exceda 100KB.

* **_Erros_** que impedem que você teste ou ative a jornada/campanha enquanto não forem resolvidos, como:

   * `From name is empty`: O campo _De_ do email (obrigatório) não está definido.

   * `The subject line is missing`: A linha de assunto do email (obrigatória) não está definida.

   * `The email version of the message is empty`: O conteúdo do email não está definido.
