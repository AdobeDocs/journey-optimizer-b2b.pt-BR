---
title: Guia de perguntas para o Assistente de IA
description: Saiba como escrever perguntas eficazes para o Assistente de IA no Journey Optimizer B2B edition.
feature: AI Assistant
role: User
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 1%

---

# Orientação de pergunta para o Assistente de IA no Journey Optimizer B2B edition

Analise o seguinte conjunto de perguntas de exemplo para consultar o Assistente de IA no Journey Optimizer B2B edition. Essas informações também incluem dicas sobre como formular suas perguntas para obter respostas ideais do Assistente de IA.

## Perguntas baseadas em objetivos

Os exemplos de perguntas a seguir são agrupados de acordo com os objetivos que você pode realizar ao usar o Assistente do AI:

| Objetivo | Descrição | Exemplo |
| --- | --- | --- |
| Conceitos de aprendizado e fluxos de trabalho contínuos | Como usuário iniciante, você pode usar o AI Assistant para aprender conceitos do Real-Time CDP e do Adobe Journey Optimizer B2B edition e integrar-se a produtos e recursos com os quais não está familiarizado. <br>Como um usuário experiente, você pode usar o Assistente de IA para resolver um caso de borda que possa estar bloqueando seu fluxo de trabalho. | <li>Conte-me alguns casos de uso para o Real-Time CDP. <li>Explique o conceito do Grupo de Compras para mim. |
| Solução de problemas | Use o Assistente de IA para saber como depurar erros básicos que você pode encontrar no fluxo de trabalho. | <li>O que significa este erro &lt;ERROR_MESSAGE>? <li>Por que não posso excluir o público-alvo chamado &quot;...&quot;? |
| Higiene da sandbox | Use o Assistente de IA para identificar objetos duplicados ou não utilizados, para que você possa manter sua sandbox com eficiência. | <li>Você pode me mostrar públicos semelhantes da conta? <li>Há esquemas que não tenham um conjunto de dados associado? |
| Análise de valor | Use o Assistente de IA para identificar os objetos de dados mais usados e avaliar os indicadores de desempenho ou encontrar os objetos de dados mais valiosos. | <li>Quantas contas existem em nossa definição de segmento &quot;...&quot;? <li>Quando os públicos-alvo foram ativados para o destino do Experience Cloud Audiences? |
| Pesquisa | Use o AI Assistant para encontrar objetos compatíveis do Experience Platform e do Adobe Journey Optimizer B2B edition, como públicos-alvo de conta, conjuntos de dados, destinos, esquemas, fontes, jornadas de conta, modelos de grupo de compra e interesses de solução | <li>Liste os públicos-alvo que contêm &quot;Luma&quot; no nome que foram usados nas jornadas da conta. <li>Quais atributos estão no esquema XDM &quot;Luma: Ações personalizadas&quot;? |
| Análise de impacto | Use o Assistente do AI para identificar objetos de dados que foram usados em determinados workflows para que você possa avaliar o impacto de quaisquer alterações. | <li>Quais públicos-alvo de conta usam `workEmail.address` no esquema &quot;Pessoa B2B&quot;? <li>Em quais conjuntos de dados... `jobTitle` são armazenados? |

## Formular suas perguntas

Você deve enviar suas perguntas ao Assistente de IA com clareza e contexto para obter uma resposta o mais precisa possível. Consulte a seguinte lista de dicas para obter orientação sobre como fazer uma pergunta clara com contexto:

* Apresente sua tarefa e/ou pergunta de maneira concisa.
* Evite linguagem ambígua ou sintaxe excessivamente complexa para facilitar a compreensão.
* Forneça contexto relevante em relação à sua tarefa e/ou pergunta, pois o contexto pode ajudar o Assistente de IA a gerar respostas mais relevantes.

As tabelas a seguir fornecem algumas práticas recomendadas que você pode seguir ao usar o Assistente de IA:

| Fazer | Exemplo |
| --- | --- |
| <li>Seja específico sobre o objeto ou as informações que deseja recuperar ou analisar. <li>Tente colocar os nomes dos objetos de dados entre aspas. <li>Se você souber apenas uma parte do nome do objeto, também poderá especificá-lo na pergunta. | <li>Quais conjuntos de dados usam o esquema &quot;Conta B2B&quot;? <li>Mostre-me os públicos ativados que têm &quot;Account&quot; no nome. Classifique-os por contagem de membros. |
| <li>Evite ambiguidades e use linguagem clara. <li>Use terminologia precisa para garantir mais clareza em seu query. <li>Ao fazer perguntas sobre o Adobe Experience Platform e o Adobe Journey Optimizer B2B edition, tente usar a terminologia específica do Experience Platform ou do Adobe Journey Optimizer B2B edition para melhorar a relevância das respostas. | <li>Quantos membros eu tenho no &quot;Público-alvo da minha conta&quot;? <li>Quantas jornadas de conta usam o Público-alvo da conta &quot;Público-alvo da minha conta&quot;? |
| <li>Forneça contexto ou especifique um critério para filtrar os resultados. <li>Use um critério de filtro nas perguntas para limitar o volume de dados na resposta. | <li>Mostre-me os públicos da conta que não foram ativados e foram criados há mais de 6 meses e que nunca foram modificados. <li>Mostrar as jornadas de conta publicadas nos últimos 7 dias e usa um público de conta com mais de 1000 membros |

| Não | Exemplo |
| --- | --- |
| Use uma linguagem vaga ou ambígua. | <li>Forneça-me informações sobre conjuntos de dados. <li>O que o jornada x faz? <li>Quantos usuários eu tenho em &quot;ACME Audience&quot;? <li>Mostrar segmentos. <li>Listar atributos. |
| Faça solicitações incompletas. | <li>&quot;Luma - Conjunto de dados de fidelidade&quot; |
| Assumir conhecimento sem contextos. | <li>Públicos nos últimos 6 meses. <li>Criar uma consulta para mim. <li>Criar uma jornada para mim |
| Formular consultas muito complexas. | <li>Fornecer uma análise abrangente da linhagem de dados em todos os objetos e suas dependências. |
| Omitir critérios ou parâmetros. | <li>Mostre-me conjuntos de dados. |

## Exemplos de perguntas não suportadas

A lista a seguir inclui exemplos de perguntas que o Assistente de IA no Journey Optimizer B2B edition não é compatível no momento:

* Quais públicos-alvo de conta usam o campo workEmail.address do grupo de campos ... em sua condição? 
* Mostre-me o número de jornadas ativas usando públicos-alvo de conta com tamanho superior a 10.000, 5000-10.000, 1000-5000 e abaixo de 1000, em um visual de distribuição
* Quem fez a última atualização na jornada da conta x?
* Quantas jornadas ativas adicionam membros do grupo de compras para o interesse da solução x?
* Quais jornadas ativas adicionam membros do grupo de compra para o interesse de solução x?
* Qual é o título mais comum de tomador de decisão de modelos de grupo de compras?
* Quem são os tomadores de decisão para comprar o modelo x do grupo?

## Próximas etapas

Para obter informações sobre como usar os recursos do Assistente de IA durante os fluxos de trabalho, consulte [Usar o Assistente de IA no Journey Optimizer B2B edition](./use-ai-assistant.md).
