---
title: Grupos de compra
description: Saiba como os grupos de compra no Journey Optimizer B2B Edition podem aumentar a eficácia do marketing por identificar e direcionar membros para suas listas de conta.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: ada98f505aad848f958cf8325ed90d66692a6cac
workflow-type: tm+mt
source-wordcount: '2151'
ht-degree: 57%

---


# Grupos de compra

As contas são fundamentais para qualquer estratégia de atividades de vendas e marketing B2B. Cada conta tem um grupo de pessoas associado, as quais podem ser funcionários ou profissionais contratados que trabalham com a conta. As contas são hierárquicas e produtos diferentes podem ser vendidos em diferentes níveis na hierarquia. Por exemplo, a Adobe Experience Platform pode ser vendida no nível corporativo a uma conta de nível superior. E o Adobe Photoshop pode ser vendido a uma conta que representa uma divisão ou departamento dentro de uma organização, como um departamento de design dentro de uma corporação maior.

![Diagrama de funções da conta](assets/account-roles-diagram.png){width="800"}

A conta pode conter um subconjunto de pessoas que compõe o _grupo de compra_. Essas são as pessoas que tomam a decisão de compra final; portanto, elas precisam de atenção especial de profissionais de marketing e podem precisar de acesso a informações diferentes em comparação com as outras pessoas associadas à conta. Os grupos de compra podem incluir um grupo diferente de pessoas para diferentes linhas de produtos ou ofertas. Por exemplo, um produto de segurança cibernética pode normalmente exigir um CIO ou CIO e um representante do departamento jurídico para aprovar uma compra. Um produto de rastreamento de erros normalmente tem um VP de Engenharia e um Diretor de TI como membros do grupo de compras.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Componentes principais

Você pode aumentar a eficácia do marketing estabelecendo grupos de compras no Journey Optimizer B2B edition que identificam membros para suas listas de contas de destino com base nas soluções pelas quais suas equipes de vendas são responsáveis. Antes de você e sua equipe de marketing começarem a criar seus grupos de compra, verifique se você tem os componentes principais definidos. Esses componentes são essenciais para atingir suas metas e objetivos de negócios.

| Componente | Finalidade |
| --------- | ------- |
| Interesse na solução | Esse componente fornece a resposta para: <ul><li>O que você está vendendo como organização de marketing?</li><li>Que produto ou coleção de produtos você pretende vender?</li></ul>  **_Exemplo:_** Venda cruzada do novo Produto X para clientes existentes |
| Público-alvo de conta | Esse componente fornece a resposta para: <ul><li>Para quem você está vendendo?</li><li>Qual é a lista de contas que você está direcionando?</li></ul> **_Exemplo:_** Segmento de conta definido por contas com o Produto Y com receita superior a 1 milhão |
| Modelos de função do grupo de compra | Esse componente fornece a resposta para: <ul><li>Quais funções você está direcionando?</li><li>Qual conjunto de regras é usado para determinar quem está atribuído às funções do grupo de compra?</li></ul>  **_Exemplo:_** Atribuir uma pessoa com título de CMO à função de Tomador de Decisão |
| Estágios do grupo de compra | (Opcional) Este componente fornece a resposta para: “Como o grupo de compra está conduzindo o sucesso ou o fracasso?” |

## Atribuição de membro

Há três maneiras pelas quais os membros são atribuídos ou removidos de um grupo de compra. A lista a seguir descreve esses métodos de adição e remoção na ordem de precedência. O método mais alto tem a precedência mais alta e um mais baixo não pode substituí-lo.

