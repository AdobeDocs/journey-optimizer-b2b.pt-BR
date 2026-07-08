---
title: Gerenciar rastreamento de abertura de email
description: Desabilite o rastreamento de abertura de email para um email individual ou capture a preferência de rastreamento de uma pessoa e use um caminho dividido para enviar variantes de email de rastreamento e não rastreamento.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 860
ht-degree: 0%

---

# Gerenciar rastreamento de abertura de email

Você pode desativar o rastreamento aberto para um email individual ou capturar a preferência de rastreamento de cada pessoa no Adobe Experience Platform e usar um caminho dividido para encaminhar as pessoas para variantes de email de rastreamento e não rastreamento.

>[!BEGINSHADEBOX &quot;Orientação da CNIL sobre pixels de rastreamento de email&quot;]

Em 14 de abril de 2026, a *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL) publicou uma [recomendação sobre o uso de pixels de rastreamento em emails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). As orientações esclarecem quando o consentimento é necessário e destacam a importância de práticas de consentimento adequadas para o rastreamento de pixels de email. Essa política pode afetar as práticas de envio para qualquer entidade que entregue emails a assinantes com sede na França.

Um pixel de rastreamento de email é uma imagem transparente 1x1 inserida na HTML de um email. Quando o cliente de email do recipient carrega essa imagem, o pixel faz o ping em um servidor que registra dados, como carimbo de data e hora, tipo de dispositivo, cliente de email e, às vezes, um endereço IP para localização aproximada. Esse log é vinculado ao registro de um recipient, permitindo que os profissionais de marketing saibam se um email está aberto.

Os recursos do produto [!UICONTROL Journey Optimizer B2B edition] descritos aqui são blocos de construção que, configurados e operados adequadamente, podem oferecer suporte a uma implementação compatível. Cada cliente é responsável por determinar e cumprir suas obrigações conforme a legislação aplicável.

>[!ENDSHADEBOX]

## Desativar o rastreamento para um único email {#disable-tracking-single-email}

Use essa opção quando quiser que um email específico nunca relate uma atividade aberta, independentemente de quem o receber.

1. Nas propriedades do nó jornada à direita, abra o email.

1. Nas propriedades de email, marque a caixa de seleção **[!UICONTROL Desabilitar rastreamento aberto]**.

   ![Desabilitar o rastreamento de aberturas de email](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   Consulte [Definir as configurações de email](./add-email.md#define-the-email-settings) para obter a lista completa de propriedades de email.

## Segmentar pessoas por preferência de rastreamento {#segment-people-tracking-preference}

Se você quiser permitir que cada pessoa escolha se suas aberturas de email são rastreadas, capture essa preferência como um atributo de pessoa no Adobe Experience Platform (AEP). Você pode usar este campo em um [formulário de página de aterrissagem](./forms.md) para que seus contatos tenham a oportunidade de recusar o rastreamento de aberturas de email. Você pode usar um nó _Split paths_ em suas jornadas para rotear pessoas que fazem rastreamento ou não rastreamento para diferentes variantes de email. Isso permite honrar uma opção de recusa individual sem desativar o rastreamento aberto para todos.

O fluxo de trabalho tem três partes:

1. [Adicione um campo personalizado para preferência de rastreamento](#add-custom-field-tracking-preference) no AEP e envie uma comunicação de recusa com um link de formulário.
1. [Adicione um caminho dividido para opção de não participação de rastreamento](#add-split-path-tracking) na jornada.
1. [Configure as variantes de email de rastreamento e de não-rastreamento](#configure-tracking-and-non-tracking-email-variants) para cada caminho.

### Adicionar um campo personalizado para preferência de rastreamento {#add-custom-field-tracking-preference}

>[!NOTE]
>
>Adicionar e mapear campos XDM personalizados é uma tarefa de administração do Adobe Experience Platform. Entre em contato com o administrador do AEP ou com a equipe de engenharia de dados para concluir esta etapa.

1. No AEP, abra o esquema usado para seu perfil de pessoa B2B (por exemplo, _Pessoa B2B_).

1. Na ID do locatário, localize ou crie um grupo de campos para os campos de gerenciamento de consentimento da sua organização (por exemplo, `consents`).

1. Adicione um campo ao grupo de campos, como um campo booleano chamado `emailTracking`, para representar se a pessoa consentiu com o rastreamento de aberturas.

1. Insira o nome e o nome de exibição do campo, defina o tipo, atribua-o ao grupo de campos e clique em **[!UICONTROL Aplicar]**.

1. Clique em **[!UICONTROL Salvar]** para salvar as alterações do esquema.

   ![Adicionar o campo emailTracking ao grupo de campos de consentimento de esquema do AEP](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. Disponibilize o campo em [!DNL Journey Optimizer B2B Edition] selecionando-o como um _Campo gerenciado_ para a classe [!UICONTROL Perfil Individual XDM] no [Gerenciamento de campo XDM](../admin/xdm-field-management.md#managed-fields).

   ![Selecione emailTracking como um campo gerenciado no gerenciamento de campos XDM](./assets/email-tracking-xdm-field-select.png){width="450"}

   Isso disponibiliza o campo como uma condição nos nós de caminho dividido.

### Adicionar um caminho dividido para opção de não participação de rastreamento {#add-split-path-tracking}

Adicione um nó [_Split paths by people_](../journeys/split-merge-paths-nodes.md#split-paths-by-people) à jornada e defina um caminho para cada valor de preferência de rastreamento.

1. Adicione um nó **[!UICONTROL Split paths]** e escolha **[!UICONTROL People]** para a divisão.

1. Para o primeiro caminho, aplique uma condição usando seu campo de preferência de rastreamento personalizado (por exemplo, `emailTracking` é `true`) para identificar pessoas que permitem o rastreamento aberto.

   ![Condição de caminho dividido - adicionar campo de rastreamento de email como verdadeiro](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. Adicione um segundo caminho e aplique a condição inversa (`emailTracking` is `false`) para identificar as pessoas que optaram por não participar do rastreamento.

   Para obter etapas gerais sobre como adicionar caminhos, aplicar condições e reordenar caminhos, consulte [Adicionar um caminho dividido pelo nó de pessoas](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).

   ![Dividir caminho por pessoas - condições de ativação e desativação do rastreamento de email](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### Configurar variantes de email de rastreamento e não rastreamento {#configure-tracking-and-non-tracking-email-variants}

Adicione um nó de ação [_[!UICONTROL Enviar email &#x200B;]_](./add-email.md) a cada caminho para que cada pessoa receba a variante de email que corresponde à sua preferência de rastreamento.

1. No caminho habilitado para rastreamento, adicione uma ação **[!UICONTROL Enviar email]** e selecione ou crie o email como de costume, deixando a opção **[!UICONTROL Desabilitar rastreamento aberto]** desmarcada nas propriedades do email.

1. No caminho de opção, adicione uma ação **[!UICONTROL Enviar email]** usando o mesmo email ou um email duplicado e marque a caixa de seleção **[!UICONTROL Desabilitar rastreamento de abertura]** nas propriedades de email à direita.

   ![Email para rastreamento fora do caminho - desabilitar rastreamento aberto](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [Publique a jornada](../journeys/create-publish-journey.md#publish-a-journey).

   As pessoas são encaminhadas automaticamente para a variante de email que corresponde ao valor do campo de preferência de rastreamento, e todas as atualizações que fizerem em suas preferências serão refletidas na próxima vez que entrarem na jornada.
