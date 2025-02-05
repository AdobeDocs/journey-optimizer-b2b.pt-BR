---
title: Exportar lista de contas
description: Saiba como exportar a lista de contas com base no filtro de grupos de compra.
source-git-commit: c51ee8c8b58e8154c81f6a2ffada3f58a08eb6b4
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Exportar lista de contas

Use o recurso _Exportar lista de contas_ para exportar todas as contas ou um conjunto de contas com base na filtragem definida. O processo de exportação produz um arquivo CSV e envia o URL do arquivo armazenado em uma notificação de pulso. Você pode usar esse recurso para mover contas para plataformas de terceiros quando necessário.

1. No Journey Optimizer B2B edition, acesse **[!UICONTROL Contas]** > **[!UICONTROL Grupos de compras]** na navegação à esquerda.

1. Selecione a guia **[!UICONTROL Procurar]**.

1. Clique em **[!UICONTROL Exportar contas]** na parte superior direita.

   ![Editar detalhes da conta](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Na caixa de diálogo, defina os parâmetros dos públicos-alvo da conta que serão exportados.

   ![Especificar a filtragem de público da conta](./assets/export-accounts-dialog.png){width="400"}

   Para a **[!UICONTROL Pontuação de engajamento]**, o operador `Between` é inclusivo, assim como os intervalos de porcentagem. Por exemplo, 5.1 e 5 estão ambos _entre_ 5 e 6.

   Parâmetros de filtragem vazios são tratados como `Is Any`.

1. Clique em **[!UICONTROL Exportar contas]** para gerar o arquivo CSV usando os filtros especificados.

1. Quando você receber a notificação de que a exportação foi concluída, clique no link de notificação para acessar o arquivo CSV.

   ![Clique na notificação para baixar o arquivo CSV da lista de contas exportadas](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Se você tiver uma assinatura de notificação para notificação por email configurada nas preferências de sua conta de usuário do Adobe, ela poderá ser uma notificação por email.

   A página do aplicativo redireciona para a guia de navegação _Grupo de Compra_, e a caixa de diálogo Salvar Arquivo do Sistema solicita que você salve o arquivo no sistema. Se precisar compartilhar os dados, você pode usar o sistema de compartilhamento de arquivos de sua equipe.
