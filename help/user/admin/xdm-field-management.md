---
title: Gerenciamento de campo XDM
description: Use o gerenciamento de campo XDM para controlar os dados disponíveis para o Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Este recurso está atualmente em uma versão beta limitada na arquitetura simplificada"
source-git-commit: afac024e5eeb6b9d230c4292a6f37e92e16d29f6
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 1%

---


# Gerenciamento de campo XDM

Os campos do Experience Data Model (XDM) são elementos de esquema que fornecem dados para o aplicativo [!DNL Journey Optimizer B2B Edition]. Use campos XDM como filtros e restrições em nós de jornada, grupos de compra e para recursos de conteúdo, como personalização de email e conteúdo condicional.

Os esquemas definem campos com base em classes XDM padrão. As classes XDM padrão incluem Perfil individual, Conta comercial e Evento de experiência. Os esquemas relacionais também definem campos que permitem modelar dados estruturados de forma semelhante aos bancos de dados relacionais tradicionais.

Os esquemas do Adobe Experience Platform (AEP) normalmente contêm muitos campos em hierarquias complexas. Percorrer árvores de esquema XDM leva tempo. O gerenciamento de campo XDM simplifica a seleção de campos ao exibir apenas os campos relevantes para cada jornada. Os administradores controlam quais campos aparecem para os criadores de jornadas. Os administradores também definem os campos como somente leitura ou editáveis. Essas ações melhoram a eficiência durante o design da jornada.

Os administradores que entendem o XDM e colaboram com engenheiros de dados ou participantes da modelagem de dados da CDP (plataforma de dados de clientes B2B) devem usar as etapas a seguir para configurar as classes XDM para [!DNL Journey Optimizer B2B Edition].

>[!NOTE]
>
>O gerenciamento de campo XDM está disponível para ambientes do Journey Optimizer B2B edition que são provisionados na [arquitetura simplificada](../simplified-architecture.md).

## Acessar classes XDM

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Classes XDM]** no painel intermediário.

   * Use as guias **[!UICONTROL Padrão]** e **[!UICONTROL Relacional]** para adicionar novos campos e disponibilizá-los no Journey Optimizer B2B edition.

   * Use a guia **Eventos** para [selecionar Eventos de Experiência do AEP específicos e seus campos associados](./configure-aep-events.md) a serem usados para nós de eventos de jornada.

## Seleções de campo

>[!IMPORTANT]
>
>Você pode atualizar a seleção de campo a qualquer momento selecionando novos campos ou desmarcando campos que não são mais necessários. Ao publicar uma jornada usando esse esquema, você bloqueia a estrutura do esquema. A exclusão ou renomeação do esquema, a adição de novos campos ou a alteração dos tipos de campo não são compatíveis e podem causar falhas de jornada.

Use a diretriz a seguir para fazer seleções de campo:

* Você pode adicionar novos campos somente depois que um esquema estiver sendo usado ativamente em uma jornada.
* Excluir, renomear ou alterar tipos de campo pode causar problemas de funcionalidade de jornada. Tenha cuidado ao manipular esquemas.
* Não renomeie ou exclua esquemas nem modifique chaves em esquemas relacionais.

### Classes padrão

Na guia _[!UICONTROL Padrão]_, você pode editar _Campos gerenciados_ e _Campos atualizáveis_ para as classes padrão:

* Os campos gerenciados são exibidos em jornadas, grupos de compra e recursos de personalização.
* Os campos atualizáveis servem como restrições para os nós de jornada _Atualizar Perfil de Conta_ e _Atualizar Perfil de Pessoa_.

