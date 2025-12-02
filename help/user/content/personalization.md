---
title: Personalização de conteúdo
description: Personalize emails B2B usando tokens de conta, pessoa e sistema no Journey Optimizer B2B edition. Saiba como usar o editor de personalização e a sintaxe.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: expressão, editor, início, personalização
source-git-commit: 5063f9a924aef0a54b05e9bf223fc2d4898bc5a5
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Personalização de conteúdo {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personalizar experiências de conteúdo"
>abstract="Use o **Adobe Journey Optimizer B2B edition** para adaptar suas mensagens a cada destinatário específico aproveitando os dados e as informações que você tem sobre ele. Pode ser o nome, a indústria, o título e muito mais."

Os recursos de personalização do [!DNL Adobe Journey Optimizer B2B Edition] permitem que você adapte suas mensagens de email a cada destinatário específico, aproveitando os dados e as informações que você tem sobre eles. Pode ser o nome, a indústria, o título e muito mais.

Usando o _editor de personalização_, você pode selecionar, organizar, personalizar e validar todos os dados para criar uma personalização personalizada para seu conteúdo. Use várias ferramentas, como funções auxiliares, para personalizar mensagens. O editor usa uma sintaxe de personalização em linha com base em _Handlebars_, em que as expressões são construídas com conteúdo delimitado por chaves duplas `{{}}`.

Ao processar a mensagem, o Journey Optimizer B2B edition substitui a expressão pelos dados contidos no conjunto de dados do Adobe Experience Platform e nos valores do sistema local. Por exemplo, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se dinamicamente `Hello John Doe`.

Usando essa sintaxe, você pode personalizar mensagens em vários campos, incluindo linhas de assunto de email, corpos de mensagens e informações do remetente.

## Tokens do Personalization

No [!DNL Journey Optimizer B2B Edition], você pode criar seu conteúdo de email dinâmico usando tokens de personalização:

* **Tokens de conta** - Esses tokens são baseados nos atributos da conta, como _nome da conta_, _setor_ e _número de funcionários_. Use esses tokens para preencher dados de atributo gerenciados pelo esquema **_Detalhes da conta de negócios XDM_**, que é definido no Adobe Experience Platform.

* **Tokens de pessoa** - Esses tokens são baseados nos atributos de pessoa de negócios, como _nome_, _cargo_ e _nome da empresa_. Use esses tokens para preencher dados de atributo gerenciados pelo esquema **_Detalhes de pessoa de negócios XDM_**, que é definido no Adobe Experience Platform.

* **Tokens do sistema** - Esses tokens são baseados nos valores do campo do sistema, como _data_, _hora_ e _link de cancelamento de inscrição_.

* **Meus tokens** (quando definido para a jornada) - Os [tokens personalizados definidos para a jornada](./personalization-my-tokens.md) onde o email está.

>[!NOTE]
>
>Saiba mais sobre os esquemas XDM na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}.

## editor do Personalization

O editor de personalização está disponível em cada contexto em que você precisa definir a personalização no conteúdo de email. No editor, você pode selecionar, organizar, personalizar e validar todos os dados para criar uma personalização personalizada para o seu conteúdo.

Adicione personalização em qualquer campo ou componente de conteúdo clicando no ícone _Adicionar personalização_ ( ![Adicionar ícone de personalização](../../assets/do-not-localize/icon-personalization-field.svg) ).

![editor do Personalization](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>As informações a seguir sobre o editor de personalização refletem as alterações disponíveis para [!DNL Journey Optimizer B2B Edition] ambientes provisionados na [arquitetura simplificada](../simplified-architecture.md).

### Tokens e funções auxiliares

Para usar um token de personalização ou uma função auxiliar, localize-o no painel de navegação esquerdo e clique em **+** para adicioná-lo à expressão.

Clique no ícone do menu _Mais_ ( **...** ) (ao lado do ícone _Adicionar_ ( **+** ) para exibir mais detalhes de cada atributo e adicionar os atributos usados com mais frequência aos _favoritos_. Os atributos adicionados aos favoritos podem ser acessados pelo menu **[!UICONTROL Favoritos]**, na navegação à esquerda do editor.

![editor do Personalization - menu Token Mais](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
Você também pode definir uma sequência de texto de fallback padrão que será exibida se um atributo de perfil do tipo sequência estiver vazio. Clique no ícone _Mais menu_ ( **...** ) do atributo e selecione **[!UICONTROL Inserir com texto de fallback]**. Insira o texto a ser exibido quando o valor do atributo estiver vazio para um perfil e clique em **[!UICONTROL Adicionar]**.

É uma prática recomendada validar a expressão antes de inseri-la no conteúdo. Clique em **[!UICONTROL Validar]** na parte inferior do editor para verificar sua sintaxe e garantir que não haja erros.

![código validado pelo editor do Personalization](./assets/personalization-editor-validated.png){width="500"}

Quando a expressão estiver concluída e sem erros, clique em **[!UICONTROL Salvar]**.

### Conjuntos de dados personalizados

Você pode usar esquemas relacionais (classes baseadas em modelo) para personalização de email. Os objetos personalizados são definidos em _esquemas relacionais_, e um administrador de produto pode [configurar campos de esquemas relacionais](../admin/xdm-field-management.md#relational-schemas) em [!DNL Journey Optimizer B2B Edition]. Esses campos estão acessíveis no editor de personalização. Somente objetos personalizados que têm uma relação um para muitos (1:M) com a Conta <!-- (M1.5 Beta) or Person (M1.5 GA) --> estão disponíveis.

>[!IMPORTANT]
>
>Antes de usar objetos personalizados para personalização com script, revise e compreenda a [linguagem de modelo do Handlebar](https://handlebarsjs.com/guide/), a [sintaxe de personalização](./personalization-syntax.md) e as [funções auxiliares](./personalization-helper-functions.md) internas.

Ao definir a personalização usando os objetos personalizados, você pode acessar todas as variáveis em objetos acessíveis por script nos **[!UICONTROL tokens do Personalization]** (pessoa/lead, conta, sistema e Meus tokens) e nas **[!UICONTROL classes baseadas em modelo]** (esquemas relacionais). Com as classes baseadas em modelo selecionadas, é possível exibir os campos clicando na pasta do objeto personalizado. Clique em **+** para cada campo que você deseja adicionar à expressão.

![Editor do Personalization - Classes baseadas em modelo - adicionar campos de objeto personalizados](./assets/personalization-editor-custom-object-fields.png){width="800" zoomable="yes"}

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->