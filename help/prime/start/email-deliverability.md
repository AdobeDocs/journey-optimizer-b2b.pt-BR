---
title: Configuração da entregabilidade de email
description: Configure pools de delegação de subdomínio, DMARC, SPF, DKIM e IP para o Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 4c3919d0f2d0c5c12236f3ced1b0e9674ef9567e
workflow-type: tm+mt
source-wordcount: 1920
ht-degree: 1%

---

# Capacidade de entrega de email

As informações a seguir são para administradores que configuram a infraestrutura de envio para suportar profissionais de marketing e criadores de conteúdo de email. Ele descreve recursos de entrega e como configurar subdomínios, autenticação e pools de IP. Consulte os seguintes tópicos para obter informações adicionais sobre canais de email:

* Configurando canais de email - [Configuração de canal de email](../admin/email-channel-configuration.md)
* Criando emails - [Adicionar emails ao jornada](../marketing/email-channel.md)
* Criação de conteúdo de email - [Criação de conteúdo de email](../content/email-authoring.md).

A capacidade de entrega de emails no [!DNL Journey Optimizer B2B Prime] é o conjunto de configurações de infraestrutura e autenticação que ajudam as mensagens de email a chegar à caixa de entrada do destinatário, não à pasta de spam, e não bloqueadas pelos ISPs (Provedores de Serviços de Internet).

Ele usa os seguintes blocos fundamentais, configurados por um administrador, normalmente na seguinte ordem:

