---
title: Experiências na Web
description: Crie, projete e publique experiências personalizadas da Web para jornadas de conta - forneça modificações de conteúdo direcionadas aos visitantes do site no Journey Optimizer B2B edition.
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: e3c00ab4657c7bf05573e049bbcb4bb3628e751e
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 1%

---

# Experiências da Web

O canal da Web no Adobe Journey Optimizer B2B edition permite criar experiências personalizadas diretamente no seu site, ajudando você a se conectar com os clientes de maneiras significativas. Esse recurso oferece um kit de ferramentas flexível que você pode usar para aprimorar o engajamento com conteúdo personalizado e integrá-lo perfeitamente a outros canais, como email e SMS.

As experiências na Web permitem:

* Fornecer modificações personalizadas de conteúdo aos visitantes do site direcionado
* Personalize elementos do site, como banners, texto, imagens e botões, com base nos atributos da conta
* Direcione páginas específicas ou aplique alterações em várias páginas usando regras de correspondência de URL
* Acompanhe o engajamento e monitore o impacto de seus esforços de personalização da Web

>[!BEGINSHADEBOX]

## Pré-requisitos

Antes de criar experiências na Web, verifique se os seguintes requisitos foram atendidos:

* Um administrador de produto configurou um ou mais canais da Web para definir os URLs (páginas) a serem incluídos em uma experiência da Web. Para obter mais informações, consulte [Configurações do canal da Web](../admin/configure-channels-web.md).

* Seu site tem o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/pt-br/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementado para identificação de visitantes e entrega de conteúdo. Verifique se a versão do Adobe Experience Platform Web SDK é a 2.16 ou superior.

