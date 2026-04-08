---
title: Nós externos
description: Saiba como usar os nós Ação externa e Caminho de divisão externo nas jornadas de conta para se conectar a serviços externos e rotear contas e pessoas com base na resposta do serviço.
feature: Account Journeys, Integrations
role: User
source-git-commit: c88ea3ce8c17e78b3e48cb3c2f9951358e822618
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Nós externos

Use nós externos para conectar sua jornada de conta a um serviço externo. Quando um público-alvo de conta atinge um desses nós, o Journey Optimizer B2B edition envia de forma assíncrona os dados de atributo do público-alvo para o serviço externo. O serviço processa os dados e responde usando um retorno de chamada, retornando as informações e os metadados do público-alvo que a jornada usa para continuar.

>[!NOTE]
>
>Os nós de ação externa estão disponíveis somente em jornadas de conta. Elas não são compatíveis com jornadas pessoais.
>
>Um administrador deve [configurar e ativar a ação externa](../admin/configure-external-actions.md) antes que os profissionais de marketing adicionem e implementem esses nós em uma jornada.

Há dois tipos de nó de ação externa:

* **[Ação externa](#external-action)** - Chama um serviço externo e continua ao longo de um único caminho de saída. Use esse nó quando quiser acionar um processo externo sem lógica de ramificação, como atualizar um registro em um sistema externo ou enviar um sinal a um serviço downstream.
* **[Caminhos divididos externos](#external-split-paths)** - Chama um serviço externo e avalia a resposta para rotear contas ao longo de um dos vários caminhos definidos. Use este nó quando o serviço externo retornar um valor, como uma pontuação, camada ou classificação, que determina a próxima etapa da jornada.

## Nó de ação externa {#external-action}

O nó _Ação externa_ chama um serviço externo e continua ao longo de um único caminho de saída, independentemente do conteúdo da resposta. Use-a para integrações em que nenhuma ramificação é necessária após a chamada externa.

1. Navegue até o mapa de jornada de conta.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ação externa]**.

   ![Adicionar um nó de ação externa](./assets/node-external-action.png){width="400"}

1. Nas propriedades do nó à direita, defina o contexto **[!UICONTROL Ação em]** para a ação externa:

   * Escolha **[!UICONTROL Contas]** quando quiser aplicar a ação externa a todas as pessoas que fazem parte das contas no caminho de nó.
   * Escolha **[!UICONTROL Pessoas]** quando quiser aplicar uma alteração a todas as pessoas no caminho de nó.

1. Selecione o **[!UICONTROL Nome do serviço]** externo.

   ![Nó de ação externa - selecione o serviço externo](./assets/node-external-action-service-name.png){width="600" zoomable="yes"}

   A lista inclui todas as ações externas configuradas que estão ativas e designadas para o tipo de _Ação externa_ e o contexto.

1. Se o serviço tiver atributos globais, insira os valores necessários nos campos exibidos abaixo do nome do serviço.

1. Continue criando a jornada a partir dos caminhos de saída do nó.

   O caminho _[!UICONTROL Timeout ou error]_ é criado automaticamente. Se o período de timeout (conforme configurado no serviço) decorrer antes que uma resposta seja recebida, a conta ou pessoa avançará por esse caminho. É o mesmo se uma resposta de erro for recebida. Você pode adicionar nós de jornada a esse caminho para lidar com esses cenários, ou a jornada termina para o membro do público-alvo.

## Nó de caminhos divididos externos {#external-split-paths}

O nó Caminhos divididos externos chama um serviço externo e usa a resposta para determinar qual caminho as contas seguirão. Cada caminho é definido por uma condição baseada em uma variável (acessadora) retornada pelo serviço externo. A jornada avalia a resposta em relação às condições de caminho definidas e encaminha cada conta ao longo do primeiro caminho correspondente. As condições do caminho são avaliadas em ordem decrescente. Cada conta continua ao longo do primeiro caminho cuja condição corresponde ao valor retornado pelo serviço externo.

1. Navegue até o mapa de jornada de conta.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Caminhos divididos externos]**.

   ![Adicionar um nó de caminho dividido externo](./assets/node-external-split-path.png){width="400"}

1. Nas propriedades do nó à direita, escolha um tipo **[!UICONTROL Split paths by]**:

   * **[!UICONTROL Contas]** - Para caminhos de divisão por contas, você pode adicionar nós de conta e pessoas nos caminhos definidos.
   * **[!UICONTROL Pessoas]** - Para caminhos divididos por pessoas, você pode adicionar somente nós de ação de pessoas nos caminhos definidos. Uma divisão com base em pessoas é fechada automaticamente com um nó _[!UICONTROL Mesclar caminhos]_ para que todas as pessoas possam avançar para a próxima etapa sem perder o contexto da conta.

1. Selecione o **[!UICONTROL Nome do serviço]**.

1. Se a configuração do serviço tiver _atributos globais_, insira os valores necessários nos campos que aparecem abaixo do nome do serviço.

1. Para _[!UICONTROL Caminho 1]_, defina a condição de ramificação:

   * Para **[!UICONTROL Rótulo]**, substitua o valor padrão por um rótulo mais descritivo.
   * Para **[!UICONTROL Selecionar variável]**, escolha um acessador. Os acessadores são valores retornados pelo serviço externo e são definidos quando a ação é configurada.
   * Para **[!UICONTROL Selecionar operador]**, escolha o operador.
   * Para **[!UICONTROL Inserir valores]**, insira o valor para corresponder.

   ![Nó de caminho dividido externo - defina a condição de caminho usando uma variável de serviço](./assets/node-external-split-path-properties.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >As variáveis de condição disponíveis e o contexto de jornada com suporte (_Conta_, _Pessoas_ ou _Pessoas na Conta_) são determinados pela configuração de ação externa. Entre em contato com o administrador se o serviço ou as variáveis esperadas não estiverem disponíveis.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e defina uma condição para cada um que você precisar.

1. Continue criando a jornada a partir de cada caminho de saída do nó.

   O caminho _[!UICONTROL Timeout ou error]_ é criado automaticamente. Se o período de timeout (conforme configurado no serviço) decorrer antes que uma resposta seja recebida, a conta ou pessoa avançará por esse caminho. É o mesmo se uma resposta de erro for recebida. Você pode adicionar nós de jornada a esse caminho para lidar com esses cenários, ou a jornada termina para o membro do público-alvo.

1. Para _Dividir por contas_, você pode adicionar um [nó de caminhos de mesclagem](./split-merge-paths-nodes.md#merge-paths) para combinar dois ou mais caminhos, conforme necessário.
