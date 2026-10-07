---
title: Consentimento de mensagens do canal
description: Saiba como o Journey Optimizer B2B Edition lê as preferências de consentimento do perfil XDM do AEP e aplica a aceitação e a recusa no momento da entrega da mensagem para canais de email, SMS e WhatsApp.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
    internal-label: Communication channels
  - id: d77af7eb-afc3-53f3-a50c-dabc0d05ecfd
    internal-label: Channels
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
    internal-label: Administration
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
    internal-label: Email channel
  - id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
    internal-label: SMS channel
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
    internal-label: Setup
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 21fbce544faf291ad01a3301a9981add95442097
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 1%
---
# Consentimento de mensagem de canal

O Adobe Journey Optimizer B2B Edition lê as preferências de consentimento por pessoa armazenadas nos perfis XDM do Adobe Experience Platform e as impõe no momento da entrega da mensagem, como parte dos [controles de governança](../admin/governance.md) do aplicativo. As pessoas que optaram por não participar de um canal são excluídas da entrega antes que o conteúdo seja enviado do canal ou do provedor de mensagens downstream.

As seções a seguir descrevem como o Journey Optimizer B2B Edition avalia o consentimento no momento do envio da mensagem para cada canal compatível.

## Email {#email}

O Journey Optimizer B2B Edition avalia o seguinte atributo XDM para consentimento de email ao enviar mensagens no [canal de email](../admin/configure-channels-emails.md):

| Atributo XDM | `y` | `n` | Nenhum valor |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | Optado | Recusado | Optado |

Considere o seguinte para consentimento por email:

* As pessoas que optaram por não participar do email globalmente podem receber emails marcados como operacionais.
* As preferências de nível de assinatura não são compatíveis.

Para analisar a atividade de cancelamento de inscrição para emails enviados, consulte o [Relatório de desempenho de email](../dashboards/email-performance-dashboard.md).

## SMS {#sms}

O Journey Optimizer B2B Edition avalia os seguintes atributos XDM para consentimento de SMS ao enviar mensagens pelo [canal de SMS](../admin/configure-channels-sms.md):

| Atributo XDM | `y` | `n` | Nenhum valor |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | Optado | Recusado | Recusado |
| `consents.marketing.subscriptions.<senderID>` | Optado | Recusado | Recusado |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | Optado | Recusado | Recusado |

Considere o seguinte para consentimento do SMS:

* Quando um registro de cliente potencial (pessoa) é recusado pelo SMS, ele é totalmente excluído e não é transmitido aos provedores de SMS downstream.
* Quando disponível, o consentimento no nível da assinatura é avaliado. A recusa global é usada como um fallback quando o consentimento no nível da assinatura não está disponível.
* As pessoas que optaram por não participar do SMS ainda poderão receber mensagens marcadas como operacionais.
* Se vários registros de lead compartilharem o mesmo número de telefone, eles compartilharão o mesmo status de aceitação ou recusa.

## WhatsApp {#whatsapp}

O Journey Optimizer B2B Edition avalia os seguintes atributos XDM para consentimento do WhatsApp ao enviar mensagens por meio de um [canal do WhatsApp](../admin/configure-channels-whatsapp.md) configurado:

| Atributo XDM | `y` | `n` | Nenhum valor |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | Optado | Recusado | Recusado |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | Optado | Recusado | Recusado |

Considere o seguinte para consentimento do WhatsApp:

* Se o valor de atributo global do WhatsApp (`consents.marketing.whatsApp.val`) estiver presente, ele será usado para avaliação de consentimento.
* Se o valor do atributo global não estiver presente, mas uma entrada específica do remetente estiver presente, a entrada específica do remetente será usada para avaliação de consentimento.
* Se nenhum valor estiver presente para nenhum dos atributos, a pessoa será tratada como recusa.

## Incompatível {#not-supported}

Atualmente, os seguintes recursos relacionados ao consentimento não são compatíveis com o Journey Optimizer B2B Edition:

* Políticas de consentimento da AEP
* Atributos de Preferência de Marketing (`consents.marketing.preferred`)
