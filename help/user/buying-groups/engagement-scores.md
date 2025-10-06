---
title: Pontuações de engajamento para grupos de compra
description: Calcule as pontuações de engajamento do grupo de compras e da pessoa usando atividades ponderadas, cálculos com base em função e janelas de pontuação de 30 dias no Journey Optimizer B2B edition.
feature: Buying Groups, Engagement
role: User
exl-id: 424d9598-92dd-42de-8447-3c7cebc71a73
source-git-commit: 859e96ce0d450b52a8216f767c595938c23a9d50
workflow-type: tm+mt
source-wordcount: '1254'
ht-degree: 28%

---

# Pontuações de engajamento {#engagement-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Pontuação de engajamento"
>abstract="As pontuações de engajamento determinam o nível de engajamento dos membros do grupo de compra."

Uma pontuação de engajamento é um número que indica o nível de engajamento dos membros de um grupo de compras. Essas pontuações são baseadas nas atividades do membro do grupo de compra, ações ponderadas e funções ponderadas. As pontuações resultantes são normalizadas em um locatário (instância) para permitir uma comparação consistente e insights acionáveis. O cálculo de pontuação é iniciado assim que você cria o grupo de compra. O sistema data hub do Journey Optimizer B2B edition calcula as pontuações diariamente e as carrega no sistema MySQL do MLM (Multi-Level Marketing) usando o serviço de assimilação.

Há dois tipos de pontuações de engajamento:

* **Pontuação de engajamento do grupo de compra** - A pontuação de engajamento do grupo de compra é uma pontuação normalizada entre 0 e 100 e se baseia na pontuação de engajamento calculada no nível da pessoa.

  A pontuação de engajamento do grupo de compras é exibida na página [Detalhes do grupo de compras](./buying-group-details.md). Você também pode visualizar os grupos de compras mais envolvidos no painel Inteligente.

  ![Grupos de compras mais engajados](./assets/person-engagement-score-attribute-filtering.png){width="700" zoomable="yes"}

