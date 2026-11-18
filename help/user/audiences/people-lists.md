---
title: Listas de pessoas
description: Saiba mais sobre listas de pessoas e como navegar, exibir, editar, excluir e usá-las no Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# Listas de pessoas

No [!DNL Journey Optimizer B2B Edition], uma lista de pessoas é uma coleção nomeada de perfis de pessoas que você pode reutilizar em suas jornadas. Em vez de recriar o mesmo conjunto de filtros em cada jornada, defina o grupo de pessoas uma vez e faça referência a ele onde for necessário. Por exemplo, use uma lista de pessoas para excluir a equipe interna ou os clientes existentes de uma jornada de criação, ou para rastrear as pessoas que concluíram uma etapa em uma jornada para que outra jornada possa agir sobre elas.

Há dois tipos de listas de pessoas:

* **[!UICONTROL Estático]** - A associação só é alterada quando você adiciona ou remove pessoas explicitamente. Você pode adicionar pessoas aplicando um conjunto de filtros para preencher a lista com base nos dados atuais da pessoa, ou adicionar e remover pessoas por meio de uma conta ou jornada de pessoa. Consulte [Listas estáticas de pessoas](./people-lists-static.md).
* **[!UICONTROL Dinâmico]** - Você define um conjunto de regras (filtros) para preparar automaticamente a lista. A lista é atualizada dinamicamente à medida que as pessoas se tornam qualificadas ou desqualificadas para a definição de regras. Consulte [Listas dinâmicas de pessoas](./people-lists-dynamic.md).

Você pode [usar listas de pessoas em jornadas de conta e jornadas de pessoa](./people-lists-journeys.md) para dividir caminhos com base na associação de listas e para adicionar ou remover pessoas de listas estáticas.

>[!NOTE]
>
>As listas de pessoas incluem perfis de pessoas que já estão sincronizados e disponíveis no [!DNL Journey Optimizer B2B Edition]. Os perfis não são lidos diretamente de [!DNL Adobe Experience Platform] públicos-alvo quando a lista é avaliada.

## Acessar e procurar listas de pessoas {#access-browse}

Acesse listas de pessoas na navegação à esquerda para exibir, criar e gerenciar a associação à lista.

