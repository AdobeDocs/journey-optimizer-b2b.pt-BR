---
title: Recursos de governança
description: Saiba mais sobre os recursos de governança disponíveis atualmente no Journey Optimizer B2B edition.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 3198ba223125c95263d8dcf5ee8cb285a888a26a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Recursos de governança

O Journey Optimizer B2B edition é um aplicativo Adobe Experience Platform integrado. Ela emprega várias ferramentas e serviços que fornecem controle dos dados de experiência coletados em conformidade com as práticas comerciais, as obrigações legais e os processos de desenvolvimento. As seções abaixo fornecem um resumo de cada um desses recursos de governança.

## Privacidade - GDPR

O Journey Optimizer B2B edition usa os recursos de governança do GDPR de Marketo Engage existentes fornecidos pelo Privacy Service e pelo Serviço de Agente de Privacidade da Marketo.

## Controle de acesso baseado em função (RBAC)

Com o Journey Optimizer B2B edition e acesso ao Adobe Admin Console, os administradores podem conceder permissões a um usuário em um Tipo de entidade (exibir segmentos, gerenciar segmentos, gerenciar jornadas e assim por diante). Esse recurso faz parte da Estrutura de permissões unificadas (UPF) que permite que todos os clientes da Adobe Experience Platform definam e gerenciem funções e permissões para sua organização.

## Criptografia de dados

**_Criptografia para dados em repouso_** - Todos os dados de contas e perfis de pessoas transferidos do Adobe Experience Platform para o Journey Optimizer B2B edition são criptografados para manter a conformidade existente do Experience Platform. Todas as entidades originárias do Journey Optimizer B2B edition, como jornadas e grupos de compra, também são criptografadas.

**_Criptografia para dados em trânsito_** (em uma rede pública) - Todas as APIs e entidades do Journey Optimizer B2B edition são criptografadas em trânsito usando TLS 1.2.

## Aceitação/recusa de consentimento

Aceitação/recusa de consentimento é uma forma de governança em que um perfil pode recusar um canal de comunicação, como email ou SMS, e um perfil é excluído do canal de comunicação.

Com o Journey Optimizer B2B edition, você pode criar e gerenciar casos de uso de assinatura/cancelamento de assinatura para seus casos de uso de delivery de email e SMS. Essas preferências de consentimento são armazenadas no Grupo de campos de consentimento do perfil XDM e são sincronizadas de e para o Journey Optimizer B2B edition como parte da Estrutura de sincronização de dados. Essas preferências são usadas no momento do delivery para excluir perfis que optaram por não participar.

## Redefinição de área restrita

A redefinição da sandbox **não é suportada no momento** para o Adobe Journey Optimizer B2B edition. Redefinir ou excluir uma sandbox mapeada para o Journey Optimizer B2B edition pode resultar em perda permanente de dados no Journey Optimizer B2B edition e exigir o provisionamento de uma nova instância do Journey Optimizer B2B edition.

## Ainda não disponível

Os seguintes recursos de governança ainda não estão disponíveis:

* Aplicação de rótulo de uso de dados (DULE) / políticas de uso
* Higiene de dados
* Políticas de consentimento
* FLAC (Field-Level Access Control, controle de acesso em nível de campo)
* Controle de acesso em nível de objeto (OLAC)
* Criptografia CMK para dados em repouso
* Serviço de auditoria de plataforma
