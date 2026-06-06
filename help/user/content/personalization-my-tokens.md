---
title: Tokens personalizados para o Personalization de email
description: Criar e gerenciar Meus tokens personalizados para personalização dinâmica de email - defina variáveis de texto e número para jornadas de conta no Journey Optimizer B2B edition.
feature: Personalization, Content, Email Authoring
role: User
exl-id: 05d4f446-6348-4555-9c46-316c2857f01d
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
autotag-review: 2026-03-30T22:21:17.156Z
TQID: https://experienceleague.adobe.com/PhcREmr9HfV-uGyGUB6YRATemaGn0du0VWaGaBHUmxY
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 605
ht-degree: 2%

---

# Tokens personalizados para personalização de email

A personalização de conteúdo usa tokens como espaços reservados ou variáveis que são preenchidas quando o artefato de conteúdo é gerado. Os tokens de personalização padrão estão disponíveis para emails, landing pages, fragmentos e templates. Você também pode definir um conjunto de tokens personalizados com valores específicos para a jornada da conta. Este conjunto de tokens personalizados é chamado de _Meus tokens_, e qualquer um desses tokens personalizados serve para personalização ao [criar emails de jornada](./email-authoring.md#content-authoring---personalization).

Além de _Meus tokens_, que são específicos para a jornada da conta, você pode usar qualquer um dos tokens padrão (incorporados) para personalização de email.

## Gerenciar meus tokens {#my-tokens}

Os _Meus tokens_ são variáveis personalizadas que você cria ou modifica para uma jornada de conta no status Rascunho. Este conjunto de tokens personalizado atualmente oferece suporte a definições de token de texto e número.

Ao adicionar um token personalizado a um email, ele é exibido como `{{my.TokenName}}`. Por exemplo, você pode ter `{{my.EventDate}}` ou `{{my.WebinarSpeaker}}` tokens criados para gerenciar conteúdo de email relacionado a webinários futuros.

_Para acessar os tokens personalizados de uma jornada de conta :_

1. Abra a jornada da conta de rascunho.

1. Clique no menu **[!UICONTROL Mais...]** na parte superior direita e escolha **[!UICONTROL Meus tokens]**.

   ![Clique em “Mais” no canto superior direito](../journeys/assets/account-journey-draft-more-menu.png){width="450"}

   A página _Meus tokens_ lista todos os tokens personalizados definidos para a jornada.

   ![Meus tokens](./assets/my-tokens-list-page.png){width="700" zoomable="yes"}

### Criar um token

1. Na página _[!UICONTROL Meus tokens]_, clique em **[!UICONTROL Criar]** e escolha o tipo de token que deseja definir:

   * **[!UICONTROL Texto]** - Use este tipo para definir um token com um valor de cadeia de caracteres de texto básico.

   * **[!UICONTROL Número]** - Use este tipo para definir um token com um valor numérico.

1. Na caixa de diálogo, insira o **[!UICONTROL Nome]** e o **[!UICONTROL Valor]** para o token.

   ![Insira um nome e um valor para o token de texto](./assets/my-tokens-create-text-token-dialog.png){width="400"}

   Não é possível usar espaços ou caracteres especiais no nome do token. Você pode usar _camel case_, como `EventType`, para usar um nome com várias palavras que seja facilmente identificado.

   Se você estiver definindo um token de _Número_, o valor poderá conter somente caracteres numéricos. Você pode usar um valor decimal.

   ![Insira um nome e um valor para o token numérico](./assets/my-tokens-create-number-token-dialog.png){width="400"}

1. Clique em **[!UICONTROL Adicionar]**.

### Editar um token

Embora a jornada da conta permaneça no status de rascunho, é possível editar qualquer um dos Meus tokens definidos.

1. Na página _[!UICONTROL Meus tokens]_, clique no ícone _Mais ações_ (**...**) ao lado do nome do token, escolha **[!UICONTROL Editar]**.

   ![Token do menu Mais ações](./assets/my-tokens-more-actions.png){width="430"}

1. Na caixa de diálogo, altere o **[!UICONTROL Nome]** e o **[!UICONTROL Valor]** conforme necessário para a jornada.

   ![Alterar o nome e o valor do token](./assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. Clique em **[!UICONTROL Editar]**.

### Excluir um token

É possível excluir um token personalizado da lista _Meus tokens_, mas verifique se ele não está sendo usado no momento no conteúdo de email da jornada.

1. Na página _[!UICONTROL Meus tokens]_, clique no ícone _Mais ações_ (**...**) ao lado do nome do token, escolha **[!UICONTROL Excluir]**.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

## Usar tokens personalizados em seu conteúdo

Ao criar conteúdo de email para sua jornada de conta, você pode usar qualquer um dos tokens da lista _Meus tokens_ ao usar as ferramentas de personalização no espaço de design visual.

1. Selecione o componente de texto e clique no ícone _Adicionar personalização_ ( ![Adicionar ícone de personalização](../../assets/do-not-localize/icon-personalization-field.svg) ) na barra de ferramentas.

   ![Clique no ícone Adicionar personalização](./assets/email-personalize-text.png){width="600"}

   Esta ação abre a caixa de diálogo _Editar Personalization_. A caixa de diálogo inclui uma pasta _[!UICONTROL Meus tokens]_ na biblioteca _[!UICONTROL Tokens do Personalization]_ se houver tokens personalizados definidos para a jornada de conta.

1. Para adicionar um de seus tokens personalizados ao espaço em branco, expanda a pasta **[!UICONTROL Meus tokens]** e clique em **+** ou **...**.

   É possível adicionar qualquer texto estático adicional, conforme necessário.

   ![Construir texto personalizado usando Meus tokens](./assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.
