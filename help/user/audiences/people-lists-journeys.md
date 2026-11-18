---
title: Usar listas de pessoas no Jornada
description: Use listas de pessoas para adicionar ou remover pessoas dinamicamente e dividir caminhos de jornada por associação de lista no Journey Optimizer B2B Edition.
feature: Audiences, Person Journeys, Account Journeys
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%
---

# Usar listas de pessoas no jornada

Há várias maneiras de incorporar [listas de pessoas](./people-lists.md) às suas jornadas de conta e jornadas de pessoas:

* **Manter uma lista estática de uma jornada** - Em um nó _Realizar uma ação_, use a ação _[!UICONTROL Adicionar à Lista de Pessoas]_ ou _[!UICONTROL Remover da Lista de Pessoas]_ para atualizar a associação de uma lista estática de pessoas à medida que as pessoas passam pela jornada.
* **Rotear pessoas com base na associação à lista** - Em um nó _Dividir caminhos_, use o filtro _[!UICONTROL Membro de Pessoa da Lista Estática de Pessoas]_ ou _[!UICONTROL Membro de Pessoa da Lista Dinâmica de Pessoas]_ para criar um caminho para pessoas que sejam (ou não) membros de uma lista.

Por exemplo, você pode criar uma lista de exclusão de membros da equipe e parceiros e usá-la para excluir essas pessoas de um caminho de criação. Ou você pode adicionar pessoas a uma lista estática quando elas atingem um ponto de qualificação em uma jornada e, em seguida, usar essa lista para ramificar pessoas em uma jornada diferente.

## Realizar um nó de ação - Adicionar à lista de pessoas {#add-to-people-list}

**_Somente listas estáticas de pessoas_**

Em uma jornada de conta ou pessoa, adicione pessoas a uma lista estática de pessoas usando o [um _Executar uma ação_ no nó](../journeys/action-nodes.md#people-actions).

Por exemplo, considere um caminho de jornada para enviar um email e algumas pessoas se registrarem em um webinário. Você considera essa resposta um ponto de qualificação na jornada. Após a qualificação, você deseja adicionar essas pessoas a uma lista estática de pessoas que outra jornada usa para dividir pessoas qualificadas em um caminho diferente.

>[!NOTE]
>
>Se uma pessoa já estiver na lista quando o nó for executado, a ação será ignorada.

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

1. (Somente jornadas da conta) Selecione a opção _[!UICONTROL Ação em]_ **[!UICONTROL Pessoas]**.

1. Para _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Adicionar à Lista de Pessoas]**.

1. Para **[!UICONTROL Selecionar Lista Estática de Pessoas]**, escolha a lista de pessoas à qual você deseja adicionar pessoas.

   ![Selecione Adicionar à Lista de Pessoas](../journeys/assets/node-action-add-to-people-list.png){width="300"}

## Realizar um nó de ação - Remover da lista de pessoas {#remove-from-people-list}

**_Somente listas estáticas de pessoas_**

Em uma jornada de conta ou pessoa, remova as pessoas de uma lista estática de pessoas usando o [nó _Realizar uma ação_](../journeys/action-nodes.md#people-actions).

Por exemplo, depois que uma pessoa converte, você deseja removê-la de uma lista estática. Essa lista é usada para encaminhar as pessoas para um caminho de criação para que elas não recebam mais comunicações de criação.

>[!NOTE]
>
>Se uma pessoa não estiver na lista da qual está agendada para remoção, a ação será ignorada.

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

1. (Somente jornadas da conta) Selecione a opção _[!UICONTROL Ação em]_ **[!UICONTROL Pessoas]**.

1. Para _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Remover da Lista de Pessoas]**.

1. Para **[!UICONTROL Selecionar Lista Estática de Pessoas]**, escolha a lista de pessoas da qual deseja remover pessoas.

   ![Selecione Remover da Lista de Pessoas](../journeys/assets/node-action-remove-from-people-list.png){width="300"}

## Nó de caminhos divididos - Membro da lista de pessoas {#split-paths-by-list-membership}

**_jornadas de conta e pessoa_**

Use os filtros de associação da lista de pessoas em um [_nó de caminhos divididos_](../journeys/split-merge-paths-nodes.md) para rotear pessoas com base no fato de serem membros de uma lista de pessoas. Dois filtros estão disponíveis:

| Filtro | Descrição |
| ------ | ----------- |
| [!UICONTROL Membro da Pessoa da Lista Dinâmica de Pessoas] | A pessoa é ou não membro de uma ou mais listas de pessoas dinâmicas. A associação reflete as regras atuais da lista. |
| [!UICONTROL Membro da Pessoa da Lista Estática de Pessoas] | A pessoa é ou não é membro de uma ou mais listas estáticas de pessoas. |

Esses filtros estão disponíveis em ambos os tipos de jornada:

* **jornadas de pessoa** - Em um nó _Caminhos divididos_.
* **jornadas de Conta** - Em um nó _Caminhos divididos_ dividido por _[!UICONTROL Pessoas]_.

Para excluir membros da equipe e parceiros de um caminho de criação, adicione o filtro _[!UICONTROL Lista Estática de Membros de Pessoas]_, defina o operador como `is not` e selecione a lista.

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](../journeys/assets/add-node-split.png){width="300" zoomable="no"}

1. (Somente jornadas da conta) Defina o nó para condições de pessoas.

   * Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para a divisão.

   * Defina **[!UICONTROL Atributos usados para condições]** como **[!UICONTROL Somente atributos de pessoas]**.

   ![jornada de conta - nó de caminho dividido - atributos de pessoas](../journeys/assets/node-split-path-account-journey-people-attributes.png){width="300" zoomable="no"}

1. Para definir uma condição para _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

1. No editor de condições, expanda a pasta _[!UICONTROL Filtros especiais]_ e arraste o filtro **[!UICONTROL Membro de Pessoa da Lista Dinâmica de Pessoas]** ou **[!UICONTROL Membro de Pessoa da Lista Estática de Pessoas]** para o espaço de trabalho de condições.

   ![Dividir o editor de condições de caminho com os filtros da Lista de Pessoas de Membro de Pessoa](../accounts/assets/account-lists-person-journeys-split-path-filter.png){width="700" zoomable="yes"}

1. Para incluir membros da lista, defina a associação como `is`.

   Para excluí-los, defina como `is not`.

1. Selecione a lista de pessoas a serem avaliadas.

   Insira texto no campo para filtrar as listas disponíveis. Somente as listas de pessoas criadas pelo usuário estão disponíveis para seleção.

1. Refine suas condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior.

   Você pode combinar filtros de associação de lista com outros filtros de pessoas e optar por corresponder todas as condições ou qualquer condição.

1. Clique em **[!UICONTROL Concluído]**.

Continue a configurar o nó de caminhos divididos conforme descrito em [_Adicionar um caminho dividido pelo nó de pessoas_](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node). Para obter mais informações sobre filtros de associação, consulte [_Filtragem de associação_](../journeys/split-merge-paths-nodes.md#membership-filtering).
