---
title: Trabalho com o Experience Manager Assets
description: Saiba como você pode usar ativos de imagem de um repositório conectado do AEM Assets ao criar conteúdo no Adobe Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 1%

---

# Trabalhar com ativos do Experience Manager

Quando o Adobe Experience Manager Assets as a Cloud Service é integrado ao Adobe Journey Optimizer B2B Edition, você pode descobrir e acessar facilmente ativos digitais para uso em seu conteúdo de marketing. À medida que você cria seu conteúdo, os ativos podem ser acessados a partir do item _[!UICONTROL Assets]_ na navegação à esquerda e ao criar conteúdo de email para uma jornada de conta. Você também pode fazer upload de ativos para o repositório as a Cloud Service do AEM Assets conectado diretamente do Adobe Journey Optimizer B2B Edition.

>[!NOTE]
>
>Atualmente, somente ativos de imagem do Adobe Experience Manager Assets são compatíveis com o Adobe Journey Optimizer B2B Edition. As alterações nos ativos devem ser feitas pelo repositório central da Adobe Experience Manager Assets. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Quando você usa esses ativos digitais, as alterações mais recentes no Assets as a Cloud Service se propagam automaticamente para campanhas de email ao vivo por meio de referências vinculadas. Se as imagens forem excluídas no Adobe Experience Manager Assets as a Cloud Service, elas serão exibidas com uma referência quebrada nos emails. Quando os ativos atualmente usados nas jornadas da conta são modificados ou excluídos, os autores da jornada são notificados sobre as alterações na imagem e a lista de jornadas que usam a imagem. Todas as alterações nos ativos devem ser feitas no repositório central da Adobe Experience Manager Assets.

## Usar o AEM Assets como fonte de imagem

Se o ambiente tiver uma ou mais [conexões de repositórios do Assets](../admin/configure-aem-repositories.md), você poderá designar o AEM Assets como fonte dos ativos ao criar ou exibir detalhes de um email, modelo de email ou fragmento visual.

* Ao criar um novo conteúdo, escolha `AEM Assets` como o item **[!UICONTROL Image Source]** na caixa de diálogo.

  ![Selecione AEM Assets como a fonte da imagem na caixa de diálogo de criação](./assets/create-dialog-aem-assets.png){width="400"}

* Ao abrir um recurso de conteúdo existente, escolha `AEM Assets` no painel _[!UICONTROL Corpo]_ à direita.

  ![Selecione o AEM Assets como fonte de imagem nas propriedades](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Acessar ativos para criação

>[!IMPORTANT]
>
>Um administrador deve adicionar usuários que precisam de acesso ao Assets aos perfis do produto Usuários do cliente do Assets e/ou Usuários do Assets. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

No editor de conteúdo visual, clique no ícone _Seletor de ativos_ na barra lateral esquerda. Isso altera o painel Ferramentas para uma lista de ativos disponíveis no repositório selecionado.

![Clique no ícone do seletor do Assets para acessar os ativos da imagem](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

Se você tiver mais de um repositório AEM conectado, clique na seta de menu de **[!UICONTROL Repositório]** para escolher o repositório que deseja usar.

![Escolha um repositório do AEM Assets para acessar os ativos da imagem](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Há vários métodos para adicionar um ativo de imagem à tela visual:

* Arraste e solte uma miniatura de imagem da navegação à esquerda.

  ![Escolha um repositório do AEM Assets para acessar os ativos da imagem](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* Adicione um componente de imagem à tela e clique em **[!UICONTROL Procurar]** para abrir a caixa de diálogo _[!UICONTROL Selecionar Assets]_.

  Na caixa de diálogo, é possível escolher uma imagem do repositório selecionado.

  Há várias ferramentas disponíveis para ajudá-lo a localizar o ativo que você precisa.

  ![use a ferramenta na caixa de diálogo Selecionar Assets para localizar e selecionar um ativo de imagem](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Altere o **[!UICONTROL Repositório]** na parte superior direita.

   * Clique em **[!UICONTROL Gerenciar ativos]** na parte superior direita para abrir o repositório do Assets em outra guia do navegador e usar as ferramentas de gerenciamento do AEM Assets.

   * Clique no seletor de _Tipo de exibição_ na parte superior direita para alterar a exibição para **[!UICONTROL Exibição de Lista]**, **[!UICONTROL Exibição de Grade]**, **[!UICONTROL Exibição de Galeria]** ou **[!UICONTROL Exibição em Cascata]**.

   * Clique no ícone _Ordem de classificação_ para alterar a ordem de classificação entre crescente e decrescente.

   * Clique na seta de menu **[!UICONTROL Classificar por]** para alterar os critérios de classificação para **[!UICONTROL Nome]**, **[!UICONTROL Tamanho]** ou **[!UICONTROL Modificado]**.

   * Clique no ícone _Filtro_ na parte superior esquerda para filtrar os itens exibidos de acordo com seus critérios.

   * Insira texto no campo Pesquisar para filtrar os itens exibidos para uma correspondência do nome do ativo.

  ![Use os filtros e o campo de pesquisa para localizar o ativo](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

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