1. [Delegar um ou mais subdomínios](#subdomain-delegation) à Adobe.
1. [Configurar registros do DMARC, SPF e DKIM](#dmarc-spf-dkim) em cada subdomínio.
1. [Confirme o pool de IPs](#ip-pools) usado para enviar emails para o subdomínio.
1. [Crie uma ou mais configurações de canal de email](../admin/email-channel-configuration.md#create-email-channel-configuration) que associam um subdomínio, um pool de IPs e uma identidade de remetente.

![Configuração da capacidade de entrega de email para o Journey Optimizer B2B Prime](./assets/email-deliverability-diagram.svg){width="450" zoomable="yes"}

>[!TIP]
>
>Trate a capacidade de entrega e a configuração do canal como uma atividade de administrador única. Quando configurados, os profissionais de marketing e autores de email não precisam revisitá-los.

## Limitações atuais {#limitations}

* **O método de delegação personalizado** para delegação de subdomínio ainda não está disponível. Use Totalmente delegado ou CNAME. A delegação personalizada está direcionada para a versão do GA.
* **Pools de IP dedicados** não estão disponíveis na Beta. O pool de IPs compartilhados é a única opção. IPs dedicados enviados na GA, incluindo planejamento de aquecimento de IP e gerenciamento de registros PTR.

## Principais conceitos {#key-concepts}

Antes de configurar o email, analise esses conceitos que se aplicam aos recursos de capacidade de entrega de canal de email:

| Conceito | O que significa em [!DNL Journey Optimizer B2B Prime] |
| ------- | ---------------------- |
| **_Subdomínio_** | Uma parte delegada do seu domínio de envio (por exemplo, `mail.contoso.com`) usada para enviar emails pelo Prime. Os subdomínios isolam sua reputação de marketing B2B do correio corporativo ou transacional. |
| **_Pool de IPs_** | Um grupo de endereços IP associados a um ou mais subdomínios. A Prime oferece suporte a um pool de IPs compartilhados gerenciado pela Adobe nesta versão; os pools de IP dedicados estão no roteiro de disponibilidade geral. |
| **_Configuração de canal_** | Um conjunto reutilizável de configurações de envio de email (identidade do remetente, endereço de resposta, subdomínio, pool de IPs, tipo de email e rastreamento) que você anexa às ações de email no jornada. É possível ter várias configurações de canal nomeadas para diferentes marcas, unidades de negócios ou tipos de envio. |

<!--

## Roles and permissions {#roles-permissions}

[!DNL Journey Optimizer B2B Prime] uses role-based access control (RBAC) for email features. Permissions are managed in the Adobe Admin Console (IMS) and synced at login. Product administrators assign granular permissions to product profiles, and then attach those product profiles to users.

Access to email functionality in [!DNL Journey Optimizer B2B Prime] is gated by two layers:

1. **Feature flag (LD).** A LaunchDarkly flag controls whether the entire feature is turned on for your organization. Email authoring and deliverability are gated by `dx_ajo_btob_channel_foundation`. Without this flag, the feature is hidden regardless of permissions.
2. **Functional permission.** A user-level permission that controls whether a specific user can read or write within a feature.

Most email features follow a `view-*` (read) and `manage-*` (write) pattern. A user needs the read permission to see a feature in the navigation, and the write permission to create, edit, or delete within it.

### Email authoring permissions {#email-authoring-permissions}

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View emails** | `view-b2b-emails` | View the email list, open emails, view content (read-only). |
| **Create / edit / delete emails** | `manage-b2b-emails` | All read access plus create, edit, duplicate, and delete emails. Required to author email content within a journey. |
| **View templates** | `view-b2b-templates` | Browse and preview templates in the Templates gallery (read-only). |
| **Create / edit / delete templates** | `manage-b2b-templates` | All read access plus create, edit, and delete saved templates. |
| **View fragments** | `view-b2b-fragments` | Browse and preview visual fragments (read-only). |
| **Create / edit fragments** | `manage-b2b-fragments` | All read access plus create and edit visual fragments. |
| **Publish fragments** | `publish-b2b-fragments` | Publish a fragment so it becomes available to email authors across the organization. |
| **Manage shared assets and library items** | `manage-b2b-library-items` | Manage the underlying shared library used by templates, fragments, and emails. Often granted alongside the template/fragment manage permissions. |
| **Manage usage labels** | `manage-b2b-delete-usage-labels` | Manage data usage labels (DULE) attached to library items for governance. |
| **Manage packages** | `manage-b2b-packages` | Bundle and move templates, fragments, and emails between sandboxes. |
| **View assets (Marketo Design Studio assets in Prime)** | `view-b2b-assets` | Browse the asset picker and preview images. Read-only. |
| **Manage assets** | `manage-b2b-assets` | All read access plus future asset-management actions (Beta scope). |
| **Export message data** | `manage-b2b-message-export` | Export email-level message data and reports. |

Within a person journey, the **Send email** action requires `manage-b2b-person-journeys` (to add the action and activate the journey). A user with only email permissions can author content but cannot add an email to a journey.

### Email deliverability permissions {#email-deliverability-permissions}

Deliverability features (subdomains, DMARC, IP pools, suppression lists, allowed lists, IP warmup plans, and seed lists) are administrator-level configuration. They are governed by two permissions covering the entire **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** area:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View email settings** | `view-b2b-email-settings` | View subdomains, PTR records, IP pools, suppression list, allowed list, IP warmup plans, and seed lists (read-only). |
| **Manage email settings** | `manage-b2b-email-settings` | All read access plus delegate subdomains, configure DMARC, manage suppression and allowed lists, manage IP warmup plans and seed lists. |

Some sub-features within Email settings are gated by additional LaunchDarkly flags — Suppression list (`enable-suppression`), Allowed list (`enable-allow-list`), Seed lists (`enable-seedlist-ui`). If a sub-feature is not visible in your organization, check with your Adobe representative on flag enablement.

### Channel configuration permissions {#channel-configuration-permissions}

Channel configurations sit under **[!UICONTROL Channels]** → **[!UICONTROL General settings]**. They tie deliverability primitives (subdomain, IP pool, sender identity) to a reusable object that journey authors reference. They are governed by a single permission:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **Manage channel configurations** | `manage-b2b-channels-configurations` | View, create, edit, and delete email channel configurations. |

-->

## Delegação de subdomínios {#subdomain-delegation}

A delegação de subdomínio informa à Internet que a Adobe está autorizada a enviar emails em nome de um subdomínio específico (por exemplo, `mail.contoso.com`) do seu domínio. Delegar um subdomínio dedicado — em vez do domínio raiz — protege o e-mail corporativo e oferece os seguintes benefícios:

* **Isolamento de reputação.** Os envios de marketing são mantidos separados do correio corporativo. Se a reputação de marketing cair, seu email transacional e corporativo não será afetado.
* **Aquecimento de IP mais rápido.** Subdomínios dedicados ajudam a estabelecer uma reputação positiva do remetente mais rapidamente com ISPs.
* **Autenticação moderna.** O SPF, o DKIM e o DMARC podem ser configurados corretamente por subdomínio sem afetar outros fluxos de email.
* **Conformidade.** Ajuda a atender aos requisitos de remetentes em massa do Gmail, Yahoo e outros principais ISPs.

>[!NOTE]
>
>Cada subdomínio no Prime só pode ser usado por um produto da Adobe. Não é possível compartilhar o mesmo subdomínio de envio entre o Prime e outro produto, como o Adobe Marketo Engage ou o Adobe Campaign — você deve usar subdomínios distintos.

### Métodos compatíveis {#supported-methods}

O Prime oferece suporte a dois dos três métodos de delegação de subdomínio nesta versão do Beta. O terceiro método (delegação personalizada) está no roteiro.

| Método | Quando usar | O que isso envolve |
| ------ | ----------- | ---------------- |
| **Totalmente Delegado** | Recomendado | Delegar autoridade DNS completa para o subdomínio à Adobe. O Adobe cria e mantém registros MX, SPF, DKIM, DMARC, A e CNAME. Menor sobrecarga operacional. O Adobe lida com as alterações de DNS para você. |
| **CNAME** | Para políticas restritas | Mantenha a autoridade DNS do seu lado e crie registros CNAME apontando para registros gerenciados pela Adobe. Use isso quando a política DNS da organização não permitir delegação completa. Você é responsável por manter os registros DNS. |
| **Delegação personalizada** | Roteiro (GA) | Mantenha a propriedade total dos certificados DNS e SSL. Fornece controle máximo, incluindo a capacidade de usar seus próprios certificados. Ele é direcionado para a versão do GA. |

### Delegar um subdomínio (método totalmente delegado) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* Decida sobre uma convenção de nomenclatura de subdomínio (por exemplo, `mail.contoso.com` para marketing, `alerts.contoso.com` para transacional).
>* Confirme com a equipe de TI/DNS que eles podem delegar o subdomínio (registros NS) à Adobe.
>* Crie o novo subdomínio em seu provedor de DNS e aguarde de de 24 a 48 horas pela propagação de DNS antes de delegar à Adobe.
>* Confirme se você tem a função Administrador no Prime.

1. Na navegação à esquerda [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Canais]**.
1. No painel, expanda **[!UICONTROL Configurações de email]** e selecione **[!UICONTROL Subdomínios]**.
1. Clique em **[!UICONTROL Configurar subdomínio]**.
1. Insira o nome completo do subdomínio (por exemplo, `mail.contoso.com`).
1. Escolha **[!UICONTROL Totalmente Delegado]** como o método de delegação.
1. Configure o DMARC para o subdomínio (consulte [DMARC, SPF e DKIM](#dmarc-spf-dkim)).

   No mínimo, configure um registro do DMARC com uma política inicial de `none` para que você possa monitorar relatórios sem afetar a entrega.

1. Revise a lista de registros DNS para o Adobe gerenciar.

   Normalmente, eles incluem registros MX, SPF, DKIM, DMARC, A e CNAME (para rastreamento e URLs de mirror page).

1. Baixe os registros DNS como um arquivo CSV usando o botão **[!UICONTROL Baixar registros]**. Compartilhe este arquivo com a equipe de DNS.

1. A equipe de DNS adiciona os registros NS na solução de hospedagem de domínio que delega o subdomínio à Adobe.

1. Depois que sua equipe de DNS confirmar que os registros estão em vigor, volte para [!DNL Journey Optimizer B2B Prime] e marque a caixa confirmando que você criou os registros necessários no site de hospedagem.

1. Clique em **[!UICONTROL Enviar]** para iniciar uma série de verificações de validação (pré-validação, MX, SPF, DKIM, DMARC, registro FBL).

1. Aguarde o status do subdomínio mudar para **[!UICONTROL Sucesso]**.

   Isso normalmente leva alguns minutos quando a propagação do DNS é concluída.

>[!NOTE]
>
>Se a validação falhar, o status será alterado para **[!UICONTROL Falha]** e [!DNL Journey Optimizer B2B Prime] exibirá o motivo (por exemplo, registro NS não encontrado, registro MX ausente ou DMARC configurado incorretamente). Corrija o problema de DNS subjacente e tente enviar novamente.

### Delegar um subdomínio (método CNAME) {#delegate-cname}

Use esse método somente se a política DNS da organização proibir a delegação completa. Com o CNAME, você mantém registros de DNS da sua parte.

1. Na navegação à esquerda [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Canais]**.
1. No painel, expanda **[!UICONTROL Configurações de email]** e selecione **[!UICONTROL Subdomínios]**.
1. Clique em **[!UICONTROL Configurar subdomínio]**.
1. Insira o nome completo do subdomínio.
1. Escolha **[!UICONTROL CNAME]** como o método de delegação.
1. Configure o DMARC para o subdomínio ([DMARC, SPF e DKIM](#dmarc-spf-dkim)).
1. Revise a lista de registros CNAME a serem gerados. Eles apontam os componentes do subdomínio para registros gerenciados pela Adobe.
1. Baixe os registros como CSV e compartilhe com a equipe DNS.
1. A equipe de DNS adiciona cada registro CNAME à solução de hospedagem de DNS.
1. Quando os registros estiverem no local e forem propagados, volte para [!DNL Adobe Journey Optimizer B2B Prime] e confirme.
1. Clique em **[!UICONTROL Enviar]**.
1. Aguarde o status alcançar **[!UICONTROL Sucesso]**.

>[!IMPORTANT]
>
>Com o CNAME, a Adobe não pode ajudar você a alterar, manter ou solucionar problemas do DNS para o subdomínio. Quaisquer alterações futuras, como a adição de um novo CNAME para uma atualização de recurso, devem ser feitas pela equipe de DNS.

### Medidas de proteção de subdomínio {#subdomain-guardrails}

* **Limite padrão:** 10 subdomínios por organização. Entre em contato com seu representante da Adobe se precisar de mais (até 100, dependendo do contrato).
* **Propagação de DNS:** Permita que as alterações ocorram de 24 a 48 horas globalmente. A validação pode falhar simplesmente porque o DNS ainda não se propagou.
* **Reutilização de subdomínio:** um subdomínio que já está sendo usado por outro produto da Adobe (Marketo Engage, Adobe Campaign) não pode ser reutilizado no Prime.

## DMARC, SPF e DKIM {#dmarc-spf-dkim}

DMARC, SPF e DKIM são padrões de autenticação de email. Juntos, eles provam aos servidores de email de recebimento que sua mensagem é realmente enviada em nome de seu domínio e não foi falsificada. ISPs modernos — Gmail, Yahoo, Microsoft — exigem esses padrões para remetentes em massa.

| Registro | Significa | Finalidade |
| ------ | ---------- | ------- |
| **SPF** | Estrutura de Política do Remetente | Lista os IPs do servidor de email permitidos para enviar emails do seu domínio. O recebimento de servidores rejeita emails de IPs que não estão nesta lista. O Adobe cria e mantém o registro SPF automaticamente ao delegar um subdomínio (Totalmente delegado). |
| **DKIM** | Email identificado de DomainKeys | Uma assinatura criptográfica adicionada a cada email de saída. O servidor de recebimento verifica a assinatura em relação a uma chave pública publicada no DNS. O Adobe gera automaticamente chaves DKIM e registros DNS durante a delegação de subdomínio. |
| **DMARC** | Autenticação de mensagens baseada em domínio, Relatórios e conformidade | Informa aos servidores receptores o que fazer se o SPF ou o DKIM falhar — e fornece relatórios sobre os resultados da autenticação. O DMARC tem três modos de política: nenhum, quarentena e rejeitar. |

### Modos de política do DMARC {#dmarc-policy-modes}

| Política | Ação | Quando usar |
| ------ | ------ | ----------- |
| `none` | Monitorar | O servidor de recebimento não faz nada se o DMARC falhar — mas ainda envia um relatório. Use isso ao delegar um subdomínio pela primeira vez para confirmar se a autenticação está funcionando sem correr o risco de perder a mensagem. |
| `quarantine` | Quarentena | O servidor de recebimento coloca mensagens com falha na pasta spam/lixo eletrônico. |
| `reject` | Rejeitar | O servidor de recebimento rejeita (devolve) mensagens com falha na autenticação. Modo estrito. Recomendado assim que você estiver confiante na configuração da autenticação. |

### Configurar DMARC {#configure-dmarc}

O DMARC é configurado no momento da delegação de subdomínio, mas você também pode adicionar ou atualizar o DMARC para um subdomínio já delegado.

1. Na navegação à esquerda [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Canais]**.

1. No painel, expanda **[!UICONTROL Configurações de email]** e selecione **[!UICONTROL Subdomínios]**.

1. Na lista Subdomínios, localize o subdomínio e verifique a coluna Registro do DMARC.

   Se um registro estiver ausente, um alerta será exibido.

1. Abra o subdomínio e role até a seção Registro do DMARC.

   * Se um registro DMARC já existir no domínio pai, [!DNL Journey Optimizer B2B Prime] buscará os valores automaticamente. Você pode mantê-las ou substituí-las.
   * Se não existir nenhum registro, escolha **[!UICONTROL Gerenciar com o Adobe]** e o Adobe criará e hospedará o registro do DMARC.

1. Defina a política: `none`, `quarantine` ou `reject`. Comece com `none` a menos que você já tenha uma postura madura de DMARC em seu domínio pai.

1. (Opcional) Configure as marcas DMARC adicionais (`sp` para política de subdomínio, `pct` para porcentagem, `rua` e `ruf` para endereços de relatório).

1. Se estiver usando Totalmente Delegado, clique em **[!UICONTROL Salvar]**.

   O Adobe aplica o registro automaticamente. Se estiver usando CNAME, copie o registro DNS e peça à sua equipe de DNS para adicioná-lo e, em seguida, confirme-o no [!DNL Journey Optimizer B2B Prime].

1. Aguarde até 48 horas para propagação DNS e verifique se o indicador de status do DMARC na página de subdomínio está verde/íntegro.

>[!TIP]
>
>Comece com `policy=none` para monitorar os relatórios de autenticação, avance para `quarantine` e finalmente para `reject` assim que seus relatórios mostrarem um alinhamento íntegro de SPF e DKIM. Mover diretamente para `reject` sem monitoramento pode fazer com que mensagens legítimas sejam rejeitadas.

## Pools de IP {#ip-pools}

Um pool de IPs é um grupo nomeado de endereços IP usados para enviar seu email. Os pools de IP são essenciais para a reputação do remetente: cada pool tem sua própria reputação com ISPs, portanto, um problema com um pool (por exemplo, um burst de marketing que aciona reclamações de spam) não contamina outro (por exemplo, confirmações transacionais).

### Tipos de pool {#pool-types}

| Tipo de pool | Disponibilidade | Descrição |
| --------- | ------------ | ----------- |
| **Pool de IPs compartilhados** | Disponível em Beta | Um pool de endereços IP gerenciados pela Adobe e compartilhados entre muitos clientes. A reputação é mantida pela Adobe em todo o pool. Melhor para volume de email baixo a médio e clientes que não desejam gerenciar o aumento gradual de IP. |
| **Pool de IPs dedicados** | Roteiro (GA) | Um ou mais endereços IP alocados exclusivamente à sua organização. Você é o dono da reputação. Recomendado para remetentes de alto volume. Inclui planejamento de aquecimento de IP e gerenciamento de registros PTR. |

### Revisar e atribuir um pool de IPs {#review-ip-pool}

Nesta versão, os pools de IP são pré-provisionados para sua organização. Atribua um pool de IP ao criar uma configuração de canal de email.

1. Na navegação à esquerda [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Canais]**.
1. No painel, expanda **[!UICONTROL Configurações de email]** e selecione **[!UICONTROL pools de IP]**.
1. Confirme se um pool de IP com o status **[!UICONTROL Ativo]** está disponível para sua organização.
1. Passe o mouse sobre o pool para visualizar os endereços IP e seus registros PTR (DNS reverso).
1. Se sua organização tiver várias unidades de negócios ou marcas, planeje como você usará os pools de IP (por exemplo, pool de marketing versus pool de webinários) antes de criar as configurações de canal.

>[!IMPORTANT]
>
>Não misture tráfego de marketing e transacional no mesmo pool de IPs, mesmo quando o pool compartilhado estiver disponível. A configuração Tipo de email na configuração do canal (Marketing versus Transacional) controla o comportamento de supressão, mas as configurações de canal ainda devem usar pools distintos, quando possível.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->

