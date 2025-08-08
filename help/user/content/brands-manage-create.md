---
title: Crie marcas para gerar e manter a consistência do conteúdo
description: Saiba como criar e personalizar suas próprias marcas para gerar e otimizar conteúdo que corresponda ao estilo da sua marca e voz.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
hide: true
hidefromtoc: true
role: User
level: Beginner, Intermediate
exl-id: 5ae7d50e-762b-48f2-a1a5-9a68ebfc291b
source-git-commit: c95323936f48a595a74c469c201b19daf1ee95e5
workflow-type: tm+mt
source-wordcount: '2052'
ht-degree: 6%

---

# Criar e gerenciar suas marcas {#brand-library}

Defina uma marca para fornecer um conjunto detalhado de regras e padrões que estabelecem uma identidade visual e verbal. Essas diretrizes fornecem uma referência para manter uma representação de marca consistente em todas as plataformas de marketing e comunicação. Ao utilizar diretrizes de marca bem definidas, as organizações podem garantir que todos os esforços de criação de conteúdo estejam alinhados às metas estratégicas e à identidade geral da marca. Essa consistência não só melhora o reconhecimento e a confiança da marca, como também contribui para uma experiência do cliente mais coesa e impactante em todos os pontos de contato.

No Journey Optimizer B2B edition, você pode definir e organizar manualmente suas definições de marca e ativos ou fazer upload de documentos de diretrizes da marca para obter informações automáticas e extração visual de ativos.

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível como um beta privado, com disponibilidade progressiva planejada para todos os clientes em versões futuras.
>
><br>
>
>É necessário um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para que você possa usar recursos habilitados por IA no Adobe Journey Optimizer B2B edition. Para obter mais informações, entre em contato com o representante da Adobe.
>
><br>
>
>Consulte [Permissões relacionadas à marca](./brands-overview.md#brand-related-permissions) para obter informações sobre como administradores de produtos podem habilitar esses recursos.

## Acessar a biblioteca de marcas

Para acessar os kits de marcas no Adobe Journey Optimizer B2B edition, vá para a navegação à esquerda e clique em **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Marcas]**. Essa ação abre uma página em que as marcas criadas são exibidas como cartões.

![Acessar a biblioteca de marcas](./assets/brands-library.png){width="800" zoomable="yes"}