1. **_Ação manual_** - Uma ação manual de adição ou remoção de membro executada por um usuário de vendas para o grupo de compras
2. **_ação de Jornada_** - Jornada [nós de ação para associação de grupo de compras](../journeys/action-nodes.md#add-a-people-based-action) (_Atribuir ao grupo de Compras_ ou _Remover do grupo de Compras_)
3. **_Trabalhos do sistema_** - [Criação](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) do grupo de compras e trabalhos de manutenção.

Para garantir que a atribuição de membro em um grupo de compra não seja substituída incorretamente, essa lista está na ordem de precedência seguida no sistema para garantir uma atribuição de membro precisa. Por exemplo, quando um usuário de vendas adiciona manualmente um membro ao grupo de compras, ele não deseja que um trabalho de manutenção altere essa adição. Usando a ordem de precedência, os seguintes cenários são aplicados:

* Se um usuário atribuir manualmente um membro a um grupo de compras, e isso for seguido por um trabalho de manutenção de grupo de compras que remove o mesmo membro do grupo de compras, o trabalho de manutenção **não removerá** esse membro e não poderá substituir a atribuição manual.
* Se um usuário atribuir manualmente um membro a um grupo de compras, e isso for seguido por um nó de jornada acionado que remove o mesmo membro do grupo de compras, a ação do nó **não removerá** esse membro e não poderá substituir a atribuição manual.
* Se um nó de ação de jornada disparada adicionar um membro a um grupo de compras, e isso for seguido por um trabalho de manutenção de grupo de compras que remove o mesmo membro do grupo de compras, o trabalho de manutenção **não removerá** esse membro e não poderá substituir a atribuição de ação de jornada.

## Fluxo de trabalho do grupo de compra

1. Criar grupos de compra.

   * Definir [interesse na solução](./solution-interests.md) e [modelo de função](./buying-groups-role-templates.md)
   * [Crie o grupo de compra](./buying-groups-create.md#create-buying-groups) e atribua [estágios do grupo de compra](./buying-group-stages.md).

1. Identificar pessoas desaparecidas por completude.

   Analise o grupo de compra usando filtros.

   **_Exemplo:_** Função de tomador de decisão ausente e pontuação de integridade &lt; 50

1. Conclua as definições de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Adicione ações de grupo de compras às suas jornadas de conta.

## Exibir grupos de compra e componentes

Na navegação à esquerda, expanda **[!UICONTROL Contas]** e clique em **[!UICONTROL Grupos de compra]**.

A página _[!UICONTROL Grupos de compra]_ é organizada em guias:

| Tabulação | Descrição |
| --- | ----------- |
| [!UICONTROL Visão geral] | Esta guia é a padrão e exibe o [painel de grupos de compra](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Procurar] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquise pelo nome do grupo de compras. </li><li>Filtrar por interesse da solução. </li><li>Especificar os detalhes do grupo de compra. </li><li>Crie um grupo de compra. </li></ul> |
| [!UICONTROL Interesses de solução] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de grupos de compra existentes. </li><li>Pesquise pelo nome do grupo de compras. </li><li>Acessar e editar as propriedades de interesse de solução. </li><li>Criar um interesse de solução. </li><li>Excluir um interesse de solução. </li><li>Exibir e excluir trabalhos de grupo de compra. </li></ul> |
| [!UICONTROL Modelos de funções] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir a lista de modelos de funções existentes. </li><li>Pesquisar por nome do modelo de funções. </li><li>Acessar e editar as propriedades e condições do modelo de funções. </li><li>Criar um modelo de funções. </li><li>Excluir um modelo de funções. </li></ul> |
| [!UICONTROL Estágios] | Essa guia oferece suporte às seguintes atividades: <ul><li>Exibir o modelo de estágios existente dos grupos de compra. </li><li>Acessar e editar o modelo de estágios de rascunho do grupo de compra. </li><li>Criar o modelo de estágios do grupo de compra. </li></ul> |

## Pesquisa e filtro do grupo de compra

Use a guia _[!UICONTROL Procurar]_ para visualizar a lista de grupos de compra. É possível pesquisar por nome e filtrar a lista por interesse de solução.

![Página procurar do grupo de compra](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Detalhes do grupo de compra

Para acessar os detalhes de um grupo de compra, clique no nome do grupo de compra na guia _[!UICONTROL Procurar]_. [Saiba mais](./buying-group-details.md)

![Detalhes do grupo de compra](assets/buying-group-details.png){width="600" zoomable="yes"}

### Pontuação de integridade do grupo de compra

A pontuação de integridade é usada para determinar se o grupo de compra está completo, o que significa que os membros certos foram atribuídos às funções e ele está pronto para ser usado em uma jornada de conta. Essa pontuação é uma porcentagem baseada no número de funções no grupo de compra e em quantas funções são atribuídas a pelo menos um lead.

Por exemplo, se houver quatro funções em um grupo de compra e três delas forem atribuídas a pelo menos um lead, o grupo de compra terá uma integridade de 75%.

A pontuação de integridade é recalculada toda vez que um grupo de compra é criado ou atualizado.

### Pontuação de engajamento do grupo de compra

A pontuação de engajamento do grupo de compra é um número para determinar o engajamento dos membros de um grupo de compra com base nas atividades que realizam.

* O cálculo da pontuação de engajamento é iniciado assim que o grupo de compra é gerado.
* Qualquer atividade de entrada realizada por membros do grupo de compra nos últimos 30 dias é usada para calcular a pontuação.
* A pontuação pode diminuir em uma janela de 30 dias e conforme as atividades expiram.
* Há um limite de frequência diário de 20 para cada atividade. Se um membro de um grupo de compra realizar a mesma atividade mais de 20 vezes por dia, a contagem da atividade será limitada a 20.
* A pontuação exibida é arredondada.  Por exemplo, uma pontuação de 75,89999 é exibida como 76.

+++Atividades usadas para pontuação

| Nome da atividade | Descrição | Tipo de engajamento | Contagem máxima de frequência diária | Peso da atividade |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visitar Página Da Web] | Um membro visita uma página da Web | Web | 20 | 40 |
| [!UICONTROL Preencher Formulário] | Um membro preenche e envia um formulário em uma página da Web | Web | 20 | 40 |
| [!UICONTROL Clicar no link] | Um membro clica em um link em uma página da Web | Web | 20 | 40 |
| [!UICONTROL Abrir email] | Um membro abre um email | Email | 20 | 30 |
| [!UICONTROL Clique em Email] | Um membro clica em um link em um email | Email | 20 | 30 |
| [!UICONTROL Abrir email de vendas] | Um membro abre um email de vendas | Email | 20 | 30 |
| [!UICONTROL Clique em Email de Vendas] | Um membro clica em um link em um email de vendas | Email | 20 | 30 |
| [!UICONTROL Momento Interessante] | Um membro tem um momento interessante | Preparado | 20 | 60 |
| [!UICONTROL Toque em Notificação por push] | Um membro recebe uma notificação por push | Dispositivos móveis | 20 | 30 |
| [!UICONTROL Atividade do aplicativo móvel] | Um membro executa uma atividade em um aplicativo móvel | Dispositivos móveis | 20 | 30 |
| [!UICONTROL Sessão de Aplicativo Móvel] | Um membro está ativo em uma sessão de aplicativo móvel | Dispositivos móveis | 20 | 30 |
| [!UICONTROL Preencher Formulário De Anúncios De Cliente Em Potencial Do Facebook] | Um membro preenche e envia um formulário de Anúncios em potencial em uma página do Facebook | Redes sociais | 20 | 30 |
| [!UICONTROL Clique em RTP Call to action] | Um membro clica em um call to action personalizado | Web | 20 | 60 |
| [!UICONTROL Exibir mensagem no aplicativo] | Um membro exibe uma mensagem no aplicativo | Dispositivos móveis | 20 | 30 |
| [!UICONTROL Toque Em Mensagem No Aplicativo] | Um membro toca em uma mensagem no aplicativo | Dispositivos móveis | 20 | 30 |
| [!UICONTROL Assinar SMS] | Um membro assina comunicações por SMS | SMS | 20 | 90 |
| [!UICONTROL Responder email de vendas] | Um membro responde a um email de vendas | Email | 20 | 30 |
| [!UICONTROL Engajado com uma caixa de diálogo] | Um membro se envolve com uma caixa de diálogo do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Interagiu com o Documento na Caixa de Diálogo] | Um membro interage com um documento em uma caixa de diálogo do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Reunião agendada na caixa de diálogo] | Um membro agenda um compromisso em uma caixa de diálogo do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Meta da caixa de diálogo atingida] | Um membro atinge uma meta em uma caixa de diálogo do Dynamic Chat |  | 20 | 90 |
| [!UICONTROL Respondeu a uma pesquisa no webinário] | Um membro responde a uma pesquisa em um evento de webinário | Chat | 20 | 90 |
| [!UICONTROL O Call to action clicou no webinário] | Um membro clica em um link do call-to-action em um evento de webinário | Chamada | 20 | 30 |
| [!UICONTROL Downloads de ativos no webinário] | Um membro baixa um arquivo/ativo em um evento de webinário | Evento | 20 | 60 |
| [!UICONTROL Faz perguntas no webinário] | Um membro faz perguntas em um evento de webinário | Evento | 20 | 60 |
| [!UICONTROL Participou do evento] | Um membro participou de um evento | Evento | 20 | 60 |
| [!UICONTROL Engajado com um Agente na Caixa de Diálogo] | Um membro se envolve com um agente em uma caixa de diálogo do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Link Clicado no Chat na Caixa de Diálogo] | Um membro clica em um link em uma caixa de diálogo do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Envolvido com um Fluxo de Conversação] | Um membro se envolve com um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Reunião Agendada em Fluxo de Conversa] | Um membro agenda um compromisso em um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Meta de Fluxo de Conversação Atingida] | Um membro atinge uma meta em um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Interagiu com o Documento no Fluxo de Conversação] | Um membro interage com um documento em um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Envolvido com um Agente em Fluxo de Conversação] | Um membro se envolve com um Agente em um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Link Clicado no Chat no Fluxo de Conversação] | Um membro clica em um link em um fluxo de conversação do Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Clique no Link no SMS V2] | Um membro clica em um link em uma mensagem SMS | SMS | 20 | 90 |

