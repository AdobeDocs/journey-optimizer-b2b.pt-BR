---
title: Interesses da solução
description: Saiba mais sobre os interesses da solução e como você pode defini-los para uso nos Grupos de compra.
feature: Buying Groups, Account Journeys
exl-id: b7dfddac-ed29-4870-b853-5e520a4cdf12
source-git-commit: c84b3e0b05581a630993077688b1dd3a3a95fcc5
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Interesses da solução

Antes de criar Grupos de Compra, você deve saber o que está vendendo e quem deseja direcionar. Sua estratégia de marketing e vendas deve estar alinhada para que você possa adicionar o interesse da solução para os grupos de compra.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Acessar e procurar interesses da solução

1. Na página inicial do Adobe Experience Platform, clique em Adobe Journey Optimizer B2B edition.

1. Na navegação à esquerda, clique em **[!UICONTROL Comprando grupos]**.

1. Na página Grupos de compra, selecione a guia **[!UICONTROL Solution interest]**.

   ![Guia Interesse da solução](assets/solution-interest-tab.png){width="700" zoomable="yes"}

   A guia fornece uma lista de inventário de todos os interesses existentes da solução. Ele fornece informações como _[!UICONTROL Nome]_, _[!UICONTROL Modelo de funções]_, _[!UICONTROL Trabalhos de criação de grupos de compras]_, _[!UICONTROL Última atualização em]_, _[!UICONTROL Atualizado por]_, _[!UICONTROL Criado em]_ e _[!UICONTROL Criado por]_ no formato de coluna.

   A lista é classificada por padrão pela _[!UICONTROL Última atualização em]_. Clique no título da coluna no cabeçalho para alternar a classificação entre decrescente e crescente.

## Exibir e excluir trabalhos de grupo de compras

Na guia _[!UICONTROL Interesse na solução]_, a coluna **[!UICONTROL Trabalhos de criação de grupo de compra]** exibe a contagem de trabalhos criados para cada interesse na solução. O número é um link e, ao clicar nele, uma caixa de diálogo é aberta, exibindo a lista de trabalhos criados para o interesse da solução.

![Comprando trabalhos do grupo para interesse na solução](assets/buying-group-jobs-for-solution-interest.png){width="700" zoomable="yes"}

Você pode excluir um trabalho do grupo de compra clicando nas reticências (...) ao lado do nome do trabalho e escolhendo **[!UICONTROL Excluir]**.

## Criar um interesse de solução

Antes de criar um interesse de solução, você deve ter um modelo de funções online (publicado) que defina as funções que deseja direcionar. Consulte [Modelos de função de grupo de compra](./buying-groups-role-templates.md) para obter mais informações sobre como criar um modelo de funções e publicar um modelo de funções.

1. Na guia _[!UICONTROL Interesse na solução]_, clique em **[!UICONTROL Criar interesse na solução]** no canto superior direito.

1. Insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

1. Escolha um **[!UICONTROL Modelo de Funções]** (obrigatório).

   Clique em **[!UICONTROL Selecionar modelo de funções]** e escolha um modelo de funções online na lista da caixa de diálogo. Você pode associar apenas um modelo de funções online a um interesse de solução. Clique em **[!UICONTROL Salvar]** para retornar à página _[!UICONTROL Criar interesse da solução]_, onde o modelo de funções selecionado é exibido.

   ![Adicionar um modelo de funções ao interesse de solução](assets/solution-interest-create.png){width="700" zoomable="yes"}

1. Selecione o **[!UICONTROL Modelo de estágio de grupo de compras]** para usar a progressão de estágio de grupo de compras (opcional).

   Para obter mais informações sobre como usar estágios de grupo de compras para rastrear a progressão da conta, consulte [Estágios de grupo de compras](./buying-group-stages.md).

1. Habilitar a configuração **[!UICONTROL Atualizar grupos de compra existentes]** (opcional).

   Quando essa opção está habilitada, todos os grupos de compras existentes combinados com os interesses da solução são atualizados por meio do ciclo de sincronização de 24 horas.

1. Clique em **[!UICONTROL Criar]** no canto superior direito.

   O novo interesse da solução é exibido na lista _[!UICONTROL Interesses da Solução]_.

## Editar um interesse de solução

A qualquer momento, você pode alterar o nome e a descrição de um interesse de solução. O modelo de funções não pode ser alterado devido à dependência de grupos de compra com base no interesse da solução e no emparelhamento do modelo de função. Nesse caso, você deve criar um novo interesse de solução usando outro template de funções.

1. Na guia _[!UICONTROL Interesse da solução]_, use um dos métodos a seguir para abrir as propriedades do interesse da solução que deseja editar:

   * Clique no nome de interesse da solução.
   * Clique nas reticências (**...**) ao lado dele e escolha **[!UICONTROL Editar]**.

   ![Menu Mais interesses da solução](assets/solution-interests-more-menu.png){width="500" zoomable="no"}

1. Se necessário, atualize o nome (obrigatório e exclusivo) e a descrição (opcional).

1. Se necessário, selecione o **[!UICONTROL Modelo de estágio de grupo de compras]** para rastrear a progressão do estágio de grupo de compras.

   Para obter mais informações sobre como usar estágios de grupo de compras para rastrear a progressão da jornada em relação às vendas, consulte [Estágios de grupo de compras](./buying-group-stages.md).

1. Se necessário, altere a configuração **[!UICONTROL Atualizar grupos de compra existentes]**.

   Quando essa opção estiver habilitada, todos os grupos de compras existentes emparelhados com os interesses da solução serão atualizados por meio do ciclo de sincronização de 7 dias.

1. Clique em **[!UICONTROL Salvar]**.

## Excluir um interesse de solução

Qualquer interesse de solução que esteja atualmente em uso por qualquer trabalho de grupo de compra ou jornada de conta não pode ser excluído. Além disso, um interesse de solução excluído não pode ser recuperado.

1. Na guia _[!UICONTROL Interesse da solução]_, clique nas reticências (**...**) ao lado do interesse da solução e escolha **[!UICONTROL Excluir]**.

   Essa ação abre uma caixa de diálogo de confirmação.

   Se o interesse da solução estiver sendo usado no momento por uma jornada de conta ou um trabalho de grupo de compras, a ação abrirá uma caixa de diálogo informativa para alertá-lo de que não pode ser excluído. Clique em [!UICONTROL OK], que interrompe a exclusão.

1. Clique em **[!UICONTROL Excluir]** para confirmar a exclusão, ou você pode anular o processo clicando em _[!UICONTROL Cancelar]_.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3433080/?learn=on)
