---
title: Comprando modelos de função de grupo
description: Crie modelos de função com atribuição automática condicional para identificar tomadores de decisão e participantes de grupos de compra no Journey Optimizer B2B edition.
feature: Buying Groups
role: User
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 5%

---

# Modelos de função do grupo de compra

Em um mercado B2B, as decisões de compra geralmente são tomadas por vários indivíduos. Essas pessoas participam do processo de tomada de decisões de acordo com sua função na organização. Crie modelos de função do Grupo de compras que contenham um grupo de definições de função de acordo com cada tipo de oferta de produto ou caso de uso de conta.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

## Acessar e procurar modelos de função

1. Na navegação à esquerda, clique em **[!UICONTROL Grupos de compra]**.

1. Na página _[!UICONTROL Grupos de compras]_, selecione a guia **[!UICONTROL Modelos de Funções]**.

   ![guia Modelos de Funções](assets/roles-templates-tab.png){width="800" zoomable="yes"}

   A guia fornece uma lista de inventário de todos os modelos de funções existentes e exibe as seguintes informações no formato da coluna:

   * [!UICONTROL Nome]
   * [!UICONTROL Status]
   * [!UICONTROL Data de criação]
   * [!UICONTROL Criado por]
   * [!UICONTROL Última atualização]
   * [!UICONTROL Última atualização por]
   * [!UICONTROL Publicado em]
   * [!UICONTROL Publicado por]

   A lista é classificada por padrão por _[!UICONTROL Última atualização]_. Todos os modelos de funções têm status de `Draft` ou `Live`.

