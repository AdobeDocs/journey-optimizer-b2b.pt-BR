---
title: Modelos de email
description: Crie modelos de email reutilizáveis do zero, da importação do HTML ou de designs existentes - gerencie modelos para jornadas de conta no Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: b27b4485e5d778f0d4cbcad7392ab19c42a79e14
workflow-type: tm+mt
source-wordcount: '1533'
ht-degree: 0%

---

# Modelos de email

Para um processo de design acelerado e aprimorado, você pode criar modelos de email independentes para reutilizar seu conteúdo personalizado nas jornadas de conta do [!DNL Adobe Journey Optimizer B2B Edition]. Por meio de modelos, os membros da equipe orientados a conteúdo podem trabalhar no conteúdo de email fora do jornada. Os estrategistas de marketing podem então reutilizar e adaptar esses templates independentes dentro de suas jornadas. Por exemplo, um membro da equipe é responsável apenas pelo conteúdo, sem acesso às jornadas da conta. No entanto, eles podem criar um template de email que os profissionais de marketing podem selecionar como ponto de partida para comunicações por email e personalizá-lo de acordo com os requisitos da jornada.

## Acessar e gerenciar modelos de email

Para acessar modelos de email no [!DNL Journey Optimizer B2B Edition], vá para a navegação à esquerda e clique em **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Modelos]**. No painel lateral, selecione **[!UICONTROL Modelos de email]**.

Essa ação abre uma página de listagem com todos os templates de email criados na instância listada no formato de tabela.

A lista é classificada pela coluna _[!UICONTROL Modificado]_ por padrão, com os modelos atualizados mais recentes no topo. Clique no título da coluna para alterar entre crescente e decrescente.

Para pesquisar um modelo por nome, digite uma string de texto na barra de pesquisa. Clique no ícone _Filtro_ na parte superior esquerda para filtrar a lista de acordo com as datas de criação ou modificação e os modelos que você criou ou modificou.

![Acessar a biblioteca de modelos de email e filtrar por nome e datas](./assets/templates-list-search-filter.png){width="800" zoomable="yes"}

Personalize as colunas que deseja exibir na tabela clicando no ícone _Personalizar tabela_ ( ![Ícone Personalizar tabela](../assets/do-not-localize/icon-column-settings.svg) ) na parte superior direita. Selecione as colunas a serem exibidas e clique em **[!UICONTROL Aplicar]**.

Na lista exibida de modelos, é possível realizar as ações descritas nas seções a seguir.

## Criar um modelo de email

