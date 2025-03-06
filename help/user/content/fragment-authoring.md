---
title: Criação de fragmentos
description: Saiba como criar fragmentos de conteúdo que podem ser reutilizados para seus emails e designs de modelo para obter eficiência e manter os padrões de design e marca.
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 14%

---

# Criação de fragmentos

Depois de [criar um fragmento](./fragments.md#create-fragments), use o editor visual para criar os componentes estruturais e de conteúdo no fragmento.

## Adicionar estrutura e conteúdo {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do fragmento. Arraste e solte um componente de **Estrutura** na tela para começar a criação do conteúdo do fragmento."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Sobre os componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de um fragmento."

{{$include /help/_includes/content-design-components.md}}

## Adicionar ativos

{{$include /help/_includes/content-design-assets.md}}

## Navegar pelas camadas, configurações e estilos

{{$include /help/_includes/content-design-navigation.md}}

## Personalizar conteúdo

{{$include /help/_includes/content-design-personalization.md}}

## Habilitar campos personalizados

Quando um autor de email ou de modelo de email adiciona o fragmento, o conteúdo do fragmento é bloqueado por padrão. Quaisquer alterações no fragmento publicado são propagadas automaticamente para todos os ativos de conteúdo nos quais o fragmento é usado. Quando você designa um parâmetro para um componente no fragmento como editável, o autor do email ou modelo pode especificar um valor de campo personalizado específico para suas necessidades. Esse sinalizador de personalização é limitado aos componentes visuais de imagem, texto e botão.

Por exemplo, se você criar um banner reutilizável que inclua um botão clicável, poderá designar o parâmetro de URL do botão como editável. Os autores de email podem usar um URL mais específico para a campanha de email. Com esses campos personalizáveis, os profissionais de marketing podem gerenciar e personalizar o conteúdo sem a necessidade de criar blocos de conteúdo totalmente novos ou interromper as atualizações herdadas do fragmento original.

1. No editor de conteúdo visual, selecione a imagem, o texto ou o elemento de botão no qual deseja habilitar a personalização.

1. Nos detalhes do componente à direita, selecione a guia **[!UICONTROL Campos editáveis]**.

1. Clique na opção **[!UICONTROL Habilitar edição]** e defina os campos editáveis.

   ![Habilitar campos editáveis para um componente de imagem de fragmento](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Você pode ativar a personalização para os campos exibidos, que dependem do tipo de componente e dos parâmetros definidos no fragmento.

   Altere a alternância para um estado ativado para cada campo onde deseja permitir a personalização.

1. Clique em **[!UICONTROL Visão geral]** para revisar todos os campos editáveis e seus valores padrão.

   ![Revisar os campos editáveis e seus valores padrão](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Salve as alterações.

## Editar rastreamento de URL vinculado

{{$include /help/_includes/content-design-links.md}}
