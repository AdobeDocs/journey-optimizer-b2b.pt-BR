---
title: Consultas do conjunto de dados
description: Saiba como usar exemplos de consulta SQL no Serviço de consulta para analisar dados de conta, grupo de compras, pessoa e jornada exportados pelo Adobe Journey Optimizer B2B Edition.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# Consultas do conjunto de dados

Encontre exemplos de consultas SQL prontas para uso para analisar os dados de conta, pessoa, grupo de compras e jornada que [!DNL Adobe Journey Optimizer B2B Edition] exporta para [!DNL Adobe Experience Platform]. Para relatar contas, grupos de compras, participação de email e atividade de jornada, execute as consultas em [!DNL Query Service].

Para obter descrições dos conjuntos de dados e campos usados nessas consultas, consulte [Conjuntos de dados exportados](./aep-exported-datasets.md).

## Pré-requisitos {#prerequisites}

Antes de executar qualquer consulta nesta página, verifique se você tem o seguinte:

* **Acesso a [!DNL Query Service]:** Você deve ter acesso ao [Serviço de Consulta](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/home){target="_blank"} em sua sandbox [!DNL Experience Platform].
* **Conjuntos de dados disponíveis:** as consultas têm como alvo os [!DNL Journey Optimizer B2B Edition] conjuntos de dados exportados. Na sandbox, vá para **[!UICONTROL Conjuntos de dados]** e verifique se os conjuntos de dados existem e contêm dados.
* **Valores de campo de esquema:** verifique se os campos nas suas consultas têm valores no esquema correspondente. Campos vazios não retornam resultados e não produzem erros.

>[!NOTE]
>
>Os exemplos usam nomes de tabela curtos, como `account_table` e `person_activity_table`. Substitua cada nome de tabela pelo nome do conjunto de dados correspondente na sandbox. Se o nome de um conjunto de dados contiver hifens, coloque-o entre aspas duplas. Substitua os valores de espaço reservado, como `Example Company` e `PASTE_COMPLETE_JOURNEY_ID_HERE`, pelos valores do seu ambiente.

## Executar uma consulta {#run}

Para executar qualquer exemplo nesta página:

1. Em [!DNL Experience Platform], selecione **[!UICONTROL Serviço de consulta]** > **[!UICONTROL consultas]**.
1. Cole o exemplo no editor de consultas e substitua os nomes da tabela e os valores do espaço reservado.
1. Selecione **[!UICONTROL Executar]**.

Os exemplos que filtram por data usam os últimos 30 dias. Para alterar o intervalo de tempo, edite o valor `INTERVAL '30' DAY`.

## Escolher uma consulta

Use a tabela a seguir para escolher uma consulta para sua tarefa de geração de relatórios.

