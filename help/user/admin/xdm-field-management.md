---
title: Gerenciamento de campo XDM
description: Use o gerenciamento de campo XDM para controlar os dados disponíveis para o Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 2%

---


# Gerenciamento de campo XDM

Os campos do Experience Data Model (XDM) são elementos de esquema que fornecem dados para o aplicativo [!DNL Journey Optimizer B2B Edition]. Você usa campos XDM como filtros e restrições em jornadas, grupos de compra e recursos, como personalização de email e conteúdo condicional.

Os esquemas definem campos com base em classes XDM padrão. As classes XDM padrão incluem Perfil individual, Conta comercial e Evento de experiência. Os esquemas relacionais também definem campos que permitem modelar dados estruturados de forma semelhante aos bancos de dados relacionais tradicionais.

Os esquemas do Adobe Experience Platform (AEP) normalmente contêm muitos campos em hierarquias complexas. Percorrer árvores de esquema XDM leva tempo. O gerenciamento de campo XDM simplifica a seleção de campos ao exibir apenas os campos relevantes para cada jornada. Os administradores controlam quais campos aparecem para os criadores de jornadas. Os administradores também definem os campos como somente leitura ou editáveis. Essas ações melhoram a eficiência durante o design da jornada.

Os administradores que entendem o XDM e colaboram com engenheiros de dados ou participantes da modelagem de dados da CDP (Plataforma de dados do cliente B2B) seguem os procedimentos deste guia.

>[!NOTE]
>[Esquemas relacionais](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) estão disponíveis para [!DNL Journey Optimizer B2B Edition] como uma versão limitada. Esquemas relacionais e do Data Mirror estão disponíveis para titulares de licença de campanhas do Journey Optimizer Orchestrated. Os esquemas relacionais também estão disponíveis como uma versão limitada para usuários do Customer Journey Analytics, dependendo da sua licença e da ativação de recursos. Entre em contato com o representante da Adobe para obter acesso.

## Acesso às classes XDM

Para abrir a área de gerenciamento de campo XDM, navegue até **Configurações** > CONFIGURAÇÃO > **Classes XDM**.

* Você pode adicionar novos campos somente depois que um esquema estiver sendo usado ativamente em uma jornada.
* Excluir, renomear ou alterar tipos de campo pode causar problemas de funcionalidade de jornada. Tenha cuidado ao manipular esquemas.
* Não renomeie ou exclua esquemas nem modifique chaves em esquemas relacionais.

>[!IMPORTANT]
>Você pode atualizar a seleção de campo a qualquer momento selecionando novos campos ou desmarcando campos que não são mais necessários. Depois de publicar uma jornada usando esse esquema, você bloqueia a estrutura do esquema. A exclusão ou renomeação do esquema, a adição de novos campos ou a alteração dos tipos de campo não são compatíveis e podem causar falhas de jornada.

## Classes padrão

Na guia Classes padrão, você pode editar _Campos gerenciados_ e _Campos atualizáveis_.

* Os campos gerenciados são exibidos em jornadas, grupos de compra e recursos de personalização.
* Os campos atualizáveis servem como restrições para os nós de jornada _Atualizar Perfil de Conta_ e _Atualizar Perfil de Pessoa_.

