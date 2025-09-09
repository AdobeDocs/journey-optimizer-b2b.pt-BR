---
title: Detalhes do Grupo de Compras
description: Visualize os detalhes do grupo de compras com insights de IA, gerencie funções de membro, rastreie pontuações de engajamento e analise dados de intenção no Journey Optimizer B2B edition.
feature: Buying Groups, Intelligent Insights
role: User
exl-id: f14301dc-d605-4ed2-8867-6a49675019de
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%

---

# Detalhes do grupo de compra

Quando você clica em um nome de grupo de compras em qualquer lugar no Journey Optimizer B2B edition, os detalhes do grupo de compras são exibidos. Essa visão geral fornece informações úteis sobre o grupo de compras, incluindo resumos de IA generativos. Também há [ações](#buying-group-actions) que você pode executar para contatos associados à conta.

![Acessar os detalhes do grupo de compras](./assets/buying-group-details.png){width="800" zoomable="yes"}

Use a guia **[!UICONTROL Visão Geral]** para revisar informações sobre a conta, e a guia **[!UICONTROL Membros]** para acessar uma lista de membros do grupo de compra.

## Guia Visão geral

A guia Visão geral é composta de três seções principais:

### Resumo do grupo de compras

![Resumo do grupo de compras](./assets/details-page-buying-group-overview.png){zoomable="yes"}

A seção de resumo do grupo de compras inclui as seguintes informações do grupo de compras:

* Nome do grupo de compra
* Nome da conta (clique no nome para abrir os [detalhes da conta](../accounts/account-details.md))
* Número de membros no grupo de compra
* Pontuação de engajamento
* Pontuação de integridade
* Estágio de grupo de compras atual
* Modelo de função (clique no nome para abrir o [modelo de funções](buying-groups-role-templates.md#access-and-browse-role-templates))
* Data da última modificação/atualização
* Resumo da IA geral do grupo de compras

### Visão geral da conta

![Visão geral da conta do grupo de compras](./assets/details-page-buying-group-account-overview.png){zoomable="yes"}

A seção de visão geral da conta inclui as seguintes informações da conta:

* Nome da conta (clique no nome para abrir os detalhes da conta)
* Número de pessoas na conta
* Setor
* Oportunidades abertas
* Três jornadas de conta mais recentes nas quais a conta está em uso no momento (clique no nome para abrir os detalhes da jornada)
* Resumo da conta da IA geral

### Dados de intenção

No Journey Optimizer B2B edition, o modelo de Detecção de intenções prevê uma solução/produto de interesse com alta confiança suficiente com base na atividade de compra dos membros do grupo. A intenção de comprar membros do grupo pode ser interpretada como a probabilidade de ter interesse em um produto.

{{intent-data-note}}

![Dados da intenção - detalhes do grupo de compras](../accounts/assets/intent-data-panel.png){width="700" zoomable="yes"}

* Níveis de intenção
* Tipos de sinal de intenção - Palavras-chave, produto e solução

### Membros do grupo de compra

![Membros do grupo de compra](./assets/details-page-buying-group-members.png){width="800" zoomable="yes"}

A seção _[!UICONTROL Membros do grupo de compra]_ exibe duas linhas que destacam membros do grupo de compra:

* **[!UICONTROL Tomador de decisão]** - Os três principais tomadores de decisão com base na pontuação de engajamento da pessoa
* **[!UICONTROL Membros mais envolvidos]** - Outros membros mais envolvidos com base na pontuação de engajamento da pessoa

Cada cartão de membro inclui os seguintes detalhes:

* Nome
* Título
* Função
* Pontuação de envolvimento do lead

Clique em **[!UICONTROL Exibir detalhes]** para acessar as seguintes informações do membro:

* Resumo da IA gerativa
* Último momento interessante
* Atividades mais recentes (duas)
* Outros grupos de compra dos quais o cliente potencial é membro (limitado a três grupos de compra com base no adicionado mais recentemente).
* Endereço de email
* Número de telefone

![Exibir mais detalhes de um membro do grupo de compras](./assets/details-page-buying-group-members-view-details.png){width="600" zoomable="yes"}

## Guia Membros

Selecione a guia **[!UICONTROL Membros]** para exibir uma lista de todos os membros do grupo de compras. Cada lista de membros inclui o nome, a função, o cargo, o endereço de email, o número de telefone e a origem.

![Guia Membros - detalhes do grupo de compra](./assets/buying-group-details-members-tab.png){width="700" zoomable="yes"}

Há várias ações que você pode executar a partir da guia _Membros_:

### Atribuir um novo membro

Uma conta pode ter um ou mais grupos de compras associados a ela, e os membros do grupo de compras normalmente são um subconjunto de contatos da conta. Você pode adicionar manualmente qualquer contato da conta associada ao grupo de compras.

1. Clique em **[!UICONTROL Atribuir novo membro]** no canto superior direito.

1. Na caixa de diálogo _[!UICONTROL Atribuir membro]_, selecione os clientes em potencial de conta que deseja adicionar ao grupo de compras e clique em **[!UICONTROL Avançar]**.

   ![Guia Membros - atribuir novos membros](./assets/buying-group-details-assign-member.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Editar nova função de membro]_, selecione a função a ser atribuída a cada um dos novos membros.

   Guia ![Membros - atribuir nova função de membro](./assets/buying-group-details-assign-member-edit-role.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.

### Remover um membro

Você pode remover um ou mais membros selecionados (até 50 de cada vez) do grupo de compras.

1. Marque as caixas de seleção dos membros que deseja remover.

1. Na barra de seleção na parte inferior, clique em **[!UICONTROL Remover membros]**.

   ![Guia Membros - remover membros](./assets/buying-group-details-remove-selected.png){width="700" zoomable="yes"}

1. No diálogo de confirmação, clique em **[!UICONTROL Remover]**.

### Editar função

Você pode alterar a função de um ou mais membros selecionados (até 50 de cada vez) do grupo de compras.

1. Marque as caixas de seleção dos membros que você deseja alterar funções.

1. Na barra de seleção na parte inferior, clique em **[!UICONTROL Editar funções]**.

   ![Guia Membros - editar funções](./assets/buying-group-details-edit-roles.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Editar função de membro]_, selecione a função a ser atribuída a cada um dos membros.

   ![Editar funções de membro - escolher funções](./assets/buying-group-details-edit-roles-choose-roles.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.

### Enviar email

Você pode enviar um email aprovado pelo profissional de marketing para um ou mais membros selecionados (até 50 de cada vez) de um grupo de compra. A lista de emails disponíveis é limitada aos emails aprovados da instância conectada do Marketo Engage.

1. Marque as caixas de seleção dos membros que deseja receber o email.

1. Na parte superior direita ou na barra de seleção na parte inferior, clique em **[!UICONTROL Enviar email]**.

   ![Guia Membros - enviar email](./assets/buying-group-details-send-email.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Enviar email]_, selecione o espaço de trabalho do Marketo Engage e marque a caixa de seleção do email que deseja enviar.

   ![Selecione um email para enviar aos membros do grupo de compras](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Enviar]**.
