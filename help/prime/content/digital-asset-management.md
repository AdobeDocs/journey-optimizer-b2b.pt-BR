---
title: Ativos
description: Gerencie ativos de imagem do Journey Optimizer B2B edition para emails, modelos e fragmentos visuais.
feature: Assets, Content
role: User
badge: label="Beta" type="Informative"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 85f61c8fa8eda07dfe8ea1e83f3c261c9159976f
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 3%

---

# Ativos

No [!DNL Adobe Journey Optimizer B2B Prime], os ativos são normalmente as imagens usadas ao criar conteúdo para oferecer suporte a jornadas. Você pode usar essas imagens em seus emails, modelos de email e fragmentos visuais do seletor de ativos ou em uma interface simples de arrastar e soltar no espaço de design visual.

Formatos de arquivo compatíveis: JPG, JPEG, GIF, PNG, EPS, SVG e RGB


>>
A importação de ativos de sistemas externos, como o DAM do Marketo Engage e o acesso a uma biblioteca de ativos pré-preenchida ainda não estão disponíveis. As versões futuras devem incluir a importação de ativos dos sistemas existentes, suporte a pastas e recursos ampliados de gerenciamento de ativos.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

A biblioteca **Assets** fornece acesso ao repositório centralizado para armazenar e gerenciar imagens e outros ativos criativos. Ele inclui recursos alimentados por IA que geram metadados automaticamente e permitem a pesquisa em linguagem natural.

Na navegação à esquerda, expanda **[!UICONTROL Gerenciamento de conteúdo]** e selecione **[!UICONTROL Assets]**.

>[!NOTE]
>
>Nesta versão do Beta, você pode escolher imagens e ativos de uma cópia única da biblioteca de ativos da Marketo Engage diretamente na tela de email. Você também pode carregar ativos de imagem adicionais da biblioteca _[!UICONTROL Assets]_ ou do espaço de design de conteúdo. Estes ativos carregados estão disponíveis para uso somente na instância [!DNL Adobe Journey Optimizer B2B Prime].

![biblioteca Assets](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

Na primeira vez que você acessar a biblioteca do _[!UICONTROL Assets]_, verifique os _[!UICONTROL Termos de Uso da IA Gerativa]_ e clique em **[!UICONTROL Concordar e Continuar]**.

![biblioteca Assets](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

A biblioteca é compatível com duas opções de layout:

* **[!UICONTROL Lista]** — Clique no ícone _Exibição de lista_ ( ![Ícone de exibição de lista](../../assets/do-not-localize/icon-falco-list-view.svg) ) para exibir ativos em uma tabela classificável com colunas de metadados.
* **[!UICONTROL Galeria]** — Clique no ícone _Modo de exibição de galeria_ ( ![Ícone de modo de exibição de galeria](../../assets/do-not-localize/icon-falco-gallery-view.svg) ) para exibir ativos como uma grade de miniaturas visuais.

## Pesquisar por ativos {#find-assets}

Use o campo _[!UICONTROL Pesquisa]_ para localizar ativos descrevendo o que é necessário em linguagem natural. Os resultados da pesquisa se baseiam em metadados gerados por IA, portanto, você não está limitado a pesquisar por nome de arquivo.

**Exemplos:**

* `team members`
* `nature`
* `exercise`

![Imagem selecionada nos resultados da pesquisa na biblioteca Assets](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## Exibir detalhes do ativo {#view-details}

Selecione um ativo para abrir sua visualização de detalhes. A exibição detalhada exibe uma descrição gerada por IA, tags e palavras-chave, além de campos de metadados adicionais. Essas informações são geradas automaticamente quando o ativo é carregado.

Selecione qualquer ativo na exibição de lista ou galeria para abrir a exibição de detalhes à direita. Selecione a guia Metadados de IA para exibir a descrição, as tags e os metadados gerados por IA.

![Imagem selecionada nos resultados da pesquisa na biblioteca Assets](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Fazer upload de um ativo {#upload}

1. Clique em **[!UICONTROL Carregar]** no canto superior direito.

1. Na caixa de diálogo, arraste e solte um arquivo do seu sistema local.

   ![Carregar um ativo de imagem](./assets/dam-upload-assets-dialog.png){width="450"}

   Como alternativa, você pode clicar em **[!UICONTROL Selecionar arquivo do seu computador]** para usar o sistema de arquivos local para localizar e selecionar o arquivo.

1. Clique em **[!UICONTROL Carregar arquivo]** para confirmar e carregar o arquivo para o repositório.

Após a conclusão do upload, o sistema gera automaticamente uma descrição, atribui tags e palavras-chave e extrai atributos visuais, como assunto e configuração. Não é necessária nenhuma marcação manual. A nova imagem será exibida com o status _[!UICONTROL PROCESSING]_ até que o processo seja concluído.

![Novo ativo de imagem no status de processamento](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
