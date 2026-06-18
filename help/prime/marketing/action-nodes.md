---
title: Fazer um nó de ação
description: Espaço reservado
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 2%

---

# Executar um nó de ação

Em uma jornada de pessoa, use uma ação em pessoas quando quiser aplicar uma alteração a todas as pessoas no caminho do nó.

## Ações e restrições {#actions}

| Ação | Restrições |
| ------ | ----------- |
| **[!UICONTROL Ativar para destino]** | <li>Selecionar ou criar uma lista estática <li>Se a lista não tiver um destino ativado, ative-a |
| **[!UICONTROL Adicionar pessoa à Jornada]** | <li>Selecionar uma jornada agendada ou ativa <li>Os critérios de público-alvo da jornada de direcionamento não são aplicados |
| **[!UICONTROL Adicionar à lista]** | <li>Criar uma nova lista estática ou selecionar uma existente |
| **[!UICONTROL Adicionar à lista do Marketo]** | <li>Selecionar uma lista estática no Marketo Engage |
| **[!UICONTROL Alterar valor de dados]** | <li>Selecionar atributo de pessoa <li>Definir novo valor |
| **[!UICONTROL Alterar dados do programa]** | <li>Selecionar atributo de programa <li>Definir novo valor |
| **[!UICONTROL Alterar Status do Programa]** | <li>Selecionar programa<li>Selecionar novo status |
| **[!UICONTROL Remover da lista]** | <li>Selecionar lista estática <li>Ignora a pessoa se não for um membro atualmente |
| **[!UICONTROL Remover da lista do Marketo]** | <li>Selecionar uma lista estática no Marketo Engage <li>Ignora a pessoa se não for um membro atualmente |
| **[!UICONTROL Remover pessoa da Jornada]** | <li>Selecionar uma jornada em tempo real <li>Ignora a pessoa se não for atualmente um membro da jornada do público alvo |
| **[!UICONTROL Solicitar campanha do Marketo]** | <li>Selecionar uma campanha do Marketo Engage |
| **[!UICONTROL Enviar Email]** | <li>Criar, editar ou usar um email personalizado com IA <li>Otimização do tempo de envio (opcional) |
| **[!UICONTROL Enviar WhatsApp]** | <li>Selecionar uma mensagem do WhatsApp |

## Adicionar um nó de ação {#add-an-action-node}

1. Navegue até a tela de jornada.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

   ![Clique em adicionar ícone no caminho da jornada](./assets/person-journey-canvas-add-node.png){width="200"}

1. Nas propriedades do nó à direita, selecione uma ação na lista e defina os valores para a ação.

+++Ativar para o destino

Use esta ação para ativar pessoas para destinos Experience Platform diretamente da sua jornada. Selecione o destino e insira um nome de público-alvo para identificar o público-alvo ativado no destino.

![Executar uma ação - Ativar para o destino](./assets/person-action-node-activate-to-destination.png){width="450"}

+++

+++[!UICONTROL Adicionar pessoa à Jornada]

Use esta ação para adicionar pessoas a outras jornadas agendadas ou ativas. As pessoas adicionadas por meio dessa ação são imediatamente adicionadas ao público-alvo da jornada de direcionamento; o critério de público-alvo da jornada não é aplicado.

![Realizar uma ação - Adicionar pessoa à jornada](./assets/person-action-node-add-to-journey.png){width="450"}

+++

+++[!UICONTROL Adicionar à lista]

Use esta ação para adicionar pessoas a uma lista estática no Journey Optimizer B2B Prime.

![Realizar uma ação - Adicionar à lista](./assets/person-action-node-add-to-list.png){width="450"}

Escolha uma das seguintes opções:

* **[!UICONTROL Criar]** — Crie um novo ativo de lista estática e adicione pessoas a ele. A lista está imediatamente disponível para uso por outros ativos no Journey Optimizer B2B Prime.
* **[!UICONTROL Selecionar]** — Seleciona um ativo de lista estática existente no qual você deseja adicionar pessoas que chegam ao nó.

