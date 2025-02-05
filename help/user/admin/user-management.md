---
title: Gerenciamento de usuários
description: Saiba como atribuir membros da equipe aos perfis de produto do Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 2d9a58182f8ca3aec9e806e343571b14f22456f1
workflow-type: tm+mt
source-wordcount: '1838'
ht-degree: 1%

---

# Gerenciamento de usuários

Após a conclusão do provisionamento e a vinculação das sandboxes, conclua as etapas a seguir para fornecer acesso ao Adobe Journey Optimizer B2B edition para sua equipe e usuários.

1. [Crie um perfil de produto Marketo Engage](#marketo-engage-profile) no Admin Console (somente nova instância Marketo Engage).
1. [Criar um grupo de usuários](#create-user-group) no Admin Console.
1. [Edite as funções internas](#edit-roles) ou [crie uma função personalizada](#create-a-custom-role) com permissões do Journey Optimizer B2B edition.
1. [Adicionar usuários](#add-users) ou [grupos](#add-user-groups-to-a-role) às funções.

Como administrador, você pode concluir essas tarefas no Adobe Admin Console, que é um local central para administrar e gerenciar licenças e usuários do produto Adobe. No Admin Console, é possível criar e gerenciar usuários em um único local em vez de em várias soluções individuais. Consulte a página [visão geral do Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para saber mais sobre suas funções e recursos.

## Acesse o Admin Console

Antes de usar o Admin Console para administrar os usuários da sua equipe, é necessário garantir que você possa acessar o Admin Console e ter as permissões apropriadas.

1. Como administrador do sistema, você deve receber vários emails do Adobe como parte do processo de integração.

   Procure o email de boas-vindas que fornece informações sobre o nome da organização à qual você recebeu acesso.

1. Clique no link **[!UICONTROL Introdução]** no email de boas-vindas para acessar o Admin Console.

   Se você não conseguir localizar o email, abra um navegador diretamente no Admin Console em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Faça logon usando sua Adobe ID.

   Depois de fazer logon, você verá a página _Visão geral_ da Adobe Admin Console.

1. Se você tiver acesso a várias organizações, verifique se fez logon na organização correta.

   Para alterar a organização, clique no nome dela no canto superior direito e escolha a organização que você precisa acessar.

1. Selecione **[!UICONTROL Administradores]** no cartão _[!UICONTROL Usuários]_ para verificar se você é um administrador do sistema.

   ![visão geral do Admin Console - clique em Administradores](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Pesquise inserindo seu email, nome de usuário, nome ou sobrenome do Adobe ID.

   * Se o acesso estiver configurado corretamente, a pesquisa retornará seu registro.

   * Se o valor na coluna **[!UICONTROL FUNÇÃO DE ADMINISTRADOR]** mostrar `System`, isso quer dizer que você (ou o usuário mostrado) é um administrador do sistema.

## Criar o perfil de produto Marketo Engage {#marketo-engage-profile}

Ao conceder aos usuários acesso a uma solução Adobe, você não deseja necessariamente conceder acesso total a eles. Os perfis de produto permitem que cada solução tenha seu próprio conjunto de permissões do usuário. Use o Admin Console para atribuir perfis de produto.

Para obter mais informações sobre como usar perfis de produtos para direitos de usuário, consulte [Gerenciar perfis de produto para usuários corporativos](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html){target="_blank"} na documentação do Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

>[!NOTE]
>
>Um administrador de sistema Admin Console ou administrador de produto Marketo Engage pode executar essas etapas.

1. Faça logon em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Selecione a guia **[!UICONTROL Produtos]**.

1. Abra a instância de Marketo Engage na qual deseja adicionar o perfil e clique em **[!UICONTROL Novo perfil]**.

   ![Admin Console - Instância Marketo Engage - Novo perfil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Insira um nome de perfil de produto, como _Usuário Padrão_.

1. Clique em **Avançar** e depois em **Salvar**.

## Criar um grupo de usuários {#create-user-group}

Um grupo de usuários é uma coleção de usuários aos quais é concedido um conjunto compartilhado de permissões. Você pode adicionar ou remover usuários em seu grupo de usuários. As permissões do grupo permanecem as mesmas enquanto os usuários no grupo são alterados.

Para obter mais informações sobre como os grupos de usuários são usados para gerenciar permissões, consulte [Gerenciar grupos de usuários](https://helpx.adobe.com/br/enterprise/using/user-groups.html){target="_blank"} na documentação do Admin Console.

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

1. Faça logon em [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Selecione a guia **[!UICONTROL Usuários]**.

1. Escolha **[!UICONTROL Grupos de Usuários]** na navegação à esquerda.

1. Clique em **[!UICONTROL Novo grupo de usuários]** na parte superior direita.

1. Insira um nome para o grupo de usuários, como _Usuários padrão_ e clique em **[!UICONTROL Salvar]**.

1. Clique no grupo de usuários que acabou de criar.

1. Selecione a guia **[!UICONTROL Perfis de produto atribuídos]** e clique em **[!UICONTROL Atribuir perfil]**.

1. Clique em **+** e adicione cada instância dos seguintes produtos:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Padrão-Todos-Usuários]
   * [!UICONTROL Coleta de dados do Adobe Experience Platform]
   * [!UICONTROL Acesso integral à Coleção de Dados]

   ![Admin Console - grupo de usuários - adicionar produtos](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.

## Adicionar usuários a um grupo

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

Para obter informações sobre o gerenciamento de usuários, consulte [Admin Console usuários](https://helpx.adobe.com/br/enterprise/using/user-groups.html) na documentação do Admin Console.

1. Ir para [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Em _[!UICONTROL Links rápidos]_, clique em **[!UICONTROL Adicionar usuários]**.

1. Adicionar cada usuário:

   * Insira o endereço de email, o nome e o sobrenome do usuário.

     ![Experience Platform - adicionar perfis para a nova função](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Para **[!UICONTROL Grupos de usuários]**, clique em **+**.

   * Selecione o grupo de usuários criado anteriormente.

   * Clique em **[!UICONTROL Aplicar]**.

1. Clique em **[!UICONTROL Salvar]**.

## Editar funções para permissões de produto {#edit-roles}

As permissões são direitos unitários que permitem definir as autorizações atribuídas a um perfil de produto. Cada permissão é coletada em um recurso, como jornadas ou grupos de compras, que representa as diferentes funcionalidades ou objetos no Journey Optimizer B2B edition.

A área _Permissões_ do Adobe Experience Platform é onde os administradores podem definir funções de usuário e políticas de acesso para gerenciar permissões de acesso para recursos e objetos em um aplicativo de produto. Neste aplicativo, você pode criar e gerenciar funções, bem como atribuir as permissões de recurso desejadas para essas funções. As permissões também permitem gerenciar sandboxes e usuários associados a uma função específica.

Para obter mais informações sobre permissões de função no Experience Platform, consulte [Gerenciar permissões para uma função](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} na documentação do Experience Platform.

### Permissões de produto B2B

As seguintes permissões controlam o acesso aos recursos do Journey Optimizer B2B edition:

| Categoria | Descrição | Permissões |
| -------- | ----------- | ---------- |
| Listas de contas B2B | Configure, gerencie, visualize e publique permissões para listas de contas B2B. Essas permissões incluem ações como adicionar, remover, importar e excluir contas de listas de contas. | <li>Gerenciar listas de contas B2B |
| Configurações do administrador B2B | Configure, gerencie e visualize permissões para configurações administrativas B2B. Essas permissões incluem conexões de gerenciamento de ativos digitais, repositórios de ativos e eventos. | <li>Gerenciar configurações de administrador B2B |
| Assets B2B | Configure, gerencie e visualize permissões para ativos B2B. Essas permissões incluem emails, SMS, landing pages, fragmentos, modelos e imagens. | <li>Gerenciar Assets B2B <li>Gerenciar modelos B2B <li>Gerenciar fragmentos B2B |
| Grupos de compra B2B | Configure, gerencie e visualize permissões para grupos de compra B2B. Essas permissões incluem interesses de solução, modelos de funções e status do grupo de compras. | <li>Gerenciar grupos de compra B2B |
| Configurações do canal B2B | Configure, gerencie e visualize permissões para configurações de canal B2B. Essas permissões incluem configurações para limites de comunicação, credenciais de API e configurações de segurança. | <li>Gerenciar configurações de canais B2B |
| Painéis B2B | Configure e visualize permissões para painéis B2B. Essas permissões incluem envolvimento de conta, estágios de grupo de compras, contas de surging e cobertura de contato. | <li>Gerenciar painéis B2B |
| Jornadas B2B | Configure permissões de gerenciamento, visualização e publicação para jornadas B2B. Essas permissões incluem ações de conta e pessoa, ouvintes de eventos e caminhos divididos | <li>Gerenciar Jornadas B2B |

### Funções integradas B2B

Quando sua organização tiver o produto Journey Optimizer B2B edition provisionado, o Experience Platform incluirá um conjunto de funções integradas (padrão) que você poderá usar para gerenciar o acesso aos recursos do produto:

| Função | Permissões |
| ---- | ----------- |
| Gerenciador de Jornada B2B | <li>Gerenciar Jornadas B2B <li>Gerenciar grupos de compra B2B <li>Gerenciar listas de contas B2B <li>Exibir painel inteligente B2B <li>Exibir painel de insights B2B |
| Gerenciador de canal B2B | <li>Gerenciar Assets B2B <li>Gerenciar modelos B2B <li>Gerenciar fragmentos B2B |
| Administrador de sistema B2B | <li>Gerenciar configurações de canais B2B <li>Gerenciar configurações de administrador B2B |
| Usuário de vendas B2B | <li>Exibir painel inteligente |

### Editar permissões de função

Para funções integradas ou personalizadas, é possível decidir adicionar ou excluir permissões a qualquer momento. Se você modificar uma função padrão ou personalizada, isso afetará cada usuário atribuído à função.

No exemplo a seguir, você deseja adicionar permissões relacionadas ao recurso Jornada B2B para usuários atribuídos à função Gerenciador de canal B2B. Essa alteração permite que os usuários dessa função também gerenciem jornadas de conta.

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

_Para alterar as permissões de uma função:_

1. Vá para [experience.adobe.com](https://experience.adobe.com/).

1. No painel _[!UICONTROL Acesso rápido]_, selecione **[!UICONTROL Permissões]**.

   >[!NOTE]
   >
   >Se você não vir _[!UICONTROL Permissões]_, talvez precise clicar em **[!UICONTROL Exibir tudo]** e selecioná-lo nos aplicativos disponíveis.

   ![Experience Platform - Permissões de acesso](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Selecione **[!UICONTROL Funções]** na navegação à esquerda.

1. Clique no nome da função **_Gerenciador de canal B2B_**.

1. Na página de detalhes, clique em **[!UICONTROL Editar]** na parte superior direita.

   ![Experience Platform - edite a função](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   No editor de funções, o menu _[!UICONTROL Recursos]_ exibe a lista de recursos que se aplicam aos produtos de aplicativos alimentados por Experience Cloud - Plataforma.

   Você pode digitar _B2B_ na ferramenta de pesquisa para filtrar a lista de permissões de produtos B2B.

1. Clique no ícone _Adicionar_ (**+**) para o recurso B2B do Jornada.

   ![Experience Platform - edite a função](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. No cartão de permissões _[!UICONTROL Jornada B2B]_, selecione **[!UICONTROL Gerenciar Jornadas de Conta B2B]**.

1. Clique em **[!UICONTROL Salvar]**.

   ![Experience Platform - edite a função](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Fechar]** para retornar à página de detalhes.

### Adicionar usuários a uma função

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

1. Abra os detalhes da função e selecione a guia **[!UICONTROL Usuários]**.

   Esta guia exibe uma lista de todos os usuários atribuídos à função.

1. Clique em **[!UICONTROL Adicionar usuários]**.

   ![Experience Platform - adicionar usuários à função](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Adicionar usuários]_, localize e selecione os usuários que deseja adicionar à função.

   * Você pode usar a ferramenta Search para filtrar a lista de usuários.

   * Marque a caixa de seleção de cada usuário.

   ![Experience Platform - Caixa de diálogo Adicionar usuários](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]** quando tiver selecionado todos os usuários que deseja adicionar.

### Adicionar grupos de usuários a uma função

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

Para obter informações sobre o gerenciamento de usuários, consulte [Admin Console usuários](https://helpx.adobe.com/br/enterprise/using/user-groups.html) na documentação do Admin Console.

1. Abra os detalhes da função e selecione a guia **[!UICONTROL Grupos de usuários]**.

   Esta guia exibe uma lista de todos os grupos de usuários atribuídos à função.

1. Clique em **[!UICONTROL Adicionar grupos]**.

   ![Experience Platform - adicionar usuários à função](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Na caixa de diálogo _[!UICONTROL Adicionar grupos]_, localize e selecione os grupos que deseja adicionar à função.

   * Você pode usar a ferramenta Pesquisar para filtrar a lista de grupos de usuários.

   * Marque a caixa de seleção para cada grupo de usuários.

   ![Experience Platform - Caixa de diálogo Adicionar grupos](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]** quando tiver selecionado todos os usuários que deseja adicionar.

## Criar uma função personalizada

>[!NOTE]
>
>Um administrador de sistema Admin Console pode executar essas etapas.

1. Selecione **[!UICONTROL Funções]** na navegação à esquerda e selecione **[!UICONTROL Criar função]**.

1. Na caixa de diálogo _[!UICONTROL Criar nova função]_, digite um nome para a função, como _Profissionais de marketing B2B_, e uma descrição (opcional).

1. Clique em **[!UICONTROL Confirmar]**.

1. Selecione suas sandboxes.

   ![Experience Platform - adicionar sandboxes para a nova função](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Adicione as permissões de perfil:

   * Na lista _[!UICONTROL Recursos]_ à esquerda, localize o item **[!UICONTROL Gerenciamento de Perfil]** e clique no ícone _Adicionar_ (**+**) para adicionar o atributo.

   * Para o atributo, adicione as seguintes permissões:
      * [!UICONTROL Exibir segmentos]
      * [!UICONTROL Gerenciar segmentos]
      * [!UICONTROL Exibir perfis]
      * [!UICONTROL Gerenciar perfis]
      * [!UICONTROL Exibir perfil B2B]
      * [!UICONTROL Gerenciar perfil B2B]

   ![Experience Platform - adicionar perfis para a nova função](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Adicionar permissões de produto B2B:

   Consulte a lista de [permissões de produto B2B](#b2b-product-permissions) para determinar quais recursos de produto você deseja para a função.

   Na lista _[!UICONTROL Recursos]_ à esquerda, localize os itens **[!UICONTROL B2B]** e clique no ícone _Adicionar_ (**+**) para adicionar cada atributo que você deseja habilitar para a função.

   Você pode digitar _B2B_ na ferramenta de pesquisa para filtrar a lista de permissões de produtos B2B.

1. Clique em **[!UICONTROL Salvar]** na parte superior direita.

1. Vá para os detalhes da função e selecione a guia **[!UICONTROL Grupos de usuários]**.

1. Clique em **[!UICONTROL Adicionar grupos]**.

   ![Experience Platform - adicionar perfis para a nova função](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Marque a caixa de seleção ao lado do grupo de usuários criado anteriormente no Admin Console.

1. Clique em **[!UICONTROL Salvar]**.
