---
title: Ativos
description: Saiba mais sobre o gerenciamento de ativos no Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Ativos

No Adobe Journey Optimizer B2B edition, os ativos normalmente são as imagens usadas na criação do conteúdo da jornada. Você pode usar essas imagens nos emails, modelos de email e fragmentos criados no Journey Optimizer B2B edition por meio de um seletor de ativos ou uma interface simples de arrastar e soltar no editor de conteúdo visual.

O Adobe Journey Optimizer B2B edition oferece aos profissionais de marketing acesso a dois tipos de bibliotecas de ativos: Adobe Marketo Engage Design Studio e Adobe Experience Manager Assets as a Cloud Service. Você pode usar somente o Adobe Marketo Engage Design Studio ou usar ambas as bibliotecas configuradas ao mesmo tempo (com base na licença do AEM Assets que você tem).

## Gerenciamento de ativos

Se você tiver uma conta de Marketo Engage e o Adobe Experience Manager como um Cloud Service, terá acesso aos repositórios do DAM Marketo Engage e do Adobe Experience Manager Assets as a Cloud Service quando a conta de usuário tiver as permissões necessárias. Esses repositórios estão separados e não estão sincronizados. Você pode usar imagens de qualquer origem, mas somente uma pode ser ativada no editor de conteúdo por vez. Um administrador pode tornar as a Cloud Service o switch do DAM do Marketo Engage para o Adobe Experience Manager Assets. O item _[!UICONTROL Assets]_ na navegação à esquerda exibe o repositório definido no momento.

### Ativos do Adobe Marketo Engage

O repositório de ativos do Adobe Marketo Engage Design Studio é fornecido por padrão com cada assinatura do Journey Optimizer B2B edition. Isso significa que você tem acesso a qualquer um dos ativos de imagem armazenados no Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL Imagens e Arquivos]. Você pode usar esse repositório como a biblioteca de ativos local, incluindo funções de upload e download de ativos. Você também pode usar esses ativos no conteúdo da jornada.

Existem medidas de proteção integradas que impedem a edição de ativos Marketo Engage do Journey Optimizer B2B edition e as operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos e, ao mesmo tempo, permitem leitura e reutilização perfeitas no Journey Optimizer B2B edition.

Formatos de arquivos suportados: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Reúna marketing e workflows criativos usando o Adobe Experience Manager Assets. Ele é integrado nativamente ao Adobe Journey Optimizer B2B edition, para que você possa acessar facilmente o Assets as a Cloud Service para descobrir e usar ativos digitais. Ele fornece acesso ao repositório do Assets para ativos que você pode usar para preencher suas mensagens.

O Adobe Experience Manager Assets pode se conectar ao Adobe Experience Manager Assets as a Cloud Service para espaços de trabalho de ativos centralizados que estendem o sistema criativo e unificam ativos digitais para oferecer experiência. O Adobe Experience Manager Assets as a Cloud Service oferece uma solução em nuvem fácil de usar para o gerenciamento eficiente de ativos digitais e operações do Dynamic Media. Ele incorpora, de maneira contínua, recursos avançados, incluindo Inteligência artificial e Aprendizado de máquina.

Saiba mais na [documentação do Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview).

O Adobe Experience Manager Assets pode ser acessado diretamente no Adobe Journey Optimizer B2B edition a partir do item **[!UICONTROL Assets]** na navegação à esquerda. Você também pode acessar ativos e pastas ao criar um conteúdo de email.

>[!NOTE]
>
>As licenças AEM Assets as Cloud Service e Dynamic Media são pré-requisitos para essa integração.<br/>
>Dependendo do contrato e da configuração, o Adobe Experience Manager Assets as a Cloud Service pode ser acessado diretamente do Adobe Journey Optimizer B2B edition por meio da seção Assets do menu esquerdo. Você também pode acessar ativos e pastas ao criar um conteúdo de email.

Atualmente, você só pode usar imagens do Adobe Experience Manager Assets no Adobe Journey Optimizer B2B edition.

## Usar ativos para criação de conteúdo

Use ativos ao criar emails, modelos de email e fragmentos visuais. A interface do editor de conteúdo visual fornece acesso às imagens nos repositórios de ativos conectados.

### Escolha uma origem de ativo

Se você tiver uma assinatura do Experience Manager Assets as a Cloud Service junto com o Adobe Marketo Engage Design Studio padrão, poderá escolher ativos de imagem de qualquer uma das origens. Para fazer isso, você deve selecionar a fonte de imagem no momento da criação para um novo email, modelo de email ou fragmento visual. Ou selecione a fonte de imagem ao editar o conteúdo. A seleção se aplica somente à experiência de edição e você pode alterar a fonte de imagem para acessar ativos de outra biblioteca quando necessário.

_**Criando um recurso de conteúdo**_ - Para escolher uma fonte de imagem ao criar um email, modelo de email ou fragmento, defina a **[!UICONTROL fonte de imagem]** na caixa de diálogo.

_**Editando um recurso de conteúdo**_ - Para escolher uma origem de ativo de imagem na visualização visual, use a configuração **[!UICONTROL Origem da imagem]** no painel à direita.

### Adicionar ativos ao seu conteúdo

É possível adicionar um ativo de imagem ao criar seu conteúdo, dependendo da fonte de ativo de imagem selecionada.

>[!BEGINTABS]

>[!TAB Adicionar ativos de imagem de Marketo Engage]

Você pode adicionar ativos de Marketo Engage usando um dos seguintes métodos:

* Adicione um elemento estrutural e arraste e solte os ativos da navegação à esquerda na tela visual.
* Adicione um elemento estrutural e arraste e solte o tipo de conteúdo _image_ na estrutura. Nas configurações de propriedades à direita, há duas maneiras de especificar a imagem:
   * Clique em **[!UICONTROL Procurar]** para abrir o seletor de ativos, no qual você pode escolher uma imagem da biblioteca de ativos do Adobe Marketo Engage Design Studio.
   * Clique em **[!UICONTROL Importar mídia]** para importar um ativo do sistema local. O ativo importado é armazenado na pasta raiz do Assets da biblioteca do Adobe Marketo Engage Design Studio.

Consulte [Usar ativos no seu conteúdo](./marketo-engage-design-studio.md#use-assets-in-your-content) para obter mais informações.

Para alterar a imagem, você pode atualizar o URL de origem da imagem nas propriedades à direita.

>[!TAB Adicionar imagens do Experience Manager Assets]

1. Ao criar seu conteúdo de email no designer de email, arraste um elemento de imagem para a tela.

   As propriedades à direita refletem a seleção do elemento de imagem.

1. Clique em **[!UICONTROL Selecionar um ativo]** para abrir o seletor de Ativos Experience Manager.

   Aqui você pode pesquisar, filtrar e acessar seu ativo de conteúdo desejado para adicionar ao seu ativo de marketing. Consulte esta página para obter mais detalhes sobre como usar o seletor.

   >[!NOTE]
   >
   >Se mais de um repositório estiver configurado, você poderá usar o alternador de repositório no seletor de Ativos

1. Selecione o ativo desejado a ser inserido no email.

>[!ENDTABS]