>[!NOTE]
>
>As atividades de pontuação de engajamento são registradas no [log de atividades do Marketo Engage para uma pessoa](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}.

+++

#### Peso

Os usuários podem atribuir _peso_ a cada função no modelo de funções e alocar pesos diferentes a uma função para calcular a pontuação de engajamento.

![Definir o peso para cada função no modelo de funções](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Cada nível de peso é convertido em um valor, que é usado para calcular a pontuação de engajamento:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Baixo] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Vital] = 100

Um modelo de funções com três funções de peso _[!UICONTROL Vital]_, _[!UICONTROL Importante]_ e _[!UICONTROL Normal]_ é convertido nas seguintes porcentagens de peso:

| Função | Peso | Valor do sistema | Cálculo de valor | Porcentagem |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Tomador de decisão | Vital | 100 | 100/240 | 41.67% |
| Influenciador | Importante | 80 | 80/240 | 33,33% |
| Profissional | Normal | 60 | 60/240 | 25% |
|               | Total | 240 |                   |           |

#### Exemplo de cálculo

O exemplo a seguir ilustra o cálculo da pontuação de engajamento usando a porcentagem de peso da função descrita, a contagem de atividades de entrada para cada membro do grupo de compra e um limite diário de 20 contagens para cada evento (se tiver ocorrido várias vezes).

