---
title: Fazer um nó de ação
description: Espaço reservado
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: af7eab5e-3580-4254-9f56-3c20b4f6ef42
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# Executar um nó de ação

Em uma jornada de pessoa, use uma ação em pessoas quando quiser aplicar uma alteração a todas as pessoas no caminho do nó. Para uma jornada de conta, esse tipo de nó pode ser usado no caminho dividido por pessoas ou no caminho dividido por contas.

## Ações e restrições

| Ação | Contrastes |
| ------ | ---------- |
| **[!UICONTROL Enviar email]** | <li>Criar email <li>Otimização do tempo de envio (opcional) |
| **[!UICONTROL Alterar valor de dados]** | <li>Selecionar atributo de pessoa <li>Definir novo valor |

## Adicionar um nó de ação {#add-an-action-node}

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

1. Nas propriedades do nó à direita, selecione uma ação na lista e defina os valores para a ação.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Enviar email]

Use esta ação para enviar um email. Depois de criar o email para o nó, você pode criar, personalizar e visualizar mensagens de email no espaço de design de email (consulte [Criação de email](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Você pode usar a [Otimização de hora de envio](../marketing/email-send-time-optimization.md) para personalizar o tempo de entrega de email prevendo quando cada perfil tem maior probabilidade de participar.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Alterar valor de dados]

Use esta ação para alterar o valor de um atributo de perfil de pessoas no banco de dados. Selecione o atributo e defina o novo valor.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++
