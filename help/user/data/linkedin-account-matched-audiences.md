---
title: Públicos-alvo correspondentes da conta do LinkedIn
description: Saiba como conectar uma conta do LinkedIn e ativar um fluxo de dados para membros da conta.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
exl-id: d2303529-16c4-4b0b-b8c8-404dff8ec63d
source-git-commit: 1cc50d33e396e490f401330688e5d322270090e3
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 13%

---

# Públicos-alvo correspondentes da conta do LinkedIn

O Journey Optimizer B2B edition oferece a capacidade de gerar públicos-alvo de anúncios do LinkedIn por meio de públicos-alvo correspondentes à conta, e foi projetado para ajudar você a preencher funções vazias em seus grupos de compra. Ao definir um conjunto de filtros de grupo de compra, você pode manter um Público-alvo correspondente do LinkedIn para direcionar os prospetos que correspondem aos parâmetros do grupo de compra. Você também pode ativar um público-alvo de uma jornada de conta de um nó _Realizar uma ação_.

Esse recurso utiliza os destinos da Experience Platform para gerenciar alguns aspectos da integração. Há um limite de dez fluxos de dados.

Antes de iniciar um fluxo de dados do Journey Optimizer B2B edition, você deve ter pelo menos uma instância do [(Empresas) Conector de destino do LinkedIn Matched Audience](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/social/linkedin#connect){target="_blank"} com uma conta do Gerenciador de campanhas do LinkedIn configurada no aplicativo do Experience Platform.

## Configurar uma nova conexão com a conta do LinkedIn {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="A configuração de destino do LinkedIn é obrigatória"
>abstract="Envie contas filtradas por grupos de compra para um destino do Linkedin para interagir com membros potenciais do grupo de compra. Você pode criar até 10 fluxos de dados para 10 grupos diferentes de contas filtradas. Para começar a usar esse recurso, adicione primeiro um destino do Linkedin."

1. No Experience Platform, vá para **[!UICONTROL Conexões]** > **[!UICONTROL Destinos]** na navegação à esquerda e selecione a guia **[!UICONTROL Catálogo]**.

1. No catálogo, localize o conector **[!UICONTROL (Empresas) LinkedIn Matched Audience]**.

   >[!TIP]
   >
   >Você pode encontrar rapidamente o conector digitando `LinkedIn` na caixa de pesquisa.

1. No cartão do conector, clique no ícone _Mais_ (**...**) e escolha **[!UICONTROL Configurar novo destino]**.

   ![Acessar o conector de Público-alvo correspondente do LinkedIn (Empresas)](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Selecione **[!UICONTROL Nova conta]** e clique em **[!UICONTROL Conectar ao destino]**.

   ![Conectar uma nova conta do LinkedIn](./assets/aep-destinations-catalog-linkedin-new-account.png){width="500"}

1. Forneça suas credenciais do LinkedIn e faça logon.

   Após a autenticação, a conta do LinkedIn é conectada como um destino no Experience Platform.

   ![Confirmação de conexão da conta exibida](./assets/aep-destinations-catalog-linkedin-connected.png){width="400"}

   >[!IMPORTANT]
   >
   >Neste ponto, **não** insira os _[!UICONTROL detalhes do Destino]_. Somente a conexão é necessária.

## Atualizar os detalhes da conta

O nome e a descrição da conta do LinkedIn estão visíveis para grupos de compras no Journey Optimizer B2B edition. É uma prática recomendada atualizar essas informações para que sejam facilmente identificáveis para seus profissionais de marketing que trabalham com grupos de compra. É possível alterar os detalhes da conta na interface do usuário do Experience Platform ou do Journey Optimizer B2B edition.

1. Vá para **[!UICONTROL Conexões]** > **[!UICONTROL Destinos]** na navegação à esquerda e selecione a guia **[!UICONTROL Contas]**.

1. Para a nova conta criada, clique no menu _Mais_ (**...**) e escolha **[!UICONTROL Editar detalhes]**.

   ![Editar detalhes da conta](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. Na caixa de diálogo do, atualize o nome e a descrição.

   ![Editar o nome e a descrição](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. Clique em **[!UICONTROL Salvar]**.

## Ativar a conta para grupos de compras

>[!NOTE]
>
>Se você já tiver dez fluxos de dados, não poderá criar outro. Se você estiver no máximo, exclua um no Experience Platform antes de criar um novo no Journey Optimizer B2B edition.

1. No Journey Optimizer B2B Edition, acesse **[!UICONTROL Contas]** > **[!UICONTROL Grupos de compra]** na navegação à esquerda.

1. Selecione a guia **[!UICONTROL Navegar]**.

1. Clique em **[!UICONTROL Ativar para destino do LinkedIn]** na parte superior direita.

   ![Editar detalhes da conta](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. Atribua um nome e uma descrição descritiva ao fluxo de dados (opcional).

   Depois de salvá-lo, o nome especificado para o fluxo de dados é anexado a _AJOB2B_ para ajudar na identificação do fluxo de dados no Experience Platform.

1. Insira a [ID da conta da sua conta do gerenciador de campanhas do LinkedIn](https://www.linkedin.com/help/lms/answer/a424270).

   Você pode encontrar sua ID de conta pelo Nome da conta na interface do usuário do Campaign Manager.

   ![Adicionar os detalhes do fluxo de dados](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar filtros de grupo de compra]** e defina os parâmetros do público-alvo da sua conta.

   >[!IMPORTANT]
   >
   >No momento, os filtros não podem ser editados depois que o fluxo de dados é ativado. Verifique novamente seu trabalho antes de ativar o fluxo de dados.

   ![Especificar a filtragem de público da conta de acordo com os grupos de compra](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   Na **[!UICONTROL Pontuação de engajamento]**, o operador `Between` é inclusivo, assim como os intervalos de porcentagem. Por exemplo, 5,1 e 5 estão ambos _entre_ 5 e 6.

   Condições vazias são tratadas como `Is Any`.

   Clique em **[!UICONTROL Salvar]** para adicionar os filtros especificados.

1. Clique em **[!UICONTROL Selecionar destino do LinkedIn]** e escolha o destino do LinkedIn configurado que você deseja usar.

   Após a ativação, essa configuração cria o fluxo de dados usando a configuração de destino e um segmento virtual correspondente.

1. Verifique suas configurações e clique em **[!UICONTROL Ativar]** na parte superior direita.

   Clique novamente em **[!UICONTROL Ativar]** na caixa de diálogo de confirmação.

   Um banner é exibido com um link para o menu de fluxos de dados no Experience Platform para que você possa verificar o registro do fluxo de dados.

## Ativar um público-alvo a partir de uma jornada de conta

A partir da versão 2025.10, use a ação _Ativar para destino_ para que as contas sejam ativadas para um destino do LinkedIn diretamente da sua jornada. Use a ação para um destino do LinkedIn para simplificar a execução da campanha, eliminando transferências de vários sistemas e reduzindo a latência. Por exemplo, como profissional de marketing, você pode ativar automaticamente contas de alto propósito para o LinkedIn para redirecionamento quando as principais funções de compra estiverem ausentes ou reengajar contas inativas com base em filtros de inatividade.

1. Com o nó _Realizar uma ação_ selecionado na tela de jornada, defina a **[!UICONTROL Ação nas contas]** como **[!UICONTROL Ativar para o destino]**.

1. Clique em **[!UICONTROL Selecionar destino]**.

   ![Nó do Jornada - executar uma ação nas contas - ativar para o destino](../journeys/assets/node-activate-destination-select-destination.png){width="600" zoomable="yes"}

1. Na caixa de diálogo, selecione o destino do LinkedIn configurado e clique em **[!UICONTROL Salvar]**.

   ![nó de Jornada - executar uma ação nas contas - ativar para destino - selecionar caixa de diálogo de destino](../journeys/assets/node-activate-destination-select-destination-dialog.png){width="700" zoomable="yes"}

1. Digite o **[!UICONTROL Nome do público-alvo]** que é usado para identificar o público-alvo ativado no destino.

   ![Nó do Jornada - executar uma ação nas contas - ativar para destino - configurações concluídas](../journeys/assets/node-activate-destination-settings.png){width="550" zoomable="yes"}

## Orquestrar o engajamento de mídia paga

Você pode se envolver com membros da conta por meio de um canal de mídia paga, como públicos-alvo de anúncios do LinkedIn, para adquirir, alimentar e qualificá-los para Vendas. Use um nó _Realizar uma ação_ em uma jornada de conta para automatizar o engajamento com membros-chave de uma conta por meio de um canal externo que seja mais adequado para membros de conta diferentes.

>[!VIDEO](https://video.tv.adobe.com/v/3448649/?learn=on)