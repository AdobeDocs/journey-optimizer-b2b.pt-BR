---
title: Mapeamento de campo XDM
description: Revise o mapeamento de campo entre o esquema XDM da AEP, o Marketo Engage e o Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 838308621a27bcfc6425b8683f642a66f1fa6a7b
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 18%

---

# Mapeamento de campo XDM

O Data Transfer Service (DTS) é responsável pela sincronização de dados do Adobe Experience Platform para o Journey Optimizer B2B Edition. O DTS depende de mapeamentos entre os campos de esquema XDM do Experience Platform e seus equivalentes no Marketo Engage.

## Mapeamentos de campo padrão de pessoa de negócios XDM

| [Pessoa de negócios XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome de exibição XDM | nome para exibição do Marketo Engage | Tipo XDM | Tipo de Marketo | Descrição do XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Nome da empresa | Nome da empresa | string | string | Nome da empresa à qual uma pessoa de negócios está associada. |
| `b2b.companyWebsite` | Site da empresa | Site | string | url | Site da empresa à qual uma pessoa de negócios está associada. |
| `b2b.isMarketingSuspended` | Indicador de suspensão de marketing | Campanha de marketing suspensa | booleano | booleano | O valor indica se o marketing é suspenso para a pessoa. |
| `b2b.marketingSuspendedCause` | Motivo susp. campanha market. | Motivo susp. campanha market. | string | string | Se o marketing for suspenso para a pessoa, essa propriedade fornecerá o motivo. |
| `b2b.personStatus` | Status da pessoa | Status do lead | string | string | Campo que registra o status atual de marketing/vendas da pessoa. |
| `consents.marketing.email.reason` | Motivo da recusa | Motivo do cancelamento de inscrição | string | string | Motivo associado à recusa de email. |
| `consents.marketing.email.val` | Inscrição cancelada | Inscrição cancelada | string | booleano | Se unsubscribed for true (por exemplo, valor = 1), defina `consents.marketing.email.val` como (n). Se a assinatura cancelada for falsa (por exemplo, valor = 0), defina consents.marketing.email.val como nulo. |
| `extendedWorkDetails.jobTitle` | Nome do cargo | Nome do cargo | string | string | Cargo da pessoa. |
| `faxPhone.number` | Número | Número de fax | string | telefone | Número de telefone do fax. |
| `mobilePhone.number` | Número | Número do celular | string | telefone | O número do celular associado à pessoa. |
| `person.birthDate` | Data de nascimento (AAAA-MM-DD) | Data de nascimento | string | data | A data completa em que uma pessoa nasceu. DD/MM/YYYY |
| `person.name.courtesyTitle` | Título de cortesia | Saudação | string | string | Normalmente, uma abreviação do título, honorífico ou saudação de uma pessoa. O courtesyTitle é usado na frente do nome completo ou do sobrenome nos textos de abertura. Por exemplo, Sr., Sra. ou Dr. |
| `person.name.firstName` | Nome | Nome | string | string | O primeiro segmento do nome na ordem escrita que é aceito com mais frequência no idioma do nome. Em muitas culturas, é o nome pessoal ou o nome preferencial. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre aconselhável. |
| `person.name.lastName` | Sobrenome | Sobrenome | string | string | O último segmento do nome na ordem escrita que é aceito com mais frequência no idioma do nome. Em muitas culturas, é o nome de família, sobrenome, patronímico ou nome matronímico herdado. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar `xdm:fullName` é sempre aconselhável. |
| `person.name.middleName` | Nome do meio | Nome do meio | string | telefone | Nomes do meio, alternativos ou adicionais fornecidos entre o nome e o sobrenome. |
| `workAddress.city ` | Cidade | Cidade | string | string | O nome da cidade. |
| `workAddress.country` | País | País | string | string | O nome do território administrado pelo governo. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `workAddress.postalCode` | Código postal | Código postal | string | string | O código postal da localização. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `workAddress.state` | Estado | Estado | string | string | O nome do estado do endereço. É um campo de forma livre. |
| `workAddress.street1` | Folha 1 | Endereço | string | texto | Informações no nível da rua principal, número do apartamento, número da rua e nome da rua. |
| `workEmail.address` | Endereço | Endereço de e-mail | string | email | O endereço técnico, por exemplo, `<name@domain.com>`, conforme comumente definido em RFC2822 e padrões subsequentes. |
| `workEmail.status` | Status | E-mail suspenso | string | booleano | Uma indicação quanto à capacidade de usar o endereço de email. |
| `workPhone.number` | Número | Número de telefone | string | telefone | Número de telefone comercial. |

## Mapeamentos de campo padrão da conta de negócios XDM

| [Conta de negócios XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nome de exibição XDM | nome para exibição do Marketo Engage | Tipo XDM | tipo de Marketo Engage | Descrição do XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Cidade | Cidade | string | string | O nome da cidade usado no endereço para cobrança. |
| `accountBillingAddress.country` | País | País | string | string | O nome do território administrado pelo governo usado no endereço de faturamento. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `accountBillingAddress.postalCode` | Código postal | CEP do endereço | string | string | O código postal da localização do endereço de cobrança. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `accountBillingAddress.region` | Região  | Região do endereço | string | string | A parte da região, cidade ou distrito do endereço para cobrança. |
| `accountBillingAddress.state` | Estado | Estado | string | string | O nome do estado do endereço para cobrança. É um campo de forma livre. |
| `accountBillingAddress.street1` | Folha 1 | Folha 1 | string | string | Informações no nível da rua principal do endereço de cobrança, que normalmente incluem o número do apartamento, o número da rua e o nome da rua. |
| `accountName` | Nome | Nome | string | string | Nome da empresa. São permitidos até 255 caracteres neste campo. |
| `accountOrganization.annualRevenue.amount` | Receita anual | Receita anual | número | currency | Quantidade estimada de receita anual da organização. |
| `accountOrganization.industry` | Setor | Setor | string | string | O setor atribuído à organização. É um campo de forma livre, e é aconselhável usar um valor estruturado para consultas ou usar a propriedade `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL do logotipo | URL do logotipo | string | string | Caminho a ser combinado com a URL de uma instância do Salesforce (por exemplo, `https://yourInstance.salesforce.com/`) para gerar uma URL para solicitar a imagem do perfil da rede social associada à conta. O URL gerado retorna um redirecionamento HTTP (código 302) para a imagem de perfil da rede social da conta. |
| `accountOrganization.numberOfEmployees` | Número de funcionários | Núm. funcionários | integer | integer | O número de funcionários na organização. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | string | string | O código de Classificação Industrial Padrão (SIC), que é um código de quatro dígitos que categoriza os setores aos quais as empresas pertencem com base em suas atividades comerciais. |
| `accountOrganization.website` | URL do site | Nome do domínio | string | string | O URL do site da organização. |
| `accountPhone.number` | N/D | Número de telefone da conta | string | string | O número de telefone associado à conta. |
| `accountSourceType` | N/D | Tipo de fonte | string | string | Tipo de Source da conta. |
