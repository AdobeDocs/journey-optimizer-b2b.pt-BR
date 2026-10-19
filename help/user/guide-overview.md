---
title: Documentação do Adobe Journey Optimizer B2B Edition
description: 'Documentação completa do Journey Optimizer B2B Edition: explore os recursos disponíveis para integração, criação de grupos de compra, criação de jornadas de conta e gerenciamento de conteúdo.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: 87bce853d68d03eabceccf02ba80a8077dce206d
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 27%
---
# Documentação do Adobe Journey Optimizer B2B Edition

O [!DNL Adobe Journey Optimizer B2B Edition] é um aplicativo inédito que permite que as equipes de marketing e vendas orquestrem experiências baseadas em contas e qualifiquem grupos de compras para produtos específicos durante todo o ciclo de vida do cliente. Ele usa IA para envolver e qualificar grupos de compras em contas de destino, ajudando suas equipes a gerar um pipeline de maior qualidade e projetar estratégias melhores de aquisição, expansão e retenção. Ela também permite que insights compartilhados entre equipes de vendas e marketing.

Esta documentação fornece informações para dominar o aplicativo. Ele foi projetado para profissionais de marketing, representantes de desenvolvimento de negócios, analistas de dados e administradores operacionais.

## Novidades

Revise esta amostragem das adições e aprimoramentos mais recentes no aplicativo e na documentação do [!DNL Journey Optimizer B2B Edition].

>[!BEGINTABS]

>[!TAB jornadas de pessoas]

Orquestrar o marketing baseado em clientes potenciais com jornadas de pessoas, que usam públicos-alvo e dados do [!DNL Adobe Experience Platform] para envolver pessoas individuais. As jornadas de pessoa agora oferecem suporte a _Ouvir um evento_, ação externa, nós de caminhos divididos externos e reentrada de jornada. Use-as juntamente com jornadas de conta e grupos de compras para orquestrar a jornada de compra completa.

[!BADGE Saiba mais]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="Saiba mais sobre jornadas de pessoas"}

>[!TAB Caminhos divididos da variante]

Teste variações dentro de uma jornada de conta ou pessoa atribuindo contas ou pessoas a diferentes caminhos de jornada com base em porcentagens definidas por você. Em jornadas pessoais, a atribuição é determinística, de modo que cada pessoa sempre segue o mesmo caminho, que suporta experimentos controlados.

[!BADGE Saiba mais]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="Saiba mais sobre caminhos de divisão de variantes"}

>[!TAB Canal do WhatsApp]

Quando desenvolvedores e administradores de produtos configuram uma integração com uma conta do Meta Business Manager, os profissionais de marketing podem incluir mensagens do WhatsApp como um canal de conteúdo nas jornadas da conta usando a API da Meta Cloud. O WhatsApp se junta ao email e ao SMS como um canal disponível para fornecer conteúdo de jornada diretamente aos membros da conta.

[!BADGE Saiba mais]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="Saiba mais sobre o canal do WhatsApp"}

>[!TAB Modelos de IA de geração]

Agora, os designers de email podem selecionar entre modelos [!DNL Firefly] padrão, modelos [!DNL Firefly] personalizados treinados em ativos específicos da marca e modelos de imagem de terceiros aprovados ao gerar imagens para conteúdo de email. Essa seleção oferece às equipes controle sobre qual modelo se encaixa em seu cenário de design específico, desde necessidades gerais de conteúdo até casos de uso de marca ou especializados.

[!BADGE Saiba mais]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="Saiba mais sobre a seleção de modelo de IA gerativa"}

>[!TAB Otimização de tempo de envio]

Para os nós de ação _Enviar email_ no jornada de pessoas, agora você pode usar a otimização de tempo de envio para personalizar o tempo de entrega de email. O sistema prevê quando cada pessoa tem maior probabilidade de participar e agenda o delivery de acordo, em vez de enviar para todos os recipients ao mesmo tempo.

[!BADGE Saiba mais]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="Saiba mais sobre a otimização de tempo de envio"}

>[!TAB reentrada de Jornada]

Agora você pode enviar contas ou pessoas por meio de uma jornada de conta ou pessoa várias vezes. A reentrada aborda vários cenários, como a reavaliação de critérios de qualificação e fluxos de trabalho de criação reutilizáveis. Use as configurações de reentrada para definir critérios, limites e tempos de espera para que as contas ou pessoas se requalifiquem para a jornada de forma controlada.

[!BADGE Saiba mais]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="Saiba mais sobre a reentrada no jornada"}

>[!ENDTABS]

## Comece a explorar {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Notas de versão mais recentes

