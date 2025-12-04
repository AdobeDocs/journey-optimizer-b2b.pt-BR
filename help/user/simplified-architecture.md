---
title: Configuração simplificada da arquitetura
description: Configure o Journey Optimizer B2B edition na arquitetura simplificada. Configure esquemas XDM, canais de email/SMS, ações de jornada do Marketo Engage e usuários.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: d2f33c30dba1ce44842f41bd2dbbfada24a8ff9c
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 7%

---

# Configuração simplificada da arquitetura

Agora, o Adobe Journey Optimizer B2B Edition está disponível com uma arquitetura simplificada. Com essa arquitetura atualizada, o Journey Optimizer B2B Edition e o Marketo Engage não estão mais no mesmo sistema nem no mesmo armazenamento de dados. O Journey Optimizer B2B Edition recebe dados somente da Adobe Experience Platform. No entanto, ele continua dependendo dos direitos do Marketo Engage e alguns recursos de configuração para provisionar e configurar o sistema.

A arquitetura simplificada é a base que desbloqueia novos recursos no Adobe Journey Optimizer B2B edition:

* **Unifique e dimensione facilmente seus dados:** A nova plataforma oferece suporte a modelos de dados complexos, incluindo objetos personalizados, grupos de compra e eventos de conta. 

* **Conecte várias instâncias do Adobe Marketo Engage:** gerencie e unifique dados de vários ambientes do Adobe Marketo Engage em um único local.

* **Mantém seus dados seguros** Recursos avançados de privacidade e segurança que ajudam a proteger as informações de seus clientes. (_Em breve_)

* **Criada para o futuro:** esta atualização oferece melhorias e inovações contínuas. 

Para ambientes provisionados para essa arquitetura, use as seguintes diretrizes para configuração.

## Namespaces e esquemas

Consulte [Namespaces e esquemas B2B](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) na documentação do Experience Platform para obter uma visão geral.

### Configuração do ambiente

Configure um ambiente do Postman para suportar o namespace B2B e o utilitário de geração automática de esquema.

