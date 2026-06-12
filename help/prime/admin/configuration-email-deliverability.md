---
title: Capacidade de entrega de email e configuração de canal
description: Defina configurações de delegação de subdomínio, DMARC, SPF, DKIM, pools de IP e canais de email para o Journey Optimizer B2B Prime.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '3414'
ht-degree: 0%

---

# Capacidade de entrega de email e configuração de canal

O Prime [!DNL Adobe Journey Optimizer B2B Edition] traz uma experiência moderna de criação e entrega de email de nível empresarial para os profissionais de marketing B2B. Esta versão apresenta ferramentas de design de email reprojetadas e um conjunto completo de controles de capacidade de entrega de email.

As informações a seguir são para administradores que configuram a infraestrutura de envio para oferecer suporte a profissionais de marketing e autores de email. Ele descreve recursos, funções e permissões de entrega e como configurar subdomínios, autenticação, pools de IP e configurações de canal.

Para obter informações detalhadas sobre como criar emails e conteúdo de email no espaço de design de email, consulte [Criação de email](../content/email-authoring.md).

## Visão geral do canal de email {#overview}

* **Ferramentas visuais de design de email de arrastar e soltar** - Projete o conteúdo de email com estruturas, componentes de conteúdo, temas, suporte para o modo escuro e fragmentos visuais reutilizáveis.
* **Configurações de canal de email** - Gerencie a identidade do remetente, o comportamento de resposta, os tipos de mensagem de marketing vs. transacional e o rastreamento.
* **Controles de capacidade de entrega de email** - Configure seu canal de capacidade de entrega de email, incluindo delegação de subdomínio (métodos totalmente delegados e CNAME), DMARC, configuração automática SPF/DKIM e suporte a pool de IP compartilhado.
* **Ação Enviar email** - De uma jornada, adicione uma ação Enviar email, incluindo personalização usando atributos de perfil (sintaxe Handlebars).
* **Ativos do Marketo Design Studio** — escolha imagens e ativos de uma cópia única da biblioteca de ativos do Marketo Engage diretamente na tela de email.
* **Modelos e fragmentos reutilizáveis** — Salve cabeçalhos, rodapés, CTAs e layouts completos de email comuns e reutilize-os no jornada.
* **Controle de Acesso com Base em Função (RBAC)** — aplique permissões granulares para criar, editar, aprovar e enviar email.

## Principais conceitos {#key-concepts}

Antes de configurar o email, analise esses conceitos, que se aplicam aos recursos do canal de email em todo o produto.

| Conceito | O que significa no Prime [!DNL Journey Optimizer B2B Edition] |
| ------- | ---------------------- |
| **_Configuração de canal_** | Um conjunto reutilizável de configurações de envio de email — incluindo identidade do remetente, endereço de resposta, subdomínio, pool de IPs, tipo de email (marketing ou transacional) e rastreamento — que você anexa às ações de email no jornada. É possível ter várias configurações de canal nomeadas para diferentes marcas, unidades de negócios ou tipos de envio. |
| **_Subdomínio_** | Uma parte delegada do seu domínio de envio (por exemplo, `mail.contoso.com`) usada para enviar emails pelo Prime. Os subdomínios isolam sua reputação de marketing B2B do correio corporativo ou transacional. |
| **_Pool de IPs_** | Um grupo de endereços IP associados a um ou mais subdomínios. A Prime oferece suporte a um pool de IPs compartilhados gerenciado pela Adobe nesta versão; os pools de IP dedicados estão no roteiro de disponibilidade geral. |
| **_Espaço de design de email_** | A tela visual e as ferramentas de design usadas para compor conteúdo de email. Ele inclui componentes de layout de arrastar e soltar, templates, fragmentos, temas e um editor de personalização. |
| **_Modelo_** | Um layout de email reutilizável que está disponível para criar um novo email. Ele pode ser um modelo integrado fornecido pelo Adobe ou um modelo personalizado criado pela sua equipe. |
| **_Fragmento visual_** | Um bloco reutilizável de conteúdo (como cabeçalho, rodapé, CTA, aviso de isenção legal) que pode ser inserido em vários emails. A atualização de um fragmento propaga a alteração para cada email que o utiliza. |
| **_Tema_** | Uma predefinição de estilo reutilizável (cores, tipografia, espaçamento, estilos de botão) aplicada em um email. |
| **_token do Personalization_** | Uma expressão Handlebars — por exemplo, `{{profile.firstName}}` — resolvida no momento do envio usando os dados de perfil de cada recipient. |
| **_Ação Enviar email_** | O nó de ação de jornada que usa uma configuração de canal e conteúdo de email para entregar um email. |