![Guia Classes padrão mostrando a configuração de classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

A lista inclui duas classes:

* **[!UICONTROL Perfil individual XDM]**
* **[!UICONTROL Conta de negócios XDM]**

As informações de classe exibidas incluem:

* Número de campos gerenciados
* Número de campos atualizáveis
* Hora da última atualização

Para selecionar campos do esquema de união para classes XDM padrão, clique no nome da classe para abrir a caixa de diálogo de seleção _Campos gerenciados_ ou clique no ícone _Mais menu_ ( **...** ) para escolher entre _[!UICONTROL Campos gerenciados]_ e _[!UICONTROL Campos atualizáveis]_.

![Clique no ícone do menu Mais para escolher entre campos gerenciados e campos atualizáveis](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Um campo deve primeiro ser _Gerenciado_ antes de poder ser _Atualizável_. Os _Campos atualizáveis_ selecionados devem existir no esquema fornecido pelo usuário. Seu esquema pode não incluir campos obrigatórios, exceto para campos definidos pelo sistema.

#### Campos gerenciados

Quando você escolhe **[!UICONTROL Campos gerenciados]**, a caixa de diálogo _Selecionar campos_ lista todos os campos configuráveis.

1. Selecione até 100 campos para cada classe XDM.

   Use o campo _[!UICONTROL Pesquisa]_ para filtrar a lista exibida por nome. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar as seleções atuais.

   ![Caixa de diálogo de seleção de campos gerenciados para classes XDM padrão exibindo opções de campos configuráveis](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]** para confirmar as seleções.

#### Campos atualizáveis

Antes de configurar campos atualizáveis, eles devem residir em um conjunto de dados personalizado. Para obter uma apresentação do fluxo de trabalho do conjunto de dados personalizado, consulte [Criar conjuntos de dados e assimilar dados](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"} e use a opção **[!UICONTROL Criar conjunto de dados do esquema]**. Esse conjunto de dados é usado para isolar campos atualizáveis. Todos os campos atualizáveis devem estar nesse conjunto de dados.

>[!IMPORTANT]
>
>Proteções para campos atualizáveis:
>
>* Esquemas - Na classe Perfil Individual XDM, todos os campos obrigatórios no esquema devem ser definidos pelo sistema, como `identityMap` ou `personID`.
>* Conjuntos de dados - Não use um conjunto de dados que já esteja em uso para outra finalidade. Como prática recomendada, crie conjuntos de dados dedicados especificamente para armazenar campos atualizáveis. Use um conjunto de dados separado para cada classe XDM.

Crie um conjunto de dados para um Perfil individual e outro para uma Conta comercial. Selecione cada novo conjunto de dados durante o processo de configuração:

1. Para **[!UICONTROL Conjuntos de Dados]**, selecione a nova fonte de dados que você criou.

1. Escolha os campos do conjunto de dados selecionado.

   ![Caixa de diálogo para selecionar campos atualizáveis dos conjuntos de dados na configuração do esquema XDM](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]** para aplicar as alterações.

### Esquemas relacionais

Esquemas relacionais permitem criar classes de dados personalizadas. Com acesso a vários conjuntos de dados, você pode criar classes especificamente personalizadas para suas necessidades de dados. Use esquemas relacionais para entidades de negócios, como compras, licenças e registros de evento em decisões de jornada e personalização de email. Você pode selecionar até 50 esquemas e até 100 campos por esquema.

Para obter informações sobre como usar os campos selecionados para personalização avançada de email, consulte [Personalização de conteúdo](../content/personalization.md#custom-datasets). Para obter informações sobre como usar os campos selecionados para a decisão de jornada (caminhos divididos por conta), consulte [Filtragem de dados personalizada](../journeys/split-merge-paths-nodes.md#custom-data-filtering). <!-- add link to split path by people in M 1.5 GA release -->

>[!NOTE]
>
>Os [Esquemas relacionais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/schema/relational#) estão disponíveis para [!DNL Journey Optimizer B2B Edition] como uma versão de disponibilidade limitada. O Data Mirror e esquemas relacionais estão disponíveis para [!DNL Journey Optimizer Orchestrated Campaigns] titulares de licença. Os esquemas relacionais também estão disponíveis como uma versão limitada para [!DNL Customer Journey Analytics] usuários, dependendo da sua licença e habilitação de recursos. Entre em contato com o representante da Adobe para obter acesso.

>[!NOTE]
>
>No momento, esse recurso oferece suporte a casos de uso de objetos personalizados relacionados à conta, com planos para oferecer suporte a mais casos de uso de objetos prontos para uso no futuro.

Você pode criar esquemas relacionais usando o editor de esquemas (vá para **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Esquemas]** na navegação à esquerda).

Ao criar um esquema para uso com [!DNL Journey Optimizer B2B Edition], os seguintes valores de configuração são obrigatórios:

* Comportamento: Registro
* Segmentação: ativada
* Tipo de relacionamento: muitos para um
* Esquema de referência: Conta B2B
* Campos obrigatórios: chave primária, chave estrangeira e descritor de versão
* Conjunto de dados associado: definido e mapeado para o esquema

Para selecionar campos de esquema relacional a serem usados em [!DNL Journey Optimizer B2B Edition]:

1. Selecione a guia **[!UICONTROL Relacional]** para exibir seus esquemas.

   ![Guia Esquemas relacionais no Editor de esquemas mostrando campos de entidade comercial para o Adobe Journey Optimizer B2B edition](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Selecionar esquema XDM relacional]**.

   >[!NOTE]
   >
   >Nesta versão de recurso beta, somente _Objetos personalizados muitos para um da conta_ são suportados.

1. Selecione um esquema relacional e clique em **[!UICONTROL Próximo]**.

   >[!NOTE]
   >
   >Nesta versão de recurso beta, não é possível remover um esquema da lista após selecioná-lo.

   ![Selecione um esquema relacional na caixa de diálogo](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Insira um namespace ou use o namespace padrão. Clique em **[!UICONTROL Avançar]**.

   Você só pode definir o namespace uma vez e não pode reverter esta ação.

   ![O namespace padrão na caixa de diálogo Criar namespace](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Revise os campos de esquema relacional.

   Clique no ícone _Informações_ ![Informações](../assets/do-not-localize/icon-info-light.svg) para exibir os metadados do campo.

1. Selecione os campos a serem habilitados para jornadas e personalização.

   A plataforma seleciona automaticamente os seguintes campos obrigatórios:

   * Chave externa
   * Chave primário
   * Descritor de versão

   Use o campo _[!UICONTROL Pesquisa]_ para filtrar a lista exibida por nome. Use o controle deslizante **[!UICONTROL Mostrar apenas campos selecionados]** para revisar as seleções atuais.

   ![Selecionar campos para o esquema relacional na caixa de diálogo](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.
