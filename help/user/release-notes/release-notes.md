---
title: Notas de versão
description: Notas de versão mais recentes do Adobe Journey Optimizer B2B Edition
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 775cecb2aa4e305ba9a80ba0655e5e854ddf69e2
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 86%

---

# Notas de versão do Journey Optimizer B2B Edition

O Adobe Journey Optimizer B2B Edition está sempre fornecendo novos recursos, melhorias para recursos existentes e correções de erros. 

O Journey Optimizer B2B Edition é integrado nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest?lang=pt-BR){target="_blank"}.

Revise a [descrição do produto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=pt-BR){target="_blank"} para obter informações sobre direitos, medidas de proteção de desempenho e limitações.

## Notas da versão 2025.3

**Data de lançamento**: quarta-feira, 1 de abril de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Listas de contas | Agora é possível criar uma lista de contas estática ou dinâmica para direcionar contas nomeadas de acordo com seus critérios definidos, como setor, local ou tamanho da empresa. <a href="../accounts/account-lists.md">Saiba mais</a> |
| Novo recurso | Meus tokens para jornadas de conta | Agora é possível definir um conjunto de tokens personalizados com valores específicos para a jornada da conta. Este conjunto de tokens personalizados é chamado de _Meus tokens_, e qualquer um desses tokens personalizados serve para personalização ao criar emails de jornada. <a href="../content/personalization-my-tokens.md">Saiba mais</a> |
| Novo recurso | Excluir estágios de grupo de compra | Você pode excluir o modelo de estágios de grupo de compras quando está em um estado de rascunho ou publicado. Se for publicado (em tempo real), você poderá excluí-lo somente quando não estiver associado a um interesse de solução. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Saiba mais</a> |
| Aprimoramento | Jornada contagens de nós | Melhoria na visibilidade das contagens de associação de jornada publicadas no nível do nó. No _mapa de Jornadas_, os nós exibem _[!UICONTROL Total de contas inseridas]_. Quando você seleciona um nó de ação, os detalhes à direita também incluem _[!UICONTROL Contas ainda não ativadas]_. Os detalhes de _Ouvir um evento_ incluem _[!UICONTROL Contas nesta etapa]_. Use essas informações para validar o progresso da conta nas jornadas ativas, concluídas e abortadas. |

## Notas da versão 2025.2

**Data de lançamento**: 11 de março de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Campos personalizáveis: fragmentos de conteúdo | Como designer do fragmento de conteúdo, você pode designar um parâmetro editável para um componente no fragmento. Isso permite que o autor do email ou modelo determine um valor de campo personalizado específico para suas necessidades. Esse sinalizador de personalização é limitado aos componentes visuais de imagem, texto e botão. <a href="../content/fragment-authoring.md#enable-fragment-customization">Saiba mais</a> |
| Novo recurso | Funções integradas e permissões de produto da versão B2B | A Experience Platform agora inclui um conjunto de funções integradas (padrão) que você pode usar para gerenciar o acesso aos recursos do produto B2B. <a href="../admin/user-management.md#b2b-built-in-roles">Saiba mais</a> <br/>Admins agora podem definir funções personalizadas na Adobe Experience Platform para incluir permissões de produto do Journey Optimizer B2B Edition.  <a href="../admin/user-management.md#b2b-product-permissions">Saiba mais</a> |
| Novo recurso | Jornada tipos de duplicação | Ao duplicar uma jornada de conta, você pode incluir detalhes do nó, excluindo emails e mensagens SMS criadas no Journey Optimizer B2B edition. Como alternativa, é possível criar uma cópia estrutural da estrutura e dos fluxos de caminho, sem detalhes e configurações de nó. <a href="../journeys/journey-overview.md#duplicate-journey">Saiba mais</a> |
| Aprimoramento | Quatro modelos de email de exemplo adicionais | A biblioteca de modelos de email agora inclui quatro modelos do SecurFinancial como exemplos de conteúdo de reengajamento, informação, estímulo e feedback |

## Notas da versão 2025.1 {#Jan-2025}

