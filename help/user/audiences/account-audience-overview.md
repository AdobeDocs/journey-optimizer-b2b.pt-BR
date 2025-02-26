---
title: Públicos da conta
description: Saiba mais sobre públicos-alvo de contas e como eles habilitam jornadas baseadas em contas.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: b6b26d9cb79926577ed7fc4ed50c094986796505
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Públicos-alvo da conta

Um público-alvo é um conjunto de pessoas que compartilham comportamentos e/ou características semelhantes. O Journey Optimizer B2B edition usa as funcionalidades de segmentação de conta encontradas nas edições B2B e B2P do Adobe Real-Time Customer Data Platform. Com a segmentação de conta, os usuários podem gerar públicos-alvo da conta aproveitando dados de qualquer uma das entidades B2B no sistema. Esses públicos-alvo de conta servem como entradas para jornadas de conta do Journey Optimizer B2B edition, facilitando a ativação contínua e o recurso de personalização.

Saiba mais sobre públicos-alvo da conta e como defini-los na [documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/types/account-audiences).

## Fluxo de trabalho de público da conta

Pense no Journey Optimizer B2B edition como um destino do Experience Platform (AEP) que não aparece no catálogo de destinos. Ative públicos-alvo da conta para o Journey Optimizer B2B edition usando as seguintes etapas:

1. Crie esquemas para seus dados no AEP.
1. Assimile seus dados na AEP.
1. Crie um segmento de conta para avaliar seus dados.
1. Ative os dados avaliados no Journey Optimizer B2B edition.

No Journey Optimizer B2B edition, os públicos-alvo das contas são usados como uma entrada para jornadas baseadas em contas, permitindo direcionar as pessoas nessas contas. Por exemplo, você pode usar os públicos-alvo da conta para recuperar registros de todas as contas que não têm informações de contato de nenhuma pessoa com o título Diretor de Operações (COO) ou Diretor de Marketing (CMO).

O Journey Optimizer B2B edition permite criar públicos-alvo de conta do Adobe Experience Platform (AEP) diretamente da navegação à esquerda e incorporá-los às jornadas da conta.

![Acessar públicos-alvo da conta](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Criar um público-alvo da conta

Defina o público da conta criando uma segmentação de conta. Você tem a opção de criar a segmentação de conta diretamente no aplicativo Journey Optimizer B2B edition, ou pode usar a [Interface do usuário do Construtor de segmentos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder). Veja a seguir as etapas que podem ser usadas para criar uma segmentação de conta no Journey Optimizer B2B edition.

1. Na navegação à esquerda, escolha **[!UICONTROL Contas]** > **[!UICONTROL Públicos-alvo]**.

1. Clique em **[!UICONTROL Criar público-alvo]** na parte superior direita.

1. Crie a definição do segmento.

   Os atributos e os públicos-alvo da conta são exibidos na barra de navegação esquerda. Na guia _[!UICONTROL Atributos]_, é possível adicionar atributos personalizados e criados pela plataforma. Arraste cada atributo para criar a lógica do segmento.

   >[!TIP]
   >
   >Ao criar um público-alvo para uma conta, esteja ciente de que os eventos estão listados em _[!UICONTROL Pessoas]_, pois esses atributos estão associados a pessoas.<br/>
   >
   >Na guia _[!UICONTROL Públicos-alvo]_, você pode adicionar públicos-alvo com base em pessoas criados anteriormente para criar novos públicos-alvo ao criar seu próprio público-alvo da conta.

   O exemplo a seguir define o público-alvo criado por meio de `Country Code`, `Revenue Amount` e `Market segment`. O query em inglês seria &quot;I want all accounts in the US who are in the Finance Segment whose revenue greater $1M&quot; (Quero todas as contas nos EUA que estão no segmento financeiro cuja receita exceda US$ 1 milhão).

   ![exemplo do construtor de segmento de público-alvo da conta](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >O atributo `Account Name` para registros de conta deve conter um valor a ser incluído nas jornadas de conta. Se este atributo estiver vazio (nulo), o registro da conta será excluído.<br/>
   >Para garantir que apenas contas com um Nome de Conta não vazio sejam incluídas, adicione o atributo **[!UICONTROL Nome de Conta]** e selecione _[!UICONTROL existe]_ como condição de correspondência.<br/>
   >![O atributo Nome da Conta existe](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Se você estiver usando um atributo personalizado como nome da conta, use seu nome de atributo personalizado no lugar de _[!UICONTROL Nome da Conta]_.

1. Clique em **[!UICONTROL Salvar e fechar]** na parte superior direita.

Para ativar o público da sua conta para o Journey Optimizer B2B edition, você deve [adicioná-lo a uma jornada de conta](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) e [publicar a jornada](../journeys/journey-overview.md).
