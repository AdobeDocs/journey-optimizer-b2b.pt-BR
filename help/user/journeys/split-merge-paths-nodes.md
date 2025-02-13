---
title: Dividir e mesclar caminhos
description: Saiba mais sobre os caminhos divididos e os tipos de nó dos caminhos de mesclagem que você pode usar para orquestrar as jornadas de conta no Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 4%

---

# Dividir e mesclar caminhos

Use os nós de caminho dividido e mesclado na jornada da conta para orquestrar as jornadas da conta. Você pode segmentar o público de acordo com as condições definidas e combinar os segmentos para continuar.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Dividir caminhos

Adicione um nó _Split paths_ para definir um ou mais caminhos segmentados com base em atributos de conta ou pessoas.

>[!NOTE]
>
>Há suporte para, no máximo, 25 caminhos.

**Dividir caminhos por contas**: os caminhos divididos por contas podem incluir ações e eventos de contas e pessoas. Esses caminhos podem ser divididos ainda mais.

_Como funciona um caminho dividido por nó de contas?_

* Quando você adiciona um nó de caminho dividido e escolhe _Conta_, cada caminho adicionado inclui um nó final com a capacidade de adicionar nós a cada borda.
* É possível dividir o caminho por Contas repetidamente, por exemplo, de maneira aninhada. Um caminho dividido inclui uma opção para não adicionar o caminho padrão.
* Se uma conta/pessoa não se qualificar para um dos caminhos de divisão, ela não avançará na jornada.
* Esses caminhos podem ser combinados usando um nó de mesclagem.