**Data de lançamento**: 6 de fevereiro de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Encaminhamento de eventos de experiência | Admins podem configurar definições de evento baseadas na Adobe Experience Platform (AEP). Essas configurações permitem que profissionais de marketing criem jornadas de conta que reagem aos eventos de experiência da AEP.  <a href="../admin/configure-aep-events.md">Saiba mais</a> |
| Novo recurso | Destinos de mídia paga | Qualifique pessoas conhecidas para campanhas de mídia paga de uma jornada de conta para que você possa engajá-las em plataformas de publicidade, como o LinkedIn. Use um nó de divisão de caminhos em uma jornada de conta para segmentar públicos-alvo de conta com base em comportamentos específicos e identificar contas que exigem engajamento adicional. Em seguida, adicione pessoas dessas contas a um público-alvo de clientes externo por meio da Real-time CDP para um destino de mídia paga compatível. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Saiba mais</a> |
| Novo recurso | Painel inteligente | Visualize a progressão dos grupos de compra por meio das jornadas de conta, incluindo insights gerados por IA, a fim de obter análises mais inteligentes e uma priorização precisa da conta. <a href="../dashboards/intelligent-dashboard.md">Saiba mais</a> |
| Novo recurso | Detalhes do grupo de compra e da conta | Visualize insights no grupo de compra e no nível da conta para ter mais dados históricos e de contexto ao iniciar o engajamento de um cliente.<p>Os detalhes do grupo de compra incluem qualquer intenção própria detectada. <a href="../buying-groups/buying-group-details.md">Saiba mais</a><p>Os detalhes da conta destacam o aumento na intenção de engajamento detectada para que você possa alertar sobre as vendas em contas que estão prontas para o engajamento personalizado com foco em vendas. <a href="../accounts/account-details.md">Saiba mais</a> |
| Novo recurso | Visão geral da jornada | Ao acessar as jornadas de conta, a guia Visão geral fornece um instantâneo abrangente das jornadas de conta ativas, detalhando o progresso da conta usando gráficos de círculo e de barra que categorizam e quantificam conclusões e atividades de engajamento.  <a href="../dashboards/journeys-dashboard.md">Saiba mais</a> |
| Novo recurso | Edição de imagens do Adobe Express | As ações rápidas do Adobe Express permitem fazer edições simples (como cortar e redimensionar) em imagens para obter uma aparência mais refinada para o conteúdo. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Saiba mais</a>  <p>Para obter um conjunto mais abrangente de ferramentas de design, essa integração habilita uma licença completa do Adobe Express no Journey Optimizer B2B Edition. Com essa configuração, a interface completa do Adobe Express fica acessível no espaço de trabalho de ativos local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Saiba mais</a> |
| Novo recurso | Filtros de intenção para funções de grupo de compra | Quando você envia as palavras-chave de intenção, o modelo de Detecção de intenção prevê uma solução/produto de interesse de alta confiança com base na atividade de um lead. <a href="../admin/intent-data.md">Saiba mais</a> <p>Estes dados de intenção estão disponíveis para definir as condições de função do grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Suporte a eventos do Marketo Engage nas jornadas | O nó de jornada _Acompanhar evento_ agora oferece suporte a dois eventos do Marketo Engage no nível de pessoas: _Visita a página da web_ e _Preenche o formulário_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Saiba mais</a> |
| Aprimoramento | Filtros de grupo de compra para listas inteligentes do Marketo Engage | Visualize e crie listas inteligentes com filtros de grupo de compra no Marketo Engage. Esses filtros adicionados permitem retirar e incluir membros do grupo de compra em campanhas e programas do Marketo Engage de jornadas de conta no Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Saiba mais</a> |
| Aprimoramento | Filtro de associação à lista do Marketo Engage para jornadas e funções | No Journey Optimizer B2B, verifique sobre a condição de associação à lista do Marketo Engage para um nó _de divisão de caminho por pessoas_ para ajudar a eliminar a duplicação em atividades de jornada. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a> <p> Para modelos de funções de grupo de compra, use a associação à lista como uma condição de função. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Painel de visão geral do engajamento | Esse painel foi atualizado para fornecer uma visão abrangente do engajamento. Ele mostra métricas de conta e interações individuais em tempo real por meio de instantâneos de gráficos de círculo e gráficos de linha que revelam tendências ao longo do tempo. <a href="../dashboards/engagement-dashboard.md">Saiba mais</a> |


## Notas de versão de outubro de 2024 {#Oct-2024}

**Data de lançamento**: 29 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Conteúdo condicional em modelos de email | Personalize o conteúdo do email com base nas características comportamentais e de perfil do destinatário, tanto no nível da conta quanto no nível de lead. <p>Ao criar um email para a jornada de conta no espaço de design visual de email, use regras condicionais para definir múltiplas variantes para qualquer componente de conteúdo. <a href="../content/conditional-content.md">Saiba mais</a> |
| Novo recurso | Ações de pessoa _Adicionar à lista_ e _Remover da lista_ nas jornadas | Personalize o conteúdo do email com base nas características comportamentais e de perfil do destinatário, tanto no nível da conta quanto no nível de lead. <a href="../journeys/action-nodes.md">Saiba mais</a> |
| Novo recurso | Governança de conteúdo e bloqueio de componentes | Para garantir a adesão aos designs de conteúdo aprovados, use os recursos de governança de conteúdo para bloquear componentes de conteúdo do modelo de email. Com a governança de conteúdo ativada no modelo de email, profissionais de marketing podem alterar apenas os elementos permitidos para mantê-lo alinhado à estratégia de conteúdo. <a href="../content/template-content-governance.md">Saiba mais</a> |
| Novo recurso | Estágios do grupo de compra | Ao definir e publicar um modelo de preparo de grupos de compra personalizado, é possível acompanhar a progressão do grupo de compra nos estágios do seu ciclo de vida. Use esses estágios para identificar as melhores ações para membros do grupo de compra. É possível configurar as regras de transição e os nós de jornada que determinam a progressão do estágio e acionam as ações com base em alterações. <a href="../buying-groups/buying-group-stages.md">Saiba mais</a> |
| Aprimoramento | Novos modelos de email prontos para uso | A biblioteca de modelos de exemplo agora inclui modelos de email adicionais criados para profissionais de marketing B2B. Use esses modelos de exemplo como ponto de partida e adicione sua própria identidade visual e mensagens. <a href="../content/email-templates.md#select-a-design-template">Saiba mais</a> |
| Aprimoramento | Campos personalizados como atributos de pessoa | Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta na Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa nas condições. Use esses atributos personalizados em: <li>Modelos de funções <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a></li><li>Divisão de caminhos por nós de jornada de pessoas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a></li> |
| Aprimoramento | Configurações do canal de email | As configurações de email agora estão visíveis na interface do Journey Optimizer B2B Edition. É possível revisar rapidamente as configurações atuais, e admins podem clicar em _[!UICONTROL Editar configurações]_ para acessar diretamente as configurações do Marketo Engage e atualizá-las de acordo com os requisitos da organização. <a href="../admin/configure-channels-emails.md">Saiba mais</a> |

