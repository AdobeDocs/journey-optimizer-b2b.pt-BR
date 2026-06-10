---
title: Configurações do Forms
description: Saiba como configurar predefinições de formulário.
feature: Setup, Channels
role: Admin
autotag-review: '2026-05-27T16:06:59.553Z'
TQID: 'https://experienceleague.adobe.com/GFW5SZ5Z-phoEIE6jTVD7EgwcT1Vx647mjoLXJejbFg'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 955fac784a8f438ec2f9aaf66e9aaeefda58e2a7
workflow-type: tm+mt
source-wordcount: 542
ht-degree: 3%

---

# Configurações do Forms

Para que os profissionais de marketing possam [criar e publicar formulários](../content/forms.md) para usar em suas páginas de aterrissagem, um administrador de produto deve criar uma ou mais predefinições dedicadas. Cada predefinição define o ponto de extremidade de conexão usado para enviar os dados de envio do formulário e o conjunto de dados usado para armazenar os dados capturados.

Quando os dados chegam ao endpoint de transmissão, eles são vinculados às informações do conjunto de dados. Usando as conexões de origem/destino geradas e o fluxo de origem, os dados são enviados para o conjunto de dados.

>[!BEGINSHADEBOX]

## Pré-requisitos

Para usar formulários web, você deve ter uma ou mais _**conexões de transmissão da API HTTP**_ definidas no Adobe Experience Platform. Verifique se cada conexão que você deseja usar atende aos seguintes requisitos:

* O tipo de dados deve ser definido como XDM (não dados brutos)
* A autenticação deve ser desabilitada (conexão não autenticada)

Para obter informações detalhadas sobre como criar conexões de origem de transmissão, consulte a [_documentação do Experience Platform_](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

A configuração de canal do Forms no Journey Optimizer B2B edition requer as [permissões](../admin/user-management.md#b2b-product-permissions) a seguir:

* _[!UICONTROL Configurações do Canal B2B]_ > _[!UICONTROL Exibir Predefinições do Forms]_ - Necessário para exibir configurações de predefinição de formulários.
* _[!UICONTROL Configurações de Canal B2B]_ > _[!UICONTROL Gerenciar Predefinições do Forms]_ - Necessário para criar, atualizar e excluir configurações de predefinição de formulários.
* _[!UICONTROL Configurações de Canal B2B]_ > _[!UICONTROL Publicar Predefinições de Forms]_ - Necessário para publicar configurações de predefinição de formulários.

>[!ENDSHADEBOX]

## Diretrizes de configuração da predefinição de formulário

Ao criar uma predefinição:

* É possível configurar várias predefinições usando diferentes combinações de conjuntos de dados e conexões de transmissão.

* É possível reutilizar o mesmo conjunto de dados ou conexão de transmissão em várias predefinições.

* Cada conexão de transmissão gera recursos automaticamente, como:

   * _conexão Source_ - de onde os dados se originam.
   * _Conexão de destino_ - onde os dados são armazenados ou consumidos.
   * _Fluxo do Source_ - o pipeline que move dados da conexão de origem para o Experience Platform. Ela lida com mapeamento, transformação e validação.

## Criar uma predefinição de formulário

1. Na navegação à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**.

1. Em _[!UICONTROL Configurações de formulário]_, no painel de navegação, selecione **[!UICONTROL Predefinições de formulário]**.

   ![Acessar as configurações de formulário](./assets/config-channels-forms.png){width="800" zoomable="yes"}

1. Clique em **[!UICONTROL Criar predefinição de formulário]**.

1. Insira um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) para a configuração.

   >[!NOTE]
   >
   >Os nomes devem começar com uma letra (A-Z) e podem conter apenas caracteres alfanuméricos. Você também pode usar sublinhado `_`, ponto `.` e hífen `-` caracteres.

1. Selecione a **[!UICONTROL Conexão de transmissão]**.

   Essa conexão é o ponto de extremidade de transmissão usado para enviar os dados quando um visualizador da Web envia um formulário. Se a conexão de transmissão necessária não for exibida na lista, verifique se os requisitos foram atendidos.

1. Clique no ícone _Selecionar conjunto de dados_ ( ![Selecionar ícone do conjunto de dados](../assets/do-not-localize/icon-select-data.svg) ) para vincular um conjunto de dados ao formulário.

   O conjunto de dados é onde as respostas do formulário são armazenadas e refletidas. Você pode inserir uma string de texto para procurar um conjunto de dados específico ou selecioná-lo na lista.

   ![Caixa de diálogo Selecionar conjuntos de dados](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >Atualmente, apenas os [conjuntos de dados do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview) habilitados para perfil e não habilitados estão disponíveis para seleção. Um conjunto de dados pode ser selecionado de cada vez. Os conjuntos de dados do sistema não podem ser usados para salvar dados de formulário.

   Marque a caixa de seleção do conjunto de dados e clique em **[!UICONTROL Selecionar]**.

1. Clique em **[!UICONTROL Salvar como rascunho]**.

## Publicar uma predefinição de formulário

1. Clique no nome da predefinição do formulário para abrir a página de configuração.

   É possível fazer ajustes no rascunho, se necessário.

1. Clique em **[!UICONTROL Publicar]**.

   Quando a predefinição de formulário é listada com um status _Publicado_, ela está disponível para uso na criação de formulários.
