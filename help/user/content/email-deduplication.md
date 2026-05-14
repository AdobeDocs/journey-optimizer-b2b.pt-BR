---
title: Desduplicação de emails
description: Saiba como usar a desduplicação de email em jornadas de conta para evitar que o mesmo email seja enviado várias vezes para o mesmo endereço de email.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: email, desduplicação, jornada, duplicado
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: 2026-03-30T22:08:16.582Z
TQID: https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 343
ht-degree: 1%

---

# Desduplicação de email

Use a desduplicação de email em jornadas de conta para garantir que o mesmo email não seja enviado várias vezes para o mesmo endereço de email em uma jornada. Quando você habilita esse recurso, endereços de email duplicados são bloqueados até que o primeiro registro com esse endereço de email conclua a jornada. Depois que uma conta terminar uma jornada, uma pessoa pode se qualificar para receber emails novamente como parte de uma nova conta que entra na jornada.

## Quando usar a desduplicação de email

Há alguns cenários principais em que você deve considerar a ativação da desduplicação de email:

* **O email não é usado como identidade no Real-Time CDP** - O mesmo endereço de email pode aparecer em vários perfis de pessoa. Se esses perfis duplicados se qualificarem para a mesma jornada e você quiser impedir o envio de email mais de uma vez, ative esse recurso.

* **Pessoa única associada a várias contas** - Se o modelo de dados do Real-Time CDP permitir que uma única pessoa seja associada a várias contas e você quiser evitar enviar o mesmo email duas vezes para essa pessoa quando várias contas (incluindo perfis com o mesmo endereço de email) se qualificarem para a mesma jornada, habilite esse recurso.

>[!NOTE]
>
>A desduplicação de email se aplica no nível da jornada. Se uma pessoa com o mesmo endereço de email se qualificar para jornadas diferentes, ainda poderá receber emails de cada jornada.

## Ativar a desduplicação de email para uma jornada

Para ativar a desduplicação de email para uma jornada de conta:

1. Abra uma jornada de conta.

1. Clique em **[!UICONTROL Mais]** (**...**) no canto superior direito do espaço de trabalho do jornada.

   ![Jornada o espaço de trabalho com o menu Mais expandido mostrando a opção de Eliminação de Duplicação de Email](./assets/email-deduplication-more-menu.png){width="450"}

1. Escolha a **[!UICONTROL Eliminação de Duplicação de Emails]**.

1. Na caixa de diálogo, marque a caixa de seleção **[!UICONTROL Desduplicação de email]**.

   ![Caixa de diálogo de Eliminação de Duplicação de Email com alternância habilitada](./assets/email-deduplication-dialog.png){width="400"}

1. Clique em **[!UICONTROL Salvar]**.

Quando a desduplicação de email está habilitada, o jornada verifica cada endereço de email antes de enviar o email. Se um registro com o mesmo endereço de email já tiver sido inserido nesse nó de jornada, a nova entrada será bloqueada até que o primeiro registro conclua a jornada.
