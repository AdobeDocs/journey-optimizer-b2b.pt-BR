---
title: Públicos-alvo baseados em eventos
description: Use públicos-alvo baseados em eventos no Journey Optimizer B2B Prime para acionar a entrada de jornada de pessoas em tempo quase real com base em atividades do Marketo Engage.
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
autotag-review: '2026-06-25T17:59:01.953Z'
TQID: 'https://experienceleague.adobe.com/04J58rjKw0hCoTOeYheZIPaX-YR8GwP-k6-Wn3XCetU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 4c3919d0f2d0c5c12236f3ced1b0e9674ef9567e
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 3%

---

# Públicos-alvo baseados em eventos

Em [!DNL Adobe Journey Optimizer B2B Prime], os _públicos-alvo baseados em eventos_ permitem que você adicione membros do público-alvo a uma [jornada de pessoa](../marketing/person-journeys.md) em tempo quase real, quando ocorrer uma atividade [!DNL Marketo Engage]. Você configura públicos-alvo baseados em eventos no nó Público-alvo da tela de jornada:

* Selecione uma ou mais [!DNL Marketo Engage] atividades (padrão ou personalizadas) como os eventos qualificados.
* Opcionalmente, adicione filtros de perfil de pessoa (como setor, região ou estágio do ciclo de vida) para restringir quais pessoas podem informar.
* Opcionalmente, defina restrições de atributo de atividade (como um formulário, URL ou programa específico) para restringir quais ocorrências de cada atividade se qualificam.

Quando uma atividade qualificada é conectada em [!DNL Marketo Engage] para um cliente potencial e replicada em [!DNL Adobe Journey Optimizer B2B Prime], o sistema avalia o registro de pessoa correspondente em relação aos filtros e restrições configurados. Se as condições forem atendidas, a pessoa entrará na jornada imediatamente por meio do nó Público-alvo.

_Para definir uma audiência baseada em eventos para uma jornada de pessoa :_

1. Selecione o nó [_Audiência da pessoa_](../marketing/person-audience-node.md).

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Público-alvo do evento]** como o tipo de entrada.

   ![Nó de jornada de público-alvo de pessoa definido como público-alvo baseado em eventos](./assets/event-based-audience-node.png){width="400"}

1. Clique em **[!UICONTROL Adicionar critérios de evento]**.

1. Na caixa de diálogo _[!UICONTROL Editar critérios de evento]_, adicione uma ou mais atividades [!DNL Marketo Engage] como eventos qualificados, como:

   * _Participa do webinário_
   * _Email entregue_
   * _Link de cliques no email_

   >[!NOTE]
   >
   >Você também pode selecionar atividades personalizadas definidas na instância [!DNL Marketo Engage] associada.

   Defina o operador e os valores correspondentes para cada atividade.

   ![Acionadores de atividade para uma audiência baseada em eventos](./assets/event-based-audience-triggers.png){width="700" zoomable="yes"}

   Uma pessoa se qualifica para a jornada quando qualquer uma dessas atividades configuradas é registrada para esse lead.

1. (Opcional) Para usar um evento e uma combinação de filtros para qualificação de público-alvo, adicione filtros de nível de pessoa.

   * Selecione a guia **[!UICONTROL Filtros]**.
   * Arraste cada filtro e defina os critérios correspondentes.

   ![Filtros de pessoa para um público-alvo baseado em eventos](./assets/event-based-audience-filters.png){width="700" zoomable="yes"}

   Se você adicionar filtros, a pessoa deverá atender a pelo menos uma condição de atividade configurada e aos filtros configurados.

1. Clique em **[!UICONTROL Salvar]**.
