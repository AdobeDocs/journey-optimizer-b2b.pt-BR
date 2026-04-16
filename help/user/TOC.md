---
user-guide-title: Documentação do Journey Optimizer B2B Edition
user-guide-description: Saiba mais sobre o Adobe Journey Optimizer B2B Edition e como ele pode ser usado para orquestrar jornadas de contas e de grupos de compra por meio da IA generativa integrada e da automação líder do setor.
source-git-commit: bbdbf74b2fb0003b84ed4d7f84dce9aa3b796aea
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 94%

---


# Guia do usuário do Journey Optimizer B2B Edition {#user}

+ [Documentação do Adobe Journey Optimizer B2B Edition](guide-overview.md)
+ [Notas de versão](./release-notes/release-notes.md)
+ Introdução {#get-started}
   + [Visão geral do Journey Optimizer B2B Edition](about-journey-optimizer-b2b-edition.md)
   + Arquitetura simplificada {#simplified-architecture}
      + [Lista de verificação de configuração](./simplified-architecture.md)
      + [Namespaces e esquemas](./data/namespaces-schemas.md)
      + [Seleção de campo XDM](./admin/xdm-field-management.md)
      + [Eventos de experiência e campos](./admin/configure-aep-events.md)
      + [Domínios de marca](./start/branding-domains.md)
      + [Acompanhamento e entrega de email](./start/email-protocols.md)
      + [Configuração de email](./start/email-setup.md)
      + [Ações de jornada do Marketo Engage](./admin/marketo-actions-connect.md)
      + [Gerenciamento de usuários](./admin/user-management.md)
   + [Integração de usuários](./start/get-started.md)
   + [Logon e página inicial](home-page.md)
+ Assistente de IA {#ai-assistant}
   + [Visão geral](./ai-assistant/ai-assistant-overview.md)
   + [Habilitar o acesso ao Assistente de IA](./ai-assistant/enable-ai-assistant-access.md)
   + [Orientação para perguntas](./ai-assistant/question-guidance.md)
   + [Usar o Assistente de IA](./ai-assistant/use-ai-assistant.md)
   + [IA gerativa para conteúdo](./ai-assistant/generative-ai-content.md)
   + Agentes {#ai-agents}
      + [Audience Agent B2B](./agents/audience-agent-b2b.md)
      + [Journey Agent B2B](./agents/journey-agent.md)
      + [Qualificador de Vendas](./agents/sales-qualifier.md)
+ Gerenciamento de jornadas {#journeys}
   + [Jornadas de conta e pessoa](./journeys/journeys-overview.md)
   + [Criar e publicar uma jornada](./journeys/create-publish-journey.md)
   + [Jornada reentrada](./journeys/journey-re-entry.md)
   + [Nós de jornada](./journeys/journey-nodes.md)
   + Nós de jornada {#journey-nodes}
      + [Público-alvo da conta](./journeys/account-audience-nodes.md)
      + [Público-alvo de pessoa (Beta)](./journeys/person-audience-nodes.md)
      + [Realizar uma ação](./journeys/action-nodes.md)
      + [Acompanhar um evento](./journeys/listen-for-event-nodes.md)
      + [Dividir e mesclar caminhos](./journeys/split-merge-paths-nodes.md)
      + [Aguardar](./journeys/wait-nodes.md)
      + [Nós externos](./journeys/external-nodes.md)
   + [Detalhes da jornada](./journeys/journey-details.md)
+ Conteúdo da jornada {#journey-content}
   + [Canal de SMS](./content/sms-authoring.md)
   + [Canal do WhatsApp](./content/whatsapp-authoring.md)
   + Canal de email {#email-channel}
      + [Adicionar um email](./content/add-email.md)
      + [Otimização de hora de envio](./content/email-send-time-optimization.md)
      + [Criação de email](./content/email-authoring.md)
      + [Assistente de IA para criação de email](./content/ai-assistant-emails.md)
      + [Fluxos de trabalho do GenStudio](./content/genstudio-email-workflow.md)
      + [Modo escuro para design de email](./content/email-dark-mode.md)
      + [Modelos controlados](./content/email-authoring-governance.md)
      + [Email de alerta de vendas](./content/sales-alert-email.md)
      + [Desduplicação de email](./content/email-deduplication.md)
   + Canal da Web (Beta) {#web-channel}
      + [Visão geral](./content/web-experiences.md)
      + [Design de experiência online](./content/web-experience-design.md)
      + [Aplicativos de página única](./content/web-single-page-applications.md)
   + [Tokens de personalização](./content/personalization-my-tokens.md)
+ Públicos-alvo {#audiences}
   + [Públicos da Experience Platform](./audiences/account-audience-overview.md)
   + [Públicos-alvo externos](./audiences/target-external-audience.md)
   + [Públicos correspondentes da conta do LinkedIn](./data/linkedin-account-matched-audiences.md)
   + [Campos XDM padrão](./admin/field-mapping.md)
+ Contas {#accounts}
   + Grupos de compra {#buying-groups}
      + [Visão geral](./buying-groups/buying-groups-overview.md)
      + [Interesses na solução](./buying-groups/solution-interests.md)
      + [Modelos de função](./buying-groups/buying-groups-role-templates.md)
      + [Funções padrão e personalizadas](./buying-groups/default-custom-roles.md)
      + [Insights de função](./buying-groups/buying-group-role-insights.md)
      + Pontuação do grupo de compras {#scoring}
         + [Pontuações de engajamento](./buying-groups/engagement-scores.md)
         + [Pontuações de completude](./buying-groups/completeness-scores.md)
      + [Estágios do grupo de compra](./buying-groups/buying-group-stages.md)
      + [Criar grupos de compra](./buying-groups/buying-groups-create.md)
      + [Exportar contas](./audiences/account-list-export.md)
      + [Filtros de grupo de compra no Market Engage](./buying-groups/marketo-engage-smart-list-buying-group-filters.md)
      + [Insights no CRM](./buying-groups/incrm-insights.md)
   + Listas de contas {#account-lists}
      + [Visão geral](./accounts/account-lists.md)
      + [Usar em jornadas e programas](./accounts/account-lists-journeys.md)
   + Experiência de vendas {#sales-experience}
      + [Detalhes da conta](./accounts/account-details.md)
      + [Detalhes do grupo de compra](./buying-groups/buying-group-details.md)
      + [Dados da pessoa](./accounts/person-details.md)
      + [Vinculação do CRM](./accounts/crm-linking.md)
+ Gerenciamento de conteúdo {#content-management}
   + Emails {#emails}
      + [Trabalhar com conteúdo de email](./content/emails-list.md)
      + Pré-visualização e validação {#preview}
         + [Simular conteúdo](./content/email-simulate-content.md)
         + [Testar o e-mail rendering](./content/email-test-rendering.md)
         + [Relatório de spam](./content/email-spam-report.md)
      + [Colaboração por email](./content/email-collaboration-tools.md)
   + Ativos {#assets}
      + [Visão geral](./content/assets-overview.md)
      + Ativos internos {#internal-dam}
         + [Trabalhar com ativos internos](./content/internal-image-assets.md)
         + [Editar imagens com o Adobe Express](./content/image-edit-adobe-express.md)
      + [Ativos de imagem do Experience Manager](./content/aem-assets.md)
   + Modelos {#templates}
      + [Governança de conteúdo](./content/template-content-governance.md)
      + Modelos de email {#email-templates}
         + [Visão geral](./content/email-templates.md)
         + [Criação de modelo de email](./content/email-template-authoring.md)
         + [Edição avançada de HTML](./content/email-template-advanced-html.md)
         + [Converter imagem em modelo](./content/email-template-image-convert.md)
      + Modelos de página de destino (beta) {#landing-page-templates}
         + [Visão geral](./content/landing-page-templates.md)
         + [Design de modelo de página de destino](./content/landing-page-template-design.md)
   + Fragmentos {#visual-fragments}
      + [Visão geral](./content/fragments.md)
      + [Criação de fragmentos](./content/fragment-authoring.md)
   + Formulários (beta) {#forms}
      + [Visão geral](./content/forms.md)
      + [Design de formulário](./content/form-design.md)
   + Páginas de destino (beta) {#landing-pages}
      + [Visão geral](./content/landing-pages.md)
      + [Design da página de destino](./content/landing-page-design.md)
      + [Assistente de IA para conteúdo de página de destino](./content/ai-assistant-landing-pages.md)
   + Ferramentas de design de conteúdo {#content-design}
      + [Componentes da estrutura](./content/structure-components.md)
      + [Componentes do conteúdo](./content/content-components.md)
      + [CSS personalizado](./content/design-custom-css.md)
   + Marcas (beta) {#brands}
      + [Visão geral](./content/brands-overview.md)
      + [Gerenciar e criar](./content/brands-manage-create.md)
      + [Modelos de IA gerativa](./content/generative-ai-models.md)
   + [Temas da marca](./content/brand-themes.md)
   + [Avaliação de conteúdo](./content/content-evaluation.md)
   + [Conteúdo condicional](./content/conditional-content.md)
   + [Acessibilidade de conteúdo](./content/accessible-content.md)
   + Personalização {#personalization}
      + [Visão geral](./content/personalization.md)
      + [Sintaxe de personalização](./content/personalization-syntax.md)
      + [Lista de funções auxiliares](./content/personalization-helper-functions.md)
+ Painéis inteligentes {#dashboards}
   + [Painel de insights](./dashboards/intelligent-dashboard.md)
   + [Painel de engajamento](./dashboards/engagement-dashboard.md)
   + [Painel de participação na Web](./dashboards/web-engagement-dashboard.md)
   + [Painel Grupos de compra](./dashboards/buying-groups-dashboard.md)
   + [Painel de Jornadas da conta](./dashboards/journeys-dashboard.md)
+ Administração {#admin}
   + [Governança](./admin/governance.md)
   + [Mapeamento de personas](./admin/persona-mapping.md)
   + Configurações {#configurations}
      + [Repositórios do AEM Assets](./admin/configure-aem-repositories.md)
      + [Dados de intenção](./admin/intent-data.md)
      + [Ponderação da pontuação de engajamento](./admin/engagement-score-weighting.md)
      + [Ações externas](./admin/configure-external-actions.md)
   + Canais {#channels}
      + [Configurações de email](./admin/configure-channels-emails.md)
      + [Configuração de SMS](./admin/configure-channels-sms.md)
      + [Configurações do WhatsApp](./admin/configure-channels-whatsapp.md)
      + [Configurações do canal da Web (Beta)](./admin/configure-channels-web.md)
      + [Configurações da página de aterrissagem (Beta)](./admin/landing-page-settings.md)
      + [Configurar sequências de dados para a coleção de eventos](./data/aep-event-collection.md)
