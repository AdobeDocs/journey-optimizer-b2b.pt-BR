---
title: Listas de contas
description: Saiba mais sobre listas de contas e como os profissionais de marketing podem usá-las para direcionar contas por meio de jornadas de conta.
feature: Account Lists
role: User
exl-id: 7d7f5612-f0fe-4bb8-ae16-29aa3552f0f9
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 1%

---

# Listas de contas

No Journey Optimizer B2B edition, uma lista de contas é uma coleção de contas nomeadas que os profissionais de marketing podem usar para a orquestração de jornadas direcionada. Uma lista de contas pode direcionar contas nomeadas de acordo com seus critérios definidos, como setor, local ou tamanho da empresa. Há dois tipos de listas de contas:

* **Estático** - Com uma lista de contas estáticas, a lista só é alterada quando você adiciona as contas. Você pode adicionar contas manualmente aplicando um conjunto de filtros para preencher a lista com base nos dados atuais da conta, ou adicionar e remover contas por meio de uma jornada de conta.
* **Dinâmico** - Com uma lista de contas dinâmica, você define um conjunto de filtros para preparar automaticamente a lista. O sistema usa esse conjunto de filtros para adicionar e remover contas de acordo com as alterações nas informações da conta. Este gerenciamento de lista é semelhante à [segmentação de público na Real-time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/segmentation/b2b){target="_blank"}.

Quando uma lista de contas está em um estado _Live_ (publicada), ela está disponível para [uso em programas de jornada e Marketo Engage](./account-lists-journeys.md).

>[!NOTE]
>
>As listas de contas usam os dados de conta do Marketo Engage para criar segmentos e listas de contas. Isso significa que se um segmento de conta do Adobe Experience Platform não for sincronizado ativamente com o Marketo Engage, as contas nesse segmento do Experience Platform podem não estar disponíveis nas listas de contas do Journey Optimizer B2B edition. Posteriormente, as pessoas das contas nos segmentos da Experience Platform que não estão sincronizadas com o Marketo Engage não podem ser incluídas nas contagens de associação de pessoas ou contadas em eventos de acionador.

## Acessar e procurar listas de contas

Na navegação à esquerda, expanda **[!UICONTROL Contas]** e clique em **[!UICONTROL Listas de contas]**.

![Acessar jornadas de conta](./assets/account-lists-browse.png){width="800" zoomable="yes"}

A página exibida _[!UICONTROL Listas de contas]_ inclui as seguintes colunas:

* [!UICONTROL Nome] (clique no nome da lista de contas para ver os detalhes)
* [!UICONTROL Status]
* [!UICONTROL Tipo]
* [!UICONTROL Última atualização em]
* [!UICONTROL Última atualização por]
* [!UICONTROL Data de criação]
* [!UICONTROL Criado por]

Esta tabela inclui a capacidade de pesquisar por Nome. A função de classificação não está disponível no momento.

Você pode personalizar a tabela exibida ao clicar no ícone _Configurações de coluna_ ( ![Configurações de coluna](../assets/do-not-localize/icon-column-settings.svg) ) no canto superior direito e marcar ou desmarcar as caixas de seleção.

![Escolha as colunas a serem exibidas na lista de jornadas de conta](./assets/account-lists-list-columns.png){width="300"}

Para exibir a descrição de uma lista de contas, clique no ícone _Informações_ ( ![Informações](../assets/do-not-localize/icon-info.svg) ) ao lado do nome.

## Criar uma lista de contas

Ao criar uma lista de contas, você define um conjunto de filtros para gerar a lista. Por exemplo, você pode usá-lo para gerar uma lista de contas em que o setor se situe na área de saúde e a receita seja superior a US$ 100 milhões.

1. Na página _[!UICONTROL Listas de contas]_, clique em **[!UICONTROL Criar lista de contas]** no canto superior direito da página.

   ![Clique em Criar lista de contas](./assets/account-lists-create.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Criar lista de contas]_, digite um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

1. Escolha o _[!UICONTROL Tipo]_ para a lista de contas, **[!UICONTROL Estático]** ou **[!UICONTROL Dinâmico]**.

   ![Escolher Estático ou Dinâmico para a lista de contas](./assets/account-list-create-dialog.png){width="380"}

1. Clique em **[!UICONTROL Criar]**.

   Uma nova lista estática de contas é aberta com uma lista vazia de contas. Uma nova lista de contas dinâmicas é aberta com o painel _[!UICONTROL Adicionar contas por filtro]_ na página.

## Adicionar contas à lista de contas

Para uma lista estática, você pode continuar a publicar a lista de contas vazia e adicionar contas por meio de uma jornada de conta. Você também pode adicionar contas manualmente aplicando um conjunto de filtros antes de publicá-lo.

Para uma lista de contas dinâmicas, é necessário adicionar o conjunto de filtros que você deseja usar para gerenciar a lista automaticamente antes de publicá-la.

>[!BEGINTABS]

>[!TAB Lista de contas estáticas]

Depois de criar a lista de contas estáticas, você pode preencher a lista aplicando um conjunto de filtros. Você também pode aplicar um conjunto de filtros para adicionar contas a uma lista de contas estáticas após sua publicação (_Live_).

