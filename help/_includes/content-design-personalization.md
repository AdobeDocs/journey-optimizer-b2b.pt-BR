---
title: Criação de conteúdo - personalização
description: Seção reutilizada sobre o uso de personalização para criação de conteúdo
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Criação de conteúdo - personalização

O Journey Optimizer B2B edition usa uma sintaxe simples em linha que permite criar expressões com conteúdo personalizado delimitado por chaves duplas `{}`. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições.

Exemplos:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Ao processar o conteúdo, o Journey Optimizer B2B edition substitui a expressão pelos dados contidos no banco de dados Experience Platform. Assim, o primeiro exemplo torna-se _Olá, John Doe_.

O exemplo a seguir descreve as etapas para personalizar o conteúdo usando atributos de lead/conta e tokens de sistema.

1. Selecione o componente de texto e clique no ícone _Adicionar personalização_ na barra de ferramentas.

   ![Clique no ícone Personalizar](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Esta ação abre a caixa de diálogo _Editar Personalization_.

1. Clique em **+** ou **...** para adicionar um token ao espaço em branco.

   ![Construir texto personalizado usando tokens](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.
