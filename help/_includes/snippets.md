---
title: Bl. conteúdo
description: Notas e elementos visuais reutilizados para observar um recurso ou página que se aplica a uma edição específica
source-git-commit: d0b2f91754ce3c5e38c6aa2c49c816fd46510403
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Bl. conteúdo

<!-- Content authoring steps for reuse -->

## Configuração de dados de intenção {#intent-data-note}

>[!NOTE]
>
>Os dados de intenção são incluídos quando configurados para sua instância do Journey Optimizer B2B edition. Também é necessário que uma ou mais jornadas publicadas **ou** tenham criado grupos de compras. Para obter mais informações sobre o modelo de Detecção de Intenção e como enviar palavras-chave, produtos e categorias, consulte [Dados de Intenção](../user/admin/intent-data.md).

## Nota de licenciamento de ativos da AEM {#aem-assets-licensing-note}

>[!NOTE]
>
>As licenças do AEM Assets as a Cloud Service e do Dynamic Media são pré-requisitos para a integração. Você deve garantir que o [Dynamic Media withOpen API](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"} esteja habilitado.<br/>
>Dependendo do contrato e da configuração, o Adobe Experience Manager Assets as a Cloud Service pode ser acessado diretamente do Adobe Journey Optimizer B2B edition ao projetar conteúdo visual.

## Criação de conteúdo - Componentes - etapa de estruturas {#structures-step}

1. Para iniciar o design do conteúdo, arraste um item das **[!UICONTROL Estruturas]** e solte-o na tela.

   Adicione quantos itens de _[!UICONTROL Estruturas]_ forem necessários e edite as configurações para cada um no painel à direita.

   >[!TIP]
   >
   >Selecione o componente _[!UICONTROL n:n coluna]_ para definir o número de colunas de sua escolha (entre três e 10). Você também pode definir a largura de cada coluna movendo as setas abaixo dela.

   ![Arraste uma estrutura para a tela e ajuste as configurações](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   Cada tamanho de coluna não pode ser menor que 10% da largura total do componente de estrutura. Somente colunas vazias podem ser removidas.

## Criação de conteúdo - Componentes - etapa de conteúdo {#contents-step}

1. Expanda a seção **[!UICONTROL Conteúdo]** e adicione quantos elementos forem necessários em um ou mais componentes da estrutura.

   ![Arraste um elemento de conteúdo para a tela e ajuste as configurações](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## Criação de conteúdo - Componentes - Etapa de configurações {#settings-step}

1. Se necessário, você pode fazer personalizações adicionais para cada componente nas guias _[!UICONTROL Configurações]_ ou _[!UICONTROL Estilo]_.

   Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente.

## Criação de conteúdo - etapa de ativos {#assets-step}

1. No seletor de _Ativos_, você pode selecionar diretamente os ativos armazenados na biblioteca de ativos.

   Clique duas vezes na pasta que contém seus ativos. Arraste e solte os itens em um componente de estrutura.

   Para obter mais informações sobre como usar os ativos do seu tipo de origem, consulte [Adicionar ativos ao seu conteúdo](../user/content/assets-overview.md#use-assets-for-content-authoring).

   ![Arraste um ativo do Marketo Engage para a tela e ajuste as configurações](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## Criação de conteúdo - etapa de personalização {#personalization-step}

1. Insira campos de personalização para personalizar seu conteúdo de atributos de perfis, associações de público-alvo, atributos contextuais e muito mais.

## Criação de conteúdo - Ativar etapa de conteúdo de condição {#dynamic-content-step}

1. Clique em **[!UICONTROL Habilitar conteúdo de condição]** para adicionar conteúdo dinâmico e adaptar o conteúdo aos perfis direcionados com base em regras condicionais.

## Criação de conteúdo - etapa de rastreamento de links {#links-tracking-step}

1. Selecione a guia **[!UICONTROL Links]** no painel esquerdo para exibir todas as URLs do seu conteúdo que é rastreado.

   Você pode modificar o _Tipo de Rastreamento_ ou o _Rótulo_ e adicionar marcas, se necessário.
