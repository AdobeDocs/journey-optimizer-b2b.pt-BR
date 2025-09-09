---
title: Pontuação de alinhamento da marca
description: Avaliar o conteúdo de email com pontuação de alinhamento de marca - valide cores, fontes, logotipos e estilo de escrita em relação às diretrizes da marca no Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
hide: true
hidefromtoc: true
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 11%

---

# Classificação de alinhamento da marca {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Seleção da marca"
>abstract="Selecione sua marca para garantir que o conteúdo seja criado em alinhamento com as diretrizes, os padrões e a identidade específicos, mantendo a consistência e a integridade da marca."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Pontuação de alinhamento da marca"
>abstract="A pontuação do alinhamento da marca mede o desempenho do conteúdo em seguir as diretrizes da marca, garantindo a consistência nas cores, fontes, logotipo, imagem e estilo de escrita."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors"
>title="Pontuação de cores"
>abstract="Pontuação de cores"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts"
>title="Pontuação de fontes"
>abstract="Pontuação de fontes"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos"
>title="Pontuação dos logotipos"
>abstract="Pontuação dos logotipos"

A avaliação do alinhamento da marca e as pontuações ajudam a criar, revisar e gerenciar o conteúdo que segue as diretrizes [definidas na marca selecionada](./brands-manage-create.md#brand-definitions). Ele garante a consistência no tom, nas mensagens e na identidade visual em todas as campanhas de email, além de servir como uma verificação de qualidade antes do conteúdo ser publicado.

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível como um beta privado, com disponibilidade progressiva planejada para todos os clientes em versões futuras.
>
>É necessário um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para que você possa usar recursos habilitados por IA no Adobe Journey Optimizer B2B edition. Para obter mais informações, entre em contato com o representante da Adobe.
>
>Consulte [Permissões relacionadas à marca](./brands-overview.md#brand-related-permissions) para obter informações sobre como administradores de produtos podem habilitar esses recursos.

## Validar o alinhamento da marca

Quando sua marca for bem definida e publicada, avalie a pontuação de alinhamento da marca diretamente no espaço de design de email para garantir que o conteúdo esteja alinhado às diretrizes da marca:

1. Após criar o conteúdo do email, clique no ícone de _Alinhamento da marca_ ( ![Ícone de alinhamento da marca](../assets/do-not-localize/icon-brand-compliance.svg) ) à direita para abrir o painel direito _Alinhamento da marca_ no espaço de design de email.

   A [marca padrão](./brands-manage-create.md#default-brand) é selecionada automaticamente.

   ![Acessar as ferramentas de alinhamento de marca](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Você pode clicar no ícone _Tela cheia_ ( ![Ícone de tela cheia](../assets/do-not-localize/icon-full-screen.svg) ) na parte superior do painel para exibir as ferramentas de alinhamento de marca no modo de tela cheia.

1. Se necessário, clique na seta de menu **[!UICONTROL Marca]** ( ![Seta para baixo](../assets/do-not-localize/icon-down-menu.svg) ) para escolher outra marca publicada.

1. Clique em **[!UICONTROL Avaliar pontuação]** para pontuar o alinhamento do conteúdo com a marca selecionada.

   O sistema avalia o conteúdo em relação às diretrizes da marca selecionada e exibe a pontuação resultante.

   ![Pontuação de avaliação do alinhamento da marca](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Revisar a avaliação

A pontuação é calculada de acordo com as violações identificadas no conteúdo de email avaliado:

* 100 = Perfeito - Nenhuma violação encontrada
* 80-99 = Bom - Somente pequenas violações
* 60-79 = Razoável - Algumas violações significativas
* Abaixo de 60 = Insatisfatório - As violações graves exigem atenção

Você pode examinar os resultados da avaliação com mais detalhes para ajudá-lo a identificar violações e melhorar suas pontuações de alinhamento de categoria (_Alto_, _Medium_ e _Baixo_) e examinar os detalhes. Para o **[!UICONTROL Estilo de escrita]** ou **[!UICONTROL Conteúdo visual]**, clique na seta _Expandir_ ( ![Expandir seta](../assets/do-not-localize/icon-expand-right.svg) ) para exibir os detalhes da avaliação.

![Detalhes da avaliação do alinhamento da marca](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Selecione qualquer diretriz sinalizada para exibir comentários e sugestões específicos.

Você pode fazer alterações no conteúdo e clicar em **[!UICONTROL Reavaliar pontuação]** para executar outra avaliação e verificar se há um resultado aprimorado.
