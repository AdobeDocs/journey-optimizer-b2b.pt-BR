---
title: Autor de um modelo controlado
description: Crie emails de modelos governados com conteúdo bloqueado - identifique áreas editáveis e trabalhe dentro das restrições de governança no Journey Optimizer B2B edition.
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
autotag-review: 2026-03-30T22:35:16.900Z
TQID: https://experienceleague.adobe.com/iwVl-dwU9oGG0rHQ9-J3EO5r3B778jQCe6XK742ArEo
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 1%

---

# Autor de um modelo controlado

Os designers de conteúdo podem habilitar a [governança (_bloqueio de conteúdo_)](./template-content-governance.md) ao criar modelos de email. Os recursos de governança permitem designar as partes do design que não podem ser alteradas quando usadas em uma jornada de conta. Quando você [seleciona um modelo salvo](./email-authoring.md#select-a-template) para criar um email, o espaço de design visual carrega o modelo para que você possa usá-lo como base para seu email.

Se o modelo tiver o controle ativado, um alerta será exibido no painel de propriedades à direita. Selecione **[!UICONTROL Realçar áreas editáveis]** na parte superior da tela para ver quais componentes e elementos de conteúdo são editáveis para uso na jornada.

![Exibir áreas editáveis em um modelo controlado](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Você também pode determinar os elementos que estão bloqueados ou editáveis usando a _árvore de navegação_. Clique no ícone da _Árvore de navegação_ ( ![Ícone de link](../assets/do-not-localize/icon-navigation-tree.svg) ) à esquerda da tela para exibir a árvore.

![Exibir áreas editáveis em um modelo controlado](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Os ícones indicam as configurações de bloqueio de conteúdo aplicadas.

| Ícone | Nome | Descrição |
|------|------|-------------|
| ![Ícone somente leitura](../assets/do-not-localize/icon-tree-lock.svg) | Somente leitura | O componente está bloqueado e não pode ser editado. Quando aplicados no nível raiz (_[!UICONTROL Corpo]_), todos os componentes filhos são bloqueados e não podem ser editados. |
| ![Ícone de edição de conteúdo](../assets/do-not-localize/icon-tree-content-lock.svg) | Bloqueio de conteúdo | O bloqueio de conteúdo é aplicado no nível do componente. |
| ![Ícone editável](../assets/do-not-localize/icon-edit.svg) | Editável | O componente é totalmente editável. No entanto, talvez não seja possível excluir o elemento. |
| ![Ícone de edição de conteúdo](../assets/do-not-localize/icon-tree-edit-text.svg) | Editável - somente conteúdo | O componente e o estilo são estáticos, mas você pode alterar o conteúdo (como texto ou imagem). |
