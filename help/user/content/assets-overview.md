---
title: Ativos
description: Saiba mais sobre o gerenciamento de ativos no Journey Optimizer B2B Edition.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: ht
source-wordcount: '981'
ht-degree: 100%

---

# Ativos

No Adobe Journey Optimizer B2B Edition, os ativos normalmente são as imagens usadas ao desenvolver conteúdo de suporte para jornadas de conta. É possível usar essas imagens nos emails, modelos de email e fragmentos por meio de um seletor de ativos ou uma interface simples de arrastar e soltar no editor de conteúdo visual.

O Adobe Journey Optimizer B2B Edition oferece a profissionais de marketing acesso a dois tipos de bibliotecas de ativos: Adobe Marketo Engage Design Studio e Adobe Experience Manager Assets as a Cloud Service. Você pode usar somente o Adobe Marketo Engage Design Studio ou usar ambas as bibliotecas configuradas ao mesmo tempo (com base em sua licença do AEM Assets).

## Gerenciamento de ativos

Se você receber o direito ao Adobe Experience Manager as a Cloud Service, também receberá acesso aos repositórios do Marketo Engage Design Studio e do Adobe Experience Manager Assets as a Cloud Service se sua conta de usuário tiver as permissões necessárias. Esses repositórios são separados e não estão sincronizados. É possível usar imagens de qualquer fonte.

### Ativos do Adobe Marketo Engage

O repositório de ativos do Adobe Marketo Engage Design Studio é fornecido por padrão com cada assinatura do Journey Optimizer B2B Edition. Isso significa que você tem acesso a qualquer ativo de imagem armazenado no Adobe Marketo Engage ([!UICONTROL Design Studio] > [!UICONTROL Imagens e arquivos]). É possível usar esse repositório como a biblioteca de ativos local, garantindo acesso a funções de upload e download de ativos. Você também pode usar esses ativos no conteúdo da jornada.

Algumas medidas de proteção integradas impedem a edição dos ativos do Marketo Engage no Journey Optimizer B2B Edition, assim como operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos enquanto permitem a leitura e reutilização contínuas no Journey Optimizer B2B Edition.

Formatos de arquivo compatíveis: JPG, JPEG, GIF, PNG, EPS, SVG e RGB

### Adobe Experience Manager Assets as a Cloud Service

Reúna fluxos de trabalho de marketing e criação usando o Adobe Experience Manager Assets. Ele é integrado nativamente ao Adobe Journey Optimizer B2B Edition, garantindo fácil acesso ao Assets as a Cloud Service para descobrir e usar ativos digitais. Ele fornece acesso ao repositório de ativos, os quais podem ser usados para preencher mensagens.

O Adobe Journey Optimizer B2B Edition pode se conectar ao Adobe Experience Manager Assets as a Cloud Service para um gerenciamento de ativos centralizado que estende seu sistema de criação e unifica ativos digitais para a entrega de experiências. O Adobe Experience Manager Assets as a Cloud Service oferece uma solução em nuvem fácil de usar para operações eficientes de gerenciamento de ativos digitais e mídia dinâmica. Ele incorpora recursos avançados com perfeição, incluindo inteligência artificial e aprendizado de máquina.

Saiba mais na [documentação do Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Acesse o Adobe Experience Manager Assets diretamente no Journey Optimizer B2B Edition a partir do item **[!UICONTROL Experience Manager Assets]** na navegação à esquerda do design de conteúdo. Também é possível acessar ativos e pastas ao criar conteúdos de email, modelo de email e fragmento visual.

Atualmente, só é possível usar imagens do Adobe Experience Manager Assets no Adobe Journey Optimizer B2B Edition.

## Usar ativos para criação de conteúdo

Use ativos ao criar emails, modelos de email e fragmentos visuais. O editor de conteúdo visual fornece acesso às imagens nos repositórios de ativos conectados. Se você tiver uma assinatura do Experience Manager Assets as a Cloud Service junto com a versão padrão do Adobe Marketo Engage Design Studio, poderá escolher ativos de imagem de qualquer uma destas fontes. Também é possível fazer upload de um ativo de imagem, o que o coloca no espaço de trabalho do Journey Optimizer B2B Edition do repositório conectado do Marketo Engage Design Studio.

Você pode escolher a fonte da imagem ao editar as configurações de um componente de imagem ou diretamente na tela.

* **_Configurações do componente de imagem_**: ao selecionar um componente de imagem no designer visual, é possível exibir e editar as configurações no painel direito. Para adicionar ou alterar o arquivo de imagem exibido no componente, escolha o tipo de origem e selecione um arquivo de imagem.

  ![Editar as configurações do componente de imagem no painel direito](./assets/content-assets-image-settings.png){width="350"}

* **_Componente vazio_**: ao adicionar um componente de imagem no designer visual, ele estará vazio e você poderá escolher com facilidade uma fonte e selecionar um arquivo de imagem.

  ![Escolha uma fonte e selecione um arquivo de imagem para o componente de imagem vazio](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barra de ferramentas do componente de imagem_**: ao selecionar um componente de imagem no designer visual, a barra de ferramentas permite escolher com facilidade uma fonte e selecionar um arquivo de imagem.

  ![Use a barra de ferramentas para escolher uma fonte e selecionar um arquivo de imagem para o componente de imagem](./assets/content-assets-image-toolbar-settings.png){width="500"}

É possível adicionar um ativo de imagem ao criar seu conteúdo, dependendo da origem do ativo de imagem.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Clique em **[!UICONTROL Marketo Engage Assets]** para abrir o seletor de ativos, onde é possível escolher uma imagem de um espaço de trabalho do Marketo Engage ou do Journey Optimizer B2B Edition.

![Selecione um ativo de imagem do espaço de trabalho](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

É possível usar a pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo no componente de imagem.

Para obter informações mais detalhadas sobre o uso de ativos de imagem do Marketo Engage, consulte [Usar ativos em seu conteúdo](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Clique em **[!UICONTROL Experience Manager Assets]** para abrir o seletor de ativos, onde é possível escolher uma imagem do repositório do Experience Manager Assets.

![Selecione um ativo de imagem do repositório do AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

É possível usar a pesquisa e filtros para localizar o ativo de imagem desejado. Selecione o ativo e clique em **[!UICONTROL Selecionar]** para usá-lo no componente de imagem.

Para obter informações mais detalhadas sobre como usar arquivos de imagem do Experience Manager Assets, consulte [Acessar imagens do AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importar mídia]

Clique em **[!UICONTROL Importar mídia]** para selecionar um arquivo de imagem e importá-lo como um ativo que pode ser usado em conteúdo do Journey Optimizer B2B Edition.

![Selecione seu próprio arquivo de imagem para importar como um ativo](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

Depois de arrastar e soltar o arquivo ou selecioná-lo no sistema de arquivos, clique em **[!UICONTROL Importar]**. O ativo importado é armazenado no espaço de trabalho do Journey Optimizer B2B Edition do repositório do Adobe Marketo Engage Design Studio.

>[!ENDTABS]
