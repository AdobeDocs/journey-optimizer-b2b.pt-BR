---
title: Visão geral do Adobe Journey Optimizer B2B Edition
description: 'Saiba mais sobre o Adobe Journey Optimizer B2B Edition: orquestre jornadas de conta com grupos de compra, insights de IA e a integração da Experience Platform para marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Visão geral do Adobe Journey Optimizer B2B Edition

Com o Adobe Journey Optimizer B2B edition, você pode orquestrar jornadas de pessoas e contas usando IA gerativa integrada e automação líder do setor para maximizar a demanda por ofertas específicas usando grupos de compras qualificados de marketing.

## Jornadas de conta com grupos de compra

Ao comparar as jornadas de conta com os recursos de jornada no Marketo Engage e no Adobe Journey Optimizer Standard, a principal distinção é que as jornadas de conta movem as contas pela jornada, não as pessoas. Uma pessoa associada a uma conta normalmente tem uma progressão não linear baseada no progresso da conta pela jornada, não em suas ações individuais. Por exemplo, quando uma conta está em uma fase inicial da jornada de compra, as informações enviadas normalmente são sobre recursos ou características gerais da solução. Além disso, ao longo do processo de compra, o conteúdo se torna mais direcionado para ofertas específicas ou outros itens voltados para o fechamento de uma venda. Depois que a solução é adquirida, as informações são alteradas novamente para fornecer guias passo a passo, práticas recomendadas, informações sobre eventos futuros ou conteúdo sobre vendas adicionais. Mesmo que um indivíduo não tenha interagido com o conteúdo da fase inicial, é possível avançá-lo para a fase atual com base nas ações de outros em sua conta ou grupo de compras.

## Arquitetura de alto nível

O Adobe Journey Optimizer B2B edition é fundamentado no Adobe Experience Platform, incluindo o Real-Time CDP B2B. O Journey Optimizer B2B edition e o Marketo Engage são executados em sistemas separados, cada um com seu próprio armazenamento de dados. O Experience Platform é o principal armazenamento de dados e a fonte autoritativa de contas, pessoas e oportunidades. O Journey Optimizer B2B edition é proprietário das suas jornadas de conta, grupos de compra e funções de grupo de compra.

Uma instância dedicada do Marketo Engage é compatível com cada assinatura do Journey Optimizer B2B edition. Essa instância não armazena as jornadas da conta, os públicos-alvo ou os grupos de compra. Em vez disso, ele fornece direitos e serviços de back-end, como entrega de email, configuração de remetente e domínios de marca.

Para oferecer suporte a ações de jornada, também é possível conectar uma ou mais instâncias existentes do Marketo Engage, incluindo a instância de produção. As ações de jornada permitem que os profissionais de marketing coordenem jornadas baseadas em conta no Journey Optimizer B2B edition com campanhas baseadas em lead no Marketo Engage, como adicionar pessoas a uma lista ou campanha de solicitação. [Saiba mais sobre como conectar instâncias do Marketo Engage](./admin/marketo-actions-connect.md).

![Arquitetura de dados de alto nível que mostra o Journey Optimizer B2B edition conectado ao Adobe Experience Platform como fonte da verdade para públicos de contas e pessoas, uma instância dedicada do Marketo Engage que fornece direitos e serviços de back-end e uma instância opcional de produção do Marketo Engage usada para executar ações de jornada.](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>Verifique seus direitos de licença e a [descrição do produto](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondente para obter as medidas de proteção de desempenho e as limitações estáticas.

### Modelo de assinatura

Uma sandbox da Experience Platform emparelhada com uma instância dedicada do Marketo Engage define uma assinatura do Journey Optimizer B2B edition. Essa instância dedicada é separada da instância do Marketo Engage de produção e existe para oferecer suporte a direitos e serviços de back-end, em vez de armazenar dados de jornada de conta. [Saiba mais sobre a configuração](./setup-ultimate.md).

O Experience Platform fornece uma exibição unificada de dados de suas instâncias conectadas do Marketo Engage e sistemas de CRM. Use esses dados unificados para criar e executar suas jornadas.

### Jornada operações

O Journey Optimizer B2B edition cria, armazena e executa as jornadas da conta. As jornadas de conta não aparecem no Marketo Engage e só podem ser usadas no Journey Optimizer B2B edition.

Uma jornada sempre começa com um público-alvo que qualifica leads ou contas e suas pessoas para a jornada. Selecione este público usando o seletor de público padrão do Experience Platform. Os profissionais de marketing implementam a jornada dividindo caminhos usando critérios de conta, critérios de pessoas ou critérios de grupo de compras. Em cada caminho, as ações enviam comunicações ou aguardam a ocorrência de um evento.

Depois de criar uma jornada de conta, publique-a para ativar a jornada. Contas qualificadas inserem uma jornada publicada em 24 horas.

### Fluxo de dados

O Journey Optimizer B2B edition funciona como um destino do Adobe Real-Time CDP B2B edition. Use a segmentação de conta da Real-Time CDP para criar e avaliar os públicos-alvo da conta e de pessoas que qualificam contas e pessoas para uma jornada. Ao publicar uma jornada, o Journey Optimizer B2B edition ativa os públicos-alvo qualificados do Experience Platform.

Grupos de compras, funções de grupos de compras e pontuações de grupos de compras são criados e armazenados no Journey Optimizer B2B edition. [Saiba mais sobre grupos de compras](./buying-groups/buying-groups-overview.md).