+++

+++[!UICONTROL Adicionar à lista do Marketo]

Use esta ação para adicionar pessoas a uma lista estática no Marketo Engage.

![Realizar uma ação - Adicionar à lista do Marketo](./assets/person-action-node-add-to-marketo-list.png){width="450"}

+++

+++[!UICONTROL Alterar valor de dados]

Use esta ação para atualizar o valor de um atributo em um registro de pessoa. Selecione o atributo e defina o novo valor.

>[!TIP]
>
>Para limpar o valor de um atributo, defina o valor como `NULL`.

![Realizar uma ação - Alterar valor de dados](./assets/person-action-node-change-data-value.png){width="450"}

+++

+++[!UICONTROL Alterar dados do programa]

Use esta ação para atualizar o valor de um atributo de programa. Selecione o atributo de programa e defina o novo valor.

![Realizar uma ação - Alterar dados do programa](./assets/person-action-node-change-program-data.png){width="450"}

+++

+++[!UICONTROL Alterar Status do Programa]

Use esta ação para alterar o status de uma pessoa em um programa do Marketo Engage. Selecione o programa e o novo status.

![Realizar uma ação - Alterar status do programa](./assets/person-action-node-change-status-program.png){width="450"}

+++

+++[!UICONTROL Remover da lista]

Use esta ação para remover pessoas de uma lista estática no Journey Optimizer B2B Prime. Se uma pessoa não for membro da lista no momento, a ação será ignorada para ela.

![Realizar uma ação - Remover da lista](./assets/person-action-node-remove-from-list.png){width="450"}

+++

+++[!UICONTROL Remover da lista do Marketo]

Use esta ação para remover pessoas de uma lista estática no Marketo Engage. Se uma pessoa não for membro da lista no momento, a ação será ignorada para ela.

![Realizar uma ação - Remover da lista do Marketo](./assets/person-action-node-remove-from-marketo-list.png){width="450"}

+++

+++[!UICONTROL Remover pessoa da Jornada]

Use esta ação para remover pessoas de outras jornadas de pessoas ativas. A pessoa é imediatamente removida da jornada de destino e nenhuma ação adicional é tomada sobre ela. Se uma pessoa não for membro da jornada de destino no momento, a ação será ignorada para ela.

![Realizar uma ação - Remover pessoa da jornada](./assets/person-action-node-remove-from-journey.png){width="450"}

+++

+++[!UICONTROL Solicitar campanha do Marketo]

Use esta ação para adicionar pessoas a uma campanha de solicitação em uma instância conectada do Marketo Engage. Selecione a campanha do Marketo Engage que será solicitada.

![Realizar uma ação - Solicitar campanha do Marketo](./assets/person-action-node-request-marketo-campaign.png){width="450"}

+++

+++[!UICONTROL Enviar Email]

Use esta ação para enviar um email para as pessoas que aceitaram. As pessoas que cancelaram a inscrição, estão na lista de bloqueios, têm emails suspensos ou têm marketing suspenso ignoram essa ação.

![Executar uma ação - Enviar email](./assets/person-action-node-send-email.png){width="450"}

Você pode criar um email, editar um email existente ou usar um email personalizado por IA. Para obter informações sobre como criar e editar emails, consulte [Canal de email](../marketing/email-channel.md).

Você pode usar a [Otimização de hora de envio](../marketing/email-send-time-optimization.md) para personalizar o tempo de entrega de email prevendo quando cada perfil tem maior probabilidade de participar.

+++

+++[!UICONTROL Enviar WhatsApp]

Use esta ação para enviar uma mensagem de WhatsApp. Você pode criar, personalizar e visualizar mensagens do WhatsApp no espaço de design visual (consulte [Criação do WhatsApp](../content/whatsapp-authoring.md)).

![Executar uma ação - Enviar WhatsApp](./assets/person-action-node-send-whatsapp.png){width="450"}

+++
