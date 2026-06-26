---
title: Nó de Jornada de público-alvo de pessoa
description: Configure o nó de público-alvo pessoa no Journey Optimizer B2B para especificar quais perfis entram em uma jornada usando listas de pessoas dinâmicas ou públicos-alvo baseados em eventos.
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 4%

---

# Nó de público-alvo de pessoa

O nó _person audience_ especifica quais perfis de pessoa entram na jornada. Quando você [cria uma jornada de pessoa](./person-journeys.md), a jornada sempre começa com um nó de público-alvo de pessoa que define sua entrada. O nó de público-alvo pessoa pode ter um dos dois tipos de entrada de público-alvo: uma lista dinâmica de pessoas ou um acionador de evento.

Se a lista dinâmica de pessoas de que você precisa para a jornada de pessoa ainda não existir, [crie a lista de pessoas](../audiences/people-lists.md#create-a-people-list) e configure o nó de público-alvo Pessoa.

_Para configurar o público-alvo da jornada :_

1. Clique no nó **[!UICONTROL Público-alvo de pessoa]**.

   Essa ação exibe as propriedades do nó à direita.

   ![Nó de jornada de público-alvo de pessoa](./assets/person-audience-node-properties.png){width="600" zoomable="yes"}

1. Use uma das seguintes opções de configuração de público-alvo para o público-alvo de pessoa:

   * **[!UICONTROL Lista dinâmica]** - Use uma lista dinâmica de pessoas baseada em regras. As regras de lista são avaliadas no tempo de execução da jornada para qualificar membros da jornada. As pessoas que depois se desqualificam para a lista dinâmica não são removidas da jornada. Consulte _[Listas dinâmicas](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Público-alvo do evento]** - Use um público-alvo de evento para definir o público-alvo de jornada com base em eventos qualificados. Defina membros do público usando a filtragem de perfil de pessoa e acione a entrada de jornada usando critérios de evento. Consulte _[Públicos-alvo baseados em eventos](../audiences/event-based-audiences.md)_.
