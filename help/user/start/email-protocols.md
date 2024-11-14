---
title: Protocolos de rastreamento e entrega de email
description: Saiba como configurar protocolos no Marketo Engage para serem usados pelo Journey Optimizer B2B edition para rastreamento e recursos de canal de email.
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protocolos de rastreamento e entrega de email

O Adobe Journey Optimizer B2B edition aproveita as funções de canal de email e o rastreamento de eventos no Marketo Engage. Incluir na lista de permissões Para garantir que o delivery de email funcione conforme o esperado em organizações que usam configurações restritivas de firewall ou servidor proxy, um administrador de sistemas deve adicionar determinados domínios e intervalos de endereços IP ao arquivo.

>[!NOTE]
>
>Se sua organização já estiver usando a instância do Marketo Engage conectado para executar suas operações de marketing, esses protocolos e configurações já deverão estar em vigor.

Verifique se os seguintes domínios (incluindo o asterisco) foram adicionados ao incluo na lista de permissões para ativar todos os recursos de Marketo Engage e soquetes da Web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Siga as etapas a seguir para garantir o rastreamento e o delivery de email:

1. [Criar registros DNS para ](#create-dns-records-for-landing-pages-and-email)
1. [Configurar SPF e DKIM](#set-up-spf-and-dkim)
1. [Configurar o DMARC](#set-up-dmarc)
1. [Configurar registros MX para o seu domínio](#set-up-mx-records-for-your-domain)
1. [Adicionar endereços IP de saída às listas de permissões](#outbound-ip-addresses)

## Criar registros DNS para o email <!-- landing pages and -->

A conexão de um registro CNAME permite que os profissionais de marketing hospedem versões da Web de emails, páginas de aterrissagem e blogs com marca consistente que melhora o tráfego e as conversões. É altamente recomendável adicionar os CNAMEs ao host do domínio raiz para que o Marketo Engage hospede seus ativos da Web com foco em marketing. Como administrador, você deve trabalhar com sua equipe de marketing para planejar e implementar um registro CNAME para os links de rastreamento incluídos nos emails enviados pelo Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Adicionar o CNAME para links de rastreamento de email

Adicione o CNAME do email para que `[YourEmailCNAME]` aponte para `[MktoTrackingLink]`, que é o link de rastreamento padrão atribuído para o Marketo Engage, no formato:

`[YourEmailCNAME].[YourDomain].com` NO CNAME `[MktoTrackingLink]`

Por exemplo:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>O valor `[MktoTrackingLink]` deve ser o Domínio de Marca Padrão.

### Provisionar o certificado SSL

Contate o [Suporte de Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"} para iniciar o processo de provisionamento de um Certificado SSL.

Esse processo pode levar até três dias úteis para ser concluído.

## Configurar SPF e DKIM

Sua equipe de marketing deve fornecer as informações de DKIM (Domain Keys Identified Mail, Chaves de domínio identificadas) a serem adicionadas ao registro de recurso DNS. Siga estas etapas para configurar o DKIM e o SPF (Estrutura de política do remetente) e notifique a equipe de marketing quando ela for atualizada.

1. Para configurar o SPF, adicione a seguinte linha nas entradas DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Se você já tiver um registro SPF existente na entrada DNS, basta adicionar o seguinte a ele:

   ```
   include: mktomail.com
   ```

   Substitua `CompanyDomain` pelo domínio principal do site (como `company.com/`) e `CorpIP` pelo endereço IP do servidor de email corporativo (como `255.255.255.255`). Se você planeja enviar emails de vários domínios por meio do Marketo Engage, adicione esta linha para cada domínio (em uma linha).

1. Para DKIM, crie registros de recursos DNS para cada domínio.

   Adicione os registros de host e os valores TXT para cada domínio:

   `[DKIMDomain1]`: O Registro do Host é `[HostRecord1]` e o Valor TXT é `[TXTValue1]`.

   `[DKIMDomain2]`: O Registro do Host é `[HostRecord2]` e o Valor TXT é `[TXTValue2]`.

   Copie os `HostRecord` e `TXTValue` para cada domínio DKIM depois de seguir as [instruções](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} na documentação do Marketo Engage. Você pode verificar os domínios no Journey Optimizer B2B edition (consulte [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configurar o DMARC

O DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um protocolo de autenticação usado para ajudar as organizações a proteger seu domínio contra o uso não autorizado. Ele estende os protocolos de autenticação existentes, como SPF e DKIM, para informar aos servidores recipients sobre as ações a serem tomadas se ocorrer uma falha de autenticação em seus domínios. O DMARC é opcional, mas é altamente recomendado porque ajuda a proteger sua marca e reputação. Os principais provedores, como Google e Yahoo, começaram a exigir o uso do DMARC para remetentes em massa a partir de fevereiro de 2024.

Para que o DMARC funcione, você deve ter pelo menos um dos seguintes registros TXT de DNS:

* Um SPF válido
* Um registro DKIM válido para o domínio FROM: (recomendado para Marketo Engage e Journey Optimizer B2B edition)

Você também deve ter um registro TXT de DNS específico da DMARC para o domínio `FROM:`. Como opção, você pode definir um endereço de email que especifique para onde os relatórios do DMARC devem ir em sua organização para o monitoramento de relatórios.

### Exemplo de fluxo de trabalho do DMARC

>[!TIP]
>
>É uma prática recomendada implementar o DMARC como uma _implantação lenta_. Escalone sua política do DMARC de `p=none` para `p=quarantine` e, em seguida, para `p=reject` à medida que você entender o impacto potencial, e defina sua política do DMARC para um alinhamento mais leve no SPF e no DKIM.

Se você receber relatórios do DMARC, faça o seguinte:

1. Use o `p=none` e analise os comentários e relatórios recebidos. Os relatórios informam o destinatário a não executar nenhuma ação em relação a mensagens com falha de autenticação e a enviar relatórios de email ao remetente.

   * Se mensagens legítimas estiverem falhando na autenticação, revise e corrija os problemas com o SPF/DKIM.

   * Determine se o SPF ou o DKIM estão alinhados e transmita a autenticação para todos os emails legítimos.

   * Revise os relatórios para garantir que os resultados sejam os esperados com base em suas políticas SPF/DKIM.

1. Ajuste a política para `p=quarantine`, que instrui o servidor de email de recebimento a colocar em quarentena emails com falha de autenticação (normalmente colocando essas mensagens na pasta de spam).

   Revise os relatórios para garantir que os resultados sejam o que você espera.

1. Se você estiver satisfeito com o comportamento das mensagens no nível `p=quarantine`, poderá ajustar a política para (`p=reject`).

   A política de rejeição informa ao destinatário para negar (devolver) qualquer email para o domínio que apresenta falha de autenticação. Com essa política ativada, somente os emails verificados como 100% autenticados pelo seu domínio terão chance de serem inseridos na caixa de entrada.

   >[!CAUTION]
   >
   >Use essa política com cuidado e determine se é apropriada para sua organização.

### Relatórios do DMARC

O DMARC oferece a capacidade de receber relatórios sobre emails com falha no SPF/DKIM. Há dois relatórios diferentes gerados pelos serviços de ISP como parte do processo de autenticação. Os remetentes podem receber esses relatórios por meio das tags RUA/RUF em sua política da DMARC.

* **Relatórios de Agregação (RUA)**: não contém nenhum PII (Informações de Identificação Pessoal) que possa ser sensível ao GDPR (Regulamento Geral sobre a Proteção de Dados).

* **Relatórios Forenses (RUF)** - Contém endereços de email que diferenciam o GDPR. Antes de implementar este relatório, verifique sua política organizacional para lidar com informações que precisam ser compatíveis com o GDPR.

O principal uso desses relatórios é receber uma visão geral dos emails que são tentados de falsificação. São relatórios altamente técnicos e melhor assimilados por meio de uma ferramenta de terceiros.

### Exemplo de registros do DMARC

* Registro mínimo: `v=DMARC1; p=none`

* Registro que direciona para um endereço de email para receber relatórios: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Tags do DMARC

Os registros DMARC têm vários componentes chamados _marcas DMARC_. Cada tag tem um valor que especifica um determinado aspecto do DMARC.

| Nome da tag | Usar | Função | Exemplo | Valor padrão |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obrigatório | Especifica a versão. Há apenas uma versão, portanto, ela tem um valor fixo de `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obrigatório | Especifica a política do DMARC, que direciona o destinatário para relatar, colocar em quarentena ou rejeitar emails que não passaram nas verificações de autenticação. | `p=none`, `p=quarantine` ou `p=reject` | - |
| `fo` | Opcional | Permite que o proprietário do domínio especifique opções de relatório. | `0`: gerar relatório se SPF e DKIM falharem <br> `1` - Gerar relatório se o SPF ou o DKIM falhar <br> `d` - Gerar relatório se o DKIM falhar <br> `s` - Gerar relatório se o SPF falhar | `1` (recomendado para relatórios do DMARC) |
| `pct` | Opcional | Especifica a porcentagem de mensagens sujeitas à filtragem. | `pct=20` | `100` |
| `rua` | Opcional (recomendado) | Designa onde os relatórios agregados são entregues. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Opcional (recomendado) | Determina onde os relatórios forenses são entregues. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Opcional | Especifica a política do DMARC para subdomínios do domínio pai. | `sp=reject` | - |
| `adkim` | Opcional | Especifica um alinhamento estrito (`s`) ou relaxado (`r`). Alinhamento simples significa que o domínio é usado na assinatura DKIM e pode ser um subdomínio do endereço `From:`. Alinhamento estrito significa que o domínio é usado na assinatura DKIM e deve corresponder exatamente ao domínio usado no endereço `From:`. | `adkim=r` | `r` |
| `aspf` | Opcional | Pode ser estrito (`s`) ou relaxado (`r`). Modo relaxado significa que o domínio Return-Path pode ser um subdomínio do endereço `From:`. Modo estrito significa que o domínio Return-Path deve ter uma correspondência exata com o endereço `From:`. | `aspf=r` | `r` |

Para obter informações detalhadas sobre a DMARC e todas as suas opções, consulte [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementação do DMARC para Marketo Engage

Há dois tipos de alinhamento para o DMARC:

* Alinhamento de **DKIM** (Domain Keys Identified Mail): o domínio especificado no cabeçalho `From:` de um email corresponde à Assinatura DKIM. A assinatura DKIM contém um valor `d=`, em que o domínio é especificado para correspondência com o domínio de cabeçalho `From:`.

  O alinhamento DKIM valida se o remetente está autorizado a enviar emails do domínio e verifica se nenhum conteúdo foi alterado durante o trânsito do email. Para implementar o DMARC alinhado ao DKIM:

   * Configure o DKIM para o domínio MAIL FROM da mensagem. Use as [instruções](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} na documentação do Marketo Engage.

   * Configure o DMARC para o domínio DKIM MAIL FROM.

  >[!NOTE]
  >
  >O alinhamento DKIM é recomendado para o Marketo Engage.

* Alinhamento de **SPF** (Estrutura de Política do Remetente): o domínio no cabeçalho `From:` deve corresponder ao domínio no cabeçalho Return-Path:. Se ambos os domínios DNS forem iguais, o SPF corresponderá (se alinhará) e dará um resultado de aprovação. Para implementar o DMARC alinhado ao SPF:

   * Configure o domínio Return-Path com marca.

      * Configure o registro SPF apropriado.
      * Altere o registro MX para apontar de volta para o MX padrão do data center do qual seu email é enviado

   * Configure o DMARC para o domínio Return-Path com marca.

  >[!NOTE]
  >
  >Alinhamento SPF estrito não é suportado ou recomendado para o Marketo Engage.

### IPs dedicados e pool compartilhado

Se você enviar emails por Marketo Engage em um IP dedicado e não tiver implementado um caminho de retorno com marca (ou não tiver certeza se o fez), abra um tíquete com [Suporte para Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

IPs confiáveis são um pool compartilhado de IPs reservados para usuários de volume inferior que enviam menos de 75 mil por mês e não se qualificam para um IP dedicado. Esses usuários também devem atender aos requisitos das práticas recomendadas.

* Se você estiver enviando emails por meio do Marketo Engage usando um pool compartilhado de IPs, poderá verificar se está qualificado para IPs Confiáveis [solicitando o programa de intervalo de envio de IPs Confiáveis](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. O caminho de retorno da marca é incluído ao enviar de IPs confiáveis de Marketo Engage. Se aprovado para este programa, entre em contato com o Suporte do Adobe para configurar o caminho de retorno da marca.

* Se você enviar mais de 100.000 mensagens por mês e quiser enviar um email por meio do Marketo Engage usando IPs compartilhados, entre em contato com a Equipe da conta do Adobe (seu gerente de conta) para comprar um IP dedicado.

## Configurar registros MX para o seu domínio

Um registro MX permite receber emails do domínio do qual você está enviando email para processar respostas e respostas automáticas. Se estiver enviando do domínio corporativo, provavelmente ela já está configurada. Caso contrário, geralmente é possível configurá-lo para mapear para o registro MX do domínio corporativo.

## Endereços IP de saída

Uma conexão de saída é feita por Marketo Engage a um servidor na Internet em seu nome. Sua organização de TI e alguns parceiros/fornecedores podem usar as listas de permissões para restringir o acesso aos servidores. Em caso positivo, você deve fornecer a eles blocos de endereço IP de saída Marketo Engage para adicionar às suas incluis na lista de permissões.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blocos de endereço IP de saída

As listas a seguir abrangem todos os servidores Marketo Engage que fazem chamadas de saída. Consulte estas listas para configurar um incluo na lista de permissões IP, servidor, firewall, lista de controle de acesso, grupo de segurança ou serviço de terceiros para receber conexões de saída do Marketo Engage.

| Bloco IP (Notação CIDR) | Endereço IP individual |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
