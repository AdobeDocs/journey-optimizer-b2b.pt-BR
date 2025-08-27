---
title: Grupos de compra
description: Saiba como os grupos de compra no Journey Optimizer B2B Edition podem aumentar a eficácia do marketing por identificar e direcionar membros para suas listas de conta.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: eb80b57b0481837a50c7c0985ac4dc5d71f3577e
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 75%

---


# Grupos de compra

As contas são fundamentais para qualquer estratégia de atividades de vendas e marketing B2B. Cada conta tem um grupo de pessoas associado, as quais podem ser funcionários ou profissionais contratados que trabalham com a conta. As contas são hierárquicas e produtos diferentes podem ser vendidos em diferentes níveis na hierarquia. Por exemplo, a Adobe Experience Platform pode ser vendida no nível corporativo a uma conta de nível superior. E o Adobe Photoshop pode ser vendido a uma conta que representa uma divisão ou departamento dentro de uma organização, como um departamento de design dentro de uma corporação maior.

![Diagrama de funções da conta](assets/account-roles-diagram.png){width="800"}

A conta pode conter um subconjunto de pessoas que compõe o _grupo de compra_. Essas são as pessoas que tomam a decisão de compra final; portanto, elas precisam de atenção especial de profissionais de marketing e podem precisar de acesso a informações diferentes em comparação com as outras pessoas associadas à conta. Os grupos de compra podem incluir um grupo diferente de pessoas para diferentes linhas de produtos ou ofertas. Por exemplo, um produto de segurança cibernética normalmente pode exigir um diretor de informação ou diretor de segurança e um representante do departamento jurídico para aprovar uma compra. Um produto de rastreamento de erros normalmente tem um VP de engenharia e um diretor de TI como membros do grupo de compra.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Componentes principais

Você pode aumentar a eficácia do marketing estabelecendo grupos de compras no Journey Optimizer B2B edition que identificam membros para suas listas de contas de destino das soluções pelas quais suas equipes de vendas são responsáveis. Antes de você e sua equipe de marketing começarem a criar os grupos de compra, verifique se os principais componentes foram definidos. Esses componentes são essenciais para atingir suas metas e objetivos de negócios.

| Componente | Finalidade |
| --------- | ------- |
| Interesse na solução | Esse componente fornece a resposta para: <ul><li>O que você está vendendo como organização de marketing?</li><li>Que produto ou coleção de produtos você pretende vender?</li></ul>  **_Example:_** Venda cruzada do novo Produto X para clientes existentes |
| Público-alvo de conta | Esse componente fornece a resposta para: <ul><li>Para quem você está vendendo?</li><li>Qual é a lista de contas que você está direcionando?</li></ul> **_Example:_** Segmento de conta definido por contas com o Produto Y com receita superior a 1 milhão |
| Modelos de função do grupo de compra | Esse componente fornece a resposta para: <ul><li>Quais funções você está direcionando?</li><li>Qual conjunto de regras é usado para determinar quem está atribuído às funções do grupo de compra?</li></ul>  **_Example:_** Atribuir uma pessoa com o título de CMO à função de tomador de decisões |
| Estágios do grupo de compra | (Opcional) Este componente fornece a resposta para: “Como o grupo de compra está conduzindo o sucesso ou o fracasso?” |

## Atribuição de membro

Há três maneiras pelas quais os membros são atribuídos ou removidos de um grupo de compra. A lista a seguir descreve esses métodos de adição e remoção na ordem de precedência. O método mais alto tem a maior precedência e um método mais baixo não pode substituí-lo.

