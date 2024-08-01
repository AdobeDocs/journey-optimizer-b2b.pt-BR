---
title: Grupos de compra
description: Saiba mais sobre grupos de compras e seus componentes.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 7%

---


# Grupos de compras

Para atividades de vendas e marketing B2B, as contas são fundamentais para qualquer estratégia. Cada conta tem um grupo de pessoas associadas a ela, e essas pessoas podem ser funcionários da conta ou contratados que trabalham com a conta. As contas são hierárquicas e produtos diferentes podem ser vendidos em diferentes níveis na hierarquia. Por exemplo, o Adobe Experience Platform pode ser vendido no nível corporativo para uma conta de nível superior, enquanto o Adobe Photoshop pode ser vendido para uma conta que representa uma divisão ou departamento dentro de uma organização, como um departamento de design dentro de uma corporação maior.

![Diagrama de funções da conta](assets/account-roles-diagram.png){width="800"}

Dentro da conta, pode haver um subconjunto de pessoas que compõem o _grupo de compras_. Essas pessoas são as que tomam a decisão de comprar, portanto, precisam de atenção especial do profissional de marketing e podem precisar de informações diferentes fornecidas para elas do que as outras pessoas associadas à conta. Os grupos de compras podem incluir um grupo diferente de pessoas para diferentes linhas de produtos ou ofertas. Por exemplo, um produto de segurança cibernética normalmente exige um CIO ou CIO e um representante do departamento jurídico para aprovar uma compra, mas um produto de rastreamento de bugs normalmente tem um vice-presidente de engenharia e um Director de TI como membros do grupo de compras.

## Componentes principais

Você pode aumentar a eficácia do marketing estabelecendo grupos de compra no Journey Optimizer B2B Edition que identificam membros ausentes para suas listas de contas de destino com base nas soluções pelas quais suas equipes de vendas são responsáveis pelas vendas. Antes de você e sua equipe de marketing começarem a criar seus grupos de compra, verifique se você tem os componentes principais definidos. Esses componentes são essenciais para atingir suas metas e objetivos de negócios.

| Componente | Finalidade |
| --------- | ------- |
| Interesse na solução | Esse componente fornece a resposta para: <ul><li>Como organização de marketing, o que você está vendendo?</li><li>Que produto ou coleção de produtos você pretende vender?</li></ul>  **_Exemplo:_** venda cruzada do novo Produto X para clientes existentes |
| Público-alvo de conta | Esse componente fornece a resposta para: <ul><li>Para quem você está vendendo?</li><li>Qual é a lista de contas que você está direcionando?</li></ul> **_Exemplo:_** Segmento de conta definido por contas com o Produto Y com receita superior a 1 milhão |
| Comprando modelos de função do grupo | Esse componente fornece a resposta para: <ul><li>Quais funções você está direcionando?</li><li>Qual conjunto de regras é usado para determinar quem está atribuído às funções de grupo de compra?</li></ul>  **_Exemplo:_** Atribua uma pessoa com título de CMO à função de Tomador de Decisão |

## Fluxo de trabalho do grupo de compra

1. Criar grupos de compra.

   Opções:
   * Usar [interesses da solução](./solution-interests.md) e [modelo de função](./buying-groups-role-templates.md)
   * Usar importação de terceiros
   * Gerar a partir do AI/ML

1. Identificar pessoas desaparecidas.

   Analise o grupo de compras usando filtros.

   **_Exemplo:_** a função de tomador de decisão está ausente e a pontuação de integridade é &lt; 50

1. Complete as definições de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Use em uma jornada de conta por meio dos interesses de solução associados.

## Acessar grupos de compras e componentes

Na navegação à esquerda, expanda **[!UICONTROL Contas]** e clique em **[!UICONTROL Comprando grupos]**.

A página _[!UICONTROL Grupos de compras]_ é organizada como guias:

