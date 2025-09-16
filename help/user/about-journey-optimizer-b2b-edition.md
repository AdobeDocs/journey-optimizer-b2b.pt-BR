---
title: Visão geral do Adobe Journey Optimizer B2B Edition
description: 'Saiba mais sobre o Adobe Journey Optimizer B2B Edition: orquestre jornadas de conta com grupos de compra, insights de IA e a integração da Experience Platform para marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 100%

---

# Visão geral do Adobe Journey Optimizer B2B Edition

Com o Adobe Journey Optimizer B2B Edition, você pode orquestrar jornadas de conta e de grupo de compra usando a IA generativa integrada e automação líder do setor para maximizar a demanda para ofertas específicas com grupos de compra qualificados para marketing.

## Jornadas de conta com grupos de compra

Ao comparar o Adobe Journey Optimizer B2B Edition com o Marketo Engage e à versão padrão do Adobe Journey Optimizer, a principal distinção é que as jornadas de conta movem as contas pela jornada, não as pessoas. Uma pessoa associada a uma conta normalmente tem uma progressão não linear baseada no progresso da conta pela jornada, não em suas ações individuais. Por exemplo, quando uma conta está em uma fase inicial da jornada de compra, as informações enviadas podem ser sobre recursos ou funcionalidades gerais da solução. Mais adiante no processo de compra, o conteúdo pode se tornar mais direcionado para ofertas específicas ou outros itens orientados para o fechamento de uma venda. Após a compra da solução, as informações podem mudar novamente para fornecer guias passo a passo, práticas recomendadas e informações sobre eventos futuros ou conteúdo sobre vendas adicionais. Mesmo que uma pessoa não tenha interagido com o conteúdo da fase inicial, é ideal que ela avance para a fase atual com base não em suas próprias ações, mas nas ações das outras pessoas em sua conta ou grupo de compra.

## Arquitetura de alto nível

O Adobe Journey Optimizer B2B Edition usa _públicos-alvo de conta_ e _públicos-alvo de pessoas_ da Adobe Experience Platform para impulsionar uma jornada de conta, que é executada no Marketo Engage. A Experience Platform é sempre a fonte da verdade para esses dados, mas toda a execução e processamento da jornada da conta acontece dentro da infraestrutura de marketing B2B do Marketo Engage. A orquestração devolve os dados para a Experience Platform quase que em tempo real pelo conector de origem “Marketo Engage - Adobe Real-Time CDP B2B Edition” existente, que transmite alterações de dados do Marketo Engage para a Experience Platform.

![Arquitetura de dados de alto nível](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Verifique seus direitos de licença e a [descrição do produto](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondente sobre proteções de desempenho e limitações estáticas.

### Modelo de assinatura

Uma assinatura do Journey Optimizer B2B Edition é definida pela combinação de sandboxes da Experience Platform (AEP) com uma assinatura do Marketo Engage _Munchkin_. Não é possível combinar mais de uma sandbox da AEP com uma única assinatura do Marketo Engage. Se você não optar por combinar uma assinatura existente do Marketo Engage com o Journey Optimizer B2B Edition, você receberá uma assinatura nova e vazia do Marketo Engage para uso com o Journey Optimizer B2B Edition.

A finalidade da Experience Platform nesta configuração é fornecer uma visualização unificada dos dados nas instâncias do Marketo Engage (e de qualquer sistema de CRM anexado) para possibilitar ações nos dados unificados por meio de uma jornada de conta.

### Operações da jornada de conta

As jornadas de conta são criadas no Journey Optimizer B2B Edition e armazenadas na instância do Marketo Engage associada à assinatura. Embora seja enviada ao armazenamento de dados do Marketo Engage, ela não é visível na interface do Marketo Engage e só pode ser usada no Journey Optimizer B2B Edition.

Uma jornada de conta sempre começa com a seleção de um segmento da conta para usar como o público-alvo da jornada. A seleção do público-alvo usa o componente de seleção de público-alvo padrão da Experience Platform. Profissionais de marketing podem então implementar a jornada de conta dividindo os caminhos da jornada de acordo com seus próprios critérios, que podem incluir critérios de conta, de pessoas ou de grupo de compra. É possível tomar ações para implementar a jornada em cada ramificação, como enviar um email ou aguardar a ocorrência de um evento.

Após criar a jornada da conta, é necessário publicá-la. No momento da publicação, a jornada da conta é validada e convertida em uma série de campanhas do Marketo Engage que implementam a experiência da jornada. Os serviços de integração de dados são contatados para iniciar o fluxo de dados que, por sua vez, inicia as operações de jornada da conta. A primeira etapa é criar os segmentos para as pessoas da conta.

### Fluxo de dados

O Journey Optimizer B2B Edition usa a segmentação de conta da Real-Time CDP para definir e executar segmentos de conta e segmentos de pessoas da conta relacionados que são exigidos pelas jornadas. Conforme a jornada publicada é executada, os dados sobre as pessoas e contas podem mudar, sendo coletados a partir das pessoas que interagem com a jornada. O Journey Optimizer B2B Edition depende do conector de origem do Marketo Engage com a Real-Time CDP B2B Edition para transmitir as alterações de dados de volta para a sandbox da Experience Platform, que é a fonte da verdade.  Esses dados são entregues à AEP em tempo quase real.

Somente os tipos de dados existentes compatíveis com o conector de origem do Marketo Engage (contas, pessoas e oportunidades) fluem de volta para a Real-Time CDP. Isso significa que os dados do grupo de compra não fluem para a AEP e, em vez disso, permanecem na instância do Marketo Engage usada pela assinatura do Journey Optimizer B2B Edition.
