---
title: Trabalhar com ativos do Marketo Engage
description: Saiba mais sobre como usar a integração de gerenciamento de ativos do Marketo Engage Design Studio no Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: 430ae5b7-2691-454c-bbd2-5a0b7a8843fb
source-git-commit: ec72c46a57109814464542fd4a8e4a9828982136
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 0%

---

# Trabalhar com ativos do Marketo Engage

O Marketo Engage Design Studio é a fonte de ativos padrão do Journey Optimizer B2B Edition e você pode gerenciar e usar facilmente os ativos disponíveis no conteúdo para suas jornadas de conta.

## Procurar e acessar ativos

Para acessar os ativos do Adobe Marketo Engage Design Studio no Journey Optimizer B2B Edition, vá para a navegação à esquerda e clique em **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Assets]**. Essa ação abre uma página de listagem com todos os ativos listados.

![Procurar ativos Marketo Engage](assets/assets-list-page.png){width="600" zoomable="yes"}

* Para exibir os ativos por pasta, abra a estrutura de pastas clicando no ícone _Mostrar pastas_ na parte superior esquerda.

* Para classificar a tabela por qualquer uma das colunas, clique no título da coluna.

* Para pesquisar um ativo de imagem na pasta selecionada, digite uma sequência de texto na barra de pesquisa.

* Para personalizar as colunas exibidas na tabela, clique no ícone _Personalizar tabela_ na parte superior direita.

  Selecione as colunas que deseja exibir na lista e clique em **[!UICONTROL Aplicar]**.

## Exibir detalhes do ativo

Clique no nome de qualquer ativo para abrir a página de detalhes do ativo.

## Exibir ativos usados por referências

Na página de detalhes do ativo, clique na guia **[!UICONTROL Usado por]** para exibir detalhes sobre onde o ativo é usado atualmente no Journey Optimizer B2B Edition, em emails, modelos de email e fragmentos.

>[!IMPORTANT]
>
>Qualquer ativo que esteja atualmente _EM USO_ em qualquer um dos emails, modelos de email ou fragmentos **não pode** ser excluído.

As referências são exibidas por categoria: _Email_, _Modelo de email_ ou _Fragmento_. Os emails no Journey Optimizer B2B Edition são incorporados e criados no jornada, portanto, a jornada principal do email que usa o ativo é exibida nas referências.

Clicar no link direciona você para o email, modelo de email ou fragmento correspondente em que o ativo é usado.

## Adicionar ativos

Na página da lista do Assets, é possível adicionar ativos de imagem ao Adobe Marketo Engage Design Studio.

1. Clique em **[!UICONTROL Adicionar Assets]** na parte superior direita.

