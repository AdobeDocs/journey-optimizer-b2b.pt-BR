---
title: Usar o assistente de IA
description: Saiba como o Assistente de IA pode ajudar você a aproveitar ao máximo os recursos do Journey Optimizer B2B edition.
feature: AI Assistant
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: d19ed2bbe850a14cb0563f6e3563cd8f1c8d3226
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Usar o assistente de IA no Journey Optimizer B2B edition

No Journey Optimizer B2B edition, o Assistente de IA é um recurso da interface do usuário que você pode usar para entender conceitos do produto, navegar e conhecer rapidamente os recursos do Journey Optimizer B2B edition e obter insights operacionais para seu ambiente específico. Ele também está disponível em vários produtos na Adobe Experience Cloud.

>[!IMPORTANT]
>
>É necessário um contrato para as Diretrizes de usuário da IA gerativa da Adobe Experience Cloud para que você possa usar o Assistente de IA. Para obter mais informações sobre este contrato e diretrizes de uso, consulte as [Diretrizes de usuário da IA gerativa da Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html).

Para acessar o Assistente de IA, clique no ícone no cabeçalho. O Assistente de IA é aberto em um painel à direita.

![Clique no ícone para acessar o Assistente de IA](./assets/ai-assistant-icon-displayed.png){width="420" zoomable="yes"}

A interface do Assistente de IA é exibida, fornecendo imediatamente informações para começar. Você pode usar as opções fornecidas em _Ideias para começar_ para responder a perguntas e comandos, como:

* Quais das jornadas da minha conta foram publicadas?
* Quais interesses de solução foram criados?
* Conte-me os principais benefícios do Journey Optimizer B2B edition.

No Adobe Journey Optimizer B2B edition, o Assistente de IA é compatível com os seguintes casos de uso:

## Conhecimento do produto

As perguntas de conhecimento do produto são sobre os conceitos do Journey Optimizer B2B edition relacionados aos aspectos do Adobe Journey Optimizer. Alguns exemplos de perguntas de conhecimento sobre produtos incluem:

* Como configurar contas do provedor de SMS?
* Como faço para enviar um email em uma jornada de conta?
* Como posso personalizar meu conteúdo de email?

Para fazer uma pergunta sobre um produto, digite-a no campo na parte inferior do painel e pressione Enter.

![Digite uma pergunta na caixa de texto](./assets/ai-assistant-ask-question.png){width="420" zoomable="yes"}

Você pode verificar as respostas retornadas pelo Assistente de IA revisando as citações disponíveis com cada resposta de conhecimento do produto.

Para exibir citações e validar a resposta do Assistente de IA, selecione **[!UICONTROL Mostrar fontes]**.

![Resultados da consulta do Assistente de IA](./assets/ai-assistant-answer.png){width="420" zoomable="yes"}

O Assistente de IA atualiza a interface e fornece links para a documentação que corroboram a resposta inicial. Além disso, quando as citações são ativadas, o Assistente de IA atualiza a resposta para incluir notas de rodapé para indicar as partes específicas da resposta que fazem referência à documentação fornecida.

Use a miniatura para cima ou para baixo para classificar a qualidade da resposta.

## Insights operacionais

As perguntas operacionais do insight são sobre os objetos de jornada na sandbox da sua organização. Alguns exemplos de perguntas ou prompts operacionais do insight incluem:

* Quantas jornadas ativas eu tenho no Adobe Journey Optimizer B2B edition?
* Fornecer uma lista de todas as jornadas agendadas
* Quantas jornadas foram criadas nos últimos sete dias?

Você deve estar em uma sandbox ativa para o Assistente de IA para fornecer uma resposta suficiente a uma pergunta sobre seus insights operacionais.

>[!NOTE]
>
>As únicas perguntas de insights operacionais do Adobe Journey Optimizer B2B edition com suporte pelo Assistente de IA estão listadas na [tabela de domínio de insights operacionais](./ai-assistant-overview.md#operational-insights). Ele pode acessar dados somente para a sandbox em que você está atualmente.

<!-- Select to view an example of an operational insights question.

In the following example, AI Assistant receives the following query: _Show me dataflows that were created using the Amazon S3 source._

screen

AI Assistant responds with a table list of your dataflows and their corresponding IDs. Click the _Download_ icon ( Download icon ) to download the table as a CSV file. To view the entire table, click the _Expand_ icon ( Expand icon ).

screen

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

screen

When prompted with an operational insights question, AI Assistant provides an explanation of how it computed the answer. In the following example, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the Amazon S3 source.

screen

You can also provide filters and modifications to your questions, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

### Verify operational insights responses

You can verify each response related to operational insights questions using an SQL query that AI Assistant provides.

Select to view example of verifying operational insights responses

After receiving an answer for an operational insights question, click **[!UICONTROL Show sources]** and then select **[!UICONTROL View source query]**.

screen

When queried with an operational insights question, AI Assistant provides an SQL query that you can use to verify the process that it took to compute its answer. This source query is for verification purposes only and is not supported on Query Service.

screen  

 -->
