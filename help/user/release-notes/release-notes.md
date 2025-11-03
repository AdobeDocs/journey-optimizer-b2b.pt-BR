---
title: Notas de versão do Journey Optimizer B2B Edition
description: Descubra os recursos, aprimoramentos e correções de erros mais recentes no Adobe Journey Optimizer B2B edition. Mantenha-se atualizado com novos recursos e melhorias de produtos.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 7b36124cf830b5cdb980a1288d3870843a10fed2
workflow-type: tm+mt
source-wordcount: '3522'
ht-degree: 85%

---

# Notas de versão do Journey Optimizer B2B Edition

O Adobe Journey Optimizer B2B Edition está sempre fornecendo novos recursos, melhorias para recursos existentes e correções de erros. 

O Journey Optimizer B2B Edition é integrado nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest?lang=pt-BR){target="_blank"}.

Consulte a [descrição do produto](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} para obter informações sobre direitos, proteções de desempenho e limitações.

## Notas da versão 2025.10

**Data de implantação**: sábado, 31 de outubro de 2025

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Modelo de dados relacional | Aproveite os dados relacionais vinculados às Contas B2B para filtrar contas em uma jornada de conta ou personalizar conteúdo de email. Esses dados relacionais podem representar entidades comerciais reais, como registros de compra, registros de evento, licenças de software, assinaturas de serviço ou reservas. |
| Recurso | Ativar para destino do jornada | Use a nova ação de conta da empresa _Ativar para destino_ para ativar diretamente para empresas, em vez de pessoas físicas. (Limitado a empresas do LinkedIn para esta versão.) |
| Recurso | Ativação múltipla do Marketo Engage | Configure conexões com instâncias remotas do Marketo Engage e use essas conexões para definir ações do Marketo Engage no jornada. Essas ações, como adicionar/remover pessoas de listas ou adicionar pessoas a uma campanha de solicitação, se aplicam à instância designada do Marketo Engage. |
| Recurso | Temas da marca | Com temas de marca, os usuários não técnicos agora têm a capacidade de criar conteúdo reutilizável que se adapta a uma marca específica e a um idioma de design, adicionando estilo personalizado sobre os modelos padrão. [Saiba mais](../content/brand-themes.md) |
| Recurso | Modelos de email - converter imagem para o HTML | Agora você pode usar seus arquivos de design armazenados como arquivos de imagem JPG ou PNG e gerar automaticamente modelos de email. [Saiba mais](../content/email-template-image-convert.md) |
| Recurso | Mapeamento de personas | Vincular membros da conta a perfis estabelecidos com mapeamento de atributo. [Saiba mais](../admin/persona-mapping.md) |
| Recurso | Insights de vendas para o Salesforce e o Dynamics | Os membros da equipe de vendas agora podem visualizar grupos de compras em vencimento e insights relacionados em uma integração do Salesforce ou do Dynamics para identificar novas oportunidades. Os detalhes do grupo de compras como estágio, pontuação e membros relacionados estão incluídos. |
| Aprimoramento | Desduplicação de fadiga de email | Agora é possível ativar a desduplicação de email para garantir que o mesmo email não seja enviado várias vezes para o mesmo endereço em uma jornada. Endereços duplicados são bloqueados até que o primeiro registro com esse endereço de email conclua a jornada. |
| Aprimoramento | Limites de comunicação | O sistema agora respeita os limites de comunicação combinados do Marketo Engage e do Journey Optimizer B2B edition. |
| Aprimoramento | Comprando trabalhos de manutenção de grupo | A frequência do trabalho de manutenção do grupo de compras é atualizada de semanal para diário. |
| Aprimoramento | Progressão da jornada de conta | Um link _Mais informações_ está visível para a progressão da jornada para acessar contagens e listas de contas. |

Os seguintes recursos de IA de agente estão disponíveis para o Journey Optimizer B2B edition na interface do Assistente de IA:

| Agente | Atualização | Descrição |
| ----- | ------ | ----------- |
| Account Qualification Agent | Novo | Veja quais contas estão prontas para a próxima etapa usando o Account Qualification Agent no Assistente de IA. Esse agente permite que os membros da equipe de vendas se concentrem nas contas certas, identificando clientes potenciais de alto valor e automatizando os fluxos de trabalho de qualificação. [Saiba mais](../agents/account-qualification-agent.md) |

