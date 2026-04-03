---
title: Criação no WhatsApp
description: Crie mensagens de WhatsApp para jornadas de conta usando modelos aprovados do Meta, tokens de personalização e configurações de entrega no Journey Optimizer B2B edition.
feature: Content, Channels, Account Journeys
role: User
source-git-commit: a9077a4fb5c90166433204d7a0a124f4f2e5ab92
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 1%

---

# Criação no WhatsApp

Use o Adobe Journey Optimizer B2B edition para enviar mensagens do WhatsApp para membros da conta em seus dispositivos móveis. Você pode criar, personalizar e pré-visualizar mensagens usando modelos de mensagem aprovados do Meta no editor do WhatsApp. <!-- Test your WhatsApp messages before publishing the account journey to ensure your intended rendering, accurate personalization, and proper configuration of all settings. -->

Antes de criar mensagens do WhatsApp para jornadas de conta, verifique se você tem o [canal do WhatsApp necessário configurado](../admin/configure-channels-whatsapp.md) nas configurações do _[!UICONTROL Administrador]_.

>[!NOTE]
>
>Somente _elementos de mensagem de saída_ do WhatsApp são suportados no Journey Optimizer B2B edition.

+++ Elementos de mensagem e opções de chamadas para ação compatíveis

Os seguintes tipos de mensagem são suportados no WhatsApp:

| Elemento de mensagem | Descrição |
| - | - |
| Cabeçalhos | Texto opcional que aparece acima do corpo da mensagem. |
| Texto | Aceita conteúdo dinâmico por meio de parâmetros. |
| Imagens (JPEG, PNG) | Deve estar no formato RGB de 8 bits ou RGBA e abaixo de 5 MB no tamanho. |
| Vídeos | Deve ser 3GPP ou MP4, com menos de 16 MB, e hospedado por URL. |
| Áudio | Disponível somente para mensagens de resposta. Deve ser o formato AAC, AMR, MP3, MP4 audio ou OGG, hospedado em um URL e menos de 16 MB. |
| Documentos | Deve ter menos de 100 MB, hospedado em uma URL e em um dos seguintes formatos: `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` ou `.pdf`. |
| Corpo de texto | Aceita conteúdo dinâmico por meio de parâmetros. |
| Texto do rodapé | Aceita conteúdo dinâmico por meio de parâmetros. |

As seguintes opções do call-to-action estão disponíveis para suas mensagens no WhatsApp:

| Call to action | Descrição |
| - | - |
| Visitar site | Somente um botão é permitido, com parâmetros variáveis incluídos. |
| Chamar no WhatsApp | Fornece um botão que abre um bate-papo do WhatsApp com o número de telefone especificado diretamente da mensagem. |
| Telefonar para número | Fornece um botão que inicia uma chamada telefônica para o número especificado quando tocado pelo usuário. |

+++

## Adicionar uma ação do WhatsApp em uma jornada de conta

Você pode configurar entregas de mensagens do WhatsApp em uma jornada de conta ao [adicionar um nó _[!UICONTROL Executar uma ação]_](../journeys/action-nodes.md) e fazer o seguinte:

1. Para o destino _[!UICONTROL Ação em]_, escolha **[!UICONTROL Pessoas]**.

1. Para a _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Enviar WhatsApp]**.

   ![Executar uma ação - enviar WhatsApp](./assets/whatsapp-journey-node.png){width="500" zoomable="yes"}

## Criar a mensagem do WhatsApp

1. Na parte inferior do painel _[!UICONTROL Realizar uma ação]_, clique em **[!UICONTROL Criar WhatsApp]**.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) exclusivos para a mensagem do WhatsApp.

   ![Caixa de diálogo Criar nova mensagem do WhatsApp](./assets/whatsapp-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

   O _espaço de design do WhatsApp_ é aberto, onde você pode definir as ações do WhatsApp e criar o conteúdo para enviar a mensagem.

### Selecionar a configuração de ações

1. No _espaço de design do WhatsApp_, selecione a guia **[!UICONTROL Ações]**.

1. Para a **[!UICONTROL configuração do WhatsApp]**, selecione a [configuração](../admin/configure-channels-whatsapp.md#create-channel-configuration) que oferece suporte às ações de marketing e às configurações de entrega de mensagens para suas necessidades.

   ![Criar WhatsApp - guia Ações](./assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Editar conteúdo]** para seguir para os parâmetros e o texto da mensagem.

### Selecionar um modelo de mensagem

>[!IMPORTANT]
>
>**Gerenciamento de consentimento do WhatsApp**: de acordo com as políticas e os regulamentos aplicáveis da Meta, todas as mensagens de marketing do WhatsApp devem ser enviadas apenas aos destinatários que optaram por receber comunicações. Os destinatários do WhatsApp podem recusar a qualquer momento respondendo com uma palavra-chave de recusa. As respostas de recusa são atendidas automaticamente e os perfis correspondentes são removidos dos futuros públicos-alvo de mensagens de marketing.

As mensagens do WhatsApp são enviadas usando modelos de mensagem pré-aprovados da sua conta comercial do Meta WhatsApp. **Os modelos devem ser revisados e aprovados pelo Meta** antes que você possa usá-los no Journey Optimizer B2B edition. Trabalhe com o administrador da sua conta do [!DNL Meta Business Manager] para gerenciar e enviar modelos para aprovação.

1. Para **[!UICONTROL Selecionar categoria do modelo]**, escolha uma das seguintes opções:

   * Marketing
   * Utilitário
   * Autenticação

1. Para **[!UICONTROL Selecionar modelo de WhatsApp]**, escolha um modelo aprovado para a conta comercial de configuração.

   O conteúdo do template é carregado no editor de mensagens, exibindo a estrutura do template e quaisquer campos de variável disponíveis para personalização.

   ![Modelo de mensagem do WhatsApp selecionado com mensagem carregada na janela de visualização](./assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   Os modelos são organizados por categoria (_Marketing_, _Utilitário_ e _Autenticação_) e status. Somente modelos **_Aprovados_** estão disponíveis para seleção. Para obter mais informações sobre como criar modelos do WhatsApp, consulte [_Criar modelos de mensagem para sua conta do WhatsApp Business_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) na documentação do Meta.

### URLs de imagem

Se o modelo incluir imagens, use o campo **[!UICONTROL URL da Imagem]** para adicionar URLs de mídia para substituir quaisquer espaços reservados no modelo. As mídias de modelo do Meta são apenas espaços reservados. Para exibir imagens, áudio ou vídeo corretamente, você deve usar URLs externos do Adobe Experience Manager ou de outras fontes.

### Personalizar o conteúdo da mensagem

Os modelos aprovados de WhatsApp podem incluir espaços reservados para variáveis definidos com o uso de dados de perfil ou valores dinâmicos.

Para cada campo de variável exibido no modelo, clique no ícone _Personalizar_ ( ![Ícone Personalizar](../assets/do-not-localize/icon-personalize.svg) ) ao lado do campo.

![Variáveis no modelo do WhatsApp](./assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

A caixa de diálogo fornece acesso aos tokens da conta, da pessoa e do sistema. Os tokens padrão e personalizados estão incluídos. Você pode usar a barra _Pesquisa_ para localizar o token necessário ou navegar pela árvore de pastas para localizar e selecionar qualquer um dos tokens.

Para obter informações detalhadas sobre o uso de tokens para personalização, consulte [Personalização de conteúdo](./personalization.md).

Quando seus tokens de personalização forem definidos, clique em **[!UICONTROL Salvar]** para salvar as alterações e retornar ao espaço de trabalho principal da mensagem do WhatsApp.