| Tabulação | Descrição |
| --- | ----------- |
| [!UICONTROL Visão geral] | Esta guia é a padrão e exibe o [Painel de grupos de compra](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Procurar] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquisar por nome do grupo de compras. </li><li>Filtrar por interesse da solução. </li><li>Detalhar detalhes do grupo de compras. </li><li>Criar um grupo de compras. Excluir um grupo de compras.</li></ul> |
| [!UICONTROL Interesses da solução] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquisar por nome do grupo de compras. </li><li>Acesse e edite as propriedades de interesse da solução. </li><li>Criar um interesse de solução. </li><li>Excluir um interesse de solução. </li><li>Exibir e excluir ordens de produção do grupo de compras. </li></ul> |
| [!UICONTROL Modelos de Funções] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de modelos de funções existentes. </li><li>Pesquisar por nome do modelo de funções. </li><li>Acesse e edite as propriedades e condições do modelo de funções. </li><li>Crie um modelo de funções. </li><li>Excluir um modelo de funções. </li></ul> |

## Pesquisa e filtro do grupo de compras

Use a guia _[!UICONTROL Procurar]_ para exibir a lista de grupos de compras. Pesquise por nome e filtre a lista por interesse na solução.

![Página de navegação do grupo de compras](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Detalhes do grupo de compras

Para acessar os detalhes de um grupo de compras, clique no nome do grupo de compras na guia _[!UICONTROL Procurar]_.

![Detalhes do grupo de compras](assets/buying-group-details.png){width="600" zoomable="yes"}

### Pontuação de integridade do grupo de compras

A pontuação de integridade é usada para determinar se o grupo de compras está completo, o que significa que ele tem os membros certos atribuídos às funções e está pronto para ser usado em uma jornada de conta. Essa pontuação é uma porcentagem baseada no número de funções no grupo de compra e quantas funções são atribuídas com pelo menos um lead.

Por exemplo, se houver quatro funções em um grupo de compra e três das quatro funções forem atribuídas a pelo menos um cliente potencial, o grupo de compra estará 75% concluído.

A pontuação de integridade do grupo de compras é recalculada toda vez que um grupo de compras é criado ou atualizado.

### Pontuação de engajamento do grupo de compra

A pontuação de engajamento é usada para avaliar a eficácia de seus programas de marketing com base nas atividades comportamentais de grupo de compra rastreadas nas jornadas. Essa pontuação é derivada da atividade nos últimos 30 dias. Qualquer alteração de função em um modelo requer o recálculo da pontuação de engajamento para todos os grupos de compra criados usando esse modelo. Somente atividades de entrada são avaliadas no cálculo de uma pontuação de envolvimento.

A pontuação exibida é arredondada (por exemplo, uma pontuação de 75,89999 é exibida como 76), não há limite superior para a pontuação para GA e há um limite de frequência diário de 20.

Os exemplos a seguir ilustram o cálculo da pontuação de engajamento:

**Grupo de compras 1** - pontuação de engajamento = 22,15

| Usuário | Função | Peso da função | Ação | Hoje | Ontem | Peso da ação | Pontuação |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Adam | Tomador de decisão | 80% | Site Visitado | 1000 | 2 | 1 | 22 |
| | | | E-mail clicado | 1 | 0 | 1 | 1 |
| | | | Pub baixado | 1 | 3 | 1 | 4 |
| Bob | Influenciador | 15% | Site Visitado | 1 | 2 | 1 | 3 |
| Calvin | Profissional | 5% | Site Visitado | 1 | 1 | 1 | 2 |

**Grupo de compras 2** - pontuação de engajamento = 8,55

| Usuário | Função | Peso da função | Ação | Hoje | Ontem | Peso da ação | Pontuação |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Alvin | Tomador de decisão | 80% | Site Visitado | 3 | 2 | 1 | 5 |
| | | | E-mail clicado | 1 | 0 | 1 | 1 |
| | | | Pub baixado | 1 | 3 | 1 | 4 |
| Bret | Influenciador | 15% | Site Visitado | 1 | 2 | 1 | 3 |
| Cam | Profissional | 5% | Site Visitado | 1 | 1 | 1 | 2 |
