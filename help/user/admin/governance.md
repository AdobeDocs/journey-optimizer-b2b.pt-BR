---
title: Recursos de governança e privacidade
description: Saiba mais sobre os recursos de governança disponíveis atualmente no Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 0%

---

# Recursos de governança e privacidade

[!DNL Journey Optimizer B2B Edition] é um aplicativo Adobe Experience Platform integrado. Ela emprega várias ferramentas e serviços que fornecem controle dos dados de experiência coletados em conformidade com as práticas comerciais, as obrigações legais e os processos de desenvolvimento. As seções abaixo fornecem um resumo de cada um desses recursos de governança.

## Privacidade

Há várias regulamentações que se aplicam a clientes do [!DNL Journey Optimizer B2B Edition] que detêm dados para residentes nas respectivas regiões ou países mencionados acima (UE, Califórnia, Tailândia, Brasil, Nova Zelândia). Estas informações nesta página não são um aconselhamento jurídico e não garantem a sua conformidade com a legislação aplicável.

### RGPD

O Regulamento Geral sobre a Proteção de Dados (GDPR) é a lei de privacidade da União Europeia (UE) que adequa e moderniza os [requisitos de proteção de dados](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"} para os países membros da UE.

[!DNL Journey Optimizer B2B Edition] usa os recursos de governança do GDPR da Marketo Engage fornecidos pelo Serviço de Agente de Privacidade da Privacy Service e da Marketo.

### CNIL

Em 14 de abril de 2026, a Commission nationale de l&#39;informatique et des libertés (CNIL) [publicou uma recomendação](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf) sobre o uso de pixels de rastreamento em emails. As orientações esclarecem quando o consentimento é necessário e destacam a importância de práticas de consentimento adequadas para o rastreamento de pixels de email. Essa política afeta qualquer entidade que envie emails a assinantes com sede na França.

A CNIL forneceu um período de três meses a partir da data da recomendação para que as empresas informassem seus destinatários de email sobre a presença dos pixels de rastreamento, sua finalidade e o direito dos destinatários de recusar. Durante esse período de transição, os usuários do Marketo Engage devem notificar seus recipients sobre o rastreamento de pixels e fornecer uma opção de não participação, se necessário. A CNIL deve iniciar as atividades de fiscalização após 14 de julho de 2026.

À medida que a CNIL e outros reguladores esclarecem orientações sobre rastreamento de pixels e questões relacionadas, a Adobe continuará a monitorar atualizações e informá-lo sobre as mudanças de recursos técnicos.

O [!DNL Journey Optimizer B2B Edition] oferece controles que ajudam você a gerenciar o rastreamento aberto no nível do email. Os usuários são responsáveis por determinar suas próprias obrigações de conformidade de acordo com as orientações e outras leis aplicáveis da CNIL. Para obter informações sobre como usar esses recursos para gerenciar o rastreamento de aberturas de email, consulte [_Gerenciar rastreamento de email_](../content/email-tracking-manage.md).

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
