---
title: Recursos de governança
description: Saiba mais sobre os recursos de governança disponíveis atualmente no Journey Optimizer B2B Edition.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Recursos de governança

Como um aplicativo Adobe Experience Platform integrado, o Journey Optimizer B2B Edition emprega vários serviços e ferramentas que permitem controlar com confiança seus dados de experiência coletados para cumprir com suas práticas comerciais, obrigações legais e processos de desenvolvimento. As seções abaixo fornecem um resumo de cada um desses recursos de governança.

## Privacidade - GDPR

O Journey Optimizer B2B Edition usa os recursos de governança do GDPR de Marketo Engage existentes fornecidos pelo Privacy Service e pelo Marketo Privacy Broker Service.

## Controle de acesso baseado em função (RBAC)

Com o Journey Optimizer B2B Edition e acesso à Adobe Admin Console, os administradores podem conceder permissões de usuário em um Tipo de entidade (exibir segmentos, gerenciar segmentos, gerenciar jornadas e assim por diante). Esse recurso faz parte da Estrutura de permissões unificadas (UPF) que permite que todos os clientes da Adobe Experience Platform definam e gerenciem funções e permissões para sua organização.

## Criptografia de dados

**_Criptografia para dados em repouso_** - Todos os dados de contas e perfis de pessoas transferidos do Adobe Experience Platform para o Journey Optimizer B2B Edition são criptografados para manter a conformidade existente do Experience Platform. Todas as entidades originárias do Journey Optimizer B2B Edition, como jornadas e grupos de compra, também são criptografadas.

**_Criptografia para dados em trânsito_** (em uma rede pública) - Todas as APIs e entidades do Journey Optimizer B2B Edition são criptografadas em trânsito usando TLS 1.2.

## Aceitação/recusa de consentimento

Aceitação/recusa de consentimento é uma forma de governança em que um perfil pode recusar um canal de comunicação, como email ou SMS, e um perfil deve ser excluído desse canal de comunicação.

Com o Journey Optimizer B2B Edition, você pode criar e gerenciar casos de uso de assinatura/cancelamento de assinatura para seus casos de uso de delivery de email e SMS. Essas preferências de consentimento são armazenadas no Grupo de campos de consentimento do perfil XDM e são sincronizadas para dentro e para fora do Journey Optimizer B2B Edition como parte da Estrutura de sincronização de dados. Essas preferências são usadas no momento do delivery para excluir perfis que optaram por não participar.

## Ainda não disponível

Os seguintes recursos de governança ainda não estão disponíveis, mas estão incluídos no roteiro do produto:

* Aplicação de rótulo de uso de dados (DULE) / políticas de uso
* Higiene de dados
* Redefinição de área restrita
* Políticas de consentimento
* FLAC (Field-Level Access Control, controle de acesso em nível de campo)
* Controle de acesso em nível de objeto (OLAC)
* Criptografia CMK para dados em repouso
* Serviço de auditoria de plataforma
