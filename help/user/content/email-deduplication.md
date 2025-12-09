---
title: Desduplicação de emails
description: Saiba como usar a desduplicação de email em jornadas de conta para evitar que o mesmo email seja enviado várias vezes para o mesmo endereço de email.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: email, desduplicação, jornada, duplicado
source-git-commit: 89dcfae6293fc2bd1eefb58943bee354c57bc73a
workflow-type: tm+mt
source-wordcount: '340'
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
