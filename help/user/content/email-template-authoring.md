---
title: Criação de modelo de email
description: Saiba como criar modelos de email de conteúdo que podem ser usados para emails de jornada de conta para reutilizar seus designs de forma fácil e eficiente.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 11%

---

# Criação de modelo de email

Depois de [criar um modelo de email](./email-templates.md#create-an-email-template), use o designer visual para criar os componentes estruturais e de conteúdo no seu modelo de email.

## Adicionar estrutura e conteúdo {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do modelo. Arraste e solte um componente de **Estrutura** na tela para começar a criar o conteúdo do modelo."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um modelo."

{{$include /help/_includes/content-design-components.md}}

### Adicionar fragmentos

No editor de conteúdo visual, o ícone _Fragmentos_ é exibido à esquerda. O exemplo a seguir descreve as etapas para adicionar fragmentos ao conteúdo do modelo.

1. Para abrir a lista de fragmentos, selecione o ícone _Fragmentos_ ( ![ícone Fragmentos](../assets/do-not-localize/icon-fragments.svg) ).

   É possível:

   * Classifique a listagem.
   * Procurar, Pesquisar ou Filtrar a listagem.
   * Alternar entre as visualizações em Miniatura e em Lista.
   * Atualize a lista para refletir qualquer um dos fragmentos criados recentemente.

   ![Selecione um fragmento da lista](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Arraste e solte qualquer um dos fragmentos no espaço reservado do componente estrutural.

   O editor renderiza o fragmento na seção/elemento da estrutura de email.

O conteúdo do fragmento é atualizado dinamicamente na estrutura para mostrar como o conteúdo aparece no email.

>[!TIP]
>
>Se quiser que o fragmento ocupe todo o layout horizontal no email, adicione uma estrutura de coluna 1:1 e, em seguida, arraste e solte o fragmento nele.

Depois que o email for salvo, ele aparecerá na página de detalhes do fragmento ao selecionar a guia _[!UICONTROL Usado por]_ no resumo. Os fragmentos adicionados a um modelo de email não são editáveis no modelo — o fragmento de origem define o conteúdo.

### Adicionar ativos

{{$include /help/_includes/content-design-assets.md}}

### Navegar pelas camadas, configurações e estilos

{{$include /help/_includes/content-design-navigation.md}}

### Personalizar conteúdo

{{$include /help/_includes/content-design-personalization.md}}

### Editar rastreamento de URL vinculado

{{$include /help/_includes/content-design-links.md}}

## Exibir opções

Aproveite as opções de exibição e validação de conteúdo disponíveis no designer visual.

* Aumentar/diminuir o zoom do conteúdo nas opções de zoom predefinidas.

* Alternar a exibição do conteúdo na área de trabalho, dispositivo móvel ou somente texto/texto sem formatação.
   * Clique no ícone _Olho_ para visualizar o conteúdo entre dispositivos.
   * Selecione um dos dispositivos prontos para uso ou insira dimensões personalizadas para visualizar o conteúdo.

### Mais opções

No menu _[!UICONTROL Mais...]_, na parte superior do designer de email, você pode realizar as seguintes ações:

![Clique em Mais para acessar as ações do modelo](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Redefinir modelo]** - Clique nesta opção para limpar a tela do designer visual para uma folha em branco e reiniciar a compilação de conteúdo.
* **[!UICONTROL Salvar como fragmento]** - Salve todo o modelo ou partes dele como um fragmento a ser reutilizado em vários emails ou modelos de email. Forneça um nome e uma descrição para o fragmento e salve-o na lista de fragmentos disponíveis.
* **[!UICONTROL Alterar seu design]** - Retorne à página _Criar seu modelo_. A partir daí, você pode optar por projetar seu modelo do zero ou usar um modelo existente para reiniciar o processo de design.
* **[!UICONTROL Exportar HTML]** - Baixe o conteúdo na tela visual para o sistema local no formato HTML empacotado como um arquivo zip.
