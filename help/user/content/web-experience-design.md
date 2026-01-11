---
title: Design de experiência online
description: 'Projete experiências da Web com editores visuais e não visuais: adicione modificações, gerencie atualizações de conteúdo, ative o rastreamento de cliques e personalize o conteúdo no Journey Optimizer B2B edition.'
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Design de experiência online

Depois de [criar uma experiência da Web](./web-experiences.md#create-a-web-experience), use o espaço de design de conteúdo para definir as modificações que deseja aplicar às suas páginas da Web.

>[!BEGINSHADEBOX]

**Pré-requisitos**

Antes de criar experiências da Web, verifique se os seguintes requisitos foram atendidos:

* Um administrador de produto configurou um ou mais canais da Web para definir os URLs (páginas) a serem incluídos em uma experiência da Web. Para obter mais informações, consulte [Configurações do canal da Web](../admin/configure-channels-web.md).

* Seu site tem o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementado para identificação de visitantes e entrega de conteúdo. O Adobe Experience Platform Web SDK versão 2.16 ou superior é necessário.

* Você tem as [permissões](../admin/user-management.md#b2b-product-permissions) necessárias para criar e gerenciar experiências da Web em uma jornada:
   * _[!UICONTROL Campanhas]_ > _[!UICONTROL Gerenciar campanhas]_ - Necessário para adicionar ou atualizar um nó de ação de personalização da Web.
   * _[!UICONTROL Campanhas]_ > _[!UICONTROL Exibir campanhas]_ - Necessário para exibir detalhes de nós de ação de personalização da Web.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Antes de criar uma experiência da web, verifique se você tem a extensão de navegador Auxiliar de edição visual do Adobe Experience Cloud instalada para o seu navegador da web. Esta extensão é necessária para abrir, criar e visualizar suas páginas da Web de forma confiável no espaço de design da experiência na Web do Journey Optimizer B2B edition.<br/>
>
>Atualmente, o Google Chrome e o Microsoft Edge são os únicos navegadores compatíveis com a extensão e a criação de experiências da Web no Journey Optimizer B2B edition. Para obter mais informações, consulte [Instalar a extensão Auxiliar de Edição Visual](./web-experiences.md#install-the-visual-editing-helper-extension).

## Editores de experiência online

O Journey Optimizer B2B edition fornece dois tipos de editores para projetar modificações na Web:

| Editor | Descrição | Melhor para |
| ------ | ----------- | -------- |
| [Editor visual](#visual-editor) | Um editor do WYSIWYG (_What You See Is What You Get_) que exibe seu site e permite selecionar e modificar elementos diretamente. Ela requer a [extensão Auxiliar de edição visual](./web-experiences.md#install-the-visual-editing-helper-extension) no Google Chrome ou no navegador da Web Microsoft Edge. | Fazer alterações visuais em elementos de página visíveis, como texto, imagens, botões e banners. |
| [Editor não visual](#non-visual-editor) | Um editor baseado em código para aplicar modificações que não podem ser feitas pelo editor visual. | Direcionamento de elementos difíceis de selecionar visualmente, aplicação de alterações CSS avançadas ou realização de modificações em elementos ocultos. |

Nas propriedades da experiência online, use a opção **[!UICONTROL Editor visual]** para determinar o tipo de editor. Habilite a opção para usar o editor visual ou desabilite-o para usar o editor não visual.

![Opção do editor visual habilitada](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Editor visual {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Usar o modo Procurar"
>abstract="Nesse modo, você pode navegar para a página exata que deseja personalizar para a configuração de canal da Web selecionada."

O editor visual carrega as páginas da Web em um iframe, onde é possível selecionar elementos e aplicar modificações diretamente na pré-visualização da página. Complete as etapas a seguir para usar o editor visual no design da experiência da web:

1. Com a guia _[!UICONTROL Conteúdo]_ exibida na página de detalhes da experiência na Web, clique em **[!UICONTROL Editar experiência na Web]** no painel direito.

   O editor visual carrega seu site com base na configuração do canal da Web.

   ![Editor visual de experiência na Web](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Se necessário, clique em **[!UICONTROL Procurar]** no canto superior direito e use a barra de navegação do site para carregar a página específica que você deseja modificar.

   Você também pode inserir o URL da página no campo na parte superior.

   >[!NOTE]
   >
   >Verifique se a página carregada corresponde aos padrões de URL definidos na configuração do canal da Web. Clique em **[!UICONTROL Exibir detalhes da configuração]** na parte superior direita para exibir a URL ou as regras de correspondência de páginas da configuração de canal da Web selecionada.

   ![Modo de navegação no editor visual](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Clique em **[!UICONTROL Design]** na parte superior direita para carregar a página no espaço de design.

1. Para definir como você deseja que a página exibida seja modificada para a experiência da Web, é possível:

   * [Insira novos componentes](#insert-new-components) (divisor, HTML, imagem, cabeçalho, parágrafo ou link) na página da experiência online.

   * Selecione qualquer elemento existente da página, como uma imagem, botão, parágrafo, texto, contêiner, cabeçalho ou link, e [modifique-o para a experiência online](#modify-elements).

   * [Adicionar rastreamento de cliques](#click-tracking-for-web-experiences) para elementos para medir o engajamento e coletar insights.

1. Repita a etapa 2 para carregar outras páginas que deseja incluir na experiência da Web e repita a etapa 3 para definir as modificações da página.

1. [Revise suas modificações](#manage-modifications) e faça os ajustes necessários.

1. Quando as modificações forem concluídas, clique na seta para a esquerda acima do editor para retornar às propriedades da experiência na web.

### Modificar elementos

Clique em um elemento na página exibida para selecioná-lo. Uma borda azul indica o elemento selecionado e uma barra de ferramentas contextual é exibida com opções de modificação.

![Selecione um elemento para modificar](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

As opções da barra de ferramentas dependem do tipo de componente selecionado:

| Ação | Descrição |
| ------ | ----------- |
| **[!UICONTROL Opções de texto]** | Altere a classe do elemento de texto ou o estilo do elemento selecionado. |
| **[!UICONTROL Escolher imagem]** | Substitua a fonte da imagem ou adicione uma imagem ao elemento. |
| **[!UICONTROL Editar link/Adicionar link]** | Modifique ou adicione um URL de link. |
| **[!UICONTROL Organizar]** | Mova o elemento selecionado para trás ou para frente na exibição. |
| **[!UICONTROL Adicionar personalização]** | Inserir personalização. |
| **[!UICONTROL Clique em rastrear elemento]** | Adicione o rastreamento de cliques para o elemento. |
| **[!UICONTROL Excluir]** | Remova o elemento selecionado da página. |

Para um elemento selecionado, as propriedades no painel direito são alteradas para refletir o estilo e as ações disponíveis. Clique em um ícone de ação na parte superior do painel para duplicar, rastrear cliques, excluir ou ocultar o elemento selecionado.

![clique em um ícone de ação para o elemento selecionado](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Elementos de texto

1. Selecione um elemento de texto na página.

1. Insira o novo conteúdo de texto ou selecione uma sequência de caracteres de texto e insira o texto de substituição.

1. (Opcional) Use as [opções de formatação de texto](./content-components.md#text), como negrito, itálico e alinhamento.

1. Clique fora do elemento de texto para aplicar a alteração.

Para obter mais informações sobre opções de estilo de texto para componentes de texto, consulte [Componentes de conteúdo](./content-components.md#text).

+++

+++Elementos da imagem

1. Selecione um elemento de imagem na página.

1. Clique no ícone _[!UICONTROL Escolher imagem]_ na barra de ferramentas contextual ou no painel direito.

1. Procure e selecione uma imagem da sua biblioteca de ativos.

1. Use as [opções de estilo de imagem](./content-components.md#image) no painel direito, conforme necessário.

+++

+++Elementos de botão

1. Selecione um elemento de botão na página.

1. (Opcional) Insira um novo texto para o botão ou selecione a sequência de caracteres de texto e insira o texto de substituição.

   Você pode usar a personalização para alterar o texto do botão usando dados de perfis de conta ou pessoa.

1. Use as [opções de estilo do botão](./content-components.md#button) no painel direito, conforme necessário.

+++

+++ Elementos de contêiner

1. Selecione um elemento de container na página.

1. Use as [opções de estilo do contêiner](./content-components.md#container) no painel direito, conforme necessário.

+++

### Inserir novos componentes

Ao selecionar o ícone **+** na navegação à esquerda do design para o editor visual, você pode adicionar os seguintes tipos de componentes à página como uma modificação de experiência da web:

* **[!UICONTROL Divisor]** - Use este componente para inserir uma linha divisória para organizar o layout e o conteúdo do seu email. Você pode ajustar atributos de estilo, como cor da linha, estilo e altura, nas propriedades no painel direito. Consulte [Divider](./content-components.md#divider) em _Componentes de conteúdo_ para obter mais informações.
* **[!UICONTROL HTML]** - Use este componente para copiar e colar o código HTML na estrutura existente. Ele permite criar componentes modulares gratuitos do HTML para reutilizar algum conteúdo externo. Consulte [HTML](./content-components.md#html) em _Componentes de conteúdo_ para obter mais informações.
* **[!UICONTROL Imagem]** - Use este componente para inserir um arquivo de imagem na página. Você pode ajustar atributos de estilo, como largura e altura, nas propriedades no painel direito. Consulte [Imagem](./content-components.md#image) em _Componentes de conteúdo_ para obter mais informações.
* **[!UICONTROL Cabeçalho]** - Use este componente para inserir texto de classe de cabeçalho. Você pode ajustar atributos de estilo, como cor do texto, estilo, fonte e tamanho nas propriedades no painel direito. Consulte [Texto](./content-components.md#text) em _Componentes de conteúdo_ para obter mais informações.
* **[!UICONTROL Parágrafo]** - Use este componente para inserir um elemento de texto padrão. Você pode ajustar atributos de estilo, como cor do texto, estilo, fonte e tamanho nas propriedades no painel direito. Consulte [Texto](./content-components.md#text) em _Componentes de conteúdo_ para obter mais informações.
* **[!UICONTROL Link]** - Use este componente para inserir um link de texto independente em uma URL especificada. Você pode ajustar atributos de estilo, como cor do texto, estilo, alinhamento e tamanho nas propriedades no painel direito.

Selecione um tipo de componente à esquerda e passe o mouse sobre um elemento adjacente ao local em que deseja adicioná-lo.

![Interface do editor visual - novo componente](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Clique em um dos botões exibidos para colocar o componente:

* ***[!UICONTROL Inserir antes de]** - Insira o componente antes do elemento selecionado.
* ***[!UICONTROL Inserir após]** - Insere o componente após o elemento selecionado.

Para desmarcar um tipo de componente para inserção, clique em **[!UICONTROL ESC]** no banner azul contextual exibido na parte superior da página.

## Editor não visual {#non-visual-editor}

Use o editor não visual quando precisar fazer modificações que não podem ser facilmente realizadas no editor visual. Essa abordagem baseada em código oferece controle preciso sobre o direcionamento e a modificação de elementos. Complete as etapas a seguir para usar o editor não visual no design da experiência da Web:

1. Com a guia _[!UICONTROL Conteúdo]_ exibida na página de detalhes da experiência online, clique em **[!UICONTROL Adicionar modificação]** no painel direito.

   O editor não visual carrega uma página com base na configuração do canal da Web.

   ![Interface do editor não visual](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Defina a primeira modificação que deseja fazer.

   O painel lateral esquerdo exibe uma lista de modificações existentes (se houver). Clique em **[!UICONTROL Adicionar]** para definir uma nova modificação. Se não houver modificações definidas, o painel assumirá como padrão as opções _[!UICONTROL Adicionar modificação]_.

   * Escolha o **[!UICONTROL Tipo de modificação]**:

     | Tipo | Descrição |
     | ---- | ----------- |
     | [**[!UICONTROL Seletor de CSS]**](#css-selector-modifications) | Direcione elementos usando uma string do seletor de CSS. |
     | [**[!UICONTROL Página]**](#page-modifications) | Insira HTML, CSS ou JavaScript personalizados em elementos no nível da página, como `<head>` ou `<body>`. |

   * Configure os parâmetros de modificação de acordo com o tipo:

      * **[!UICONTROL Seletor de CSS]** - Insira um seletor de CSS válido para direcionar elementos específicos.
      * **[!UICONTROL Tipo de ação]** - Escolha a ação a ser executada (editar, ocultar, excluir, inserir, substituir).
      * **[!UICONTROL Conteúdo]** - Forneça o conteúdo ou estilo a ser aplicado.

1. Clique em **[!UICONTROL Salvar]** para aplicar a modificação.

### Modificações do seletor de CSS

As modificações do seletor de CSS permitem direcionar elementos com precisão usando a sintaxe padrão do seletor de CSS.

1. Escolha **[!UICONTROL Seletor de CSS]** como o tipo de modificação.

1. Insira o seletor no campo **[!UICONTROL Seletor de Elemento CSS]**.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Exemplo de seletores:**
    
    | Seletor | Metas |
    | — | — |
    | `#hero-banner` | Elemento com a ID &quot;hero-banner&quot; |
    | `.cta-button` | Todos os elementos com classe &quot;cta-button&quot; |
    | &quot;header nav a&quot; | Links na navegação, dentro do cabeçalho |
    | `[data-offer=&quot;premium&quot;]` | Elementos com um atributo de dados específico |

1. Escolha um **[!UICONTROL Tipo de ação]** e especifique as informações/conteúdo necessários.

   * **[!UICONTROL Definir Conteúdo]** - Insira o texto no campo **[!UICONTROL Conteúdo]** para o elemento identificado pelo valor _[!UICONTROL Seletor de Elemento CSS]_.

   * **[!UICONTROL Definir Atributo]** - Especifique um atributo a ser associado ao seletor de CSS atual para que o elemento possa ser identificado por este atributo. Insira um nome no campo **[!UICONTROL Nome do atributo]** e um valor no campo **[!UICONTROL Conteúdo]**. Se o atributo já existir, o valor será atualizado; caso contrário, um novo atributo será adicionado com o nome e o valor especificados.

   ![Modificação do seletor de css do editor não visual](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Opcional) Clique em **[!UICONTROL Adicionar personalização]** e use o [editor de personalização](./personalization.md#personalization-editor) para criar uma personalização personalizada para o conteúdo.

### Modificações de página

Você pode adicionar um código personalizado usando o tipo de modificação Página `<head>`. O elemento `<head>` é um contêiner de metadados (dados sobre dados) e é colocado entre a marca `<html>` e a marca `<body>`. Nesse caso, o código não aguarda os eventos body ou page-load; ele é executado no início do carregamento da página.

O elemento `<head>` é usado com frequência para adicionar código JavaScript ou CSS à parte superior da página. Os seletores para ações visuais subsequentes dependem dos elementos HTML adicionados nessa guia.

>[!NOTE]
>
>O código personalizado é executado no navegador do visitante. Certifique-se de que seu código esteja seguro, testado e não afete negativamente o desempenho da página ou a experiência do usuário.

1. Escolha **[!UICONTROL Página`<head>`]** como o tipo de modificação.

1. Adicione seu código personalizado na caixa **[!UICONTROL Conteúdo]**.

   >[!CAUTION]
   >
   >Você só pode adicionar elementos `<script>` e `<style>` à seção `<head>`. Adicionar `<div>` marcas e outros elementos pode fazer com que os `<head>` elementos restantes sejam preenchidos dentro de `<body>`.

   ![Modificação do cabeçalho da página do editor não visual](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Opcional) Clique em **[!UICONTROL Adicionar personalização]** e use o [editor de personalização](./personalization.md#personalization-editor) para criar uma personalização personalizada para o conteúdo.

## Gerenciar modificações {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Gerenciar facilmente todas as alterações"
>abstract="Usando esse painel, você pode navegar por todos os ajustes e adições definidos para a página da Web e gerenciá-los."

Todas as modificações que você cria são rastreadas e podem ser gerenciadas no painel **[!UICONTROL Modificações]** do editor visual e do editor não visual. Clique no ícone _[!UICONTROL Modificações]_ <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) -->na barra de ferramentas esquerda para exibir todas as modificações.

Cada registro de modificação inclui:

* O elemento ou seletor de destino
* O tipo de modificação (como editar, ocultar ou inserir)
* Uma visualização da alteração

![Painel de modificações](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Editar uma modificação

1. Na lista _[!UICONTROL Modificações]_, localize a modificação que deseja editar.

1. Clique no ícone _Mais menu_ ( **...** ) e escolha **[!UICONTROL Editar]**.

1. Atualize as propriedades de modificação conforme necessário.

1. Clique em **[!UICONTROL Salvar]** para salvar as alterações.

### Excluir uma modificação

1. Na lista _[!UICONTROL Modificações]_, encontre a modificação que deseja remover.

1. Clique no ícone _Mais menu_ ( **...** ) e escolha **[!UICONTROL Excluir modificação]**.

1. Confirme a remoção quando solicitado.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Visualizar suas modificações

Antes de publicar, visualize como as modificações são exibidas para os visitantes.

Use as opções de visualização de dispositivo na parte superior do editor visual para exibir as modificações em:

* Desktop
* Tablet
* Dispositivos móveis

![Alterar o tamanho do dispositivo para a visualização](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

A visualização é atualizada para mostrar como as modificações são renderizadas em cada tamanho de dispositivo.

Use a barra de URL para navegar para páginas diferentes na configuração do canal da Web. Em seguida, verifique se as modificações se aplicam corretamente às páginas direcionadas com base nas regras de correspondência de URL.

## Rastreamento de cliques para experiências da Web {#web-click-tracking}

Rastreie as interações do usuário com elementos para medir o engajamento e coletar insights. Os dados de rastreamento de cliques estão disponíveis nos relatórios de engajamento e podem ser usados para medir a eficácia das modificações da experiência online.

Quando sua experiência na Web é ativada (ativa), você também pode criar relatórios usando o Adobe Customer Journey Analytics (que requer uma assinatura do produto). Para melhorar o monitoramento da experiência online, você também pode rastrear os cliques em qualquer elemento específico do site. O rastreamento permite exibir o número de cliques desse elemento nos relatórios da Web.

Para obter mais informações sobre o Customer Journey Analytics e a criação de relatórios da Web, consulte a [documentação do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing).

1. Selecione um elemento no editor de experiência online, como uma imagem ou link.

1. Nas propriedades do elemento ou na barra de ferramentas contextual, clique no ícone _[!UICONTROL Rastrear elemento]_.

   ![Habilitar o rastreamento de cliques para elementos de experiência online](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Abra a lista Rastrear cliques no painel esquerdo e modifique o valor **[!UICONTROL Ações rastreadas]** para identificar essa interação em seus relatórios.

   ![Definir identificação de rastreamento de cliques para experiência online](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
