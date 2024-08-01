---
title: Campos XDM
description: Revise os campos de atributo padrão que são sincronizados entre o Adobe Experience Platform e o Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: b38878ca063967e6c1ae56617674af52c10913df
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 16%

---

# Campos XDM

Os dados de público-alvo da conta são armazenados como atributos nas classes Conta de negócios XDM e Pessoa de negócios XDM. Os dados são sincronizados periodicamente entre o Adobe Experience Platform e o Journey Optimizer B2B Edition. As seções a seguir listam os conjuntos padrão de atributos.

## Atributos de pessoa de negócios XDM

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Nome da empresa | Nome da empresa | String | Nome da empresa à qual uma pessoa de negócios está associada. |
| `b2b.companyWebsite` | Site da empresa | Site | String | Site da empresa à qual uma pessoa de negócios está associada. |
| `b2b.isMarketingSuspended` | Indicador de suspensão de marketing | Campanha de marketing suspensa | Booleano | O valor indica se o marketing é suspenso para a pessoa. |
| `b2b.marketingSuspendedCause` | Motivo susp. campanha market. | Motivo susp. campanha market. | String | Se o marketing for suspenso para a pessoa, essa propriedade fornecerá o motivo. |
| `b2b.personStatus` | Status da pessoa | Status do lead | String | Campo que registra o status atual de marketing/vendas da pessoa. |
| `consents.marketing.email.reason` | Motivo da recusa | Motivo do cancelamento de inscrição | String | Motivo associado à recusa de email. |
| `consents.marketing.email.val` | Inscrição cancelada | Inscrição cancelada | String | Se unsubscribed for true (por exemplo, valor = 1), defina `consents.marketing.email.val` como (n). Se unsubscribed for falso (por exemplo, valor = 0), defina `consents.marketing.email.val` como nulo. |
| `extendedWorkDetails.jobTitle` | Nome do cargo | Nome do cargo | String | Cargo da pessoa. |
| `faxPhone.number` | Número | Número de fax | String | Número de telefone do fax. |
| `mobilePhone.number` | Número | Número do celular | String | O número do celular associado à pessoa. |
| `person.birthDate` | Data de nascimento (AAAA-MM-DD) | Data de nascimento | String | A data completa em que uma pessoa nasceu. DD/MM/YYYY |
| `person.name.courtesyTitle` | Título de cortesia | Saudação | String | Normalmente, uma abreviação do título, honorífico ou saudação de uma pessoa. O courtesyTitle é usado na frente do nome completo ou do sobrenome nos textos de abertura. Por exemplo, Sr., Sra. ou Dr. |
| `person.name.firstName` | Nome | Nome | String | O primeiro segmento do nome na ordem escrita que é aceito com mais frequência no idioma do nome. Em muitas culturas, é o nome pessoal ou o nome preferencial. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre aconselhável. |
| `person.name.lastName` | Sobrenome | Sobrenome | String | O último segmento do nome na ordem escrita que é aceito com mais frequência no idioma do nome. Em muitas culturas, é o nome de família, sobrenome, patronímico ou nome matronímico herdado. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre aconselhável. |
| `person.name.middleName` | Nome do meio | Nome do meio | String | Nomes do meio, alternativos ou adicionais fornecidos entre o nome e o sobrenome. |
| `workAddress.city ` | Cidade | Cidade | String | O nome da cidade. |
| `workAddress.country` | País | País | String | O nome do território administrado pelo governo. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `workAddress.postalCode` | Código postal | Código postal | String | O código postal da localização. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `workAddress.state` | Estado | Estado | String | O nome do estado do endereço. É um campo de forma livre. |
| `workAddress.street1` | Folha 1 | Endereço | String | Informações no nível da rua principal, número do apartamento, número da rua e nome da rua. |
| `workEmail.address` | Endereço | Endereço de e-mail | String | O endereço técnico, por exemplo, `<name@domain.com>`, conforme comumente definido em RFC2822 e padrões subsequentes. |
| `workEmail.status` | Status | E-mail suspenso | String | Uma indicação quanto à capacidade de usar o endereço de email. |
| `workPhone.number` | Número | Número de telefone | String | Número de telefone comercial. |

## Atributos da conta de negócios XDM

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Cidade | Cidade | String | O nome da cidade usado no endereço para cobrança. |
| `accountBillingAddress.country` | País | País | String | O nome do território administrado pelo governo usado no endereço de faturamento. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `accountBillingAddress.postalCode` | Código postal | CEP do endereço | String | O código postal da localização do endereço de cobrança. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `accountBillingAddress.region` | Região  | Região do endereço | String | A parte da região, cidade ou distrito do endereço para cobrança. |
| `accountBillingAddress.state` | Estado | Estado | String | O nome do estado do endereço para cobrança. É um campo de forma livre. |
| `accountBillingAddress.street1` | Folha 1 | Folha 1 | String | Informações no nível da rua principal do endereço de cobrança, que normalmente incluem o número do apartamento, o número da rua e o nome da rua. |
| `accountName` | Nome | Nome | String | Nome da empresa. São permitidos até 255 caracteres neste campo. |
| `accountOrganization.annualRevenue.amount` | Receita anual | Receita anual | Número | Quantidade estimada de receita anual da organização. |
| `accountOrganization.industry` | Setor | Setor | String | O setor atribuído à organização. É um campo de forma livre, e é aconselhável usar um valor estruturado para consultas ou usar a propriedade `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL do logotipo | URL do logotipo | String | Caminho a ser combinado com a URL de uma instância do Salesforce (por exemplo, `https://yourInstance.salesforce.com/`) para gerar uma URL para solicitar a imagem do perfil da rede social associada à conta. O URL gerado retorna um redirecionamento HTTP (código 302) para a imagem de perfil da rede social da conta. |
| `accountOrganization.numberOfEmployees` | Número de funcionários | Núm. funcionários | Inteiro | O número de funcionários na organização. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | String | O código de Classificação Industrial Padrão (SIC), que é um código de quatro dígitos que categoriza os setores aos quais as empresas pertencem com base em suas atividades comerciais. |
| `accountOrganization.website` | URL do site | Nome do domínio | String | O URL do site da organização. |
| `accountPhone.number` | N/D | Número de telefone da conta | String | O número de telefone associado à conta. |
| `accountSourceType` | N/D | Tipo de fonte | String | Tipo de Source da conta. |
