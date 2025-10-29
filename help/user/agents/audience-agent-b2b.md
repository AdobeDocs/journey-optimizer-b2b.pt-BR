---
title: Audience Agent para B2B
description: Audience Agent B2B no Jornada OtimizerB2B Edition usa análise de intenção e mapeamento de persona para criar grupos de compra e acelerar workflows de marketing B2B.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent para B2B

Equipado com o [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), o Audience Agent B2B está disponível no Journey Optimizer B2B edition. O uso desse agente melhora a eficiência e a eficácia na exploração e dimensionamento de públicos, acelerando a criação de grupos de compra e fluxos de trabalho contínuos para ativação de jornada:

* **_Priorizar públicos-alvo por intenção_**: inferir personalidades com base na intenção do produto para vários públicos-alvo e simplificar o planejamento de campanha, reduzindo o tempo gasto na validação do público-alvo.

* **_Aproveite a IA para detectar grupos de compras_**: use a IA, dados estruturados, não estruturados e dados unificados de terceiros para simplificar a descoberta e a criação de grupos de compras.

![Audience Agent para B2B no modo de página inteira](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Para usar o Audience Agent para B2B, são necessários definições e mapeamentos de dados:<br/>
>
>* [Taxonomia/mapeamento de dados de intenção](../admin/intent-data.md)
>* [Taxonomia/mapeamento de campo XDM](#xdm-data-prerequisites)

## Audience Agent para recursos B2B

| Área | O que faz | Valor comercial |
| ---- | ------------ | -------------- |
| Análise de intenção | <li> Meça a intensidade da intenção da conta (como baixa, média e alta) para produtos específicos. <li>Comparar tendências de interesse de produtos ao longo do tempo (como os principais produtos dos últimos _n_ dias). <li>Identificar contas que mostram ativamente interesse em produtos específicos. <li>Padrões de envolvimento de superfície que combinam atividade da conta com cobertura de persona. | <li>Ajuda as equipes a se concentrarem nas contas certas na hora certa. <li>Melhora a qualidade do pipeline ao priorizar contas com sinais de compra genuínos. <li>Permite o engajamento pró-ativo antes que os concorrentes ajam. |
| Mapeamento pessoal | <li>Detecte e classifique os principais perfis por intenção de produto. <li>Identifique os perfis envolvidos na compra de um ou vários produtos. <li>Mapeie personas para funções funcionais (como _Especialista_, _Decisor_ e _Influenciador_) com justificativa. <li>Validar por que uma determinada pessoa é considerada um campeão. | <li>Garante que a equipe de vendas envolva os verdadeiros responsáveis pelas decisões e influenciadores. <li>Reduz o desperdício de esforços em contatos de baixo impacto. <li>Aumenta as taxas de ganho ao alinhar o alcance com a dinâmica do poder do comprador. |
| Avaliação do grupo de compras | <li>Avalie o tamanho do grupo de compras (por exemplo, grupos com mais de _n_ membros). <li>Meça a cobertura de persona entre contas (por exemplo, abaixo de _x_%). <li>Rastrear a distribuição de funções e as lacunas de cobertura nos grupos de compra. <li>Destaque as contas com campeões identificados em ofertas recentes. | <li>Revela lacunas de cobertura que podem impedir os negócios. <li>Fortalece as estratégias de múltiplos processos, garantindo uma representação completa das funções. <li>Melhora o rastreamento da integridade do negócio por meio de insights de engajamento no nível do grupo. |

## Exemplos de prompt

Estes exemplos de prompts demonstram algumas maneiras pelas quais você pode usar o agente:

* Mostrar a janela de tendência: atualização mais antiga e mais recente da intenção de produto por produto da conta.
* Para `<product>`, liste os grupos de compras com intenção de produto e pontuações.
* Para `<product>`, liste perfis e funções com suas métricas de oportunidade (taxa de ganho, taxa de associação, contagens).
* Para contas em `<industry>`, qual é a cobertura de persona média da conta para `<product>`?
* Quais contas têm pouca intenção para qualquer produto, mas ainda têm oportunidades em aberto (que valha a pena cuidar)?
* Quais contas adicionaram novos sinais de intenção para `<account_name>` esta semana?

## Conceitos

| Conceito | Explicação |
| ------- | ----------- |
| Detecção de público | Nos bastidores, o agente observa sinais de intenção próprios com base em duas coisas: o grau de engajamento das pessoas com a sua marca e os tipos de personalidades que elas representam. A análise retroage os últimos 18 meses de atividade para detectar a intenção do produto em todos na conta, especialmente durante o tempo que antecede o fechamento de uma oportunidade. Essa análise ajuda o agente a destacar a pessoa mais propensa a influenciar o negócio.<br/><br/>Às vezes, as contas não têm todos os dados de oportunidade em perfeito estado, o que é correto, e o agente ainda pode detectar a intenção do produto apenas com base nos padrões de envolvimento. |
| Persona | As personalidades representam os tipos de pessoas que se envolvem em uma conta. O agente o cria observando o cargo, a função e o nível de antiguidade e, em seguida, normalizando essas informações para que sejam consistentes em diferentes contas. Dessa forma, em vez de se perder em títulos confusos, você pode ver rapidamente se está atingindo tomadores de decisão, influenciadores ou funções de suporte. Personas ajudam você a entender quem está demonstrando interesse, não apenas quanto interesse há. <br/><br/> Quando o agente mapeia personas para funções de grupo de compras, ele seleciona o tipo de persona identificada com base no cargo, função, antiguidade e qualquer outro atributo que você queira adicionar e alinha-os às funções que provavelmente serão desempenhadas em uma decisão de compra, como _tomador de decisão_, _influenciador_ ou _campeão_. Essas funções são relevantes para o produto específico em questão, para que você possa ver quem é mais importante para essa oportunidade. O agente também mostra cobertura para cada função, ajudando você a entender rapidamente quais funções estão bem representadas e onde pode haver lacunas para preencher sua estratégia de envolvimento. |
| Mapeamento de funções de grupos de compra | Depois que as personas são mapeadas para funções, você as reúne em um grupo de compra. Pense nisso como a equipe completa dentro da conta que provavelmente influenciará ou decidirá sobre a compra. Cada função (como _tomador de decisão_, _influenciador_ ou _campeão_) adiciona uma parte da imagem, para que você tenha uma visão clara de todo o comitê que orienta o negócio. <br/><br/> Ao mapear personas para funções de grupo de compras, você seleciona o tipo de persona identificada com base no cargo, função, antiguidade e qualquer outro atributo que desejar adicionar, e alinha-os à função que eles provavelmente desempenharão em uma decisão de compra, como _tomador de decisão_, _influenciador_ ou _campeão_. Essas funções são relevantes para o produto específico em questão, para que você possa ver quem é mais importante para essa oportunidade. O agente mostra a cobertura de cada função, ajudando você a entender rapidamente quais funções estão bem representadas e onde pode haver lacunas para preencher sua estratégia de envolvimento. |
| Grupos de compra | Os grupos de compra permitem que os profissionais de marketing gerenciem a verdadeira complexidade dos comitês de compra, não de leads isolados ou contas. O Adobe Journey Optimizer B2B edition oferece as ferramentas (insights orientados por IA, jornadas com base em funções e rastreamento de integridade) para trazer estrutura, personalização e clareza analítica a esse processo, alinhando, em última análise, o marketing e as vendas mais estreitamente aos resultados da receita.<br/><br/>Criar um grupo de compras significa reunir três itens principais: o público-alvo correto, o contexto do produto e as funções do grupo de compras. Veja a seguir uma visualização passo a passo de como funciona: <ol><li>**Identificar seu público-alvo** <ul><li>Primeiro, o agente descobre as contas que são mais relevantes para seu produto. Essa descoberta inclui contas que já mostram juros e contas com potencial.<li>Nessas contas, ele identifica as pessoas (seus principais perfis) que podem influenciar ou fazer parte da decisão de compra.<li>Ele escolhe entre as contas a serem exibidas: uma lista de contas ou um público-alvo de conta.</ul><li>**Considere o contexto do produto**<ul><li>Em seguida, ele analisa o produto ou a solução em que você está se concentrando, o que garante que as personalidades identificadas sejam realmente relevantes para o que você deseja vender ou promover.<li>Também ajuda a destacar qualquer lacuna na cobertura (talvez determinadas funções estejam ausentes no produto) para que você saiba onde se concentrar.</ul> <li>**Mapear personas para funções de grupo de compra** <ul><li>Por fim, o agente mapeia essas personas para funções específicas de grupos de compra, como tomadores de decisão, influenciadores e campeões.<li>Com base nesse mapeamento, o agente pode recomendar uma composição de grupo de compra para você, que pode ser revisada, ajustada ou confirmada.</ul> </ol> Quando esses três componentes se unem, ele cria seu grupo de compra, completo com detalhes, funções e insights do membro prontos para uso. |
| Comprar grupos em uma jornada | Dentro de uma jornada, um grupo de compra pode ser usado como a unidade central de orquestração, o que permite que os profissionais de marketing projetem experiências que se adaptam à dinâmica do grupo em vez de tratar os membros de forma isolada. Por exemplo, você pode direcionar todo o grupo com mensagens coordenadas e, ao mesmo tempo, personalizar o conteúdo específico de função para tomadores de decisão, influenciadores ou usuários finais. À medida que os sinais de intenção e o fluxo de dados de envolvimento no, as jornadas podem se ramificar com base na disponibilidade do grupo, exibir alertas para vendas quando as funções críticas se envolvem ou acionar automaticamente etapas de criação se os perfis principais estiverem ausentes. Esse fluxo garante que cada ponto de contato (de emails a anúncios baseados em conta a alcance de vendas) trabalhe em conjunto para fazer o grupo avançar em seu processo de compra, acelerando o consenso e reduzindo o atrito no caminho para a compra. |
| Jornadas no Journey Optimizer B2B edition | Uma jornada pode ser criada com ou sem um grupo de compras, mas o nível de precisão e impacto muda significativamente:<ul><li>**Sem um grupo de compra**, as jornadas normalmente são criadas em torno de contas. Os profissionais de marketing ainda podem usar sinais como intenção, comportamento ou interesse no produto para acionar fluxos de criação e alcance externo. Esse método funciona para movimentos mais simples ou quando você tem dados limitados sobre uma conta. No entanto, corre o risco de ignorar o conjunto mais amplo de partes interessadas que influenciam o acordo, o que pode retardar a conversão ou causar lacunas no engajamento.<li>**Com um grupo de compra**, as jornadas são orquestradas em torno do conjunto completo de personalidades envolvidas em uma decisão de compra. Você pode alinhar etapas a marcos em nível de grupo (como quando o comitê atinge uma pontuação de integridade ou mostra engajamento coletivo), enquanto também personaliza pontos de contato para cada função. Esse método permite projetar o envolvimento coordenado de vários segmentos: um tomador de decisões pode receber conteúdo estratégico de ROI, enquanto os influenciadores recebem aprofundamentos sobre os produtos, e as vendas são alertadas quando as funções críticas se envolvem. Ao mapear a jornada individual e coletiva, profissionais de marketing e vendedores podem acelerar a criação de consensos e fazer com que as oportunidades avancem com mais eficiência. </ul> |
| Usar dados de oportunidade para detectar persona | Para fornecer a visão mais precisa de quem está se envolvendo e onde estão seus interesses, o agente aborda a classificação de persona e a intenção do produto de acordo com o seguinte: <ul><li>Cenário mais adequado: se você puder fornecer dados como _Estágio da oportunidade_, _Data de fechamento da oportunidade_ e um _Mapeamento de oportunidade para produto_ claro, o agente poderá classificar personas com confiança por produto.<li>Essa classificação fornece uma compreensão precisa do engajamento e interesse na conta. </ul>Mas o agente sabe que os dados nem sempre estão completos, o que está correto. Ele inclui fallbacks inteligentes para manter as coisas em movimento:<ul><li>O agente analisa o volume de atividades, dando mais peso às recentes usando o declínio de tempo.<li>Essa ponderação permite que o agente diferencie e classifique perfis, mesmo sem dados de oportunidade completos. </ul>Quando se trata de vincular oportunidades a produtos, veja como o agente lida com isso:<ul><li>_Ideal_: você fornece ou ajuda ao agente para criar a tabela de mapeamento.<li>_Se não estiver disponível_: o agente usa a correspondência difusa para conectar os pontos.<li>_Nenhuma vinculação_: o agente infere a intenção do produto com base em atividades recentes anteriores à data de fechamento.</ul>Essa abordagem em camadas garante que o agente ainda possa fornecer insights significativos, mesmo quando os dados não são perfeitos. |
| Análise de oportunidade | O agente examina os dados históricos da oportunidade para entender quais fatores preveem uma vitória com mais intensidade e usa três dimensões principais para fazer isso:<ol><li>Taxa de vitórias: mostra a frequência com que as negociações são fechadas com êxito quando determinadas personalidades estão envolvidas. Se as contas com um padrão de persona específico (como um avaliador técnico ou um tomador de decisão de nível VP) tendem a converter mais frequentemente, o modelo oferece maior peso a esse padrão. Essas informações representam um percentual do total de oportunidades, como oportunidades fechadas ou ganhas.<li>Taxa de associação: mede a frequência com que um tipo de pessoa é exibido entre oportunidades para um determinado produto. Se determinadas pessoas aparecem consistentemente em negociações bem-sucedidas, isso indica que elas desempenham uma função crítica no processo de compra.<li>Influência pessoal: quantifica o quanto uma determinada pessoa contribui para o resultado, não apenas se ela está presente, mas como seu envolvimento ou nível de atividade se correlaciona com as vitórias.</ol>Juntos, esses sinais ajudam a inferir quais perfis têm mais impacto nos resultados da compra, mesmo quando os dados da oportunidade estão incompletos. Com o tempo, ele permite que o sistema exiba perfis e padrões de alto impacto mais preditivos do sucesso do negócio, que informam a intenção da conta, o mapeamento da pessoa e as recomendações do grupo de compras. |
| Intenção | Quando alguém visita uma página da Web ou clica em um link de email relacionado a um produto, isso é um sinal de que está interessado, e é chamado de _intenção_.<br/><br/>O agente começa com uma taxonomia, que é basicamente uma lista dos produtos do cliente e as palavras-chave que os descrevem. Essas informações ajudam o agente a entender sobre o que se trata cada parte do conteúdo ou interação.<br/><br/>Em seguida, o agente usa essa taxonomia para rotular a atividade do visitante, como a quais palavras-chave ou produtos suas ações estão relacionadas.<br/><br/>Em seguida, o agente verifica a intensidade do envolvimento de alguém, como a quantidade de páginas que visita ou a frequência com que interage. Ela usa essas informações para calcular sua pontuação de intenção individual para palavras-chave, produtos ou categorias de produtos específicas. Ele agrupa cada pontuação de intenção na intenção _Alta_, _Medium_ ou _Baixa_ para indicar a intensidade do interesse. (Baixa intenção: `<=0.2`, intenção do Medium: `0.2 < score <= 0.6`, Alta intenção: `0.6 < score <= 1`)<br/><br/>Por fim, o agente combina as pontuações de intenção de todas as pessoas da mesma empresa (conta) para ver a intenção geral no nível da conta, mostrando em quais produtos ou tópicos essa empresa parece estar mais interessada. |
| Funções que influenciam um grupo de compras | Cada grupo de compras é composto de funções que contribuem de forma diferente para a decisão de compra, como _Decisor_, _Influenciador_, _Campeão_ e _Usuário Final_. Cada função tem vários graus de impacto.<br/><br/>Os tomadores de decisão têm mais influência e geralmente controlam as aprovações de orçamento. Os influenciadores moldam a avaliação e as recomendações. Os especialistas ajudam a criar um consenso interno, enquanto os usuários finais validam o ajuste do produto.<br/><br/>Ao mostrar essas funções, o agente ajuda você a entender quem está conduzindo a decisão de compra, onde seu engajamento é mais forte e onde podem existir lacunas de cobertura. Essas informações permitem que você se concentre nas funções mais importantes para esse produto. |
| Cobertura de pessoa ou função | Para qualquer produto, geralmente há um conjunto de funções e personalidades principais que são conhecidas por influenciar a compra (_N_ personas ou funções).<br/><br/>Para cada conta, o agente calcula a cobertura verificando quantas dessas _N_ funções são representadas por pelo menos uma pessoa nessa conta.<br/><br/>Se todas as funções de _N_ estiverem presentes, a conta terá cobertura total. Se apenas algumas funções forem representadas, a cobertura é parcial.<br/><br/>Em termos simples, a cobertura de funções e personalidades mede a conclusão do seu grupo de compras para um produto, com base no fato de todos os tomadores de decisão, influenciadores e campeões importantes estarem incluídos. |

## Pré-requisitos de dados XDM

O Audience Agent fornece insights sobre contas que mostram a intenção própria de produtos e calcula perfis e funções com base nos dados definidos. Verifique se os seguintes dados de pré-requisito estão configurados para usar os recursos do Audience Agent:

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
          <span>  Perfis</span>
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
          <span>  Perfis</span>
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
      <td>Nome da pessoa, usado pelo Audience Agent para exibir nomes na interface do usuário quando atendido por qualquer critério</td>
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
      <td>Nome completo da pessoa, usado pelo Audience Agent para exibir nomes na interface do usuário quando atendido por qualquer critério</td>
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
      <td>Sobrenome da pessoa, usado pelo Audience Agent para exibir nomes na interface do usuário quando atendido por qualquer critério</td>
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
      <td>Nome da conta usada pelo Audience Agent para exibir na interface do usuário quando atendido por qualquer critério apresentado na consulta do usuário</td>
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
      <td>Descrição da conta/empresa usada pelo Audience Agent para aplicar o filtro em contas com base na consulta do usuário na interface </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Contas</span>
        </p>
      </td>
      <td>Setor de conta/empresa usado pelo Audience Agent para aplicar filtro em contas com base na consulta do usuário na interface </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Contas</span>
        </p>
      </td>
      <td>Endereço de cobrança da conta/empresa usada pelo Audience Agent para aplicar o filtro em contas com base na consulta do usuário na interface </td>
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
      <td>Nome da oportunidade usada pelo Audience Agent </td>
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
      <td>se a oportunidade foi conquistada (binário)</td>
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
      <td>Descrição da oportunidade usada pelo Audience Agent </td>
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

O Audience Agent utiliza a intenção própria detectada no Journey Optimizer B2B edition:

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
      <td>Obtenha o tipo de evento, pois o agente processa apenas quatro eventos (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscribed, web.webpagedetails.pageViews)</span>
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
      <td>Somente para referência/manutenção de livro; informações sobre o nome da campanha</td>
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
      <td>Somente para referência/manutenção de livro; informações sobre a ID de origem para a qual o email é direcionado</td>
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
      <td>Somente para referência/manutenção de livro; informações da instância de origem para a qual o email é direcionado</td>
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
      <td>Usado para buscar o conteúdo de email do data center da Marketo Engage; é composto de (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Apenas para referência/manutenção de livros; Informações sobre o tipo de fonte ou a origem da fonte </td>
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
      <td>Informações sobre a origem de origem para a qual o email é direcionado</td>
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
      <td>apenas para referência/manutenção de livros</td>
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
      <td>Somente para referência/manutenção de livro; informações sobre a ID de origem para a qual o email é direcionado</td>
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
      <td>Somente para referência/manutenção de livro; informações sobre a instância de origem para a qual o email foi direcionado</td>
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
      <td>Somente para referência/manutenção de livros; é composto de (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Apenas para referência/escrituração; Informações relativas ao tipo de fonte ou à origem da fonte</td>
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
