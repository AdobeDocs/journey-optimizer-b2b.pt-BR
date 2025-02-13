---
title: Notas de versão
description: Notas de versão mais recentes do Adobe Journey Optimizer edição B2B
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 24e39a532903ae2ca389f7c1a761ec7b5e03157d
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 10%

---

# Notas de versão do Journey Optimizer B2B edition

O Adobe Journey Optimizer B2B edition oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros.

O Journey Optimizer B2B edition é construído nativamente no [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest?lang=pt-BR){target="_blank"}.

Revise a [descrição do produto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} para obter informações sobre direitos, medidas de proteção de desempenho e limitações.

## Notas da versão de janeiro de 2025 {#Jan-2025}

**Data de lançamento**: 6 de fevereiro de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Encaminhamento de evento de experiência | Os administradores podem configurar definições de evento baseadas no Adobe Experience Platform (AEP). Essas configurações permitem que os profissionais de marketing criem jornadas de conta que reagem aos eventos de experiência da AEP.  <a href="../admin/configure-aep-events.md">Saiba mais</a> |
| Novo recurso | Destinos de mídia paga | Qualifique pessoas conhecidas para campanhas de mídia paga de uma jornada de conta para que você possa engajá-las em plataformas de publicidade, como o LinkedIn. Use um nó de caminhos divididos em uma jornada de conta para segmentar públicos da conta com base em um comportamento específico e identificar contas que exigem engajamento adicional. Em seguida, adicione pessoas dessas contas a um público-alvo de clientes externos por meio da Real-time CDP para um destino de mídia paga compatível. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Saiba mais</a> |
| Novo recurso | Painel inteligente | Visualize a progressão dos grupos de compras por meio de suas jornadas de conta, incluindo insights gerados por IA para análises mais inteligentes e priorização de conta precisa. <a href="../dashboards/intelligent-dashboard.md">Saiba mais</a> |
| Novo recurso | Detalhes do grupo de compras e da conta | Visualize insights no grupo de compras e no nível da conta para ter mais dados de contexto e histórico quando você começar a se envolver com um cliente.<p>Os detalhes do grupo de compras incluem qualquer intenção própria detectada. <a href="../buying-groups/buying-group-details.md">Saiba mais</a><p>As contas de detalhes da conta destacam o aumento da intenção de envolvimento detectada, para que você possa alertar as vendas sobre contas que estão prontas para o envolvimento focado em vendas personalizado.  <a href="../accounts/account-details.md">Saiba mais</a> |
| Novo recurso | Visão geral do Jornada | Ao acessar as jornadas da conta, a guia Visão geral fornece um instantâneo abrangente das jornadas da conta ativa, detalhando o progresso da conta usando gráficos de círculo e de barra que categorizam e quantificam conclusões e atividades de envolvimento.  <a href="../dashboards/journeys-dashboard.md">Saiba mais</a> |
| Novo recurso | edição de imagens do Adobe Express | As Ações rápidas do Adobe Express permitem fazer edições simples (como cortar e redimensionar) em imagens para obter uma aparência mais elegante no conteúdo. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Saiba mais</a>  <p>Para obter um conjunto mais abrangente de ferramentas de design, essa integração permite uma licença completa do Adobe Express no Journey Optimizer B2B edition. Com essa configuração, a interface completa do usuário do Adobe Express fica acessível no espaço de trabalho do ativo local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Saiba mais</a> |
| Novo recurso | Filtros de intenção para funções de grupos de compra | Quando você envia as palavras-chave de intenção, o modelo de Detecção de intenção prevê uma solução/produto de interesse com alta confiança suficiente com base na atividade de um lead. <a href="../admin/intent-data.md">Saiba mais</a> <p>Estes dados de intenção estão disponíveis para definir as condições de função do grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Suporte a eventos do Marketo Engage no jornada | O nó de jornada _Escutar Evento_ agora oferece suporte a dois eventos Marketo Engage no nível de pessoas: _Página da Web de Visitas_ e _Preenche o formulário_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Saiba mais</a> |
| Aprimoramento | Filtros de grupo de compra para listas inteligentes do Marketo Engage | Visualize e crie listas inteligentes com filtros de grupo de compra no Marketo Engage. Esses filtros adicionados permitem suprimir e incluir membros do grupo de compras em campanhas e programas do Marketo Engage de jornadas de conta no Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Saiba mais</a> |
| Aprimoramento | Filtro de associação de lista do Marketo Engage para jornadas e funções | No Journey Optimizer B2B, verifique a associação à lista do Marketo Engage como uma condição para um nó _split path by people_ para ajudar a eliminar a duplicação em atividades de jornada. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a> <p> Para modelos de funções de grupos de compras, use a associação de lista como uma condição de função. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Painel de visão geral do envolvimento | Esse painel é atualizado para fornecer uma visão abrangente do engajamento. Ele mostra métricas de conta e interações individuais em tempo real por meio de gráficos de círculo de instantâneos e gráficos de linha reveladores de tendências ao longo do tempo. <a href="../dashboards/engagement-dashboard.md">Saiba mais</a> |


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
| Aprimoramento | Biblioteca de ativos central | A _biblioteca central de ativos_ aprimorada permite usar todos os ativos de imagem na sua instância do Marketo Engage, em todos os espaços de trabalho do Design Studio. Existem medidas de proteção integradas que impedem a edição de ativos da Marketo Engage do Journey Optimizer B2B edition, bem como as operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos e, ao mesmo tempo, permitem leitura e reutilização perfeitas no Journey Optimizer B2B edition.<p>Para ativos exclusivos para uso no Journey Optimizer B2B edition, um espaço de trabalho específico fornece funções completas de gerenciamento de ativos. <a href="../content/marketo-engage-design-studio.md">Saiba mais</a> |
| Novo recurso | Ativos acessados recentemente | A página inicial no aplicativo Journey Optimizer B2B edition agora inclui a seção _[!UICONTROL Acessados recentemente]_, que fornece uma lista dos ativos acessados mais recentemente para o profissional de marketing ou administrador. Você pode usar essa lista para ir diretamente para o ativo no qual você trabalhou recentemente sem navegar por uma série de páginas de ativos e pesquisas. <p>A lista fornece informações adicionais sobre a modificação para que você possa tomar a decisão sobre quais dos ativos precisam de modificações adicionais da última sessão. Para ativos de email, ele exibe a jornada da conta onde o ativo de email é usado. <a href="../home-page.md">Saiba mais</a> |
| Aprimoramento | Nó dividido do Jornada - reordenar caminhos | Em nós de caminho dividido, a filtragem de caminho é avaliada em ordem decrescente. Cada pessoa ou conta continua pelo primeiro caminho que corresponde a. Você pode reordenar os caminhos definidos clicando nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Saiba mais</a> |
| Aprimoramento | Jornada nó dividido - Atributos de condição de histórico de atividades adicionais | Ao usar condições para definir a filtragem de caminho para um nó dividido por pessoas, há dois atributos adicionais: _Email aberto_ e _Email entregue_. Essas adições fornecem maior flexibilidade para filtrar pessoas no jornada com base na atividade de email. <a href="../journeys/journey-nodes.md#split-paths">Saiba mais</a> |

## Notas de versão de agosto de 2024 {#Aug-2024}

**Data de lançamento**: 29 de agosto de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Públicos correspondentes da conta do LinkedIn | Gere públicos-alvo de anúncio do LinkedIn por meio dos Públicos-alvo de conta correspondentes para ajudar a preencher funções vazias em seus grupos de compra. Ao definir um conjunto de filtros de grupo de compra, você pode manter um Público-alvo correspondente do LinkedIn para direcionar os prospetos que correspondem aos parâmetros do grupo de compra. <p>Esse recurso aproveita o Experience Platform Destinations para gerenciar alguns aspectos da integração. <a href="../data/linkedin-account-matched-audiences.md">Saiba mais</a> |
| Aprimoramento | Ciclo de vida do status para fragmentos de conteúdo visual | Os fragmentos visuais agora são gerenciados usando um ciclo de vida de status. O status do fragmento determina sua disponibilidade para uso em um email ou modelo de email e as alterações que você pode fazer nele. <p>Esse fluxo de trabalho aprimorado facilita o gerenciamento de conteúdo reutilizado de acordo com seu calendário promocional e de comunicações. <a href="../content/fragments.md#fragment-status-and-lifecycle">Saiba mais</a> |
