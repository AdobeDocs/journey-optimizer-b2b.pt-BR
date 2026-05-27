---
title: Relatório de desempenho de emails
description: Use o Relatório de desempenho de email no Journey Optimizer B2B edition para monitorar as métricas de envio de email, entrega, engajamento e recusa em todas as jornadas em uma exibição unificada.
feature: Dashboards, Reporting
role: User
autotag-review: '2026-05-21T15:04:51.176Z'
TQID: 'https://experienceleague.adobe.com/hA63o9-2-atw0kRNFeEu6H449WmZ59CjL3uiVS7nEcA'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 833
ht-degree: 5%

---

# Relatório de desempenho de email

O relatório de **Desempenho do email** fornece aos profissionais de marketing uma exibição unificada da atividade de email em todas as jornadas do Adobe Journey Optimizer B2B edition. Ele agrega métricas de envio, entrega, envolvimento e recusa. Ao detectar contagens brutas e taxas calculadas, você pode monitorar a integridade da campanha, comparar o desempenho do email e identificar rapidamente os problemas de entrega ou engajamento. Para obter métricas em nível de jornada em canais de email e SMS, consulte o [painel Jornadas da conta](./journeys-dashboard.md).

## Acessar o relatório

1. Na navegação à esquerda, selecione **[!UICONTROL Painel]**.
1. Selecione a guia **[!UICONTROL Desempenho do email]** na parte superior do painel de relatórios.

![Relatório de desempenho de email](./assets/email-performance-dashboard.png){width="800" zoomable="yes"}

## Filtrar os dados

Clique no ícone _Filtro_ ( ![Ícone Filtro](../assets/do-not-localize/icon-filter.svg) ) na parte superior esquerda para filtrar a exibição de dados usando os dois tipos de filtro compatíveis. Esses filtros se aplicam a todos os painéis simultaneamente:

* **[!UICONTROL Jornada]** - Filtra o relatório para mostrar os dados de uma ou mais jornadas selecionadas. Use esse filtro para isolar o desempenho das jornadas importantes para sua campanha ou programa.

* **Intervalo de datas** - Restringe todas as métricas aos emails enviados dentro da janela de tempo especificada. Suporta intervalos predefinidos e um seletor de datas personalizado. O seletor de intervalo de datas está no canto superior direito do painel.

![Filtros de Jornada e intervalo de datas na caixa de diálogo de filtros](./assets/email-performance-filters.png){width="500"}

Ao alterar filtros na caixa de diálogo de filtros, clique em **[!UICONTROL Aplicar]**.

## Gráficos de métrica de contagem e taxa

A seção superior do Relatório de desempenho de email contém dois gráficos de barras lado a lado que fornecem um resumo visual da integridade geral do programa de email no intervalo de datas e na jornada selecionados.

**Contar métricas** — Exibe o volume absoluto de atividades de email. Cada barra representa a contagem total de um evento principal de email em todos os emails no escopo filtrado: Enviado, Entregue, Aberto, Clicado, Devolvido e Cancelamentos de assinatura.

**Métricas de taxa** — Exibe taxas de porcentagem calculadas, permitindo que você avalie a qualidade do envolvimento e da capacidade de entrega independentemente do volume: taxa de entrega, taxa de abertura, taxa de cliques, taxa de rejeição, taxa de clique para abrir e taxa de cancelamento de inscrição.

Passe o mouse sobre o gráfico para exibir dados numéricos.

![Passe o mouse sobre o gráfico de barras - contagem exibida](./assets/email-performance-counts-hover.png){width="500"}

