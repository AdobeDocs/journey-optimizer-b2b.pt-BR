---
title: Páginas de destino
description: 'Criar, projetar e publicar páginas de aterrissagem para jornadas de pessoas: crie do zero, importe o HTML, adicione formulários, personalize o conteúdo e crie links de emails no Journey Optimizer B2B Prime.'
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1894dc537653c08a3e8d10cde14bd651f206d946
workflow-type: tm+mt
source-wordcount: 2164
ht-degree: 7%

---

# Páginas de destino

Uma landing page é uma página da Web independente onde você pode direcionar contatos e clientes depois que eles clicarem em um item vinculado em um email, mensagem SMS ou qualquer local digital. É possível incorporar essas páginas em suas jornadas para que seus clientes potenciais e de terceiros visualizem suas mensagens na Web e avancem com suas jornadas. Você pode criar, personalizar e visualizar páginas de aterrissagem no espaço de design visual da página de aterrissagem.

Casos de uso comuns para landing pages:

* Forneça aceitar ou recusar comunicações de marketing ou um serviço específico. Use um link em um email ou outra comunicação para uma lista direcionada.
* Colete o consentimento antes de enviar comunicações e envie um email de confirmação ao aceitar ou recusar.
* Capture ou atualize os dados de perfil (criação de perfil progressiva, preferências, registros e cenários semelhantes) usando formulários nas páginas de aterrissagem.
* Direcione pessoas para informações específicas de campanha criadas para a orquestração de jornadas.
* Redirecionar pessoas para um formulário web dedicado sem criar uma página externa fora de [!DNL Journey Optimizer B2B Prime].

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in [!DNL Journey Optimizer B2B Prime]: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test the landing page](./landing-pages-create.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->

## Acessar e gerenciar páginas de destino {#access-manage-landing-pages}

Para acessar as páginas de aterrissagem em [!DNL Journey Optimizer B2B Prime], vá para a navegação à esquerda e clique em **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Páginas de aterrissagem]**. Essa ação exibe uma lista de todas as landing pages criadas na instância.

A lista é classificada de acordo com a coluna _[!UICONTROL Modificado]_, com os itens atualizados mais recentes no topo. Clique no título da coluna para alterar entre crescente e decrescente.

### Filtrar a lista de páginas de destino {#filter-list}

Para procurar uma página de aterrissagem por nome, digite uma string de texto na barra de pesquisa para uma correspondência. Clique no ícone _Filtro_ ( ![Ícone Mostrar ou ocultar filtros](../../user/assets/do-not-localize/icon-filter.svg) ) para mostrar as opções de filtro disponíveis e alterar as configurações para filtrar os itens exibidos de acordo com seus critérios especificados.

