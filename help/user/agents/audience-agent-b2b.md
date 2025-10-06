---
title: Audience Agent B2B
description: Audience Agent B2B no Jornada OtimizerB2B Edition usa análise de intenção e mapeamento de persona para criar grupos de compra e acelerar workflows de marketing B2B.
feature: Audiences, AI Assistant
role: User
hidefromtoc: true
source-git-commit: 9cb77da73778c313392af1c42632d6b9e7e92f3b
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Audience Agent B2B

Equipado com o [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), o Audience Agent B2B está disponível no Journey Optimizer B2B edition. O uso desse agente melhora a eficiência e a eficácia na exploração e dimensionamento de públicos, acelerando a criação de grupos de compra e fluxos de trabalho contínuos para ativação de jornada:

* **_Priorizar públicos-alvo por intenção_** - Infira personalidades com base na intenção do produto para vários públicos-alvo e simplifique o planejamento de campanha, reduzindo o tempo gasto na validação do público-alvo.

* **_Aproveite a IA para detectar grupos de compras_** - Use a IA, dados estruturados, não estruturados e dados unificados de terceiros para simplificar a descoberta e a criação de grupos de compras.

![Audience Agent B2B no modo de página inteira](./assets/audience-agent-full.png){width="700" zoomable="yes"}

## Recursos do Audience Agent

| Área | O que faz | Valor comercial |
| ---- | ------------ | -------------- |
| Análise de intenção | <li> Meça a intensidade da intenção da conta (como baixa, média e alta) para produtos específicos. <li>Comparar tendências de interesse de produtos ao longo do tempo (como os principais produtos dos últimos _n_ dias). <li>Identificar contas que mostram ativamente interesse em produtos específicos. <li>Padrões de envolvimento de superfície que combinam atividade da conta com cobertura de persona. | <li>Ajuda as equipes a se concentrarem nas contas certas na hora certa. <li>Melhora a qualidade do pipeline ao priorizar contas com sinais de compra genuínos. <li>Permite o engajamento pró-ativo antes que os concorrentes ajam. |
| Mapeamento pessoal | <li>Detectar e classificar personalidades de alto nível por intenção de produto. <li>Identifique os perfis envolvidos na compra de um ou vários produtos. <li>Mapeie personas para funções funcionais (Champion, Decision Maker, Influencer etc.) com justificativa. <li>Validar por que uma determinada pessoa é considerada um campeão. | <li>Garante que as vendas envolvam os verdadeiros responsáveis pelas decisões e influenciadores. <li>Reduz o desperdício de esforços em contatos de baixo impacto. <li>Aumenta as taxas de ganho ao alinhar o alcance com a dinâmica do poder do comprador. |
| Avaliação do grupo de compras | <li>Avaliar o tamanho do grupo de compras (por exemplo, grupos com mais de n membros). <li>Meça a cobertura de persona nas contas (por exemplo, abaixo de x%). <li>Rastrear a distribuição de funções e as lacunas de cobertura nos grupos de compra. <li>Destaque as contas com campeões identificados em ofertas recentes. | <li>Revela lacunas de cobertura que podem impedir os negócios. <li>Fortalece as estratégias de múltiplos processos, garantindo uma representação completa das funções. <li>Melhora o rastreamento da integridade do negócio por meio de insights de engajamento no nível do grupo. |

## Exemplos de Prompt

Estes exemplos de prompts demonstram algumas maneiras pelas quais você pode usar o agente:

* Mostrar a janela de tendência: atualização mais antiga e mais recente da intenção de produto por produto da conta.
* Para `<product>`, liste os grupos de compras com intenção de produto e pontuações.
* Para `<product>`, liste perfis e funções com suas métricas de oportunidade (taxa de ganho, taxa de associação, contagens).
* Para contas em `<industry>`, qual é a cobertura de persona média da conta para `<product>`?
* Quais contas têm pouca intenção para qualquer produto, mas ainda têm oportunidades em aberto (que valha a pena cuidar)?
* Quais contas adicionaram novos sinais de intenção para `<account_name>` esta semana?
