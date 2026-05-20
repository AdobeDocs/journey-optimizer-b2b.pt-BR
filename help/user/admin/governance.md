---
title: Recursos de governança
description: Saiba mais sobre os recursos de governança disponíveis atualmente no Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: d7e971b6d533a173632224baa359f7559b865497
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 0%

---

# Recursos de governança

O Journey Optimizer B2B edition é um aplicativo Adobe Experience Platform integrado. Ela emprega várias ferramentas e serviços que fornecem controle dos dados de experiência coletados em conformidade com as práticas comerciais, as obrigações legais e os processos de desenvolvimento. As seções abaixo fornecem um resumo de cada um desses recursos de governança.

## Privacidade - GDPR

O Journey Optimizer B2B edition usa os recursos de governança do GDPR da Marketo Engage fornecidos pelo Serviço de Agente de Privacidade da Privacy Service e da Marketo.

## Controle de acesso baseado em função (RBAC)

Com o Journey Optimizer B2B edition e acesso ao Adobe Admin Console, os administradores podem conceder permissões a um usuário em um Tipo de entidade (exibir segmentos, gerenciar segmentos, gerenciar jornadas e assim por diante). Esse recurso faz parte da Estrutura de permissões unificadas (UPF) que permite que todos os clientes da Adobe Experience Platform definam e gerenciem funções e permissões para sua organização.

## Criptografia de dados

**_Criptografia para dados em repouso_** - Todos os dados de conta e perfil de pessoa transferidos do Adobe Experience Platform para o Journey Optimizer B2B edition são criptografados para manter a conformidade existente do Experience Platform. Todas as entidades originárias do Journey Optimizer B2B edition, como jornadas e grupos de compra, também são criptografadas.

**_Criptografia para dados em trânsito_** (em uma rede pública) - Todas as APIs e entidades do Journey Optimizer B2B edition são criptografadas em trânsito usando TLS 1.2.

## Aceitação/recusa de consentimento

O Journey Optimizer B2B edition lê as preferências de consentimento por pessoa armazenadas nos perfis XDM do Adobe Experience Platform e as aplica no momento da entrega de mensagens para canais de email, SMS e WhatsApp. Uma pessoa que recusou a participação em um canal é excluída da entrega antes que o conteúdo seja enviado do canal ou do provedor de mensagens downstream.

O consentimento é avaliado no momento do delivery usando campos XDM do Grupo de campos de consentimento de perfil. O comportamento de consentimento padrão difere por canal — o padrão do email é aceitar quando nenhuma preferência é definida, enquanto o SMS e o WhatsApp assumem o padrão de recusar.

Para obter detalhes sobre os atributos XDM avaliados para cada canal e seus comportamentos padrão, consulte [Preferências de consentimento](../content/channels-consent-preferences.md).

## Redefinição de área restrita

A redefinição da sandbox **não é suportada no momento** para o Adobe Journey Optimizer B2B edition. Redefinir ou excluir uma sandbox mapeada para o Journey Optimizer B2B edition pode causar perda permanente de dados e exigir o provisionamento de uma nova instância.

## Ainda não disponível

Os seguintes recursos de governança ainda não estão disponíveis:

* Aplicação de rótulo de uso de dados (DULE) / políticas de uso
* Higiene de dados
* Políticas de consentimento
* FLAC (Field-Level Access Control, controle de acesso em nível de campo)
* Controle de acesso em nível de objeto (OLAC)
* Criptografia CMK para dados em repouso
* Serviço de auditoria de plataforma