![Filtrar as páginas de aterrissagem exibidas](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Status e ciclo de vida da página de destino {#landing-page-status}

O status da landing page determina a disponibilidade para vinculação no conteúdo de email e SMS e as alterações que você pode fazer nela.

| Status | Descrição |
| -------------------- | ----------- |
| Rascunho | Quando você cria uma página de aterrissagem, ela está no status de rascunho. Ele permanece nesse status conforme você define ou edita o conteúdo visual e até que você o publique como uma página hospedada. Ações disponíveis:<br/><ul><li>Editar nome ou descrição</li><li>Editar URL do link</li><li>Editar no espaço de design visual</li><li>Publicação</li><li>Duplicar</li><li>Excluir</li></ul> |
| Publicado | Ao publicar uma página de aterrissagem, ela fica hospedada na instância do [!DNL Journey Optimizer B2B Prime] e fica disponível para vinculação em um conteúdo de mensagem de email ou SMS. Ações disponíveis:<br/><ul><li>Editar nome ou descrição</li><li>Editar URL do link</li><li>Adicionar link no conteúdo do email ou da mensagem SMS</li><li>Criar versão de rascunho</li><li>Duplicar</li><li>Excluir</li></ul> |
| Publicado com rascunho | Ao criar um rascunho de uma página de aterrissagem publicada, a versão publicada permanece e o conteúdo do rascunho pode ser modificado no espaço de design visual. Se você publicar a versão de rascunho, ela substituirá a versão publicada atual e o conteúdo será atualizado na página hospedada. Ações disponíveis:<br/><ul><li>Editar nome ou descrição</li><li>Editar URL do link</li><li>Adicionar link no conteúdo do email ou da mensagem SMS</li><li>Editar versão de rascunho no espaço de design visual</li><li>Publicar versão de rascunho</li><li>Duplicar</li><li>Excluir (exclui ambas as versões)</li><li>Descartar rascunho (retorna ao status publicado)</li></ul> |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## Criar uma página de destino {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Definir e configurar a página de destino"
>abstract="Para criar uma página de destino, você precisa selecionar uma predefinição, configurar a página principal e as subpáginas e, por fim, testar a página antes de publicá-la."

Para direcionar membros de um público-alvo da jornada de pessoas para uma página da Web definida quando clicarem em um link específico, crie uma página de aterrissagem no [!DNL Journey Optimizer B2B Prime]. Você seleciona uma predefinição, configura a página principal e todas as subpáginas, [testa a página](#test-landing-page) e a publica.

>[!IMPORTANT]
>
>Antes de criar sua primeira landing page, conclua a configuração da landing page. Isso inclui configurar um subdomínio para hospedar suas páginas de aterrissagem e definir pelo menos uma predefinição que especifique o subdomínio e outras configurações de canal. Selecione uma predefinição ao criar a landing page. Para obter a configuração do administrador, consulte [Configuração da página de aterrissagem](../admin/configuration-presets-landing-pages.md).
>
>Para casos de uso de captura de dados, crie um [formulário](./forms.md) antes de incorporá-lo a uma página de aterrissagem.

Para criar uma landing page, siga estas etapas:

1. Vá para a navegação à esquerda e selecione **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Páginas de aterrissagem]**.

1. Na lista de páginas de aterrissagem, clique em **[!UICONTROL Criar página de aterrissagem]**.

1. Insira um **[!UICONTROL Título]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

   Critérios de título e descrição:

   * **Título** — Máximo de 100 caracteres. Deve ser exclusivo (não diferencia maiúsculas de minúsculas).
   * **Descrição** — Máximo de 300 caracteres.
   * São permitidos caracteres Alpha, numéricos e especiais.
   * Os caracteres reservados **_não são permitidos_**: `\ / : * ? " < > |`

1. Selecione uma **[!UICONTROL Predefinição]**.

   Um administrador [cria predefinições de página de aterrissagem](../admin/configuration-presets-landing-pages.md#lp-presets) para definir o subdomínio e outras configurações usadas para páginas de aterrissagem. Selecione uma predefinição e clique em **[!UICONTROL Exibir predefinição]** para revisar suas configurações e confirmar se elas correspondem aos requisitos da página de aterrissagem.

1. Clique em **[!UICONTROL Criar]**.

   A página principal e suas propriedades são exibidas. Saiba como [definir as configurações da página principal](#configure-primary-page).

1. Para adicionar uma subpágina (por exemplo, uma página de agradecimento ou de erro), clique no ícone **+**.

   É possível adicionar até duas subpáginas por página de aterrissagem.

Depois de configurar e projetar a página principal e quaisquer subpáginas, [teste sua página de aterrissagem](#test-landing-page) antes de publicá-la.

>[!CAUTION]
>
>Você não pode acessar sua landing page copiando e colando o URL definido em um navegador da Web, mesmo que a página seja publicada. Teste a página usando a função de visualização conforme descrito em [Testar a página de aterrissagem](#test-landing-page).

## Configurar a página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Definir as configurações da página principal"
>abstract="Defina a página principal, que é exibida imediatamente quando um destinatário clica no link da página de destino, como de um email ou site."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Definir o URL da página de destino"
>abstract="Nesta seção, defina um URL de página de destino exclusivo. A primeira parte do URL requer que você configure anteriormente um subdomínio da página de destino como parte da predefinição selecionada."

A página principal é a página imediatamente exibida quando um recipient clica no link da página de aterrissagem, como de um email ou site.

Para definir as configurações da página principal, siga estas etapas:

1. Altere o **[!UICONTROL Nome da página]** de acordo com suas necessidades, que é a _Página principal_ por padrão.

1. Defina a parte final do URL da página.

   A predefinição selecionada determina a primeira parte do URL. Um administrador configura o [subdomínio da página de aterrissagem](../admin/configuration-presets-landing-pages.md#lp-subdomains) como parte da predefinição.

   >[!CAUTION]
   >
   >O URL da landing page deve ser exclusivo.
   >
   >Você não pode acessar sua landing page copiando e colando esse URL em um navegador da Web, mesmo que a página seja publicada. Teste-o usando a função de visualização, conforme descrito em [Testar a página de aterrissagem](#test-landing-page).

1. Se quiser uma página de aterrissagem anônima, desabilite a opção **[!UICONTROL Requer usuários identificados]**.

1. Clique no ícone _Calendário_ para definir a **[!UICONTROL Expiração da página]**.

   Após selecionar uma data de expiração, escolha a ação após a expiração da página:

   * **[!UICONTROL URL de redirecionamento]** - Digite a URL da página para usar como redirecionamento.
   * **[!UICONTROL Erro do navegador]** - Digite o texto do erro a ser exibido no lugar da página.

## Testar a página de destino {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Visualizar e testar a página de destino"
>abstract="Após definir as configurações e o conteúdo da página de destino, use perfis de teste para visualizar a página."

Quando as configurações e o conteúdo da landing page são definidos, você pode usar perfis de teste para visualizar a página. Se você inseriu [conteúdo personalizado](email-authoring.md#personalize-content), é possível verificar como esse conteúdo é exibido na página de aterrissagem usando os dados do perfil de teste.

>[!PREREQUISITES]
>
>Para visualizar e testar páginas de aterrissagem, você deve ter a permissão **[!UICONTROL Publicar mensagens]** e um conjunto de dados definido que contenha perfis de teste.

1. Clique em **[!UICONTROL Visualizar e testar]** para abrir a seleção de perfil de teste.

   >[!NOTE]
   >
   >Você também pode usar **[!UICONTROL Simular conteúdo]** quando estiver no espaço de design visual.

1. Na tela _[!UICONTROL Simular]_, selecione um perfil de teste.

   Se os perfis necessários não estiverem listados, clique em **[!UICONTROL Gerenciar perfis de teste]** para usar um endereço de email de perfil de teste conhecido e adicioná-lo à lista.

   +++Adicionar perfis de teste

   Para o **[!UICONTROL Namespace de identidade]**, clique no ícone _Selecionar_ ( ![Selecionar ícone](../../user/assets/do-not-localize/icon-select-data.svg) ) e escolha o namespace `Email` a ser usado para testar perfis.

   No campo **[!UICONTROL Valor de identidade]**, insira o endereço de email para identificar o perfil de teste e clique em **[!UICONTROL Adicionar perfil]**. Você pode repetir isso para adicionar vários perfis.

   Clique na seta para trás na parte superior esquerda para retornar à página _[!UICONTROL Simular]_.

   +++

1. Selecione **[!UICONTROL Abrir visualização]** para testar a página de aterrissagem.

   A pré-visualização da landing page é aberta em uma nova guia. Os dados do perfil de teste selecionado substituem os elementos personalizados.

1. Selecione outros perfis de teste para visualizar a renderização de cada variante da página de aterrissagem.

## Editar uma landing page {#edit-landing-page}

As edições em uma landing page dependem do status atual:

* Quando a página de aterrissagem está com o status **_Rascunho_**, você pode editar os detalhes, a URL e o conteúdo visual dela.
* Quando a página de aterrissagem está no status **_Publicado_**, você pode editar a descrição, mas não o nome. Para alterar o conteúdo visual, você deve criar uma versão de rascunho da página.
* Quando a página de aterrissagem está no status **_Publicado com rascunho_**, a edição de detalhes fica limitada à descrição. Também é possível editar o conteúdo visual da versão de rascunho.

>[!BEGINTABS]

>[!TAB Rascunho]

1. Na página de listagem _[!UICONTROL Landing pages]_, clique no nome da landing page para abri-la.

   Uma visualização do conteúdo visual é exibida, com os detalhes da landing page à direita.

1. Modifique quaisquer detalhes, como nome e descrição.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. Para fazer alterações no conteúdo do espaço de design visual, clique em **[!UICONTROL Editar página de aterrissagem]**.

1. Clique em **[!UICONTROL Salvar]** ou **[!UICONTROL Salvar e fechar]** para retornar aos detalhes da página de aterrissagem.

1. Quando a página atender aos seus critérios e você desejar disponibilizá-la para exibição, clique em **[!UICONTROL Publicar]**.

>[!TAB Publicado]

1. Na página de listagem _[!UICONTROL Landing pages]_, clique no nome da página para abri-la.

   Uma visualização do conteúdo visual é exibida, com os detalhes da landing page à direita.

1. Modifique a descrição, se necessário.

   Para uma landing page publicada, todos os outros detalhes não podem ser alterados.

1. Para atualizar o conteúdo, clique em **[!UICONTROL Editar página de aterrissagem]** à direita.

   Clique em **[!UICONTROL Criar versão de rascunho]** na caixa de diálogo para abrir a versão de rascunho no espaço de design visual.

1. Clique em **[!UICONTROL Salvar]** ou **[!UICONTROL Salvar e fechar]** para retornar aos detalhes da página de aterrissagem.

1. Quando a landing page de rascunho atender aos seus critérios e você quiser disponibilizar as alterações na página publicada, clique em **[!UICONTROL Publicar]**.

   Ao publicar a versão de rascunho, ela substitui a versão publicada atual e o conteúdo é atualizado para o URL da página.

>[!TAB Publicado com rascunho]

Ao abrir a landing page, a versão de rascunho é exibida. As guias na parte superior do espaço de visualização permitem alternar a exibição entre as versões publicada e de rascunho. Os rascunhos de ações e detalhes são exibidos à direita.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

Para atualizar o conteúdo:

1. Clique em **[!UICONTROL Editar página de aterrissagem]** na parte superior direita.

1. Clique em **[!UICONTROL Salvar]** ou **[!UICONTROL Salvar e fechar]** para retornar aos detalhes da página de aterrissagem.

1. Quando a página de rascunho atender aos seus critérios e você desejar disponibilizar as alterações, clique em **[!UICONTROL Publicar]**.

   Ao publicar a versão de rascunho, ela substitui a versão publicada atual e o conteúdo é atualizado na página hospedada.

>[!ENDTABS]

## Duplicação de uma landing page {#duplicate-landing-page}

É possível duplicar uma landing page usando um dos seguintes métodos:

* Na página de listagem _[!UICONTROL Landing page]_, clique no ícone _Mais_ (**...**) ao lado do nome da página de aterrissagem, escolha **[!UICONTROL Duplicar]**.
* Na parte superior direita da página de detalhes, clique em **[!UICONTROL ... Mais]** e escolha **[!UICONTROL Duplicar]**.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

Na caixa de diálogo, digite um nome útil (exclusivo) e uma descrição (opcional). Clique em **[!UICONTROL Duplicar]** para concluir a ação.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

A página duplicada (nova) aparece na listagem _Landing pages_.

## Excluir uma página de destino {#delete-landing-page}

É possível excluir uma landing page usando um dos seguintes métodos:

* Na página de listagem _[!UICONTROL Landing page]_, clique no ícone _Mais_ (**...**) ao lado do nome da página de aterrissagem, escolha **[!UICONTROL Excluir]**.
* Na parte superior direita da página de detalhes, clique em **[!UICONTROL ... Mais]** e escolha **[!UICONTROL Excluir]**.

Essa ação abre uma caixa de diálogo de confirmação. Você pode anular o processo clicando em **[!UICONTROL Cancelar]** ou em **[!UICONTROL Excluir]** para confirmar a exclusão.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## Link para uma landing page {#link-to-landing-page}

Como profissional de marketing ou criador que produz conteúdo de email, fragmento e página, você pode incorporar links às páginas de aterrissagem publicadas (online) que são criadas na instância do [!DNL Journey Optimizer B2B Prime].

1. Conforme você trabalha no espaço de design visual de um fragmento, email, página de aterrissagem ou modelo, selecione um trecho de texto, um componente de botão ou um componente de imagem para o link.

   As opções **[!UICONTROL Link]** são exibidas no painel direito.

1. Para a opção **[!UICONTROL Tipo]**, escolha **[!UICONTROL Página de aterrissagem]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. Na opção **[!UICONTROL Página de aterrissagem]**, clique no ícone _Selecionar página_ ( ![Ícone Mostrar links](../../user/assets/do-not-localize/icon-landing-page-select.svg) ).

1. Na caixa de diálogo Selecionar página de aterrissagem, defina a **[!UICONTROL Origem da página de aterrissagem]** como **[!UICONTROL Journey Optimizer B2B edition]**, marque a caixa de seleção da página de aterrissagem na lista de páginas publicadas e clique em **[!UICONTROL Selecionar]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. Para a opção **[!UICONTROL Target]**, escolha o comportamento de destino do link:

   * **[!UICONTROL Nenhum]** - Abre o link usando o comportamento padrão do navegador.
   * **[!UICONTROL Em branco]** - Abre o link em uma nova janela ou guia.
   * **[!UICONTROL Self]** - Abre o link no mesmo quadro.
   * **[!UICONTROL Pai]** - abre o link no quadro pai.
   * **[!UICONTROL Superior]** - Abre o link no corpo inteiro da janela.

1. (Somente link de texto) Se quiser sublinhar o texto vinculado, marque a caixa de seleção **[!UICONTROL Sublinhar link]**.

   É possível definir um estilo adicional para o texto do link, incluindo a cor do link, selecionando a guia **[!UICONTROL Estilos]** no painel direito.
