---
title: Criar modelos de pontuação personalizados
description: Crie, visualize e publique modelos de pontuação de lead personalizados no Journey Optimizer B2B Prime usando a habilidade Scoring Studio na interface de bate-papo do Assistente de IA.
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
autotag-review: '2026-06-25T21:20:26.754Z'
TQID: 'https://experienceleague.adobe.com/-D5EaJ-3GQ5iwaE6hChscZGEdflKmZ3tdp6VUNuPjWk'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d8f352c636ebd8980614922099701de8f755e8e4
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 2%

---

# Criar modelos de pontuação personalizados

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Scoring Studio"
>abstract="Use a habilidade Scoring Studio para criar, configurar e publicar modelos de pontuação de lead personalizados por meio da interface de bate-papo do Assistente de IA."

A habilidade [_Scoring Studio_](./skills.md#scoring-signals) em [!DNL Adobe Journey Optimizer B2B Prime] fornece uma solução de pontuação de cliente potencial nativa de IA que permite criar, configurar e publicar modelos de pontuação de cliente potencial. O estúdio combina um fluxo de trabalho orientado por agente com uma interface visual — você pode criar modelos de pontuação por meio de prompts de linguagem natural na [interface de chat do Assistente de IA](./chat-interface.md) ou interagindo diretamente com os controles da interface.

* **Habilidade** - `scoring-studio`
* **Invocação** - Use um comando de barra para abrir o Scoring Studio. Por exemplo: _&quot;abrir Scoring Studio.&quot;_
* **Leituras/gravações em** - [!DNL Journey Optimizer B2B Prime] serviço de pontuação; lê [!DNL Marketo Engage] campos de cliente potencial e tipos de atividade

No lançamento, o Assistente de IA busca automaticamente contexto relevante — incluindo tipos de atividade, campos de cliente potencial, listas de pessoas e listas de pontuação existentes — para fundamentar suas sugestões em seus dados.

![O Scoring Studio foi iniciado na interface de chat do Assistente de IA](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Criar um modelo de pontuação {#create-model}

Quando você abre o Scoring Studio, o Assistente de IA propõe um modelo de pontuação de exemplo relevante pré-preenchido com uma lista estática e um conjunto de atividades pontuadas. Você pode aceitar esse ponto de partida sugerido ou fornecer seu próprio prompt para definir um modelo personalizado.

### Visualizar o modelo {#preview-model}

Depois de fornecer um prompt, o Assistente de IA gera uma pré-visualização do modelo antes de fazer qualquer alteração. A visualização é exibida:

* Dimensões de pontuação em uso
* Atributos e atividades que estão sendo pontuados
* Listas estáticas ou smart lists aplicadas como segmentos
* Um resumo da meta do modelo, do segmento alvo e dos sinais primários

Você pode revisar a visualização e optar por criar o modelo com base nele ou continuar refinando o chat antes de finalizar.

### Estrutura do modelo {#model-structure}

O modelo criado está organizado em _dimensões_ e _sinais_. Você pode configurar cada sinal usando o painel de propriedades na interface do usuário:

* **Tipo de sinal** — baseado em atividade ou em atributo
* **Atividade ou atributo** — O item específico a ser pontuado
* **Parâmetros de sinal** — Configurações ajustáveis para o sinal

Você pode criar e configurar modelos totalmente por meio do agente usando linguagem natural ou interagir diretamente com os controles da interface do usuário.

## Publicar um modelo de pontuação {#publish-model}

Quando seu modelo estiver finalizado, instrua o agente a publicá-lo. O processo de publicação trata automaticamente do seguinte:

| Etapa | O que acontece |
|---|---|
| **Compilação de regras** | Todas as regras de pontuação são compiladas e validadas |
| **Criação da tarefa de pontuação** | Uma tarefa de pontuação programada é criada e configurada para ser executada diariamente |

Após a publicação, você também tem a opção de acionar uma execução manual para processar pontuações imediatamente.

## Exibir resultados de pontuação {#view-results}

Quando uma execução de pontuação é concluída, as pontuações são gravadas de volta em [!DNL Marketo Engage] por meio do processo de importação de clientes potenciais. Após a conclusão da importação, as pontuações atualizadas podem ser verificadas diretamente no [!DNL Marketo Engage].

Após cada execução, é possível exibir um resumo dos resultados que mostra:

* Quantas pessoas foram pontuadas
* A pontuação individual muda por pessoa

Um log de auditoria está disponível para revisar detalhes de execução adicionais.
