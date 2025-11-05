---
title: Pontuações de integridade para grupos de compra
description: Calcule as pontuações de integridade do grupo de compras usando limites baseados em função, requisitos de membro personalizáveis e configurações de integridade no Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 3%

---


# Pontuações de integridade {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Pontuação de integridade"
>abstract="As pontuações de integridade refletem o quão bem a associação ao grupo de compras está alinhada para um grupo de compras pronto para vendas."

Uma pontuação de integridade é uma porcentagem que indica como um grupo de compra é preenchido com os membros necessários em suas funções definidas. Essas pontuações são baseadas nos limites do membro da função que você configura no modelo de funções e no número real de membros atribuídos a cada função no grupo de compra. As pontuações resultantes ajudam os profissionais de marketing a avaliar a prontidão das vendas e identificar lacunas na composição do grupo de compras. O cálculo de pontuação ocorre automaticamente conforme a associação de grupo de compra é alterada.

![Pontuações de integridade do grupo de compra](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Há dois tipos de pontuações de integridade:

* **Pontuação de integridade do grupo de compra** - A pontuação de integridade do grupo de compra é uma porcentagem entre 0% e 100% e representa a integridade geral do grupo de compra com base nos cálculos de integridade de nível de função.

  A pontuação de conclusão do grupo de compras é exibida na página [Detalhes do grupo de compras](./buying-group-details.md). Essa pontuação fornece uma visão rápida sobre se o grupo de compras tem as partes interessadas necessárias em vigor para o envolvimento de vendas.

* **Pontuação de integridade da função** - A pontuação de integridade da função é uma porcentagem para cada função individual em um grupo de compra, com base no número de membros atribuídos a essa função.

  A pontuação de integridade da função para cada função é exibida na página de detalhes do grupo de compra quando você edita funções e ajusta as configurações de integridade. Essas pontuações ajudam a identificar quais funções específicas precisam de membros adicionais para atingir o limite pronto para vendas.

  A página de detalhes exibe as duas primeiras pontuações de integridade da função com um link n_+ para quaisquer funções adicionais. Clique no link para exibir as pontuações adicionais de integridade da função.

As pontuações de integridade refletem o estado atual da associação de grupo de compra e são atualizadas automaticamente à medida que os membros são adicionados ou removidos. As pontuações exibidas são exibidas como porcentagens inteiras (por exemplo, uma pontuação de 66,67% é exibida como 67%).

## Avaliar prontidão de vendas

O Adobe Journey Optimizer B2B edition equipe os profissionais de marketing com ferramentas que garantem que os grupos de compra se alinhem aos processos reais de tomada de decisão. Você pode definir grupos de compras completos usando limites de membros de função personalizáveis que reflitam a metodologia de vendas da sua organização. Ao definir requisitos mínimos e máximos de membros para cada função, você estabelece critérios claros para o que constitui um grupo de compras pronto para vendas.

A pontuação de integridade do grupo de compras fornece uma medida precisa da disponibilidade de vendas do grupo. Por exemplo, para concluir uma oportunidade para uma solução específica, você pode precisar de pelo menos dois tomadores de decisão, um influenciador e pelo menos um profissional. O cálculo da pontuação de integridade leva em conta cada um desses requisitos específicos da função, fornecendo uma visualização da disponibilidade geral do grupo de compras.

## Medir a eficácia da jornada

A integridade do grupo de compra atua como um indicador principal de desempenho (KPI) para a eficácia da jornada. A meta de uma jornada específica pode ser aumentar a integridade do grupo de compras em uma determinada porcentagem ou atingir um limite mínimo antes de acionar alertas prontos para vendas.

Em uma grande empresa, você pode identificar uma pessoa por função. No entanto, essa pessoa pode não ser o contato correto para a venda ou você pode precisar de vários contatos em funções críticas. Por exemplo, uma grande organização pode ter vários tomadores de decisão em tecnologia da informação (TI) distribuídos entre departamentos ou unidades de negócios. Identificar um tomador de decisão pode não ser suficiente para uma venda complexa de uma empresa.

Depois de analisar a integridade atual do grupo de compras, você pode ajustar o número necessário de contatos para cada função no modelo de funções. Esses ajustes permitem ajustar a estratégia do grupo de compras com base em padrões do mundo real e resultados de vendas.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Cálculo de integridade da função {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Cálculo de integridade da função"
>abstract="As pontuações de integridade da função são calculadas como uma porcentagem com base no número de membros atribuídos a uma função."

O Journey Optimizer B2B edition calcula a pontuação de integridade para cada função de grupo de compras individual como uma porcentagem. Baseie essa pontuação em quantos membros são atribuídos à função, em comparação ao [número necessário no modelo de funções](./buying-groups-role-templates.md#change-the-completeness-score-settings) para conclusão.

O cálculo de integridade da função é uma porcentagem linear entre zero e o limite especificado (membros necessários):

* Se o número de membros atribuídos for **zero**, a conclusão da função será **0%**.
* Se o número de membros atribuídos for **no limite ou acima dele**, a integridade da função será **100%**.
* Se o número de membros atribuídos for **entre um e o limite**, a integridade será calculada proporcionalmente.

### Fórmula de integridade da função

A porcentagem de integridade da função é calculada usando a seguinte fórmula:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Onde:

* `Assigned Members` = Número atual de membros na função
* `Threshold` = Conjunto de valores obrigatórios dos membros no modelo de funções

### Exemplos de integridade de função

Os exemplos a seguir ilustram os cálculos de integridade da função com diferentes configurações de limite:

| Função | Membros exigidos | Membros atribuídos | Cálculo | Integridade da função |
|------|------------------|------------------|-------------|-------------------|
| Tomador de decisão | 3 | 0 | None | 0% |
|  |  | 1 | 1/3 × 100 | 33% |
|  |  | 2 | 2/3 × 100 | 66% |
|  |  | 3 | No limite | 100% |
|  |  | 4 | Acima do limite | 100% |
| Influenciador | 5 | 0 | None | 0% |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40% |
|  |   | 3 | 3/5 × 100 | 60% |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | No limite | 100% |
|  |   | 6 | Acima do limite | 100% |

## Cálculo de integridade do grupo de compras {#buying-group-completeness-calculation}

A pontuação de integridade do grupo de compras agrega as pontuações de integridade da função individual. Esse cálculo fornece uma visualização integral da disponibilidade do grupo de compra em todas as funções definidas.

### Fórmula de integridade do grupo de compras

A porcentagem de integridade do grupo de compras é calculada usando a seguinte fórmula:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Onde:

* `Role Completeness %` = Porcentagem de conclusão da função individual (0-100%)
* `Σ` = Soma em todas as funções no grupo de compra

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->