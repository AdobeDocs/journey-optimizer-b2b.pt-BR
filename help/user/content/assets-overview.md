---
title: Ativos
description: Saiba mais sobre o gerenciamento de ativos no Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 728d5316cfdeee92bd4f67277d299bbec2773a4f
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# Ativos

No Adobe Journey Optimizer B2B edition, os ativos normalmente são as imagens usadas ao projetar conteúdo para oferecer suporte às jornadas da conta. Você pode usar essas imagens nos emails, modelos de email e fragmentos por meio de um seletor de ativos ou uma interface simples de arrastar e soltar no editor de conteúdo visual.

O Adobe Journey Optimizer B2B edition oferece aos profissionais de marketing acesso a dois tipos de bibliotecas de ativos: Adobe Marketo Engage Design Studio e Adobe Experience Manager Assets as a Cloud Service. Você pode usar somente o Adobe Marketo Engage Design Studio ou usar ambas as bibliotecas configuradas ao mesmo tempo (com base na licença do AEM Assets que você tem).

## Gerenciamento de ativos

Se você tiver provisionado com o Adobe Experience Manager as a Cloud Service, terá acesso aos repositórios do Marketo Engage Design Studio e do Adobe Experience Manager Assets as a Cloud Service quando sua conta de usuário tiver as permissões necessárias. Esses repositórios estão separados e não estão sincronizados. Você pode usar imagens de qualquer origem.

### Ativos do Adobe Marketo Engage

O repositório de ativos do Adobe Marketo Engage Design Studio é fornecido por padrão com cada assinatura do Journey Optimizer B2B edition. Isso significa que você tem acesso a qualquer ativo de imagem armazenado no Adobe Marketo Engage ([!UICONTROL Design Studio] > [!UICONTROL Imagens e Arquivos]). Você pode usar esse repositório como a biblioteca de ativos local, incluindo funções de upload e download de ativos. Você também pode usar esses ativos no conteúdo da jornada.

Existem medidas de proteção integradas que impedem a edição de ativos Marketo Engage do Journey Optimizer B2B edition e as operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos e, ao mesmo tempo, permitem leitura e reutilização perfeitas no Journey Optimizer B2B edition.

Formatos de arquivos suportados: JPG, JPEG, GIF, PNG, EPS, SVG e RGB

### Adobe Experience Manager Assets as a Cloud Service

Reúna marketing e workflows criativos usando o Adobe Experience Manager Assets. Ele é integrado nativamente ao Adobe Journey Optimizer B2B edition, para que você possa acessar facilmente o Assets as a Cloud Service para descobrir e usar ativos digitais. Ele fornece acesso ao repositório do Assets para ativos que você pode usar para preencher suas mensagens.

O Adobe Journey Optimizer B2B edition pode se conectar ao Adobe Experience Manager Assets as a Cloud Service para um gerenciamento centralizado de ativos que estende seu sistema criativo e unifica ativos digitais para oferecer uma experiência. O Adobe Experience Manager Assets as a Cloud Service oferece uma solução em nuvem fácil de usar para o gerenciamento eficiente de ativos digitais e operações do Dynamic Media. Ele incorpora, de maneira contínua, recursos avançados, incluindo Inteligência artificial e Aprendizado de máquina.

Saiba mais na [documentação do Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview).

{{aem-assets-licensing-note}}

Acesse o Adobe Experience Manager Assets diretamente no Journey Optimizer B2B edition a partir do item **[!UICONTROL Experience Manager Assets]** na navegação à esquerda do design de conteúdo. Você também pode acessar ativos e pastas ao criar conteúdo de email, modelo de email e fragmento visual.

Atualmente, você pode usar somente imagens do Adobe Experience Manager Assets no Adobe Journey Optimizer B2B edition.

## Usar ativos para criação de conteúdo

Use ativos ao criar emails, modelos de email e fragmentos visuais. O editor de conteúdo visual fornece acesso às imagens nos repositórios de ativos conectados. Se você tiver uma assinatura do Experience Manager Assets as a Cloud Service junto com o Adobe Marketo Engage Design Studio padrão, poderá escolher ativos de imagem de qualquer uma das origens. Também é possível carregar um ativo de imagem, que o coloca no espaço de trabalho do Journey Optimizer B2B edition do repositório conectado do Marketo Engage Design Studio.

Você pode escolher a fonte da imagem ao editar as configurações de um componente de imagem ou diretamente na tela.

* **_Configurações do componente de imagem_** - Quando um componente de imagem está selecionado no designer visual, você pode exibir e editar as configurações no painel direito. Para adicionar ou alterar o arquivo de imagem exibido no componente, escolha o tipo de origem e selecione um arquivo de imagem.

  ![Editar as configurações do componente de imagem no painel direito](./assets/content-assets-image-settings.png){width="350"}

* **_Componente vazio_** - Quando você adiciona um componente de imagem no designer visual, ele fica vazio e fornece acesso fácil para escolher uma fonte e selecionar um arquivo de imagem.

  ![Escolha uma origem para selecionar um arquivo de imagem para o componente de imagem vazio](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barra de ferramentas do componente de imagem_** - Quando um componente de imagem está selecionado no designer visual, a barra de ferramentas fornece acesso fácil para escolher uma origem e selecionar o arquivo de imagem.

  ![Use a barra de ferramentas para escolher uma fonte para selecionar um arquivo de imagem para o componente de imagem](./assets/content-assets-image-toolbar-settings.png){width="500"}

É possível adicionar um ativo de imagem ao criar seu conteúdo, dependendo da fonte do ativo de imagem.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Clique em **[!UICONTROL Marketo Engage Assets]** para abrir o seletor de ativos, onde é possível escolher uma imagem de um espaço de trabalho Marketo Engage ou do Journey Optimizer B2B edition.

![Selecione um ativo de imagem do espaço de trabalho](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

Você pode usar pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo para o componente de imagem.

Para obter informações mais detalhadas sobre o uso de ativos de imagem de Marketo Engage, consulte [Usar ativos no seu conteúdo](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Clique em **[!UICONTROL Experience Manager Assets]** para abrir o seletor de ativos, onde é possível escolher uma imagem do repositório do Experience Manager Assets.

![Selecione um ativo de imagem do repositório do AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Você pode usar pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo para o componente de imagem.

Para obter informações mais detalhadas sobre como usar arquivos de imagem do Experience Manager Assets, consulte [Acessar imagens do AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importar mídia]

Clique em **[!UICONTROL Importar mídia]** para selecionar um arquivo de imagem e importá-lo como um ativo que pode ser usado para conteúdo do Journey Optimizer B2B edition.

![Selecione seu próprio arquivo de imagem para importar como um ativo](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

Depois de arrastar e soltar o arquivo ou selecioná-lo no sistema de arquivos, clique em **[!UICONTROL Importar]**. O ativo importado é armazenado no espaço de trabalho do Journey Optimizer B2B edition do repositório do Adobe Marketo Engage Design Studio.

>[!ENDTABS]
