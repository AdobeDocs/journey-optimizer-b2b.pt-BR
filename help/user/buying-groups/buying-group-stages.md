---
title: Estágios de Grupo de Compras
description: Saiba mais sobre estágios de grupo de compras e como defini-los para rastrear a progressão da jornada em relação às metas de vendas.
feature: Buying Groups, Account Journeys
exl-id: 3067e51d-4cbe-47da-aed1-ec58496ca6d0
source-git-commit: 3336a09a58d4c68418ffa1563b6c4c65097e1a49
workflow-type: tm+mt
source-wordcount: '2250'
ht-degree: 0%

---

# Estágios do grupo de compra

Os estágios de grupo de compra são projetados para rastrear a progressão dos grupos de compra na conversão de oportunidades em clientes. Use este recurso para rastrear a progressão do grupo de compras e identificar as próximas melhores ações para membros do grupo de compras.

Defina os estágios em um único modelo de preparo, definindo vários estágios e o fluxo de transição entre eles. Um ou mais estágios são designados para entrada no ciclo de vida. O modelo também permite a progressão não linear, onde você pode especificar transições de um estágio para outro, como do estágio A para os estágios B, C ou D. É necessário que um estágio seja designado como o estágio de sucesso, como uma compra ou contrato assinado. É opcional que outro estágio seja designado como um estágio de falha, como um contrato rejeitado ou a compra de uma solução concorrente de outro fornecedor. Isso é feito por meio de [painéis inteligentes](../dashboards/intelligent-dashboard.md) que mostram como os grupos de compras estão progredindo em termos de conclusão de uma oportunidade de venda ou de conversão de uma oportunidade em um cliente.

![Exemplo de estágios de grupo de compras](assets/buying-group-stages-lifecycle-diagram.png){width="800" zoomable="yes"}

## Definir seu modelo de estágios de grupo de compras

Você cria e configura um modelo de estágios de grupo de compras por:

* Adição dos estágios do ciclo de vida
* Definição dos fluxos de transição
* Designando os estágios de entrada e destino

Há suporte para apenas um modelo, portanto, é importante trabalhar com as equipes de Marketing e Vendas para planejar o modelo ideal para a sua organização antes de criá-lo e publicá-lo no Journey Optimizer B2B edition.<!-- Initially, only one stage model can be created, but future releases will support multiple stage models, allowing users to select which model to use in a journey. -->

Ao criar o modelo de estágio de grupo de compra, ele estará automaticamente no status _Rascunho_ e não poderá ser excluído nem renomeado. Ele permanece nesse status à medida que você define os estágios e configura o fluxo de transição entre os estágios. Quando o modelo está em um status publicado (_Live_), ele não pode ser alterado.

### Criar o modelo

1. Na navegação à esquerda, vá para **[!UICONTROL Contas]** > **[!UICONTROL Grupos de Compras]**.

1. Na página Grupos de compra, selecione a guia **[!UICONTROL Estágios]**.

   ![Guia Estágios](assets/stages-tab-none.png){width="800" zoomable="yes"}

   Esta guia _[!UICONTROL Estágios]_ estará em um estado _vazio_ até que você crie o modelo.

1. Clique em **[!UICONTROL Criar modelo]** no centro da página.

1. Na caixa de diálogo, insira o **[!UICONTROL Nome]** (obrigatório) e a **[!UICONTROL Descrição]** (opcional) do modelo.

   ![Adicionar o nome e a descrição do modelo](assets/stages-create-model-dialog.png){width="700" zoomable="yes"}

   Se você clicar em _[!UICONTROL Cancelar]_ nesta caixa de diálogo, retornará à guia _[!UICONTROL Estágios]_ em um estado _vazio_.

1. Clique em **[!UICONTROL Criar]**.

### Definir os estágios

Depois de criar o modelo, ele é aberto no espaço de trabalho e você é solicitado a criar os estágios do modelo.

