---
title: Criação de fragmentos
description: Crie fragmentos de conteúdo reutilizáveis com ferramentas de design visual - adicione estrutura, ativos, personalização, conteúdo condicional e rastreamento de URL vinculado para emails e modelos no Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: e1663313-7961-4100-bea9-fa9f4edf8493id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# Criação de fragmentos

Depois de [criar um fragmento](./fragments.md#create-fragments), use o espaço de design visual para criar os componentes de estrutura e conteúdo no fragmento.

## Adicionar estrutura e conteúdo {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Adicionar ativos {#add-assets}

No espaço de design visual, selecione o ícone do _Assets_ ( ![Assets](../../assets/do-not-localize/icon-assets-me.svg) ) na barra de navegação à esquerda para procurar e selecionar ativos de imagem da biblioteca de ativos [!DNL Journey Optimizer B2B Prime].

Para obter as etapas para selecionar, substituir ou carregar ativos de imagem, consulte [Usar ativos para criação de conteúdo](./digital-asset-management.md#assets-authoring).

## Navegar pelas camadas, configurações e estilos {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personalizar conteúdo {#personalize-content}

[!DNL Journey Optimizer B2B Prime] usa a sintaxe Handlebars para personalização. Os tokens são substituídos no momento do envio por valores dos dados de perfil de cada recipient.

_Para adicionar personalização :_

1. Selecione o componente de texto e clique no ícone _Adicionar personalização_ ( ![Ícone de personalização](../../user/assets/do-not-localize/icon-personalize.svg) ) na barra de ferramentas.
1. Na caixa de diálogo de personalização, navegue na árvore do esquema à esquerda e selecione um atributo de perfil. O editor insere a expressão Handlebars correspondente — por exemplo, `{{profile.firstName}}`.
1. Adicione um valor de fallback para lidar com dados ausentes, se necessário — por exemplo, `{{profile.firstName | default: "there"}}`.
1. Clique em **[!UICONTROL Confirmar]** ou **[!UICONTROL Inserir]**. A expressão aparece em linha no campo.

Para obter detalhes sobre as ferramentas e a sintaxe do editor de expressões, consulte [editor do Personalization](./personalization-expressions.md).

## Editar rastreamento de URL vinculado {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
