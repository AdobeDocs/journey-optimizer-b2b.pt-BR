---
title: Campos XDM
description: Revise os campos de atributo padrão que são sincronizados entre o Adobe Experience Platform e o Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 34ef9681b75ef1cd43d34e3f2836a60affb95b33
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 16%

---

# Campos XDM

Os dados de público-alvo da conta são armazenados como atributos nas classes Conta de negócios XDM e Pessoa de negócios XDM. Os dados são sincronizados periodicamente entre o Adobe Experience Platform e o Journey Optimizer B2B edition. As seções a seguir lista os conjuntos padrão de atributos.

>[!TIP]
>
>Você pode modelar as classes XDM Empresas Pessoa e XDM Empresas Conta em um relação muitos para muitos usando a classe XDM Empresas Account Person Relation, conforme descrito na [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/relationship-b2b) Experience Platform XDM.

## Atributos de relação de pessoa da conta Empresas XDM

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Funções de pessoa | Função | Matriz de strings | Uma matriz de funções associadas à pessoa na conta, como `owner, accountant, designer`. |

## Atributos de pessoa de negócios XDM

>[!IMPORTANT]
>
>O atributo `workEmail.Address` é obrigatório. Se estiver vazio para um membro do público-alvo da conta, essa pessoa não será assimilada e será omitida das jornadas de conta e dos grupos de compra que fazem referência ao público-alvo.

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indicador de suspensão de marketing | Campanha de marketing suspensa | Booleano | O valor indica se marketing da pessoa foi suspensa. |
| `b2b.marketingSuspendedCause` | Motivo susp. campanha market. | Motivo susp. campanha market. | String | Se o marketing for suspenso para a pessoa, essa propriedade fornecerá o motivo. |
| `b2b.personStatus` | Status da pessoa | Status do lead | String | Campo que registra o status atual de marketing/vendas da Pessoa. |
| `consents.marketing.email.reason` | Motivo da opção de rejeição | Motivo do cancelamento de inscrição | String | Motivo associado ao recusar de email. |
| `consents.marketing.email.val` | Inscrição cancelada | Inscrição cancelada | String | Se unsubscribed for true (por exemplo, valor = 1), defina `consents.marketing.email.val` como (n). Se a subscrição cancelada for false (por exemplo, valor = 0), defina `consents.marketing.email.val` como nulo. |
| `extendedWorkDetails.jobTitle` | Nome do cargo | Nome do cargo | String | Cargo da pessoa. |
| `faxPhone.number` | Número | Número de fax | String | Número de telefone de fax. |
| `mobilePhone.number` | Número | Número do celular | String | O número do celular associado com a pessoa. |
| `person.birthDate` | Data de nascimento (DD/MM/YYYY) | Data de nascimento | String | A data completa em que uma pessoa nasceu. DD/MM/YYYY |
| `person.name.courtesyTitle` | Título de cortesia | Saudação | String | Normalmente, uma abreviação do título, honorífico ou saudação de uma pessoa. O courtesyTitle é usado na frente do nome completo ou do sobrenome nos textos de abertura. Por exemplo, Sr., Ms., ou Dr. |
| `person.name.firstName` | Nome | Nome | String | A primeira segmento do nome na solicitar escrita que é mais comumente aceita na língua do nome. Em muitas culturas, é o nome pessoal ou o nome preferencial. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre preferível. |
| `person.name.lastName` | Sobrenome | Sobrenome | String | A última segmento do nome na solicitar escrita que é mais comumente aceita na língua do nome. Em muitas culturas, é o nome herdado da família, sobrenome, patronímico ou matronômico. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com os sistemas existentes que modelam nomes de maneira simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre aconselhável. |
| `person.name.middleName` | Nome do meio | Nome do meio | String | Nomes intermediários, alternativos ou adicionais fornecidos entre o nome e sobrenome. |
| `workAddress.city ` | Cidade | Cidade | String | O nome da cidade. |
| `workAddress.country` | País | País | String | O nome do território administrado pelo governo. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `workAddress.postalCode` | Código postal | Código postal | String | O código postal do local. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `workAddress.state` | Estado | Estado | String | O nome do estado do endereço. É um campo de forma livre. |
| `workAddress.street1` | Folha 1 | Endereço | String | Informações no nível da rua principal, número do apartamento, número da rua e nome da rua. |
| `workEmail.address` | Endereço | Endereço de email | String | **Campo obrigatório** <br/>O endereço técnico, por exemplo, `<name@domain.com>` tão comumente definido em RFC2822 e padrões subsequentes. |
| `workEmail.status` | Status | E-mail suspenso | String | Uma indicação sobre a capacidade de usar o endereço de email. |
| `workPhone.number` | Número | Número de telefone | String | Número do telefone de trabalho. |

## Atributos da conta Empresas XDM

