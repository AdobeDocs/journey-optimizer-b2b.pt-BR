---
title: Notas de versão
description: Notas de versão mais recentes do Adobe Journey Optimizer edição B2B
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Notas de versão do Journey Optimizer B2B edition

O Adobe Journey Optimizer B2B edition oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros.

O Journey Optimizer B2B edition é construído nativamente no [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest?lang=pt-BR){target="_blank"}.

Revise a [descrição do produto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} para obter informações sobre direitos, medidas de proteção de desempenho e limitações.

## Notas de versão de outubro de 2024 {#Oct-2024}

**Data de lançamento**: 29 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Conteúdo condicional em modelos de email | Personalize seu conteúdo de email com base no comportamento do recipient e nas características do perfil, tanto no nível da conta quanto no nível de lead. <p>Ao criar um email para sua jornada de conta no designer de email, use regras condicionais para definir várias variantes para qualquer componente de conteúdo. <a href="../content/conditional-content.md">Saiba mais</a> |
| Novo recurso | _Adicionar à Lista_ e _Remover da lista_ ações de pessoas no jornada | Personalize seu conteúdo de email com base no comportamento do recipient e nas características do perfil, tanto no nível da conta quanto no nível de lead. <a href="../journeys/action-nodes.md">Saiba mais</a> |
| Novo recurso | Governança de conteúdo e bloqueio de componentes | Para garantir a adesão aos designs de conteúdo aprovados, use os recursos de governança de conteúdo para bloquear componentes de conteúdo do modelo de email. Com a governança de conteúdo ativada no modelo de email, os profissionais de marketing podem alterar apenas os elementos permitidos para mantê-lo alinhado à estratégia de conteúdo. <a href="../content/template-content-governance.md">Saiba mais</a> |
| Novo recurso | Estágios do grupo de compra | Ao definir e publicar um modelo de preparo de grupos de compra personalizados, você pode rastrear a progressão dos grupos de compra nos estágios do ciclo de vida do grupo de compra. Use esses estágios para identificar as próximas melhores ações para membros do grupo de compras. Você configura as regras de transição e os nós de jornada que determinam a progressão do estágio e acionam as ações com base nas alterações. <a href="../buying-groups/buying-group-stages.md">Saiba mais</a> |
| Aprimoramento | Novos modelos de email prontos para uso | A biblioteca de modelos de amostra agora inclui modelos de email adicionais criados para profissionais de marketing B2B. Use esses modelos de amostra como ponto de partida e adicione sua própria identidade visual e mensagens. <a href="../content/email-templates.md#select-a-design-template">Saiba mais</a> |
| Aprimoramento | Campos personalizados como atributos de pessoa | Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta no Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa em condições. Use esses atributos personalizados em: <li>Modelos de funções <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a></li><li>Dividir caminhos por nós de jornada de pessoas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a></li> |
| Aprimoramento | Configurações do canal de email | As configurações de email agora estão visíveis na interface do Journey Optimizer B2B edition. Você pode examinar rapidamente as configurações atuais, e os administradores podem clicar em _[!UICONTROL Editar configurações]_ para ir diretamente para as configurações no Marketo Engage e atualizá-las de acordo com os requisitos da sua organização. <a href="../admin/configure-channels-emails.md">Saiba mais</a> |

## Notas de versão de setembro de 2024 {#Sept-2024}

**Data de lançamento**: 7 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Aprimoramento | Biblioteca de ativos central | A _biblioteca central de ativos_ aprimorada permite usar todos os ativos de imagem na sua instância do Marketo Engage, em todos os espaços de trabalho do Design Studio. Existem medidas de proteção integradas que impedem edições nos ativos Marketo Engage do Journey Optimizer B2B edition, bem como operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos e, ao mesmo tempo, permitem leitura e reutilização perfeitas no Journey Optimizer B2B edition.<p>Para ativos exclusivos para uso no Journey Optimizer B2B edition, um espaço de trabalho específico fornece funções completas de gerenciamento de ativos. <a href="../content/marketo-engage-design-studio.md">Saiba mais</a> |
| Novo recurso | Ativos acessados recentemente | A página inicial no aplicativo Journey Optimizer B2B edition agora inclui a seção _[!UICONTROL Acessados recentemente]_, que fornece uma lista dos ativos acessados mais recentemente para o profissional de marketing ou administrador. Você pode usar essa lista para ir diretamente para o ativo no qual você trabalhou recentemente sem navegar por uma série de páginas de ativos e pesquisas. <p>A lista fornece informações adicionais sobre a modificação para que você possa tomar a decisão sobre quais dos ativos precisam de modificações adicionais da última sessão. Para ativos de email, ele exibe a jornada da conta onde o ativo de email é usado. <a href="../home-page.md">Saiba mais</a> |
| Aprimoramento | Nó dividido do Jornada - reordenar caminhos | Em nós de caminho dividido, a filtragem de caminho é avaliada em ordem decrescente. Cada pessoa ou conta continua pelo primeiro caminho que corresponde a. Você pode reordenar os caminhos definidos clicando nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Saiba mais</a> |
| Aprimoramento | Jornada nó dividido - Atributos de condição de histórico de atividades adicionais | Ao usar condições para definir a filtragem de caminho para um nó dividido por pessoas, há dois atributos adicionais: _Email aberto_ e _Email entregue_. Essas adições fornecem maior flexibilidade para filtrar pessoas no jornada com base na atividade de email. <a href="../journeys/journey-nodes.md#split-paths">Saiba mais</a> |

## Notas de versão de agosto de 2024 {#Aug-2024}

**Data de lançamento**: 29 de agosto de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Públicos-alvo correspondentes da conta do linkedIn | Gere públicos-alvo de anúncio do LinkedIn por meio de Públicos-alvo correspondentes da conta para ajudar você a preencher funções vazias em seus grupos de compra. Definindo um conjunto de filtros de grupo de compras, você pode manter um Público-alvo correspondente do LinkedIn para direcionar prospetos que correspondem aos parâmetros do grupo de compras. <p>Esse recurso aproveita o Experience Platform Destinations para gerenciar alguns aspectos da integração. <a href="../data/linkedin-account-matched-audiences.md">Saiba mais</a> |
| Aprimoramento | Ciclo de vida do status para fragmentos de conteúdo visual | Os fragmentos visuais agora são gerenciados usando um ciclo de vida de status. O status do fragmento determina sua disponibilidade para uso em um email ou modelo de email e as alterações que você pode fazer nele. <p>Esse fluxo de trabalho aprimorado facilita o gerenciamento de conteúdo reutilizado de acordo com seu calendário promocional e de comunicações. <a href="../content/fragments.md#fragment-status-and-lifecycle">Saiba mais</a> |