1. Na caixa de diálogo _[!UICONTROL Adicionar ativos]_, arraste e solte um ou mais arquivos do sistema na caixa de arquivo.

   ![Adicionar ativos ao Marketo Engage Design Studio](./assets/assets-add-dialog.png){width="500" zoomable="yes"}

   Você também pode clicar no link _[!UICONTROL Selecionar um arquivo do seu computador]_ para usar o sistema de arquivos local para localizar e selecionar arquivos.

   Você pode fazer upload de ativos do seu sistema local de até 10 arquivos por vez. O tamanho máximo do arquivo é 100 MB.

   Os nomes de arquivo das imagens selecionadas são exibidos na caixa de diálogo. Os nomes dos arquivos do ativo devem ser exclusivos (em várias pastas). Se um arquivo com o nome já existir, uma mensagem será exibida. Os nomes podem ter no máximo 100 caracteres e não podem conter caracteres especiais (como `;`, `:`, `\` e `|`).

1. Selecione a pasta de destino para armazenar os ativos usando o seletor de pastas.

1. Para substituir arquivos ao carregar um ou mais arquivos com um nome de arquivo existente, marque a caixa de seleção **[!UICONTROL Substituir arquivos existentes]**.

1. Clique em **[!UICONTROL Adicionar]**.

## Excluir ativos

Não é possível excluir nenhum ativo que esteja sendo usado em nenhum dos emails, modelos de email ou fragmentos. Verifique as referências usadas por antes de iniciar a remoção de um ativo. Além disso, uma ação de exclusão não pode ser desfeita, portanto, verifique antes de iniciar uma ação de remoção.

É possível excluir um ativo usando um dos seguintes métodos:

* Vá para os detalhes do ativo, clique em **[!UICONTROL ... Mais]** no canto superior direito e escolha **[!UICONTROL Excluir]** nas opções.

  ![Acessar ações do ativo](./assets/assets-details-more-menu.png){width="500" zoomable="yes"}

* Na página de listagem _[!UICONTROL Assets]_, clique nas _Reticências_ (**[!UICONTROL ...]**) ao lado do item de ativo e escolha **[!UICONTROL Excluir]** nas opções.

  ![Acessar ações do ativo](./assets/assets-list-file-more-menu.png){width="500" zoomable="yes"}

Essa ação abre uma caixa de diálogo de confirmação. Você pode anular o processo clicando em **[!UICONTROL Cancelar]** ou em **[!UICONTROL Excluir]** para confirmar a exclusão.

Se o ativo estiver em uso no momento, a ação abrirá uma caixa de diálogo informativa que o alerta de que não pode ser excluído. Clique em **[!UICONTROL OK]**, que interrompe a exclusão.

## Substituir ativos

É possível substituir um ativo usando um dos seguintes métodos:

* Vá para os detalhes do ativo, clique em **[!UICONTROL ... Mais]** no canto superior direito e escolha **[!UICONTROL Substituir]** nas opções.

* Na página de listagem _[!UICONTROL Assets]_, clique nas _Reticências_ (**[!UICONTROL ...]**) ao lado do item de ativo e escolha **[!UICONTROL Substituir]** nas opções.

Na caixa de diálogo _[!UICONTROL Substituir ativo]_, arraste e solte o arquivo de substituição do seu sistema na caixa de arquivo. Você também pode clicar no link _[!UICONTROL Selecionar um arquivo do seu computador]_ para usar o sistema de arquivos local para selecionar um arquivo. (Se você selecionar vários arquivos no sistema local, o primeiro arquivo selecionado será usado para a substituição.)

![Caixa de diálogo Substituir ativo](./assets/assets-replace-dialog.png){width="520" zoomable="yes"}

Para continuar, clique em **[!UICONTROL Substituir]**. Você pode anular o processo clicando em **[!UICONTROL Cancelar]**.

Se o arquivo a ser substituído estiver em uso no momento, uma caixa de diálogo informativa alertará que o novo arquivo de imagem substitui a imagem em todos os locais em que é usada (emails, modelos de email e fragmentos).

## Baixar ativos

É possível baixar um ativo usando um dos seguintes métodos:

* Vá para os detalhes do ativo e clique em **[!UICONTROL Baixar]** na parte superior direita.

* Na página de listagem _[!UICONTROL Assets]_, clique nas _Reticências_ (**[!UICONTROL ...]**) ao lado do item de ativo e escolha **[!UICONTROL Baixar]** nas opções.

Na caixa de diálogo de confirmação, clique em **[!UICONTROL Baixar]** para iniciar o download do ativo para o sistema local. Você pode anular o processo clicando em **[!UICONTROL Cancelar]**.

## Aplicar ações em massa em ativos selecionados

Na página de listagem (_[!UICONTROL Gerenciamento de Conteúdo]_ > _[!UICONTROL Assets]_), selecione vários ativos de cada vez marcando cada caixa de seleção à esquerda. Um banner de mensagem é exibido na parte inferior ao selecionar vários ativos.

![Ativos selecionados](./assets/assets-list-selected.png){width="700" zoomable="yes"}

Você pode realizar as seguintes ações em massa:

+++Mover ativos

1. No banner de seleção, clique em **Mover**.

   Esta ação abre a caixa de diálogo _[!UICONTROL Mover Assets]_, que lista os nomes dos ativos selecionados e permite selecionar a pasta _destino_ para onde você deseja mover esses ativos.

1. Selecione uma pasta.

   As atualizações de caminho ao lado de _[!UICONTROL Ativos selecionados serão movidas para:]_.

1. Clique em **[!UICONTROL Mover]**.

+++

+++Excluir ativos

>[!NOTE]
>
>É possível aplicar uma exclusão em massa para no máximo 20 ativos selecionados.

1. No banner de seleção, clique em **[!UICONTROL Excluir]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

   Se qualquer um dos ativos selecionados estiver em uso no momento, a remoção desse ativo será anulada e uma mensagem de alerta será exibida.

+++

## Criar uma pasta

1. Na página de listagem _[!UICONTROL Assets]_, clique em **[!UICONTROL Criar Pasta]** na parte superior direita.

1. Na caixa de diálogo, digite o nome da pasta e selecione a pasta de destino (principal) da nova pasta.

   Os nomes das pastas devem ser exclusivos, com no máximo 100 caracteres, e não podem conter caracteres especiais, como `;`, `:`, `\`, `|`.

   ![Caixa de diálogo Criar pasta](./assets/assets-create-folder-dialog.png){width="500"}

1. Clique em **[!UICONTROL Adicionar]**.

## Aplicar ações no nível da pasta

É possível aplicar ações a uma pasta ou a ativos dentro dela. Clique no ícone de reticências (**...**) da pasta para revelar as opções de ações nela.

![Aplicar ações a uma pasta ou a ativos dentro dela](./assets/assets-folder-menu-options.png){width="500"}

Você pode executar as seguintes ações no nível da pasta:

+++Adicionar ativos

1. Escolha **[!UICONTROL Adicionar ativos]** para carregar arquivos de imagem para a pasta.

1. Na caixa de diálogo _[!UICONTROL Adicionar ativos]_, arraste e solte os arquivos do seu sistema. Você também pode clicar no link para usar seu sistema de arquivos para selecionar os arquivos.

   Você pode adicionar ativos do seu sistema local de até 10 arquivos de cada vez. Você tem a opção de substituir arquivos ao fazer upload de um ou mais arquivos com um nome de arquivo existente.

   Os nomes de arquivo das imagens selecionadas são exibidos na caixa de diálogo. Os nomes dos arquivos do ativo devem ser exclusivos (em várias pastas). Uma mensagem de erro será exibida se um arquivo com o nome já existir. Os nomes podem ter no máximo 100 caracteres e não podem conter caracteres especiais (como `;`, `:`, `\` e `|`).

1. Clique em **[!UICONTROL Adicionar]**.

+++

+++Criar uma subpasta

1. Escolha **[!UICONTROL Criar pasta]**.

1. Na caixa de diálogo, digite o nome da pasta.

   Os nomes das pastas devem ser exclusivos, com no máximo 100 caracteres, e não podem conter caracteres especiais, como `;`, `:`, `\`, `|`.

1. Clique em **[!UICONTROL Adicionar]**.

+++

+++Renomear a pasta

1. Escolha **[!UICONTROL Renomear]**.

1. Na caixa de diálogo, digite o nome da nova pasta.

   Os nomes das pastas devem ser exclusivos, com no máximo 100 caracteres, e não podem conter caracteres especiais, como `;`, `:`, `\`, `|`.

1. Clique em **[!UICONTROL Salvar]**.

+++

+++Mover a pasta

1. Para mover a pasta para outra pasta pai, escolha **[!UICONTROL Mover]**.

1. Na caixa de diálogo, selecione a pasta de destino como o novo pai da subpasta.

1. Clique em **[!UICONTROL Mover]**.

   Se você tentar mover uma pasta para uma de suas próprias subpastas (dentro da estrutura da pasta selecionada), uma mensagem de erro será exibida e a movimentação será cancelada.

+++

+++Excluir a pasta

1. Escolha **[!UICONTROL Excluir]**.

1. No diálogo de confirmação, clique em **[!UICONTROL Excluir]**.

Se qualquer um dos ativos na pasta estiver em uso no momento, a ação abrirá uma caixa de diálogo de alerta para informá-lo de que ele não pode ser excluído. Clique em **[!UICONTROL OK]**, que interrompe a remoção.

+++

+++Converter em uma pasta de arquivo morto

O arquivamento de uma pasta torna os arquivos dentro dela não pesquisáveis. Use a função de arquivamento para arquivos de ativos que você não deseja que o membro da sua equipe use a partir de agora, como um selo promocional de evento desatualizado ou conteúdo sazonal. Posteriormente, você poderá desarquivar uma pasta se quiser que o conteúdo fique disponível novamente.

* Escolha **[!UICONTROL Converter para pasta de arquivo morto]**. Um banner de confirmação é exibido para confirmar que o status da pasta é alterado para arquivado.

* Escolha **[!UICONTROL Desarquivar pasta]**. Um banner de confirmação é exibido para confirmar que o status da pasta foi alterado para desarquivado.

+++

## Usar ativos no conteúdo de email

O Assets pode ser usado no email da sua equipe, no modelo de email ou na criação de fragmentos visuais no editor de conteúdo visual.

Na interface do editor visual, selecione o ícone _Seletor de ativos_ na barra lateral esquerda.

![Ativos selecionados](./assets/content-assets-selector-icon.png){width="700" zoomable="yes"}

Essa ação altera o painel de ferramentas que exibe uma lista dos ativos disponíveis. Há vários métodos para adicionar um ativo de imagem à tela visual:

* Arraste e solte uma miniatura de imagem da navegação à esquerda.

* Adicione um componente de imagem à tela e clique em **[!UICONTROL Procurar]** para abrir a caixa de diálogo _[!UICONTROL Selecionar ativo da Adobe Marketo Engage]_.

  ![Use os filtros e o campo de pesquisa para localizar o ativo necessário](./assets/assets-select-dialog-marketo.png){width="700" zoomable="yes"}

  Na caixa de diálogo, é possível escolher uma imagem do repositório selecionado. Clique em **[!UICONTROL Selecionar]** para adicionar o ativo.

  Há ferramentas disponíveis para ajudar a localizar o ativo necessário:

   * Clique no ícone _Filtro_ na parte superior esquerda para filtrar os itens exibidos de acordo com seus critérios.

   * Digite texto no campo _Pesquisa_ para filtrar os itens exibidos para uma correspondência do nome do ativo.

  ![Use os filtros e o campo de pesquisa para localizar o ativo necessário](./assets/assets-select-dialog-marketo-filtered.png){width="600" zoomable="yes"}
