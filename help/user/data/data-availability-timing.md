---
title: Disponibilidade de dados e tempo de sincronização
description: Saiba com que rapidez as alterações de dados aparecem nas jornadas do [!DNL Journey Optimizer B2B Edition] e quais linhas do tempo são normais.
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# Disponibilidade de dados e tempo de sincronização {#data-availability}

Use este tópico para entender rapidamente as alterações de dados aparecem nas jornadas do [!DNL Adobe Journey Optimizer B2B Edition] e quais linhas do tempo são normais. Conhecer o tempo esperado ajuda a projetar as jornadas de acordo e a reconhecer quando um atraso é o comportamento esperado.

## Tempos de espera esperados

| Tipo de dados | Disponibilidade típica |
| --- | --- |
| [Associação de público-alvo](#daily-refresh) | Até 24 horas (ciclo diário) |
| [Alterações no relacionamento entre conta e pessoa](#daily-refresh) | Até 24 horas (ciclo diário) |
| [Dados de [!DNL Experience Platform] a [!DNL Journey Optimizer B2B Edition]](#platform-sync) | Até 30 minutos (tempo quase real) |
| [Dados de [!DNL Journey Optimizer B2B Edition] a [!DNL Experience Platform]](#platform-sync) | Até quatro horas (microlotes) |
| [Eventos de atividade, como cliques e aberturas](#activity-and-actions) | Até quatro horas |
| [[!DNL Marketo Engage] adicionar ou remover lista](#activity-and-actions) | Em 30 minutos (tempo quase real) |
| [Eventos gerados pelo Journey Optimizer B2B Edition](#activity-and-actions) | Pode ser usado somente em públicos-alvo em lote |
| [População de público-alvo do LinkedIn](#linkedin-timing) | Mesmo dia a 36-40 horas (pior caso) |

## Dados de público-alvo e relacionamento {#daily-refresh}

[!DNL Journey Optimizer B2B Edition] avalia a associação à conta e a pessoas uma vez por dia, acionada por um agendador de trabalhos em lotes. Como resultado:

* Contas ou pessoas que se qualificaram recentemente para um público-alvo se qualificam para inserir uma jornada dentro de 24 horas após a qualificação.
* As alterações nos critérios de público-alvo entrarão em vigor no próximo ciclo diário de avaliação.
* Se uma conta se qualificou para um público-alvo hoje, mas ainda não entrou na jornada, aguarde até que o próximo ciclo diário seja concluído antes de investigar.
* Quando a associação de conta de uma pessoa é alterada, por exemplo, quando um contato é movido para uma conta diferente, a atualização do relacionamento se propaga dentro de 24 horas por meio do ciclo de sincronização diário. As jornadas que dependem da associação à conta refletem a relação atualizada após o próximo ciclo diário. Nenhuma ação é necessária.

>[!TIP]
>
>Crie jornadas entendendo que a associação de público-alvo é atualizada diariamente, não em tempo real. Se você precisar de respostas quase em tempo real, use [acionadores baseados em eventos](../journeys/listen-for-event-nodes.md) em vez da entrada baseada em público-alvo.

## Sincronização de dados com [!DNL Experience Platform] {#platform-sync}

[!DNL Experience Platform] é o armazenamento de dados principal de contas, pessoas e oportunidades, e [!DNL Journey Optimizer B2B Edition] possui jornadas, grupos de compras e funções de grupos de compras. [Saiba mais sobre a arquitetura](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

Os dados se movem entre os dois sistemas em cada direção em um ritmo diferente:

* **[!DNL Experience Platform]a[!DNL Journey Optimizer B2B Edition]** - Sincronizações de dados em tempo quase real, que podem levar até 30 minutos.
* **[!DNL Journey Optimizer B2B Edition]a[!DNL Experience Platform]** - Sincronizações de dados em microlotes e podem levar até 4 horas.

## Eventos de atividade e ações de jornada {#activity-and-actions}

O tempo para dados de atividade e ações de jornada depende de como os dados se movem entre sistemas:

* **Dados da atividade** - Os registros de atividade da pessoa, como aberturas de email, cliques em links e preenchimentos de formulário, podem levar aproximadamente quatro horas para serem exibidos em [!DNL Journey Optimizer B2B Edition]. Esse tempo se aplica aos dados de atividade em lote; os acionadores de Evento de Experiência [!DNL Experience Platform] usam dados de fluxo e podem reagir em tempo quase real.
* **[!DNL Marketo Engage]ações** - as ações de Jornada que chamam [!DNL Marketo Engage] são quase em tempo real porque são chamadas de API. Por exemplo, quando uma etapa de jornada adiciona ou remove uma pessoa de uma lista [!DNL Marketo], a ação normalmente é concluída em 30 minutos. [Saiba mais sobre ações de jornada](../journeys/action-nodes.md).
* **Ações que passam por[!DNL Experience Platform]** - Qualquer ação que retorne a [!DNL Experience Platform] primeiro é agrupada em lote, portanto, está sujeita ao tempo em lote, em vez de ao tempo quase real.
* **Eventos gerados por[!DNL Journey Optimizer B2B Edition]** - Eventos que [!DNL Journey Optimizer B2B Edition] gera em [!DNL Experience Platform] só podem ser usados em públicos em lote.

## [!DNL LinkedIn] destinos de público {#linkedin-timing}

Se sua jornada incluir uma ação de destino [!DNL LinkedIn], espere a seguinte linha do tempo depois de publicar a jornada.

| Cenário | Espera esperada |
| --- | --- |
| As contas já estavam no público quando a jornada foi publicada | Mesmo dia, se o processamento for concluído antes da meia-noite, horário local |
| Contas recebidas após a publicação da jornada | Até 24 horas |
| Contas recebidas após a primeira janela de sincronização diária | Até 36 a 40 horas |

[!DNL LinkedIn] contagem de público-alvo pode não ser atualizado imediatamente. Esse atraso é esperado enquanto o [!DNL Experience Platform] processa e entrega o arquivo de público-alvo para [!DNL LinkedIn]. Se a contagem de público-alvo ainda for 0 após 48 horas, investigue. [Saiba mais sobre os Públicos Correspondentes à Conta do LinkedIn](./linkedin-account-matched-audiences.md).
