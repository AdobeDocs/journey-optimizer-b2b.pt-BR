---
title: Gerenciamento de público-alvo
description: Página de espaço reservado para públicos-alvo.
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 442
ht-degree: 4%

---

# Gerenciamento de públicos-alvo

Como os públicos-alvo são reproduzidos no AJO B2B Prime?

No hub de Gerenciamento de marketing, clique em **[!UICONTROL Listas de pessoas]** na navegação à direita.

![Acessar listas de pessoas para gerenciar seus públicos-alvo](./assets/people-lists.png){width="800" zoomable="yes"}

Há duas guias para a página onde você pode exibir e gerenciar **[!UICONTROL Listas dinâmicas]** e **[!UICONTROL Listas estáticas]**. Clique na guia para alternar a exibição de lista entre cada tipo.

Nessa página, é possível:

* Criar novas listas dinâmicas e estáticas
* Pesquisar listas existentes
* Consulte informações do ativo
* Listas de acesso para revisão de seus membros

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Criar uma lista de pessoas


Para criar uma nova lista dinâmica ou estática:

1. Clique em **Criar lista** na parte superior direita da página _[!UICONTROL Listas de pessoas]_.
1. Selecione um programa como **[!UICONTROL Pai]** para a lista.
1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** da lista (opcional).
1. Escolha e liste **[!UICONTROL Type]**:

   * **[!UICONTROL Estático]** - A associação é determinada por filtros qualificados avaliados quando você cria a lista. A associação à lista não é atualizada a menos que você qualifique ou desqualifique registros manualmente.
***[!UICONTROL Dinâmico]** - A associação é determinada dinamicamente por filtros qualificados. A associação à lista é atualizada automaticamente.

1. Clique em **[!UICONTROL Criar]**.

>[!NOTE]
>
>Atualmente, não há suporte para exclusão e duplicação em listas de pessoas nesta versão do Beta.

## Listas estáticas

A associação de lista estática é definida por filtros simples que fazem referência a atributos e atividades de pessoas. A associação não é alterada, a menos que você qualifique ou desqualifique membros manualmente.

### Adicionar membros

1. Abra a lista estática e clique em **[!UICONTROL Adicionar pessoas]** na parte superior direita.

1. Na caixa de diálogo, defina as regras para qualificar seus leads arrastando e soltando filtros da esquerda.

   É possível filtrar pessoas usando qualquer combinação de:

   * Histórico de atividades
   * Atributos da empresa
   * Atributos da pessoa
   * Filtros especiais, como associação de Jornada

1. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

1. Selecione a guia **[!UICONTROL Membros]**.

   Após um breve período, os membros qualificados serão exibidos na lista.

### Remover membros

1. Abra a lista estática e clique em **[!UICONTROL Remover pessoas]** na parte superior direita.

1. Na caixa de diálogo, adicione os filtros a membros correspondentes que você deseja desqualificar.

1. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

1. Selecione a guia **[!UICONTROL Membros]**.

   Após um breve período, os membros desqualificados deixam a lista.

## Listas dinâmicas

A associação de lista dinâmica é definida usando filtros simples que fazem referência a atributos e atividades de pessoas. A associação é mantida automaticamente ao qualificar e desqualificar leads de acordo com a lógica do filtro.

### Definir a lógica de associação

1. Abra a lista estática e selecione a guia Regras.

1. Clique em Editar regras.

1. Na caixa de diálogo, defina as regras para qualificar seus leads arrastando e soltando filtros da esquerda.

   Você pode qualificar leads para a lista usando qualquer combinação de:

   * Histórico de atividades
   * Atributos da empresa
   * Atributos da pessoa
   * Filtros especiais, como associação de Jornada

1. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

1. Selecione a guia **[!UICONTROL Membros]**.

   Após um breve período, os membros qualificados serão exibidos na lista.

Para abrir a página de detalhes do perfil de cliente potencial, onde é possível exibir o resumo e as atividades recentes, clique no nome de uma pessoa na lista.