1. **_Ação manual_**: uma ação manual de adição ou remoção de membro realizada por um usuário de vendas para o grupo de compra
2. **_Ação de jornada_**: [nós de ação de jornada para associação ao grupo de compra](../journeys/action-nodes.md#add-a-people-based-action) (_Atribuir ao grupo de compra_ ou _Remover do grupo de compra_)
3. **_Trabalhos do sistema_**: trabalhos de [criação](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) e manutenção de grupo de compras.

Para evitar a substituição incorreta de uma atribuição de membro em um grupo de compra, essa lista está na ordem de precedência seguida no sistema para garantir uma atribuição de membro precisa. Por exemplo, quando um usuário de vendas adiciona manualmente um membro ao grupo de compra, ele não deseja que um trabalho de manutenção altere essa adição. Usando a ordem de precedência, os seguintes cenários são aplicados:

* Se um usuário atribuir manualmente um membro a um grupo de compras e ele for seguido por um trabalho de manutenção de grupo de compras que remove o mesmo membro do grupo de compras, o trabalho de manutenção **não removerá** esse membro e não poderá substituir a atribuição manual.
* Se um usuário atribuir manualmente um membro a um grupo de compras e ele for seguido por um nó de jornada acionado que remove o mesmo membro do grupo de compras, a ação do nó **não removerá** esse membro e não poderá substituir a atribuição manual.
* Se um nó de ação de jornada disparada adicionar um membro a um grupo de compras e for seguido por um trabalho de manutenção de grupo de compras que remove o mesmo membro do grupo de compras, o trabalho de manutenção **não removerá** esse membro e não poderá substituir a atribuição de ação de jornada.

## Fluxo de trabalho do grupo de compra

1. Criar grupos de compra.

   * Definir [interesse na solução](./solution-interests.md) e [modelo de função](./buying-groups-role-templates.md)
   * [Crie o grupo de compra](./buying-groups-create.md#create-buying-groups) e atribua [estágios do grupo de compra](./buying-group-stages.md).

1. Identificar pessoas ausentes após a conclusão.

   Analise o grupo de compra usando filtros.

   **_Example:_** A função de tomador de decisão está ausente e a pontuação de conclusão é &lt; 50

1. Conclua as definições de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Adicione ações de grupo de compra às suas jornadas de conta.

## Exibir grupos de compra e componentes

Na navegação à esquerda, expanda **[!UICONTROL Contas]** e clique em **[!UICONTROL Grupos de compra]**.

A página _[!UICONTROL Grupos de compra]_ é organizada em guias:

| Tabulação | Descrição |
| --- | ----------- |
| [!UICONTROL Visão geral] | Esta guia é a padrão e exibe o [painel de grupos de compra](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Procurar] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquisar por nome do grupo de compra. </li><li>Filtrar por interesse da solução. </li><li>Especificar os detalhes do grupo de compra. </li><li>Crie um grupo de compra. </li></ul> |
| [!UICONTROL Interesses de solução] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquisar por nome do grupo de compra. </li><li>Acessar e editar as propriedades de interesse de solução. </li><li>Criar um interesse de solução. </li><li>Excluir um interesse de solução. </li><li>Exibir e excluir trabalhos de grupo de compra. </li></ul> |
| [!UICONTROL Modelos de funções] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de modelos de funções existentes. </li><li>Pesquisar por nome do modelo de funções. </li><li>Acessar e editar as propriedades e condições do modelo de funções. </li><li>Criar um modelo de funções. </li><li>Excluir um modelo de funções. </li></ul> |
| [!UICONTROL Estágios] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir o modelo de estágios existente dos grupos de compra. </li><li>Acessar e editar o modelo de estágios de rascunho do grupo de compra. </li><li>Criar o modelo de estágios do grupo de compra. </li></ul> |

## Pesquisa e filtro do grupo de compra

Use a guia _[!UICONTROL Procurar]_ para visualizar a lista de grupos de compra. É possível pesquisar por nome e filtrar a lista por interesse de solução.

![Página procurar do grupo de compra](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Detalhes do grupo de compra

Para acessar os detalhes de um grupo de compra, clique no nome do grupo de compra na guia _[!UICONTROL Procurar]_. [Saiba mais](./buying-group-details.md)

![Detalhes do grupo de compra](assets/buying-group-details.png){width="600" zoomable="yes"}

### Pontuação de integridade do grupo de compra

A pontuação de integridade é usada para determinar se o grupo de compras tem os membros certos atribuídos às funções e está pronto para ser usado em uma jornada de conta. Essa pontuação é uma porcentagem baseada no número de funções no grupo de compra e em quantas funções são atribuídas a pelo menos um lead.

Por exemplo, se houver quatro funções em um grupo de compra e três delas forem atribuídas a pelo menos um lead, o grupo de compra terá uma integridade de 75%.

A pontuação de integridade é recalculada toda vez que um grupo de compra é criado ou atualizado.

### Pontuação de engajamento do grupo de compra {#engagement-score}

A pontuação de engajamento é baseada nas atividades de membro do grupo de compra, ações ponderadas e funções ponderadas. A pontuação resultante é normalizada no locatário/instância para permitir uma comparação consistente e insights acionáveis.

O cálculo da pontuação de engajamento inicial começa assim que você cria o grupo de compra e é recalculado diariamente.

Consulte [Pontuações de engajamento](./engagement-scores.md) para obter informações detalhadas sobre atividades e cálculos de pontuação de engajamento.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