Nó do ![Jornada - caminhos divididos por conta](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Dividir caminhos por pessoas**: caminhos divididos por pessoas e podem incluir somente ações de pessoas. Esses caminhos não podem ser divididos novamente e se unem automaticamente.

_Como funciona um caminho dividido por nó de pessoas?_

* _Dividir caminho por pessoas_ nós são nós agrupados. Os caminhos se mesclam automaticamente para que todas as pessoas no público-alvo possam avançar para a próxima etapa sem perder o contexto da conta.
* Os nós _Dividir caminho por pessoas_ não podem ser aninhados. Não é possível adicionar um caminho dividido para pessoas em um caminho que esteja nesse nó agrupado.
* Os nós de caminho dividido incluem uma opção para omitir um caminho padrão, de modo que as contas/pessoas sem um caminho correspondente não avancem na jornada.
* Os nós _Dividir caminho por pessoas_ oferecem suporte ao uso de _relações conta-pessoa_, que permitem filtrar pessoas com base em sua função (como contratante ou funcionário em tempo integral), conforme definido nos modelos de funções.

![Nó do Jornada - caminhos divididos por pessoas](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Condições de caminho {#path-conditions}

| Contexto do nó | Condições de caminho | Descrição |
| ------------ | --------------- | ----------- |
| [Contas](#add-a-split-path-by-account-node) | Atributos de contas | Atributos do perfil da conta, incluindo: <li>Receita anual</li><li>Cidade</li><li>País</li><li>Tamanho do funcionário</li><li>Setor</li><li>Nome</li><li>Código SIC</li><li>Estado</li> |
| | [!UICONTROL Filtros especiais] > [!UICONTROL Tem Grupo de Compras] | A conta tem ou não membros de grupos de compras avaliados em relação a um ou mais dos seguintes critérios: <li>Interesse da solução</li><li>Status do Grupo de Compras</li><li>Pontuação de integridade</li><li>Pontuação de envolvimento</li> |
| [Pessoas](#add-a-split-path-by-people-node) > [!UICONTROL Somente atributos de pessoas] | [!UICONTROL Atributos da pessoa] | Atributos do perfil de pessoa, incluindo: <li>Cidade</li><li>País</li><li>Data de nascimento</li><li>Endereço de email</li><li>Email inválido</li><li>Email suspenso</li><li>Nome</li><li>Região inferida</li><li>Nome do cargo</li><li>Sobrenome</li><li>Número do celular</li><li>Número de telefone</li><li>Código postal</li><li>Estado</li><li>Inscrição cancelada</li><li>Motivo do cancelamento de inscrição</li> |
| | [!UICONTROL Histórico de atividades] > [!UICONTROL Email] | Atividades de email associadas à jornada: <li>[!UICONTROL Link clicado no email]</li><li>E-mail aberto</li><li>O email foi entregue</li><li>O email foi enviado</li> Essas condições são avaliadas usando uma mensagem de email selecionada anteriormente na jornada. |
| | [!UICONTROL Histórico de atividades] > [!UICONTROL Valor dos dados alterado] | Para um atributo de pessoa selecionado, ocorreu uma alteração de valor. Esses tipos de alterações incluem: <li>Novo valor</li><li>Valor anterior</li><li>Motivo</li><li>Origem</li><li>Data da atividade</li><li>Número número de vezes</li> |
| | [!UICONTROL Histórico de Atividades] > [!UICONTROL Teve Um Momento Interessante] | Atividade de momento interessante definida na instância associada do Marketo Engage. As restrições incluem: <li>Data importante</li><li>Email</li><li>Web</li> |
| | [!UICONTROL Filtros especiais] > [!UICONTROL Membro do Grupo de Compras] | A pessoa é ou não é um membro do grupo de compra avaliado em relação a um ou mais dos seguintes critérios: <li>Interesse da solução</li><li>Status do Grupo de Compras</li><li>Pontuação de integridade</li><li>Pontuação de envolvimento</li><li>Função</li> |
| | [!UICONTROL Filtros especiais] > [!UICONTROL Membro da Lista] | A pessoa é ou não membro de uma ou mais listas do Marketo Engage. |
| [Pessoas](#add-a-split-path-by-people-node) > [!UICONTROL Somente atributos Account-person] | Função nos atributos da conta | Uma função na conta é atribuída ou não à pessoa. Restrições opcionais: <li>Insira um nome de função</li> |

### Adicionar um caminho dividido pelo nó da conta

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](./assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para a divisão.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

   ![Nó de caminho dividido - adicionar condição](./assets/node-split-properties-apply-condition.png){width="500"}

1. No editor de condições, adicione um ou mais filtros para definir o caminho dividido.

   * Arraste e solte atributos de filtro da navegação à esquerda e conclua a definição de correspondência.

   * Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você escolhe corresponder todas as condições de atributo ou qualquer condição.

     ![Nó de caminho dividido - lógica de filtro de contas de condições](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e repita as etapas anteriores para adicionar condições aplicáveis a este caminho.

   Você também pode rotular cada caminho com base nessas condições ou usar os rótulos padrão.

1. Se necessário, reordene os caminhos de acordo com a prioridade desejada para a divisão.

   A filtragem de caminho é avaliada em ordem decrescente. Cada conta continua pelo primeiro caminho correspondente.

   Clique nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista de caminhos.

   ![Nó de caminho dividido - reordenar caminhos](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Habilite a opção **[!UICONTROL Outras contas]** para adicionar um caminho padrão para contas que não correspondam aos caminhos definidos. Se não, a jornada acaba para essas pessoas.

### Adicionar um caminho dividido pelo nó de pessoas

>[!NOTE]
>
>Quando você divide caminhos por pessoas, um nó _Fechar caminhos divididos_ é inserido automaticamente para encerrar a divisão. Um caminho dividido por pessoas permite somente _Realizar uma ação_ em nós de pessoas.

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](./assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para a divisão.

1. Defina os **[!UICONTROL Atributos usados para as condições]**.

   * Escolha **[!UICONTROL Somente atributos de pessoas]** para usar condições relacionadas ao perfil de pessoa e aos eventos.
   * Escolha **[!UICONTROL Somente atributos Conta-Pessoa]** para usar condições relacionadas à associação de função da pessoa em uma conta.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

1. No editor de condições, adicione um ou mais filtros para definir o caminho dividido.

   * Arraste e solte qualquer um dos atributos de pessoas da navegação à esquerda e conclua a definição de correspondência.

     >[!NOTE]
     >
     >Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta no Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa em condições.

   * Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você escolhe corresponder todas as condições de atributo ou qualquer condição.

     ![Nó de caminho dividido - lógica de filtro de pessoa de condições](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e repita as etapas anteriores para adicionar condições aplicáveis a este caminho.

   Você também pode rotular cada caminho com base nessas condições ou usar os rótulos padrão.

1. Se necessário, reordene os caminhos de acordo com a prioridade desejada para a divisão.

   A filtragem de caminho é avaliada em ordem decrescente. Cada pessoa continua pelo primeiro caminho que corresponde a.

   Clique nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista de caminhos.

   ![Nó de caminho dividido - reordenar caminhos](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Habilite a opção **[!UICONTROL Outras pessoas]** para adicionar um caminho padrão para pessoas que não correspondam aos caminhos definidos. Se não, a jornada acaba para essas pessoas.

>[!BEGINSHADEBOX &quot;associação à lista do Marketo Engage&quot;]

No Marketo Engage, as _Campanhas inteligentes_ verificam a associação de programas para garantir que os clientes potenciais não recebam emails duplicados e não sejam membros de vários fluxos de emails ao mesmo tempo. No Journey Optimizer B2B, você pode verificar a associação à lista do Marketo Engage como uma condição para o caminho dividido por pessoas para ajudar a eliminar a duplicação em atividades de jornada.

Para fazer isso, expanda **[!UICONTROL Filtros Especiais]** e arraste a condição **[!UICONTROL Membro da Lista]** para o espaço de filtro e conclua a definição do filtro para avaliar a associação em uma ou mais listas do Marketo Engage.

![Dividir caminho por condição de pessoas para associação à lista de Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Quando você tem condições definidas para cada caminho para dividir o público no nível das pessoas, é possível adicionar ações que deseja realizar nas pessoas.

>[!NOTE]
>
>Ao dividir o público por pessoas, você pode adicionar somente ações de pessoas até que os caminhos sejam fechados ou mesclados.

## Caminhos de mesclagem

Adicione um nó _Merge paths_ para combinar diferentes caminhos divididos por conta em sua jornada.

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

1. Clique no nó dividido para abrir as propriedades à direita.

1. Clique em [!UICONTROL Adicionar caminho] para criar três caminhos.

1. Adicione uma combinação de ações e eventos a cada caminho.

1. Clique no ícone de adição ( **+** ) de qualquer um desses caminhos e escolha **[!UICONTROL Mesclar]** nas opções exibidas.

   ![Nó do Jornada - caminhos de mesclagem](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Nas propriedades do nó dos caminhos de mesclagem, selecione os caminhos que deseja mesclar.

   ![Nó do Jornada - caminhos de mesclagem](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Nesse ponto, os caminhos são mesclados para que as contas dos caminhos selecionados sejam combinadas em um único caminho que possa continuar avançando pela jornada.

1. Se necessário, você pode desfazer a mesclagem de caminhos navegando de volta para as propriedades do nó dos caminhos de mesclagem e desmarcando a caixa de seleção de todos os caminhos que deseja remover.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