## Funções e permissões {#roles-permissions}

O Prime [!DNL Journey Optimizer B2B Edition] usa o controle de acesso baseado em função (RBAC) para recursos de email. As permissões são gerenciadas no Adobe Admin Console (IMS) e sincronizadas no logon. Os administradores de produtos atribuem permissões granulares a perfis de produtos e, em seguida, anexam esses perfis de produtos aos usuários.

O acesso à funcionalidade de email no Prime [!DNL Journey Optimizer B2B Edition] é restringido por duas camadas:

1. **Sinalizador de recurso (LD).** Um sinalizador do LaunchDarkly controla se todo o recurso está ativado para a organização. A criação e a entrega de emails foram restringidas por `dx_ajo_btob_channel_foundation`. Sem esse sinalizador, o recurso fica oculto independentemente das permissões.
2. **Permissão funcional.** Uma permissão no nível do usuário que controla se um usuário específico pode ler ou gravar em um recurso.

A maioria dos recursos de email segue um padrão `view-*` (leitura) e `manage-*` (gravação). Um usuário precisa da permissão de leitura para ver um recurso na navegação e da permissão de gravação para criar, editar ou excluir dentro dele.

### Permissões de criação de email {#email-authoring-permissions}

| Recurso | Permissão | O que ele permite |
| ---------- | ---------- | -------------- |
| **Exibir emails** | `view-b2b-emails` | Exibir a lista de emails, abrir emails, exibir conteúdo (somente leitura). |
| **Criar / editar / excluir emails** | `manage-b2b-emails` | Todo o acesso de leitura além de criar, editar, duplicar e excluir e-mails. Obrigatório para criar conteúdo de email em uma jornada. |
| **Exibir modelos** | `view-b2b-templates` | Procurar e visualizar modelos na galeria Modelos (somente leitura). |
| **Criar / editar / excluir modelos** | `manage-b2b-templates` | Todo o acesso de leitura, além de criar, editar e excluir modelos salvos. |
| **Exibir fragmentos** | `view-b2b-fragments` | Procurar e visualizar fragmentos visuais (somente leitura). |
| **Criar/editar fragmentos** | `manage-b2b-fragments` | Todo o acesso de leitura, além de criar e editar fragmentos visuais. |
| **Publicar fragmentos** | `publish-b2b-fragments` | Publique um fragmento para que ele fique disponível para autores de email em toda a organização. |
| **Gerenciar ativos compartilhados e itens de biblioteca** | `manage-b2b-library-items` | Gerencie a biblioteca compartilhada subjacente usada por modelos, fragmentos e emails. Geralmente, concedido junto com as permissões de gerenciamento de modelo/fragmento. |
| **Gerenciar rótulos de uso** | `manage-b2b-delete-usage-labels` | Gerenciar DULE (rótulos de uso de dados) anexados aos itens de biblioteca para governança. |
| **Gerenciar pacotes** | `manage-b2b-packages` | Agrupar e mover modelos, fragmentos e emails entre sandboxes. |
| **Exibir ativos (ativos do Marketo Design Studio no Prime)** | `view-b2b-assets` | Navegue pelo seletor de ativos e visualize imagens. Somente leitura. |
| **Gerenciar ativos** | `manage-b2b-assets` | Todo o acesso de leitura e futuras ações de gerenciamento de ativos (escopo do Beta). |
| **Exportar dados da mensagem** | `manage-b2b-message-export` | Exportar dados e relatórios de mensagens no nível de email. |

