---
title: Ativos
description: Gerencie ativos de imagem do Journey Optimizer B2B edition e do AEM Assets para emails, modelos e fragmentos.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 60%

---

# Ativos

No [!DNL Adobe Journey Optimizer B2B Edition], os ativos normalmente são as imagens usadas ao criar conteúdo de suporte para jornadas de conta. Você pode usar essas imagens em seus emails, modelos de email e fragmentos do seletor de ativos ou em uma interface simples de arrastar e soltar no espaço de design visual.

O [!DNL Journey Optimizer B2B Edition] oferece aos designers e comerciantes acesso a dois tipos de bibliotecas de ativos: um repositório interno de ativos [!DNL Journey Optimizer B2B Edition] e [!DNL Adobe Experience Manager Assets as a Cloud Service]. Você pode usar somente o repositório interno ou ambos os tipos de biblioteca ao mesmo tempo (com base na licença [!DNL Experience Manager Assets] que você tem).

## Gerenciamento de ativos

Se você estiver provisionado com [!DNL Adobe Experience Manager as a Cloud Services] e ele estiver configurado como uma origem de ativo em [!DNL Journey Optimizer B2B Edition], você terá acesso aos dois tipos de repositório quando sua conta de usuário tiver as permissões necessárias. Esses repositórios são separados e não estão sincronizados. É possível usar imagens de qualquer fonte.

### Ativos internos

O repositório interno de ativos é fornecido por padrão com cada assinatura do [!DNL Journey Optimizer B2B Edition]. Isso significa que você tem acesso a qualquer um dos ativos de imagem armazenados no sistema de arquivos de ativos [!DNL Adobe Marketo Engage] conectado. É possível usar esse repositório como a biblioteca de ativos local, garantindo acesso a funções de upload e download de ativos. Você também pode usar esses ativos no conteúdo da jornada.

Você pode [editar esses ativos usando o Adobe Express](./image-edit-adobe-express.md) e movê-los para pastas para organizá-los para uso em seus emails, modelos e fragmentos.

Formatos de arquivo compatíveis: JPG, JPEG, GIF, PNG, EPS, SVG e RGB

### Adobe Experience Manager Assets as a Cloud Service

Junte os fluxos de trabalho de marketing e de criação usando o [!DNL Adobe Experience Manager Assets]. Ele é integrado nativamente ao [!DNL Journey Optimizer B2B Edition], garantindo fácil acesso ao Assets as a Cloud Service para descobrir e usar ativos digitais. Ele fornece acesso ao repositório de ativos, os quais podem ser usados para preencher mensagens.

O [!DNL Adobe Journey Optimizer B2B Edition] pode se conectar ao [!DNL Adobe Experience Manager Assets as a Cloud Service] para um gerenciamento centralizado de ativos que estende seu sistema de criação e unifica ativos digitais para a entrega de experiências. O [!DNL Adobe Experience Manager Assets as a Cloud Service] oferece uma solução em nuvem fácil de usar para operações eficientes de gerenciamento de ativos digitais e mídia dinâmica. Ele incorpora recursos avançados com perfeição, incluindo inteligência artificial e aprendizado de máquina.

Saiba mais na [documentação do Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Acesse o [!DNL Adobe Experience Manager Assets] diretamente no [!DNL Journey Optimizer B2B Edition] a partir do item **[!UICONTROL Experience Manager Assets]** no painel de navegação à esquerda do design de conteúdo. Também é possível acessar ativos e pastas ao criar conteúdos de email, modelo de email e fragmento visual.

Atualmente, só é possível usar imagens do Adobe Experience Manager Assets no Adobe Journey Optimizer B2B Edition.

## Usar ativos para criação de conteúdo

Use ativos ao criar emails, modelos de email e fragmentos visuais. O editor de conteúdo visual fornece acesso às imagens nos repositórios de ativos conectados. Se você também tiver uma assinatura do Experience Manager Assets as a Cloud Service, poderá escolher ativos de imagem de qualquer origem. Também é possível fazer upload de um ativo de imagem, que o coloca no repositório de ativos interno.

Você pode escolher a fonte da imagem ao editar as configurações de um componente de imagem ou diretamente na tela:

* **_Configurações do componente de imagem_** - Quando um componente de imagem está selecionado na tela, você pode exibi-las e editá-las no painel direito. Para adicionar ou alterar o arquivo de imagem exibido no componente, escolha o tipo de origem e selecione um arquivo de imagem.

  ![Editar as configurações do componente de imagem no painel direito](./assets/content-assets-image-settings.png){width="350"}

* **_Componente vazio_** - Quando você adiciona um componente de imagem à tela, ele fica vazio e fornece acesso fácil para escolher uma fonte e selecionar um arquivo de imagem.

  ![Escolha uma fonte e selecione um arquivo de imagem para o componente de imagem vazio](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barra de ferramentas do componente de Imagem_** - Quando você tem um componente de Imagem selecionado na tela, a barra de ferramentas fornece acesso fácil para escolher uma fonte e selecionar o arquivo de imagem.

  ![Use a barra de ferramentas para escolher uma fonte e selecionar um arquivo de imagem para o componente de imagem](./assets/content-assets-image-toolbar-settings.png){width="500"}

É possível adicionar um ativo de imagem ao criar o conteúdo, dependendo da origem do ativo de imagem. Você também pode escolher um ativo de imagem nas configurações de plano de fundo de um componente de estrutura.

>[!BEGINTABS]

>[!TAB Selecionar ativo]

Clique em **[!UICONTROL Selecionar ativo]** para abrir o seletor de ativos, onde é possível escolher uma imagem do repositório de ativos do Journey Optimizer B2B edition.

![Selecione um ativo de imagem](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

É possível usar a pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo no componente de imagem.

Para obter informações mais detalhadas sobre o uso de ativos de imagem internos, consulte [Usar ativos no seu conteúdo](./internal-image-assets.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Clique em **[!UICONTROL Experience Manager Assets]** para abrir o seletor de ativos, onde é possível escolher uma imagem do repositório do Experience Manager Assets.

![Selecione um ativo de imagem do repositório do AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

É possível usar a pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo no componente de imagem.

Para obter informações mais detalhadas sobre como usar arquivos de imagem do [!DNL Experience Manager Assets], consulte [Acessar imagens do AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importar mídia]

Clique em **[!UICONTROL Importar mídia]** para selecionar um arquivo de imagem e importá-lo como um ativo que pode ser usado em conteúdo do Journey Optimizer B2B Edition.

![Selecione seu próprio arquivo de imagem para importar como um ativo](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

Depois de arrastar e soltar o arquivo ou selecioná-lo no sistema de arquivos, clique em **[!UICONTROL Importar]**. O ativo importado é armazenado no repositório de ativos [!DNL Journey Optimizer B2B Edition].

>[!ENDTABS]