| Eu quero | Ir para |
|---|---|
| Revisar nomes de contas, setores e locais | [Examinar detalhes da conta](#account-details) |
| Comparar grupos de compras por envolvimento | [Comparar o envolvimento com o grupo de compras](#buying-group-engagement) |
| Localizar as pessoas associadas a uma conta | [Localizar pessoas em uma conta](#account-people) |
| Rastrear alterações no status do grupo de compras | [Revisar alterações de status do grupo de compras](#buying-group-status-changes) |
| Localizar pessoas que clicaram em um email | [Localizar pessoas que clicaram em um email](#email-clicks) |
| Comparar atividades recentes por tipo | [Comparar atividades recentes de pessoas](#person-activity) |
| Comparar jornadas da conta por tamanho | [Comparar contagens de conta por jornada](#account-journey-counts) |
| Listar as contas em uma jornada | [Listar contas em uma jornada](#journey-accounts) |
| Rastrear a atividade diária de jornada na conta | [Rastrear atividade diária da conta](#account-daily-activity) |
| Investigar o histórico de uma conta em uma jornada | [Revisar uma linha do tempo de jornada de conta](#account-timeline) |
| Comparar jornadas de pessoas por tamanho e status | [Comparar contagens de pessoas por jornada](#person-journey-counts) |
| Listar as pessoas em uma jornada | [Listar pessoas em uma jornada](#journey-people) |
| Veja onde as pessoas estão em uma jornada | [Comparar contagens de pessoas por etapa](#person-step-counts) |
| Acompanhar atividade recente de jornada pessoal | [Rastrear atividade de jornada recente](#person-journey-activity) |
| Investigar o histórico de uma pessoa em uma jornada | [Revisar uma linha do tempo de jornada de pessoa](#person-timeline) |

## Consultas de conta e grupo de compra

Use essas consultas para revisar as contas, os grupos de compra e as pessoas disponíveis para relatórios.

### Revisar detalhes da conta {#account-details}

Analise nomes de contas, setores, locais e tamanhos da empresa para entender as contas disponíveis para relatórios.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### Comparar o engajamento do grupo de compras {#buying-group-engagement}

Comparar grupos de compras por pontuação de engajamento registrada, junto com integridade e interesse pela solução.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### Localizar pessoas em uma conta {#account-people}

Encontre as pessoas e cargos associados a uma conta para entender seus contatos. Substitua `Example Company` com um nome de conta da sua sandbox.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Revisar alterações de status do grupo de compras {#buying-group-status-changes}

Revise as alterações de status do grupo de compra nos últimos 30 dias para entender como os grupos mudam ao longo do tempo.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Consultas de engajamento da pessoa

Use essas consultas para analisar o engajamento no email e outras atividades registradas da pessoa.

### Localizar pessoas que clicaram em um email {#email-clicks}

Para analisar o engajamento recente com o email, identifique as pessoas com cliques de email registrados nos últimos 30 dias.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Comparar atividades recentes de pessoas {#person-activity}

Compare os tipos de atividades registrados e o número de pessoas envolvidas para entender o engajamento recente.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## Consultas de jornada de conta

Use essas consultas para analisar jornadas de conta. Substitua `PASTE_COMPLETE_JOURNEY_ID_HERE` pelo valor `_id` da jornada da conta e `PASTE_COMPLETE_ACCOUNT_ID_HERE` pelo valor `_id` da conta.

### Comparar contagens de conta por jornada {#account-journey-counts}

Compare as jornadas de conta por status e contagem de associação registrada para ver quais jornadas têm as maiores populações de contas.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### Listar contas em uma jornada {#journey-accounts}

Revise as contas associadas a uma jornada específica, incluindo seus setores e países.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### Rastrear atividades diárias da conta {#account-daily-activity}

Acompanhe adições diárias de conta, remoções e alterações de etapa para entender a atividade em uma jornada nos últimos 30 dias.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### Revisar uma linha do tempo de jornada de conta {#account-timeline}

Investigue o histórico de jornadas recente de uma conta revisando seus eventos gravados e as etapas de jornada.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Consultas de jornada de pessoa

Use essas consultas para analisar jornadas de pessoas. Substitua `PASTE_COMPLETE_JOURNEY_ID_HERE` pelo valor `_id` da jornada de pessoa e `PASTE_COMPLETE_PERSON_ID_HERE` pelo valor `_id` da pessoa.

### Comparar contagens de pessoas por jornada {#person-journey-counts}

Compare as jornadas de pessoas por contagem de associação registrada, status e datas para entender seu tamanho e ciclo de vida.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### Listar pessoas em uma jornada {#journey-people}

Revise quem está associado a uma jornada, quando ela foi inserida pela última vez e com que frequência ela foi inserida.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### Comparar contagens de pessoas por etapa {#person-step-counts}

Veja como as pessoas são distribuídas pelas etapas registradas em suas associações de jornada.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### Rastrear atividade de jornada recente {#person-journey-activity}

Compare os inícios, os términos e as transições da jornada registrada para entender a atividade da pessoa em uma jornada nos últimos 30 dias.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### Revisar uma linha do tempo de jornada de pessoa {#person-timeline}

Investigue o histórico de jornadas recente de uma pessoa, incluindo transições de etapas, escolhas divididas e atualizações de perfil atribuídas pela jornada.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