1. Clique em **[!UICONTROL Editar estágios]**.

   ![Adicionar estágios ao modelo vazio](assets/stages-model-empty.png){width="700" zoomable="yes"}

1. Defina o primeiro estágio inserindo o **[!UICONTROL Nome]** (obrigatório) e a **[!UICONTROL Descrição]** (opcional).

   ![Adicionar o nome e a descrição para o primeiro estágio](assets/stages-model-stage-1.png){width="700" zoomable="yes"}

   Os estágios não precisam ser adicionados em uma ordem específica, mas isso determina como os estágios são listados na página de detalhes do modelo. Você designa o estágio de entrada e o fluxo entre estágios ao definir as regras de transição.

1. Clique em **[!UICONTROL Adicionar estágio]** e repita a etapa 2 para definir outro estágio.

   Repita essa etapa até ter as etapas necessárias para o modelo.

   ![Estágios definidos para o modelo](assets/stages-model-stages-added.png){width="700" zoomable="yes"}

1. Quando estiver satisfeito com os estágios definidos, clique em **[!UICONTROL Salvar]**.

   >[!IMPORTANT]
   >
   >**Depois que os estágios do grupo de compra forem salvos, eles não poderão ser removidos.** No entanto, você pode alterar o nome e a descrição de qualquer um dos estágios, desde que o modelo permaneça no status _Rascunho_.

### Configurar o fluxo de trabalho e as regras de transição

Depois de salvar os estágios, ele retorna ao espaço de trabalho de modelo. A coluna _[!UICONTROL Trânsito permitido para]_ está vazia, o que indica que as regras de transição para os estágios de modelo ainda não estão definidas.

![As regras de transição ainda não estão definidas](assets/stages-model-stages-empty-rules.png){width="700" zoomable="yes"}

As regras de transição determinam como um grupo de compras pode se mover de um estágio para outro. Por exemplo, ela pode se mover de um estágio de entrada para um estágio intermediário e de um estágio intermediário para vários outros estágios. Um estágio de entrada é um estágio inicial no qual um grupo de compras pode entrar a partir de um estado em branco, e os estágios de destino são classificados como estágios de sucesso ou falha.

1. Clique em **[!UICONTROL Editar regras de transição]** na parte superior direita.

   Esta ação abre a caixa de diálogo _[!UICONTROL Editar regras de estágio]_, na qual você define a lógica do fluxo.

   À medida que você define as opções, há algumas medidas de proteção e mensagens integradas para ajudar você a evitar erros lógicos no fluxo. Você pode clicar em _[!UICONTROL Cancelar]_ para fechar a caixa de diálogo e retornar à página de guia _[!UICONTROL Estágios]_ sem alterações.

1. Na seção _[!UICONTROL Selecionar estágio]_, designe estágios inicial e final para o fluxo:

   * **[!UICONTROL Estágio do ponto de entrada]** (obrigatório) - Designe um ou mais estágios de entrada para a oportunidade de grupo de compras.

   * **[!UICONTROL Estágio de sucesso]** (obrigatório) - Designe o estágio que indica que a oportunidade de grupo de compras foi bem-sucedida (destino).

   * **[!UICONTROL Estágio de falha]** (opcional) - Designe um ou mais estágios que indiquem que a oportunidade de grupo de compra atingiu um ponto de falha (destino).

   ![Configurar os estágios de ponto de entrada e um estágio de falha opcional](./assets/stages-model-edit-stage-rules.png){width="700" zoomable="yes"}

1. Para cada estágio que não seja de destino, defina um ou mais estágios que se seguem no fluxo (transição).

   Todos os estágios que não são de destino devem ter pelo menos um estágio **[!UICONTROL Trânsito permitido]** selecionado. Caso contrário, a lógica do modelo não é válida e as contas podem ficar _travadas_ nesse estágio sem nenhuma maneira de progredir para o sucesso ou falha.

   ![Configurar transições entre estágios que não sejam de destino](./assets/stages-model-edit-stage-rules-transitons.png){width="700" zoomable="yes"}

   Opcionalmente, é possível especificar uma transição de um estágio de falha. Por exemplo, você pode designar um estágio chamado _Sem resposta_ como um estágio de falha. Mas também designe um estágio chamado _Resurgence_ como uma possível transição para identificar casos em que uma conta inativa é reativada.

