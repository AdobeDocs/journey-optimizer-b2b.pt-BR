---
title: Campos XDM
description: Revise os campos de atributo padrão que são sincronizados entre o Adobe Experience Platform e o Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 16%

---

# Campos XDM

Os dados de público-alvo da conta são armazenados como atributos nas classes Conta de negócios XDM e Pessoa de negócios XDM. Os dados são sincronizados periodicamente entre o Adobe Experience Platform e o Journey Optimizer B2B edition. As seções a seguir listam os conjuntos padrão de atributos.

>[!TIP]
>
>Você pode modelar as classes de Pessoa Comercial XDM e Conta Comercial XDM em uma relação muitos para muitos usando a classe de Relação de Pessoa da Conta Comercial XDM, conforme descrito na [documentação do Experience Platform XDM](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

## Atributos de relação pessoal da conta comercial XDM

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Funções da pessoa | Função | Matriz de string | Uma matriz de funções associadas à pessoa na conta, como `owner, accountant, designer`. |

## Atributos de pessoa de negócios XDM

>[!IMPORTANT]
>
>O atributo `workEmail.Address` é obrigatório. Se estiver vazio para um membro do público-alvo da conta, essa pessoa não será assimilada e será omitida das jornadas de conta e dos grupos de compra que fazem referência ao público-alvo.

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
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
| `workEmail.address` | Endereço | Endereço de email | String | **Campo obrigatório** <br/>O endereço técnico, por exemplo, `<name@domain.com>`, conforme definido normalmente em RFC2822 e padrões subsequentes. |
| `workEmail.status` | Status | E-mail suspenso | String | Uma indicação quanto à capacidade de usar o endereço de email. |
| `workPhone.number` | Número | Número de telefone | String | Número de telefone comercial. |

## Atributos da conta de negócios XDM

>[!IMPORTANT]
>
>O atributo `accountName` é obrigatório. Se estiver vazio para uma conta em um público-alvo de conta, essa conta não será assimilada e será omitida das jornadas de conta e dos grupos de compra que fazem referência ao público-alvo.

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Cidade | Cidade | String | O nome da cidade usado no endereço para cobrança. |
| `accountBillingAddress.country` | País | País | String | O nome do território administrado pelo governo usado no endereço de faturamento. Além de `xdm:countryCode`, é um campo de forma livre que pode ter o nome do país em qualquer idioma. |
| `accountBillingAddress.postalCode` | Código postal | CEP do endereço | String | O código postal da localização do endereço de cobrança. Os códigos postais não estão disponíveis para todos os países. Em alguns países, contém apenas parte do código postal. |
| `accountBillingAddress.region` | Região  | Região do endereço | String | A parte da região, cidade ou distrito do endereço para cobrança. |
| `accountBillingAddress.state` | Estado | Estado | String | O nome do estado do endereço para cobrança. É um campo de forma livre. |
| `accountBillingAddress.street1` | Folha 1 | Folha 1 | String | Informações no nível da rua principal do endereço de cobrança, que normalmente incluem o número do apartamento, o número da rua e o nome da rua. |
| `accountName` | Nome | Nome | String | **Campo obrigatório** <br/>Nome da empresa. São permitidos até 255 caracteres neste campo. |
| `accountOrganization.annualRevenue.amount` | Receita anual | Receita anual | Número | Quantidade estimada de receita anual da organização. |
| `accountOrganization.industry` | Setor | Setor | String | O setor atribuído à organização. É um campo de forma livre, e é aconselhável usar um valor estruturado para consultas ou usar a propriedade `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL do logotipo | URL do logotipo | String | Caminho a ser combinado com a URL de uma instância do Salesforce (por exemplo, `https://yourInstance.salesforce.com/`) para gerar uma URL para solicitar a imagem do perfil da rede social associada à conta. O URL gerado retorna um redirecionamento HTTP (código 302) para a imagem de perfil da rede social da conta. |
| `accountOrganization.numberOfEmployees` | Número de funcionários | Núm. funcionários | Inteiro | O número de funcionários na organização. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | String | O código de Classificação Industrial Padrão (SIC) é um código de quatro dígitos que categoriza os setores aos quais as empresas pertencem com base em suas atividades comerciais. |
| `accountOrganization.website` | URL do site | Nome do domínio | String | O URL do site da organização. |
| `accountPhone.number` | N/D | Número de telefone da conta | String | O número de telefone associado à conta. |
| `accountSourceType` | N/D | Tipo de fonte | String | Tipo de Source da conta. |

## Atributos de oportunidade de negócios XDM

Além disso, os dados da oportunidade são armazenados como atributos na classe de Oportunidade Comercial XDM, que pode ser associada à classe de Conta Comercial XDM por meio de uma relação muitos para um, conforme descrito na [documentação da Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

| [Propriedade](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} | Nome de exibição | Nome para exibição do Journey Optimizer B2B | Tipo de dados | Descrição |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Data de fechamento prevista | Data de fechamento esperada da oportunidade | String | Data prevista de fechamento da oportunidade. |
| `expectedRevenue.amount` | Receita esperada | Receita total esperada da oportunidade | String | Receita calculada com base no valor e na probabilidade. |
| `fiscalQuarter` | Trimestre fiscal | Trimestre fiscal da oportunidade | String | O trimestre fiscal direcionado para a oportunidade. |
| `fiscalYear` | Ano fiscal | Ano fiscal da oportunidade | String | O ano fiscal de destino da oportunidade. |
| `forecastCategory` | Categoria de previsão | Categoria de Previsão de Oportunidades | String | Categoria de Previsão determinada pelo valor do Estágio da oportunidade. |
| `forecastCategoryName` | Nome da categoria de previsão | Nome da categoria de previsão de oportunidade | String | Nome da categoria de previsão que é exibido nos relatórios para uma determinada categoria de previsão. |
| `isClosed` | Sinalizador fechado | Oportunidade fechada | String | Sinalizador que indica se a oportunidade está fechada. |
| `isWon` | Sinalizador conquistado | Oportunidade ganha | String | Sinalizador que indica se a oportunidade foi conquistada. |
| `lastActivityDate` | Data da última atividade | Data da última atividade | String | Data da última atividade para a oportunidade. |
| `leadSource` | Fonte do lead | Fonte do lead | String | Source da oportunidade, como Anúncio, Parceiro ou Web. |
| `nextStep` | Próxima etapa | Próxima etapa da oportunidade | String | Descrição da próxima tarefa para fechar a oportunidade. |
| `opportunityAmount.amount` | Valor da oportunidade | Valor total da oportunidade | String | Valor total estimado da venda da oportunidade. |
| `opportunityDescription` | Descrição da oportunidade | Descrição da oportunidade | String | Informações adicionais para descrever a oportunidade, como possíveis produtos para vender ou compras anteriores do cliente. |
| `opportunityName` | Nome da oportunidade | Nome da oportunidade | String | Assunto ou nome descritivo, como o pedido esperado ou o nome da empresa, para a oportunidade. |
| `opportunityQuantity` | Quantidade da oportunidade | Quantidade da oportunidade | String | Total de todos os valores do campo de quantidade para todos os produtos na lista de Produtos relacionada para a oportunidade. |
| `opportunityStage` | Estágio da oportunidade | Estágio da oportunidade | String | Estágio de vendas da oportunidade para ajudar a equipe de vendas em seus esforços para ganhá-la. |
| `opportunityType` | Tipo de oportunidade | Tipo de oportunidade | String | Tipo atribuído à oportunidade, como _Negócios Existentes_ ou _Novos Negócios_ |
| `probabilityPercentage` | Porcentagem de probabilidade | Porcentagem de probabilidade da oportunidade | String | Probabilidade de fechamento da oportunidade, expressa em porcentagem. |
