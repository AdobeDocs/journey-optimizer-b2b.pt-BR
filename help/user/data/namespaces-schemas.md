---
title: Namespaces e esquemas B2B
description: Configure namespaces e esquemas do Experience Platform B2B para o Journey Optimizer B2B edition usando o utilitário de geração automática do Postman.
feature: Setup, Data Management
role: Admin
exl-id: 40d01027-7cf2-4189-8a49-7a0783c00721
source-git-commit: 944d2616fa21e7f8d2f8c439eaa2f5e529dacb84
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 98%

---

# Namespaces e esquemas B2B

A configuração do Journey Optimizer B2B Edition inclui a configuração dos namespaces e esquemas do Experience Platform usados com fontes B2B. O utilitário de automação do Postman é necessário para gerar namespaces e esquemas B2B.

>[!AVAILABILITY]
>
>- Você deve ter acesso ao [Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"} para que seus esquemas B2B sejam qualificados no [Perfil do Cliente em Tempo Real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/home){target="_blank"}.
>
>- Suas entidades B2B do Experience Platform devem usar as relações padrão descritas no [guia de namespaces e esquemas B2B](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}.

Revise as seguintes informações sobre a configuração subjacente para os namespaces e esquemas a serem usados com origens B2B. Ele também fornece detalhes para configurar o utilitário de automação do Postman, que é necessário para gerar namespaces B2B e esquemas.

## Configurar o utilitário de geração automática

Consulte os seguintes recursos para obter pré-requisitos e informações detalhadas sobre como configurar o ambiente do [!DNL Postman] para oferecer suporte ao namespace B2B e ao utilitário de geração automática de esquema.

- Baixe a coleção de utilitários de geração automática de namespace e esquema e o ambiente do [repositório do GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}.
- Para obter informações sobre como usar as APIs do Experience Platform, incluindo detalhes sobre como coletar valores para cabeçalhos necessários e ler chamadas de API de amostra, consulte [_Introdução às APIs do Adobe Experience Platform_](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}.
- Para obter informações sobre como gerar suas credenciais para APIs do Experience Platform, consulte [_Autenticar e acessar APIs do Experience Platform_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}.
- Para obter informações sobre como configurar o [!DNL Postman] para APIs do Experience Platform, consulte [_[!DNL Postman] no Adobe Experience Platform _](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}.

### Valores de ambiente

Com um console de desenvolvedor do Experience Platform e uma configuração do [!DNL Postman], você pode aplicar os valores de ambiente apropriados ao seu ambiente [!DNL Postman]. A tabela a seguir fornece valores de exemplo e informações adicionais sobre o preenchimento do ambiente [!DNL Postman]:

| Variable | Descrição | Exemplo |
| --- | --- | --- |
| `CLIENT_SECRET` | Um identificador exclusivo usado para gerar o `{ACCESS_TOKEN}`. | `{CLIENT_SECRET}` |
| `API_KEY` | Um identificador exclusivo usado para autenticar chamadas para APIs do Experience Platform. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | O token de autorização necessário para concluir chamadas para APIs do Experience Platform. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | Com relação a [!DNL Journey Optimizer B2B] e [!DNL Marketo Engage], esse valor é fixo e sempre é definido como: `ent_dataservices_sdk`. | `ent_dataservices_sdk` |
| `CONTAINER_ID` | O container `global` contém todas as classes, grupos de campos de esquema, tipos de dados e esquemas padrão fornecidos pelo parceiro da Adobe e da Experience Platform. Com relação a [!DNL Marketo], esse valor é fixo e sempre é definido como `global`. | `global` |
| `TECHNICAL_ACCOUNT_ID` | Uma credencial usada para integrar ao Adobe I/O. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | O Sistema Identity Management (IMS) fornece a estrutura para autenticação de serviços da Adobe. Com relação a [!DNL Journey Optimizer B2B] e [!DNL Marketo Engage], esse valor é fixo e sempre é definido como: `ims-na1.adobelogin.com`. | `ims-na1.adobelogin.com` |
| `IMS_ORG` | Uma entidade corporativa que pode ser proprietária ou licenciar produtos e serviços e permitir acesso a seus membros. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | O nome da partição de sandbox virtual que você está usando. | `prod` |
| `TENANT_ID` | Uma ID usada para garantir que os recursos criados tenham o namespace adequado e estejam contidos na organização. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | O endpoint de URL para o qual você está fazendo chamadas de API. Este valor é fixo e está sempre definido como: `http://platform.adobe.io/`. | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### Execute os scripts

Depois que os valores de ambiente estiverem no lugar, use a interface [!DNL Postman] para executar o script para criar namespaces e esquemas. Selecione a pasta raiz do utilitário gerador automático e, em seguida, selecione **[!DNL Run]** no cabeçalho superior.

![Pasta raiz do gerador de Namespaces e Esquemas na interface do usuário do Postman](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

A interface [!DNL Runner] é exibida. Aqui, verifique se todas as caixas de seleção estão marcadas e selecione **[!DNL Run Namespaces and Schemas Autogeneration Utility]**.

![Interface do usuário do Postman com várias solicitações na coleção Namespaces e Esquemas selecionada.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

Uma solicitação bem-sucedida cria os namespaces e esquemas B2B necessários.

## Namespaces B2B

Os namespaces de identidade são um componente do Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"} que serve para distinguir o contexto de uma identidade. Uma identidade totalmente qualificada inclui um valor de identidade e um namespace. Consulte [visão geral dos namespaces](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces){target="_blank"} para obter mais informações.

Os namespaces B2B são usados na identidade principal da entidade.

| Nome de exibição | Símbolo de identidade | Tipo de identidade |
| --- | --- | --- |
| Pessoa B2B | `b2b_person` | `CROSS_DEVICE` |
| Conta B2B | `b2b_account` | `B2B_ACCOUNT` |
| Oportunidade B2B | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| Relação pessoal da oportunidade B2B | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| Campanha B2B | `b2b_campaign` | `B2B_CAMPAIGN` |
| Membro da campanha B2B | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| Lista de marketing B2B | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| Membro da lista de marketing B2B | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| Relação pessoal da conta B2B | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## Esquemas B2B

A Experience Platform usa esquemas para descrever a estrutura dos dados de forma consistente e reutilizável. Ao definir os dados de forma consistente em todos os sistemas, fica mais fácil manter o significado e, portanto, obter valor dos dados.

Antes que o Experience Platform possa assimilar dados, deve haver um schema que descreva a estrutura dos dados e forneça restrições ao tipo de dados que pode estar contido em cada campo. Os esquemas consistem em uma classe base e zero ou mais grupos de campos de esquema.

Para obter mais informações sobre o modelo de composição de esquema, incluindo princípios de design e práticas recomendadas, consulte [_Noções básicas sobre a composição de esquema_](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}.

+++ Conta B2B

<table>
    <tr>
        <td style="width: 30%;">Classe base</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">Conta empresarial XDM</a></td>
    </tr>
    <tr>
        <td>Grupos de campos</td>
        <td>Detalhes da conta empresarial XDM</td>
    </tr>
    <tr>
        <td>[!DNL Profile] no esquema</td>
        <td>Habilitado</td>
    </tr>
    <tr>
        <td>Identidade principal</td>
        <td><code>accountKey.sourceKey</code> na classe base</td>
    </tr>
    <tr>
        <td>Namespace de identidade principal</td>
        <td>Conta B2B</td>
    </tr>
    <tr>
        <td>Identidade secundária</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> na classe base</td>
    </tr>
    <tr>
        <td>Namespace de identidade secundário</td>
        <td>Conta B2B</td>
    </tr>
    <tr>
        <td>Relação</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> no grupo de campos Detalhes da conta de negócios XDM</li><li>Propriedade de destino: <code>/accountKey/sourceKey</code></li><li>Tipo: um para um</li><li>Esquema de referência: Conta B2B</li><li>Namespace: conta B2B</li></ul> </td>
    </tr>
</table>

+++

+++ Pessoa B2B

<table>
    <tr>
        <td style="width: 30%;">Classe base</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile">Perfil individual XDM</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Grupos de campos</td>
        <td><ul><li>Detalhes da pessoa de negócios XDM</li><li>Componentes de pessoa de negócios XDM</li><li>IdentityMap</li><li>Detalhes sobre consentimento e preferência</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] no esquema</td>
        <td>Habilitado</td>
    </tr>
    <tr>
        <td>Identidade principal</td>
        <td><code>b2b.personKey.sourceKey</code> no Grupo de campos Detalhes da pessoa de negócios XDM</td>
    </tr>
    <tr>
        <td>Namespace de identidade principal</td>
        <td>Pessoa B2B</td>
    </tr>
    <tr>
        <td>Identidade secundária</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> do grupo de campos Detalhes da pessoa de negócios XDM</li><li><code>workEmail.address</code> do grupo de campos Detalhes da pessoa de negócios XDM</li></ol></td>
    </tr>
    <tr>
        <td>Namespace de identidade secundário</td>
        <td><ol><li>Pessoa B2B</li><li>Email</li></ol></td>
    </tr>
    <tr>
        <td>Relação</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> do grupo de campos Componentes de pessoa de negócios XDM</li><li>Tipo: De muitos para um</li><li>Esquema de referência: conta B2B</li><li>Namespace: conta B2B</li><li>Propriedade de destino: accountKey.sourceKey</li><li>Nome do relacionamento do esquema atual: Conta</li><li>Nome do relacionamento do esquema de referência: Pessoas</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++
-->