Em uma jornada, a ação **Enviar email** requer `manage-b2b-person-journeys` (para adicionar a ação e ativar a jornada). Um usuário com permissões somente de email pode criar conteúdo, mas não pode adicionar um email a uma jornada.

### Permissões de entregabilidade de email {#email-deliverability-permissions}

Os recursos de entrega (subdomínios, DMARC, pools de IP, listas de supressão, listas de permissões, planos de aumento de IP e listas de propagação) são configurações no nível do administrador. Eles são regidos por duas permissões que abrangem toda a área **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]**:

| Recurso | Permissão | O que ele permite |
| ---------- | ---------- | -------------- |
| **Exibir configurações de email** | `view-b2b-email-settings` | Exibir subdomínios, registros PTR, pools de IP, lista de supressão, lista de permissões, planos de aumento gradual de IP e listas de propagação (somente leitura). |
| **Gerenciar configurações de email** | `manage-b2b-email-settings` | Todos os subdomínios de acesso de leitura mais delegados, configuração do DMARC, gerenciamento de supressão e listas de permissões, gerenciamento de planos de aquecimento de IP e listas de propagação. |

Alguns sub-recursos nas configurações de email são limitados por sinalizadores adicionais do LaunchDarkly — Lista de supressão (`enable-suppression`), Lista de permissões (`enable-allow-list`), Listas de propagação (`enable-seedlist-ui`). Se um sub-recurso não estiver visível em sua organização, verifique com o representante da Adobe a ativação do sinalizador.

### Permissões de configuração de canal {#channel-configuration-permissions}

As configurações de canal estão em **[!UICONTROL Canais]** → **[!UICONTROL Configurações gerais]**. Eles vinculam primitivos de capacidade de entrega (subdomínio, pool de IP, identidade do remetente) a um objeto reutilizável que os autores do jornada referenciam. Elas são regidas por uma única permissão:

| Recurso | Permissão | O que ele permite |
| ---------- | ---------- | -------------- |
| **Gerenciar configurações de canal** | `manage-b2b-channels-configurations` | Exibir, criar, editar e excluir configurações de canal de email. |

## Visão geral da capacidade de entrega de email {#deliverability-overview}

A capacidade de entrega de emails no Prime [!DNL Journey Optimizer B2B Edition] é o conjunto de configurações de infraestrutura e autenticação que ajudam as mensagens de email a chegar à caixa de entrada do destinatário, não à pasta de spam, e não bloqueadas pelos ISPs (Provedores de Serviços de Internet).

Ele usa os seguintes blocos fundamentais, configurados por um administrador, normalmente na seguinte ordem:

1. Delegar um ou mais subdomínios à Adobe.
1. Configure registros do DMARC, SPF e DKIM em cada subdomínio.
1. Confirme o pool de IPs que enviará emails para o subdomínio.
1. Crie uma ou mais configurações de canal de email que vinculam um subdomínio, pool de IPs e identidade do remetente.
1. Use essas configurações de canal nas ações de email do jornada.

>[!TIP]
>
>Trate a configuração da capacidade de entrega como uma atividade de administrador única por unidade de negócios ou marca. Quando configurados, os profissionais de marketing e autores de email não precisam revisitá-los.

## Delegação de subdomínios {#subdomain-delegation}

A delegação de subdomínio informa à Internet que a Adobe está autorizada a enviar emails em nome de um subdomínio específico (por exemplo, `mail.contoso.com`) do seu domínio. Delegar um subdomínio dedicado — em vez do domínio raiz — protege o e-mail corporativo e resulta em uma

* **Isolamento de reputação.** Os envios de marketing são mantidos separados do correio corporativo. Se a reputação de marketing cair, seu email transacional e corporativo não será afetado.
* **Aquecimento de IP mais rápido.** Subdomínios dedicados ajudam a estabelecer uma reputação positiva do remetente mais rapidamente com ISPs.
* **Autenticação moderna.** O SPF, o DKIM e o DMARC podem ser configurados corretamente por subdomínio sem afetar outros fluxos de email.
* **Conformidade.** Ajuda a atender aos requisitos de remetentes em massa do Gmail, Yahoo e outros principais ISPs.