>[!AVAILABILITY]
>
>As seguintes permissões de produto controlam o acesso a listas de pessoas:
>
>* [!UICONTROL Gerenciar listas de pessoas B2B] - Exibir, criar, editar e excluir listas de pessoas.
>* [!UICONTROL Exibir Listas de Pessoas B2B] - Exibir listas de pessoas e seus membros (somente leitura).
>
>Para obter informações sobre como atribuir permissões, consulte [Acesso e permissões do usuário](../admin/user-management.md#b2b-product-permissions).

* Na navegação à esquerda, expanda **[!UICONTROL Contas]** e selecione **[!UICONTROL Listas de pessoas]**.

* Selecione **[!UICONTROL Listas dinâmicas]** ou **[!UICONTROL Listas estáticas]** para alternar entre os dois tipos de lista.

* Digite texto no campo _Pesquisa_ na parte superior da lista para filtrar a lista exibida por nome.

  ![Acesse listas de pessoas para gerenciar seus públicos-alvo de nível de pessoa](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* Clique no ícone _Configurações de coluna_ ( ![Ícone de configurações de coluna](../assets/do-not-localize/icon-column-settings-new.svg) ) no canto superior direito para selecionar ou limpar as colunas exibidas.

* Para alterar a largura de uma coluna, arraste o divisor entre os cabeçalhos da coluna.

Cada guia inclui as colunas **[!UICONTROL Nome]**, **[!UICONTROL Última atualização]**, **[!UICONTROL Atualização por]**, **[!UICONTROL Criação em]** e **[!UICONTROL Criação por]**. Clique no nome da lista de pessoas para exibir seus detalhes.

Nessa página, também é possível:

* Criar novas listas dinâmicas e estáticas.
* Abrir uma lista e [examinar membros atuais](#view-list-members).
* Clique no ícone _Mais ações_ ( **...** ) para obter uma lista e escolha [editar](#edit-list-properties) ou [excluir](#delete-people-list).

## Criar uma lista de pessoas {#create-people-list}

1. Clique em **[!UICONTROL Criar lista]** na parte superior direita da página _[!UICONTROL Listas de pessoas]_.

   ![Caixa de diálogo Criar lista de pessoas](./assets/people-list-create-dialog.png){width="450"}

1. Insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) para a lista.

   O nome pode incluir até 180 caracteres e deve ser exclusivo entre as listas do mesmo tipo. A descrição pode incluir até 2.000 caracteres.

1. Escolha a lista **[!UICONTROL Tipo]**:

   * [**[!UICONTROL Estático]**](./people-lists-static.md) - Os filtros de qualificação determinam a associação quando você os aplica à lista. A associação é atualizada somente quando você adiciona pessoas manualmente ou quando uma jornada as adiciona ou remove.
   * [**[!UICONTROL Dinâmico]**](./people-lists-dynamic.md) - Os filtros de qualificação determinam a associação dinamicamente. A associação é atualizada automaticamente.

1. Clique em **[!UICONTROL Criar]**.

   A nova lista de pessoas é aberta na página de detalhes e o editor de filtro é aberto para que você possa definir as pessoas para a lista. Para adicionar pessoas a uma lista estática, aplique um ou mais filtros. Para uma lista dinâmica, defina as regras para associação à lista.

## Exibir membros da lista {#view-list-members}

Na página de detalhes de uma lista de pessoas, a lista **[!UICONTROL Membros]** exibe as pessoas na lista. O número total de pessoas na lista é exibido na parte superior da tabela.

A tabela de membros inclui as seguintes colunas:

* **[!UICONTROL Nome]**
* **[!UICONTROL Endereço de email]**
* **[!UICONTROL Cargo]**
* **[!UICONTROL Empresa]**
* **[!UICONTROL Cancelamento de assinatura]**
* **[!UICONTROL Criado em]**
* **[!UICONTROL Última modificação]**

Por padrão, o sistema classifica os membros por **[!UICONTROL Última modificação]**, mostrando primeiro as pessoas modificadas mais recentemente. Você também pode classificar por **[!UICONTROL Nome]**, **[!UICONTROL Endereço de email]** ou **[!UICONTROL Criado em]**.

* Para localizar um membro específico, use o campo _Pesquisa_. Você pode pesquisar por nome, endereço de email ou empresa.
* Para escolher as colunas a serem exibidas, clique no ícone _Configurações de coluna_ e marque ou desmarque as caixas de seleção. A coluna _[!UICONTROL Name]_ é sempre exibida.
* Para ver a associação mais recente, use o menu _[!UICONTROL Mais]_ para escolher **[!UICONTROL Atualizar membros]**.
* Para exibir mais informações sobre uma pessoa, clique no nome dela para abrir a página [detalhes da pessoa](../accounts/person-details.md), onde você pode exibir seu resumo e atividades recentes.

## Editar propriedades da lista de pessoas {#edit-list-properties}

É possível alterar o nome e a descrição de uma lista estática ou dinâmica de pessoas.

1. Abra a caixa de diálogo _[!UICONTROL Editar lista]_ usando um dos seguintes métodos:

   * Na página _[!UICONTROL Listas de pessoas]_, clique no ícone _Mais ações_ ( **...** ) da lista e escolha **[!UICONTROL Editar]**.
   * Na página de detalhes da lista, clique em **[!UICONTROL Editar propriedades da lista]**.

1. Atualize o **[!UICONTROL Nome]** ou a **[!UICONTROL Descrição]**.

1. Clique em **[!UICONTROL Salvar]**.

## Excluir uma lista de pessoas {#delete-people-list}

>[!IMPORTANT]
>
>A exclusão de uma lista de pessoas é permanente e não pode ser desfeita. Não é possível excluir uma lista de pessoas que está sendo usada por uma jornada ativa.

1. Exclua a lista usando um dos seguintes métodos:

   * Na página _[!UICONTROL Listas de pessoas]_, clique no ícone _Mais ações_ ( **...** ) ao lado do nome da lista e escolha **[!UICONTROL Excluir]**.
   * Na página de detalhes da lista, clique em **[!UICONTROL Excluir lista]**.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.