## Notas de versão de setembro de 2024 {#Sept-2024}

**Data de lançamento**: 7 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Aprimoramento | Biblioteca central de ativos | A _biblioteca central de ativos_ aprimorada permite usar todos os ativos de imagem da instância do Marketo Engage nos espaços de trabalho do Design Studio. Algumas medidas de proteção integradas impedem a edição dos ativos do Marketo Engage no Journey Optimizer B2B Edition, bem como as operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos enquanto permitem a leitura e reutilização contínuas no Journey Optimizer B2B Edition.<p>Para ativos de uso exclusivo no Journey Optimizer B2B Edition, há um espaço de trabalho específico que fornece funções completas de gerenciamento de ativos. <a href="../content/marketo-engage-design-studio.md">Saiba mais</a> |
| Novo recurso | Ativos acessados recentemente | A página inicial no aplicativo Journey Optimizer B2B Edition agora inclui a seção _[!UICONTROL Acessados recentemente]_, que fornece uma lista dos ativos acessados mais recentemente para profissionais de marketing ou admins. Você pode usar essa lista e acessar diretamente o ativo no qual trabalhou recentemente sem ter que navegar por uma série de páginas de ativos e realizar pesquisas. <p>A lista fornece informações adicionais sobre a modificação para que você possa tomar a decisão sobre quais dos ativos precisam de modificações adicionais desde a última sessão. Para ativos de email, ela exibe a jornada da conta onde o ativo de email é usado. <a href="../home-page.md">Saiba mais</a> |
| Aprimoramento | Nó de divisão de jornada: reordenar caminhos | Em nós de divisão de caminho, a filtragem de caminho é avaliada de cima para baixo. Cada pessoa ou conta continua pelo primeiro caminho que corresponder. É possível reordenar os caminhos definidos clicando nas setas para cima e para baixo na parte superior direita de cada cartão de caminho, para movê-lo para cima ou para baixo na lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Saiba mais</a> |
| Aprimoramento | Nó de divisão de jornada: atributos adicionais de condição do histórico de atividades | Ao usar condições para definir a filtragem de caminho de um nó de divisão por pessoas, há dois atributos adicionais: _Email aberto_ e _Email entregue_. Essas adições fornecem maior flexibilidade para filtrar pessoas na jornada com base na atividade de email. <a href="../journeys/journey-nodes.md#split-paths">Saiba mais</a> |

## Notas de versão de agosto de 2024 {#Aug-2024}

**Data de lançamento**: 29 de agosto de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Novo recurso | Públicos-alvo correspondentes da conta do LinkedIn | Gere públicos-alvo de anúncios do LinkedIn por meio de públicos-alvo de conta correspondentes para ajudar a preencher funções vazias em seus grupos de compra. Ao definir um conjunto de filtros de grupo de compra, você pode manter um público-alvo correspondente do LinkedIn para direcionar clientes em potencial que correspondem aos parâmetros do grupo de compra. <p>Esse recurso utiliza os destinos da Experience Platform para gerenciar alguns aspectos da integração. <a href="../data/linkedin-account-matched-audiences.md">Saiba mais</a> |
| Aprimoramento | Ciclo de vida do status para fragmentos de conteúdo visual | Os fragmentos visuais agora são gerenciados usando um ciclo de vida de status. O status do fragmento determina sua disponibilidade para uso em um email ou modelo de email e as alterações que você pode fazer nele. <p>Esse fluxo de trabalho aprimorado facilita o gerenciamento de conteúdo reutilizado de acordo com o calendário promocional e de comunicações. <a href="../content/fragments.md#fragment-status-and-lifecycle">Saiba mais</a> |
