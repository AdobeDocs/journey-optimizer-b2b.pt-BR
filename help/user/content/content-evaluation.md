---
title: Avaliação e pontuação de conteúdo
description: Avaliar o conteúdo de email com pontuação de alinhamento de marca - valide cores, fontes, logotipos e estilo de escrita em relação às diretrizes da marca no Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: bbdbf74b2fb0003b84ed4d7f84dce9aa3b796aea
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 8%

---

# Avaliação e pontuação de conteúdo {#content-scoring}

A avaliação e a pontuação do conteúdo ajudam a criar, revisar e gerenciar o conteúdo que segue as diretrizes [definidas na marca selecionada](./brands-manage-create.md#brand-definitions) e os padrões gerais de qualidade. A execução de uma avaliação garante a consistência no tom, nas mensagens e na identidade visual em suas campanhas de email, além de servir como uma verificação de qualidade antes do conteúdo ser publicado.

>[!AVAILABILITY]
>
>É necessário um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para que você possa usar recursos habilitados por IA no Adobe Journey Optimizer B2B edition. Para obter mais informações, entre em contato com o seu representante da Adobe.
>
>Consulte [Permissões relacionadas à marca](./brands-overview.md#brand-related-permissions) para obter informações sobre como administradores de produtos podem habilitar esses recursos.

## Executar uma avaliação

1. Após criar o conteúdo do email, clique no ícone de _Alinhamento da marca_ ( ![Ícone de alinhamento da marca](../assets/do-not-localize/icon-brand-compliance.svg) ) à direita para abrir o painel direito _Alinhamento da marca_ no espaço de design de email.

   A [marca padrão](./brands-manage-create.md#default-brand) é selecionada automaticamente.

   ![Acessar as ferramentas de alinhamento de marca](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Você pode clicar no ícone _Tela cheia_ ( ![Ícone de tela cheia](../assets/do-not-localize/icon-full-screen.svg) ) na parte superior do painel para exibir as ferramentas de alinhamento de marca no modo de tela cheia.

1. Se necessário, clique na seta de menu **[!UICONTROL Marca]** ( ![Seta para baixo](../assets/do-not-localize/icon-down-menu.svg) ) para escolher outra marca publicada.

1. Clique em **[!UICONTROL Avaliar pontuação]** para pontuar o alinhamento do conteúdo com a marca selecionada.

   O sistema avalia o conteúdo em relação às diretrizes da marca selecionada e exibe a pontuação resultante.

   ![Pontuações de avaliação no painel direito](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Pontuação de alinhamento da marca {#brand-alignment-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Seleção da marca"
>abstract="Selecione sua marca para garantir que o conteúdo seja criado em alinhamento com as diretrizes, os padrões e a identidade específicos, mantendo a consistência e a integridade da marca."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Pontuação de alinhamento da marca"
>abstract="A pontuação do alinhamento da marca mede o desempenho do conteúdo em seguir as diretrizes da marca para garantir a consistência nas cores, fontes, logotipo, imagem e estilo de escrita."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="Pontuação de cores"
>abstract="Pontuação de cores"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="Pontuação de fontes"
>abstract="Pontuação de fontes"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="Pontuação dos logotipos"
>abstract="Pontuação dos logotipos"

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível como um beta público.

Quando sua marca for bem definida e publicada, avalie a pontuação de alinhamento da marca diretamente no espaço de design de email para garantir que o conteúdo esteja alinhado às diretrizes da marca:

A pontuação é calculada de acordo com as violações identificadas no conteúdo de email avaliado:

* 100 = Perfeito - Nenhuma violação encontrada
* 80-99 = Bom - Somente pequenas violações
* 60-79 = Razoável - Algumas violações significativas
* Abaixo de 60 = Insatisfatório - As violações graves exigem atenção

Você pode examinar os resultados da avaliação com mais detalhes para ajudar a identificar violações e melhorar as pontuações de alinhamento da categoria (_Alto_, _Medium_ e _Baixo_).

Para o **[!UICONTROL Estilo de escrita]** ou **[!UICONTROL Conteúdo visual]**, clique na seta _Expandir_ ( ![Expandir seta](../assets/do-not-localize/icon-expand-right.svg) ) para exibir os detalhes da avaliação.

![Detalhes da avaliação do alinhamento da marca](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Clique no ícone _Tela cheia_ ( ![Ícone de tela cheia para obter insights detalhados](../assets/do-not-localize/icon-full-screen.svg) ) para obter uma exibição detalhada de cada pontuação do insight.

Selecione qualquer diretriz sinalizada para exibir comentários e sugestões específicos.

![Detalhes da avaliação do alinhamento da marca na exibição de tela inteira](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

Você pode fazer alterações no conteúdo e clicar em **[!UICONTROL Reavaliar pontuação]** para executar outra avaliação e verificar se há um resultado aprimorado.

## Pontuação de qualidade do conteúdo {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="Qualidade do conteúdo"
>abstract="Avalie a qualidade do conteúdo geral para identificar possíveis problemas de legibilidade, coesão do conteúdo e eficácia. A avaliação da qualidade é independente das diretrizes da sua marca."

>[!NOTE]
>
>A avaliação da qualidade do conteúdo é independente das diretrizes da marca. Mesmo que uma marca seja selecionada, suas diretrizes não serão aplicadas à verificação de qualidade. A seleção de marca só é relevante para a pontuação do alinhamento da marca.

Além do alinhamento da marca, você pode avaliar a qualidade geral do conteúdo para identificar possíveis problemas de legibilidade, coesão do conteúdo e eficácia, independentemente das diretrizes da sua marca.

Role até a seção **[!UICONTROL Qualidade do conteúdo]** para analisar os insights e as recomendações de qualidade.

![Avaliação da qualidade do conteúdo](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

Selecione qualquer item sinalizado para exibir comentários específicos e sugestões acionáveis de melhoria. As pontuações são baseadas nas seguintes categorias:

* **[!UICONTROL Eficácia do CTA]**: avalia o desempenho de sua call-to-action para motivar seus leitores a realizarem a ação desejada.
* **[!UICONTROL Linha de assunto]**: avalia a clareza, a relevância e a qualidade inspiradora de atenção para incentivar aberturas de email.
* **[!UICONTROL Legibilidade]**: mede a facilidade e o engajamento do seu conteúdo para que os leitores possam entender.
* **[!UICONTROL Verificação de spam]**: identifica disparadores de spam comuns que podem afetar a entrega.
* **[!UICONTROL Coerência de conteúdo]**: garante que o conteúdo flua sem problemas e permaneça no tópico.
* **[!UICONTROL Revisão]**: verifica problemas de ortografia, gramática e clareza.

Clique no ícone _Tela cheia_ ( ![Ícone de tela cheia para obter insights detalhados](../assets/do-not-localize/icon-full-screen.svg) ) para obter uma exibição detalhada da sua pontuação de qualidade.

![Exibição em tela cheia da avaliação de qualidade do conteúdo](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

Com base nas recomendações, você pode editar seu conteúdo para melhorar a legibilidade, a coesão do conteúdo e a qualidade geral. Clique em **[!UICONTROL Reavaliar pontuação]** depois de fazer alterações para atualizar a pontuação de qualidade.
