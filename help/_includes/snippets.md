---
title: Bl. conteúdo
description: Notas e elementos visuais reutilizados para observar um recurso ou página que se aplica a uma edição específica
source-git-commit: 8892aff0501a157006506663ef304be5ccc9695c
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Bl. conteúdo

<!-- Content authoring steps for reuse -->

## Configuração de dados de intenção {#intent-data-note}

>[!NOTE]
>Os dados de intenção também podem ser incluídos na página quando configurada para sua instância do Journey Optimizer B2B edition. Para obter mais informações sobre o modelo de detecção de intenção e como enviar palavras-chave, consulte [Dados de intenção](../user/admin/intent-data.md).
>

## Nota de licenciamento de ativos AEM {#aem-assets-licensing-note}

>[!NOTE]
>
>As licenças da AEM Assets as a Cloud Service e da Dynamic Media são pré-requisitos para a integração. Você deve garantir que a [API do Dynamic Media withOpen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"} esteja habilitada.<br/>
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

   ![Arraste um ativo de Marketo Engage para a tela e ajuste as configurações](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## Criação de conteúdo - etapa de personalização {#personalization-step}

1. Insira campos de personalização para personalizar seu conteúdo de atributos de perfis, associações de público-alvo, atributos contextuais e muito mais.

## Criação de conteúdo - Ativar etapa de conteúdo de condição {#dynamic-content-step}

1. Clique em **[!UICONTROL Habilitar conteúdo de condição]** para adicionar conteúdo dinâmico e adaptar o conteúdo aos perfis direcionados com base em regras condicionais.

## Criação de conteúdo - etapa de rastreamento de links {#links-tracking-step}

1. Selecione a guia **[!UICONTROL Links]** no painel esquerdo para exibir todas as URLs do seu conteúdo que é rastreado.

   Você pode modificar o _Tipo de Rastreamento_ ou o _Rótulo_ e adicionar marcas, se necessário.