Se ainda não houver marcas criadas, um único gráfico será exibido com um botão para [criar sua primeira marca](#create-and-define-a-brand).

### Ações de gerenciamento da marca

Para cada cartão, você pode clicar no ícone do menu _Mais_ ( ![ícone do menu Mais](../../assets/do-not-localize/icon-more-menu.svg) ) e escolher uma ação para a marca:

* **[!UICONTROL Exibir marca]** - Abra a página de marca e exiba as definições.
* **[!UICONTROL Marcar como marca padrão]** (Somente online) - [Marcar a marca como padrão](#default-brand) para alinhamento e geração de conteúdo.
* **[!UICONTROL Editar]** - Abra a página da marca e edite as diretrizes, exclusões e exemplos da marca.
* **[!UICONTROL Duplicar]** - Criar uma cópia como uma nova marca de rascunho.
* **[!UICONTROL Publicar]** (somente rascunho) - [Publicar a marca](#publish-the-brand) para torná-la disponível para uso com alinhamento e geração de conteúdo.
* **[!UICONTROL Cancelar publicação]** (somente online) - Cancele a publicação da marca para removê-la do uso para alinhamento e geração de conteúdo.
* **[!UICONTROL Excluir]** - Remova a marca da biblioteca de marcas.

![Acessar o menu Mais da marca](./assets/brands-library-card-more-menu.png){width="440"}

### Marca padrão

Você pode designar uma marca padrão a ser aplicada automaticamente ao gerar conteúdo e calcular pontuações de alinhamento durante a criação do conteúdo. Somente uma marca publicada (_Live_) pode ser padrão.

Na biblioteca de Marcas, a placa de marca padrão é exibida com um sinalizador.

![Sinalizador de marca padrão](./assets/brands-default-flag.png){width="200"}

Você pode definir qualquer marca publicada (_Live_) como a marca padrão. Na placa da marca, clique no ícone do menu _Mais_ ( ![ícone do menu Mais](../../assets/do-not-localize/icon-more-menu.svg) ) e escolha **[!UICONTROL Marcar como marca padrão]**.

![Designar a identidade de marca padrão](./assets/brands-set-default.png){width="350"}

## Criar e definir uma marca {#create-brand}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brands_create"
>title="Crie sua marca"
>abstract="Insira o nome e faça upload do arquivo de diretrizes da marca. A ferramenta extrairá automaticamente os principais detalhes, facilitando a manutenção da identidade da marca."

Para criar e definir as diretrizes de marca, você pode inserir os detalhes ou fazer upload dos documentos de diretrizes de marca para usar na extração automática.

### Adicionar a marca

1. Na parte superior direita da página _[!UICONTROL Marcas]_, clique em **[!UICONTROL Criar marca]**.

1. Digite um **[!UICONTROL Nome]** para sua marca.

1. Arraste e solte ou selecione seu arquivo para fazer upload das diretrizes da marca e extrair automaticamente informações relevantes sobre a marca.

   ![Definir uma nova marca](./assets/brands-create-new.png){width="500"}

   >[!NOTE]
   >
   >Se você não tiver um documento salvo no formato PDF, poderá adicionar manualmente as diretrizes e fazer upload de ativos visuais individuais após a criação da marca.

1. Clique em **[!UICONTROL Criar marca]**.

   Se você incluir um ou mais arquivos para criar a marca, o processo de extração de informações será iniciado. Pode levar vários minutos para ser concluído.

   Quando o processo de extração for concluído, o conteúdo e os padrões de criação visual serão preenchidos automaticamente.

   ![Diretrizes de marca iniciais do documento carregado](./assets/brands-create-new-page.png){width="700" zoomable="yes"}

### Refine e atualize as diretrizes da marca

1. Navegue pelas diferentes guias para adaptar e definir informações mais detalhadas, conforme necessário.

   * [!UICONTROL Visão geral]

   * [[!UICONTROL Sobre a marca]](#about-the-brand)

   * [[!UICONTROL Estilo de escrita]](#writing-style)

   * [[!UICONTROL Conteúdo visual]](#visual-content)

   Se você incluiu um ou mais documentos ao criar a marca, o processo de extração de informações criou definições para as guias e seções. A integridade depende do escopo e dos detalhes incluídos em qualquer documento. Ao revisar o resultado, você pode alterar ou remover qualquer uma das informações.

   No _Mais menu_ ( ![Mais ícone de menu](../../assets/do-not-localize/icon-more-menu.svg) ) para cada guia ou categoria, você pode adicionar documentos para extrair automaticamente informações relevantes sobre a marca. Também é possível limpar o conteúdo existente.

   ![Limpar a seção/categoria ou adicionar referência de extração](./assets/brands-sections-categories-more-menu.png){width="500" zoomable="yes"}

   Se quiser revisar a origem das informações extraídas em uma subseção, clique no link **[!UICONTROL Exibir origem]**.

   ![Exibir a fonte de conteúdo da marca](./assets/brands-view-source.png){width="700" zoomable="yes"}

1. Em cada guia de detalhes, revise as categorias e melhore a marca adicionando, removendo e alterando suas definições.

   Uma subseção rotulada **[!UICONTROL Do&#39;s]** descreve as diretrizes da categoria. Use esta área para adicionar descrições de diretrizes e exemplos das diretrizes.

   ![Diretriz definida com exemplos](./assets/brands-guidelines-examples.png){width="500" zoomable="yes"}

   Uma subseção denominada **[!UICONTROL Não]** descreve as exclusões. Use essa área para adicionar descrições de exclusão e exemplos das exclusões.

   ![Exclusões definidas com exemplos](./assets/brands-exclusions-examples.png){width="500" zoomable="yes"}

   * **Adicionar uma diretriz ou exclusão**.

     Na seção em que você deseja adicionar uma diretriz, clique no ícone _Adicionar_ ( ![Ícone Adicionar](../assets/do-not-localize/icon-add-components.svg) ) à direita. Na caixa de diálogo pop-up, insira a diretriz e marque as caixas de seleção para designar os canais e elementos aos quais a diretriz se aplica. Em seguida, clique em **[!UICONTROL Adicionar]**.

     ![Adicionar uma diretriz](./assets/brands-guideline-add.png){width="600" zoomable="yes"}

   * **Alterar uma diretriz ou exclusão**.

     Na seção onde você deseja remover uma diretriz, clique no widget de diretriz. Na caixa de diálogo pop-up, altere o conteúdo da diretriz e das caixas de seleção selecionadas, conforme necessário. Em seguida, clique em **[!UICONTROL Atualizar]**.

     ![Alterar uma diretriz](./assets/brands-guideline-update.png){width="600" zoomable="yes"}

   * **Remover uma diretriz ou exclusão**.

     Na seção onde você deseja remover uma diretriz, clique no widget de diretriz. Na caixa de diálogo pop-up, clique no ícone _Excluir_ ( ![Excluir](../assets/do-not-localize/icon-delete.svg) ) na parte superior.

   * **Adicione ou revise exemplos de suas diretrizes e exclusões**.

     No bloco de exemplo exibido, clique no ícone _Editar_ ( ![Editar](../assets/do-not-localize/icon-edit.svg) ) para alterar o exemplo ou clique no ícone _Excluir_ ( ![Excluir](../assets/do-not-localize/icon-delete.svg) ) para removê-lo.

1. Quando tiver tudo definido, clique em **[!UICONTROL Salvar]**.

   Você pode continuar fazendo alterações no rascunho da marca até decidir que ele está pronto para publicação.

### Publicar a marca

Quando sua marca incluir um conjunto completo de definições e atender aos seus requisitos, clique em **[!UICONTROL Publicar]** para disponibilizar as diretrizes da sua marca para alinhamento e geração de conteúdo.

As marcas publicadas podem ser acessadas a partir da opção **[!UICONTROL Marca]** no [alinhamento de marca](./brand-alignment.md) da IA e nas ferramentas de geração de conteúdo. <!-- [Learn more about content generation](gs-generative.md) -->

![Opções de marca para conteúdo](./assets/brand-menu-content-ai-tools.png){width="300"}

## Definições da marca

As definições da marca são organizadas em três categorias, exibidas como guias. Selecione cada guia para concluir e atualizar as diretrizes da marca.

### Sobre a marca {#about-brand}

Use a guia **[!UICONTROL Sobre a marca]** para estabelecer a identidade principal da sua marca. Essas informações descrevem a finalidade, a personalidade, o slogan e outros atributos de alto nível.

1. Adicione as informações fundamentais da sua marca na categoria **[!UICONTROL Detalhes da chave]**:

   * **[!UICONTROL Nome do kit de marcas]** - Atualize o nome da marca.

   * **[!UICONTROL Quando usar]** - Especifique cenários ou contextos nos quais esta marca deve ser aplicada.

   * **[!UICONTROL Nome da marca]** - Digite o nome oficial da marca.

   * **[!UICONTROL Descrição desta marca]** - Forneça uma visão geral do que esta marca representa.

   * **[!UICONTROL Slogan (Padrão)]** - Adicione o slogan principal associado à marca.

   ![Sobre a marca - Detalhes principais](./assets/brands-about-key-details.png){width="600" zoomable="yes"}

1. Na categoria **[!UICONTROL Princípios orientadores]**, esclareça a direção principal e a filosofia da sua marca:

   * **[!UICONTROL Missão]** - Detalhe a finalidade da marca.

   * **[!UICONTROL Visão]** - Descreva a meta de longo prazo ou o estado futuro desejado.

   * **[!UICONTROL Posicionamento do mercado]** - Explique como a marca é posicionada no mercado.

   ![Sobre a marca - Princípios orientadores](./assets/brands-about-guiding-principles.png){width="600" zoomable="yes"}

   Na categoria **[!UICONTROL Valores de marca principais]**, analise os valores de marca definidos e ajuste-os conforme necessário.

   * Para definir um novo valor principal, clique no ícone _Adicionar_ ( ![Ícone Adicionar](../assets/do-not-localize/icon-add-components.svg) ) à direita e conclua os detalhes:

     ![Sobre a marca - Princípios orientadores - adicionar valor principal](./assets/brands-about-guiding-principles-add-core-values.png){width="500" zoomable="yes"}

      * **[!UICONTROL Valor]** - Digite o nome do valor da marca principal.

      * **[!UICONTROL Descrição]** - Explique o que esse valor significa para sua marca.

      * **[!UICONTROL Comportamentos]** - Descreva as ações ou atitudes que refletem este valor na prática.

      * **[!UICONTROL Manifestações]** - Forneça exemplos de como esse valor é expresso em marcas reais.

   * Para alterar ou excluir um valor de marca principal, clique no ícone _Editar_ ( ![Editar ícone](../assets/do-not-localize/icon-edit.svg) ) para atualizar ou excluir um valor de marca principal.

     ![Sobre a marca - Princípios orientadores - editar valor principal](./assets/brands-about-guiding-principles-edit-core-values.png){width="500" zoomable="yes"}

     Altere os detalhes e clique em **[!UICONTROL Atualizar]**. Ou clique no ícone _Excluir_ ( ![Excluir ícone](../assets/do-not-localize/icon-delete.svg) ) na parte superior para remover o valor principal.

1. Na categoria **[!UICONTROL Documentos de diretrizes da marca]**, revise os documentos usados para gerar as diretrizes da marca.

   Clique no ícone do menu Mais e escolha uma opção para atualizar as diretrizes da marca usando os documentos de referência carregados:

   * **[!UICONTROL Reextrair diretrizes]** - Escolha esta ação para executar um trabalho de extração usando os documentos atuais.
   * **[!UICONTROL Adicionar referência para extração]** - Escolha esta ação para carregar outro documento e executar um trabalho de extração.

   ![Sobre a marca - Documentos de diretrizes da marca](./assets/brands-about-documents.png){width="600" zoomable="yes"}

Você pode prosseguir para refinar as diretrizes, exclusões e exemplos do [estilo de escrita](#writing-style) ou do [conteúdo visual](#visual-content), ou pode [publicar sua marca](#publish-the-brand).

### Estilo de escrita {#writing-style}

>[!CONTEXTUALHELP]
>id="ajo_brand_writing_style"
>title="Estilo de escrita e pontuação de alinhamento"
>abstract="A seção Estilo de escrita define padrões para idioma, formatação e estrutura para garantir conteúdo claro e consistente. A pontuação de alinhamento, classificada de alta a baixa, mostra o desempenho do seu conteúdo em seguir essas diretrizes e destaca as áreas a serem melhoradas."

As definições de _[!UICONTROL Estilo de gravação]_ descrevem os padrões para gravação de conteúdo e detalham como a linguagem, a formatação e a estrutura devem ser usadas para manter a clareza, a coerência e a consistência entre todos os materiais.

Selecione a guia **[!UICONTROL Estilo de Escrita]** e revise cada categoria.

![Guia de estilo de escrita](./assets/brands-writing-style-tab.png){width="600" zoomable="yes"}

| Categoria | Subcategoria | Exemplo de diretrizes | Exemplo de exclusões |
|----------------------------|----------------|-----------------------|-----------------------|
| [!UICONTROL Estilo de comunicação da marca] | [!UICONTROL Características de personalidade da marca] | Amigável e acessível. | Não seja derrotista. |
|                            | [!UICONTROL Mecânica de Gravação] | Mantenha as frases curtas e impactantes. | Não use jargão em excesso. |
|                            | [!UICONTROL Tom de situação] | Mantenha um tom profissional nas comunicações de crise. | Não ignore as comunicações de suporte. |
|                            | [!UICONTROL Diretrizes de Escolha do Word] | Use palavras como _Innovative_ e _smart_. | Evite palavras como _barato_ ou _hack_. |
|                            | [!UICONTROL Padrões de Idioma] | Siga as convenções do inglês americano. | Não misture ortografias britânicas e americanas. |
| [!UICONTROL Padrões de mensagem da marca] | [!UICONTROL Padrões de mensagem da marca] | Destaque a inovação e as mensagens direcionadas ao cliente. | Não exagere nos recursos do produto. |
|                            | [!UICONTROL Uso do slogan] | Coloque o slogan abaixo do logotipo em todos os ativos de marketing digital. | Não modifique ou traduza o slogan. |
|                            | [!UICONTROL Mensagens principais] | Enfatize a principal declaração de benefícios, como maior produtividade. | Não use propostas de valor não relacionadas. |
|                            | [!UICONTROL Nomeação de padrões] | Use nomes simples e descritivos como _ProScheduler_. | Não use termos complexos ou caracteres especiais. |
| [!UICONTROL Padrões de conformidade legal] | [!UICONTROL Padrões de marca comercial] | Sempre use o símbolo ™ ou ®. | Não omita símbolos legais quando necessário. |
|                            | [!UICONTROL Padrões de direitos autorais] | Inclua avisos de direitos autorais nos materiais de marketing. | Não use conteúdo de terceiros sem permissão. |
|                            | [!UICONTROL Padrões de isenção de responsabilidade] | Exibir avisos de isenção de responsabilidade de forma legível em ativos digitais. | Não oculte isenções de responsabilidade em áreas não visíveis. |

<!-- #### Preferred and avoided terms

Supplement your work choice guidelines by adding preferred and avoided terms. 


#### Primary tagline and variations


#### Brand names and variations



#### Approved and restricted statements
-->

### Conteúdo visual {#visual-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_imagery"
>title="Pontuação de alinhamento de conteúdo visual"
>abstract="A Pontuação de alinhamento do conteúdo visual indica o quanto o conteúdo corresponde às diretrizes de marca configuradas. Com pontuação de alta a baixa, ajuda a avaliar o alinhamento rapidamente. Explore as diferentes categorias para identificar áreas para aprimoramento e os elementos que podem ser exteriores à marca."

As definições de _[!UICONTROL Conteúdo visual]_ descrevem os padrões de imagem e design e detalham as especificações necessárias para manter uma aparência de marca unificada e consistente.

Selecione a guia **[!UICONTROL Visual content]** e revise cada categoria.

![Guia Conteúdo visual](./assets/brands-visual-content-tab.png){width="600" zoomable="yes"}

| Categoria | Exemplo de diretrizes | Exemplo de exclusões |
|------------------------|---------------------|---------------------|
| [!UICONTROL Padrões de fotografia] | Use a iluminação natural para fotos ao ar livre. | Evite imagens editadas ou pixeladas em excesso. |
| [!UICONTROL Padrões de ilustração] | Use estilos limpos e minimalistas. | Evite complexos demais. |
| [!UICONTROL Padrões de ícones] | Use um sistema de grade de 24px consistente. | Não misture dimensões de ícone, use espessuras de traçado inconsistentes ou desvie das regras de grade. |
| [!UICONTROL Diretrizes de uso] | Escolha imagens de estilo de vida que reflitam clientes reais usando o produto em ambientes profissionais. | Não use imagens que estejam em contradição com o tom da marca ou que apareçam fora de contexto. |

<!-- #### Styles

To define the overall style for the category, click **[!UICONTROL Add style]**. In the popup dialog, enter the style type and description. 

![Add style for visual content category](./assets/brands-visual-content-add-style.png){width="500" zoomable="yes"}

#### Specifications

-->

#### Exemplo de imagens

Para adicionar uma imagem mostrando o uso correto ou incorreto, escolha **[!UICONTROL Exemplo]** na caixa de diálogo pop-up _[!UICONTROL Adicionar diretriz]_ ou _[!UICONTROL Adicionar exclusão]_. Clique em **[!UICONTROL Selecionar imagem]** para escolher um arquivo de imagem do seu sistema. Clique em **[!UICONTROL Adicionar]** para carregar a imagem e exibir a miniatura da área.

![Adicionar imagem de exemplo](./assets/brands-guidelines-example-image.png){width="500" zoomable="yes"}

## Editar uma marca publicada

Não é possível fazer modificações em uma marca publicada (ao vivo), mas você pode criar uma cópia de rascunho para editar. Ao publicar o rascunho com suas edições, essa versão substitui a versão em tempo real.

1. Abra a página da marca e clique em **[!UICONTROL Editar marca]** na parte superior direita.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Editar Marca]**.

   Essa ação cria uma cópia de rascunho da marca.

1. Navegue pelas diferentes guias para atualizar as informações da marca, conforme necessário.

   * Visão geral

   * [Sobre a marca](#about-the-brand)

   * [Estilo de escrita](#writing-style)

   * [Conteúdo visual](#visual-content)

1. Clique em **[!UICONTROL Salvar]** enquanto trabalha com as atualizações de rascunho e em **[!UICONTROL Publicar]** quando estiver pronto para substituir a versão _Live_.
