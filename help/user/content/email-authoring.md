---
title: Criação de mensagens de email
description: Saiba como criar conteúdo de email no Adobe Journey Optimizer B2B. Use modelos, importações do HTML e ferramentas alimentadas por IA para personalizar e otimizar suas comunicações por email.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 15%

---

# Criação de mensagens de email

Depois de &lbrack;adicionar um novo ativo de email<!-- or duplicated --> a um nó de ação de jornada&rbrack;(./add-email.md), você pode definir o conteúdo da mensagem de email.

Clique em **[!UICONTROL Adicionar conteúdo de email]** na parte superior do painel de visualização do _[!UICONTROL Email]_.

![Clique em Adicionar conteúdo de email ](./assets/add-email-content.png){width="700" zoomable="yes"}

Essa ação inicia as ferramentas de design de email, onde você pode escolher como deseja criar seu email a partir das seguintes opções:

* [Crie o email do zero](#design-your-email-from-scratch) usando a interface Designer de email.

* [Importe conteúdo existente do HTML](#import-existing-html-content) de um arquivo ou de uma pasta .zip.

* [Selecione um modelo existente](#select-a-template) em uma lista de modelos de email predefinidos ou personalizados.

Para configurar e personalizar a linha de assunto com o editor de expressão, clique no ícone _Personalization_ e adicione qualquer um dos tokens do Marketo Engage.

Após criar e personalizar o conteúdo do email, você pode exportar o conteúdo para validação ou para uso posterior. Clique em **[!UICONTROL Exportar HTML]** para salvar o conteúdo como um arquivo .zip que inclui seu HTML e seus ativos.

>[!TIP]
>
>Use o Assistente de IA no Adobe Journey Optimizer B2B edition, viabilizado pela IA gerativa, para elevar seu conteúdo ao próximo nível. O Assistente de IA pode ajudá-lo a otimizar o impacto de seus deliveries, gerando emails inteiros, conteúdo de texto direcionado e obtendo recomendações do Assistente de IA para imagens que refletem em seu público-alvo. [Saiba mais](./ai-assistant-emails.md)

## Criar email do zero {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout da página de destino. Arraste e solte um componente de **Estrutura** na tela para começar a criação do conteúdo da página de destino."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Sobre os componentes de conteúdo"
>abstract="Os componentes de conteúdo são espaços reservados de conteúdo vazios que você pode usar para criar o layout de uma página de destino."

Use o editor de conteúdo visual para definir a estrutura do conteúdo de email. Ao adicionar e mover componentes estruturais com ações simples de arrastar e soltar, você pode criar a forma do conteúdo de email reutilizável em segundos.

1. Na página inicial _[!UICONTROL Criar seu modelo]_, selecione a opção **[!UICONTROL Criar do zero]**.

1. [Adicionar estrutura e conteúdo](#add-structure-and-content) à mensagem de email.
1. [Adicionar ativos de imagem](#add-assets) à mensagem de email.
1. [Personalizar o conteúdo do email](#personalize-content).
1. [Examinar e atualizar links](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Quando o conteúdo estiver concluído, clique em **[!UICONTROL Simular conteúdo]** na parte superior para verificar a renderização. Você pode escolher a visualização de desktop ou móvel.

Quando estiver satisfeito com o conteúdo, clique em **[!UICONTROL Salvar]**.

## Importar conteúdo existente do HTML

{{$include /help/_includes/content-design-import.md}}

![importar conteúdo html em um arquivo zip](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Usar uma marca `<table>` como a primeira camada em um arquivo do HTML pode causar perda de estilo, incluindo configurações de plano de fundo e largura na marca de camada superior.

Você pode personalizar o conteúdo importado conforme necessário com as ferramentas do editor visual de email.

## Selecione um modelo

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Os modelos salvos podem ter configurações de governança (bloqueio de conteúdo) aplicadas a um ou mais componentes. O designer visual fornece diretrizes sobre componentes bloqueados quando você [cria um email a partir de um modelo controlado](./email-authoring-governance.md).

## Adicionar estrutura e conteúdo {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Adicionar componentes da estrutura"
>abstract="Os componentes de estrutura definem o layout do email. Arraste e solte um componente de **Estrutura** na tela para iniciar a criação do conteúdo de email."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Sobre os componentes de conteúdo"
>abstract="Componentes de conteúdo são espaços reservados de conteúdo vazios que podem ser usados para criar o layout de um email."

{{$include /help/_includes/content-design-components.md}}

### Adicionar fragmentos

{{$include /help/_includes/content-design-use-fragments.md}}

Depois que o email for salvo, ele aparecerá na página de detalhes do fragmento ao selecionar a guia _[!UICONTROL Usado por]_ no resumo.

### Adicionar ativos

{{$include /help/_includes/content-design-assets.md}}

### Navegar pelas camadas, configurações e estilos

{{$include /help/_includes/content-design-navigation.md}}

### Personalizar conteúdo

{{$include /help/_includes/content-design-personalization.md}}

>[!NOTE]
>
>Se _[!UICONTROL Meus tokens]_ forem definidos para a jornada da conta, você também poderá usar esses tokens específicos da jornada para o seu conteúdo de email. Consulte [Personalizar tokens para personalização de email](./personalization-my-tokens.md) para obter mais informações.

### Editar rastreamento de URL vinculado

{{$include /help/_includes/content-design-links.md}}

### Exibir opções

Aproveite as opções de exibição e validação de conteúdo disponíveis no editor visual de email.

* Aumentar/diminuir o zoom do conteúdo nas opções de zoom predefinidas.

* Alternar a exibição do conteúdo na área de trabalho, dispositivo móvel ou somente texto/texto sem formatação.
   * Clique no ícone _Exibir_ para visualizar o conteúdo entre dispositivos.
   * Selecione um dos dispositivos prontos para uso ou insira dimensões personalizadas para visualizar o conteúdo.

### Mais opções

No menu _[!UICONTROL Mais...]_, na parte superior do espaço de design de email, você pode realizar as seguintes ações:

![Clique em Mais para acessar as ações do modelo](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Redefinir email]** - Clique nesta opção para limpar a tela do designer de email visual em branco e reiniciar a criação do conteúdo.
* **[!UICONTROL Salvar como fragmento]** - Salve todo o email ou partes dele como um fragmento a ser reutilizado em vários emails ou modelos de email. Forneça um nome e uma descrição para o fragmento e salve-o na lista de fragmentos disponíveis.
* **[!UICONTROL Alterar seu design]** - Retorne à página _Criar seu email_. A partir daí, você pode escolher outro modelo para reiniciar o processo de design ou optar por projetar o conteúdo do zero em uma tela preta.\
* **[!UICONTROL Salvar como modelo de conteúdo]** - Salve o corpo do email como um modelo de email a ser reutilizado em vários emails ou modelos de email. Forneça um nome e uma descrição para o modelo e salve-o na lista de modelos de email salvos.
* **[!UICONTROL Exportar HTML]** - Baixe o conteúdo na tela visual para o sistema local no formato HTML empacotado como um arquivo zip.

## Verificar e testar o email {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Verificar como o conteúdo está sendo renderizado"
>abstract="Após o conteúdo ser definido, você poderá visualizá-lo e verificar se a renderização está correta de acordo com o canal que está usando."

Quando o conteúdo da mensagem é definido, você pode usar perfis de teste para pré-visualizá-la, enviar provas e controlar sua renderização em clientes populares de desktop, móveis e baseados na Web. Se você inseriu conteúdo personalizado, é possível visualizar como esse conteúdo é exibido na mensagem usando os dados do perfil de teste.

Para visualizar o conteúdo do email, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar sua mensagem usando os dados do perfil de teste.

![Simular o conteúdo do email para verificar seu design](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
