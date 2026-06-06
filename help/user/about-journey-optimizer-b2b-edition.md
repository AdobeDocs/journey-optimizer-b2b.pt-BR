---
title: Visão geral do Adobe Journey Optimizer B2B Edition
description: 'Saiba mais sobre o Adobe Journey Optimizer B2B Edition: orquestre jornadas de conta com grupos de compra, insights de IA e a integração da Experience Platform para marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 66%

---

# Visão geral do Adobe Journey Optimizer B2B Edition

Com o Adobe Journey Optimizer B2B Edition, você pode orquestrar jornadas de conta e de grupo de compra usando a IA generativa integrada e automação líder do setor para maximizar a demanda para ofertas específicas com grupos de compra qualificados para marketing.

## Jornadas de conta com grupos de compra

Ao comparar as jornadas de conta com os recursos de jornada no Marketo Engage e no Adobe Journey Optimizer Standard, a principal distinção é que as jornadas de conta movem as contas pela jornada, não as pessoas. Uma pessoa associada a uma conta normalmente tem uma progressão não linear baseada no progresso da conta pela jornada, não em suas ações individuais. Por exemplo, quando uma conta está em uma fase inicial da jornada de compra, as informações enviadas normalmente são sobre recursos ou características gerais da solução. Além disso, ao longo do processo de compra, o conteúdo se torna mais direcionado para ofertas específicas ou outros itens voltados para o fechamento de uma venda. Depois que a solução é adquirida, as informações são alteradas novamente para fornecer guias passo a passo, práticas recomendadas, informações sobre eventos futuros ou conteúdo sobre vendas adicionais. Mesmo que um indivíduo não tenha interagido com o conteúdo da fase inicial, é possível avançá-lo para a fase atual com base nas ações de outros em sua conta ou grupo de compras.

## Arquitetura de alto nível

O Adobe Journey Optimizer B2B Edition usa _públicos-alvos da conta_ e _públicos-alvos de pessoas_ da Adobe Experience Platform para impulsionar uma jornada de conta, que é executada no Marketo Engage. O Experience Platform é sempre a principal fonte desses dados, mas toda a execução e processamento da jornada da conta ocorre na infraestrutura de marketing B2B do Marketo Engage. A orquestração devolve os dados para a Experience Platform quase que em tempo real pelo conector de origem “Marketo Engage - Adobe Real-Time CDP B2B Edition” existente, que transmite alterações de dados do Marketo Engage para a Experience Platform.

![Arquitetura de dados de alto nível](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Verifique seus direitos de licença e a [descrição do produto](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondente sobre proteções de desempenho e limitações estáticas.

### Modelo de assinatura

Um par de sandboxes do Experience Platform (AEP) com uma assinatura do Marketo Engage _Munchkin_ define uma assinatura do Journey Optimizer B2B edition. Não é possível combinar mais de uma sandbox da AEP com uma única assinatura do Marketo Engage. Se você não optar por combinar uma assinatura existente do Marketo Engage com o Journey Optimizer B2B Edition, você receberá uma assinatura nova e vazia do Marketo Engage para uso com o Journey Optimizer B2B Edition.

O Experience Platform fornece uma visualização unificada de dados de instâncias do Marketo Engage e sistemas de CRM conectados para agir sobre esses dados usando uma jornada de conta.

### Operações da jornada de conta

As jornadas de conta são criadas no Journey Optimizer B2B Edition e armazenadas na instância do Marketo Engage associada à assinatura. Embora sejam armazenados no armazenamento de dados do Marketo Engage, eles não estão visíveis na interface do usuário do Marketo Engage e só podem ser usados no Journey Optimizer B2B edition.

Uma jornada de conta sempre começa com a seleção de um segmento da conta para usar como o público-alvo da conta da jornada. A seleção do público-alvo usa o componente de seleção de público-alvo padrão da Experience Platform. Profissionais de marketing podem então implementar a jornada de conta dividindo os caminhos da jornada de acordo com seus próprios critérios, que podem incluir critérios de conta, de pessoas ou de grupo de compra. É possível tomar ações para implementar a jornada em cada ramificação, como enviar um email ou aguardar a ocorrência de um evento.

Após criar a jornada da conta, é necessário publicá-la. No momento da publicação, a jornada da conta é validada e convertida em uma série de campanhas do Marketo Engage que implementam a experiência da jornada. Os Data Integration Services são contatados para iniciar o fluxo de dados que, por sua vez, inicia as operações de jornada de conta. A primeira etapa é criar os segmentos para as pessoas da conta.

### Fluxo de dados

O Journey Optimizer B2B Edition usa a segmentação de conta da Real-Time CDP para definir e executar segmentos de conta e segmentos de pessoas da conta relacionados que são exigidos pelas jornadas. Conforme a jornada publicada é executada, os dados sobre as pessoas e contas podem mudar, sendo coletados a partir das pessoas que interagem com a jornada. O Journey Optimizer B2B edition depende do conector de origem do Marketo Engage para que o Real-Time CDP B2B edition faça o fluxo das alterações de dados de volta para a sandbox da Experience Platform, que é a fonte de dados principal.  Esses dados são entregues à AEP em tempo quase real.

Somente os tipos de dados existentes compatíveis com o conector de origem do Marketo Engage (contas, pessoas e oportunidades) fluem de volta para a Real-Time CDP. Isso significa que os dados do grupo de compra não fluem para a AEP e, em vez disso, permanecem na instância do Marketo Engage usada pela assinatura do Journey Optimizer B2B Edition.
