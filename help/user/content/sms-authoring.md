---
title: Criação de SMS
description: Saiba como enviar mensagens de texto (SMS) para seus clientes em seus dispositivos móveis e personalizar e visualizar mensagens no formato de texto pelo editor de SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: a5f3f5533adefeb2daa6fc93e9cdef094aee9d37
workflow-type: tm+mt
source-wordcount: '1879'
ht-degree: 0%

---

# Criação de SMS

Use o Adobe Journey Optimizer B2B Edition para enviar mensagens de texto (SMS) aos clientes em seus dispositivos móveis. Você pode criar, personalizar e visualizar mensagens no formato de texto do editor de SMS.

## Configurações de SMS

O Adobe Journey Optimizer B2B Edition envia mensagens de texto por meio de provedores de serviços SMS (ou provedores de gateway SMS). Antes de criar a mensagem SMS, configure o provedor de serviços nas configurações do _Administrador_.

### Provedores de serviços de gateway de SMS

Atualmente, o Adobe Journey Optimizer B2B Edition está integrado a provedores de terceiros que oferecem serviços de mensagens de texto de forma independente. Os provedores de mensagens de texto compatíveis são Sinch, Twilio e Infobip.

Antes de configurar um canal SMS no Adobe Journey Optimizer B2B Edition, você deve criar uma conta com um desses provedores para obter o token da API e a ID do serviço. Essas credenciais são necessárias para configurar a conexão entre o Adobe Journey Optimizer B2B Edition e o provedor aplicável.

>[!IMPORTANT]
>
>O uso dos serviços de mensagens de texto está sujeito a termos e condições adicionais do provedor aplicável. Como soluções de terceiros, o Sinch, o Twilio e o Infobip estão disponíveis para usuários do Adobe Journey Optimizer B2B Edition por meio de uma integração. A Adobe não controla e não é responsável por produtos de terceiros. Em caso de problemas ou solicitações de assistência relacionados aos serviços de mensagens de texto (SMS), entre em contato com seu provedor.

### Verificar uma configuração de API de SMS existente

>[!NOTE]
>
>As configurações descritas podem ser acessadas somente pelos usuários com privilégios de administrador de SMS.

Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

![Acessar a configuração de credenciais da API AMA](./assets/config-sms-api.png){width="800" zoomable="yes"}

A página lista as configurações de API disponíveis para sua instância. Você pode filtrar as credenciais de API exibidas pelo provedor de serviços SMS ou criador.

![Clique no ícone de filtro para filtrar a lista de credenciais de API](./assets/config-sms-api-filter.png){width="500"}

