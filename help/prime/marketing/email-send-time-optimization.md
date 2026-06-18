---
title: Otimização do tempo de envio de email
description: A Otimização de tempo de envio (STO) no Adobe Journey Optimizer B2B Prime personaliza a entrega de email para jornadas de pessoas. Saiba como habilitar o STO e melhorar o engajamento.
autotag-review: '2026-06-17T20:52:02.535Z'
TQID: 'https://experienceleague.adobe.com/wlxhS7E8DnbThm5ge-wzTkMcn-eBzFUXfw3ZGrfcRHA'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
source-git-commit: 951d9ceaa95656952e36b6d8f238348b08c796ca
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Otimização do tempo de envio de email

Use o recurso de Otimização de hora de envio (STO) para personalizar o tempo de entrega de email para [jornadas de pessoas](./person-journeys.md), prevendo quando cada perfil tem maior probabilidade de participar. Em vez de um tempo de envio fixo, o STO usa sinais históricos de engajamento de email para agendar a entrega no horário ideal para cada recipient, melhorando o engajamento geral.

O STO analisa o engajamento histórico de cada perfil usando um grande modelo de linguagem. Ele prevê e classifica os possíveis tempos de envio e, em seguida, agenda o delivery no momento com a classificação mais alta na janela de otimização.

<!-- Performance insights, such as usage, engagement lift, and STO vs. non-STO comparisons, are available through natural language queries in the AI Assistant. -->

>[!BEGINSHADEBOX]

Há muitos **_aprimoramentos futuros_** planejados para o STO:

* Configuração STO global na área _[!UICONTROL Admin]_
* Ativação de STO no nível da jornada
* Divisões de teste/controle configuráveis

>[!ENDSHADEBOX]

## Configuração {#configuration}

Você pode configurar a otimização de hora de envio ao [adicionar um nó _[!UICONTROL Executar uma ação]_](./action-nodes.md) a uma jornada de pessoa e escolher a ação **[!UICONTROL Enviar email]**.

1. Selecione o nó da ação de jornada _Enviar email_.

1. Nas propriedades do nó à direita, habilite a opção **[!UICONTROL Otimização de Tempo de Envio]**.

   ![Nó de jornada de envio de email - Opções de Otimização de Tempo de Envio](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Para especificar a janela e a distribuição de teste, defina as opções STO:

   * **[!UICONTROL Enviar no próximo]** - Esse valor determina a janela de otimização (em dias), que é o intervalo de tempo no qual os emails podem ser entregues. Por exemplo, para um webinário que ocorre em cinco dias, você pode definir uma janela de quatro ou cinco dias. O STO seleciona o melhor tempo de envio previsto para cada perfil nessa janela.

   * **STO / Distribuição fixa** - STO cria automaticamente uma _divisão de teste e controle_ para dividir perfis qualificados entre tempos de envio otimizados e fixos. A divisão permite a comparação direta de desempenho. (Aprimoramentos futuros estão planejados para permitir porcentagens divididas personalizadas.)

   >[!NOTE]
   >
   >Perfis com um histórico de engajamento forte são divididos uniformemente em grupos de controle e teste para medir o impacto do STO. Para garantir resultados estatisticamente confiáveis, a divisão STO versus não STO é restrita entre 30% e 70%. Isso ajuda a evitar que coortes menores distorçam os resultados e garante comparações significativas.

1. Diretamente após o nó _[!UICONTROL Enviar email]_, [adicionar um nó _Aguardar_](./wait-nodes.md).

   Um nó de espera deve seguir imediatamente uma ação de email habilitada para STO. A adição desse nó garante que os perfis permaneçam na jornada até que a janela de otimização completa seja limpa e todos os envios de STO sejam concluídos. Se você omitir esse nó, o sistema sinalizará a configuração como inválida.

1. Após concluir o restante da jornada de pessoas, prossiga para [publicar](./person-journeys.md#publish).

## Relatório