1. Clique em **[!UICONTROL Salvar]**.

   Com o retorno à página de detalhes do modelo, os estágios são listados em uma tabela com as transições permitidas e as propriedades de entrada e de destino.

| Coluna | Descrição |
| ------ | ---------- |
| **[!UICONTROL Nome do estágio]** | Nome do estágio. Clique no ícone de informações para exibir a descrição do estágio. |
| **[!UICONTROL Trânsito permitido para]** | Lista os estágios válidos para uma ação _mover para_ dentro do modelo. |
| **[!UICONTROL Estágio do ponto de entrada]** | Indica se o estágio é válido como um estágio de ponto de entrada ([!UICONTROL Sim] ou [!UICONTROL Não]). |
| **[!UICONTROL Destino]** | Indica se o estágio é designado como um estágio de destino ([!UICONTROL Sucesso] ou [!UICONTROL Falha]). |

![Estágios e regras de transição definidos para um modelo de rascunho](assets/stages-model-draft-details.png){width="700" zoomable="yes"}

## Editar um modelo de rascunho

Desde que o modelo de estágios do grupo de compra permaneça em um estado de _Rascunho_, você pode editar os estágios e as regras de transição.

Para exibir o modelo preliminar:

1. Na navegação à esquerda, vá para **[!UICONTROL Contas]** > **[!UICONTROL Grupos de Compras]**.

1. Na página _Grupos de Compra_, selecione a guia **[!UICONTROL Estágios]**.

1. Clique no nome do modelo para abrir os detalhes dele.

### Alterar os estágios no modelo

1. Clique em **[!UICONTROL Editar estágios]**.

   Na caixa de diálogo _[!UICONTROL Editar estágios]_, você pode adicionar novos estágios ou alterar o nome e a descrição dos estágios existentes.

   * Altere o **[!UICONTROL Nome]** ou a **[!UICONTROL Descrição]** de qualquer estágio, conforme necessário.

   * Role para baixo e clique em **[!UICONTROL Adicionar estágio]** para definir um novo estágio para o modelo, se necessário.

1. Quando estiver satisfeito com os estágios definidos, clique em **[!UICONTROL Salvar]**.

   Você também pode clicar em _[!UICONTROL Cancelar]_ para fechar a caixa de diálogo e retornar à página de detalhes do modelo sem alterações.

### Editar as regras de transição do modelo

1. Clique em **[!UICONTROL Editar regras de transição]**.

1. Na caixa de diálogo _Editar regras de estágio_, altere as opções de fluxo conforme necessário.

   Consulte [Configurar as regras de fluxo de trabalho e transição](#configure-the-workflow-and-transition-rules) para obter mais informações sobre essas opções e como elas afetam o fluxo do modelo.

1. Quando estiver satisfeito com as regras de transição definidas, clique em **[!UICONTROL Salvar]**.

   Você também pode clicar em _[!UICONTROL Cancelar]_ para fechar a caixa de diálogo e retornar à página de detalhes do modelo sem alterações.

## Publish o modelo de estágios de grupo de compras

Se não houver erros de validação, o modelo poderá ser publicado. Quando publicado, ele muda para um estado _Live_ e pode ser usado para continuar comprando estágios de grupo nas jornadas da conta.

>[!IMPORTANT]
>
>**Depois que o modelo é publicado, ele não pode ser atualizado ou excluído.** Verifique se o que você tem está correto antes de publicar o modelo.

1. Revise os estágios e as transições definidos com cuidado.

   Se forem necessárias revisões, edite os estágios de modelo.

1. Clique em **[!UICONTROL Publish]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Publish]**.

   Com o retorno à página de detalhes do modelo, o modelo é designado como _[!UICONTROL Live]_. Clique na seta _Voltar_ na parte superior esquerda para retornar à página de guia _[!UICONTROL Estágios]_.