| Função | Membro | Tipo de atividade | Contagem de ontem | Contagem de hoje | Cálculo | Pontuação total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Tomador de decisão | Adam | Site visitado | 37 | 15 | 20 + 15 | 35 |
|               |          | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Site visitado | 5 | 3 | 5 + 3 | 8 |
|               |          | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | PUB baixado | 3 | 2 | 3 + 2 | 5 |
| **Pontuação total de tomadores de decisão** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influenciador | John | Site visitado | 19 | 9 | 19 + 9 | 28 |
| **Pontuação total de influenciadores** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Profissional | Bob | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Email clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | Site visitado | 1 | 7 | 1 + 7 | 8 |
|               |          | PUB baixado | 1 | 2 | 1 + 2 | 3 |
| **Pontuação total de profissionais** |         |             |                 |             |      | **17** |

A pontuação final de engajamento é calculada aplicando o peso de cada uma das pontuações de função:

| Função | Pontuação total da função | % de peso da função | % de peso da pontuação X |
|-------------- |---------------- |------------- |---------------- |
| Tomadores de decisão | 52 | 41.67% | 21,67 |
| Influenciadores | 28 | 33,33% | 9,33 |
| Profissionais | 17 | 25% | 4,25 |
| **Pontuação final de engajamento** |                |             | **35,25** |

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3452936/?learn=on&captions=por_br)