>[!NOTE]
>
>Se quiser que a lista de contas comece como vazia, não selecione nenhum filtro e basta publicar a lista de contas. É útil começar com uma lista vazia quando você planeja adicionar membros por meio de uma ação de jornada de conta (consulte [Executar um nó de ação - Adicionar à conta](#take-an-action-node---add-to-account)).

1. Clique em **[!UICONTROL Adicionar contas]**.

   ![Adicionar um filtro de conta para popular a lista ](./assets/account-lists-static-new-add-accounts.png){width="700" zoomable="yes"}

   Você pode acessar essa função na página de lista vazia ou na parte superior direita.

1. Na caixa de diálogo _[!UICONTROL Adicionar contas por filtro]_, use o menu **[!UICONTROL Filtros de Conta]** para adicionar os atributos e atividades que deseja usar para criar o conjunto de filtros:

   Os filtros são aninhados em pastas de categoria. É possível expandir cada pasta e percorrer as listas de filtros disponíveis. Ou use a ferramenta _Pesquisa_ na parte superior para localizar o filtro necessário.

   * Arraste e solte o filtro do menu esquerdo para o espaço de definição de filtro.
   * Conclua a definição de avaliação de correspondência.
   * Repita essas ações para cada filtro que deseja incluir.

     ![Adicionar filtros para popular a lista de contas ](./assets/account-lists-static-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * Você pode ajustar suas condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você pode optar por corresponder todas as condições de atributo ou qualquer condição.

     ![Lógica de filtro de lista de contas](./assets/account-lists-filter-logic.png){width="450"}

1. Quando o conjunto de filtros e a lógica estiverem concluídos, clique em **[!UICONTROL Preencher contas]**.

   O processo de preenchimento pode levar algum tempo, dependendo do número de contas a serem avaliadas e preenchidas (o tamanho do banco de dados e os critérios de filtro selecionados). Pode levar até duas horas para que as contas sejam preenchidas na lista.

Você pode continuar a publicar a lista para disponibilizá-la para adicionar e remover ações em uma jornada de conta.

>[!TAB Lista de contas dinâmicas]

Depois de criar uma lista de contas dinâmicas, defina o conjunto de filtros usado para gerenciar a lista (adicionar/remover contas) quando ela estiver _Ativa_ (publicada). Não é possível adicionar/remover contas por meio de jornadas de conta, mas uma lista de contas dinâmicas publicada está disponível para o nó de público-alvo da conta inicial.

1. Clique em **[!UICONTROL Selecionar filtros]**.

   ![Selecione os filtros usados para popular a lista dinamicamente ](./assets/account-lists-dynamic-new-select-filters.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Adicionar contas por filtro]_, use o menu **[!UICONTROL Filtros de Conta]** para adicionar os atributos e filtros especiais que deseja usar para criar o conjunto de filtros:

   Os filtros são aninhados em pastas de categoria. É possível expandir cada pasta e percorrer as listas de filtros disponíveis. Ou use a ferramenta _Pesquisa_ na parte superior para localizar o filtro necessário.

   * Arraste e solte o filtro do menu esquerdo para o espaço de definição de filtro.
   * Conclua a definição de avaliação de correspondência.
   * Repita essas ações para cada filtro que deseja incluir.

     ![Adicionar filtros para popular a lista de contas ](./assets/account-lists-dynamic-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * Você pode ajustar suas condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você pode optar por corresponder todas as condições de atributo ou qualquer condição.

     ![Lógica de filtro de lista de contas](./assets/account-lists-filter-logic.png){width="450"}

1. Quando o conjunto de filtros e a lógica estiverem concluídos, clique em **[!UICONTROL Concluído]**.

   Se você estiver satisfeito com o conjunto de filtros, poderá prosseguir para [publicar a lista](#publish-an-account-list) para torná-la disponível para o [nó de público-alvo da conta](#account-audience-node) inicial em uma jornada de conta.

   >[!NOTE]
   >
   >Não é possível atualizar os filtros de uma lista de contas dinâmicas depois que a lista é publicada.

   O processo de preenchimento pode levar algum tempo, dependendo do número de contas a serem avaliadas e preenchidas (o tamanho do banco de dados e os critérios de filtro selecionados). Pode levar até duas horas para que as contas sejam preenchidas na lista.

>[!ENDTABS]

## Publicar uma lista de contas

Você pode continuar a publicar uma lista de contas assim que o conjunto de filtros estiver concluído.

>[!BEGINTABS]

>[!TAB Lista de contas estáticas]

1. Clique em **[!UICONTROL Publicar]** na parte superior direita.

   ![Clique em Publicar na parte superior direita](./assets/account-lists-static-publish.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Publicar lista de contas estáticas]_, clique em **[!UICONTROL Publicar]** para confirmar.

   ![Confirmar publicação para uma lista de contas estáticas](./assets/account-lists-static-publish-confirm.png){width="400"}

O status da lista de contas estáticas é alterado para _[!UICONTROL Live]_ e está disponível para [uso em uma jornada de conta](#account-list-usage-in-account-journeys).

>[!TAB Lista de contas dinâmicas]

Você pode continuar a publicar uma lista de contas dinâmicas assim que o conjunto de filtros estiver concluído. Depois que a lista de contas está com o status Ativo, ela fica disponível para seleção em um nó de jornada de público-alvo de conta.

1. Clique em **[!UICONTROL Publicar]** na parte superior direita.

   ![Clique em Publicar na parte superior direita](./assets/account-lists-dynamic-publish.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Publicar lista de contas dinâmicas]_, clique em **[!UICONTROL Publicar]** para confirmar.

   ![Confirmar publicação para uma lista de contas dinâmicas](./assets/account-lists-dynamic-publish-confirm.png){width="400"}

O status da lista de contas dinâmicas é alterado para _[!UICONTROL Live]_ e está disponível para [uso em uma jornada de conta](#account-list-usage-in-account-journeys).

>[!ENDTABS]