| Métrica | Tipo | Descrição |
|--------|------|-------------|
| Enviado | Contagem | Número total de mensagens de email enviadas para entrega. |
| Entrega | Contagem | Emails aceitos com êxito pelo servidor de email do destinatário. |
| Aberto | Contagem | Número de emails entregues que foram abertos pelo menos uma vez. |
| Clicado | Contagem | Número de emails que receberam pelo menos um clique de link. |
| Devolvido | Contagem | Emails que não puderam ser entregues (rejeição permanente ou temporária). |
| Cancelamentos de inscrição | Contagem | Recipients que optaram por cancelar a inscrição por meio de um link no email. |
| Taxa de entrega | Taxa | Entregue ÷ Enviado. Indica a porcentagem de emails que chegaram às caixas de entrada. |
| Taxa de abertura | Taxa | Aberto ÷ Entregue. Mede o envolvimento do recipient com as linhas de assunto. |
| Taxa de cliques | Taxa | Clicado ÷ Entregue. Mede o envolvimento geral com cliques por email entregue. |
| Taxa de rejeição | Taxa | ÷ Devolvido. Realça a capacidade de entrega e os problemas de integridade da lista. |
| Taxa de cliques para abrir (CTOR) | Taxa | Clicado ÷ Aberto. Mede o conteúdo e a eficácia do CTA entre leitores envolvidos. |
| Taxa de cancelamentos de assinatura | Taxa | Cancelamentos De Assinatura ÷ Entregues. Relevância de sinais e adequação de público-alvo. |

## Tabela de desempenho de email

Na parte inferior da página, uma tabela detalhada mostra as métricas por email para cada ativo de email no escopo filtrado. Por padrão, a tabela exibe 10 linhas por página.

A coluna **Cancelar inscrição %** é uma métrica priorizada para monitorar a atividade de recusa diretamente na exibição de tabela.

| Coluna | Descrição |
|--------|-------------|
| Nome do e-mail | O nome do [ativo de email](../content/add-email.md) conforme configurado na jornada. |
| Enviado | Total de envios para este email dentro do intervalo de datas selecionado. |
| Entrega | Número de emails entregues com êxito aos servidores de email do destinatário. |
| % de Entrega | Entregue ÷ Enviado, expresso como uma porcentagem. |
| Aberturas | Número total de eventos abertos registrados para este email. |
| % Aberta | Aberturas ÷ Entregues, expresso como uma porcentagem. |
| Cliques | Total de eventos de clique em links para este email. |
| Clique em % | Cliques ÷ Entregue, expresso como uma porcentagem. |
| % CTOR | Taxa de cliques para abertura: Cliques ÷ aberturas, expresso como uma porcentagem. |
| Rejeições | Número de emails não entregues (devoluções permanentes + temporárias). |
| % de rejeição | Devoluções ÷ Enviado, expresso como uma porcentagem. |
| Percentual de cancelamentos | Cancelamentos De Assinatura ÷ Entregues. Métrica priorizada para monitorar a integridade da recusa. |
| Primeira atividade | Carimbo de data e hora do primeiro evento gravado (envio, abertura ou clique) neste email no período selecionado. |
| Última atividade | Carimbo de data e hora do evento gravado mais recente para este email no período selecionado. |

## Exportar dados do relatório

O relatório de desempenho de email oferece suporte à exportação de dados para análise adicional em ferramentas externas ou para compartilhar resultados com as partes interessadas. É possível exportar os dados da tabela no formato CSV, que é compatível com qualquer análise de dados ou ferramenta de BI.

>[!CAUTION]
>
>As exportações refletem os filtros ativos no momento. Verifique se o intervalo de datas e os filtros de jornada estão definidos corretamente antes da exportação para evitar dados incompletos no arquivo de saída.

**_Para exportar os dados do relatório:_**

1. Defina o intervalo de datas no canto superior direito e aplique a filtragem **[!UICONTROL Jornada]** conforme necessário.
1. Clique no ícone de menu **...** no canto superior direito do painel Desempenho de email e escolha **[!UICONTROL Exibir mais]**.
1. Clique em **[!UICONTROL Baixar CSV]** no menu.

   ![Exibir dados detalhados e baixar o CSV](./assets/email-performance-data-export.png){width="700" zoomable="yes"}

   O arquivo é baixado automaticamente para o local de download padrão do navegador.

1. Clique em **[!UICONTROL Fechar]** para retornar ao Relatório de desempenho de email.
