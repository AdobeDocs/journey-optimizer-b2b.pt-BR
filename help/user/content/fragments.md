---
title: Fragmentos
description: Saiba como criar e usar fragmentos de conteúdo visual como componentes reutilizáveis para emails e modelos de email no Adobe Journey Optimizer B2B Edition.
feature: Content, Email Authoring
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 0%

---

# Fragmentos

Um fragmento é um componente reutilizável que pode ser referenciado em um ou mais emails e modelos de email no Adobe Journey Optimizer B2B Edition. Geralmente, é um bloco de conteúdo (texto, imagem ou ambos) que pode ser pré-criado e inserido rapidamente em um email ou modelo de email. Com essa funcionalidade, você pode pré-criar vários blocos de conteúdo personalizados que podem ser usados pelos membros da equipe de marketing para reunir conteúdo de email para um processo de design aprimorado. Casos de uso comuns incluem blocos de conteúdo de cabeçalho/rodapé para email, banners para convites de eventos e saudações sazonais.

Para aproveitar ao máximo os fragmentos em seus workflows:

* _Criar seus próprios fragmentos_ - Crie fragmentos visuais, do zero ou salvando o conteúdo como fragmento a qualquer momento do editor de conteúdo visual.
* _Reutilizar os fragmentos_s - Use-os quantas vezes forem necessárias no conteúdo.

## Fragmentos visuais

Fragmentos visuais são blocos visuais predefinidos criados usando o editor de conteúdo visual, que podem ser reutilizados em vários emails ou modelos de email. O escopo atual do Journey Optimizer B2B Edition e esta documentação são somente os fragmentos visuais. Fragmentos baseados em expressão ainda não são compatíveis com o Journey Optimizer B2B Edition.

## Acessar e gerenciar fragmentos

Para acessar fragmentos visuais na edição B2B do Adobe Journey Optimizer, vá para a navegação à esquerda e clique em **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**. Essa ação abre uma página de listagem com todos os fragmentos criados na instância listada em uma tabela.

![Acessar a biblioteca de fragmentos](./assets/fragments-list.png){width="700" zoomable="yes"}

A tabela é classificada pela coluna _[!UICONTROL Modificado]_, com os fragmentos atualizados mais recentemente no topo da lista por padrão. Clique no título da coluna para alterar entre crescente e decrescente.

Procure qualquer fragmento inserindo uma string de texto na barra de pesquisa para uma correspondência pelo nome do fragmento. Clique no ícone _Filtro_ para filtrar os itens exibidos de acordo com seus critérios especificados.

