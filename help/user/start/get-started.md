---
title: Orientação sobre a integração de administradores e profissionais de marketing
description: Como novo administrador ou usuário do Journey Optimizer B2B Edition, saiba mais sobre as principais áreas do processo de integração.
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 1e430af82b972dc73178161e64da10d1cdaaefaf
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 96%

---

# Orientação sobre integração

Os recursos e ferramentas que você pode usar no Adobe Journey Optimizer B2B Edition dependem da sua função na equipe. Com base na sua organização, os administradores podem definir vários tipos de usuários e conceder a eles acesso a determinados recursos, dependendo das suas permissões.

>[!TIP]
>
>Verifique também seus direitos de licença e a [descrição do produto](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondente sobre proteções de desempenho e limitações estáticas.

>[!BEGINTABS]

>[!TAB Administrador]

Antes que sua equipe possa começar a usar os recursos do Adobe Journey Optimizer B2B Edition, várias etapas são necessárias para preparar seu ambiente. Siga estas etapas para que o engenheiro de dados e o profissional de marketing possam começar a trabalhar com o Adobe Journey Optimizer B2B Edition.

Como administrador do sistema, você precisa entender os perfis de produtos e atribuir permissões para administração da sandbox e configuração de canais. Você também precisa configurar sandboxes e gerenciá-las para os perfis de produto disponíveis. Você pode atribuir membros da equipe aos perfis de produto. Os administradores de produto com acesso ao Adobe Admin Console podem gerenciar esses recursos. [Saiba mais sobre o Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html).

Saiba mais sobre o gerenciamento de acesso nas seguintes páginas:

1. **Criar sandboxes** para particionar suas instâncias em ambientes virtuais separados e isolados. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Colabore com o seu engenheiro de dados** para planejar e implementar a ativação do seu perfil e público-alvo B2B. Confira os blueprints publicados e siga as diretrizes de acordo com as suas necessidades. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Planeje e implemente a integração do Marketo Engage** para incorporar o esquema personalizado, a assimilação de perfis e contas e a orquestração de jornadas personalizadas para grupos de compras. [Saiba mais](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/b2b-journeys-with-marketo){target="_blank"}

1. **Configure o perfil de produto**. Um perfil de produto é um conjunto de direitos unitários na Adobe Experience Platform que permite aos usuários acessar determinadas funcionalidades ou objetos na interface. [Saiba mais](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configure permissões de usuário** para perfis de produtos, incluindo sandboxes, e dê acesso aos membros da sua equipe atribuindo-os a diferentes perfis de produtos. Esta tarefa é executada no Admin Console. [Saiba mais](../admin/user-management.md#create-a-user-group)

1. **Configure a entrega de email** no Marketo Engage, o que permite que sua equipe envie conteúdo de email de jornadas de conta. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **Configure serviços de SMS**. Configure um dos provedores de SMS terceirizados com suporte que oferecem serviços de mensagens de texto de forma independente e configure as credenciais da conta no Adobe Journey Optimizer B2B Edition. [Saiba mais](../admin/configure-channels-sms.md)

1. **Configure e habilite o uso do Adobe Experience Manager Assets** para equipes que usam o Assets as a Cloud Service para o gerenciamento centralizado de ativos digitais. [Saiba mais](../admin/configure-aem-repositories.md)

1. **Configure definições de eventos de experiência da Adobe Experience Platform (AEP)** para equipes responsáveis por criar jornadas de conta que acompanham eventos de experiência da AEP. [Saiba mais](../admin/configure-aep-events.md)

>[!TAB Profissional de marketing]

Como profissional de marketing ou _Profissional de jornada de contas_, você é responsável por criar jornadas e criar conteúdo. Você pode começar a trabalhar com o Adobe Journey Optimizer B2B Edition depois que o administrador do sistema e o engenheiro de dados prepararem seu ambiente e concederem acesso.

Consulte as seções a seguir para configurar sua primeira jornada, adicionar ativos e enviar conteúdo:

1. **Adicione públicos-alvo de contas**. O Journey Optimizer B2B Edition permite criar públicos-alvo de contas por meio de definições de segmentos diretamente do aplicativo e utilizá-los em suas jornadas de conta. [Saiba mais](../audiences/account-audience-overview.md)

1. **Crie grupos de compra**. Defina os principais componentes para atingir suas metas e objetivos comerciais e crie grupos de compras que identifiquem os membros para suas listas de contas de destino. [Saiba mais](../buying-groups/buying-groups-overview.md)

1. **Criar e gerenciar ativos**. O Adobe Experience Manager Assets fornece um repositório único e centralizado de ativos que você pode usar para preencher suas mensagens. [Saiba mais](../content/assets-overview.md)

1. **Adicione modelos de email personalizados e dinâmicos**. Aproveite a personalização e os recursos de conteúdo dinâmico do Journey Optimizer B2B Edition para adaptar sua mensagem ao seu público-alvo. [Saiba mais](../content/email-templates.md)

1. **Crie jornadas de conta para oferecer experiências personalizadas e contextuais**. O Journey Optimizer B2B Edition permite criar casos de uso de orquestração em tempo real com dados contextuais armazenados em eventos ou fontes de dados. Crie cenários avançados de várias etapas com os seguintes recursos:

   * Envie uma entrega unitária em tempo real acionada quando um evento é recebido ou em lote usando públicos-alvo da Adobe Experience Platform.

   * Use dados contextuais de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

   * Use as ações de canal integradas (email e SMS) para enviar mensagens projetadas no Journey Optimizer B2B Edition.

   * No mapa da jornada, crie casos de uso em várias etapas, adicione condições e envie mensagens personalizadas.

[Saiba mais](../journeys/journey-overview.md)

>[!ENDTABS]
