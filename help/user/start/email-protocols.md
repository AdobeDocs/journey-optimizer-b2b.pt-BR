---
title: Protocolos de rastreamento e entrega de email
description: Aprenda a configurar protocolos no Marketo Engage para uso pelo Journey Optimizer B2B Edition para recursos de rastreamento e canal de email.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: ht
source-wordcount: '1798'
ht-degree: 100%

---

# Protocolos de rastreamento e entrega de email

O Adobe Journey Optimizer B2B Edition aproveita as funções de canal de email e rastreamento de eventos no Marketo Engage. Para garantir que a entrega de email funcione conforme o esperado para organizações que usam configurações restritivas de firewall ou servidor proxy, o administrador de sistemas deve adicionar determinados domínios e intervalos de endereços IP à lista de permissões.

>[!NOTE]
>
>Se sua organização já estiver usando a instância conectada do Marketo Engage para executar as operações de marketing, esses protocolos e configurações já deverão estar em vigor.

Verifique se os seguintes domínios (incluindo o asterisco) foram adicionados à lista de permissões para habilitar todos os recursos e web sockets do Marketo Engage:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Siga as seguintes etapas para garantir o rastreamento e a entrega dos emails:

1. [Criar registros DNS para ](#create-dns-records-for-landing-pages-and-email)
1. [Configurar a SPF e o DKIM](#set-up-spf-and-dkim)
1. [Configurar DMARC](#set-up-dmarc)
1. [Configurar registros MX para o seu domínio](#set-up-mx-records-for-your-domain)
1. [Adicionar endereços IP de saída às listas de permissões](#outbound-ip-addresses)

## Criar registros DNS para o <!-- landing pages and -->email

Conectar um registro CNAME permite que os profissionais de marketing hospedem versões web de emails, páginas de destino e blogs com uma marca consistente que melhora o tráfego e as conversões. É altamente recomendável que você adicione os CNAMEs ao seu host de domínio raiz para que o Marketo Engage hospede seus ativos da web focados em marketing. Como administrador, você deve trabalhar com sua equipe de marketing para planejar e implementar um registro CNAME para os links de rastreamento incluídos nos emails enviados pelo Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Adicionar o CNAME para links de rastreamento de email

Adicione o CNAME do email para que o `[YourEmailCNAME]` aponte para `[MktoTrackingLink]`, que é o link de rastreamento padrão atribuído pelo Marketo Engage, no formato:

`[YourEmailCNAME].[YourDomain].com` NO CNAME `[MktoTrackingLink]`

Por exemplo:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>O valor `[MktoTrackingLink]` deve ser o Domínio de marca padrão.

### Provisionar o certificado SSL

Entre em contato com o [Suporte da Adobe](https://experienceleague.adobe.com/home?lang=pt-br&amp;support-tab=home#support){target="_blank"} para iniciar o processo de provisionamento de um Certificado SSL.

Esse processo pode levar até três dias úteis para ser concluído.

## Configurar a SPF e o DKIM

Sua equipe de marketing deve fornecer as informações de DKIM (Domain Keys Identified Mail) a serem adicionadas ao seu registro de recursos DNS. Siga estas etapas para configurar o DKIM e a SPF (Estrutura de Política do Remetente) e notifique a equipe de Marketing quando ela for atualizada.

1. Para configurar a SPF, adicione a seguinte linha às entradas de DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Se você já tiver um registro SPF na entrada DNS, basta adicionar o seguinte a ele:

   ```
   include: mktomail.com
   ```

   Substitua `CompanyDomain` pelo domínio principal do site (como `company.com/`) e `CorpIP` pelo endereço IP do servidor de email corporativo (como `255.255.255.255`). Se você planeja enviar emails de vários domínios por meio do Marketo Engage, adicione esta linha para cada domínio (em uma linha).

1. Para o DKIM, crie registros de recursos DNS para cada domínio.

   Adicione os registros de host e os valores TXT para cada domínio:

   `[DKIMDomain1]`: o Registro do Host é `[HostRecord1]` e o Valor TXT é `[TXTValue1]`.

   `[DKIMDomain2]`: o Registro do Host é `[HostRecord2]` e o Valor TXT é `[TXTValue2]`.

   Copie o `HostRecord` e `TXTValue` para cada domínio DKIM após seguir as [instruções](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} na documentação do Marketo Engage. Você pode verificar os domínios no Journey Optimizer B2B Edition (consulte [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configurar DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um protocolo de autenticação usado para ajudar organizações a proteger seus domínios contra uso não autorizado. Ele estende os protocolos de autenticação existentes, como SPF e DKIM, para informar os servidores destinatários sobre as ações a serem tomadas caso ocorra uma falha de autenticação em seu domínio. O DMARC é opcional, mas é altamente recomendado porque ajuda a proteger sua marca e reputação. Grandes provedores, como Google e Yahoo, começaram a exigir o uso do DMARC para remetentes em massa a partir de fevereiro de 2024.

Para que o DMARC funcione, você deve ter pelo menos um dos seguintes registros DNS TXT:

* Uma SPF válida
* Um registro DKIM válido para o seu FROM: domínio (recomendado para Marketo Engage e Journey Optimizer B2B Edition)

Você também deve ter um registro DNS TXT específico do DMARC para seu domínio `FROM:`. Como opção, você pode definir um endereço de email que especifique para onde os relatórios DMARC devem ir na sua organização para monitoramento de relatórios.

### Exemplo de fluxo de trabalho DMARC

>[!TIP]
>
>É uma prática recomendada implementar o DMARC como uma _implementação lenta_. Aumente sua política DMARC de `p=none` para `p=quarantine` e depois para `p=reject` conforme você entende o impacto potencial e defina sua política DMARC para alinhamento flexível na SPF e no DKIM.

Se você receber relatórios DMARC, faça o seguinte:

1. Use `p=none` e analise o feedback e os relatórios que você receber. Os relatórios informam ao destinatário para não executar nenhuma ação em mensagens com falha na autenticação e enviam relatórios por email ao remetente.

   * Se mensagens legítimas estiverem com falha na autenticação, revise e corrija os problemas com a SPF ou o DKIM.

   * Determine se a SPF ou o DKIM estão alinhados e autenticando todos os emails legítimos.

   * Revise os relatórios para garantir que os resultados sejam os esperados com base em suas políticas de SPF/DKIM.

1. Ajuste a política para `p=quarantine`, que informa ao servidor de email receptor para colocar em quarentena os emails com falha na autenticação (normalmente colocando essas mensagens na pasta de spam).

   Revise os relatórios para garantir que os resultados sejam o esperado.

1. Se estiver satisfeito com o comportamento das mensagens no nível `p=quarantine`, você pode ajustar a política para (`p=reject`).

   A política de rejeição informa ao destinatário para negar (devolver) qualquer email do domínio com falha na autenticação. Com essa política habilitada, somente emails verificados como 100% autenticados pelo seu domínio terão chance de serem colocados na caixa de entrada.

   >[!CAUTION]
   >
   >Use esta política com cautela e determine se ela é apropriada para sua organização.

### Relatórios do DMARC

O DMARC oferece a capacidade de receber relatórios sobre emails com falham na SPF/DKIM. Há dois relatórios diferentes gerados pelos serviços de ISP como parte do processo de autenticação. Os remetentes podem receber esses relatórios por meio das tags RUA/RUF em sua política DMARC.

* **Relatórios agregados (RUA)**: não contêm PII (informação de identificação pessoal) que possa ser sensível ao RGPD (Regulamento Geral sobre a Proteção de Dados).

* **Relatórios forenses (RUF)**: contém endereços de email que são sensíveis ao RGPD. Antes de implementar este relatório, verifique sua política organizacional para lidar com informações que precisam estar em conformidade com o RGPD.

O principal uso desses relatórios é receber uma visão geral dos emails que são tentativas de falsificação. São relatórios altamente técnicos e são melhor assimilados por meio de uma ferramenta de terceiros.

### Exemplo de registros do DMARC

* Registro mínimo: `v=DMARC1; p=none`

* Registro que direciona para um endereço de email para receber relatórios: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Tags do DMARC

Os registros do DMARC têm vários componentes chamados _Tags do DMARC_. Cada tag tem um valor que especifica um determinado aspecto do DMARC.

| Nome da tag | Usar | Função | Exemplo | Valor padrão |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obrigatório | Especifica a versão. Existe apenas uma versão, portanto ela tem um valor fixo de `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obrigatório | Especifica a política DMARC, que instrui o destinatário a relatar, colocar em quarentena ou rejeitar emails que não passam nas verificações de autenticação. | `p=none`, `p=quarantine` ou `p=reject` | - |
| `fo` | Opcional | Permite que o proprietário do domínio especifique opções de relatórios. | `0`: gerar relatório se SPF e DKIM apresentarem falha <br> `1`: gerar relatório se SPF ou DKIM apresentar falha <br> `d`: gerar relatório se o DKIM falhar <br> `s`: gerar relatório se a SPF falhar | `1` (recomendado para relatórios do DMARC) |
| `pct` | Opcional | Especifica a porcentagem de mensagens sujeitas à filtragem. | `pct=20` | `100` |
| `rua` | Opcional (recomendado) | Designa onde os relatórios agregados são entregues. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Opcional (recomendado) | Designa onde os relatórios forenses são entregues. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Opcional | Especifica a política do DMARC para subdomínios do domínio principal. | `sp=reject` | - |
| `adkim` | Opcional | Especifica um alinhamento estrito (`s`) ou simples (`r`). Alinhamento simples significa que o domínio é usado na assinatura do DKIM e pode ser um subdomínio do endereço `From:`. Alinhamento estrito significa que o domínio é usado na assinatura do DKIM e deve ser uma correspondência exata do domínio usado no endereço `From:`. | `adkim=r` | `r` |
| `aspf` | Opcional | Pode ser estrito (`s`) ou simples (`r`). Modo simples significa que o domínio Return-Path pode ser um subdomínio do endereço `From:`. Modo estrito significa que o domínio Return-Path deve ter uma correspondência exata com o endereço `From:`. | `aspf=r` | `r` |

Para obter informações detalhadas sobre o DMARC e todas as suas opções, consulte [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementação do DMARC para Marketo Engage

Há dois tipos de alinhamento para o DMARC:

* Alinhamento ao **DKIM** (Domain Keys Identified Mail): o domínio especificado no cabeçalho `From:` de um email corresponde à assinatura DKIM. A assinatura do DKIM contém um valor `d=` no qual o domínio é especificado para correspondência com o domínio de cabeçalho `From:`.

  O alinhamento do DKIM valida se o remetente está autorizado a enviar emails do domínio e verifica se nenhum conteúdo foi alterado durante o trânsito do email. Para implementar o DMARC alinhado ao DKIM:

   * Configure o DKIM para o domínio MAIL FROM da mensagem. Use as [instruções](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} na documentação do Marketo Engage.

   * Configure o DMARC para o domínio DKIM MAIL FROM.

  >[!NOTE]
  >
  >O alinhamento do DKIM é recomendado para o Marketo Engage.

* Alinhamento à **SPF** (Estrutura de Política do Remetente): o domínio no cabeçalho `From:` deve corresponder ao domínio no cabeçalho Return-Path:. Se ambos os domínios DNS forem iguais, a SPF corresponderá (se alinhará) e dará um resultado de aprovação. Para implementar o DMARC alinhado à SPF:

   * Configure o domínio Return-Path com marca.

      * Configure o registro SPF apropriado.
      * Altere o registro MX para apontar de volta para o MX padrão do datacenter do qual seu email é enviado

   * Configure o DMARC para o domínio Return-Path com marca.

  >[!NOTE]
  >
  >O alinhamento estrito da SPF não é compatível ou recomendado para o Marketo Engage.

### IPs dedicados e pool compartilhado

Se você enviar emails pelo Marketo Engage por um IP dedicado e não tiver implementado um caminho return-path com marca (ou se não tiver certeza), abra um tíquete com o [Suporte da Adobe](https://experienceleague.adobe.com/home?lang=pt-br&amp;support-tab=home#support){target="_blank"}.

IPs confiáveis são um conjunto compartilhado de IPs reservados para usuários de baixo volume que enviam menos de 75 mil mensagens por mês e não se qualificam para um IP dedicado. Esses usuários também devem atender aos requisitos de prática recomendada.

* Se você estiver enviando emails pelo Marketo Engage usando um pool compartilhado de IPs, poderá verificar se você se qualifica para IPs confiáveis [inscrevendo-se no programa de intervalo de envio de IP confiável](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. O return-path com marca é incluído ao enviar de IPs confiáveis do Marketo Engage. Se aprovado para este programa, entre em contato com o Suporte da Adobe para configurar o return-path com marca.

* Se você enviar mais de 100.000 mensagens por mês e quiser enviar emails pelo Marketo Engage usando IPs compartilhados, entre em contato com a equipe de contas da Adobe (seu gerente de conta) para adquirir um IP dedicado.

## Configurar registros MX para o seu domínio

Um registro MX permite que você receba emails no domínio de onde está enviando os emails para processar respostas e respostas automáticas. Se estiver enviando do seu domínio corporativo, ele provavelmente já está configurado. Caso contrário, geralmente é possível configurá-lo para mapear para o registro MX do domínio corporativo.

## Endereços IP de saída

Uma conexão de saída é aquela feita pelo Marketo Engage a um servidor na Internet em seu nome. Sua organização de TI e alguns parceiros/fornecedores podem usar listas de permissões para restringir o acesso aos servidores. Nesse caso, você deve fornecer a eles blocos de endereços IP de saída do Marketo Engage para adicionar às suas listas de permissão.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blocos de endereço IP de saída

As listas a seguir abrangem todos os servidores do Marketo Engage que fazem chamadas de saída. Consulte estas listas para configurar uma lista de permissões de IP, servidor, firewall, lista de controle de acesso, grupo de segurança ou serviço de terceiros para receber conexões de saída do Marketo Engage.

| Bloco de IP (Notação CIDR) | Endereço IP individual |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