![O modelo publicado](assets/stages-tab-model-live.png){width="700" zoomable="yes"}
<!-- list these later when the Published columns are working correctly

Columns - Name, Status, Created by, Created date, Last updated by, Last update, Published by, Published on.
Name - Name of the stage model, hyperlinked. Clicking on it will navigate to the stage inventory page. 
Info icon beside the name - display the description on click.
Status - Live, Draft. If a draft stage model is Published, then its status is updated to Live. -->

## Usar o modelo nas jornadas da conta

Quando o modelo de estágios de compra estiver em um status _Live_ (publicado), adicione o modelo aos interesses de solução onde deseja usá-lo para rastrear a progressão do grupo de compras. Nas suas jornadas de conta, você pode incluir ações para fazer a transição de contas para um estágio especificado e adicionar transições de estágio como eventos que determinam como as contas se movem pela jornada.

### Associação de interesse de solução

Para cada interesse de solução existente onde você deseja associar o modelo de estágios de grupo de compras, abra os detalhes de interesse da solução e adicione o modelo. Você também pode adicionar o modelo às propriedades ao [criar um interesse de solução](./solution-interests.md#create-a-solution-interest).

1. Selecione a guia _[!UICONTROL Solution interest]_.

1. Abra o interesse da solução usando um dos métodos a seguir para abrir as propriedades do interesse da solução que deseja editar:

   * Clique no nome de interesse da solução.
   * Clique nas reticências (**...**) ao lado dele e escolha **[!UICONTROL Editar]**.

   ![Menu Mais interesses da solução](assets/solution-interests-more-menu.png){width="500" zoomable="no"}

1. Selecione o **[!UICONTROL Modelo de estágio de grupo de compras]** para usar a progressão de estágio de grupo de compras (opcional).

   ![Selecione o modelo de estágios dos grupos de compra para o interesse da solução](assets/solution-interest-edit-buying-group-stages-model.png){width="700" zoomable="yes"}

1. Se necessário, altere a configuração **[!UICONTROL Atualizar grupos de compra existentes]**.

   Quando essa opção está habilitada, todos os grupos de compras existentes combinados com os interesses da solução são atualizados por meio do ciclo de sincronização de 24 horas.

1. Clique em **[!UICONTROL Salvar]**.

### Dividir caminhos

Usando um [nó de caminho dividido](../journeys/journey-nodes.md#split-paths), você pode filtrar no nível de conta ou no nível de pessoas de acordo com estágios de grupo de compra. Por exemplo, adicione um estágio de grupo de compra como uma condição de caminho ao dividir caminhos por membro do grupo de compra.

>[!BEGINTABS]

>[!TAB Nível da conta]

1. Abra a jornada da conta no editor.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](../journeys/assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para a divisão.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

   ![Nó de caminho dividido - adicionar condição](../journeys/assets/node-split-properties-apply-condition.png){width="500"}

1. No editor de condições, adicione o filtro de grupo de compra para definir o caminho dividido.

   * À esquerda, expanda os **[!UICONTROL Filtros especiais]** na parte inferior e arraste o atributo **[!UICONTROL Tem Grupo de Compras]** para o espaço de trabalho do filtro.

   * Defina o **[!UICONTROL Interesse da Solução]** para um que esteja associado ao modelo de estágios de grupo de compras.

   * Clique em **[!UICONTROL Adicionar restrição]** e escolha **[!UICONTROL Estágio de compra de grupo]**.

     ![Nó de caminho dividido - lógica de filtro de condições](./assets/stages-split-condition-buying-group-stage.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

   O caminho dividido é definido nas propriedades do nó à direita.

   ![propriedades do nó dividido do Jornada](./assets/stages-split-node-account-properties.png){width="600" zoomable="yes"}

1. Continue a definir outros caminhos para o nó dividido e salve a jornada.

>[!TAB Nível de pessoas]

1. Abra a jornada da conta no editor.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](../journeys/assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para a divisão.

   Deixe o padrão para _[!UICONTROL Atributo usado para condições]_ como **[!UICONTROL Somente atributos de pessoas]**.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

   ![Nó de caminho dividido - adicionar condição](../journeys/assets/node-split-properties-apply-condition.png){width="500"}

1. No editor de condições, adicione o filtro de grupo de compra para definir o caminho dividido.

   * À esquerda, expanda os **[!UICONTROL Filtros especiais]** na parte inferior e arraste o atributo **[!UICONTROL Membro do Grupo de Compras]** para o espaço de trabalho do filtro.

   * Defina o **[!UICONTROL Interesse da Solução]** para um que esteja associado ao modelo de estágios de grupo de compras.

   * Clique em **[!UICONTROL Adicionar restrição]** e escolha **[!UICONTROL Estágio de compra de grupo]**.

     ![Nó de caminho dividido - lógica de filtro de condições](./assets/stages-split-condition-member-of-buying-group.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

   O caminho dividido é definido nas propriedades do nó à direita.

   ![Nó de Jornada - escutar eventos na conta](./assets/stages-split-node-people-properties.png){width="600" zoomable="yes"}

1. Continue a definir outros caminhos para o nó dividido e salve a jornada.

>[!ENDTABS]

### Atualizar ação da conta de estágio de grupo de compras

Usando um [nó de ação de conta](../journeys/journey-nodes.md#add-an-account-action), você pode atualizar o estágio de grupo de compra. A definição desse nó envolve selecionar o interesse da solução e definir o novo estágio para o grupo de compras.

>[!NOTE]
>
>Se o novo estágio não for uma transição válida (conforme definido no modelo), a ação não será aplicada à conta.

1. Abra a jornada da conta no editor.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

   ![Adicionar nó de jornada - execute uma ação](../journeys/assets/add-node-action.png){width="400"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para a ação.

1. Defina a ação para atualizar o estágio de grupo de compras.

   * Para **[!UICONTROL Ação nas contas]**, selecione **[!UICONTROL Atualizar Estágio do Grupo de Compras]**.

   * Para **[!UICONTROL Selecionar interesse da solução]**, selecione um que esteja associado ao modelo de estágios de grupo de compras.

   * Para **[!UICONTROL Novo estágio]**, selecione o estágio para fazer a transição da conta.

   A ação é definida nas propriedades do nó à direita.

   Nó do ![Jornada - executar uma ação em uma conta](./assets/stages-take-action-node-update-buying-group-stage.png){width="600" zoomable="yes"}

1. Continue a fazer outras alterações e salvar a jornada.

### Evento de conta

Use a ocorrência de uma alteração de estágio de grupo de compra para mover a conta para a próxima etapa da jornada. A definição desse nó envolve a seleção do interesse da solução e restrições adicionais para atender ao acionador do evento.

1. Abra a jornada da conta no editor.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

   ![Adicionar nó de jornada - escutar um evento](../journeys/assets/add-node-event.png){width="400"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para o tipo de evento.

1. Para **[!UICONTROL Selecionar evento de contas]**, escolha **[!UICONTROL Alterar Estágio de Grupo de Compras]**.

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

   * Para **[!UICONTROL Interesse da Solução]**, corresponda à condição para um interesse de solução associado ao modelo de estágios de grupo de compras.

   * Clique em **[!UICONTROL Adicionar restrição]** e selecione a alteração do estágio de grupo de compras que você deseja usar para acionar o evento.

     ![Nó de Jornada - escutar eventos na conta](./assets/stages-event-node-edit-buying-group-stage-change.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

   O evento é definido nas propriedades do nó à direita.

   ![Nó de Jornada - escutar eventos na conta](./assets/stages-event-node-stage-change-properties.png){width="700" zoomable="yes"}

1. Continue a fazer outras alterações e salvar a jornada.