### Criar novas credenciais de API para um provedor de serviços SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Para configurar o Sinch como seu provedor de SMS com o Adobe Journey Optimizer B2B Edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Sinch](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Sinch` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a credencial da API.

   * **[!UICONTROL ID de Serviço]** e **[!UICONTROL Token de API]** - Acesse a página de APIs da sua conta Sinch (você pode encontrar suas credenciais na guia SMS).

   Para obter mais informações sobre como encontrar essas informações para sua conta Sinch, consulte a [documentação do desenvolvedor da Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Clique em **[!UICONTROL Enviar]** quando os detalhes de configuração das suas credenciais de API estiverem concluídos.

>[!TAB Twilio]

_Para configurar o Twilio como seu provedor de SMS com o Adobe Journey Optimizer B2B Edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Twilio` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a definição de credencial de API.

   * **[!UICONTROL SID da Conta]** e **[!UICONTROL Token de Autenticação]** - Acesse o painel _Informações da Conta_ da página Painel do Console do Twilio para encontrar suas credenciais.

   Para obter mais informações sobre como encontrar essas informações para sua conta do Twilio, consulte a [Central de Ajuda do Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Clique em **[!UICONTROL Enviar]** no canto superior direito da página quando os detalhes de configuração das suas credenciais de API forem concluídos.

>[!TAB Infobip]

_Para configurar o Infobip como seu provedor de SMS com o Adobe Journey Optimizer B2B Edition:_

1. Na navegação à esquerda, expanda a seção **[!UICONTROL Administrador]** e clique em **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Criar novas credenciais de API]** na parte superior direita da lista _[!UICONTROL Credenciais de API]_.

1. Configurar suas credenciais da API de SMS:

   ![Configurar as credenciais da API de SMS do Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fornecedor de SMS]** - Escolha `Infobip` como o provedor de SMS.

   * **[!UICONTROL Nome]** - Digite um nome para a definição de credencial de API.

   * **[!UICONTROL URL de base de API]** e **[!UICONTROL chave de API]** - Acesse a página inicial da interface da Web ou a página de gerenciamento de chaves de API da sua conta Infobip para encontrar suas credenciais.

   Para obter mais informações sobre como encontrar essas informações para sua conta Infobip, consulte a [documentação do Infobip](https://www.infobip.com/docs/api/_blank).

1. Clique em **[!UICONTROL Enviar]** no canto superior direito da página quando os detalhes de configuração das suas credenciais de API forem concluídos.

>[!ENDTABS]

Ao clicar em _[!UICONTROL Enviar]_, as credenciais são imediatamente validadas e salvas, redirecionando você para a página de listagem _[!UICONTROL credenciais de API]_. Se as credenciais enviadas forem inválidas, o sistema exibirá uma mensagem de erro na página de listagem. Nesse caso, você pode optar por cancelar a configuração ou atualizá-la e enviar novamente.

## Adicionar uma ação de SMS em uma jornada de conta

Você pode configurar entregas de mensagens de texto em uma Jornada de conta ao adicionar um nó _[!UICONTROL Realizar uma ação]_ e fazer o seguinte:

1. Para o destino _[!UICONTROL Ação em]_, escolha **[!UICONTROL Pessoas]**.

1. Para a _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Enviar SMS]**.

   ![Executar uma ação - enviar sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Na parte inferior do painel _[!UICONTROL Realizar uma ação]_, clique em **[!UICONTROL Criar SMS]**.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

   ![Criar nova caixa de diálogo de SMS](assets/create-new-sms.png){width="500"}

## Criar a mensagem SMS

>[!IMPORTANT]
>
>**Gerenciamento de consentimento de SMS**<br/>
><br/>
>De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. Para fazer isso, os destinatários de SMS podem responder com palavras-chave de aceitação e recusa. Todas as palavras-chave padrão de aceitação e recusa são compatíveis e respeitadas. Além disso, qualquer palavra-chave personalizada configurada para sua conta de provedor de serviços SMS é compatível e respeitada.

1. Digite o texto que deseja enviar no campo **[!UICONTROL Mensagem]**.

   Você pode criar uma mensagem de até 1600 caracteres, a cada 160 caracteres considerados como uma única mensagem SMS.

1. **Personalizar a mensagem de texto**.

   A qualquer momento durante a criação da mensagem de texto, clique no ícone _Personalizar_ à direita da caixa de mensagem de texto.

   ![Clique no ícone Personalizar para adicionar tokens à mensagem](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   A página exibida fornece acesso aos tokens do Adobe Marketo Engage Lead e do Sistema. Os tokens padrão e personalizados estão incluídos. Você pode usar a barra de pesquisa para localizar o token necessário ou navegar pela árvore de pastas para localizar e selecionar qualquer um dos tokens de lead/sistema.

   Coloque o cursor no local da mensagem em que deseja adicionar o token. Adicione um token clicando no sinal de adição ( **+** ) ao lado dele. Para adicionar o token com um fallback (padrão exibido caso o campo não esteja disponível para um cliente potencial), clique nas reticências ( **...** ) e escolha **[!UICONTROL Inserir com texto de fallback]**.

   ![Clique nas reticências para usar um fallback para o token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   Na caixa de diálogo _[!UICONTROL Inserir valor de fallback]_, insira o texto que aparece como um fallback e clique em **[!UICONTROL Adicionar]**.

   ![Insira o texto de fallback para o token](./assets/sms-message-personalize-fallback-text.png){width="400"}

   Quando os tokens de personalização forem colocados, clique em **[!UICONTROL Salvar]** para salvar as alterações e retornar ao espaço de trabalho de criação do SMS principal. Você pode continuar a editar a mensagem com os tokens conforme necessário.

1. **Adicionar URLs à mensagem de texto**.

   Depois de definir o conteúdo, você pode adicionar URLs à mensagem clicando no ícone _Link_.

   Essa ação abre uma caixa de diálogo, na qual você pode escolher um dos dois tipos de URLs a serem vinculados:

   * **[!UICONTROL URL Externa]** - Esse tipo é qualquer URL externa que você digitar na caixa de texto.
   * **[!UICONTROL Página de aterrissagem]** - Escolha essa opção para selecionar qualquer uma das páginas de aterrissagem aprovadas do Adobe Marketo Engage Design Studio da sua instância do Marketo Engage.

   A caixa de diálogo também inclui opções para os links de URL:

   * **[!UICONTROL Encurtar URL]** - Marque esta caixa de seleção para _encurtar_ a URL, que é necessária para rastreamento. Para uma página de aterrissagem, ela usa o subdomínio Marketo Engage para o URL mais curto. Uma amostra do formato de URL mais curto é exibida. O URL real é criado quando o SMS é enviado ao recipient.

   * **[!UICONTROL Incluir mkt_tok]** - Marque esta caixa de seleção para rastrear a atividade em relação a um usuário.

   Quando as opções de link estiverem concluídas, clique em **[!UICONTROL Adicionar]** para salvar as alterações e adicionar o link de URL à mensagem SMS.

## Definir as propriedades do SMS

1. Na seção _[!UICONTROL Propriedades de SMS]_, insira um **[!UICONTROL Nome]** (obrigatório, máximo de 100 caracteres) e uma **[!UICONTROL Descrição]** (opcional, máximo de 300 caracteres) para a mensagem.

   Caracteres especiais, numéricos e de Alpha são permitidos nesses campos. Os seguintes caracteres reservados são **não permitidos**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` e `|`.

1. Escolha o **[!UICONTROL Tipo de SMS]**:

   * Use `Marketing` para mensagens de texto promocionais, que exigem o consentimento do usuário.
   * Use `Transactional` para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega.

1. Para **[!UICONTROL configuração de SMS]**, escolha uma das configurações de API predefinidas.

   Esta configuração determina qual provedor de serviço de gateway SMS e conta são usados para entregar a mensagem.

1. Digite o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

   ![Executar uma ação - enviar sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   O número do destinatário é sempre mapeado para o campo `Lead.mobilePhone` no Marketo Engage.

## Simular o conteúdo da mensagem de texto

Quando o conteúdo da mensagem é definido, você pode usar perfis de teste para simular (pré-visualizar) o conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem usando os dados do perfil de teste.

>[!IMPORTANT]
>
>Salve a mensagem SMS antes de continuar a simular a mensagem de texto.

1. Clique em **[!UICONTROL Simular Conteúdo]** na parte superior do espaço de trabalho de criação do SMS.

1. Na página _[!UICONTROL Simular Conteúdo]_, clique em **[!UICONTROL Adicionar Pessoas]**.

1. Use a página _Simular Conteúdo_ para gerenciar os clientes em potencial usados para seu perfil de teste.

   Na lista exibida, você pode pesquisar e adicionar qualquer um dos leads (até 10 leads de cada vez) do banco de dados de leads do Marketo Engage.

   Para pesquisar, digite o endereço de email completo e pressione _Enter_. O perfil de lead correspondente é exibido para seleção.

   A visualização atualiza os campos de personalização do perfil selecionado.

   Todos os clientes em potencial adicionados aparecem à esquerda.

   Você pode gerenciar essa lista adicionando mais pessoas e excluindo clientes potenciais individuais da lista de perfis (ela não os remove do banco de dados).

1. Simular conteúdo para um cliente potencial selecionado.

   Selecione qualquer um dos clientes potenciais listados à esquerda e a visualização de SMS nas atualizações de página para o cliente potencial correspondente.

   Você também pode selecionar um cliente potencial no seletor acima do espaço de visualização para atualizar a visualização do SMS na página do cliente potencial correspondente.

1. Para sair da página _[!UICONTROL Simular Conteúdo]_ e retornar ao espaço de trabalho de criação do SMS, clique em **[!UICONTROL Fechar]** na parte superior direita.

## Gerenciamento de consentimento por SMS

Oferecer aos recipients a capacidade de cancelar a inscrição para receber comunicações de uma marca e honrar essa escolha é um requisito legal. O não cumprimento desses regulamentos traz riscos legais para sua marca. Essa função também ajuda a evitar o envio de comunicações não solicitadas para seus recipients, o que pode fazer com que eles marquem suas mensagens como spam e prejudiquem sua reputação.

Quando você fornece essa opção, os destinatários de SMS podem responder com palavras-chave de aceitação e recusa. Todas as palavras-chave padrão de aceitação e recusa são compatíveis e respeitadas, bem como todas as palavras-chave personalizadas configuradas no provedor de serviços SMS. Quando a assinatura é cancelada, os perfis são removidos automaticamente do público-alvo de futuras mensagens de marketing.

O Journey Optimizer B2B Edition fornece a capacidade de gerenciar a opção de não participação em mensagens SMS usando a seguinte lógica:

* Por padrão, se um cliente potencial optar por não receber comunicações de você, o perfil correspondente será excluído dos deliveries de SMS subsequentes

* Esse consentimento principal proveniente de diferentes fontes (como a AEP ou o provedor de serviços SMS) é sincronizado com o Journey Optimizer B2B Edition. Atualmente, ele suporta apenas um único estado de consentimento por lead no nível da instância (uma &quot;John Doe&quot; lead recebe ou cancela a assinatura de todos os SMS promocionais na instância). No momento, não há suporte para aceitação dupla no nível da marca/consentimento no nível da lista de assinaturas individuais.