>[!NOTE]
>
>As alterações de versão começam a ser implantadas em sábado, 31 de outubro de 2025, com uma implantação em fases de cada recurso. As datas de lançamento dos recursos e aprimoramentos estão sujeitas a alterações.

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Notas da versão 2025.9

**Data de implantação**: 30 de setembro de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Colaboração de conteúdo de email | Agora é possível comentar sobre a colaboração com outros usuários do Journey Optimizer B2B Edition no contexto de um ativo de email. É possível marcar os membros da equipe para que recebam uma notificação por email com os detalhes do comentário. A notificação também está disponível como uma notificação de pulso. [Saiba mais](../content/email-collaboration-tools.md) |
| Recurso | Modo escuro para design de email | O espaço de design de email agora inclui a capacidade de alternar para o _modo escuro_. No modo escuro, é possível visualizar o conteúdo do email e definir configurações personalizadas a serem exibidas especificamente para destinatários que visualizam seus emails no modo escuro. [Saiba mais](../content/email-dark-mode.md) |
| Aprimoramento | Jornadas: dividir caminho pelo número de pessoas na função | Use um caminho dividido pelo nó da conta para direcionar uma conta com o número de pessoas em uma ou mais funções de grupo de compra. No caminho, você pode avaliar a prontidão do grupo de compras com respeito a alertas de vendas e outras interações com base na profundidade da função. [Saiba mais](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| Aprimoramento | Jornadas: filtros de pessoa para eventos | Use filtros de pessoas para acompanhar eventos de pessoas. Esses filtros incluem a capacidade de direcionar uma função específica para um grupo de compra correspondente. [Saiba mais](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

Os seguintes recursos de IA de agente estão disponíveis para o Journey Optimizer B2B edition na interface do Assistente de IA:

| Agente | Atualização | Descrição |
| ----- | ------ | ----------- |
| Agente de construção de jornada | Novo | O Agente de build de Jornada analisa, idealiza e cria jornadas em tempo real, permitindo que os profissionais de marketing iniciem mais rapidamente, melhorem o engajamento e impulsionem taxas de conversão mais altas. [Saiba mais](../agents/journey-agent.md) |
| Audience Agent | Novo | O Audience Agent identifica e cria grupos de compras automaticamente usando dados estruturados e não estruturados. Ele ajuda os profissionais de marketing a direcionar as pessoas certas de forma mais rápida e precisa. [Saiba mais](../agents/audience-agent-b2b.md) |

>[!NOTE]
>
>As alterações de versão começam a ser implantadas em 30 de setembro de 2025, com uma implantação em fases de cada recurso. As datas de lançamento dos recursos e aprimoramentos estão sujeitas a alterações.

## Notas da versão 2025.8

**Data de implantação**: 26 de agosto de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Filtros de pontuação de engajamento da pessoa para modelos de funções e jornadas | Agora é possível usar a _Pontuação de engajamento da pessoa_ como filtro nos modelos de funções utilizados para criar grupos de compra e nos nós de jornada de caminho dividido. [Saiba mais](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| Recurso | Configuração de funções personalizadas para grupos de compra | Agora você tem a flexibilidade de configurar funções personalizadas para grupos de compra, o que permite definir as funções específicas para os casos de uso. [Saiba mais](../buying-groups/default-custom-roles.md) |
| Recurso | Configuração do peso da pontuação de engajamento | Agora é possível atribuir pesos às atividades que influenciam a pontuação de engajamento do grupo de compra. Esse recurso inclui definir seus próprios modelos de pontuação personalizados e alterar o modelo ativo que influencia os cálculos da pontuação de engajamento. [Saiba mais](../admin/engagement-score-weighting.md) |
| Aprimoramento | Conteúdo condicional para fragmentos | Agora é possível usar as ferramentas de conteúdo condicional para o design de fragmentos visuais. [Saiba mais](../content/conditional-content.md) |
| Aprimoramento | Atualizações da pontuação de engajamento | A lógica da pontuação de engajamento do grupo de compra é atualizada para normalizar as pontuações. Além disso, é possível trabalhar com pontuações de engajamento no nível dos membros, bem como pontuações de engajamento coletivo para todo o grupo de compra. [Saiba mais](../buying-groups/engagement-scores.md) |
| Aprimoramento | Observabilidade da jornada ativa: contas em cada nó | Para uma jornada de conta ativa, é possível acessar uma lista das contas que atingiram cada nó de conta na jornada. |

## Notas da versão 2025.6

**Data de implantação**: 15 de julho de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Integração com o GenStudio for Performance Marketing | (Disponibilidade limitada) Agora é possível integrar as experiências de email do GenStudio for Performance Marketing com o Journey Optimizer B2B Edition para melhorar a eficiência do marketing e manter a consistência da marca. Com essa integração, é possível combinar a criação de conteúdo viabilizada por IA do GenStudio com os recursos avançados de orquestração do Journey Optimizer B2B Edition. [Saiba mais](../content/genstudio-email-workflow.md) |
| Recurso | Relatórios de detecção de spam | Para evitar filtros de spam e garantir que as mensagens sejam entregues nas caixas de entrada do público-alvo, você pode gerar um _relatório de spam_ diretamente no espaço de design do email. [Saiba mais](../content/email-spam-report.md) |
| Recurso | Página de detalhes da pessoa | Agora você pode clicar no nome de uma pessoa quando ele for exibido (como um hiperlink) no Painel inteligente, na página de detalhes do grupo de compra e na página de detalhes da conta. Essa ação abre a página de detalhes da pessoa associada, que contém informações de contato, sua atividade e grupos de compras mais engajados. [Saiba mais](../accounts/person-details.md) |
| Recurso | Ações de conta e grupo de compra | Realize ações diretamente nas páginas de detalhes da conta e detalhes do grupo de compra para um engajamento oportuno e intencional. <li>Use a ação _Enviar email_ para enviar um email do Marketo Engage aprovado para contatos de conta ou membros do grupo de compra selecionados. [Saiba mais](../accounts/account-details.md#send-emails) <li>Nos detalhes do grupo de compra, as ações também incluem as opções _Atribuir um novo membro_, _Remover um membro_ e _Editar uma função_. [Saiba mais](../buying-groups/buying-group-details.md#members-tab) |
| Recurso | Acesso no CRM às páginas de detalhes | Agora é possível configurar links diretos para as páginas de detalhes do Journey Optimizer B2B Edition para contas, contatos e leads em sua ferramenta de Gerenciamento de Relacionamento com o Cliente (CRM), como Salesforce ou Microsoft Dynamics. [Saiba mais](../accounts/crm-linking.md) |
| Recurso | Suporte a CSS personalizado para design de conteúdo | Agora é possível adicionar seu próprio CSS personalizado ao criar conteúdo de emails e de páginas de destino no espaço de design. [Saiba mais](../content/design-custom-css.md) |
| Recurso | Configuração de mapeamento de palavra-chave de intenção | Para ativar e gerenciar o modelo de detecção de intenção, agora é possível fazer upload de uma planilha para definir uma categoria de mapeamento de dados de intenção. [Saiba mais](../admin/intent-data.md) |
| Aprimoramento | Simular conteúdo do resumo de email | Agora você pode acessar as ferramentas _Simular conteúdo_ do resumo de email (detalhes e propriedades) ao abrir um email na lista Emails. Esse acesso é uma adição ao espaço de design de email. [Saiba mais](../content/email-simulate-content.md#display-the-email-preview) |
| Aprimoramento | Exibição da contagem total da lista de modelos de funções | A página da lista _[!UICONTROL Modelos de funções]_ é aprimorada com a exibição da contagem total ao lado da barra de pesquisa. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Notas da versão 2025.5

**Data de implantação**: 3 de junho de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Testes de email com o Litmus | Com uma [conta Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, agora você pode visualizar o e-mail rendering em clientes de email populares do Journey Optimizer B2B Edition. Essa integração ajuda a garantir que o conteúdo do seu email tenha uma ótima aparência e funcione conforme planejado em todas as caixas de entrada de email. [Saiba mais](../content/email-test-rendering.md) |
| Aprimoramento | Duplicar email | Ao adicionar um email relacionado a um nó da jornada, agora é possível duplicar um email existente. Modifique a configuração ou o conteúdo do email duplicado, ou deixe-o intacto.  [Saiba mais](../content/add-email.md#add-an-email-to-your-journey) |
| Aprimoramento | Formato de token handlebar para email | Os tokens de personalização para conteúdo de email agora usam um formato atualizado que é totalmente compatível com os scripts handlebar. Este formato usa _camel case_ ou sublinhados, eliminando espaços. [Saiba mais](../content/email-authoring.md#content-authoring---personalization) |
| Aprimoramento | Exibição da contagem total de listas | As páginas de lista _[!UICONTROL Interesses da solução]_ e _[!UICONTROL Jornadas da conta]_ foram aprimoradas com a exibição da contagem total ao lado da barra de pesquisa. |

## Notas da versão 2025.4

**Data de implantação**: 29 de abril de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Listas de contas | Agora você pode criar uma lista de contas estáticas ou dinâmicas para segmentar contas nomeadas de acordo com seus critérios definidos, como setor, localização ou tamanho da empresa. <a href="../accounts/account-lists.md">Saiba mais</a> |
| Recurso | Orquestração de jornada da lista de contas | Use os nós de ação de jornada para adicionar e remover contas de listas de contas estáticas. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Saiba mais</a> |
| Aprimoramento | Filtrar associação de jornada no Marketo Engage | Use as listas de contas do Adobe Journey Optimizer B2B Edition para o público-alvo da jornada e, em seguida, use o filtro _Membro de uma lista de contas_ nas listas inteligentes do Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Saiba mais</a> |
| Recurso | Filtros de inatividade | Orquestre jornadas com base na inatividade em campanhas e programas do Marketo Engage, incluindo inatividade de email, momentos interessantes, alterações no valor de dados e páginas da Web visitadas. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Saiba mais</a> |
| Aprimoramento | Filtro de página da Web visitada | Orquestre jornadas com base na atividade de páginas da web visitadas associadas a campanhas e programas do Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-filters">Saiba mais</a> |
| Aprimoramento | Lista de emails | Exiba uma lista global de emails ativos e de rascunho para pesquisá-los, analisá-los e atualizá-los nas jornadas de conta associadas. <a href="../content/emails-list.md">Saiba mais</a> |

## Notas da versão 2025.3

**Data de implantação**: 1º de abril de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Duplicar jornadas de conta | Uma ação duplicada agora está disponível para jornadas de conta. Você pode duplicar os detalhes da jornada da conta ou apenas um esqueleto simples do fluxo e da estrutura do caminho. <a href="../journeys/journey-overview.md#duplicate-journey">Saiba mais</a> |
| Recurso | Meus tokens para jornadas de conta | Agora você pode definir um conjunto de tokens personalizados com valores específicos para a jornada da conta. Este conjunto de tokens personalizados é chamado de _Meus tokens_, e qualquer um desses tokens personalizados serve para personalização ao criar emails de jornada. <a href="../content/personalization-my-tokens.md">Saiba mais</a> |
| Recurso | Excluir estágios do grupo de compra | Você pode excluir o modelo de estágios do grupo de compra quando ele estiver em estado de rascunho ou publicado. Se for publicado (ao vivo), você poderá excluí-lo somente quando não estiver associado a um interesse de solução. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Saiba mais</a> |
| Aprimoramento | Contagens de nós de jornada | Visibilidade aprimorada nas contagens de membros de jornadas publicadas no nível do nó. No _Mapa de jornada_, os nós exibem o _[!UICONTROL Total de contas inseridas]_. Ao selecionar um nó de ação, os detalhes à direita também incluem _[!UICONTROL Contas ainda não acionadas]_. Os detalhes de nós _Monitorar um evento_ incluem _[!UICONTROL Contas nesta etapa]_. Use essas informações para validar o progresso da conta nas jornadas ativas, concluídas e canceladas. |

## Notas da versão 2025.2

**Data de implantação**: 11 de março de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Campos personalizáveis: fragmentos de conteúdo | Durante o design do fragmento visual, é possível designar parâmetros de um componente no fragmento como editáveis. Esse recurso permite que o autor do email ou modelo especifique um valor de campo personalizado específico para suas necessidades. Esse sinalizador de personalização é limitado aos componentes visuais de imagem, texto e botão. <a href="../content/fragment-authoring.md#enable-fragment-customization">Saiba mais</a> |
| Recurso | Tipos de duplicação de jornada | Ao duplicar uma jornada de conta, você pode incluir detalhes do nó, excluindo emails e mensagens SMS criados no Journey Optimizer B2B Edition. Como alternativa, você pode criar uma cópia da estrutura e dos fluxos de caminho, sem detalhes e configurações do nó. <a href="../journeys/journey-overview.md#duplicate-journey">Saiba mais</a> |
| Aprimoramento | Quatro modelos de email de exemplo adicionais | A biblioteca de modelos de email agora inclui quatro modelos do SecurFinancial como exemplos de conteúdo de reengajamento, informação, estímulo e feedback |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Notas da versão 2025.1 {#Jan-2025}

**Data de implantação**: 6 de fevereiro de 2025

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Encaminhamento de eventos de experiência | Admins podem configurar definições de evento baseadas na Adobe Experience Platform (AEP). Essas configurações permitem que profissionais de marketing criem jornadas de conta que reagem aos eventos de experiência da AEP.  <a href="../admin/configure-aep-events.md">Saiba mais</a> |
| Recurso | Destinos de mídia paga | Qualifique pessoas conhecidas para campanhas de mídia paga de uma jornada de conta para que você possa engajá-las em plataformas de publicidade, como o LinkedIn. Use um nó de divisão de caminho para segmentar públicos-alvo da conta com base em comportamentos específicos e identificar contas que exigem engajamento adicional. Em seguida, adicione pessoas dessas contas a um público-alvo de clientes externo por meio da Real-time CDP para um destino de mídia paga compatível. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Saiba mais</a> |
| Recurso | Painel inteligente | Visualize a progressão dos grupos de compra por meio das jornadas de conta, incluindo insights gerados por IA, a fim de obter análises mais inteligentes e uma priorização precisa da conta. <a href="../dashboards/intelligent-dashboard.md">Saiba mais</a> |
| Recurso | Detalhes do grupo de compra e da conta | Visualize insights no grupo de compra e no nível da conta para ter mais dados históricos e de contexto ao iniciar o engajamento de um cliente.<p>Os detalhes do grupo de compra incluem qualquer intenção própria detectada. <a href="../buying-groups/buying-group-details.md">Saiba mais</a><p>Os detalhes da conta destacam o aumento na intenção de engajamento detectada para que você possa alertar sobre as vendas em contas que estão prontas para o engajamento personalizado com foco em vendas. <a href="../accounts/account-details.md">Saiba mais</a> |
| Recurso | Visão geral da jornada | Ao acessar as jornadas de conta, a guia Visão geral fornece um instantâneo abrangente das jornadas de conta ativas, detalhando o progresso da conta usando gráficos de círculo e de barra que categorizam e quantificam conclusões e atividades de engajamento.  <a href="../dashboards/journeys-dashboard.md">Saiba mais</a> |
| Recurso | Edição de imagens do Adobe Express | As ações rápidas do Adobe Express permitem fazer edições simples (como cortar e redimensionar) em imagens para obter uma aparência mais refinada para o conteúdo. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Saiba mais</a>  <p>Para obter um conjunto mais abrangente de ferramentas de design, essa integração habilita uma licença completa do Adobe Express no Journey Optimizer B2B Edition. Com essa configuração, a interface completa do Adobe Express fica acessível no espaço de trabalho de ativos local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Saiba mais</a> |
| Recurso | Filtros de intenção para funções de grupo de compra | Quando você envia as palavras-chave de intenção, o modelo de Detecção de intenção prevê uma solução/produto de interesse de alta confiança com base na atividade de um lead. <a href="../admin/intent-data.md">Saiba mais</a> <p>Estes dados de intenção estão disponíveis para definir as condições de função do grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Suporte a eventos do Marketo Engage nas jornadas | O nó de jornada _Acompanhar evento_ agora oferece suporte a dois eventos do Marketo Engage no nível de pessoas: _Visita a página da web_ e _Preenche o formulário_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Saiba mais</a> |
| Aprimoramento | Filtros de grupo de compra para listas inteligentes do Marketo Engage | Visualize e crie listas inteligentes com filtros de grupo de compra no Marketo Engage. Esses filtros adicionados permitem retirar e incluir membros do grupo de compra em campanhas e programas do Marketo Engage de jornadas de conta no Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Saiba mais</a> |
| Aprimoramento | Filtro de associação à lista do Marketo Engage para jornadas e funções | No Journey Optimizer B2B, verifique sobre a condição de associação à lista do Marketo Engage para um nó _de divisão de caminho por pessoas_ para ajudar a eliminar a duplicação em atividades de jornada. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a> <p> Para modelos de funções de grupo de compra, use a associação à lista como uma condição de função. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a> |
| Aprimoramento | Painel de visão geral do engajamento | Esse painel foi atualizado para fornecer uma visão abrangente do engajamento. Ele mostra métricas de conta e interações individuais em tempo real por meio de instantâneos de gráficos de círculo e gráficos de linha que revelam tendências ao longo do tempo. <a href="../dashboards/engagement-dashboard.md">Saiba mais</a> |

## Versões de 2024

Expanda as listas a seguir para obter os recursos e aprimoramentos do Journey Optimizer B2B Edition lançados em 2024.

+++Notas de versão de outubro de 2024

**Data de implantação**: 29 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Conteúdo condicional em emails | Personalize o conteúdo do email com base nas características comportamentais e de perfil do destinatário, tanto no nível da conta quanto no nível de lead. <p>Ao criar um email para a jornada de conta no espaço de design visual de email, use regras condicionais para definir múltiplas variantes para qualquer componente de conteúdo. <a href="../content/conditional-content.md">Saiba mais</a> |
| Recurso | Ações de pessoa _Adicionar à lista_ e _Remover da lista_ nas jornadas | Personalize o conteúdo do email com base nas características comportamentais e de perfil do destinatário, tanto no nível da conta quanto no nível de lead. <a href="../journeys/action-nodes.md">Saiba mais</a> |
| Recurso | Governança de conteúdo e bloqueio de componentes | Para garantir a adesão aos designs de conteúdo aprovados, use os recursos de governança de conteúdo para bloquear componentes de conteúdo do modelo de email. Com a governança de conteúdo ativada no modelo de email, profissionais de marketing podem alterar apenas os elementos permitidos para mantê-lo alinhado à estratégia de conteúdo. <a href="../content/template-content-governance.md">Saiba mais</a> |
| Recurso | Estágios do grupo de compra | Ao definir e publicar um modelo de preparo de grupos de compra personalizado, é possível acompanhar a progressão do grupo de compra nos estágios do seu ciclo de vida. Use esses estágios para identificar as melhores ações para membros do grupo de compra. É possível configurar as regras de transição e os nós de jornada que determinam a progressão do estágio e acionam as ações com base em alterações. <a href="../buying-groups/buying-group-stages.md">Saiba mais</a> |
| Aprimoramento | Novos modelos de email prontos para uso | A biblioteca de modelos de exemplo agora inclui modelos de email adicionais criados para profissionais de marketing B2B. Use esses modelos de exemplo como ponto de partida e adicione sua própria identidade visual e mensagens. <a href="../content/email-templates.md#select-a-design-template">Saiba mais</a> |
| Aprimoramento | Campos personalizados como atributos de pessoa | Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta na Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa nas condições. Use esses atributos personalizados em: <li>Modelos de funções <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Saiba mais</a></li><li>Divisão de caminhos por nós de jornada de pessoas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Saiba mais</a></li> |
| Aprimoramento | Configurações do canal de email | As configurações de email agora estão visíveis na interface do Journey Optimizer B2B Edition. É possível revisar rapidamente as configurações atuais, e admins podem clicar em _[!UICONTROL Editar configurações]_ para acessar diretamente as configurações do Marketo Engage e atualizá-las de acordo com os requisitos da organização. <a href="../admin/configure-channels-emails.md">Saiba mais</a> |

+++

+++Notas de versão de setembro de 2024

**Data de implantação**: 7 de outubro de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Aprimoramento | Biblioteca central de ativos | A _biblioteca central de ativos_ aprimorada permite usar todos os ativos de imagem da instância do Marketo Engage nos espaços de trabalho do Design Studio. Algumas medidas de proteção integradas impedem a edição dos ativos do Marketo Engage no Journey Optimizer B2B Edition, bem como as operações de exclusão e movimentação. Essas proteções garantem que os ativos de origem (Marketo Engage Design Studio) sejam mantidos enquanto permitem a leitura e reutilização contínuas no Journey Optimizer B2B Edition.<p>Para ativos de uso exclusivo no Journey Optimizer B2B Edition, há um espaço de trabalho específico que fornece funções completas de gerenciamento de ativos. <a href="../content/marketo-engage-design-studio.md">Saiba mais</a> |
| Recurso | Ativos acessados recentemente | A página inicial no aplicativo Journey Optimizer B2B Edition agora inclui a seção _[!UICONTROL Acessados recentemente]_, que fornece uma lista dos ativos acessados mais recentemente para profissionais de marketing ou admins. Você pode usar essa lista e acessar diretamente o ativo no qual trabalhou recentemente sem ter que navegar por uma série de páginas de ativos e realizar pesquisas. <p>A lista fornece informações adicionais sobre a modificação para que você possa tomar a decisão sobre quais dos ativos precisam de modificações adicionais desde a última sessão. Para ativos de email, ela exibe a jornada da conta onde o ativo de email é usado. <a href="../home-page.md">Saiba mais</a> |
| Aprimoramento | Nó de divisão de jornada: reordenar caminhos | Em nós de divisão de caminho, a filtragem de caminho é avaliada de cima para baixo. Cada pessoa ou conta continua pelo primeiro caminho que corresponder. É possível reordenar os caminhos definidos clicando nas setas para cima e para baixo na parte superior direita de cada cartão de caminho, para movê-lo para cima ou para baixo na lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Saiba mais</a> |
| Aprimoramento | Nó de divisão de jornada: atributos adicionais de condição do histórico de atividades | Ao usar condições para definir a filtragem de caminho de um nó de divisão por pessoas, há dois atributos adicionais: _Email aberto_ e _Email entregue_. Essas adições fornecem maior flexibilidade para filtrar pessoas na jornada com base na atividade de email. <a href="../journeys/journey-nodes.md#split-paths">Saiba mais</a> |

+++

+++Notas de versão de agosto de 2024

**Data de implantação**: 29 de agosto de 2024

Esta versão inclui os seguintes novos recursos e melhorias:

| Tipo | Item | Descrição |
| ---- | ---- | ----------- |
| Recurso | Públicos-alvo correspondentes da conta do LinkedIn | Gere públicos-alvo de anúncios do LinkedIn por meio de públicos-alvo de conta correspondentes para ajudar a preencher funções vazias em seus grupos de compra. Ao definir um conjunto de filtros de grupo de compra, você pode manter um público-alvo correspondente do LinkedIn para direcionar clientes potenciais que correspondem aos parâmetros do grupo de compra. <p>Esse recurso utiliza os destinos da Experience Platform para gerenciar alguns aspectos da integração. <a href="../data/linkedin-account-matched-audiences.md">Saiba mais</a> |
| Aprimoramento | Ciclo de vida do status para fragmentos de conteúdo visual | Os fragmentos visuais agora são gerenciados usando um ciclo de vida de status. O status do fragmento determina sua disponibilidade para uso em um email ou modelo de email e as alterações que você pode fazer nele. <p>Esse fluxo de trabalho aprimorado facilita o gerenciamento de conteúdo reutilizado de acordo com o calendário promocional e de comunicações. <a href="../content/fragments.md#fragment-status-and-lifecycle">Saiba mais</a> |

+++