Você pode criar um modelo de email na página de listagem de modelos de email clicando em **[!UICONTROL Criar modelo]** na parte superior direita.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** úteis (opcional).

   ![Inserir propriedades iniciais para o novo modelo de email](./assets/templates-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

A página _[!UICONTROL Criar seu modelo]_ é aberta e fornece várias opções para a criação do modelo: _[!UICONTROL Criar do zero]_, _[!UICONTROL Importar HTML]_ ou _[!UICONTROL Selecionar modelo de design]_.

![Escolha como deseja começar com o design do seu modelo de email](./assets/templates-create-design.png){width="800" zoomable="yes"}

Após selecionar o método que deseja usar para iniciar o design do modelo de email, use o espaço de design visual para [criar o conteúdo do modelo de email](./email-template-authoring.md).

### Criar do zero

Use o editor de conteúdo visual para definir a estrutura do conteúdo de email. Ao adicionar e mover componentes estruturais com ações simples de arrastar e soltar, você pode criar a forma do conteúdo de email reutilizável em segundos.

>[!NOTE]
>
>As ferramentas de design disponíveis são equivalentes às ferramentas usadas para [criação de email](./email-authoring.md). A diferença é que esse conteúdo é então salvo como um modelo que pode ser reutilizado em vários nós _enviar email_ nas jornadas da conta.

1. Na página inicial _[!UICONTROL Criar seu modelo]_, selecione a opção **[!UICONTROL Criar do zero]**.

1. Na caixa de diálogo _[!UICONTROL Criar email]_, escolha o tipo de conteúdo de email que deseja usar para o modelo.

   * **[!UICONTROL Usar Temas]** - Escolha esta opção para criar o modelo de email no _Modo de tema_. Nesse modo, é possível usar um tema de marca definido para simplificar o processo de criação de conteúdo e garantir que o design se alinhe aos padrões definidos.

   ![Criar seu email - Usar temas](./assets/create-email-use-theme.png){width="450"}

   * **[!UICONTROL Estilo Manual]** - Escolha esta opção para criar o modelo de email no _Modo manual_. Nesse modo, você define manualmente o estilo de todos os componentes de estrutura e conteúdo adicionados à tela em branco.

1. (_Modo de temas_ somente) Aplicar um tema.

   No espaço de design de email, clique no ícone _Temas_ ( ![Temas](../assets/do-not-localize/icon-design-themes.svg) ) à direita.

   ![Espaço de design de email - Ícone de temas selecionado](./assets/email-design-themes-icon-selected.png){width="600" zoomable="yes"}

   O tema padrão ou o tema aplicado ao modelo é exibido. Você pode alternar entre as variantes de cor deste tema.

   Clique na seta ao lado do tema exibido para exibir a lista de temas personalizados e do Adobe disponíveis. Selecione **[!UICONTROL Meus temas]** para usar um tema personalizado criado para sua organização.

   Ao clicar fora da lista, o tema selecionado aplica os estilos. É possível alternar entre as variantes de cor.

1. [Adicionar estrutura e conteúdo](./email-authoring.md#add-structure-and-content) ao modelo.

   Se houver um tema aplicado, os componentes adicionados herdarão automaticamente os estilos definidos no tema.

### Importar HTML

O Adobe Journey Optimizer B2B edition permite importar conteúdo existente do HTML para criar seus modelos de email.

{{$include /help/_includes/content-design-import.md}}

![importar conteúdo html em um arquivo zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>Usar uma marca `<table>` como a primeira camada em um arquivo do HTML pode causar perda de estilo, incluindo configurações de plano de fundo e largura na marca de camada superior.

Você pode personalizar o conteúdo importado conforme necessário no espaço de design visual.

### Selecionar um modelo de design

{{$include /help/_includes/content-design-select-template.md}}

## Exibir detalhes do modelo de email

Na página da listagem de modelos, clique no nome de um modelo de email para abrir a página de detalhes do modelo de email. Aqui, é possível visualizar as propriedades básicas do modelo de email e acessar o editor de conteúdo visual para fazer alterações no conteúdo do modelo.

![Acessar a biblioteca de modelos de email e filtrar por nome e datas](./assets/template-details.png){width="700" zoomable="yes"}

* Exibir os detalhes do modelo de email, como nome e descrição. Essas configurações podem ser editadas. Clique fora da caixa de descrição para salvar as alterações automaticamente.

* Visualize as propriedades do template de email, como criado por, criado em, atualizado pela última vez em e modificado por.

* Clique em **[!UICONTROL Mais]** na parte superior direita para executar ações rápidas no modelo de email, como _Duplicar_ e _Excluir_.

* Se houver alertas ativos (erros e avisos para o modelo de email), clique em **[!UICONTROL Alertas]** na parte superior direita para exibir as informações.

  Esses alertas não proíbem o uso do modelo de e-mail para criação de e-mails. As informações fornecem visibilidade aos profissionais de marketing da sua equipe sobre o que pode não funcionar e as atualizações necessárias antes que possam ser usadas para o delivery.

## Exibir modelo de email usado por referências

Na página de detalhes dos modelos de email, clique na guia **[!UICONTROL Usado por]** para exibir detalhes sobre onde esse modelo de email é usado em emails nas jornadas de conta.

![Clique na guia Usado por para verificar o uso do modelo](./assets/template-details-used-by.png){width="400"}

Os emails no Journey Optimizer B2B edition são incorporados e criados no jornada, portanto, a jornada principal do email que usa o modelo é exibida nas referências.

* Ao clicar no link, você é direcionado ao email de jornada correspondente onde o template de email é usado.

* Saia da exibição a qualquer momento clicando na seta Voltar, que o levará de volta à página da listagem.

## Editar modelos de email

Esta ação pode ser tomada a partir de:

* A página de detalhes - Clique em **[!UICONTROL Editar modelo de email]**.
* A página de listagem - Clique nas reticências (**...**) ao lado de um modelo de email e escolha **[!UICONTROL Editar]**.

Esta ação direciona você à página _Criar modelo_ ou à página do editor de conteúdo visual (com base no último status salvo do modelo de email). Aqui, você pode editar o conteúdo do seu modelo de email conforme necessário. Consulte [Criar modelos de email](#create-email-templates) para obter informações sobre as opções de edição.

## Modelos de email duplicados

É possível duplicar um template de email usando um dos seguintes métodos:

* Nos detalhes do modelo de email à direita, expanda **[!UICONTROL Mais]** e clique em **[!UICONTROL Duplicar]**.

  ![Clique em Mais para acessar as ações Excluir e Duplicar](./assets/template-details-more-menu.png){width="400"}

* Na página de listagem _[!UICONTROL Modelos de email]_, clique nas reticências (...) ao lado do modelo e escolha **[!UICONTROL Duplicar]**.

Na caixa de diálogo do, digite um nome útil (exclusivo) e uma descrição. Clique em **[!UICONTROL Duplicar]** para concluir a ação.

O (novo) modelo de email duplicado aparece na lista _[!UICONTROL Modelos de email]_.

## Excluir modelos de email

A remoção de um modelo de email não pode ser desfeita, portanto, verifique antes de iniciar uma ação de exclusão. É possível excluir um template de email usando um dos seguintes métodos:

* Nos detalhes do modelo à direita, expanda **[!UICONTROL Mais]** e clique em **[!UICONTROL Excluir]**.
* Na página de listagem _[!UICONTROL Modelos de email]_, clique nas reticências (...) ao lado do modelo e escolha **[!UICONTROL Excluir]**.

  ![Clique em ... para acessar as ações Duplicar e Excluir](./assets/templates-list-more-menu.png){width="500"}

Essa ação abre uma caixa de diálogo de confirmação. Você pode anular o processo clicando em **[!UICONTROL Cancelar]** ou em **[!UICONTROL Excluir]** para confirmar a remoção.

## Realizar ações em massa

Na página de listagem de modelos de email, selecione vários modelos de cada vez marcando as caixas de seleção à esquerda. Um banner é exibido na parte inferior ao selecionar vários modelos.

![Um banner exibe o número de modelos selecionados e o ícone Excluir](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Excluir]** — É possível excluir até 20 modelos de uma vez. Uma caixa de diálogo de confirmação permite suspender a ação ou confirmar a remoção dos modelos.

## Criar um email a partir de um modelo salvo

Na tela _Criar seu email_, use a seção _Selecionar modelo de design_ para começar a criar o conteúdo a partir de um modelo.

Para começar a criar o conteúdo com um dos templates de email criados, siga estas etapas:

1. Acesse o Designer de email na página _Editar conteúdo_.

   Na página _Criar email_, a guia _Modelos de amostra_ é selecionada por padrão.

1. Para usar um modelo de email personalizado, selecione a guia **[!UICONTROL Modelos salvos]**.

   Essa guia exibe uma lista de todos os modelos de email criados na sandbox. Você pode classificá-los _Pelo nome_, _Última modificação_ e _Última criação_.

1. Selecione o template de sua escolha na lista.

   Após a seleção, é exibida uma pré-visualização do modelo. No modo de visualização, você pode navegar entre todos os modelos de uma categoria (amostra ou salva, dependendo da seleção) usando as setas para a direita e para a esquerda.

1. Clique em **[!UICONTROL Usar este modelo]** na parte superior direita.

1. No espaço de design visual, edite o conteúdo conforme necessário.
