---
title: Journey Agent B2B
description: Saiba como usar o Journey Agent alimentado por IA e suas habilidades para criar, gerenciar e observar jornadas B2B robustas.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
source-git-commit: 51bb47fe4f494095f1c598639f02f273b9a125ae
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Journey Agent B2B

O Journey Agent B2B é um assistente alimentado por IA no Adobe Journey Optimizer B2B edition que ajuda você a projetar, executar, otimizar e monitorar jornadas B2B por meio da linguagem natural. Ele reduz o tempo e a complexidade envolvidos na criação e no gerenciamento de jornadas do cliente, combinando automação, recomendações orientadas por dados e observação em tempo real.

![Prompt B2B do Journey Agent](./assets/journey-agent-prompt.png)

O B2B do Journey Agent fornece um conjunto de habilidades de IA, cada uma focada em um aspecto diferente do ciclo de vida da jornada B2B. As habilidades disponíveis atualmente são:

* **[Habilidade de compilação do Jornada](#journey-build-skill)** - Crie, atualize e otimize jornadas a partir de prompts de linguagem natural
* **[Habilidade de observação da Jornada](#journey-observability-skill)** - Faça perguntas sobre como as contas e as pessoas estão se movimentando pelas jornadas ativas

## Habilidade do Jornada Build

A habilidade Build do Jornada traduz seus objetivos de marketing, estratégia de engajamento e KPIs em jornadas completas de clientes B2B. Ele aborda três desafios principais que os profissionais de marketing B2B enfrentam atualmente:

* Lidar com jornadas cada vez mais complexas do cliente (complexidade no público-alvo, conteúdo e mensagens e onicanal)
* Aumento da eficiência à luz de orçamentos mais apertados
* Descobrir como a jornada ideal do cliente deve ser estruturada

Como profissional de marketing, você pode usar essa habilidade para:

* **Criar** - Traduza objetivos de marketing, produtos, estratégia de engajamento e KPIs em uma jornada de cliente personalizada com automação e condições
* **Recomendado** - Aproveite o engajamento de marketing anterior e outros dados históricos para otimizar a criação de jornadas
* **Otimizar** - Analisar, ajustar e otimizar jornadas ativas com base em previsões ou no desempenho real
* **Gerenciar** - Priorizar, gerenciar e orquestrar jornadas sobrepostas e entrega de mensagens

### Uso básico

Para usar a habilidade do Journey Agent Build, digite na janela do prompt o que deseja criar, usando a linguagem natural:

&quot;Crie uma jornada B2B para convidar tomadores de decisão para uma apresentação em contas engajadas com maior probabilidade de abrir um novo pipeline.&quot;

![Solicitação B2B do agente de Jornada para a habilidade de compilação](./assets/journey-agent-tasks.png)

Quanto mais detalhes puder fornecer, melhor será a resposta. Se você tiver material de marketing existente que descreva o evento, seu produto etc., cole-o no prompt para que o agente tenha um melhor senso do objetivo.

&quot;Atue como um estrategista de jornada B2B para criar uma jornada de conta de cliente em vários estágios que nutre e envolva tomadores de decisão e profissionais de marketing na fase inicial de exploração do `<Solution Name>`. O objetivo é converter visitantes anônimos em contatos conhecidos, aprofundar o engajamento com conteúdo relevante no `<domain>`.com e fornecer clientes potenciais qualificados para `<Product Name>` alcance de vendas. Use canais como email e mídia paga, aproveitando o conteúdo e os segmentos de público-alvo existentes. Estruturar a jornada em estágios de conscientização, consideração e avaliação ao longo de 4 a 6 semanas, com acionadores, ações e metas claros para cada estágio. Inclua KPIs como taxas de conversão, pontuações de engajamento e solicitações de demonstração e retorne a saída como um fluxo de jornada estruturado.&quot;

Este prompt detalhado fornece:

* **Limpar intenção**: o que você deseja que a IA faça? Seja específico sobre a tarefa ou o resultado.
* **Rico Em Contexto**: Forneça o plano de fundo ou as restrições relevantes. Inclua exemplos ou referências, se possível.
* **Formato Estruturado**: Use marcadores, etapas numeradas ou modelos.
* **Atribuição de função**: especifique a função da IA - &#39;Atue como um analista de dados...&#39;

Use o agente para iterar o refinamento: comece de forma simples e, em seguida, refine seu prompt com base nos resultados. Os loops de feedback melhoram os resultados ao longo do tempo.

### Criação completa de jornadas B2B

A habilidade Build do Jornada pode gerar um fluxo de jornada completo (jornada de conta ou pessoa) a partir de prompts de texto e metadados em linguagem natural, por meio de uma experiência conversacional em vez de uma interface de usuário tradicional.

Exemplos completos de prompt de Jornada:

* Crie uma jornada entre canais para nutrir contas que não se envolveram com meu conteúdo nos últimos 30 dias.
* Crie uma jornada para fazer a venda cruzada de uma solução para contas que mostram alta intenção sem pipeline aberto, fornecendo conteúdo personalizado para as funções de grupo de compra mais importantes.
* Crie uma jornada B2B para convidar tomadores de decisão para uma apresentação em contas engajadas com maior probabilidade de abrir um novo pipeline.
* Crie uma jornada para contas de espaço em branco com intenção para minha solução, focando pessoas envolvidas com conteúdo no site.

### Jornadas em vários estágios

Você pode agir como um designer de jornada B2B para criar uma jornada de conta de cliente em vários estágios que informa os tomadores de decisão e os profissionais de marketing antecipadamente na fase de exploração.
O objetivo é converter visitantes anônimos em contatos conhecidos, aprofundar o engajamento com conteúdo relevante e fornecer leads qualificados para alcance de vendas.

* Use canais como `Email`, `Paid media`, `Personalized web experiences` para aproveitar os segmentos e o conteúdo de público existentes.
* Estruturar a jornada nos estágios `awareness`, `consideration` e `evaluation` de 4 a 6 semanas, com acionadores, ações e metas claros para cada estágio.
* Inclua KPIs, como `conversion rates`, `engagement scores` e `demo requests`, e retorne a saída como um fluxo de jornada estruturado.

## Jornada habilidade de observação

A habilidade Observability do Jornada permite que você faça perguntas em linguagem natural sobre como as contas e as pessoas estão se movendo através de suas jornadas B2B, sem pesquisar em mapas, logs ou painéis de jornada. Abrange duas áreas principais: progressão da jornada e observabilidade da sincronização de dados.

Você pode acessá-lo em dois lugares no Journey Optimizer B2B edition:

* **Assistente do painel direito no mapa de jornadas** - Faça perguntas específicas sobre jornadas diretamente no mapa de jornadas. O nome da jornada é inserido automaticamente no contexto.

* **Página do Assistente de Tela Inteira** - Uma exibição conversacional maior, adequada para perguntas complexas ou entre contas, e para explorar várias jornadas.

### Jornada insight no nível da conta

Rastreie como uma conta específica fluiu por uma jornada fazendo perguntas como:

* &quot;Dê-me informações básicas sobre a conta ACME Industries.&quot;
* &quot;Conte-me como a Northstar Services passou pela Estratégia de Amparo da jornada ABM.&quot;
* &quot;Quando a conta da Contoso LLC iniciou essa jornada?&quot;

### Raciocínio e contagens de caminho de nó dividido

Entenda por que uma ramificação foi criada e quantas pessoas ou contas seguiram cada caminho:

* &quot;Por que a conta QiDemoAccount24 foi para o pequeno caminho técnico da Califórnia nos EUA no nó dividido c764a9?&quot;
* &quot;Dê-me a contagem de pessoas para cada caminho no nó dividido-459c7c.&quot;
* &quot;Mostre-me pessoas no caminho de San Jose para Account8.&quot;

O agente inspeciona a lógica de divisão, os atributos da conta e as atividades para explicar as decisões de roteamento e retornar contagens por caminho ou listas de pessoas.

### Resultados da jornada no nível de pessoas

Analise os resultados individuais em uma conta ou em uma jornada inteira, especialmente útil para a análise de grupos de compras e o rastreio do responsável pela tomada de decisões em relação ao comportamento do influenciador:

* &quot;Dê-me a contagem de pessoas em cada caminho para este nó dividido da Account123.&quot;
* &quot;Listar pessoas no caminho de salto oculto.&quot;
* &quot;Mostre-me as pessoas no caminho de localização de San Diego para esta conta.&quot;

### Ciclo de vida e tempo da jornada

Recuperar carimbos de data e hora principais para uma jornada ou contas específicas:

* &quot;Quando esta jornada foi publicada?&quot;
* &quot;Quando a primeira conta entrou nessa jornada?&quot;
* &quot;Quando a conta QiDemoAccount50 iniciou essa jornada?&quot;

### Público externo e visibilidade de ativação

No caso de jornadas enviadas para canais externos, como LinkedIn, é possível verificar o status de ativação:

* &quot;O bsmith@acme.com está no público externo?&quot;
* &quot;Lista todas as pessoas ativadas para o LinkedIn por meio de ObservabilityExtAudience01.&quot;

### Sincronização de dados e observabilidade do pipeline

A habilidade Observability também pode exibir informações de integridade da sincronização de dados para ajudar a solucionar problemas por que uma conta ou um lead pode não ter sido incluído em uma jornada:

* Métricas e status do trabalho de exportação de público externo
* Agendamentos de segmentação em lote e horários de conclusão
* Programação de manutenção do grupo de compras
* Estatísticas do gerenciador de trabalhos (concluído/com falha)