* Você tem as [permissões](../admin/user-management.md#b2b-product-permissions) necessárias para criar e gerenciar experiências da Web em uma jornada:
   * _[!UICONTROL Campanhas]_ > _[!UICONTROL Gerenciar campanhas]_ - Necessário para adicionar ou atualizar um nó de ação de personalização da Web.
   * _[!UICONTROL Campanhas]_ > _[!UICONTROL Exibir campanhas]_ - Necessário para exibir detalhes de nós de ação de personalização da Web.
   * _[!UICONTROL Campanhas]_ > _[!UICONTROL Aprovar e publicar campanhas]_ - é necessário publicar uma jornada que tenha um ou mais nós de ação de personalização da Web.

* Você tem a [extensão de navegador Auxiliar de edição visual](#install-the-visual-editing-helper-extension) do Adobe Experience Cloud instalada para o seu navegador da Web. Essa extensão é necessária para abrir, criar e pré-visualizar suas páginas da Web de forma confiável no espaço de design de conteúdo do Journey Optimizer B2B edition.

  >[!NOTE]
  >
  >O Google Chrome e o Microsoft Edge são, atualmente, os únicos navegadores compatíveis com a criação de páginas da Web no Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

## Instalar a extensão Auxiliar de edição visual

1. Abra uma nova guia no navegador ([!DNL Google Chrome] ou [!DNL Microsoft Edge]).

1. Vá para a [Google Chrome Web Store](https://chromewebstore.google.com/category/extensions).

   Se você estiver usando o [!DNL Microsoft Edge], selecione _Permitir extensões_ de outros armazenamentos no banner superior. Habilitar esta opção permite adicionar extensões de [!DNL Chrome Web Store] a [!DNL Microsoft Edge].

1. Pesquise e navegue até a extensão de navegador _[!DNL Adobe Experience Cloud Visual Editing Helper]_.

   ![Extensão do Adobe Experience Cloud Visual Editing Helper para Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar ao Chrome]** e em **[!UICONTROL Adicionar Extensão]** na caixa de diálogo de confirmação.

   Se você estiver usando o [!DNL Microsoft Edge], esta ação adicionará a extensão ao [!DNL Edge].

1. Verifique se a extensão de navegador [!DNL Visual Editing Helper] está habilitada corretamente na barra de ferramentas do navegador.

   ![Ícone da extensão Auxiliar de edição visual do Adobe Experience Cloud na barra de ferramentas do Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

O [!DNL Adobe Experience Cloud Visual Editing Helper] agora é habilitado automaticamente quando um site é aberto no editor visual do Journey Optimizer B2B edition para experiências da web. A extensão não tem configurações condicionais e lida com todas as configurações automaticamente, incluindo configurações de cookies SameSite.

>[!NOTE]
>
>Alguns sites podem não abrir de forma confiável no editor da Web do Journey Optimizer B2B edition devido a um dos seguintes motivos:
>
>* O site tem políticas de segurança rigorosas.
>* O site está em um iframe.
>* O site de controle de qualidade ou preparo do cliente não está disponível externamente (o site é interno).

## Criar uma experiência online

Você pode configurar experiências da Web em uma jornada ao [adicionar um nó _[!UICONTROL Executar uma ação]_](../journeys/action-nodes.md) e fazer o seguinte:

1. Para o destino _[!UICONTROL Ação em]_, escolha **[!UICONTROL Pessoas]**.

1. Para a _[!UICONTROL Ação em pessoas]_, escolha **[!UICONTROL Personalizar experiência da Web]**.

   ![Realizar uma ação - personalizar experiência da Web](./assets/web-experience-add-journey-node.png){width="500"}

1. Clique em **[!UICONTROL Criar experiência na Web]**.

1. Na caixa de diálogo _[!UICONTROL Criar experiência na Web]_, digite um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** úteis (opcional).

   * Nome - Máximo de 100 caracteres; deve ser exclusivo, não diferencia maiúsculas de minúsculas

   * Descrição - Máximo de 300 caracteres

   >[!NOTE]
   >
   >Os campos de nome e descrição suportam caracteres alfanuméricos, numéricos e especiais. Os caracteres reservados (`\ / : * ? " < > |`) **_não são permitidos_**.

   ![Caixa de diálogo Criar experiência na Web](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. Na guia **[!UICONTROL Propriedades]**, insira a descrição da experiência online.

1. Clique na guia **[!UICONTROL Ações]** e selecione o **[!UICONTROL canal da Web]** a ser usado para a experiência online.

   A configuração do canal da Web determina onde as modificações de conteúdo são aplicadas com base nas regras de correspondência da página configuradas. Consulte [Configurações do canal da Web](../admin/configure-channels-web.md) para obter mais informações.

   ![Configuração de canal da Web selecionada](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. Para definir as modificações da Web, clique em **[!UICONTROL Editar conteúdo]**.

   O editor é aberto na guia _[!UICONTROL Conteúdo]_, onde você pode definir as modificações para sua experiência online. Consulte [design de experiência na Web](./web-experience-design.md) para obter informações detalhadas sobre como usar as ferramentas de design para adicionar as modificações de conteúdo da experiência na Web.

1. No painel direito, defina as propriedades da experiência da Web de acordo com como você deseja defini-la e gerenciá-la.

   * **[!UICONTROL Editor visual]** - alternar entre o [editor visual e não visual](./web-experience-design.md#web-design-tools) para o design de modificação de experiência da Web.
   * **[!UICONTROL Redirecionamento de visitante]** - Habilite esta opção para [redirecionar visitantes para outra URL existente](#redirect-to-url) em vez de criar uma nova variação na guia de conteúdo.

   ![Alternar propriedades para o editor visual e a URL de redirecionamento](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Editar página da Web]** para [criar suas modificações na Web](./web-experience-design.md).

1. Quando as modificações forem concluídas, clique na seta para a esquerda acima do editor para retornar à guia de conteúdo e às propriedades do nó de experiência da Web personalizado.

   Você pode clicar na seta para a esquerda na parte superior para retornar à tela de jornada.

## Editar uma experiência online

1. Abra a jornada e selecione o nó de ação **[!UICONTROL Personalizar experiência da Web]**.

1. Para fazer alterações na configuração ou no conteúdo do canal Web, clique em **[!UICONTROL Editar experiência Web]**.

1. Selecione a guia **[!UICONTROL Ações]** e altere a configuração da Web conforme necessário.

1. Selecione a guia **[!UICONTROL Conteúdo]** e use as ferramentas de design visual conforme necessário.

   * _Editor visual_ - Clique em **[!UICONTROL Editar conteúdo]**.
   * _Editor não visual_ - Clique em **[!UICONTROL Adicionar uma modificação]**.

   Consulte o [design de experiência da Web](./web-experience-design.md) para obter informações detalhadas.

1. Quando as definições de modificação estiverem concluídas, clique na seta para a esquerda acima do editor para retornar à guia de conteúdo e às propriedades da experiência da Web.

   Você pode clicar na seta para a esquerda na parte superior para retornar à tela de jornada.

## Redirecionar para URL

Ao criar uma experiência da Web, você pode redirecionar os visitantes para outro URL existente, em vez de criar uma nova variação no editor de conteúdo. Essa opção é útil quando você deseja executar um experimento de conteúdo comparando duas experiências diferentes, em vez de apenas alterar alguns elementos em uma página.

Por exemplo, crie uma campanha da Web com dois tratamentos:

No Tratamento A, crie uma experiência da Web usando o editor de conteúdo para metade da população direcionada.

Em Tratamento B, selecione a opção _[!UICONTROL Redirecionar para URL]_ para a outra metade da população direcionada. Insira o URL de uma página com um design alternativo que você criou fora do Journey Optimizer B2B edition.

![Defina o redirecionamento de visitante para redirecionar visitantes para uma URL específica](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Com essa opção selecionada, a visualização do site não é exibida e a opção _[!UICONTROL Editor visual]_ é desativada.

Quando sua campanha da Web está ativa, você pode acompanhar o desempenho da experiência da Web definida no Journey Optimizer B2B edition em relação às experiências da Web que usaram um redirecionamento para a página alternativa.

## Testar a experiência da web

Após a conclusão do design de conteúdo para a experiência online, você pode usar o recurso _Simular conteúdo_ para visualizar as modificações da sua página da Web. Se você inseriu conteúdo personalizado, é possível usar os dados do perfil de teste para verificar como o conteúdo é renderizado. As ferramentas de simulação estão disponíveis na guia _[!UICONTROL Conteúdo]_ para a experiência online ou no editor de design visual de conteúdo.

1. Clique em **[!UICONTROL Simular conteúdo]** na parte superior direita.

1. Selecione um perfil de teste.

1. Adicione um perfil de teste para verificar sua página da Web usando os dados do perfil de teste.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## Ativar sua experiência online

Sua experiência na Web é ativada e se torna visível para o público-alvo quando você [publica a jornada](../journeys/create-publish-journey.md#publish-a-journey). Antes de ativar uma experiência da Web por meio de uma jornada, considere o seguinte:

* Se você publicar uma jornada com uma experiência da Web que afete as mesmas páginas que outra jornada já ativa, todas as alterações serão aplicadas às páginas da Web.

* Se várias jornadas atualizarem os mesmos elementos do site, a alteração aplicada mais recentemente terá prioridade.

### Requisitos de entrega

Para habilitar a entrega de experiência online, as seguintes configurações devem ser definidas:

* Na Coleção de dados da Adobe Experience Platform, verifique se você tem um fluxo de dados definido com a opção Adobe Journey Optimizer B2B edition ativada no serviço Adobe Experience Platform.

  Essa configuração garante que o Adobe Experience Platform Edge possa lidar corretamente com os eventos de entrada. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/datastreams/configure)

* Na Adobe Experience Platform, verifique se você tem uma política de mesclagem com a _[!UICONTROL Política de mesclagem ativa no Edge]_ ativada.

  Selecione uma política no menu Experience Platform Cliente > Perfis > Mesclar políticas. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Essa política de mesclagem é usada pelos canais de entrada do Journey Optimizer B2B edition para ativar e publicar corretamente as experiências de entrada da web na borda. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/merge-policies/ui-guide)

### Solução de problemas

Você pode usar a visualização do Edge Delivery no Adobe Experience Platform Assurance para solucionar problemas de entrega de experiências na Web do Journey Optimizer B2B edition. Este plug-in permite que você inspecione chamadas de solicitação em detalhes, verifique as chamadas de borda esperadas e examine dados do perfil. Esses dados de perfil incluem mapas de identidade, associações de segmento e configurações de consentimento. Você também pode revisar as atividades qualificadas e não qualificadas da solicitação.

Para obter mais informações sobre o modo de exibição Edge Delivery no Assurance, consulte a [documentação do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery).