![Guia Classes padrão mostrando campos gerenciados e atualizáveis para configuração de classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

Siga estas etapas para selecionar campos do esquema de união para classes XDM padrão:

1. Vá para **Administração** > **Configurações** > **Classes XDM**.
1. Abra a guia **Padrão**. Escolha uma das seguintes classes:

   * Perfil individual XDM
   * Conta empresarial XDM

A tabela exibe informações que incluem:

* Número de campos gerenciados
* Número de campos atualizáveis
* Hora da última atualização

Clique no nome da classe para abrir o diálogo de seleção _Campos gerenciados_.

![Caixa de diálogo de seleção de campos gerenciados para classes XDM padrão exibindo opções de campos configuráveis](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Clique no menu **...** para alternar entre _[!UICONTROL Campos gerenciados]_ e _[!UICONTROL Campos atualizáveis]_. A caixa de diálogo lista todos os campos configuráveis.
1. Selecione até 100 campos para cada classe XDM.
1. Clique em **[!UICONTROL Salvar]** para confirmar as seleções.

Use o filtro [!UICONTROL Mostrar apenas campos selecionados] para exibir apenas campos ativos.

Para _Campos atualizáveis_, você acessa uma caixa de diálogo separada que permite escolher campos de outras fontes de dados:

1. Na lista suspensa Conjuntos de dados, selecione a fonte de dados que deseja configurar.
1. Edite os campos a partir do conjunto de dados selecionado.
1. Clique em **[!UICONTROL Salvar]** para aplicar as alterações.

![Caixa de diálogo para selecionar campos atualizáveis dos conjuntos de dados na configuração do esquema XDM](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

O campo deve primeiro ser _Gerenciado_ antes de poder ser _Atualizável_. Os _Campos atualizáveis_ selecionados devem existir no esquema fornecido pelo usuário.

## Esquemas relacionais

Esquemas relacionais permitem criar classes de dados personalizadas. Com acesso a vários conjuntos de dados, você pode criar classes especificamente personalizadas para suas necessidades de dados.
Use esquemas relacionais para entidades de negócios, como compras, licenças e registros de evento em decisões de jornada e personalização de email. Você pode selecionar até 50 esquemas e até 100 campos por esquema.

![Guia Esquemas relacionais no Editor de esquemas mostrando campos de entidade comercial para o Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>No momento, esse recurso oferece suporte a casos de uso de objetos personalizados relacionados à conta, com planos para oferecer suporte a mais casos de uso de objetos prontos para uso no futuro.

Criar esquemas relacionais usando o Editor de Esquemas em **Gerenciamento de Dados** > **Esquemas**.

Esses valores de configurações devem ser incluídos ao criar um esquema para uso com [!DNL Journey Optimizer B2B Edition]:

* Comportamento: Registro
* Segmentação: ativada
* Tipo de relacionamento: muitos para um
* Esquema de referência: Conta B2B
* Campos obrigatórios: chave primária, chave estrangeira e descritor de versão
* Conjunto de dados associado: definido e mapeado para o esquema

### Criar um Esquema Relacional

Siga estas etapas para selecionar campos a serem usados em [!DNL Journey Optimizer B2B Edition]:

1. Vá para **Administração** > **Configurações** > **Classes XDM**.
1. Abra a guia **Relacional** para exibir seus esquemas.
1. Clique em **[!UICONTROL Selecionar esquema XDM relacional]**.

   * Na versão beta, há suporte apenas para _Objetos personalizados muitos para um da conta_.

1. Selecione um esquema relacional e clique em **[!UICONTROL Próximo]**.

   * Na versão beta, não é possível remover um esquema da lista após selecioná-lo.

1. Insira um namespace ou use o namespace padrão. Clique em **[!UICONTROL Avançar]**.

   * Você só pode definir o namespace uma vez e não pode reverter esta ação.

1. Revise os campos de esquema relacional. Clique no ícone ![Informações](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Informações] para exibir os metadados do campo.
1. Selecione os campos a serem habilitados para jornadas e personalização. A plataforma seleciona automaticamente os seguintes campos obrigatórios:

   * Chave externa
   * Chave primário
   * Descritor de versão

1. Use o controle deslizante [!UICONTROL Mostrar apenas campos selecionados] para visualizar suas seleções.
1. Filtrar campos por nome usando a barra de Pesquisa.
1. Clique em **[!UICONTROL Salvar]**.

## Eventos

Use Eventos de experiência e seus campos associados em decisões de jornada. É possível selecionar até 50 eventos e até 100 campos por evento.

![Guia Eventos mostrando a seleção de eventos de experiência e campos de esquema para jornadas e personalização](assets/xdm-events.png){width="700" zoomable="yes"}

Clique em um nome de evento para exibir detalhes e editar os campos configurados.

Siga estas etapas para selecionar Eventos de experiência e campos de esquema:

1. Vá para **Administração** > **Configurações** > **Classes XDM**.
1. Abra a guia **Eventos**.
1. Para selecionar campos para um evento, clique em **[!UICONTROL Selecionar evento de experiência]**.
1. Na página Detalhes, clique em **[!UICONTROL Selecionar tipo de evento]**.
1. Na lista Evento, escolha o evento.
1. Clique em **[!UICONTROL Selecionar]** para fechar a caixa de diálogo.

   * Na versão beta, não é possível remover eventos selecionados.

1. Clique em **[!UICONTROL Selecionar campos]**.
1. Use o controle deslizante [!UICONTROL Mostrar apenas campos selecionados] para exibir suas seleções atuais.
1. Selecione os campos a serem usados em [!DNL Journey Optimizer B2B Edition]. Clique em **[!UICONTROL Selecionar]** para fechar a caixa de diálogo.
1. Clique em [!UICONTROL Salvar].