* **Pontuação de engajamento da pessoa** - A pontuação de engajamento da pessoa é baseada nas atividades de um membro de grupo de compras individual.

  A pontuação de engajamento da pessoa para cada membro do grupo de compras é exibida na página de detalhes do grupo de compras [_[!UICONTROL guia Membros ]_](./buying-group-details.md#buying-group-members). Essas pontuações também são exibidas em páginas e painéis que incluem membros mais engajados e informações de contatos sobrepostas.

  ![Membros mais engajados do grupo de compras](./assets/top-engaged-buying-group-members.png){width="550" zoomable="yes"}

>[!BEGINSHADEBOX]

A pontuação de engajamento da pessoa é um atributo que está disponível para ser usado para filtragem nos [nós de funções](./buying-groups-role-templates.md#add-the-template-roles) e [nós de divisão de caminho por pessoas da jornada](../journeys/split-merge-paths-nodes.md#people-path-filters).

![Acessar as definições de evento configuradas](./assets/most-engaged-buying-groups.png){width="550" zoomable="yes"}

>[!ENDSHADEBOX]

Qualquer atividade ponderada por envolvimento executada pelos membros do grupo de compra nos últimos 30 dias é usada para calcular as pontuações. Com a janela de 30 dias, as ocorrências de atividade expiram e as pontuações podem ser movidas para baixo (declínio de pontuação). As pontuações exibidas são arredondadas (por exemplo, uma pontuação de 75,89999 é exibida como 76).

## Atividades usadas para pontuação de engajamento

A pontuação do grupo de compras não é _baseada em acionamentos_. É um processo diário que avalia a atividade em todos os membros do grupo de compras e recalcula a pontuação. As atividades usam _pesos_ para informar a pontuação do grupo de compras de acordo com o modelo de ponderação ativa, que determina como cada atividade é ponderada.

Há um limite de frequência diário de 20 para cada atividade. Se um membro de um grupo de compras executar a mesma atividade mais de 20 vezes em um único dia, a contagem da atividade será limitada a 20.

| Nome da atividade | Descrição | Tipo de engajamento | Contagem máxima de frequência diária | Peso de atividade do modelo padrão |
|---------------|-------------|-----------------|---------------------------|-------------------------------|
| Participar de evento | Um membro participou de um evento | Evento | 20 | 60 |
| Email clicado | Um membro clica em um link em um email | Email | 20 | 30 |
| Email aberto | Um membro abre um email | Email | 20 | 30 |
| Formulário preenchido | Um membro preenche e envia um formulário em uma página da Web | Web | 20 | 40 |
| Momento interessante | Um membro tem um momento interessante | Preparado | 20 | 60 |
| Cliques de link | Um membro clica em um link em uma página da Web | Web | 20 | 40 |
| Page Views | Um membro exibe uma página da Web | Web | 20 | 40 |
| Inscrever-se em um evento | Um membro registrado para um evento | Evento | 20 | 60 |

<!-- old list

| Activity name | Description | Engagement type | Max daily frequency count | Activity weight |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visit Webpage]| A member visits a web page | Web | 20 | 40 |
| [!UICONTROL Fill Out Form]| A member fills and submits a form on a web page | Web | 20 | 40 |
| [!UICONTROL Click Link] | A member clicks a link on a web page | Web | 20 | 40 |
| [!UICONTROL Open Email] | A member opens an email | Email | 20 | 30 |
| [!UICONTROL Click Email] | A member clicks a link in an email | Email | 20 | 30 |
| [!UICONTROL Open Sales Email] | A member opens a sales email | Email | 20 | 30 |
| [!UICONTROL Click Sales Email] | A member clicks a link in a sales email | Email | 20 | 30 |
| [!UICONTROL Interesting Moment] | A member has an interesting moment | Curated | 20 | 60 |
| [!UICONTROL Tap Push Notification] | A member receives a push notification | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Activity] | A member performs an activity on a mobile app | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Session] | A member is active on a mobile app session | Mobile | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | A member fills and submits a Lead Ads form on a Facebook page | Social | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | A member clicks a personalized call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | A member views an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Tap In-App Message] | A member taps an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Subscribe SMS] | A member subscribes to SMS communications | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | A member replies to a sales email | Email | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | A member engages with a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | A member interacts with a document in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | A member schedules an appointment in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | A member reaches a goal in a Dynamic Chat dialogue |  |20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | A member responds to a poll in a webinar event | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | A member clicks a call-to-action link in a webinar event | Call | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | A member downloads a file/asset in a webinar event | Event | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | A member asks questions in a webinar event | Event | 20 | 60 |
| [!UICONTROL Has attended event] | A member attended an event | Event | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | A member engages with an agent in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | A member clicks a link in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | A member engages with a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | A member schedules an appointment in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | A member reaches a goal in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | A member interacts with a document in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | A member engages with an Agent in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | A member clicks a link in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | A member clicks a link in an SMS message | SMS | 20 | 90 | -->

>[!NOTE]
>
>As atividades de pontuação de engajamento são registradas no log de atividades do Marketo Engage de uma pessoa. Você pode acessar esse log na instância conectada do Marketo Engage. Para obter mais informações, consulte [Localizar o Log de Atividades de uma Pessoa](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} na documentação do Marketo Engage.

## Ponderação do modelo de função {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="Ponderação da função da pontuação de engajamento"
>abstract="Use a ponderação de função para personalizar o cálculo da pontuação de engajamento."

Os usuários podem atribuir _ponderação_ a cada função no [modelo de funções](./buying-groups-role-templates.md) para alocar pesos diferentes para uma função.

![Definir o peso para cada função no modelo de funções](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Cada nível de peso é convertido em um valor, que é usado para calcular a pontuação de engajamento:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Baixo] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Vital] = 100

Um modelo de funções com três funções de peso _[!UICONTROL Vital]_, _[!UICONTROL Importante]_ e _[!UICONTROL Normal]_ é convertido nas seguintes porcentagens de peso:

| Função | Peso | Valor do sistema | Cálculo de valor | Porcentagem |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Tomador de decisão | Vital | 100 | 100/240 | 41.67% |
| Influenciador | Importante | 80 | 80/240 | 33,33% |
| Profissional | Normal | 60 | 60/240 | 25% |
|               | Total | 240 |                   |           |

## Exemplo de cálculo de pontuação

O exemplo a seguir ilustra o cálculo da pontuação de engajamento. Ele usa a porcentagem de peso de função descrita, a contagem de atividades de entrada para cada membro do grupo de compra e um limite diário de 20 para cada ocorrência de evento.