>[!NOTE]
>
>Cada subdomínio no Prime só pode ser usado por um produto da Adobe. Não é possível compartilhar o mesmo subdomínio de envio entre o Prime e outro produto, como o Adobe Marketo Engage ou o Adobe Campaign — você deve usar subdomínios distintos.

### Métodos compatíveis

O Prime oferece suporte a dois dos três métodos de delegação de subdomínio no Alpha. O terceiro método (delegação personalizada) está no roteiro.

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

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime, navegue até **[!UICONTROL Administração]** → **[!UICONTROL Canais]** → **[!UICONTROL Configurações de email]** → **[!UICONTROL Subdomínios]**.
1. Clique em **[!UICONTROL Configurar subdomínio]**.
1. Insira o nome completo do subdomínio (por exemplo, `mail.contoso.com`).
1. Escolha **[!UICONTROL Totalmente Delegado]** como o método de delegação.
1. Configure o DMARC para o subdomínio (consulte [DMARC, SPF e DKIM](#dmarc-spf-dkim)).

   No mínimo, configure um registro do DMARC com uma política inicial de `none` para que você possa monitorar relatórios sem afetar a entrega.

1. Revise a lista de registros DNS para o Adobe gerenciar.

   Normalmente, eles incluem registros MX, SPF, DKIM, DMARC, A e CNAME (para rastreamento e URLs de mirror page).

1. Baixe os registros DNS como um arquivo CSV usando o botão **[!UICONTROL Baixar registros]**. Compartilhe este arquivo com a equipe de DNS.

1. A equipe de DNS adiciona os registros NS na solução de hospedagem de domínio que delega o subdomínio à Adobe.

1. Depois que sua equipe de DNS confirmar que os registros estão em vigor, volte para o Prime [!DNL Journey Optimizer B2B Edition] e marque a caixa confirmando que você criou os registros necessários no site de hospedagem.

1. Clique em **[!UICONTROL Enviar]** para iniciar uma série de verificações de validação (pré-validação, MX, SPF, DKIM, DMARC, registro FBL).

1. Aguarde o status do subdomínio mudar para **[!UICONTROL Sucesso]**.

   Isso normalmente leva alguns minutos quando a propagação do DNS é concluída.

>[!NOTE]
>
>Se a validação falhar, o status será alterado para **[!UICONTROL Falha]** e o Prime [!DNL Journey Optimizer B2B Edition] exibirá o motivo (por exemplo, registro NS não encontrado, registro MX ausente ou DMARC configurado incorretamente). Corrija o problema de DNS subjacente e tente enviar novamente.

### Delegar um subdomínio (método CNAME) {#delegate-cname}

Use esse método somente se a política DNS da organização proibir a delegação completa. Com o CNAME, você mantém registros de DNS da sua parte.

1. No Prime [!DNL Adobe Journey Optimizer B2B Edition], navegue até **[!UICONTROL Administração]** → **[!UICONTROL Canais]** → **[!UICONTROL Configurações de email]** → **[!UICONTROL Subdomínios]**.
1. Clique em **[!UICONTROL Configurar subdomínio]**.
1. Insira o nome completo do subdomínio.
1. Escolha **[!UICONTROL CNAME]** como o método de delegação.
1. Configure o DMARC para o subdomínio ([DMARC, SPF e DKIM](#dmarc-spf-dkim)).
1. Revise a lista de registros CNAME gerada pelo Prime — eles apontam os componentes do subdomínio para registros gerenciados pela Adobe.
1. Baixe os registros como CSV e compartilhe com a equipe DNS.
1. A equipe de DNS adiciona cada registro CNAME à solução de hospedagem de DNS.
1. Depois que os registros estiverem em vigor e forem propagados, volte para a Prime e confirme. Clique em **[!UICONTROL Enviar]**.
1. Aguarde o status alcançar **[!UICONTROL Sucesso]**.

>[!IMPORTANT]
>
>Com o CNAME, a Adobe não pode ajudar você a alterar, manter ou solucionar problemas do DNS para o subdomínio. Quaisquer alterações futuras, por exemplo, a adição de um novo CNAME para uma atualização de recurso, devem ser feitas pela equipe de DNS.

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

### Modos de política do DMARC

| Política | Ação | Quando usar |
| ------ | ------ | ----------- |
| `none` | Monitorar | O servidor de recebimento não faz nada se o DMARC falhar — mas ainda envia um relatório. Use isso ao delegar um subdomínio pela primeira vez para confirmar se a autenticação está funcionando sem correr o risco de perder a mensagem. |
| `quarantine` | Quarentena | O servidor de recebimento coloca mensagens com falha na pasta spam/lixo eletrônico. |
| `reject` | Rejeitar | O servidor de recebimento rejeita (devolve) mensagens com falha na autenticação. Modo estrito. Recomendado assim que você estiver confiante na configuração da autenticação. |

### Configurar DMARC {#configure-dmarc}

O DMARC é configurado no momento da delegação de subdomínio, mas você também pode adicionar ou atualizar o DMARC para um subdomínio já delegado.

1. Navegue até **[!UICONTROL Administração]** → **[!UICONTROL Canais]** → **[!UICONTROL Configurações de email]** → **[!UICONTROL Subdomínios]**.

1. Na lista Subdomínios, localize o subdomínio e verifique a coluna Registro do DMARC.

   Se um registro estiver ausente, um alerta será exibido.

1. Abra o subdomínio e role até a seção Registro do DMARC.

   * Se um registro DMARC já existir no domínio pai, o Prime [!DNL Journey Optimizer B2B Edition] buscará os valores automaticamente. Você pode mantê-las ou substituí-las.
   * Se não existir nenhum registro, escolha **[!UICONTROL Gerenciar com o Adobe]** e o Adobe criará e hospedará o registro do DMARC.

1. Defina a política: `none`, `quarantine` ou `reject`. Comece com `none` a menos que você já tenha uma postura madura de DMARC em seu domínio pai.

1. (Opcional) Configure as marcas DMARC adicionais (`sp` para política de subdomínio, `pct` para porcentagem, `rua` e `ruf` para endereços de relatório).

1. Se estiver usando Totalmente Delegado, clique em **[!UICONTROL Salvar]**.

   O Adobe aplica o registro automaticamente. Se estiver usando CNAME, copie o registro DNS e peça à sua equipe de DNS para adicioná-lo e, em seguida, confirme-o no Prime [!DNL Journey Optimizer B2B Edition].

1. Aguarde até 48 horas para propagação DNS e verifique se o indicador de status do DMARC na página de subdomínio está verde/íntegro.

>[!TIP]
>
>Comece com `policy=none` para monitorar os relatórios de autenticação, avance para `quarantine` e finalmente para `reject` assim que seus relatórios mostrarem um alinhamento íntegro de SPF e DKIM. Mover diretamente para `reject` sem monitoramento pode fazer com que mensagens legítimas sejam rejeitadas.

## Pools de IP {#ip-pools}

Um pool de IPs é um grupo nomeado de endereços IP usados para enviar seu email. Os pools de IP são essenciais para a reputação do remetente: cada pool tem sua própria reputação com ISPs, portanto, um problema com um pool (por exemplo, um burst de marketing que aciona reclamações de spam) não contamina outro (por exemplo, confirmações transacionais).

### Tipos de pool

| Tipo de pool | Disponibilidade | Descrição |
| --------- | ------------ | ----------- |
| **Pool de IPs compartilhados** | Disponível em Alpha | Um pool de endereços IP gerenciados pela Adobe e compartilhados entre muitos clientes. A reputação é mantida pela Adobe em todo o pool. Melhor para volume de email baixo a médio e clientes que não desejam gerenciar o aumento gradual de IP. |
| **Pool de IPs dedicados** | Roteiro (GA) | Um ou mais endereços IP alocados exclusivamente à sua organização. Você é o dono da reputação. Recomendado para remetentes de alto volume. Inclui planejamento de aquecimento de IP e gerenciamento de registros PTR. |

### Revisar e atribuir um pool de IPs {#review-ip-pool}

Nesta versão, os pools de IP são pré-provisionados para sua organização. Atribua um pool de IP ao criar uma configuração de canal de email.

1. Navegue até **[!UICONTROL Administração]** → **[!UICONTROL Canais]** → **[!UICONTROL Configurações de email]** → **[!UICONTROL Pools de IP]**.
1. Confirme se um pool de IP com o status **[!UICONTROL Ativo]** está disponível para sua organização.
1. Passe o mouse sobre o pool para visualizar os endereços IP e seus registros PTR (DNS reverso).
1. Se sua organização tiver várias unidades de negócios ou marcas, planeje como você usará os pools de IP (por exemplo, pool de marketing versus pool de webinários) antes de criar as configurações de canal.

>[!IMPORTANT]
>
>Não misture tráfego de marketing e transacional no mesmo pool de IPs, mesmo quando o pool compartilhado estiver disponível. A configuração Tipo de email na configuração do canal (Marketing versus Transacional) controla o comportamento de supressão, mas as configurações de canal ainda devem usar pools distintos, quando possível.

## Configurações de canal de email {#email-channel-configurations}

Uma configuração de canal é o objeto central que une a identidade do remetente, o subdomínio, o pool de IPs e as configurações de rastreamento. As ações de email no jornada fazem referência a uma configuração de canal para saber como enviar a mensagem:

* **Canal:** Email.
* **Tipo de email:** Marketing ou Transacional. Essa configuração determina se as regras de supressão se aplicam (Marketing as aplica; Transacional ignora a supressão de reclamação de spam por padrão para mensagens transacionais legítimas).
* **Parâmetros de cabeçalho:** Do nome, Do email, Nome para resposta, Email para resposta, Email para erro.
* **Subdomínio:** o subdomínio delegado usado para envio. O De email deve usar este subdomínio.
* **Pool de IPs:** o pool de IPs usado para entregar a mensagem.
* **Rastreamento de URL:** Habilite ou desabilite o rastreamento de cliques e aberturas; configure o domínio de rastreamento.
* **Marcas:** Marcas para organização e pesquisa.

### Criar uma configuração de canal de email {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Pelo menos um subdomínio deve ser delegado e estar Ativo.
>* Pelo menos um pool de IPs deve ser atribuído à sua organização.
>* Você precisa ter a função Administrador.

1. Navegue até **[!UICONTROL Canais]** → **[!UICONTROL Configurações gerais]** → **[!UICONTROL Configurações de canal]**.
1. Clique em **[!UICONTROL Criar configuração de canal]**.
1. Insira um Nome (por exemplo, &quot;Marketing B2B da Contoso — América do Norte&quot;) e uma Descrição opcional.
1. Selecione o canal de **[!UICONTROL Email]**.
1. Opcionalmente, selecione tags para categorizar a configuração.
1. Na seção **[!UICONTROL Tipo de email]**, escolha Marketing ou Transacional.
1. Na seção **[!UICONTROL Subdomínio]**, selecione um subdomínio delegado anteriormente.
1. Na seção **[!UICONTROL Pool de IPs]**, selecione um pool de IPs Ativo. Você pode passar o mouse sobre os IPs para visualizar registros PTR.
1. Configure os **[!UICONTROL Parâmetros de cabeçalho]**:
   * Do Nome (por exemplo, &quot;Marketing da Contoso&quot;).
   * Do Email — deve usar o subdomínio selecionado (por exemplo, `marketing@mail.contoso.com`).
   * Nome para Resposta e Email para Resposta — o padrão é De, caso esteja em branco.
   * E-mail de erro — endereço que recebe notificações de falha na entrega.
1. Habilite **[!UICONTROL Rastreamento de URL]** e selecione o domínio de rastreamento.
1. Clique em **[!UICONTROL Enviar]**.
1. O Prime executa a validação: status do subdomínio, registro MX, alinhamento SPF/DKIM/DMARC, preparação do pool de IP, registro FBL. A configuração passa por Rascunho → Processamento → Ativo.

>[!NOTE]
>
>Se a validação falhar, a configuração será movida para o status **[!UICONTROL Falha]**. Abra a configuração para exibir o motivo da falha — as causas comuns são falha de validação de registro MX, IPs no pool que não correspondem à configuração ou desalinhamento da DMARC. Resolver e enviar novamente.

### Edição ou exclusão de uma configuração de canal {#edit-channel-configuration}

É possível editar as configurações de canal após a criação, mas com uma restrição importante:

* **Não é possível alterar o canal.** Uma configuração está associada ao seu canal.

Quando você edita uma configuração que está em uso:

* **Para jornadas publicadas:** a alteração é aplicada na próxima recorrência ou execução. As execuções em andamento continuam com as configurações anteriores.
* **Para mensagens transacionais ou em tempo real:** as alterações se propagam dentro de aproximadamente cinco minutos.

Para excluir uma configuração, primeiro remova ou atualize cada ação de email que faz referência a ela. [!DNL Journey Optimizer B2B Edition] A Prime não exclui uma configuração usada atualmente por uma jornada ativa.

### Configurações de vários canais {#multiple-channel-configurations}

A maioria das organizações B2B usa configurações de vários canais para separar marcas, regiões ou tipos de envio. Padrões comuns:

* Uma configuração de marketing separada por unidade de negócios (por exemplo, *Marketing BU-A*, *Marketing BU-B*).
* Uma configuração transacional dedicada com Tipo de email = Transacional para notificações de produto ou contrato.
* Configurações específicas de região usando subdomínios específicos de região (por exemplo, `mail.eu.contoso.com`, `mail.us.contoso.com`) para alinhar com ISPs regionais e conformidade.

>[!TIP]
>
>Nomeie suas configurações com uma convenção clara e estruturada — por exemplo: *[Marca] - [Região] - [Tipo]*. Isso se torna crítico quando você tem uma dúzia ou mais de configurações.

### Limitações conhecidas {#known-limitations}

* **O método de Delegação personalizado** para delegação de subdomínio ainda não está disponível — use Totalmente Delegado ou CNAME. A delegação personalizada está direcionada para disponibilidade geral.
* **Pools de IP dedicados** não estão disponíveis na Alpha. O pool de IPs compartilhados é a única opção. IPs dedicados enviados na GA, incluindo planejamento de aquecimento de IP e gerenciamento de registros PTR.
* **A importação do HTML por meio do upload de .html ou .zip** é limitada no Alpha. A importação completa do HTML — incluindo o editor de código + visualização dupla, validação e conversão automática em linha de CSS — é fornecida na Beta.
* **O carregamento de imagens nativas e o DAM no Prime** (carregar, organizar, editar) estão no roteiro do Beta. Use os ativos do Marketo Design Studio nesta versão. Os recarregamentos no Marketo não são refletidos no Prime.
* **Perfis de teste, Simular conteúdo e Enviar prova** não estão disponíveis nesta versão. A renderização de Litmus e os relatórios de spam baseados no SpamAssassin estão no roteiro do Beta.
* **A personalização em nível de conta e os dados de objeto personalizado** não estão disponíveis nesta versão. Use atributos de perfil.
* A **migração automatizada do Velocity para Handlebars** dos modelos existentes do Marketo é enviada na data de disponibilidade geral.
* **Comentários e colaboração em emails** (comentários incorporados, @mentions, fluxo de trabalho de solicitação-revisão) são enviados na versão de Acompanhamento Rápido.
* As **integrações do AEM Assets, dos Fragmentos de conteúdo do AEM e do Adobe Express** estão no roteiro de Acompanhamento Rápido.

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
