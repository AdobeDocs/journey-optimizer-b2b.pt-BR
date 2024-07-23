---
title: Mapeamento de campo XDM
description: Revise o mapeamento de campo entre o esquema XDM da AEP, o Marketo Engage e o Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 20%

---

# Mapeamento de campo XDM

O Serviço de transferência de dados (DTS) no é responsável pela sincronização dos dados do Adobe Experience Platform com o Journey Optimizer B2B Edition. O DTS depende de mapeamentos entre os campos de esquema XDM do Experience Platform e seus equivalentes no Marketo Engage.

## Mapeamentos de campo padrão de pessoa de negócios XDM

| Pessoa de negócios XDM | Nome para Exibição da Pessoa Marketo Engage | Nome de exibição da pessoa B2B do AJO | Tipo XDM | Tipo de Marketo | Descrição do XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Endereço | ? | string | texto | Informações no nível da rua principal, número do apartamento, número da rua e nome da rua. |
| `workAddress.city ` | Cidade | Cidade | string | string | O nome da cidade. |
| `b2b.companyName` | Nome da empresa | ? | string | string | Nome da empresa à qual uma pessoa de negócios está associada. |
| `workAddress.country` | País | País | string | string | O nome do território administrado pelo governo. Além de `xdm:countryCode`, este é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `person.birthDate` | Data de nascimento | Data de nascimento | string | data | A data de nascimento completa de uma pessoa.  DD/MM/YYYY |
| `workEmail.address` | Endereço de e-mail | Endereço de e-mail | string | email | O endereço técnico, por exemplo, &#39;<name@domain.com>&#39;, conforme geralmente definido em RFC2822 e padrões subsequentes. |
| `workEmail.status` | E-mail suspenso | E-mail suspenso | string | booleano | Uma indicação quanto à capacidade de usar o endereço de email. |
| `faxPhone.number` | Número de fax | ? | string | telefone | Número de telefone do fax. |
| `person.name.firstName` | Nome | Nome | string | string | O primeiro segmento do nome na ordem de escrita aceito com mais frequência no idioma do nome. Em muitas culturas, este é o nome pessoal ou o nome preferencial. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar xdm:fullName é sempre aconselhável. |
| `extendedWorkDetails.jobTitle` | Nome do cargo | Nome do cargo | string | string | Cargo da pessoa. |
| `person.name.lastName` | Sobrenome | Sobrenome | string | string | O último segmento do nome na ordem de escrita aceito com mais frequência no idioma do nome. Em muitas culturas, este é o nome de família, sobrenome, patronímico ou nome matronímico herdado. As propriedades firstName e lastName foram introduzidas para manter a compatibilidade com sistemas existentes que definem nomes de forma simplificada, não semântica e não internacionalizável. Usar xdm:fullName é sempre aconselhável. |
| `b2b.personStatus` | Status do lead | ? | string | string | Campo que registra o status atual de marketing/vendas da pessoa. |
| `b2b.isMarketingSuspended` | Campanha de marketing suspensa | ? | booleano | booleano | Indica se o marketing é suspenso para a pessoa. |
| `b2b.marketingSuspendedCause` | Motivo susp. campanha market. | ? | string | string | Se o marketing for suspenso para a pessoa, essa propriedade fornecerá o motivo. |
| `person.name.middleName` | Nome do meio | ? | string | telefone | Nomes do meio, alternativos ou adicionais fornecidos entre o nome e o sobrenome. |
| `mobilePhone.number` | Número do celular | Número do celular | string | telefone | Número do celular. |
| `workPhone.number` | Número de telefone | Número de telefone | string | telefone | Número de telefone comercial. |
| `workAddress.postalCode` | Código postal | Código postal | string | string | O código postal da localização. Os códigos postais não estão disponíveis para todos os países. Em alguns países, conterá apenas parte do código postal. |
| `person.name.courtesyTitle` | Saudação | ? | string | string | Normalmente, uma abreviação de um título de pessoa, honorífico ou saudação. O courtesyTitle é usado na frente do nome completo ou do sobrenome nos textos de abertura. Por exemplo, Sr., Srta. ou Dr. |
| `workAddress.state` | Estado | Estado | string | string | O nome do Estado. Este é um campo de forma livre. |
| `consents.marketing.email.val` | Inscrição cancelada | Inscrição cancelada | string | booleano | Se unsubscribed for true (por exemplo, valor = 1), defina `consents.marketing.email.val` como (n). Se a assinatura cancelada for falsa (por exemplo, valor = 0), defina consents.marketing.email.val como nulo. |
| `consents.marketing.email.reason` | Motivo do cancelamento de inscrição | Motivo do cancelamento de inscrição | string | string |  |
| `b2b.companyWebsite` | Site | ? | string | url | Site da empresa à qual uma pessoa de negócios está associada. |

