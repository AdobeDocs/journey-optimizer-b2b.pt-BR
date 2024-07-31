---
title: Criação de email
description: Saiba como criar conteúdo de email personalizado que é usado em Jornadas de conta.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: ce38e378ad316fb379cb649a4592ed831250296d
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 1%

---

# Criação de email

Use o Adobe Journey Optimizer B2B Edition para enviar mensagens de email aos seus clientes. Você pode criar, personalizar e visualizar mensagens no Designer de email.

## Adicionar uma ação de email em uma jornada de conta

Você pode configurar entregas de email em uma Jornada de conta ao adicionar um nó _[!UICONTROL Realizar uma ação]_ e fazer o seguinte:

1. Para o destino _[!UICONTROL Ação em]_, escolha **[!UICONTROL Pessoas]**.
1. Para a _[!UICONTROL Ação sobre pessoas]_, escolha **[!UICONTROL Enviar email]**.
1. Para a _[!UICONTROL origem do email]_, escolha **[!UICONTROL Criar novo email]**.

   Como alternativa, você também pode selecionar a opção _[!UICONTROL Selecionar email do Adobe Marketo Engage]_ para usar um dos emails pré-criados no Marketo Engage e enviá-lo como parte da Jornada de Conta.

   >[!NOTE]
   >
   >Se estiver criando um email pela primeira vez, verifique se o canal de email está configurado no Adobe Marketo Engage. Para saber mais, consulte [Garantir a capacidade de entrega de emails](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) na documentação do Marketo Engage.

   ![Realizar uma ação - enviar um email](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Na parte inferior do painel _[!UICONTROL Realizar uma ação]_, clique em **[!UICONTROL Criar email]**.

1. Na caixa de diálogo, insira um **[!UICONTROL Nome]** exclusivo para o email e uma **[!UICONTROL Linha de assunto]**.

   ![Caixa de diálogo Criar novo email](assets/create-new-email.png){width="400"}

1. Clique em **[!UICONTROL Criar]**.

   Na seção _[!UICONTROL Propriedades de email]_ da página de conteúdo de email, os campos _[!UICONTROL Do email]_ e _[!UICONTROL Responder para endereço]_ já estão configurados. Você pode inserir valores para os campos _[!UICONTROL De nome]_ e _[!UICONTROL Descrição]_ (opcional).

## Criar o conteúdo do email

Clique em **[!UICONTROL Adicionar conteúdo de email]** na parte superior do painel de visualização do _[!UICONTROL Email]_.

![Clique em Adicionar conteúdo de email ](./assets/add-email-content.png){width="700" zoomable="yes"}

Essa ação inicia o Designer de email, onde você pode escolher como deseja criar seu email a partir das seguintes opções:

* [Crie o email do zero](#design-your-email-from-scratch) usando a interface Designer de email.

* [Importar conteúdo de HTML existente](#import-existing-html-content) de um arquivo ou de uma pasta .zip.

* [Selecione um modelo existente](#select-a-template) em uma lista de modelos de email predefinidos ou personalizados.

Para configurar e personalizar a linha de assunto com o editor de expressão, clique no ícone _Personalization_ e adicione qualquer um dos tokens Marketo Engage.

Após criar e personalizar o conteúdo do email, você pode exportar o conteúdo para validação ou para uso posterior. Clique em **[!UICONTROL Exportar HTML]** para salvar o conteúdo como um arquivo .zip que inclui seu HTML e seus ativos.

>[!TIP]
>
>Use o Assistente de IA no Adobe Journey Optimizer B2B Edition, alimentado por IA gerativa para elevar seu conteúdo ao próximo nível. O Assistente de IA pode ajudá-lo a otimizar o impacto de seus deliveries, gerando emails inteiros, conteúdo de texto direcionado e obtendo recomendações do Assistente de IA para imagens que refletem em seu público-alvo. [Saiba mais](./ai-assistant-emails.md)

### Projetar o email do zero

1. Na página inicial do Designer, selecione a opção **[!UICONTROL Design do zero]**.

1. Para iniciar o design do conteúdo, arraste um item das **[!UICONTROL Estruturas]** e solte-o na tela.

   Repita essa etapa para cada componente de estrutura para construir o layout do seu email.

1. Adicione quantos itens de _Estruturas_ forem necessários e edite as configurações para cada um no painel à direita.

   Selecione o componente de coluna n:n para definir o número de colunas de sua escolha (entre três e 10). Você também pode definir a largura de cada coluna movendo as setas abaixo dela.

   Cada tamanho de coluna não pode ser menor que 10% da largura total do componente de estrutura. Somente colunas vazias podem ser removidas.

1. Expanda a seção **[!UICONTROL Conteúdo]** e adicione quantos elementos forem necessários em um ou mais componentes da estrutura.

1. Se necessário, você pode fazer personalizações adicionais para cada componente nas guias _[!UICONTROL Configurações]_ ou _[!UICONTROL Estilo]_.

   Por exemplo, é possível alterar o estilo do texto, o preenchimento ou a margem de cada componente.

1. No Seletor de ativos, é possível selecionar diretamente os ativos armazenados na biblioteca do Assets.

   Clique duas vezes na pasta que contém seus ativos. Arraste e solte os itens em um componente de estrutura.

1. Insira campos de personalização para personalizar seu conteúdo de atributos de perfis, associações de público-alvo, atributos contextuais e muito mais.

<!-- 1. Click **[!UICONTROL Enable condition content]** to add dynamic content and adapt the content to the targeted profiles based on conditional rules.
-->
1. Selecione a guia **[!UICONTROL Links]** no painel esquerdo para exibir todas as URLs do seu conteúdo que são rastreadas.

   Você pode modificar o _Tipo de Rastreamento_ ou o _Rótulo_ e adicionar marcas, se necessário.

Se necessário, você pode personalizar seu email clicando em **[!UICONTROL Alternar para o editor de código]** no menu avançado. O editor de código permite editar o código fonte do email, como adicionar tags de rastreamento ou HTML personalizadas.

>[!CAUTION]
>
>Você não pode reverter para o designer visual neste email depois de alternar para o editor de código.

Quando o conteúdo estiver concluído, clique em **[!UICONTROL Simular conteúdo]** na parte superior para verificar a renderização. Você pode escolher a visualização de desktop ou móvel.

Quando estiver pronto, clique em Salvar.

### Importar conteúdo de HTML existente

O conteúdo importado pode ser:

* Um arquivo HTML com uma folha de estilos incorporada
* Uma pasta .zip que inclui um arquivo HTML, a folha de estilos (.css) e os arquivos de imagem

>[!NOTE]
>
>Não há restrições na estrutura do arquivo .zip. No entanto, as referências devem ser relativas e se encaixar na estrutura de árvore da pasta .zip.

_Para importar um arquivo com conteúdo HTML:_

1. Na página inicial do Designer de email, selecione **[!UICONTROL Importar HTML]**.

1. Arraste e solte o arquivo HTML ou .zip que contém o conteúdo HTML e clique em [!UICONTROL Importar].

   Quando o carregamento do conteúdo do HTML for concluído, seu conteúdo estará no _Modo de compatibilidade_. Nesse modo, você só pode personalizar seu texto, adicionar links ou incluir ativos ao seu conteúdo.

### Selecione um modelo

Você pode escolher entre:

* Modelos de exemplo. A interface do Journey Optimizer oferece 20 modelos de email prontos para uso que você pode escolher.

* Modelos salvos.

* Um modelo personalizado que você criou do zero usando o menu _Modelos_ ou salvou de um email em uma jornada usando a opção _[!UICONTROL Salvar como modelo de conteúdo]_.

_Para começar a criar seu conteúdo com um dos modelos de exemplo ou salvos:_

1. Acesse o _Designer de email_ do espaço de trabalho de edição de conteúdo de email.

   Na página _[!UICONTROL Criar email]_, a guia **[!UICONTROL Modelos de amostra]** é selecionada por padrão.

1. Para usar um modelo personalizado, selecione a guia **[!UICONTROL Modelos salvos]**.

   A lista de todos os modelos de conteúdo criados na sandbox atual é exibida. Você pode classificá-los por nome, Última modificação ou Última criação.

1. Selecione o template de sua escolha na lista.

1. Depois de selecionar uma categoria, você pode navegar entre todos os modelos dessa categoria (amostra ou salvo, dependendo da seleção) usando as setas para a direita e para a esquerda.

1. Clique em **[!UICONTROL Usar este modelo]** na parte superior direita da página.

1. Edite o conteúdo conforme necessário na _Designer de email_.

## Verificar alertas

À medida que você cria o conteúdo da sua mensagem de email, os alertas são exibidos na interface (canto superior direito da página) quando as principais configurações estão ausentes.

Se você não vir esse botão, não há problemas detectados.

Dois tipos de alertas podem ser detectados:

* **_Avisos_** que se referem a recomendações e práticas recomendadas, como:

   * `The opt-out link is not present in the email body`: adicionar um link de cancelamento de assinatura ao corpo do email é uma prática recomendada.

     >[!NOTE]
     >
     >As mensagens de email de estilo de marketing devem incluir um link para opção de não participação, que não é necessário para mensagens transacionais.

   * `Text version of HTML is empty`: não se esqueça de definir uma versão de texto do corpo do email, que é usada quando o conteúdo do HTML não pode ser exibido.

   * `Empty link is present in email body`: verifique se todos os links no seu email estão corretos.

   * `Email size has exceeded the limit of 100KB`: para uma entrega ideal, verifique se o tamanho do seu email não excede 100KB.

* **_Erros_** que impedem que você teste ou ative a jornada/campanha enquanto não forem resolvidos, como:

   * `The subject line is missing`: a linha de assunto do email é obrigatória.

   * `The email version of the message is empty`: este erro é exibido quando o conteúdo do email não foi configurado.

## Verificar e testar o email

Quando o conteúdo da mensagem é definido, você pode usar perfis de teste para pré-visualizá-la, enviar provas e controlar sua renderização em clientes populares de desktop, móveis e baseados na Web. Se você inseriu conteúdo personalizado, é possível visualizar como esse conteúdo é exibido na mensagem usando os dados do perfil de teste.

Para visualizar o conteúdo do email, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar sua mensagem usando os dados do perfil de teste.

![Simular o conteúdo do email para verificar seu design](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