* Você pode baixar a coleção de utilitários de geração automática de namespace e esquema e o ambiente do [repositório do GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Para obter informações sobre como usar as APIs do Experience Platform, incluindo detalhes sobre como coletar valores para cabeçalhos necessários e ler chamadas de API de exemplo, consulte o guia [introdução às APIs do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/platform-apis/api-guide).

* Para obter informações sobre como gerar suas credenciais para as APIs do Experience Platform, consulte o tutorial sobre [autenticação e acesso às APIs do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication).

* Para obter informações sobre como configurar o Postman para APIs do Experience Platform, consulte as etapas detalhadas em [Postman no Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman).

Com um console de desenvolvedor do Experience Platform e uma configuração do Postman configurada, agora é possível começar a aplicar os valores de ambiente apropriados ao seu ambiente do Postman.

### Execute os scripts

Com a configuração da coleção e do ambiente do Postman, é possível executar o script na interface do Postman.

Na interface do Postman, selecione a pasta raiz do utilitário gerador automático e selecione **Executar** no cabeçalho superior.

Quando a interface do Executor for exibida, verifique se todas as caixas de seleção estão selecionadas e selecione **Executar Namespaces e Utilitário de Geração Automática de Esquemas**.

Uma solicitação bem-sucedida cria os namespaces e esquemas necessários para o B2B.

## Seleção de campo XDM

É possível gerenciar os campos XDM disponíveis em todo o aplicativo na interface do usuário do Journey Optimizer B2B edition. Esses campos ajudam a simplificar sua instância, expondo apenas os campos relevantes para a compilação de **_jornadas_**, **_grupos de compras_** ou **_personalizações de email_**.

### Classes XDM

#### Classes padrão

Use as etapas abaixo para definir campos para classes XDM padrão:

1. Navegue até **[!UICONTROL Administração] > [!UICONTROL Configurações]**.

1. No painel de navegação, selecione **[!UICONTROL Classes XDM]**.

1. Selecione a guia **[!UICONTROL Padrão]** para exibir as classes XDM disponíveis:

   * Perfil individual XDM

   * Conta empresarial XDM

#### Campos gerenciados

Defina quais campos estarão disponíveis no aplicativo.

1. Clique no ícone _Mais menu_ (**...**) e selecione **[!UICONTROL Editar campos gerenciados]**.

1. Revise a lista de campos disponíveis (clique no ícone _Informações_ para obter metadados do campo).

1. Selecione os campos que deseja incluir e desmarque as seleções dos campos desnecessários.

1. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar suas seleções.

1. Clique em **[!UICONTROL Salvar]**.

#### Campos atualizáveis

Escolha quais campos podem ser modificados por meio das ações de jornada **[!UICONTROL Atualizar Perfil da Conta]** ou **[!UICONTROL Atualizar Perfil da Pessoa]**.

1. Clique no ícone _Mais menu_ (**...**) e selecione **[!UICONTROL Editar campos atualizáveis]**.

1. Selecione **[!UICONTROL Esquema]** e depois **[!UICONTROL Conjunto de Dados]**.

   Esses esquemas e conjuntos de dados são fornecidos por sua organização.

1. Revise a lista de campos atualizáveis (clique no ícone _Informações_ para obter metadados).

   Somente os campos gerenciados são editáveis.

1. Selecione os campos que você deseja disponibilizar para atualização no jornada.

1. Clique em **Salvar**

### Esquemas relacionais

Selecione [esquemas relacionais](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational) para usar na **_decisão de jornada_** e na **_personalização_**. No momento, esses esquemas são para casos de uso de Objeto personalizado. No futuro, os esquemas relacionais também poderão ser usados para outros casos de uso de objeto.

1. Selecione a guia **[!UICONTROL Relacional]**.

1. Clique em **[!UICONTROL Selecionar classe XDM relacional]**.

   No momento, somente o Objeto personalizado de conta muitos para um é compatível.

1. Revise a lista de campos de esquema (clique no ícone _informações_ para exibir os metadados).

1. Selecione os campos que deseja incluir.

1. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar suas seleções.

1. Clique em **[!UICONTROL Salvar]**.

>[!NOTE]
>
>Observe que os esquemas relacionais devem ter as seguintes configurações:
>
><li>Comportamento: Registro
&gt; <li>Segmentação: ativada
&gt; <li>Tipo de relacionamento: muitos para um
&gt; <li>Esquema de referência: <a href="https://experienceleague.adobe.com/pt-br/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">Conta B2B - Esquema de conta de negócios XDM</a>
&gt; <li>Campos obrigatórios: chave primária, chave estrangeira e descritor de versão
&gt; <li>Conjunto de dados associado: definido e mapeado para o esquema

### Eventos

Selecione os Eventos de Experiência a serem usados na **_decisão de jornada_**.

1. Selecione a guia **[!UICONTROL Eventos]**.

1. Clique em **[!UICONTROL Selecionar evento de experiência]**.

1. Clique em **[!UICONTROL Selecionar tipo de evento]**, escolha o tipo de evento e clique em **[!UICONTROL Selecionar]**.

1. Clique em **[!UICONTROL Selecionar campos]**, escolha os campos necessários e clique em **[!UICONTROL Selecionar]**.

1. Clique em **[!UICONTROL Salvar]**.

## Configuração de email

As informações a seguir devem ser configuradas para enviar emails do Journey Optimizer B2B edition.  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protocolos de rastreamento e entrega de email

1. [Criar registros DNS para email](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Configurar SPF e DKIM](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Configurar DMARC](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [Configurar registros MX para o seu domínio](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [Adicionar endereços IP de saída a incluis na lista de permissões](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Se precisar compartilhar o pool de IP dedicado, entre em contato com a equipe de avaliação do delivery sobre a viabilidade e a configuração assistida.

### Configurações de canal de email

Na arquitetura simplificada, as configurações de email são definidas no aplicativo do Marketo Engage. Complete as etapas de configuração relacionadas ao email:

* [https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

* [https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Limites de comunicação

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Canais]**.

1. No painel de navegação, selecione **[!UICONTROL Limite de comunicação]**.

1. Crie um conjunto de regras de limite de comunicação global (esse conjunto de regras é criado por padrão em cada instância do Journey Optimizer B2B edition).

   Não há limite de comunicação se o conjunto de regras global não for criado.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Limites de comunicação compartilhados

Na nova arquitetura, o Journey Optimizer B2B edition e o Marketo Engage têm limites de comunicação independentes por padrão.

Se quiser que a instância do Marketo Engage compartilhe o limite de comunicação definido na instância do Journey Optimizer B2B edition, entre em contato com o Suporte da Adobe para obter assistência na configuração ou abra um tíquete de Suporte. Mediante solicitação, a equipe de engenharia pode habilitar o compartilhamento de limites de comunicação entre o Journey Optimizer B2B edition e uma ou mais instâncias do Marketo Engage.

Quando os limites de comunicação compartilhada estiverem ativados, você poderá definir as regras no Journey Optimizer B2B edition e estender o compartilhamento desses limites para os códigos Marketo Munchkin. Para obter mais informações, consulte [Limites de comunicação](./admin/configure-channels-emails.md#communication-limits)

<!-- internal info only 

Currently, the shared communication limit in the Marketo Engage instance must be set up through an API call.

For example, when:

* The munchkinId of the Journey Optimizer B2B Edition instance is `JKL-567-MNO`.
* The munchkinId of the Marketo Engage instance is `ABC-123-DEF` and it is in the SJ datacenter

The API request should look similar to the following:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```
-->

## Configuração do canal de SMS

Consulte [_configurações de SMS_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms) para obter informações detalhadas.

## Ações do Marketo Engage do jornada

É possível configurar uma ou mais instâncias remotas do **_Marketo Engage_** para serem usadas com as seguintes ações de jornada:

* Adicionar à lista do Marketo
* Remover da lista do Marketo
* Adicionar à campanha de solicitação do Marketo

Conclua as seguintes etapas para configurar essas conexões:

1. Navegue até **[!UICONTROL Administração] > [!UICONTROL Configurações]**.

1. No painel de navegação, selecione **[!UICONTROL Classes XDM]**.

1. Selecione a guia **[!UICONTROL Integrações]**.

1. Clique em **[!UICONTROL Criar conexão]**.

1. Insira o **[!UICONTROL Nome]** e a **[!UICONTROL Descrição]**.

1. Selecione **[!UICONTROL Atualizar política]** para registros de pessoas correspondentes.

1. Insira a **[!UICONTROL Munchkin ID]**, a **[!UICONTROL ID do Cliente]**, o **[!UICONTROL Segredo do Cliente]** e clique em **[!UICONTROL Conectar-se à Marketo]**.

1. Clique em **[!UICONTROL Criar]**.

## Integração de usuários

Consulte a página [Gerenciamento de usuários](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) para obter uma visão geral.

### Grupos de usuários existentes

Se todos os usuários existentes do Journey Optimizer B2B edition precisarem acessar a nova arquitetura, use o grupo de usuários existente do Journey Optimizer B2B edition. Um administrador do sistema ou administrador de produto pode executar as seguintes etapas.

1. Crie um perfil de produto no Marketo Engage dedicado.

1. Adicionar um grupo de usuários existente ao perfil de produto criado.

Os perfis concedem todas as funções e permissões já atribuídas a esse grupo de usuários, que já devem estar configuradas para que os usuários acessem o Journey Optimizer B2B edition. Se apenas um subconjunto de usuários precisar acessar a nova arquitetura, conclua as etapas descritas abaixo. Mais detalhes na [documentação atual](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management).

### Criar um novo grupo de usuários

1. Crie um perfil de produto na instância dedicada do Marketo Engage.
1. Crie um grupo de usuários para novos usuários.
1. Selecione e atribua os perfis de produto necessários ao grupo de usuários:

   * O perfil do Marketo Engage que você criou
   * Perfis do Adobe Experience Platform
      * AEP-Padrão-Todos-Usuários
      * Coleção de dados da Adobe Experience Platform
      * Acesso integral à coleção de dados

1. Adicione os usuários ao grupo de usuários.
1. Adicione um novo grupo de usuários às funções do Journey Optimizer B2B edition no Experience Platform.
