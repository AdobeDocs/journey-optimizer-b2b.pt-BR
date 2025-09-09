---
title: Trabalho com o Experience Manager Assets
description: Acesse e use imagens do AEM Assets na criação de conteúdo - arraste e solte, pesquise, filtre e sincronize alterações automaticamente no Journey Optimizer B2B edition.
feature: Assets, Content, Integrations
role: User
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 2%

---

# Trabalhar com ativos da Experience Manager

Quando o [!DNL Adobe Experience Manager Assets as a Cloud Service] é integrado ao [!DNL Adobe Journey Optimizer B2B Edition], você pode descobrir e acessar facilmente ativos digitais para uso em seu conteúdo de marketing. À medida que você cria seu conteúdo, os ativos podem ser acessados a partir do item _[!UICONTROL Experience Manager Assets]_ na navegação à esquerda e ao criar conteúdo de email para uma jornada de conta.

{{aem-assets-licensing-note}}

Quando você usa esses ativos digitais, as alterações mais recentes no [!DNL Assets as a Cloud Service] se propagam automaticamente para campanhas de email ao vivo por meio de referências vinculadas. Se as imagens forem excluídas em [!DNL Adobe Experience Manager Assets as a Cloud Service], elas aparecerão com uma referência corrompida nos emails. Quando os ativos atualmente usados nas jornadas da conta são modificados ou excluídos, os autores da jornada são notificados sobre as alterações na imagem e a lista de jornadas que usam a imagem. Todas as alterações nos ativos devem ser feitas no repositório central [!DNL Adobe Experience Manager Assets].

Quando o ambiente tem uma ou mais [conexões de repositórios Assets](../admin/configure-aem-repositories.md), os autores de conteúdo podem usar [!DNL Experience Manager Assets] como fonte para ativos ao criar um email, modelo de email ou fragmento visual.

>[!IMPORTANT]
>
>Um administrador deve adicionar usuários que precisam de acesso ao Assets aos perfis do produto Usuários do cliente do Assets e/ou Usuários do Assets. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console){target="_blank"}

## Acessar imagens do AEM Assets

No espaço de design de conteúdo, clique no ícone do _[!UICONTROL Experience Manager Assets]_ ( ![Experience Manager Assets](../../assets/do-not-localize/icon-assets-aem.svg) ) na barra lateral esquerda. Isso altera o painel Ferramentas para uma lista de ativos disponíveis no repositório selecionado.

![Clique no ícone do seletor do Assets para acessar os ativos da imagem](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Atualmente, somente ativos de imagem de [!DNL Adobe Experience Manager Assets] são suportados no [!DNL Adobe Journey Optimizer B2B Edition]. As alterações nos ativos devem ser feitas pelo repositório central [!DNL Adobe Experience Manager Assets]. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets){target="_blank"}

### Alterar o repositório exibido

Se você tiver mais de um repositório do AEM conectado, clique na seta de menu de **[!UICONTROL Repositório]** para escolher o repositório que deseja exibir no painel esquerdo.

![Escolha um repositório do AEM Assets para acessar os ativos da imagem](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Há vários métodos para adicionar um ativo de imagem à tela visual.

### Arraste e solte uma imagem

1. Navegue pelas miniaturas de imagem exibidas no painel esquerdo.

1. Arraste a miniatura da imagem e solte-a na tela de desenho onde deseja adicionar o novo componente de imagem.

   ![Arraste e solte um ativo de imagem](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

## Localizar e selecionar uma imagem

1. Adicione um componente de imagem à tela e clique em **[!UICONTROL Experience Manager Assets]** para abrir a caixa de diálogo _[!UICONTROL Selecionar Assets]_.

   ![Selecione um ativo para o componente de imagem](./assets/content-image-component-empty.png){width="600" zoomable="yes"}

1. Na caixa de diálogo, escolha uma imagem usando as ferramentas disponíveis para localizar o ativo necessário:

   * Altere o **[!UICONTROL Repositório]** na parte superior direita.

   * Clique em **[!UICONTROL Gerenciar ativos]** na parte superior direita para abrir o repositório do Assets em outra guia do navegador e usar as ferramentas de gerenciamento do AEM Assets.

   * Clique no seletor de _Tipo de exibição_ na parte superior direita para alterar a exibição para **[!UICONTROL Exibição de Lista]**, **[!UICONTROL Exibição de Grade]**, **[!UICONTROL Exibição de Galeria]** ou **[!UICONTROL Exibição em Cascata]**.

   * Clique no ícone _Ordem de classificação_ para alterar a ordem de classificação entre crescente e decrescente.

     ![Use as ferramentas na caixa de diálogo Selecionar Assets para localizar e selecionar um ativo de imagem](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Clique na seta de menu **[!UICONTROL Classificar por]** para alterar os critérios de classificação para **[!UICONTROL Nome]**, **[!UICONTROL Tamanho]** ou **[!UICONTROL Modificado]**.

   * Clique no ícone _Filtro_ na parte superior esquerda para filtrar os itens exibidos de acordo com seus critérios.

   * Insira texto no campo Pesquisar para filtrar os itens exibidos para uma correspondência do nome do ativo.

   ![Use os filtros e o campo de pesquisa para localizar o ativo](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar]**.
<!-- 

## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.
-->
