---
title: Gerenciamento de usuários
description: Saiba como atribuir membros da equipe aos perfis de produto do Journey Optimizer B2B Edition.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# Gerenciamento de usuários

Após a conclusão do provisionamento e a vinculação das sandboxes, conclua as seguintes etapas para fornecer acesso ao Adobe Journey Optimizer B2B Edition para sua equipe e usuários.

1. [Crie um perfil de produto Marketo Engage](#marketo-engage-profile) no Admin Console (somente nova instância Marketo Engage).
1. [Criar um grupo de usuários](#create-user-group) no Admin Console.
1. [Criar uma função](#create-role) nas Permissões da AEP.
1. [Adicionar usuários](#add-users) no Admin Console.

Como administrador, você pode concluir essas tarefas no Adobe Admin Console, que é um local central para administrar e gerenciar licenças e usuários do produto Adobe. No Admin Console, é possível criar e gerenciar usuários em um único local em vez de em várias soluções individuais. Consulte a página [visão geral do Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para saber mais sobre suas funções e recursos.

## Acesse o Admin Console

Antes de usar o Admin Console para administrar os usuários da sua equipe, é necessário garantir que você possa acessar o Admin Console e ter as permissões apropriadas.

1. Como administrador do sistema, você deve receber vários emails do Adobe como parte do processo de integração.

   Procure o email de boas-vindas que fornece informações sobre o nome da organização à qual você recebeu acesso.

1. Clique no link **[!UICONTROL Introdução]** no email de boas-vindas para acessar o Admin Console.

   Se você não conseguir localizar o email, abra um navegador diretamente no Admin Console em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Faça logon usando sua Adobe ID.

   Depois de fazer logon, você verá a página Visão geral da Adobe Admin Console.

1. Se você tiver acesso a várias organizações, verifique se fez logon na organização correta.

   Para alterar a organização, clique no nome dela no canto superior direito e escolha a organização que você precisa acessar.

1. Selecione Administradores no cartão Usuários para verificar se você é um administrador do sistema.

1. Pesquise inserindo seu email, nome de usuário, nome ou sobrenome do Adobe ID.

   * Se o acesso estiver configurado corretamente, a pesquisa retornará seu registro.

   * Se o valor na coluna **[!UICONTROL FUNÇÃO DE ADMINISTRADOR]** mostrar `System`, isso quer dizer que você (ou o usuário mostrado) é um administrador do sistema.

## Criar o perfil de produto Marketo Engage {#marketo-engage-profile}

Ao conceder aos usuários acesso a uma solução Adobe, você não deseja necessariamente conceder acesso total a eles. Os perfis de produto permitem que cada solução tenha seu próprio conjunto de permissões do usuário. Use o Admin Console para atribuir perfis de produto.

>[!NOTE]
>
>Estas etapas só podem ser executadas por um administrador de sistema do Admin Console ou por um administrador de produto do Marketo Engage.

1. Faça logon em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Escolha Produtos > Marketo Engage.

1. Clique em Novo perfil e digite um nome de perfil de produto, como _Usuário Padrão_.

1. Clique em Avançar > Salvar

## Criar um grupo de usuários {#create-user-group}

Um grupo de usuários é uma coleção de usuários aos quais é concedido um conjunto compartilhado de permissões. Você pode adicionar ou remover usuários em seu grupo de usuários. As permissões do grupo permanecem as mesmas enquanto os usuários no grupo são alterados.

>[!NOTE]
>
>Essas etapas só podem ser executadas por um administrador de sistema Admin Console.

1. Faça logon em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Escolha **[!UICONTROL Usuários]** > **[!UICONTROL Grupos de Usuários]** > **[!UICONTROL Novo grupo de usuários]**.

1. Insira um nome para o grupo de usuários, como _Usuários padrão_ e clique em **[!UICONTROL Salvar]**.

1. Clique no grupo de usuários que acabou de criar.

1. Clique em **[!UICONTROL Perfis de produto atribuídos]** > **[!UICONTROL Atribuir perfil]**.

1. Selecione os seguintes produtos:
   * [!UICONTROL Marketo Engage - Usuário Padrão]
   * [!UICONTROL Adobe Experience Platform - AEP-Padrão-Todos-Usuários]
   * [!UICONTROL Coleta de dados do Adobe Experience Platform - Padrão]
   * [!UICONTROL Acesso integral à Coleção de Dados]

1. Clique em **[!UICONTROL Salvar]**.

## Criar uma função nas permissões da AEP {#create-role}

As permissões são direitos unitários que permitem definir as autorizações atribuídas a um perfil de produto. Cada permissão é coletada em um recurso, como jornadas ou grupos de compras, que representa as diferentes funcionalidades ou objetos no Journey Optimizer B2B Edition.

_Permissões_ é a área do Adobe Experience Platform em que os administradores podem definir funções de usuário e políticas de acesso para gerenciar permissões de acesso para recursos e objetos em um aplicativo de produto. Neste aplicativo, você pode criar e gerenciar funções, bem como atribuir as permissões de recurso desejadas para essas funções. As permissões também permitem gerenciar rótulos, sandboxes e usuários associados a uma função específica.

>[!NOTE]
>
>Para concluir as etapas a seguir, você deve ser um administrador de produto do Adobe Experience Platform.

1. Vá para [experience.adobe.com](https://experience.adobe.com/).

1. Selecione **[!UICONTROL Permissões]**.

   >[!NOTE]
   >
   >Se você não vir as Permissões, talvez seja necessário clicar em Exibir tudo e selecioná-las nos aplicativos disponíveis.

1. Selecione **[!UICONTROL Funções]** na navegação à esquerda e selecione **[!UICONTROL Criar função]**.

1. Na caixa de diálogo _[!UICONTROL Criar nova função]_, digite um nome para a função, como _Usuário Padrão_, e uma descrição (opcional).

1. Clique em **[!UICONTROL Confirmar]**.

1. Selecione suas sandboxes.

1. Adicione as permissões de perfil:

   * Na lista _[!UICONTROL Recursos]_ à esquerda, localize o item **[!UICONTROL Gerenciamento de Perfil]** e clique no ícone de adição (**+**) para adicionar o atributo.

   * Para o atributo, adicione as seguintes permissões:
      * [!UICONTROL Exibir segmentos]
      * [!UICONTROL Gerenciar segmentos]
      * [!UICONTROL Exibir perfis]
      * [!UICONTROL Gerenciar perfis]
      * [!UICONTROL Exibir perfil B2B]
      * [!UICONTROL Gerenciar perfil B2B]

1. Clique em **[!UICONTROL Salvar]** na parte superior direita.

1. Escolha **[!UICONTROL Grupos de usuários]** > **[!UICONTROL Adicionar grupos]**.

1. Marque a caixa de seleção ao lado do grupo de usuários criado anteriormente no Admin Console.

1. Clique em **[!UICONTROL Salvar]**.

## Adicionar usuários no Admin Console

>[!NOTE]
>
>Essas etapas só podem ser executadas por um administrador de sistema do Admin Console ou por um administrador de produto.

1. Ir para [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Clique em **[!UICONTROL Adicionar usuários]**.

1. Adicionar cada usuário:

   * Insira o endereço de email, o nome e o sobrenome do usuário.
   * Clique em [!UICONTROL Grupos de usuários].
   * Selecione o grupo de usuários criado anteriormente.

1. Clique em **[!UICONTROL Aplicar]**.

1. Clique em **[!UICONTROL Salvar]**.
