---
title: Habilidades do público-alvo para contas B2B e pessoas
description: Saiba mais sobre as habilidades do público-alvo para contas B2B e pessoas. Explore a intenção do produto, identifique perfis, avalie a cobertura da função e crie modelos de grupo de compras.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# Habilidades de público para contas B2B e pessoas

Use as habilidades do público-alvo para B2B na interface [!DNL CX Coworker]. Explore a intenção do produto entre contas e pessoas. Identifique perfis relevantes, avalie a cobertura do grupo de compras e crie modelos de função do grupo de compras.

* Avalie o interesse da conta em produtos específicos e compare as tendências de intenção.
* Identifique pessoas e perfis associados aos interesses do produto.
* Revise as funções dos grupos de compra e identifique lacunas de cobertura.
* Gerar e refinar modelos de função de grupo de compra.

>[!PREREQUISITES]
>
>Antes de usar habilidades de público-alvo para contas B2B e pessoas, configure as seguintes definições de dados e mapeamentos:
>
>* [Taxonomia e mapeamento de dados de intenção](../admin/intent-data.md)
>* [Mapeamento de campo XDM](#xdm-data-prerequisites)

Clique no ícone _Perguntar[!DNL Coworker]_ ( ![Perguntar [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ) na parte superior do aplicativo para abrir o aplicativo [!DNL Coworker]. Digite o prompt do seu idioma natural na interface do bate-papo.

![Aviso de público-alvo em [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}

## Áreas de foco de habilidades do público

Use áreas de foco de habilidade do público-alvo para explorar a intenção da conta, entender pessoas e personas e preparar modelos de grupo de compra.

| Focus | Tarefas |
| ----- | ----- |
| Tentativa de conta | Avalie a intenção da conta para produtos específicos usando níveis de intenção baixo, médio e alto. Compare as tendências de juros do produto ao longo do tempo e identifique as contas que mostram interesse em produtos específicos. Analise os padrões de envolvimento junto com a cobertura de persona. |
| Pessoas e personalidades | Identifique e classifique perfis por intenção de produto em um ou mais produtos. Analise as métricas de oportunidade, incluindo taxa de ganho, taxa de associação e contagens. Mapeie personas para funções como _Especialista_, _Decisor_ e _Influenciador_, e revise as explicações para atribuições de funções. |
| Cobertura do grupo de compras | Avaliar o tamanho do grupo de compras e a cobertura da pessoa em todas as contas. Revise a distribuição de funções e identifique perfis ou funções ausentes. Encontre contas com campeões identificados em ofertas recentes. |
| Modelos de grupo de compras | Gerar modelos de função do grupo de compras para produtos específicos e revisar os mapeamentos de persona recomendados. Refine modelos incluindo ou excluindo perfis e funções. Valide as funções necessárias antes de criar grupos de compra. |

## Limitações

Os insights do público-alvo dependem da taxonomia de intenção configurada, dos mapeamentos de campo XDM e dos dados do evento de experiência. Dados de oportunidade incompletos, taxonomia ausente ou desatualizada ou identificadores de perfil e conta ausentes podem reduzir a confiabilidade da insight.

O cálculo de intenção usa apenas estes eventos de experiência: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` e `web.webpagedetails.pageViews`.

## Exemplos de prompt

Digite os seguintes prompts na interface [!DNL CX Coworker] para explorar a intenção de conta, entender pessoas e personalidades e preparar modelos de grupos de compra.

### Tentativa de conta

Explore o interesse da conta em produtos e analise as alterações de intenção.

* Mostrar a janela de tendência: atualizações mais antigas e mais recentes da intenção de produto da conta por produto.
* Quais contas têm pouca intenção para qualquer produto, mas ainda têm oportunidades em aberto (que valha a pena cuidar)?
* Quais novos sinais de intenção foram gravados para `<account_name>` esta semana?

### Pessoas e personalidades

Identifique perfis associados a interesses de produtos e revise as funções de grupo de compras recomendadas.

* Mostre-me os perfis associados a `<product>`.
* Mostre-me a recomendação de mapeamento de função para pessoa para `<product>`.
* Para `<product>`, liste perfis e funções com suas métricas de oportunidade (taxa de ganho, taxa de associação, contagens).

### Comprando grupos e modelos

Revise a intenção e a cobertura do grupo de compras e gere ou refine os modelos.

* Para `<product>`, liste os grupos de compras com intenção de produto e pontuações.
* Para contas em `<industry>`, qual é a cobertura de persona média da conta para `<product>`?
* Criar um modelo de grupo de compra para `<product>`.
* Crie um modelo de grupo de compra para `<product>` sem a persona `<persona>` e remova a função `<role>`.

## Conceitos

Use esses conceitos para interpretar a intenção da conta, as classificações de persona e as recomendações de grupo de compras.

| Conceito | Explicação |
| ------- | ----------- |
| Detecção de público | Analise sinais de engajamento primários entre as pessoas em uma conta para identificar o interesse do produto e os perfis relevantes. A análise considera os 18 meses anteriores de atividade, incluindo a atividade antes do fechamento da oportunidade. Os padrões de engajamento podem indicar a intenção do produto quando os dados da oportunidade estão incompletos, mas a ausência de dados pode reduzir a confiabilidade da insight. |
| Persona | As personalidades agrupam as pessoas por cargo, função e antiguidade normalizados. Use perfis para entender quem está se envolvendo em uma conta, incluindo tomadores de decisão, influenciadores e funções de suporte. |
| Mapeamento de funções de grupos de compra | Mapeie personas para funções de grupos de compra específicas do produto com base no cargo, função, antiguidade e atributos configurados. Essas funções representam as pessoas em uma conta que influenciam ou decidem sobre uma compra. Revise a cobertura para identificar funções ausentes. |
| Dados de oportunidade para classificação de persona | O estágio de oportunidade, a data de fechamento e os mapeamentos de oportunidade para produto oferecem suporte à classificação de persona para cada produto. Quando os dados da oportunidade estão incompletos, a classificação usa o volume de atividade e o declínio de tempo para dar mais peso à atividade recente.<br/><br/>A vinculação de produtos usa uma tabela de mapeamento de oportunidade para produto fornecida ou gerada quando disponível. Caso contrário, a correspondência difusa vincula oportunidades a produtos. Se nenhuma vinculação estiver disponível, a intenção do produto será inferida a partir da atividade recente antes da data de fechamento da oportunidade. Esses métodos de fallback não eliminam as limitações de confiabilidade dos dados incompletos. |
| Análise de oportunidade | A análise de oportunidade histórica usa três dimensões para identificar padrões de persona associados aos resultados de compra:<ul><li>Taxa de vitórias: mede a frequência com que as oportunidades são conquistadas quando pessoas específicas estão envolvidas. Padrões de personalidade associados com maiores taxas de ganho recebem mais peso.</li><li>Taxa de associação: mede a frequência com que uma pessoa aparece em oportunidades para um determinado produto.</li><li>Influência pessoal: mede como o engajamento ou a atividade pessoal se correlaciona com vitórias, além de se a persona estiver presente.</li></ul>Esses sinais informam a intenção da conta, o mapeamento de persona e as recomendações do grupo de compra. |
| Intenção | A intenção indica o interesse do produto por meio do engajamento, como visitas à página da Web ou cliques em links de email. A taxonomia de produtos conecta a atividade de engajamento a palavras-chave, produtos e categorias de produtos. A profundidade e a frequência do engajamento determinam as pontuações de intenção individuais para cada palavra-chave, produto ou categoria de produto.<br/><br/>As pontuações indicam intensidade de interesse: `<=0.2`, intenção de Medium: `0.2 < score <= 0.6`, intenção alta: `0.6 < score <= 1`.<br/><br/>As pontuações de intenção individuais são agregadas entre pessoas na mesma conta para determinar a intenção de conta. |
| Funções que influenciam um grupo de compras | As funções de grupo de compra representam diferentes contribuições para uma decisão de compra. _Tomadores de decisão_ normalmente controlam aprovações de orçamento. _Influenciadores_, avaliação de forma e recomendações. _Campeões_ criam um consenso interno. _Usuários Finais_ validam a adequação do produto.<br/><br/>Revise as atribuições de funções e a cobertura para entender quem influencia a decisão e onde as lacunas de engajamento permanecem. |
| Cobertura de pessoa ou função | A cobertura mede quantas pessoas ou funções esperadas têm pelo menos um representante em uma conta. Para um produto com as personalidades ou funções esperadas _N_, cobertura completa significa que todos os _N_ estão representados. Cobertura parcial significa que alguns estão ausentes. Use a cobertura para avaliar a integridade do grupo de compras e identificar lacunas. |

## Pré-requisitos de dados XDM

Configure os seguintes mapeamentos de campo XDM para oferecer suporte à análise de intenção de conta, identificação de pessoa e mapeamento de função de grupo de compra.

### Mapeamento de campo XDM

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entidade</th>
      <th>Definição de negócios</th>
      <th>Detalhes adicionais</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfis</span>
        </p>
      </td>
      <td>Identificador da conta, usado em associações para dados de oportunidade, evento e intenção</td>
      <td rowspan="2">Análise de oportunidade<br/>Exploração de conta<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfis</span>
        </p>
      </td>
      <td>Identificador de pessoa, usado em associações envolvendo dados do evento para dados de perfil</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span> Perfis</span>
        </p>
      </td>
      <td>Departamento de Trabalho do perfil/pessoa</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Mapeamento de persona</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span> Perfis</span>
        </p>
      </td>
      <td>Cargo do perfil/pessoa usado no cálculo da persona</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>pessoa.nome.primeiroNome</span>
        </p>
      </td>
      <td>
        <p>
          <span >Perfis</span>
        </p>
      </td>
      <td>Exibe o nome da pessoa nos resultados que correspondem à sua consulta.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Perfis</span>
        </p>
      </td>
      <td>Exibe o nome completo da pessoa nos resultados que correspondem à sua consulta.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>pessoa.nome.sobrenome</span>
        </p>
      </td>
      <td>
        <p>
          <span> Perfis</span>
        </p>
      </td>
      <td>Exibe o sobrenome da pessoa nos resultados que correspondem à sua consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> Contas</span>
        </p>
      </td>
      <td>Identificador da conta, usado em associações para dados de oportunidade, evento e intenção</td>
      <td>Análise de oportunidade<br/>Exploração de conta</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Contas</span>
        </p>
      </td>
      <td>Exibe o nome da conta nos resultados que correspondem à sua consulta.</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Exploração de Conta</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>descriçãoDaConta</span>
        </p>
      </td>
      <td>
        <p>
          <span>Contas</span>
        </p>
      </td>
      <td>Suporta filtragem de conta por descrição de conta com base em sua consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span> Contas</span>
        </p>
      </td>
      <td>Oferece suporte à filtragem de conta por setor com base em sua consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span> Contas</span>
        </p>
      </td>
      <td>Oferece suporte à filtragem de conta por região de endereço de faturamento com base na sua consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Identificador da conta, usado em associações para dados de oportunidade, evento e intenção</td>
      <td rowspan="2">
        <p>Análise de Oportunidade<br/>Exploração de Conta</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Identificador de oportunidade, usado em associações para dados de conta</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Oportunidade</span>
        </p>
      </td>
      <td>Nome da oportunidade usado na análise da oportunidade.</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Análise de oportunidades</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Se a oportunidade foi conquistada (binária)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>descriçãoDaOportunidade</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Descrição da oportunidade usada na análise da oportunidade.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityAmount</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Valor de $ envolvido na oportunidade</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>opportunityType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Tipo de oportunidade</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityStage</span>
        </p>
      </td>
      <td>
        <p>
          <span> Oportunidade</span>
        </p>
      </td>
      <td>Estágio da Oportunidade (fechado ganho ou fechado perdido ou qualquer um dos estágios intermediários) </td>
      <td rowspan="4">
        <p>Análise de oportunidade<br/>Exploração de conta</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>atualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Data real de fechamento da oportunidade</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> Oportunidade</span>
        </p>
      </td>
      <td>Data de fechamento esperada da oportunidade</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidade</span>
        </p>
      </td>
      <td>Data de criação desta oportunidade</td>
    </tr>
  </tbody>
</table>

### Dados de taxonomia

As habilidades do público usam dados de intenção própria de [!DNL Adobe Journey Optimizer B2B Edition]. O cálculo de intenção conecta a taxonomia do produto com a atividade de envolvimento e agrega pontuações individuais no nível da conta.

1. O cálculo de intenção requer dados de taxonomia (produtos do cliente e palavras-chave correspondentes) de Clientes > Taxonomia
1. Os dados de taxonomia são usados para rotular dados do evento (rotulagem de ativos). Esses dados fornecem insights sobre em quais palavras-chave e produtos os visitantes estão interessados com base nos dados do evento > Rotulagem de ativos 
1. Os ativos rotulados (dados do evento) são combinados com os comportamentos do visitante (número de páginas visitadas) para determinar a intenção do visitante no nível de palavra-chave, produto e categoria de produto → Cálculo de intenção
1. As pontuações de intenção em um nível de perfil do visitante são agregadas em nível de conta para determinar a intenção da conta em uma determinada palavra-chave, produto e categoria de produto > Agregação de conta de intenção

Os seguintes campos são obrigatórios além de [configurar a taxonomia de intenção](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entidade</th>
      <th>Definição de negócios</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>perfil de pessoa</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfil</span>
        </p>
      </td>
      <td>Ajuda a identificar um identificador de pessoa (email ou b2b_person)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfil</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Usado como uma taxonomia para rotular ativos (eventos de experiência, como emails clicados, páginas da Web visitadas)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>carimbo de data/hora</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Usado para obter preenchimento retroativo e execução incremental</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Identifica o tipo de evento. O cálculo de intenção usa apenas <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> e <code>web.webpagedetails.pageViews</code>.
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/contabilidade; Informações sobre o nome da campanha</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/escrituração; Informações sobre a ID de origem para a qual o email é direcionado</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/escrituração contábil; Informações da instância de origem para a qual o email é direcionado</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Usado para buscar o conteúdo de email do data center do [!DNL Adobe Marketo Engage]. Ele inclui (SourceID@SourceInstanceID.SourceType).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/escrituração contábil; Informações sobre o tipo da origem ou de onde a origem se originou </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Informações sobre a origem da visita à página web</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>URL real usado para obter conteúdo</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Parâmetro de consulta adicional para o URL usado para buscar conteúdo direcionado </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>apenas para referência/contabilidade</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/escrituração; Informações sobre a ID de origem para a qual o email é direcionado</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiência</span>
        </p>
      </td>
      <td>Somente para referência/escrituração contábil; Informações sobre a instância de origem para a qual o email foi direcionado</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Evento de experiência</span>
      </td>
      <td>Somente para referência/escrituração contábil; é composto de (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Evento de experiência</span>
      </td>
      <td>Somente para referência/escrituração contábil; Informações para o tipo de origem ou de onde a origem é</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Evento de experiência</span>
      </td>
      <td>Usado para buscar o URL real se web.webPageDetails.name não o possuir.</td>
    </tr>
  </tbody>
</table>