| Função | Membro | Tipo de atividade | Contagem de ontem | Contagem de hoje | Cálculo | Pontuação total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Tomador de decisão | Adam | Site visitado | 37 | 15 | 20 + 15 | 35 |
|               |          | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Site visitado | 5 | 3 | 5 + 3 | 8 |
|               |          | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | PUB baixado | 3 | 2 | 3 + 2 | 5 |
| **Pontuação total de tomadores de decisão** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influenciador | John | Site visitado | 19 | 9 | 19 + 9 | 28 |
| **Pontuação total de influenciadores** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Profissional | Bob | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | Site visitado | 1 | 7 | 1 + 7 | 8 |
|               |          | PUB baixado | 1 | 2 | 1 + 2 | 3 |
| **Pontuação total de profissionais** |         |             |                 |             |      | **17** |

A pontuação final de engajamento é calculada aplicando o peso de cada uma das pontuações de função:

| Função | Pontuação total da função | % de peso da função | % de peso da pontuação X |
|-------------- |---------------- |------------- |---------------- |
| Tomadores de decisão | 52 | 41.67% | 21,67 |
| Influenciadores | 28 | 33,33% | 9,33 |
| Profissionais | 17 | 25% | 4,25 |
| **Pontuação final de engajamento** |                |             | **35,25** |

## Lógica de pontuação

Além da lógica de cálculo descrita no exemplo de cálculo, há uma normalização significativamente complexa das pontuações que ocorre no sistema, em todas as pessoas, grupos de compra e contas na sua instância. Uma pontuação de engajamento do grupo de compra depende das pontuações de engajamento da pessoa, de acordo com a seguinte lógica ordenada:

### Lógica de cálculo da pontuação de engajamento da pessoa

1. Identifique todos os tipos de atividades _ponderadas por engajamento_ que tenham um peso associado e uma cota diária, como visitas a sites, cliques em emails e participação em webinários.

1. Identifique todas as ações _ponderadas pelo envolvimento_ da pessoa executadas na janela de retrospectiva da atividade, que atualmente está embutida em código para 30 dias.

1. Normalize os pesos do tipo de atividade em todos os _pesos do tipo de atividade ponderados por engajamento_ identificados na etapa 1, ignorando os que não ocorreram na janela de retrospectiva.

   Esta etapa aproveita a _Normalização mín-máx_ e reduz significativamente a diluição artificial do peso do tipo de atividade para um locatário que não aproveita a maioria deles.

1. Aplicar a filtragem de cota diária por pessoa e tipo de atividade.

   Essa etapa atenua a possibilidade de valores atípicos muito grandes, evitando que atividades de valor mais baixo/alto volume desviem as pontuações.

1. Calcule a pontuação bruta de engajamento da pessoa somando a atividade diária por tipo de atividade, multiplicando-a pelo peso associado e somando os resultados de todos os dias da janela de retrospectiva.

1. Use uma transformação de _Transformação de Potência_ (Raiz Quadrada) para estabilizar a variação, reduzindo possíveis valores atípicos.

   Essas transformações ajudam a reduzir a distorção e a tornar os padrões nos dados mais lineares.

1. Aplique uma transformação adicional de _Normalização em Escala_ para garantir que as pontuações aproveitem todo o intervalo de 0 a 100.

### Lógica de cálculo da pontuação de engajamento do grupo de compra

1. Aplique um peso normalizado a cada membro do grupo de compra por função, de acordo com o peso configurado no modelo de funções.

1. Normalize o peso da função do grupo de compra para cada grupo de compra.

   Essa normalização evita diluição desnecessária do peso da função se um grupo de compra não usar todas as funções.

1. Agregar todas as pontuações de engajamento da pessoa do membro do grupo de compra multiplicando a pontuação de engajamento da pessoa pelo peso da função normalizada da pessoa e adicionando-as juntas.

1. Aplique uma transformação _Transformação de Energia_ (Raiz Quadrada) para estabilizar a variação, reduzindo possíveis valores atípicos, especialmente para grupos de compras muito grandes.

1. Aplique uma transformação adicional de _Normalização em Escala_ para garantir que as pontuações aproveitem todo o intervalo de 0 a 100.
