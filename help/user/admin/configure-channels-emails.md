---
title: Configurações de canal de email
description: Defina configurações de delivery de email, limites de comunicação e protocolos de autenticação para otimizar a capacidade de delivery no Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: cbd9117daffc3820196c1d8436af2a568e1140b7
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# Configurações de canal de email

O Adobe Journey Optimizer B2B edition aproveita as funções de canal e o rastreamento de eventos no Marketo Engage. Os administradores devem garantir que as configurações de entrega e rastreamento estejam em vigor para habilitar a entrega por canal para profissionais de marketing. Para obter informações sobre os protocolos necessários para entrega e rastreamento de email por meio do Marketo Engage, consulte [Protocolos para rastreamento e entrega de email](../start/email-protocols.md).

## Configurações de entrega

As configurações padrão de email são usadas quando os profissionais de marketing criam um email em uma jornada de conta. Para examinar as configurações de entrega de email, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**. Em _[!UICONTROL Email]_, no painel de navegação, selecione **[!UICONTROL Configurações de Entrega]**.

![Acessar as configurações de entrega de email](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

As configurações são somente leitura no Journey Optimizer B2B edition. Clique em **[!UICONTROL Editar configurações]** na parte superior direita para acessar as opções de configuração na instância conectada do Marketo Engage.

>[!NOTE]
>
>Para acessar e editar essas configurações no Adobe Marketo Engage, é necessário ter permissões de administrador do produto.

Selecione cada uma das guias a seguir para analisar as configurações atuais.

### [!UICONTROL Parâmetros de cabeçalho de email] {#email-header}

Os parâmetros de cabeçalho de email definem os valores padrão para o seguinte:

* **[!UICONTROL Do Email]** - O endereço de email listado no campo _De_ no cabeçalho do email.

* **[!UICONTROL Do Rótulo]** - O nome exibido para o endereço do remetente do email.

* **[!UICONTROL Cancelar inscrição do HTML]** - O HTML (para clientes de email com suporte) que é exibido em emails não operacionais para explicar ações de cancelamento de inscrição para o destinatário. Esse texto e os links são anexados à parte inferior.

* **[!UICONTROL Texto de cancelamento de inscrição]** - O texto sem formatação exibido em emails não operacionais para explicar ações de cancelamento de inscrição ao destinatário. Esse texto e os links são anexados à parte inferior.

* **[!UICONTROL Exibir como página da Web HTML]** - A HTML (para clientes de email com suporte) usada para _Exibir como Página da Web_, que fornece um link para mostrar um email em um navegador.

* **[!UICONTROL Exibir como texto da página da Web]** - O texto sem formatação usado para _Exibir como Página da Web_, que fornece um link para mostrar um email em um navegador.

### [!UICONTROL Domínios de marca] {#branding-domains}

Para examinar os domínios de identidade visual, clique na guia **[!UICONTROL Domínios de identidade visual]**.

![Acessar as configurações dos domínios de identidade visual](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

Essa configuração define seu domínio primário para um ou mais espaços de trabalho na instância conectada do Marketo Engage. Novos emails usam este domínio como padrão, mas os profissionais de marketing podem [substituí-lo por email](../content/add-email.md#define-the-email-settings). Para obter mais informações sobre como definir o domínio de marca padrão, consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}.

>[!NOTE]
>
>Se você estiver comercializando várias marcas e quiser que cada uma tenha seus próprios links de rastreamento de marca, poderá adicionar outro domínio de marca. Para obter mais informações sobre como adicionar vários domínios de marca, consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}.

### [!UICONTROL Opções de cabeçalho personalizado] {#custom-header-options}

Para revisar as opções de cabeçalho personalizado, clique na guia **[!UICONTROL Opções de cabeçalho personalizado]**.

![Acessar as opções de cabeçalho personalizado](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

Quando a _[!UICONTROL Segurança de Transporte Restrita]_ está habilitada, ela garante que os links de rastreamento sejam servidos por HTTPS (somente para assinaturas com links de rastreamento protegidos por SSL).

## Limites de comunicação

Os limites de comunicação controlam o número de emails que um contato recebe da organização. Os limites definidos são compartilhados entre o Journey Optimizer B2B edition e a instância conectada do Marketo Engage. Definir esses limites garante que um lead não receba mais do que um número máximo de emails em um determinado período.

>[!AVAILABILITY]
>
>Os limites de comunicação estão disponíveis para ambientes Journey Optimizer B2B edition que são provisionados na [arquitetura simplificada](../simplified-architecture.md). Entre em contato com o Suporte da Adobe ou abra um tíquete de Suporte para habilitar o compartilhamento de limites de comunicação entre o Journey Optimizer B2B edition e uma ou mais instâncias do Marketo Engage.

Por exemplo, com um limite definido de cinco emails por dia, o sistema garante que um contato não receba um sexto email em um dia, suprimindo o sexto email. Com limites de comunicação compartilhados entre o Journey Optimizer B2B edition e o Marketo Engage, as regras de limite de comunicação são definidas em um local. O sexto email é suprimido, independentemente da ação de envio proveniente do Journey Optimizer B2B edition ou do Marketo Engage.

Todas as instâncias de produção do Marketo Engage têm limites de comunicação definidos por padrão (consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"} para obter mais informações). Para usar limites de comunicação compartilhada, defina as regras no Journey Optimizer B2B edition e estenda o compartilhamento desses limites para os códigos do Marketo Munchkin.

>[!IMPORTANT]
>
>Para estender o conjunto de regras de comunicação para os códigos Munchkin do Marketo, entre em contato com a equipe de gerenciamento de conta da Adobe. Normalmente, essa configuração faz parte do processo de integração.

Para revisar ou definir as regras de limite de comunicação, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**. Em _[!UICONTROL Email]_, no painel de navegação, selecione **[!UICONTROL Limites de comunicação]**.

![Acessar a configuração de limites de comunicação](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

Por padrão, há um conjunto de regras global em que você pode definir, ativar e desativar várias regras de acordo com seus requisitos. Clique no nome do conjunto de regras para exibir a lista de regras.

### Criar uma regra

1. Clique em **[!UICONTROL Criar regra]** na parte superior direita.

   ![Acessar a configuração de limites de comunicação](./assets/config-email-communication-limits-create-rule-select.png){width="600" zoomable="yes"}

1. Insira o **[!UICONTROL Nome da regra]**.

1. Defina o **[!UICONTROL Valor limite]**.

   Insira o valor ou clique na seta _Para cima_ ou _Para baixo_ à direita para aumentar ou diminuir o valor.

1. Escolha o valor **[!UICONTROL Redefinir frequência de limite]** de acordo com a maneira como você deseja definir o período de tempo para o limite.

   Você pode escolher _[!UICONTROL Por hora]_, _[!UICONTROL Diariamente]_, _[!UICONTROL Semanalmente]_ ou _[!UICONTROL Mensalmente]_.

   ![Acessar a configuração de limites de comunicação](./assets/config-email-communication-limits-create-rule-settings.png){width="600" zoomable="yes"}

1. Defina o valor **[!UICONTROL A cada]** de acordo com quantas unidades de frequência serão incluídas no período.

   Por exemplo, se você usar _Diariamente_ como frequência e definir esse valor como `3`, o período será definido como três dias.

1. Clique em **[!UICONTROL Criar regra]** na parte superior direita.

A nova regra está no estado _Rascunho_ e não é aplicada aos limites de comunicação até que você opte por ativá-la.

### Gerenciar regras

Desde que uma regra esteja no estado _Rascunho_, você pode editar a definição ou excluir a regra. Quando quiser que a regra seja aplicada, você poderá ativá-la. Clique no ícone _Mais menu_ (***...***) ao lado do nome da regra de rascunho na lista e escolha **[!UICONTROL Ativar]**.

![Clique no menu Mais para obter uma regra de limites de comunicação de rascunho](./assets/config-email-communication-limits-draft-more-menu.png){width="400" zoomable="yes"}

Em seguida, clique em **[!UICONTROL Ativar]** na caixa de diálogo de confirmação.

Uma regra ativa não pode ser editada ou excluída, só pode ser desativada. Para uma regra ativa que você deseja remover dos limites de comunicação aplicados, clique no ícone _Desativar_ ( ![Ícone Desativar](../assets/do-not-localize/icon-deactivate.svg) ) ao lado do nome da regra ativa.

![Clique no ícone Desativar para uma regra de limites de comunicação ativa](./assets/config-email-communication-limits-active-deactivate.png){width="400" zoomable="yes"}

Em seguida, clique em **[!UICONTROL Desativar]** na caixa de diálogo de confirmação.

A regra é exibida com um status _Inativo_. É semelhante a uma regra de rascunho, e você pode editá-la, excluí-la ou ativá-la quando necessário.

## SPF/DKIM

Melhore as taxas de delivery de email incorporando o SPF (Estrutura de Política do Remetente) e o DKIM (Domain Keys Identified Mail) às configurações de DNS. Essas tecnologias garantem aos recipients que seus emails não são spam. Para ajudar a impedir que os filtros de spam dos recipients rejeitem emails, verifique se o SPF e o DKIM estão configurados para os seus domínios.

Para examinar as configurações atuais, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**. Em _[!UICONTROL Email]_, no painel de navegação, selecione **[!UICONTROL SPF/DKIM]**.

![Acessar a configuração SPF/DKIM](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

As configurações são somente leitura no Journey Optimizer B2B edition. Clique em **[!UICONTROL Editar configurações]** na parte superior direita para acessar as opções de configuração na instância conectada do Marketo Engage.

>[!NOTE]
>
>Para acessar e editar essas configurações no Adobe Marketo Engage, é necessário ter permissões de administrador do produto.

### Configuração do SPF

O administrador da rede deve adicionar a seguinte linha às suas entradas de DNS:

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

Nesta entrada, substitua `[domain]` pelo domínio primário do seu site (como `company.com`) e `[corpIP]` pelo endereço IP do seu servidor de email corporativo (como `255.255.255.255`). Se você enviar emails de vários domínios por meio do Marketo Engage, adicione essa entrada para cada domínio em uma única linha.

Se você já tiver um registro SPF na sua entrada DNS, adicione o seguinte a ele:

`include:mktomail.com`

### Configuração do DKIM

O DKIM é um protocolo de autenticação usado pelos destinatários de email para validar o remetente da mensagem de email. Geralmente, melhora a capacidade de delivery de emails para a caixa de entrada, pois um receptor pode ter certeza de que a mensagem não é uma falsificação.

Quando a chave pública está em seu registro DNS e o domínio de envio está ativado na instância conectada do Marketo Engage, a assinatura personalizada do DKIM é usada para suas mensagens de saída. A assinatura personalizada do DKIM inclui uma assinatura digital criptografada com cada email enviado. Os destinatários podem descriptografar a assinatura digital procurando a _chave pública_ no DNS do domínio de envio. Se a chave no email corresponder à chave no registro DNS, o servidor de email de recebimento terá mais probabilidade de aceitar o email enviado pelo Marketo Engage.

Para obter mais informações sobre como configurar uma assinatura personalizada do DKIM para entrega de email, consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}.

## Atividade de bot

A atividade de bot de email pode inflar erroneamente seus dados de abertura e de clique.

O Marketo Engage usa dois métodos para confirmar a atividade do bot:

* **Corresponder com a lista do Interative Advertising Bureau (IAB)** - Atividades que correspondem a qualquer item na lista UA/IP (Agente do usuário/endereço IP) do IAB são marcadas como bots.

* **Corresponder ao Padrão de Proximidade** - Quando duas ou mais atividades ocorrem ao mesmo tempo (em um segundo), elas são identificadas como bots. Esse método considera os seguintes atributos para comparação:

   * ID do lead (deve ser o mesmo)
   * Ativo de email (deve ser o mesmo)
   * Clique em links ou e-mail aberto
   * Diferença de tempo (deve ser menor que um segundo)

Para atividades de clique em links de email e abertura de email, novos atributos são preenchidos com os seguintes valores:

* As atividades identificadas como bots têm a _Atividade de Bot_ como `True` e o _Padrão de Atividade de Bot_ como padrão/método identificado.
* As atividades identificadas como não sendo bots têm _Atividade de Bot_ como `False` e _Padrão de Atividade de Bot_ como `N/A`.
* As atividades que acontecem antes da introdução dos atributos têm _Atividade de bot_ como vazia (nula) e _Padrão de atividade de bot_ como vazia (nula)

Para examinar as configurações atuais, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**. Em _[!UICONTROL Email]_ no painel de navegação, selecione **[!UICONTROL Atividade de bot]**.

![Acessar a configuração da atividade de bot para entrega de email](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

As configurações são somente leitura no Journey Optimizer B2B edition. Clique em **[!UICONTROL Editar configurações]** na parte superior direita para acessar as opções de configuração na instância conectada do Marketo Engage.

>[!NOTE]
>
>Para acessar e editar essas configurações no Adobe Marketo Engage, é necessário ter permissões de administrador do produto.

Para obter mais informações sobre como configurar as opções de atividade de bot, consulte a [documentação do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}.
