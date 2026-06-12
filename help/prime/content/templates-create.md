---
title: Criar modelos de email
description: Saiba como criar modelos de email no Journey Optimizer B2B Prime — criar do zero, salvar um email de uma jornada como modelo ou converter uma imagem de design em um modelo de email.
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---


# Criar modelos de email

Você pode criar um modelo de email no [!DNL Journey Optimizer B2B Edition Prime] de três maneiras:

* **Criar do zero** — crie um novo modelo na biblioteca de modelos usando o espaço de design visual de email.
* **Salvar de um email de jornada** — Salve um email criado em uma jornada como um modelo reutilizável.
* **Converter uma imagem** — carregue uma imagem de design e use a IA gerativa para convertê-la em um modelo de email editável.

>[!NOTE]
>
>Nesta versão do Beta, somente os modelos de email são compatíveis.

## Criar um modelo do zero {#design-from-scratch}

1. Navegue até **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Modelos]**.
1. Clique em **[!UICONTROL Criar modelo]**.
1. Insira um **[!UICONTROL Nome do modelo]** e uma **[!UICONTROL Descrição]** opcional.
1. Opcionalmente, adicione tags para categorizar o modelo.
1. Clique em **[!UICONTROL Criar]** para abrir o espaço de design de email.
1. Crie o layout do email usando estruturas e componentes de conteúdo. Para obter uma referência completa sobre as ferramentas disponíveis, consulte [Criação de email](email-authoring.md).
1. Opcionalmente, configure o [bloqueio de conteúdo](template-content-locking.md) para restringir quais partes dos autores de modelo podem editar ao usá-lo em uma jornada.
1. Clique em **[!UICONTROL Salvar]**.

## Salvar um email de jornada como modelo {#save-as-template}

Ao criar um email em uma jornada que deseja reutilizar, salve-o diretamente na biblioteca de modelos dentro do espaço de design de email.

1. No espaço de design de email, abra a lista suspensa **[!UICONTROL Salvar]** na parte superior do editor.
1. Selecione **[!UICONTROL Salvar como modelo de conteúdo]**.
1. Insira um **[!UICONTROL Nome do modelo]** e uma **[!UICONTROL Descrição]** opcional.
1. Opcionalmente, adicione tags e configure o [bloqueio de conteúdo](template-content-locking.md).
1. Clique em **[!UICONTROL Salvar]**.

O email original da jornada não é afetado. O modelo salvo está disponível na biblioteca de modelos para todos os usuários na sandbox.

## Converter uma imagem em um modelo {#image-to-template}

O [!DNL Journey Optimizer B2B Edition Prime] pode converter uma imagem estática — como um modelo do Figma ou do Photoshop — em um modelo de email editável usando IA gerativa. Isso elimina a necessidade de recriar manualmente os layouts dos arquivos de design.

### Requisitos

Antes de começar:

* Sua organização deve ter assinado o adendo da IA gerativa com a Adobe.
* Você deve ter a permissão **[!UICONTROL Gerar Conteúdo]** além de **[!UICONTROL Gerenciar modelos de conteúdo]**.
* O arquivo de imagem deve atender às seguintes especificações:
   * Formato: JPEG (.jpg, .jpeg) ou PNG (.png)
   * Tamanho máximo do arquivo: 10 MB
   * Largura recomendada: 600 a 800 pixels
   * Imagem clara e de alta qualidade com texto legível e elementos visuais distintos

>[!IMPORTANT]
>
>A imagem não deve conter informações de identificação pessoal (PII) ou dados confidenciais.

### Converter uma imagem

1. Navegue até **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Modelos]**.
1. Clique em **[!UICONTROL Converter imagem em modelo]** no cabeçalho.
1. Insira um **[!UICONTROL Nome do modelo]** e uma **[!UICONTROL Descrição]** opcional.
1. Opcionalmente, selecione um **[!UICONTROL Tema da marca]** para aplicar as cores, fontes e espaçamento da sua marca na saída gerada.
1. Faça upload da imagem usando a função arrastar e soltar ou o navegador de arquivos.
1. Confirme se a imagem não contém dados pessoais.
1. Revise e aceite as Diretrizes de usuário da IA gerativa da Adobe (somente primeira vez).
1. Clique em **[!UICONTROL Converter]**.

   A conversão normalmente é concluída em cinco minutos. Imagens complexas ou grandes podem levar até dez minutos. Você pode navegar para fora do escritório — o processo continua em segundo plano.

1. Quando a conversão estiver concluída, clique no nome do template para pré-visualizar e editar o conteúdo gerado.

>[!NOTE]
>
>O resultado não é exibido automaticamente. Atualize a página ou retorne à biblioteca de modelos para ver o modelo concluído.

### Editar após a conversão

O modelo convertido é aberto no espaço de design de email como um email totalmente editável. Use as ferramentas de design padrão para:

* Editar texto e adicionar tokens de [personalização](email-authoring.md#personalization).
* Atualize ou substitua imagens e adicione links.
* Ajustar cores, fontes e espaçamento.
* Adicione, remova ou reorganize componentes de conteúdo.
* Configurar [bloqueio de conteúdo](template-content-locking.md).

>[!IMPORTANT]
>
>A IA gerativa produz HTML estático com base na imagem visual. Revise todo o texto para obter a precisão e adicione personalização, conteúdo dinâmico e rastreamento manualmente após a conversão.

O modelo convertido é salvo automaticamente na biblioteca de modelos quando a conversão é concluída.

### Dicas para obter melhores resultados

Use as diretrizes a seguir para obter os melhores resultados da conversão de imagem em modelo:

**Antes da conversão:**

* Use a versão de resolução mais alta do arquivo de design.
* Projete em larguras de email padrão (600-800 pixels) e inclua o layout completo — cabeçalho por rodapé — em uma única imagem.
* Garanta contraste suficiente entre o texto e os planos de fundo e use tamanhos de fonte legíveis.

**Design para conversão precisa:**

* Use layouts simples e bem estruturados com uma separação clara entre as seções.
* Siga padrões padrão de email — cabeçalho, corpo, chamadas para ação, rodapé — em vez de designs complexos de várias camadas.
* Mantenha os elementos visuais distintos para que a IA possa identificar corretamente os limites estruturais.

**Após a conversão:**

* Teste a renderização em clientes de email e dispositivos antes de usar o modelo em uma jornada.
* Verificar alinhamento com cores da marca, fontes e diretrizes de estilo.
* Revise e aprimore a acessibilidade, incluindo o texto alternativo de imagem.