1. Para filtrar a lista por nome, use o campo de pesquisa na parte superior da lista.

   Insira os primeiros caracteres do nome para reduzir a lista exibida aos itens correspondentes.

   ![Modelos de Funções filtrados por cadeia de caracteres de pesquisa](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Criar um modelo de funções

1. Na guia _[!UICONTROL Modelos de Funções]_, clique em **[!UICONTROL Criar modelo]** no canto superior direito.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) exclusivos para o modelo.

   ![Caixa de diálogo Criar Modelo de Funções](assets/roles-template-create-dialog.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

### Adicionar as funções de modelo

Após criar o modelo, ele será aberto no espaço de trabalho e você receberá uma solicitação para adicionar as funções. O primeiro cartão de função é exibido por padrão.

Cada função definida para o modelo usa um conjunto de filtros, ou _condições_, para determinar os membros atribuídos à função. Use os seguintes tipos de filtro para definir as condições para uma função:

| Tipo | Condição |
| ---- | --------- |
| Atributos da pessoa | <li>Endereço de email <li>Email inválido <li>Email suspenso <li>Número de fax <li>Nome <li>Região inferida <li>Nome do cargo <li>Sobrenome <li>Segundo nome <li>Número do celular <li>Pontuação de engajamento da pessoa <li>Número de telefone <li>Código postal <li>Estado <li>Inscrição cancelada <li>Motivo do cancelamento de inscrição |
| Filtros especiais | <li>Membro da lista <li>Membro do programa |
| Dados de intenção | Tentativa de categoria <li>Intenção do produto <li>Tentativa de palavra-chave<br/>[Saiba mais sobre dados de intenção](../admin/intent-data.md). |

1. Para o primeiro cartão de função, defina as propriedades da função.

   * Escolha a **[!UICONTROL Função do grupo de compra]** na lista.

     Há seis funções padrão: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` e `Other`. A lista também inclui quaisquer [funções personalizadas definidas na lista _Funções_](./default-custom-roles.md#custom-roles).

     ![Lista de funções do grupo de compra](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Defina a **[!UICONTROL Ponderação]** da função, que é usada para calcular a pontuação de engajamento.

     O valor de cada opção é convertido em uma porcentagem para o cálculo de pontuação: [!UICONTROL Trivial] = 20, [!UICONTROL Menor] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Importante] = 80 e [!UICONTROL Vital] = 100.

     Por exemplo, um modelo de função com funções que usam Vital, Importante e Normal é convertido como 100/240, 80/240, 60/240.

   * **[!UICONTROL Adicionar condições para atribuição automática]** - marque esta caixa de seleção para adicionar condições para atribuir automaticamente membros ao grupo de compras que correspondem à condição. Se a caixa de seleção não estiver marcada, a adição de condições NÃO será necessária.

   * **[!UICONTROL Obrigatório para pontuação de integridade]** - Marque esta caixa de seleção para a função se desejar que ela seja um requisito para o cálculo de uma pontuação de integridade.

1. Clique em **[!UICONTROL Adicionar Condição]** e defina a regra condicional para a função.

   * Na caixa de diálogo _[!UICONTROL Condição]_, expanda a lista de **[!UICONTROL Atributos de pessoa]** e localize um atributo que você deseja usar para corresponder à função. Arraste-o para a direita e solte-o no espaço de filtro.

     ![Atributo de arrastar condição de adição de modelo de funções](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta no Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa em condições.

   * Use o atributo para criar um filtro correspondente usando um ou mais valores.

     No exemplo a seguir, o atributo Cargo é usado para identificar uma correspondência do Tomador de decisão. Qualquer valor de título que comece com `Director` ou `Sr Director` é avaliado como verdadeiro para a condição.

     ![Exemplo de condição de modelo de funções usando o título do trabalho](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * Se necessário, adicione outro atributo e condição que refine ainda mais os critérios para uma correspondência à função.

   * Clique em **[!UICONTROL Concluído]**.

1. Para cada função adicional que você deseja incluir no modelo, clique em **[!UICONTROL Adicionar outra função]** e repita as etapas 1 e 2 para definir a função.

   ![Modelo de funções com várias funções definidas](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;associação à lista do Marketo Engage&quot;]

No Marketo Engage, as _Campanhas inteligentes_ verificam a associação de programas para garantir que os clientes potenciais não recebam emails duplicados e não sejam membros de vários fluxos de emails ao mesmo tempo. No Journey Optimizer B2B, você pode verificar a associação à lista do Marketo Engage como uma condição para seu modelo de funções para ajudar a eliminar a duplicação na compra de associação de grupo e atividades de jornada.

Para usar a associação de lista como uma condição de função, expanda **[!UICONTROL Filtros Especiais]** e arraste a condição **[!UICONTROL Membro da Lista]** para o espaço de filtro. Em seguida, conclua a definição do filtro para avaliar a associação em uma ou mais listas do Marketo Engage.

![Condição de modelo de funções para associação à lista de Marketo Engage](assets/roles-template-conditions-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Suas alterações são salvas automaticamente no status _Rascunho_. Se você não estiver pronto para publicar o modelo de funções, clique na seta para a esquerda (para trás) na parte superior da página e retorne à lista _[!UICONTROL Modelos de funções]_.

### Publicar o modelo de funções

Se o modelo estiver pronto para uso, clique em **[!UICONTROL Publicar]** no canto superior direito.

A publicação do modelo define o status como _Ativo_ e o disponibiliza para associação com um interesse de solução. Deve haver pelo menos uma função definida para publicar o modelo de funções.

## Editar um modelo de funções de rascunho

Quando um modelo de funções está em um estado de _Rascunho_, você pode continuar a editar as funções definidas. Todas as alterações feitas são salvas automaticamente.

Altere qualquer uma das configurações no cabeçalho do cartão de função, incluindo a função do grupo de compra, ponderação, atribuição automática e requisito de pontuação de integridade.

![Alterar propriedades de função de grupo de compra](./assets/roles-template-role-properties.png){width="600"}

### Modificar as condições para uma função

Para alterar a condição/lógica de filtragem de qualquer uma das funções, clique no ícone _Editar_ ( ![Editar ícone](../assets/do-not-localize/icon-edit.svg) ) na parte superior direita do cartão de função. Esta ação abre o espaço de trabalho _[!UICONTROL Condições]_, no qual você pode modificar um filtro existente, adicionar ou remover um filtro ou alterar a lógica do filtro.

### Excluir um cartão de função

Para remover uma função do modelo, clique no ícone _Excluir_ ( ![Excluir ícone](../assets/do-not-localize/icon-delete.svg) ) no cartão de função.

### Definir a prioridade de funções

É possível reordenar as funções no modelo, o que determina a prioridade para atribuir leads a uma função. Há um controlador de **[!UICONTROL Prioridade]** exibido à direita de cada cartão de função. Clique na seta _Para cima_ ou _Para baixo_ à direita para mover a placa de função para cima ou para baixo em prioridade.

![Alterar prioridade de função](./assets/roles-template-role-priority.png){width="700"}

## Excluir um modelo de funções

Você pode excluir um modelo de funções se ele estiver no status _Rascunho_.

1. Selecione o modelo de funções na lista para abri-lo.

1. Clique em **[!UICONTROL Excluir]** na parte superior direita.

   ![Alterar prioridade de função](./assets/roles-template-delete.png){width="700"}

1. Na caixa de diálogo, clique em **[!UICONTROL Excluir]** para confirmar.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3453306/?learn=on&captions=por_br)
