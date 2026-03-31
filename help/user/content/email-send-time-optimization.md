---
title: Otimização do tempo de envio de email
description: A Otimização de hora de envio (STO) no Adobe Journey Optimizer personaliza a entrega de email para jornadas de pessoas. Saiba como habilitar o STO e melhorar o engajamento.
feature: Person Journeys, Channels
role: User
source-git-commit: 55cfcd3b4ee777ee8945ea9a1cd1429625ee61c3
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Otimização do tempo de envio de email

Use o recurso de Otimização de hora de envio (STO) para personalizar o tempo de entrega de email para [jornadas de pessoas](../journeys/journeys-overview.md), prevendo quando cada perfil tem maior probabilidade de participar. Em vez de um tempo de envio fixo, o STO usa sinais históricos de engajamento de email para agendar a entrega no horário ideal para cada recipient, melhorando o engajamento geral.

O STO analisa o engajamento histórico de cada perfil usando um grande modelo de linguagem. Ele prevê e classifica os possíveis tempos de envio e, em seguida, agenda o delivery no momento com a classificação mais alta na janela de otimização.

## Disponibilidade e escopo atuais

No momento, a otimização de tempo de envio é compatível com:

* **Tipo de Jornada**: Jornadas de pessoas
* **Canal**: Email
* **Configuração**: nó da ação _Enviar email_
* **Relatórios**: assistente de IA por meio da habilidade de observação da Jornada

  Os insights de desempenho, como uso, aumento de engajamento e comparações STO versus não STO, estão disponíveis por meio de consultas de linguagem natural no Assistente de IA.

>[!BEGINSHADEBOX]

Há muitos **_aprimoramentos futuros_** planejados para o STO:

* Suporte para _Jornadas de conta_
* Configuração STO global na área _[!UICONTROL Admin]_
* Ativação de STO no nível da jornada
* Divisões de teste/controle configuráveis
* Um painel de relatórios STO dedicado

>[!ENDSHADEBOX]

## Configuração

Você pode configurar a otimização de hora de envio ao [adicionar um nó _[!UICONTROL Executar uma ação]_](../journeys/action-nodes.md) a uma jornada de pessoa.

1. Para _[!UICONTROL Selecionar ação]_, escolha **[!UICONTROL Enviar email]**.

1. Use a opção **[!UICONTROL Otimização de Tempo de Envio]** para habilitar o recurso.

1. Defina as opções de STO para especificar a janela e a distribuição de teste:

   * **[!UICONTROL Enviar no próximo]** - Esse valor determina a janela de otimização (em dias), que é o intervalo de tempo no qual os emails podem ser entregues. Por exemplo, para um webinário que ocorre em cinco dias, você pode definir uma janela de quatro ou cinco dias. O STO seleciona o melhor tempo de envio previsto para cada perfil nessa janela.

   * **STO / Distribuição fixa** - STO cria automaticamente uma _divisão de teste e controle_ para dividir perfis qualificados entre tempos de envio otimizados e fixos. A divisão permite a comparação direta de desempenho. (Aprimoramentos futuros estão planejados para permitir porcentagens divididas personalizadas.)

   >[!NOTE]
   >
   >Perfis com um histórico de engajamento forte são divididos uniformemente em grupos de controle e teste para medir o impacto do STO. Para garantir resultados estatisticamente confiáveis, a divisão STO versus não STO é restrita entre 30% e 70%. Isso ajuda a evitar que coortes menores distorçam os resultados e garante comparações significativas.

   ![Nó de jornada de envio de email - Opções de Otimização de Tempo de Envio](./assets/email-node-send-time-optimization.png){width="700" zoomable="no"}

1. Diretamente após o nó _[!UICONTROL Enviar email]_, [adicionar um nó _Aguardar_](../journeys/wait-nodes.md).

   Um nó de espera deve seguir imediatamente uma ação de email habilitada para STO. A adição desse nó garante que os perfis permaneçam na jornada até que a janela de otimização completa seja limpa e todos os envios de STO sejam concluídos. Se você omitir esse nó, o sistema sinalizará a configuração como inválida.

1. Após concluir o restante da jornada de pessoas, prossiga para [publicar](../journeys/create-publish-journey.md#publish-a-journey).

## Insights de STO

Os insights de STO são entregues por meio do _Assistente de IA_ usando a [_habilidade de observação_](../agents/journey-agent.md#journey-observability-skill) da Journey Agent. Você pode consultar uso, métricas de engajamento, resultados de teste/controle, desempenho do nó e impacto geral na jornada.
