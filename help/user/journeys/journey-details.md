---
title: Detalhes do Jornada
description: Monitore o desempenho da jornada da conta com taxas de conclusão, métricas de envolvimento, análise de email/SMS e insights de IA no Journey Optimizer B2B edition.
feature: Dashboards, Account Journeys
role: User
exl-id: 09a0e06a-1fd3-44da-9774-23f125f2823d
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: 2026-03-30T23:21:08.953Z
TQID: https://experienceleague.adobe.com/a5tIOW39sq3Lq30pQ3yr7-IvLGaAXC6LKqY8-mpxCDY
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 0%

---

# Detalhes da jornada

Ao clicar no nome de uma jornada de conta ativa, os detalhes da jornada são exibidos. A guia _[!UICONTROL Visão geral]_ fornece informações úteis sobre a jornada, incluindo resumos de IA generativos.

Esse painel fornece uma visão geral abrangente de uma jornada de conta selecionada, detalhando o progresso da conta usando gráficos de círculo e de linha que categorizam e quantificam conclusões, atividades em andamento e anulações ao longo do tempo. Ele ajuda as equipes de marketing a avaliar a eficácia de canais de email e SMS por meio de métricas principais de entrega e engajamento. Para métricas de email agregadas em todas as jornadas, consulte o [Relatório de desempenho de email](../dashboards/email-performance-dashboard.md).

Essa visão geral está disponível para jornadas de conta publicadas e leva aproximadamente quatro horas para que os dados comecem a preencher os gráficos e as tabelas.

![Acessar os detalhes da jornada ativa](./assets/journey-detail-overview.png){width="700" zoomable="yes"}

## Conclusão da jornada

Esta seção apresenta duas métricas de conclusão:

* **[!UICONTROL Status da Jornada]** - Este gráfico de círculo oferece um detalhamento dos status de jornada categorizando as contas em _Concluídas_, _Em Andamento_ e _Anuladas_. Cada segmento é rotulado com as porcentagens e os números de conta correspondentes na borda externa do gráfico.
* **[!UICONTROL Conclusão de Jornada ao longo do tempo]** - Este gráfico de linha controla o número de contas que concluíram sua jornada ao longo do tempo. O eixo horizontal mapeia a linha do tempo enquanto o eixo vertical quantifica as contas, fornecendo uma visualização simples das tendências de conclusão.

## Jornada envolvimento

Esta seção apresenta duas métricas de engajamento:

* **[!UICONTROL Envolvimento por contas]** - Este gráfico de círculo segmenta as contas em uma jornada em _Envolvido_ e _Não envolvido_ categorias. A figura central exibe a contagem total. Essa visualização fornece uma rápida compreensão do envolvimento geral com a conta.
* **Participação de pessoas** - Esta visualização exibe o número total de pessoas qualificadas como _envolvidas_ em uma jornada.

## Desempenho da jornada

Esta seção apresenta duas métricas vitais:

* **[!UICONTROL Taxa de conclusão da Jornada]** - A porcentagem de contas que concluíram com êxito sua jornada.
* **[!UICONTROL Duração da Jornada]** - O tempo médio necessário para que as contas concluam a jornada.

## Desempenho de email e SMS

As tabelas de desempenho fornecem informações detalhadas sobre a eficácia dos canais de email e SMS. Cada tabela mostra métricas, como taxas de delivery e taxas de click-through, que ajudam a avaliar o impacto de cada ponto de contato de comunicação. As tabelas abaixo mostram métricas de email e SMS somente para esta jornada. Para as mesmas métricas de email em todas as jornadas, use o [Relatório de desempenho de email](../dashboards/email-performance-dashboard.md).

Colunas da tabela de **[!UICONTROL Desempenho do email]**:

* _[!UICONTROL Nome do ativo]_ - Nome do ativo
* _[!UICONTROL Enviado]_ - Número de emails enviados
* _[!UICONTROL Taxa de entrega]_ - Número de emails entregues dividido pelo número enviado
* _[!UICONTROL Taxa de Abertura]_ - Número de emails abertos dividido pelo número entregue
* _[!UICONTROL Taxa de click-through]_ - Número de emails clicados dividido pelo número entregue

**[!UICONTROL Colunas da tabela de desempenho de SMS]**:

* _[!UICONTROL Nome do ativo]_ - Nome do ativo
* _[!UICONTROL Enviado]_ - Número de mensagens SMS enviadas
* _[!UICONTROL Taxa de entrega]_ - Número de mensagens SMS entregues dividido pelo número enviado
* _[!UICONTROL Taxa de click-through]_ - Número de mensagens SMS clicadas dividido pelo número entregue
<!--
To generate a shareable PDF of your current view, click **[!UICONTROL Export]** at the top right of the page. 
-->

## Melhor interação

Interaja com os dados usando o ícone de ação (**...**) na parte superior direita de cada gráfico ou tabela.

### Drill-Through

Para o gráfico _[!UICONTROL status da Jornada]_, escolha **[!UICONTROL Drill-through]** para obter uma análise detalhada dos status de contas individuais.

![O drill-through para os dados de gráfico](./assets/journey-status-drill-through.png){width="600" zoomable="yes"}
<!--
The applied global filters are carried over to the view and displayed at the top. Click the _Filter_ icon at the top left to filter the data display by journey.
-->

### Visualizar mais

Escolha **[!UICONTROL Exibir mais]** para acessar os dados estendidos. O pop-up exibido fornece um detalhamento dos dados.

![Exibir dados estendidos](./assets/journey-completion-over-time-view-more.png){width="600" zoomable="yes"}

Para baixar os dados, clique em **[!UICONTROL Baixar CSV]** na parte superior direita da tabela de dados. Para retornar ao painel _Visão geral_, clique em **[!UICONTROL Fechar]**.
