---
title: Conjuntos de dados do Experience Platform exportados
description: Referência para os nomes dos conjuntos de dados e caminhos de campos-chave do Adobe Experience Platform exportados pelo Adobe Journey Optimizer B2B Edition.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 7%
---

# [!DNL Experience Platform] conjuntos de dados exportados

[!DNL Adobe Journey Optimizer B2B Edition] disponibiliza as informações de conta, pessoa, grupo de compras e jornada em [!DNL Adobe Experience Platform]. Um conjunto de dados é uma coleção de registros relacionados. Por exemplo, um conjunto de dados de pessoa descreve pessoas, um conjunto de dados de associação conecta pessoas a contas ou jornadas e um conjunto de dados de evento registra ações como abrir um email.

Use este guia para entender o que cada conjunto de dados contém, o que significam seus campos e como os registros relacionados se conectam. Os nomes dos conjuntos de dados seguem este padrão:

**`AJOB2B-<datasetVersion>-<entity>`**

Aqui, `<entity>` descreve as informações, como `person`, `account_relational` ou `person_event`. `<datasetVersion>` identifica a versão das definições de campo do conjunto de dados. Os cabeçalhos de seção mostram os nomes documentados; seu ambiente [!DNL Experience Platform] também pode conter versões mais antigas.

Para obter a configuração de namespace e esquema que oferece suporte a essas exportações, consulte [namespaces e esquemas B2B](./namespaces-schemas.md).

>[!NOTE]
>
>O Adobe retém versões mais antigas do conjunto de dados para evitar a interrupção do uso existente. Como resultado, você pode encontrar várias versões do mesmo conjunto de dados na sandbox. Se você não usar mais um conjunto de dados mais antigo, poderá solicitar que a Adobe o remova. Antes de solicitar a remoção, confirme se o conjunto de dados não está mais em uso.

## Lendo este guia

- **Nome do campo:** o nome exato que você vê em [!DNL Experience Platform]. Pontos separam níveis dentro de um campo, como `consents.marketing.email.val`.
- **ID do Registro:** identifica o registro nesse conjunto de dados.
- **Relacionamento:** nomeia o conjunto de dados e o campo correspondentes ao identificador. Por exemplo, `Matches AJOB2B-1_5_4-buying_group (_id)` significa que o campo se refere ao `_id` de um grupo de compra. Corresponder ao identificador completo; não o encurte nem tente recriá-lo.
- **Formato padrão Adobe:** usa as definições de campo compartilhado do Adobe.
- **Formato de registro relacionado:** organiza as informações como registros que você pode conectar usando identificadores correspondentes.

Por exemplo, `buying_group_member.buyingGroupID` corresponde a `buying_group._id`, e seu `personID` corresponde a `person_relational._id` ou ao conjunto de dados de Pessoa `personKey.sourceKey`. Esses links ajudam você a entender quem pertence a um grupo de compra. [!DNL Experience Platform] não cria automaticamente relatórios ou públicos-alvo somente com os links.

Alguns identificadores se referem a informações que não têm conjunto de dados separado neste guia, como um programa de marketing. A coluna Relacionamento observa isso em vez de nomear um conjunto de dados que não existe aqui.

`isDeleted` é `true` quando o registro está marcado como excluído e `false` quando não está. Não o trate como um membro ativo geral ou indicador de consentimento. `lastUpdatedDate` descreve a última atualização de dados do registro; para eventos, use `timestamp` para entender quando a atividade aconteceu. Um campo em branco significa que as informações não estão disponíveis ou não se aplicam a esse registro.

Os conjuntos de dados de registros relacionados usam a versão `1_5_4`. Quando um campo não estiver preenchido no momento ou precisar de manuseio especial, a seção relevante explica a limitação visível ao cliente.

Um público-alvo é um grupo de pessoas que atendem aos critérios selecionados. A disponibilidade para criação de público-alvo depende da configuração do [!DNL Experience Platform] para combinar informações em perfis de pessoas. A presença de um conjunto de dados em [!DNL Experience Platform], por si só, não significa que ele esteja disponível para segmentação.

## Escolha de um conjunto de dados

| O que você quer entender | Conjuntos de dados a serem procurados |
|---|---|
| Pessoas e suas preferências de email | `person` |
| Detalhes da conta e detalhes de contato da pessoa | `account_relational`, `person_relational` |
| Quais pessoas estão associadas a uma conta | `account_member`, `account_person` |
| Grupos de compras, seus membros e alterações de status | `buying_group`, `buying_group_member`, `buying_group_event` |
| Jornadas de conta e contas participantes | `account_journey`, `account_journey_member`, `account_event` |
| Jornadas de pessoas e pessoas participantes | `person_journey`, `person_journey_member` |
| Etapas em uma jornada | `account_journey_node`, `person_journey_node`, `journey_node` |
| Email, Web e outras atividades de pessoas suportadas | `person_event`, `person_event_relational` |

