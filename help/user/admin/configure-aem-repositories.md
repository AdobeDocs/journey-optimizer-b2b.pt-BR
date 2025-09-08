---
title: Configurar repositórios de ativos da Experience Manager
description: Conecte repositórios do Experience Manager Assets ao Journey Optimizer B2B edition para obter acesso fácil a ativos digitais na criação de conteúdo.
feature: Assets, Integrations
role: Admin
exl-id: 4cdfc8bc-823f-4320-a2c3-08226f26eec2
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---

# Configurar repositórios de ativos da Experience Manager

O [!DNL Adobe Journey Optimizer B2B Edition] integra-se ao [!DNL Adobe Experience Manager Assets as a Cloud Service], permitindo o uso de ativos no seu conteúdo de email. Ela garante a transparência ao trocar informações com [!DNL Experience Manager Assets]. Configure a conexão com [!DNL Adobe Experience Assets] para habilitar esse recurso.

O Adobe Experience Manager Cloud Manager está organizado em programas, e cada programa tem vários ambientes e repositórios ([Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types){target="_blank"}). Ao configurar o Adobe Experience Manager Assets no Adobe Journey Optimizer B2B edition, você configura conexões para cada repositório que deseja usar para acessar ativos digitais.

{{aem-assets-licensing-note}}

## Pré-requisitos

* Gere credenciais de serviço para o ambiente desejado no AEM Headless Developer Console ([Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials){target="_blank"}).
* Adquira os certificados necessários para a conexão. Como prática recomendada, verifique se os certificados têm pelo menos seis meses restantes antes da expiração. Os certificados expiram a cada 365 dias.
* O Adobe Journey Optimizer B2B edition oferece suporte ao acesso a uma fonte de gerenciamento de ativos digitais por vez. Verifique se os ativos necessários estão disponíveis no Adobe Experience Manager antes de alternar.

>[!IMPORTANT]
>
>As credenciais de serviço são de boa-fé e contêm uma chave privada. Essas credenciais devem ser armazenadas, gerenciadas e acessadas de acordo com a política de TI e segurança da sua organização.

## Adicionar uma conexão de repositório

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Assets]** no painel intermediário.

   ![Acessar o espaço de configuração do Assets](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
Aqui, é possível configurar as conexões com cada repositório de ambiente do AEM, uma por uma.

1. Na caixa _[!UICONTROL Adobe Experience Manager Assets]_, clique na seta ao lado de **[!UICONTROL Configurar um repositório]** e escolha o repositório.

   ![Escolha um repositório do AEM Assets](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. Clique em **[!UICONTROL Adicionar um certificado]** e use as ferramentas de caixa de diálogo para carregar o arquivo.

   É possível carregar um arquivo .json arrastando-o para a caixa de diálogo. Você também pode clicar no link para localizar e selecionar um arquivo do seu sistema.

   ![Carregar o arquivo JSON de certificado](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   Após o upload, o certificado é exibido na parte inferior.

   >[!NOTE]
   >
   >Se um arquivo inválido for usado, a caixa de diálogo exibirá um erro na parte inferior.

   Clique em **[!UICONTROL Adicionar]** para concluir o certificado.

1. Clique na seta para trás ( Esquerda) para retornar à página de configuração principal.

   O repositório configurado é exibido na tabela sob o painel de seleção. Você pode adicionar outro repositório repetindo as etapas de 3 a 4.

   ![Revisar os repositórios de ativos configurados do AEM](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

Quando você terminar de configurar os repositórios, os membros da equipe poderão selecionar o [!DNL Adobe Experience Manager Assets] ao criar o conteúdo.

>[!NOTE]
>
>O Adobe Journey Optimizer B2B edition oferece suporte ao acesso a uma fonte de gerenciamento de ativos digitais por vez durante a criação de conteúdo. 

## Substituir um certificado

Os certificados expiram a cada 365 dias a partir da data de criação. Para garantir que sua equipe continue acessando os ativos, substitua o certificado antes que ele expire.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer B2B Edition] se comunica com [!DNL Experience Manager Assets] para obter informações de uso. A conexão deve permanecer ativa para a sincronização de dados de uso confiável e para evitar discrepâncias de dados. Os administradores recebem notificações sobre certificados que estão expirando por meio das notificações no aplicativo. As datas de expiração também são exibidas na subseção _Assets_ da área _[!UICONTROL Administração]_.

1. Na página Gerenciamento de ativos digitais, localize a lista dos repositórios configurados.

1. Clique no repositório desejado para substituir o certificado.

1. Clique no ícone de reticências (**...**) do arquivo de certificado para revelar as opções de ações nele.

   ![Acesse o menu de opções para o certificado do repositório de ativos da AEM](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. Escolha **[!UICONTROL Substituir]** para abrir a caixa de diálogo para carregar arquivos.

1. Carregue um arquivo arrastando-o para a caixa de diálogo ou usando o link. Verifique se o arquivo é do tipo JSON.

   ![Carregar o arquivo JSON de certificado do repositório de ativos da AEM de substituição](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. Clique em **[!UICONTROL Substituir]** para confirmar o carregamento.

## Exibir um certificado

Você pode exibir o arquivo JSON de certificado associado à conexão do repositório.

1. Na página Gerenciamento de ativos digitais, localize a lista dos repositórios configurados.

1. Clique no repositório conectado.

1. Clique no ícone de reticências (**...**) do arquivo de certificado para revelar as opções de ações nele.

1. Escolha **[!UICONTROL Exibir]**.

   ![Exibir o arquivo JSON de certificado para um repositório de ativos conectado do AEM](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. Clique em **[!UICONTROL Fechar]** para retornar à página Configurar repositório.

## Excluir uma conexão do repositório

A exclusão de um repositório remove o acesso do usuário ao ambiente do Experience Manager Assets no Journey Optimizer B2B edition.

1. Na página _[!UICONTROL Gerenciamento de ativos digitais]_, localize a lista dos repositórios de ativos configurados.

1. Clique no nome do repositório desejado para editar a conexão.

1. Clique no ícone de reticências (**...**) do arquivo de certificado para revelar as opções de ações nele.

1. Escolha **[!UICONTROL Excluir]**.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