Mantenha-se atualizado com as notas de versão mais recentes, os novos recursos e as melhorias do [!DNL Adobe Journey Optimizer B2B Edition].

[Visualizar notas de versão](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Introdução

Revise as orientações de integração do [!DNL Journey Optimizer B2B Edition] para administradores e profissionais de marketing.

[Administradores](./setup-ultimate.md)
[Usuários](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Gerenciar seus dados

Ative os esquemas e campos XDM que deseja usar no [!DNL Adobe Journey Optimizer B2B Edition] e saiba como os dados funcionam no [!DNL Adobe Experience Platform].

[Exibir gerenciamento de campo XDM](./admin/xdm-field-management.md)
[Conjuntos de dados exportados](./data/aep-exported-datasets.md)
[Consultas do conjunto de dados](./data/aep-query-examples.md)
[Disponibilidade de dados e sincronização de tempo](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Canais de comunicação

Configure e gerencie e-mails, SMS, WhatsApp e outros canais para interações personalizadas com o cliente.

[Configurar canal de email](./admin/configure-channels-emails.md)
[Configurar canal de SMS](./admin/configure-channels-sms.md)
[Configurar canal do WhatsApp](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Criar uma jornada

Projete, orquestre, gerencie e otimize jornadas personalizadas de conta e pessoa.

[Explore jornadas](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg)

Compreender grupos de compra

Orientação detalhada sobre como criar, gerenciar e otimizar grupos de compras para um direcionamento eficaz.

[Saiba mais sobre grupos de compras](./buying-groups/buying-groups-overview.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## Demonstração de visão geral

Descubra os componentes de um grupo de compra e entenda os conceitos básicos da criação de uma jornada de conta.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## Explorar a documentação

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="Introdução"><br/>
      <strong>Introdução</strong><br/><a href="home-page.md">Logon e página inicial</a><br/><a href="./start/get-started.md">Orientação de integração</a> <br/><a href="./ai-coworker/ai-assistant-overview.md">Recursos de IA</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="Grupos de compra"><br/>
      <strong>Grupos de compra</strong><br/><a href="./buying-groups/buying-groups-overview.md">Visão geral dos grupos de compra</a><br/><a href="./buying-groups/buying-groups-role-templates.md">Modelos de função</a><br/><a href="./buying-groups/solution-interests.md">Interesses de solução</a><br/><a href="./buying-groups/buying-groups-create.md">Criar grupos de compra</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="Jornadas da conta"><br/>
      <strong>Jornadas de conta</strong><br/><a href="./journeys/journeys-overview.md">Visão geral das jornadas</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">Criar uma jornada de conta</a><br/><a href="./journeys/journey-nodes.md">Nós de jornada</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="Conteúdo da jornada"><br/>
      <strong>Conteúdo da Jornada</strong><br/><a href="./content/add-email.md">Canal de email</a><br/><a href="./content/generate-content-emails.md">Gerar conteúdo de email</a><br/><a href="./content/genstudio-email-workflow.md">experiências de email do GenStudio</a><br/><a href="./content/sms-authoring.md">Canal de SMS</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="Gerenciamento de conteúdo"><br/>
      <strong>Gestão de conteúdo</strong><br/><a href="./content/assets-overview.md">Visão geral do Assets</a><br/><a href="./content/email-templates.md">Modelos de email</a><br/><a href="./content/fragments.md">Fragmentos visuais</a><br/><a href="./content/conditional-content.md">Conteúdo condicional</a><br/><a href="./content/brand-themes.md">Temas de marca</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="Insights e painéis"><br/>
      <strong>Insights</strong><br/><a href="./dashboards/intelligent-dashboard.md">Painel inteligente</a><br/><a href="./dashboards/engagement-dashboard.md">Painel de envolvimento</a><br/><a href="./dashboards/buying-groups-dashboard.md">Painel de grupos de compras</a><br/><a href="./dashboards/journeys-dashboard.md">Painel do Jornada</a><br/><a href="./buying-groups/incrm-insights.md">Insights no CRM</a>
    </td>

</tr>
</table>

## Recursos adicionais

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">Vídeos e tutoriais</a> - <a href="https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">Descrição do produto</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/home" target="_blank">Documentação</a> - <a href="https://business.adobe.com/br/products/experience-platform/documentation-and-developer-resources.html" target="_blank">Recursos do desenvolvedor</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/home" target="_blank">Documentação</a> - <a href="https://experienceleague.adobe.com/pt-br/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">Tutoriais para desenvolvedores</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/en/docs/marketo/using/home?lang=pt-BR" target="_blank">Documentação do usuário</a> - <a href="https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/home" target="_blank">Documentação do desenvolvedor</a>
</td>
</tr></table>

