---
title: Visão geral do Adobe Journey Optimizer B2B edition
description: Descubra os principais recursos, casos de uso e arquiteturas do Adobe Journey Optimizer edição B2B.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d1696eb54c9ff25963b51a0e3934a02e103923e4
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Visão geral do Adobe Journey Optimizer B2B edition

Com o Adobe Journey Optimizer edição B2B, você pode orquestrar jornadas de conta e de grupo de compra usando a IA gerativa integrada e a automação líder do setor para maximizar a demanda para ofertas específicas usando grupos de compra qualificados para marketing.

## Jornadas de conta com grupos de compra

Ao comparar o Adobe Journey Optimizer B2B edition com o Marketo Engage e o Adobe Journey Optimizer Standard, a principal distinção é que as jornadas de conta movem as contas pela Jornada, não as pessoas. Uma pessoa associada a uma conta normalmente tem uma progressão não linear baseada no progresso da conta por meio da jornada, não com base em suas ações individuais. Por exemplo, quando uma conta está em uma fase inicial da jornada de compra, as informações enviadas podem ser sobre recursos ou características gerais da solução. Além disso, durante o processo de compra, o conteúdo pode se tornar mais direcionado para ofertas específicas ou outros itens direcionados para o fechamento de uma venda. Após a compra da solução, as informações podem mudar novamente para fornecer guias passo a passo, práticas recomendadas ou informações sobre eventos futuros, ou conteúdo sobre vendas adicionais. Mesmo que um indivíduo não tenha interagido com o conteúdo da fase inicial, você ainda deseja avançá-lo para a fase atual com base não em suas próprias ações, mas nas ações das outras pessoas em sua conta ou grupo de compras.

## Arquitetura de alto nível

O Adobe Journey Optimizer B2B edition usa _Públicos-alvo da conta_ e _Públicos-alvo de pessoas_ da Adobe Experience Platform para potencializar uma jornada de conta, que é executada dentro do Marketo Engage. O Experience Platform é sempre a fonte da verdade para esses dados, mas toda a execução e processamento da jornada da conta acontece dentro da infraestrutura de marketing Marketo Engage B2B. A orquestração traz dados de volta ao Experience Platform em tempo quase real pelo conector de origem Marketo Engage - Adobe Real-Time CDP B2B edition existente, que transmite as alterações de dados do Marketo Engage para o Experience Platform.

![Arquitetura de dados de alto nível](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Verifique seus direitos de licença e a [descrição do produto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondente sobre medidas de proteção de desempenho e limitações estáticas.

### Modelo de assinatura

Uma assinatura do Journey Optimizer B2B edition é definida por um par de sandboxes Experience Platform (AEP) com uma assinatura Marketo Engage _Munchkin_. Não é possível que uma única assinatura de Marketo Engage seja emparelhada a mais de uma sandbox da AEP. Se você não optar por emparelhar uma assinatura de Marketo Engage existente com o Journey Optimizer B2B edition, você receberá uma nova assinatura de Marketo Engage vazia para uso com o Journey Optimizer B2B edition.

O objetivo do Experience Platform nessa configuração é fornecer uma visualização unificada dos dados das instâncias Marketo Engage (e de quaisquer sistemas CRM conectados) e, em seguida, poder agir nos dados unificados usando uma jornada de conta.

### Operações de jornada de conta

As jornadas de conta são criadas no Journey Optimizer B2B edition e armazenadas na instância de Marketo Engage associada à assinatura. Embora seja armazenado no armazenamento de dados do Marketo Engage, não é visível na interface do usuário do Marketo Engage e só pode ser usado no Journey Optimizer B2B edition.

Uma jornada de conta sempre começa com a seleção de um segmento de conta para usar como público-alvo da jornada. A seleção do público-alvo usa o componente seletor de público-alvo de Experience Platform padrão. Os profissionais de marketing podem implementar a jornada de conta dividindo os caminhos da jornada de acordo com seus próprios critérios, que podem incluir critérios de conta, critérios de pessoas ou critérios de grupo de compras. Em cada ramificação, ações podem ser tomadas para implementar a jornada, como enviar um email ou aguardar a ocorrência de um evento.

Depois que a jornada da conta é criada, ela deve ser publicada. No momento da publicação, a jornada da conta é validada e convertida em uma série de campanhas de Marketo Engage que implementam a experiência de jornada. Os Data Integration Services são contatados para iniciar o fluxo de dados que, por sua vez, inicia as operações de jornada de conta. A primeira etapa é criar os segmentos para as Pessoas da conta.

### Fluxo de dados

O Journey Optimizer B2B edition usa a segmentação de conta do Real-Time CDP para definir e executar segmentos de conta e segmentos de conta de pessoa relacionados exigidos pelo jornada. Conforme uma jornada publicada é executada, dados sobre as pessoas e contas podem mudar, e os dados são coletados nas pessoas que interagem com a jornada. O Journey Optimizer B2B edition depende do conector de origem do Marketo Engage para que o Real-Time CDP B2B edition faça o fluxo das alterações de dados de volta para a sandbox do Experience Platform, que é a fonte da verdade.  Esses dados são entregues à AEP em tempo quase real.

Somente os tipos de dados existentes compatíveis com o conector de origem do Marketo Engage (contas, pessoas e oportunidades) fluem de volta para o Real-Time CDP. Isso significa que a compra de dados do grupo não flui para o AEP e, em vez disso, reside na instância do Marketo Engage usada pela assinatura do Journey Optimizer B2B edition.
