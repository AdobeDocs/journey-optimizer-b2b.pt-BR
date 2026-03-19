---
title: Configuração simplificada da arquitetura
description: Configure o Journey Optimizer B2B edition na arquitetura simplificada. Configure esquemas XDM, canais de email/SMS, ações de jornada do Marketo Engage e usuários.
feature: Setup, Administration
role: Admin, Data Engineer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 38d1794ed30a34dbb34dfaec2d3088bc3a4680ac
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 17%

---

# Configuração simplificada da arquitetura

Agora, o Adobe Journey Optimizer B2B Edition está disponível com uma arquitetura simplificada. Com essa arquitetura, o Journey Optimizer B2B edition e o Marketo Engage não estão mais no mesmo sistema e armazenamento de dados. O Journey Optimizer B2B Edition recebe dados somente da Adobe Experience Platform. No entanto, ele continua a depender de direitos do Marketo Engage e alguns recursos de back-end, como entrega de email, para provisionar e configurar o sistema.

A arquitetura simplificada é a base que desbloqueia novos recursos no Journey Optimizer B2B edition:

* **Unifique e dimensione facilmente seus dados:** A nova plataforma oferece suporte a modelos de dados complexos, incluindo objetos personalizados, grupos de compra e eventos de conta.

* **Conecte várias instâncias do Adobe Marketo Engage:** gerencie e unifique dados de vários ambientes do Marketo Engage em um único local.

* **Mantém seus dados seguros** Recursos avançados de privacidade e segurança que ajudam a proteger as informações de seus clientes. (_Em breve_)

* **Criada para o futuro:** esta atualização oferece melhorias e inovações contínuas.

Para ambientes provisionados para essa arquitetura, use as seguintes diretrizes para configuração.

Use esta lista de verificação para concluir a configuração do Journey Optimizer B2B edition na arquitetura simplificada.

## &#x200B;1. Gerar namespaces e esquemas B2B

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuração do ambiente:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Baixe o namespace e o utilitário de geração automática de esquema do GitHub.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Obtenha as credenciais da API do Experience Platform e os cabeçalhos necessários.</td>
<td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/platform-apis/api-guide">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Aplique valores de ambiente ao seu ambiente do Postman.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Execute os scripts:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Execute o utilitário de geração <em>Namespaces e Esquemas</em> no Postman e confirme se os namespaces e os esquemas foram criados.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Saiba mais</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. Configurar campos e eventos XDM

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Classes XDM padrão</strong>: configurar o Perfil Individual XDM e as classes de Conta Comercial XDM.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Selecione campos gerenciados a serem expostos para jornadas, grupos de compra e personalização de email.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Editar campos atualizáveis para esquemas.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Esquemas relacionais</strong>: selecione a classe XDM relacional (objeto personalizado muitos para um da conta).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Certifique-se de que os esquemas tenham os valores de configuração necessários.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Eventos</strong>: configurar tipos e campos de eventos do Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configure cada tipo de evento do Experience Platform com campos que serão aceitos nos caminhos de decisão/divisão do jornada.</td>
<td><a href="./admin/configure-aep-events.md">Saiba mais</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Configurar rastreamento e capacidade de entrega de email

Para enviar emails do [!DNL Journey Optimizer B2B Edition] na arquitetura simplificada, configure o rastreamento de email e a capacidade de entrega na instância de produção [!DNL Marketo Engage] anexada e no aplicativo [!DNL Journey Optimizer B2B Edition].

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuração inicial</strong> para a instância do Marketo Engage anexada</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar novo CNAME para Links de rastreamento em registros DNS</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar domínios de marca para a instância do Marketo Engage anexada</td>
<td><a href="./start/branding-domains.md">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar o DKIM e o SPF para a instância do Marketo Engage anexada</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar registros MX para o seu domínio</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Adicionar endereços IP de saída ao incluo na lista de permissões</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuração de email</strong> para a instância do Marketo Engage anexada</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Do Email</em> e <em>Do Rótulo</em> (opcional)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Cancelar assinatura do HTML</em> e <em>Cancelar assinatura do texto</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Exibir como Página da Web HTML</em> e <em>Exibir como Página da Web Text</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Limites de Recuperação de Objeto Personalizado</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Opções de Cabeçalho Personalizadas</em></td>
<td><a href="./start/email-setup.md#custom-header-options">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar a filtragem da <em>Atividade de bot</em></td>
<td><a href="./start/email-setup.md#filter-email-bots">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuração do canal de email</strong> para o Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar <em>Limites de comunicação</em> no Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Saiba mais</a></td>
</tr>
</tbody>
</table>

<!-- TBD for later 

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Configurar canais de conteúdo adicionais

Para oferecer suporte aos profissionais de marketing para a inclusão de outros canais em suas jornadas, configure canais adicionais.

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">Configuração de canal de <strong>SMS</strong> para o Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configure cada conta SMS que você deseja que tenha suporte.</td>
<td><a href="./admin/configure-channels-sms.md">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configurações de canal do Journey Optimizer B2B edition para páginas de aterrissagem</strong> (Beta).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Conclua as configurações da landing page para oferecer suporte aos profissionais de marketing que criam e publicam essas páginas</td>
<td><a href="./admin/landing-page-settings.md">Saiba mais</a></td>
</tr>
<tr>
<td colspan="2">Configuração do canal <strong>Web</strong> (Beta) para o Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar o site da empresa para oferecer suporte ao Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/collection/js/js-overview">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Adicione propriedades da Web por um URL em que o conteúdo é entregue.</td>
<td><a href="./admin/configure-channels-web.md">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Instrua os autores da experiência Web a instalar a extensão de navegador Auxiliar de edição visual do Adobe Experience Cloud.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Saiba mais</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Conectar a instância do Marketo Engage para oferecer suporte a ações de jornada (opcional)

Se você planeja complementar os recursos do Journey Optimizer B2B edition com campanhas e programas no Marketo Engage, configure o suporte para ações do Marketo Engage. Essas ações permitem que suas equipes de marketing coordenem o marketing _baseado em conta_ no Journey Optimizer B2B edition e os esforços de marketing _baseado em lead_ no Marketo Engage.

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Para cada instância do Marketo Engage</strong> para oferecer suporte a ações de jornada</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Criar o serviço personalizado do Marketo Engage</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Adicionar a integração no Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Saiba mais</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Habilitar acesso do usuário

Quando o provisionamento estiver concluído, as sandboxes serão vinculadas e as tarefas de configuração iniciais serão concluídas, configure o Journey Optimizer B2B edition e o Marketo Engage Access para sua equipe e usuários.

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fornecer acesso e permissões ao produto</strong> para usuários</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Criar um perfil de produto do Marketo Engage na Adobe Admin Console (somente nova instância do Marketo Engage)</td>
<td><a href="./admin/user-management.md#create-the-marketo-engage-product-profile">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Adicionar um grupo de usuários para o perfil</td>
<td><a href="./admin/user-management.md#add-a-user-group-for-the-profile">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Configurar funções de usuário B2B</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Saiba mais</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção"/></td>
<td>Adicionar usuários ou grupos às funções</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Saiba mais</a></td>
</tr>
</tbody>
</table>