As seções a seguir fornecem os nomes completos dos conjuntos de dados e detalhes dos campos. Uma jornada descreve a experiência em geral; uma associação conecta uma pessoa ou conta a essa jornada; um evento descreve algo que aconteceu.

+++Diagrama de relação de entidade

![Diagrama de relacionamento de entidade para conjuntos de dados exportados para [!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg)

+++

## `AJOB2B-1_5_1-person`

Cada registro descreve uma pessoa, seus identificadores e sua preferência de marketing por email. Use-o para relatórios no nível da pessoa e, quando Perfil estiver configurado, para ajudar a criar públicos-alvo.

**Formato:** Formato Adobe padrão

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `personID` | ID do registro | Identificador da pessoa. Use o valor completo para corresponder registros relacionados. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `identityMap` |  | Outros identificadores que ajudam [!DNL Experience Platform] a reconhecer a mesma pessoa nos dados conectados. |
| `consents.marketing.email.val` |  | Preferência de marketing por email: `n` indica uma opção de não participação; `y` indica nenhuma opção de não participação registrada neste campo. Este campo sozinho não estabelece permissão para enviar email de marketing. |
| `consents.marketing.email.time` |  | Data e hora da última atualização da preferência de email. |
| `consents.marketing.email.reason` |  | Motivo da recusa, quando fornecido (definido somente quando cancelado). |
| `isDeleted` |  | Se este registro de pessoa está marcado como excluído. |

>[!NOTE]
>
>Sua organização pode ter campos de pessoa adicionais além daqueles listados aqui.

Quando sua organização usa sua própria conta configurada ou conjuntos de dados de pessoa, esses registros também podem incluir `isDeleted`. Consulte [Conjuntos de dados de propriedade do cliente](#customer-owned-datasets).

## `AJOB2B-1_5_4-account_member`

Cada registro vincula uma conta a uma pessoa. Use esse conjunto de dados para relatar quais pessoas estão associadas a cada conta; ele descreve a relação em vez de ambos os perfis.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro do relacionamento. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador da conta. |
| `personID` | Corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de pessoa. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-buying_group`

Cada registro descreve um grupo de compras associado a uma conta, incluindo nome, status, interesse na solução e pontuações de engajamento e integridade. O estágio de grupo de compras não está preenchido no momento.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro do grupo de compras (use o valor completo). |
| `buyingGroupName` |  | Nome do grupo de compras. |
| `engagementScore` |  | Pontuação de envolvimento. |
| `completenessScore` |  | Pontuação de integridade. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de conta relacionado. |
| `solutionInterest` |  | Rótulo de interesse da solução. |
| `buyingGroupStatus` |  | Status. |
| `buyingGroupStage` |  | Nome do estágio de grupo de compras. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

>[!NOTE]
>
>**Observação sobre disponibilidade:** `buyingGroupStage` está em branco no momento. Não o use para filtrar ou agrupar grupos de compras por estágio.

## `AJOB2B-1_5_4-buying_group_member`

Cada registro vincula uma pessoa a um grupo de compra e registra a função dessa pessoa. Use-o para relatar a composição do grupo de compras e a cobertura da função.

`isDeleted` nem sempre indica se uma pessoa foi removida de um grupo de compra. Não use este campo sozinho para determinar a associação atual. O nome da função pode ficar em branco quando nenhuma informação de função estiver disponível.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro de associação. |
| `buyingGroupID` | Corresponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador do grupo de compras. |
| `personID` | Corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de pessoa. |
| `buyingGroupMemberRole` |  | Nome da função, quando disponível. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_journey`

Cada registro descreve uma jornada de conta, com seu nome, status e datas de início e término. Use-o para relatar o ciclo de vida e o status da jornada das contas.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro de Jornada (use o valor completo). |
| `accountJourneyName` |  | Nome da jornada. |
| `accountJourneyStatus` |  | Status (por exemplo, rascunho, ativo, concluído). |
| `startDate` |  | Carimbo de data e hora inicial. |
| `endDate` |  | Carimbo de data e hora final. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_journey_member`

Cada registro conecta uma conta a uma jornada de conta. Use-o para identificar e relatar quais contas estão participando de cada jornada.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro de associação. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador da conta. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de jornada da conta. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-person_journey`

Cada registro descreve uma jornada de pessoa, com seu nome, status e datas de início e término. Use-o para relatar o ciclo de vida e o status da jornada para jornadas com foco em pessoas.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro de Jornada (use o valor completo). |
| `personJourneyName` |  | Nome da jornada. |
| `personJourneyStatus` |  | Status (por exemplo, rascunho, ativo, concluído). |
| `startDate` |  | Carimbo de data e hora inicial. |
| `endDate` |  | Carimbo de data e hora final. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-person_journey_member`

Cada registro descreve a associação de uma pessoa em uma jornada, incluindo o nó atual da jornada, as datas de associação e entrada e a contagem de entradas. Use-o para relatar o andamento da inscrição, da reentrada e da jornada.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro de associação. |
| `marketingProgramID` |  | Identificador do programa de marketing ao qual a jornada pertence. |
| `personID` | Corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de pessoa. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó de jornada em que a pessoa está no momento. |
| `membershipDate` |  | Quando a pessoa se tornou membro do programa de marketing. |
| `lastEntryDate` |  | Quando a pessoa entrou na jornada pela última vez. |
| `reentryOpensAt` |  | Quando a pessoa pode entrar novamente na jornada. |
| `entryCount` |  | Contagem de vezes que a pessoa entrou na jornada. |
| `createdDate` |  | Quando o registro foi criado. |
| `updatedDate` |  | Quando o registro foi alterado pela última vez. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_journey_node`

Cada registro descreve uma etapa em uma jornada, incluindo o tipo de etapa e a jornada à qual ela pertence. Um nó de jornada é uma etapa, como iniciar, aguardar ou tomar uma decisão. As mesmas etapas podem aparecer em `person_journey_node`; corresponda `accountJourneyID` a uma jornada de conta antes de tratar uma etapa como específica da conta.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID de registro do nó (use o valor completo). |
| `accountJourneyID` | Corresponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador da jornada pai. |
| `uuid` |  | Identificador adicional da etapa de jornada. |
| `journeyNodeTypeID` |  | Número que identifica o tipo de etapa de jornada. |
| `nodeType` |  | Rótulo que identifica o tipo de etapa de jornada. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `createdDate` |  | Quando o registro foi criado. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-person_journey_node`

Cada registro descreve uma etapa em uma jornada, incluindo o tipo de etapa e a jornada à qual ela pertence. As mesmas etapas podem aparecer em `account_journey_node`; corresponda `personJourneyID` a uma jornada de pessoa antes de tratar uma etapa como específica da pessoa.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID de registro do nó (use o valor completo). |
| `personJourneyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador da jornada pai. |
| `uuid` |  | Identificador adicional da etapa de jornada. |
| `journeyNodeTypeID` |  | Número que identifica o tipo de etapa de jornada. |
| `nodeType` |  | Rótulo que identifica o tipo de etapa de jornada. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `createdDate` |  | Quando o registro foi criado. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_event`

Cada registro captura um evento de jornada de conta: uma conta que está sendo adicionada ou removida de uma jornada ou que está se movendo entre nós de jornada. Use `eventType` e `timestamp` para criar uma linha do tempo de atividade de conta; `buyingGroupID` está disponível quando o evento é atribuído a grupos de compra.

**Formato:** Formato de registro relacionado

`eventType` fornece informações sobre o que aconteceu. As tabelas a seguir descrevem os campos para cada tipo de atividade.

`lastUpdatedDate` não está preenchido no momento para esses eventos. Use `timestamp` para a data da atividade.

### Conta adicionada a uma jornada (`account.addAccountToJourney`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador da conta. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `buyingGroupID` | Corresponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador do grupo de compras, quando a adição da jornada é atribuída ao grupo de compras. |
| `lastUpdatedDate` |  | Tempo de atualização do registro. Atualmente em branco; use carimbo de data e hora para a data da atividade. |

### Conta removida de uma jornada (`account.removeAccountFromJourney`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador da conta. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `buyingGroupID` | Corresponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador do grupo de compras, quando a remoção da jornada é atribuída ao grupo de compras. |
| `lastUpdatedDate` |  | Tempo de atualização do registro. Atualmente em branco; use carimbo de data e hora para a data da atividade. |

### Conta movida entre etapas do jornada (`account.changeAccountJourneyNode`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador da conta. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `previousJourneyNodeID` | Refere-se a `AJOB2B-1_5_4-account_journey_node` (`_id`); os valores podem não corresponder | Identificador da etapa de jornada anterior. Este valor pode não corresponder ao registro de etapa correspondente; não dependa dele sozinho para conectar registros. |
| `buyingGroupID` | Corresponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador do grupo de compras, quando a alteração de nó é atribuída ao grupo de compras. |
| `lastUpdatedDate` |  | Tempo de atualização do registro. Atualmente em branco; use carimbo de data e hora para a data da atividade. |

## `AJOB2B-1_5_4-buying_group_event`

Cada registro captura uma alteração no status de um grupo de compras, incluindo o novo status e quando ele foi alterado. O campo new-stage não está preenchido no momento.

**Formato:** Formato de registro relacionado

### Status do grupo de compras alterado (`buyingGroup.changeStatus`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `buyingGroupID` | Corresponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador do grupo de compras. |
| `newStatus` |  | Novo valor de status. |
| `newStage` |  | Nova fase de grupo de compra. Atualmente em branco. |
| `lastUpdatedDate` |  | Tempo de atualização do registro. |

>[!NOTE]
>
>**Observação sobre disponibilidade:** use `newStatus` para relatar alterações de status. Não use `newStage` para reportar alterações de estágio, pois ele está em branco.

## `AJOB2B-1_5-person_event`

Cada registro descreve um evento da Web, de email ou de outra atividade compatível. Use `eventType` e `timestamp` para analisar o comportamento ao longo do tempo, com detalhes específicos do evento preenchidos somente para o tipo de evento correspondente.

**Formato:** Formato Adobe padrão

`eventType` informa o que aconteceu. As tabelas a seguir descrevem os campos para cada tipo de atividade. Os detalhes que não se aplicam a um evento ficam em branco.

### Email enviado (`directMarketing.emailSent`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.emailSent.mailingName` |  | Nome da mala direta. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

### Email entregue (`directMarketing.emailDelivered`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

### Cancelar inscrição de email (`directMarketing.emailUnsubscribed`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

### Email aberto (`directMarketing.emailOpened`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |
| `device.isMobileDevice` |  | Se um dispositivo móvel foi gravado para a atividade. |
| `device.model` |  | Informações do dispositivo ou do cliente de email. |
| `environment.browserDetails.userAgent` |  | Informações do navegador ou do cliente de email. |
| `environment.operatingSystem` |  | Sistema operacional. |

### Link de email clicado (`directMarketing.emailClicked`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `directMarketing.linkURL` |  | URL do link clicado. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |
| `device.isMobileDevice` |  | Se um dispositivo móvel foi gravado para a atividade. |
| `device.model` |  | Informações do dispositivo ou do cliente de email. |
| `environment.browserDetails.userAgent` |  | Informações do navegador ou do cliente de email. |
| `environment.operatingSystem` |  | Sistema operacional. |

### Email rejeitado (`directMarketing.emailBounced`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `directMarketing.emailBouncedCode` |  | Categoria/código de rejeição. |
| `directMarketing.emailBouncedDetails` |  | Texto detalhado. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

### Rejeição temporária de email (`directMarketing.emailBouncedSoft`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID do ativo de mala direta. |
| `directMarketing.mailingKey.sourceType` |  | Nome do produto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID da instância. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo do conteúdo do email. |
| `directMarketing.mailingName` |  | Nome da mala direta. |
| `directMarketing.email` |  | Endereço de email. |
| `directMarketing.emailBouncedCode` |  | Categoria/código de rejeição. |
| `directMarketing.emailBouncedDetails` |  | Texto detalhado. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

### Página da Web exibida (`web.webpagedetails.pageViews`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `web.webPageDetails.webPageKey.sourceID` |  | ID do ativo da página. |
| `web.webPageDetails.webPageKey.sourceType` |  | Nome do produto conectado. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | ID da instância. |
| `web.webPageDetails.webPageKey.sourceKey` |  | Identificador de página completo. |
| `web.webPageDetails.name` |  | Nome da página. |
| `web.webPageDetails.URL` |  | URL da página. |
| `web.webPageDetails.queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `web.webPageDetails.webPageID` |  | ID da página. |
| `environment.browserDetails.userAgent` |  | Informações do navegador ou do cliente de email. |
| `web.webReferrer.URL` |  | URL do referenciador. |

### Link da Web clicado (`web.webinteraction.linkClicks`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `web.webInteraction.webInteractionKey.sourceID` |  | ID do ativo de interação. |
| `web.webInteraction.webInteractionKey.sourceType` |  | Nome do produto conectado. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | ID da instância. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | Identificador completo de interação. |
| `web.webInteraction.linkID` |  | ID do link. |
| `web.webInteraction.linkURL` |  | URL de destino. |
| `web.webPageDetails.queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `web.webPageDetails.webPageID` |  | ID da página. |
| `environment.browserDetails.userAgent` |  | Informações do navegador ou do cliente de email. |
| `web.webReferrer.URL` |  | URL do referenciador. |

### Formulário enviado (`web.formFilledOut`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `web.fillOutForm.webFormKey.sourceID` |  | ID do ativo de formulário. |
| `web.fillOutForm.webFormKey.sourceType` |  | Nome do produto conectado. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | ID da instância. |
| `web.fillOutForm.webFormKey.sourceKey` |  | Preencha o identificador do formulário. |
| `web.fillOutForm.webFormID` |  | ID do formulário. |
| `web.fillOutForm.webFormName` |  | Nome do formulário. |
| `web.webPageDetails.queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `web.webPageDetails.webPageID` |  | ID da página. |
| `environment.browserDetails.userAgent` |  | Informações do navegador ou do cliente de email. |
| `web.webReferrer.URL` |  | URL do referenciador. |

### Momento interessante registrado (`leadOperation.interestingMoment`)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `personID` | Corresponde a `AJOB2B-1_5_1-person` (`personID`) | Identificador de pessoa. |
| `personKey.sourceID` |  | Identificador de pessoa no sistema conectado. |
| `personKey.sourceType` |  | Nome do produto conectado. |
| `personKey.sourceInstanceID` |  | Identificador do ambiente [!DNL Experience Platform] ou da conta conectada. |
| `personKey.sourceKey` |  | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `leadOperation.interestingMoment.date` |  | Data/hora do momento. |
| `leadOperation.interestingMoment.description` |  | Descrição |
| `leadOperation.interestingMoment.source` |  | Nome do produto ou campanha relacionada. |
| `leadOperation.interestingMoment.type` |  | Rótulo de tipo. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID da jornada (se atribuída). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Jornada a ID do nó (se atribuída). |

## `AJOB2B-1_5_4-journey_node`

Cada registro descreve uma etapa de jornada, a jornada à qual pertence e o tipo de etapa. As mesmas etapas podem aparecer nos conjuntos de dados da etapa de jornada de conta e pessoa. Corresponder `journeyID` à jornada apropriada; não conte uma etapa mais de uma vez porque ela aparece em vários conjuntos de dados.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID de registro do nó (use o valor completo). |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-account_journey` ou `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador da jornada pai. |
| `nodeType` |  | Tipo de etapa de jornada, como início, término, espera ou decisão. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_relational`

Cada registro descreve uma conta, incluindo detalhes da organização, local, tamanho, receita e campos personalizados. Use essas informações para adicionar o contexto da conta aos relatórios de grupos de compras e de jornadas.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID do registro da conta (use o valor completo). |
| `accountName` |  | Nome da conta. |
| `industry` |  | Classificação do setor. |
| `country` |  | País. |
| `sicCode` |  | Código da Classificação Industrial Padrão. |
| `domainName` |  | Domínio primário da Web. |
| `primaryEmailDomain` |  | Domínio de email principal. |
| `street` |  | Endereço. |
| `city` |  | Cidade. |
| `state` |  | Estado ou região. |
| `postalCode` |  | CEP/código postal. |
| `region` |  | Região geográfica. |
| `phoneNumber` |  | Número de telefone. |
| `logoUrl` |  | URL do logotipo da conta. |
| `annualRevenue` |  | Receita anual. |
| `numberOfEmployees` |  | Número de funcionários. |
| `createdDate` |  | Quando o registro foi criado. |
| `sourceType` |  | Nome do sistema conectado que identifica a conta. |
| `sourceInstanceID` |  | Identificador da organização ou conta nesse sistema conectado. |
| `sourceID` |  | Identificador da conta nesse sistema conectado. |
| `customAttributes` |  | Nomes e valores de campos personalizados armazenados juntos como texto. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-person_relational`

Cada registro descreve uma pessoa, incluindo suas informações de contato, detalhes do cargo, identificadores e campos personalizados. Use-a para adicionar informações da pessoa aos relatórios de associação, jornada e atividade.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador de pessoa completo usado para corresponder a registros relacionados. |
| `email` |  | Endereço de email. |
| `firstName` |  | Nome. |
| `middleName` |  | Nome do meio. |
| `lastName` |  | Sobrenome. |
| `jobTitle` |  | Cargo. |
| `personType` |  | Tipo de pessoa: contato, cliente potencial ou lead pendente. |
| `isLead` |  | Se a pessoa é um cliente em potencial. |
| `isAnonymous` |  | Se a pessoa é anônima. |
| `salutation` |  | Saudação ou honorífico. |
| `phone` |  | Número de telefone principal. |
| `mobile` |  | Número do celular. |
| `sourceType` |  | Nome do sistema conectado que identifica a pessoa, como [!DNL Marketo Engage]. |
| `sourceInstanceID` |  | Identificador da organização ou conta nesse sistema conectado. |
| `sourceID` |  | Identificador de pessoa nesse sistema conectado. |
| `identityNamespace` |  | Rótulo que identifica o tipo de identificador de pessoa adicional. |
| `identityValue` |  | Valor da identidade secundária. |
| `customAttributes` |  | Nomes e valores de campos personalizados armazenados juntos como texto. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-account_person`

Cada registro vincula um perfil de conta a um perfil de pessoa. Use-a para relatar relacionamentos entre os conjuntos de dados de conta e perfil de pessoa.

**Formato:** Formato de registro relacionado

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | ID de registro de relacionamento conta-pessoa (use o valor completo). |
| `accountID` | Corresponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de conta completo (referências `account_relational._id`). |
| `personID` | Corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de pessoa completo (referências `person_relational._id`). |
| `createdDate` |  | Quando a relação conta-pessoa foi criada. |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

## `AJOB2B-1_5_4-person_event_relational`

Cada registro descreve uma atividade de pessoa suportada, como visualizar uma página da Web, interagir com um email ou percorrer uma jornada. Use `eventType` e `activityTypeID` para entender o que aconteceu. Somente os detalhes relevantes para esse tipo de atividade são preenchidos.

**Formato:** Formato de registro relacionado

A lista de campos a seguir abrange todos os tipos de atividades compatíveis. Um registro individual contém apenas os detalhes que se aplicam à atividade.

>[!NOTE]
>
>**Disponibilidade:** algumas atividades podem ter um `_id` em branco. Não suponha que cada atividade tenha um identificador de registro utilizável. O conjunto de dados não é uma garantia de um histórico completo de atividades.

Os detalhes da jornada (`journeyID`, `journeyNodeID`, `journeyStepID` e campos semelhantes) são fornecidos para atividades de jornada (`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) e para atividades de `person.attributeChanged` associadas a uma etapa de jornada &quot;Atualizar perfil de pessoa&quot;.

Os campos de alteração de atributo (`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`) são preenchidos somente para `person.attributeChanged`.

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id` | ID do registro | Identificador da atividade, quando disponível. |
| `timestamp` |  | Quando a atividade ocorreu. |
| `eventType` |  | Rótulo da atividade. Valores: `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`. |
| `activityTypeID` |  | Código da atividade. Use-o com `eventType` para distinguir atividades que compartilham o mesmo rótulo de evento. |
| `personID` | Corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de pessoa completo usado para corresponder a atividade a um registro de pessoa. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Preencha o identificador da jornada. Em branco para atividades não associadas a uma jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador de etapa de jornada completo. Em branco para atividades não associadas a uma jornada. |
| `previousJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nó de jornada anterior (preenchido para `person.journeyNodeTransition` e `person.journeySplitNode`). |
| `newJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID do nó de jornada de destino (`person.journeyNodeTransition` e `person.journeySplitNode`). Geralmente é igual a `journeyNodeID`. |
| `journeyStepID` |  | Identificador da etapa de jornada associada à atividade. |
| `journeyChoiceNumber` |  | Número de opção dividida para `person.journeySplitNode`. Registrado como um número inteiro. |
| `journeyEntryCount` |  | Número de vezes que essa pessoa inseriu a jornada (preenchida em jornada adicionar / iniciar eventos). Registrado como um número inteiro. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Identificador do programa de marketing associado à atividade de jornada. |
| `activitySource` |  | Nome do produto ou ação associado à atividade. |
| `campaignID` |  | [!DNL Marketo Engage] ID da campanha quando a atividade é atribuída à campanha. |
| `attributeName` |  | Nome do campo que foi alterado (`person.attributeChanged` somente). |
| `attributeID` |  | Identificador do campo alterado (`person.attributeChanged` somente). |
| `attributeNewValue` |  | Novo valor de campo, registrado como texto (`person.attributeChanged` somente). |
| `attributeOldValue` |  | Valor de campo anterior, registrado como texto (`person.attributeChanged` somente). |
| `attributeChangeReason` |  | Rótulo de motivo da alteração (somente `person.attributeChanged`). |
| `assetID` |  | Identificador do conteúdo de email, página ou formulário relacionado. |
| `assetName` |  | Nome do conteúdo relacionado. |
| `recipientEmail` |  | Endereço de email do destinatário, quando disponível. Preenchido somente para códigos de atividade **27** (rejeição temporária) e **48** (rejeição temporária de email de vendas); em branco para outras atividades de email. Para essas atividades, procure o registro de pessoa usando `personID`. `assetName` identifica o conteúdo do email, não o endereço do destinatário. |
| `bouncedCode` |  | Código de categoria de rejeição (somente emailBounce/emailBounceSoft). |
| `bouncedDetails` |  | Motivo detalhado da rejeição (somente emailBounce/emailBounceSoft). |
| `isMobileDevice` |  | Se um dispositivo móvel foi gravado para um email aberto ou clique. |
| `deviceModel` |  | Modelo do dispositivo (somente emailOpened/emailClicked). |
| `operatingSystem` |  | Sistema operacional (somente emailOpened / emailClicked). |
| `userAgent` |  | Informações do navegador ou cliente de email, para aberturas de email, cliques de email e atividades da Web. |
| `clickedLinkUrl` |  | URL do link de email clicado (somente emailClicked). |
| `webPageUrl` |  | URL da página da Web (`web.webpagedetails.pageViews` somente). |
| `queryParameters` |  | Informações adicionais em um endereço da Web, para exibições de página, envios de formulários ou cliques em links da Web. |
| `webPageID` |  | ID da página da Web [!DNL Marketo Engage] (pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | URL do referenciador (pageViews, formFilledOut, linkClicks). |
| `formID` |  | [!DNL Marketo Engage] ID do formulário (somente `web.formFilledOut`). |
| `linkID` |  | [!DNL Marketo Engage] id do link (`web.webinteraction.linkClicks` somente). |
| `interestingMomentDate` |  | Data do momento (`leadOperation.interestingMoment` somente). |
| `interestingMomentDescription` |  | Descrição de texto livre (somente interessanteMoment). |
| `interestingMomentSource` |  | Produto ou campanha relacionada (somente interessanteMoment). |
| `interestingMomentType` |  | Categoria / tipo (somente interessanteMoment). |
| `isDeleted` |  | Se este registro está marcado como excluído. |
| `lastUpdatedDate` |  | Hora da última modificação. |

### Referência de campo por tipo de atividade

As tabelas a seguir mostram quais detalhes se aplicam a cada atividade. Outros detalhes estão em branco. Algumas atividades compartilham o mesmo rótulo `eventType`: os códigos 8 e 48 usam `directMarketing.emailBounced`. Use `activityTypeID` para diferenciá-los.

#### Página da Web exibida (`web.webpagedetails.pageViews`) (Atividade tipo 1)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID da página. |
| `assetName` |  | Nome da página. |
| `webPageUrl` |  | URL da página. |
| `queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `webPageID` |  | [!DNL Marketo Engage] id da página da Web. |
| `referrerUrl` |  | URL do referenciador. |
| `userAgent` |  | Informações do navegador ou do cliente de email. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Formulário enviado (`web.formFilledOut`) (Atividade tipo 2)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID do formulário. |
| `assetName` |  | Nome do formulário. |
| `formID` |  | [!DNL Marketo Engage] ID do formulário. |
| `queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `webPageID` |  | [!DNL Marketo Engage] id da página da Web. |
| `referrerUrl` |  | URL do referenciador. |
| `userAgent` |  | Informações do navegador ou do cliente de email. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Link da Web clicado (`web.webinteraction.linkClicks`) (Atividade tipo 3)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | Interação/id do link. |
| `assetName` |  | URL de destino. |
| `linkID` |  | [!DNL Marketo Engage] id do link. |
| `queryParameters` |  | Informações adicionais incluídas em um endereço da Web. |
| `webPageID` |  | [!DNL Marketo Engage] id da página da Web. |
| `referrerUrl` |  | URL do referenciador. |
| `userAgent` |  | Informações do navegador ou do cliente de email. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Email enviado (`directMarketing.emailSent`) (Tipos de atividade 6, 39)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Email entregue (`directMarketing.emailDelivered`) (Tipos de atividade 7, 45)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Cancelar inscrição de email (`directMarketing.emailUnsubscribed`) (Tipo de atividade 9)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Email aberto (`directMarketing.emailOpened`) (Tipos de atividade 10, 40)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `isMobileDevice` |  | Se um dispositivo móvel foi gravado para a atividade. |
| `deviceModel` |  | Modelo do dispositivo. |
| `operatingSystem` |  | Sistema operacional. |
| `userAgent` |  | Informações do navegador ou do cliente de email. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Link de email clicado (`directMarketing.emailClicked`) (Tipos de atividade 11, 41)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `clickedLinkUrl` |  | URL do link clicado. |
| `isMobileDevice` |  | Se um dispositivo móvel foi gravado para a atividade. |
| `deviceModel` |  | Modelo do dispositivo. |
| `operatingSystem` |  | Sistema operacional. |
| `userAgent` |  | Informações do navegador ou do cliente de email. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Email rejeitado (`directMarketing.emailBounced`): rejeição permanente (Atividade tipo 8)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `bouncedCode` |  | Código de categoria de rejeição. |
| `bouncedDetails` |  | Motivo detalhado da rejeição. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

Esta atividade compartilha o rótulo `directMarketing.emailBounced` com o código de atividade 48, mas `recipientEmail` está em branco para o código 8. Use `activityTypeID` para distinguir os dois.

#### Email rejeitado (`directMarketing.emailBounced`): rejeição temporária de email de vendas (Tipo de atividade 48)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `recipientEmail` |  | Endereço de email do destinatário. |
| `bouncedCode` |  | Código de categoria de rejeição. |
| `bouncedDetails` |  | Motivo detalhado da rejeição. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Rejeição temporária de email (`directMarketing.emailBouncedSoft`) (Tipo de atividade 27)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `assetID` |  | ID de mala direta. |
| `assetName` |  | Nome da mala direta. |
| `recipientEmail` |  | Endereço de email do destinatário. |
| `bouncedCode` |  | Código de categoria de rejeição. |
| `bouncedDetails` |  | Motivo detalhado da rejeição. |
| `campaignID` |  | [!DNL Marketo Engage] id da campanha, quando atribuída à campanha. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Registro de momento interessante (`leadOperation.interestingMoment`) (Tipo de atividade 46)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `interestingMomentDate` |  | Data/hora do momento. |
| `interestingMomentDescription` |  | Descrição de texto livre. |
| `interestingMomentSource` |  | Nome do produto ou campanha relacionada. |
| `interestingMomentType` |  | Rótulo de tipo. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

`assetID` e `assetName` não estão preenchidos para este tipo de atividade.

#### Campo de pessoa alterado (`person.attributeChanged`) (Tipo de atividade 13)

Incluído somente quando a alteração estiver associada a uma jornada, como uma etapa &quot;Atualizar perfil de pessoa&quot;. As alterações fora de uma jornada não são incluídas.

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `attributeName` |  | Nome do campo que foi alterado. |
| `attributeID` |  | Identificador do campo que foi alterado. |
| `attributeNewValue` |  | Novo valor de campo, registrado como texto. |
| `attributeOldValue` |  | Valor do campo anterior, registrado como texto. |
| `attributeChangeReason` |  | Rótulo de motivo da alteração. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `journeyStepID` |  | Identificador da etapa de jornada. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Jornada ID do programa. |
| `activitySource` |  | Produto ou ação associado à atividade. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Pessoa adicionada ou iniciada em uma jornada (`person.journeyAdd`, `person.journeyStart`) (Tipos de atividade 182, 184)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `journeyStepID` |  | Identificador da etapa de jornada. |
| `journeyEntryCount` |  | Número de vezes que essa pessoa inseriu a jornada. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Jornada ID do programa. |
| `activitySource` |  | Produto ou ação associado à atividade. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Pessoa removida ou encerrou uma jornada (`person.journeyRemove`, `person.journeyEnd`) (Tipos de atividade 183, 185)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó de Jornada. |
| `journeyStepID` |  | Identificador da etapa de jornada. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Jornada ID do programa. |
| `activitySource` |  | Produto ou ação associado à atividade. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### A pessoa seguiu uma ramificação de jornada (`person.journeySplitNode`) (Tipo de atividade 186)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó do Jornada (o nó dividido). |
| `previousJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nó em que a pessoa estava antes da divisão. |
| `newJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nó para o qual a pessoa foi movida (geralmente igual a `journeyNodeID`). |
| `journeyStepID` |  | Identificador da etapa de jornada. |
| `journeyChoiceNumber` |  | Qual ramificação da divisão foi tirada. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Jornada ID do programa. |
| `activitySource` |  | Produto ou ação associado à atividade. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

#### Pessoa movida entre etapas de jornada (`person.journeyNodeTransition`) (Tipo de atividade 600)

| Nome do campo | Relação | O que isso lhe diz |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID do Registro: `_id`; `personID` corresponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comuns. |
| `journeyID` | Corresponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de jornada. |
| `journeyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador do nó de jornada atual. |
| `previousJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nó do qual a pessoa fez a transição. |
| `newJourneyNodeID` | Corresponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nó para o qual a pessoa fez a transição (geralmente igual a `journeyNodeID`). |
| `journeyStepID` |  | Identificador da etapa de jornada. |
| `journeyProgramID` | Nenhum conjunto de dados de programa de marketing separado neste guia | Jornada ID do programa. |
| `activitySource` |  | Produto ou ação associado à atividade. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comuns. |

## Conjuntos de dados de propriedade do cliente {#customer-owned-datasets}

Sua organização pode usar seus próprios conjuntos de dados do [!DNL Experience Platform] para contas ou pessoas. Quando configurado, [!DNL Adobe Journey Optimizer B2B Edition] pode adicionar informações a esses conjuntos de dados, em vez de criar outra conta ou conjunto de dados de pessoa.

Os nomes e os campos disponíveis dependem da configuração da organização. Use a conta configurada ou o identificador de pessoa para reconhecer registros correspondentes. Ter registros nesses conjuntos de dados não os disponibiliza automaticamente para públicos-alvo; a disponibilidade depende da configuração do [!DNL Experience Platform].
