---
title: Configuração de email
description: Configure opções do Marketo Engage para delivery de email B2B do Journey Optimizer, incluindo padrões, cancelamento de inscrição, visualização da Web, limites de objetos do Velocity, cabeçalhos de rastreamento e filtragem de bot.
feature: Setup, Channels
role: Admin
exl-id: 5b28d8f2-a3a4-420a-ab03-d1115cf3ab61
source-git-commit: 0a9cff812d0631a34a09cca059ffb8496248c2b4
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 83%

---

# Configuração de email

Para oferecer suporte à infraestrutura de delivery de email fornecida pela instância do Marketo Engage anexada, defina as seguintes opções de email. Um administrador de produto do Marketo Engage pode definir essas configurações navegando até a área **[!UICONTROL Administrador]** na instância do Marketo Engage e selecionando **[!UICONTROL Email]**.

## Configurações de email

Para configurar valores padrão de email para a instância do Marketo Engage anexada, altere os valores configurados para refletir o uso por sua organização de marketing.

### Do email e rótulo

Altere os valores do email de origem e do rótulo para que novos emails sejam preenchidos automaticamente com esses valores padrão.

>[!NOTE]
>
>A alteração é aplicável somente aos emails criados por você e não a outros usuários do Marketo Engage ou do Journey Optimizer B2B edition.

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. No painel _[!UICONTROL Configurações]_, digite os valores padrão desejados para **[!UICONTROL Do Email]** e **[!UICONTROL Do Rótulo]**.

   ![Configurações de email - Do email e dos valores padrão do rótulo](./assets/me-admin-email-settings-from.png){width="500"}

1. Clique em **[!UICONTROL Salvar alterações]**.

### Cancelar inscrição de mensagens

Para emails de marketing não operacionais, o texto de cancelamento de inscrição e os links são anexados na parte inferior. Como administrador de produto, você deve configurar o HTML padrão e o texto que é preenchido quando um profissional de marketing não marca o email como operacional.

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. No painel _[!UICONTROL Configurações]_, digite os valores padrão desejados para **[!UICONTROL Cancelar inscrição do HTML]** e **[!UICONTROL Cancelar inscrição do texto]**.

   >[!TIP]
   >
   >Os profissionais de marketing podem alterar a posição do HTML de cancelamento de inscrição em seus emails usando tokens do sistema.

   ![Configurações de email - Cancelar inscrição do HTML e cancelar inscrição de valores padrão de texto](./assets/me-admin-email-settings-unsubscribe.png){width="500"}

   >[!CAUTION]
   >
   >As variáveis a seguir são críticas. **Não exclua** eles.
   >
   >* `%mkt_opt_out_prefix%`
   >* `mkt_unsubscribe=1&mkt_tok=##MKT_TOK##`

1. Clique em **[!UICONTROL Salvar alterações]**.

Se você precisar reverter para o conteúdo padrão do sistema, copie e cole o seguinte:

+++ Texto de cancelamento de inscrição padrão do sistema

```
<p><font face="Verdana" size="1">If you no longer wish to receive these emails, click on the following link: <a href="%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##">Unsubscribe</a><br/></font></p>` [!UICONTROL Unsubscribe Text]:
%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##
```

+++

### Exibir como página da Web

O conteúdo de email tem recursos de exibição limitados (CSS limitado e sem JavaScript ou formulários). Os profissionais de marketing podem usar a opção _Exibir como página da Web_ para aplicar um cookie ao destinatário de email usando o Marketo Munchkin. Como administrador de produto, você deve configurar o HTML padrão e o texto que é preenchido quando um profissional de marketing escolhe essa opção.

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. No painel _[!UICONTROL Configurações]_, altere o conteúdo dos campos **[!UICONTROL Exibir como HTML da Página da Web]** e **[!UICONTROL Exibir como Texto da Página da Web]** para refletir seu tom e suas mensagens.

   ![Configurações de email - Exibir como HTML da Página da Web e Exibir como Valores padrão de Texto da Página da Web](./assets/me-admin-email-settings-view-as-web-page.png){width="500"}

   >[!CAUTION]
   >
   >As variáveis a seguir são críticas. **Não exclua** eles.
   >
   >`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
   >
   >A segunda parte `##MKT_TOK##` é o cookie Munchkin dessa pessoa. Ele garante que os cookies sejam aplicados adequadamente quando o recipient do email clicar no link.
   >
   >Evite:
   >
   >* Adicionar URLs adicionais a qualquer uma das caixas do HTML
   >* Inserção do HTML na versão de texto