![Filtrar os fragmentos exibidos](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

Personalize as colunas que deseja exibir na tabela clicando no ícone _Personalizar tabela_ na parte superior direita. Selecione as colunas a serem exibidas e clique em **[!UICONTROL Aplicar]**.

## Criar fragmentos

Você pode criar novos fragmentos visuais no Journey Optimizer B2B Edition clicando em **[!UICONTROL Criar fragmento]** na parte superior direita.

1. Na caixa de diálogo _[!UICONTROL Criar fragmento]_, insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** úteis (opcional).

   Requisitos de fragmento:

   * Nome - Máximo de 100 caracteres; deve ser exclusivo, não diferencia maiúsculas de minúsculas

   * Descrição - Máximo de 300 caracteres

   * Alpha, numérico, caracteres especiais são permitidos

   * Caracteres reservados não são permitidos: `\ / : * ? " < > |`

   ![Caixa de diálogo Criar fragmento](./assets/assets-fragments-create-dialog.png){width="500"}

1. Clique em **[!UICONTROL Criar]**.

   O editor de conteúdo visual é aberto com uma tela vazia. Para criar um fragmento usando o editor de conteúdo visual, consulte os tópicos de criação de conteúdo:

<!-- To be linked to the corresponding sections on this page: Adobe Journey Optimizer B2B Edition - Email Templates

Adding structure & content
Adding assets
Navigating the layers
Previewing & editing URLs
View options
More options -->

## Exibir detalhes do fragmento

Clique no nome de qualquer fragmento na página da lista para abrir a página de detalhes do fragmento.

Aqui, você pode optar por editar o fragmento, renomear o fragmento ou atualizar a descrição do fragmento (fazer atualizações e clicar fora da caixa de nome/descrição para salvar automaticamente as alterações).

Clique em **[!UICONTROL Editar]** para abrir o fragmento no editor de conteúdo visual.

Saia da exibição a qualquer momento clicando na seta _Voltar_ na parte superior esquerda, que o retorna à página da lista _Fragmentos_.

## Exibir fragmento usado por referências

Na página de detalhes do fragmento, clique na guia **[!UICONTROL Usado por]** para exibir detalhes sobre onde o fragmento é usado atualmente no Journey Optimizer B2B Edition, em emails, modelos de email e fragmentos.

>[!IMPORTANT]
>
>Qualquer fragmento que esteja sendo usado atualmente por qualquer email ou modelo de email não pode ser excluído.

As referências são exibidas de acordo com a categoria: _Email_ ou _Modelo de email_. Os emails no Journey Optimizer B2B Edition são incorporados e criados nas jornadas de conta, de modo que a jornada principal do email que usa o fragmento é exibida nas referências.

Clique no link para abrir o email ou modelo de email correspondente onde o fragmento é usado.

## Excluir fragmentos

Qualquer fragmento que esteja sendo usado atualmente por qualquer email ou modelo de email não pode ser excluído, portanto, verifique as referências _usado por_ antes de iniciar a remoção de um fragmento. Além disso, uma remoção não pode ser desfeita, portanto, verifique antes de iniciar uma ação de exclusão.

É possível excluir um fragmento usando um dos seguintes métodos:

* Nos detalhes do fragmento à direita, clique em **[!UICONTROL Excluir]**.
* Na página de listagem _[!UICONTROL Fragmentos]_, clique nas reticências ao lado do fragmento e escolha **[!UICONTROL Excluir]**.

Essa ação abre uma caixa de diálogo de confirmação. Você pode anular o processo clicando em **[!UICONTROL Cancelar]** ou em **[!UICONTROL Excluir]** para confirmar a exclusão.

Se o fragmento estiver em uso no momento, a ação abrirá uma caixa de diálogo informativa que o alerta de que não pode ser excluído. Clique em **[!UICONTROL OK]**, que interrompe a exclusão.

## Editar fragmentos

É possível editar um fragmento usando um dos seguintes métodos:

* Nos detalhes do fragmento à direita, clique em **[!UICONTROL Editar]**.
* Na página de listagem _[!UICONTROL Fragmentos]_, clique nas reticências ao lado do fragmento e escolha **[!UICONTROL Editar]**.

Esta ação abre o fragmento em um editor de conteúdo visual, no qual você pode editar o fragmento usando qualquer um dos recursos para [criar um fragmento](#create-fragments).

## Duplicar fragmentos

É possível duplicar um fragmento usando um dos seguintes métodos:

* Nos detalhes do fragmento à direita, clique em **[!UICONTROL Duplicar]**.
* Na página de listagem _[!UICONTROL Fragmentos]_, clique nas reticências ao lado do fragmento e escolha **[!UICONTROL Duplicar]**.

Na caixa de diálogo do, digite um nome útil (exclusivo) e uma descrição. Clique em **[!UICONTROL Duplicar]** para concluir a ação.

O fragmento duplicado (novo) aparece na listagem _Fragmentos_.

## Salvar um fragmento do email ou do editor de modelo

Sempre que você estiver no editor de conteúdo visual para criar/editar um email ou modelo de email, poderá optar por salvar todo o conteúdo ou partes dele como um fragmento para que ele fique disponível para reutilização.

1. Quando tiver conteúdo a ser salvo como fragmento, clique em **[!UICONTROL Mais]** e escolha **[!UICONTROL Salvar como fragmento]**.

1. Selecione os diferentes elementos a serem incluídos no fragmento.

   Selecione várias estruturas mantendo pressionado o botão CTRL

   Você só pode selecionar estruturas adjacentes entre si e a interface não permite selecionar elementos não adjacentes.

1. Com o conteúdo selecionado, clique em **[!UICONTROL Criar]** na parte superior direita.

1. Na caixa de diálogo, insira um nome e uma descrição úteis para o fragmento. Depois clique em **[!UICONTROL Criar]**.

   O novo fragmento é exibido na página de listagem _Fragmentos_ e também está disponível para uso em emails e modelos de email.

## Adicionar fragmentos visuais a um email ou modelo

Os fragmentos são projetados para reutilização e podem ser inseridos para criação de template de email e email. Você pode adicionar até 30 fragmentos em um determinado email ou modelo. Os fragmentos podem ser aninhados somente até um nível.

>[!BEGINTABS]

>[!TAB Adicionar fragmentos a um email]

1. Navegue até Jornadas de Conta e abra uma jornada existente ou crie uma nova jornada.

1. Crie um nó &quot;Realizar uma ação > Ação de pessoas > Enviar email&quot;.

1. Criar ou editar conteúdo de email do nó.

1. Arraste e solte um item do menu Componentes para fornecer uma _estrutura_ para o fragmento.

1. Para abrir a lista de fragmentos, clique no ícone _Fragmentos_.

   Você pode:
   * Classifique a listagem.
   * Procurar, Pesquisar, Filtrar a listagem.
   * Alternar entre as visualizações em Miniatura e em Lista.
   * Atualize a lista para refletir qualquer um dos fragmentos criados recentemente.

1. Arraste e solte qualquer um dos fragmentos no espaço reservado do componente de estrutura.

   O editor renderiza o fragmento na seção/elemento da estrutura de email.

O conteúdo do fragmento é atualizado dinamicamente na estrutura para renderizar um visual de como o conteúdo aparece no email.

Se quiser adicionar o fragmento para que ele ocupe o layout horizontal inteiro no email, adicione uma estrutura de coluna 1:1 e, em seguida, arraste e solte o fragmento nele.

Depois que o email é salvo, ele é exibido na página de detalhes do fragmento > na seção Usado por. Os fragmentos adicionados a um email não são editáveis no email — o conteúdo é definido pelo fragmento de origem.

>[!TAB Adicionar fragmentos a um modelo de email]

1. Na navegação à esquerda, clique em **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Modelos]**.

1. Crie um novo modelo ou abra um modelo de email existente e clique em **[!UICONTROL Editar Modelo de Email]**.

1. Arraste e solte um item do menu Componentes para fornecer uma _estrutura_ para o fragmento.

1. Para abrir a lista de fragmentos, clique no ícone _Fragmentos_.

   Você pode:
   * Classifique a listagem.
   * Procurar, Pesquisar, Filtrar a listagem.
   * Alternar entre as visualizações em Miniatura e em Lista.
   * Atualize a lista para refletir qualquer um dos fragmentos criados recentemente.

1. Arraste e solte qualquer um dos fragmentos no espaço reservado do componente de estrutura.

   O editor renderiza o fragmento na seção/elemento da estrutura do modelo de email.

1. Arraste e solte qualquer um dos fragmentos no espaço reservado do componente de estrutura.

   O editor renderiza o fragmento na seção/elemento da estrutura do modelo de email.

Se quiser adicionar o fragmento para que ele ocupe o layout horizontal inteiro no modelo de email, adicione uma estrutura de coluna 1:1 e, em seguida, arraste e solte o fragmento nele.

Depois que o modelo de email for salvo, ele aparecerá na página de detalhes do fragmento > _[!UICONTROL Usado por]_. Os fragmentos adicionados a um modelo de email não são editáveis no modelo — o conteúdo é definido pelo fragmento de origem.

>[!ENDTABS]

## Ações de fragmento durante a criação

Depois que um fragmento é adicionado a um email ou modelo de email, o conteúdo do fragmento não pode ser editado no email ou modelo. No entanto, você pode aplicar as seguintes ações:

* **[!UICONTROL Excluir]** - Esta ação remove o fragmento do conteúdo do email ou do modelo de email atual (a origem do fragmento não é afetada).
* **[!UICONTROL Atualizar]** - Esta ação atualiza o conteúdo do fragmento no email ou modelo de email atual. Isso é útil quando você deseja refletir qualquer edição recente no fragmento depois que ele foi adicionado ao email ou ao modelo de email.
* **[!UICONTROL Duplicar]** - Esta ação duplica o fragmento no mesmo email ou modelo de email no editor, com as mesmas dimensões e adicionada logo abaixo dele.
* **[!UICONTROL Abrir fragmento]** - Essa ação abre uma nova guia do navegador com a página e os detalhes do editor de fragmento.
* **[!UICONTROL Interromper herança]** - Esta ação interrompe a herança do fragmento (e suas alterações) da origem. Use esta ação para disponibilizar o conteúdo do fragmento como conteúdo independente e editável no modelo de email ou de email. Esta ação também remove o email ou o modelo de email da referência _Usado por_ do fragmento original.

Quando você seleciona o fragmento na página do editor, essas ações estão disponíveis na barra de ferramentas de contexto e no painel de propriedades à direita.