>[!IMPORTANT]
>
>O `accountName` atributo é obrigatório. Se estiver vazio para um conta em uma público-alvo de conta, essa conta não é assimilada e é omitida de jornadas conta e grupos de compras que fazem referência ao público-alvo.

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nome de exibição | Nome B2B exibição do Journey Optimizer | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Cidade | Cidade | String | O nome da cidade usada no endereço do faturamento. |
| `accountBillingAddress.country` | País | País | String | O nome do território administrado pelo governo usado no endereço faturamento. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `accountBillingAddress.postalCode` | Código postal | Code postais de endereço | String | O código postal da localização do endereço do faturamento. Os códigos postais não estão disponíveis para todos os países. Em alguns países, ele contém apenas parte do código postal. |
| `accountBillingAddress.region` | Região  | Região do endereço | String | A parte região, município ou distrito do endereço do faturamento. |
| `accountBillingAddress.state` | Estado | Estado | String | O nome do estado do endereço para cobrança. É um campo de forma grátis. |
| `accountBillingAddress.street1` | Rua 1 | Rua 1 | String | Informações primárias do nível da rua para o endereço faturamento, que normalmente incluiria o número do apartamento, o número da rua e o nome da rua. |
| `accountName` | Nome | Nome | String | **Nome do campo** <br/>obrigatório do empresa. Nesse campo são permitidos até 255 caracteres. |
| `accountOrganization.annualRevenue.amount` | Receita anual | Receita anual | Número | Quantidade estimada de receita anual da organização. |
| `accountOrganization.industry` | Setor | Setor | String | O setor atribuído à organização. É um campo de forma livre, e é aconselhável usar um valor estruturado para consultas ou usar a propriedade `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL do logotipo | URL do logotipo | String | Caminho a ser combinado com o URL de uma instância do Salesforce (por exemplo) `https://yourInstance.salesforce.com/`para gerar um URL para solicitação a imagem rede social perfil associada à conta. A URL gerada retorna uma redirecionar HTTP (código 302) para a imagem perfil rede social para o conta. |
| `accountOrganization.numberOfEmployees` | Número de funcionários | Núm. funcionários | Inteiro | O número de funcionários na organização. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | String | O código De classificação industrial padrão (SIC) é um código de quatro dígitos que categoriza os setores aos quais as empresas pertencem com base em suas atividades comerciais. |
| `accountOrganization.website` | URL do site | Nome do domínio | String | O URL do site da organização. |
| `accountPhone.number` | N/D | Número de telefone da conta | String | O número de telefone associado à conta. |
| `accountSourceType` | N/D | Tipo de fonte | String | Tipo de Source da conta. |

## Atributos do XDM Empresas Opportunity

Além disso, oportunidade dados são armazenados como atributos na classe XDM Empresas Opportunity, que pode ser associada à classe XDM Empresas Account por meio de um relacionamento muitos para um, conforme descrito [aqui](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field).

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) | Nome de exibição | Nome B2B exibição do Journey Optimizer | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Data de fechamento prevista | Data de encerramento oportunidade esperada | String | Data esperada de encerramento para o oportunidade. |
| `expectedRevenue.amount` | Receita esperada | Receita total esperada da oportunidade | String | Receita calculada com base no valor e na probabilidade. |
| `fiscalQuarter` | Trimestre fiscal | Trimestre fiscal da oportunidade | String | O trimestre fiscal direcionado para o oportunidade. |
| `fiscalYear` | Ano fiscal | Oportunidade ano fiscal | String | O ano fiscal direcionado para o oportunidade. |
| `forecastCategory` | Categoria de previsão | Previsão de oportunidade categoria | String | A previsão Categoria determinada pelo valor oportunidade estágio. |
| `forecastCategoryName` | Nome da categoria de previsão | Nome da categoria de previsão de oportunidade | String | Nome da categoria de previsão que é exibido nos relatórios para uma determinada categoria de previsão. |
| `isClosed` | Sinalizador fechado | Oportunidade fechada | String | Sinalizador que indica se a oportunidade está fechada. |
| `isWon` | Sinalizador conquistado | Oportunidade ganha | String | Sinalizador que indica se a oportunidade foi conquistada. |
| `lastActivityDate` | Data da última atividade | Data da última atividade | String | Última data atividade do oportunidade. |
| `leadSource` | Fonte do lead | Fonte do lead | String | Origem do oportunidade, como Anúncio, Parceiro ou Web. |
| `nextStep` | Próxima etapa | Próxima etapa da oportunidade | String | Descrição do próximo tarefa para fechar a oportunidade. |
| `opportunityAmount.amount` | Valor da oportunidade | Valor total da oportunidade | String | Valor total estimado de venda para o oportunidade. |
| `opportunityDescription` | Descrição da oportunidade | Descrição da oportunidade | String | Informações adicionais para descrever a oportunidade, como possíveis produtos para vender ou compras passadas do cliente. |
| `opportunityName` | Nome da oportunidade | Nome da oportunidade | String | Assunto ou nome descritivo, como o pedido esperado ou o nome da empresa, para a oportunidade. |
| `opportunityQuantity` | Quantidade da oportunidade | Oportunidade quantidade | String | Total de todos os valores de campo de quantidade para todos os produtos na lista de Produtos relacionados para a oportunidade. |
| `opportunityStage` | Estágio da oportunidade | Oportunidade estágio | String | As vendas estágio do oportunidade para ajudar as vendas a equipe em seus esforços para ganhá-la. |
| `opportunityType` | Tipo de oportunidade | Tipo de oportunidade | String | Tipo atribuído à oportunidade, como _Negócios Existentes_ ou _Novos Negócios_ |
| `probabilityPercentage` | Porcentagem de probabilidade | Porcentagem de probabilidade da oportunidade | String | A probabilidade de fechar a oportunidade foi declarada como uma porcentagem. |