1. Clique em **[!UICONTROL Salvar alterações]**.

Se você precisar reverter para o conteúdo padrão do sistema, copie e cole o seguinte:

+++ HTML de página da Web padrão do sistema

```
<div style="text-align: center"><font face="Verdana" size="1">To view this email as a web page, <a href="%mkt_webview_url%?mkt_tok=##MKT_TOK##">click here</a></font></div>
```

+++

+++ Texto da página da Web padrão do sistema

```
To view this email as a web page, go to the following address:
`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
```

+++

## Limites de recuperação de objeto personalizado

Se você usar [!DNL Velocity Script] para exibir dados de objetos personalizados em emails, ajuste o limite de recuperação de objetos personalizados pai. Por padrão, o limite permite acesso a 10 objetos personalizados principais do Velocity Script. Você pode aumentar esse limite, se necessário.

[[!DNL Apache Velocity]](https://velocity.apache.org/) é uma linguagem criada em [!DNL Java] que foi projetada para modelagem e script de conteúdo HTML. A infraestrutura de email do Marketo Engage é compatível com seu uso no contexto de emails por meio de tokens de script, que fornecem acesso aos dados armazenados em objetos personalizados.

Você pode fazer referência a objetos personalizados pai e filho que estão diretamente conectados ao cliente potencial ou contato, mas não a objetos personalizados de terceiro nível. Para cada objeto personalizado, os 10 registros atualizados mais recentes por pessoa/contato estão disponíveis no tempo de execução e são ordenados da atualização mais recente (às `0`) para a atualização mais antiga (às `9`).

_Para alterar o limite :_

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. Role até o painel _[!UICONTROL Limites de Recuperação de Objeto Personalizados]_ e insira um novo valor no **[!UICONTROL Limite de Recuperação Pai]**
campo.

   ![Administrador de email do Marketo Engage - Valores padrão de Limites de Recuperação de Objeto Personalizado](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   Valores de 10 a 100 são suportados. O _[!UICONTROL Limite de Recuperação do Filho]_ é definido automaticamente ao dividir 1000 pelo limite do pai. Por exemplo, se você definir o limite pai como 50, o limite filho será calculado como 20 (1000 ÷ 50 = 20).

1. Clique em **[!UICONTROL Salvar alterações]**.

## Opções de cabeçalho personalizado

Altere as _[!UICONTROL Opções de Cabeçalho Personalizadas]_ para email para configurar cabeçalhos de link de rastreamento de email. Habilite essas opções para implementar links de rastreamento seguro usando HTTPS com Transporte Restrito.

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. Role até o painel _[!UICONTROL Opções de cabeçalho personalizadas]_ e altere a configuração de acordo com as políticas do link de rastreamento:

   ![Administrador de email do Marketo Engage - Configurações padrão das Opções de Cabeçalho Personalizado](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   * **[!UICONTROL Segurança de Transporte Restrita]** - Defina esta opção como Habilitada para garantir que os links de rastreamento sejam sempre servidos por HTTPS (só deve ser definida para assinaturas com links de rastreamento protegidos por SSL).
   * **[!UICONTROL Idade máxima]** - este campo oferece suporte à diretiva obrigatória para especificar o tempo, em segundos, que o navegador deve lembrar para acessar somente o domínio por HTTPS.
   * **[!UICONTROL IncludeSubDomains]** - Use esta opção para incluir a diretiva que aplica a diretiva HSTS a todos os subdomínios do host.

   >[!IMPORTANT]
   >
   >Revise essas configurações com sua equipe de TI para garantir que elas estejam alinhadas às políticas de sua organização. Configurações incorretas podem impedir que alguns visitantes acessem seus links de email.

1. Clique em **[!UICONTROL Salvar alterações]**.

## Filtrar atividade de bot de email {#filter-email-bots}

A atividade de bot de email, também chamada de interações não humanas (NHI), pode aumentar os dados de _aberturas_ e _cliques_ do email, distorcendo suas métricas de envolvimento e acionando a progressão da jornada com base em eventos. Use a filtragem de bot por email para manter a integridade das métricas e insights de envolvimento de cliques. Há dois métodos para identificar atividades suspeitas de bot:

* _&#x200B;**[!UICONTROL Corresponder com a Lista de bot IAB]**&#x200B;_ - Atividades que correspondem a qualquer item na [Lista de bot do Interative Advertising Bureau](https://www.iab.com/guidelines/iab-abc-international-spiders-bots-list/){target="_blank"} (Agente do usuário/endereço IP) são marcadas como bots.
* _&#x200B;**[!UICONTROL Corresponder com Padrão de Proximidade]**&#x200B;_ - Duas ou mais atividades que ocorrem ao mesmo tempo (em menos de um segundo) são identificadas como bots. Os atributos considerados durante a comparação são:
   * ID do lead (deve ser o mesmo)
   * Ativo de email (deve ser o mesmo)
   * Clique em links ou e-mail aberto

Para atividades de clique em links de email e abertura de email, os atributos são preenchidos com os seguintes valores:

* Atividades identificadas como bots - _Atividade de Bot_ = `true` e _Padrão de Atividade de Bot_ = padrão/método identificado
* Atividades identificadas como não bots - _Atividade de Bot_ = `false` e _Padrão de Atividade de Bot_ = `n/a`

### Definir os filtros

1. Vá para a área **[!UICONTROL Administrador]** na instância do Marketo Engage anexada e selecione **[!UICONTROL Email]**.

1. Selecione a guia **[!UICONTROL Atividade de bot]**.

   ![Administrador de email do Marketo Engage - guia Atividade de bot](./assets/me-admin-email-bot-activity.png){width="700" zoomable="yes"}

   O painel Identificação da atividade de bot exibe dois controles deslizantes que você pode usar para identificar a atividade de bot.

1. Alterne o controle deslizante para ativar um ou ambos.

   Para cada método habilitado, escolha _[!UICONTROL Registrar Atividade de Bot]_ ou _[!UICONTROL Filtrar Atividade de Bot]_.

   >[!IMPORTANT]
   >
   >Se você escolher [!UICONTROL Filtrar atividade de bot], poderá ver uma queda no número de aberturas e cliques de email, pois as atividades falsas serão eliminadas.

   ![Administrador de email do Marketo Engage - Opções de identificação da atividade de bot](./assets/me-admin-email-bot-activity-set-filters.png){width="500"}

   Para _[!UICONTROL Corresponder com o Padrão de Proximidade]_, você também pode definir o número de segundos para **[!UICONTROL Duração entre Atividades]** (o padrão é `0`, o máximo é `3`).

   >[!NOTE]
   >
   >Com a _Duração Entre Atividades_ definida como `0` segundos, o Marketo Engage identifica as atividades de email que estão ocorrendo exatamente nesse segundo. Se várias atividades de email ocorrerem dentro do número designado de segundos, elas serão identificadas como uma atividade de bot.

   Para desativar qualquer método de filtragem, alterne o controle deslizante para a esquerda. Se você fizer isso, os dados não serão redefinidos.

### INCLUIR NA LISTA DE BLOQUEIOS IP

A Adobe identificou uma lista de endereços IP responsáveis por gerar milhões de envolvimentos falsos, já que esses envolvimentos recebidos de qualquer um dos seguintes IPs são automaticamente filtrados e não adicionados à instância do Marketo Engage. Essa filtragem pode resultar em uma redução nas aberturas de email, cliques e outras atividades relacionadas. Esta lista pode ser atualizada periodicamente.

+++ Endereços IP bloqueados

* 40.94.34.52
* 40.94.34.86
* 52.34.76.65
* 54.70.53.60
* 54.71.187.124
* 60.28.2.248
* 64.235.150.252
* 64.235.153.10
* 64.235.153.2
* 64.235.154.105
* 64.235.154.109
* 64.235.154.140
* 64.74.215.1
* 64.74.215.100
* 64.74.215.138
* 64.74.215.139
* 64.74.215.142
* 64.74.215.146
* 64.74.215.150
* 64.74.215.154
* 64.74.215.158
* 64.74.215.162
* 64.74.215.164
* 64.74.215.166
* 64.74.215.170
* 64.74.215.174
* 64.74.215.176
* 64.74.215.178
* 64.74.215.51
* 64.74.215.56
* 64.74.215.58
* 64.74.215.59
* 64.74.215.86
* 64.74.215.98
* 65.154.226.101
* 66.249.91.149
* 70.42.131.106
* 74.125.217.116
* 74.217.90.250
* 104.129.41.4
* 104.47.55.126
* 104.47.58.126
* 104.47.70.126
* 104.47.73.126
* 104.47.73.254
* 104.47.74.126
* 128.220.160.1
* 155.70.39.101
* 162.129.251.14
* 162.129.251.42
* 208.52.157.204

>[!NOTE]
>
>Cada endereço IP é cuidadosamente analisado e examinado antes de ser incluído nessa lista, garantindo que apenas os IPs mais críticos e prejudiciais sejam bloqueados.

+++
