---
title: Content Credentials
description: Saiba como o Adobe Journey Optimizer B2B edition aplica automaticamente o Content Credentials a imagens geradas ou editadas com ferramentas de IA geradora e o que isso significa para o seu conteúdo.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: edb796d131c2b058215b73519b845125432d84f8
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 0%

---

# Content Credentials

As organizações de marketing estão mais preocupadas do que nunca com a transparência do conteúdo, a divulgação de IA e a prevenção de adulteração de ativos. O Content Authenticity Initiative (CAI) na Adobe cria ferramentas compatíveis com o padrão técnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). O _Content Credentials_ é o conjunto de metadados criptografados e invioláveis que ajuda os visualizadores a entender a linhagem do conteúdo e garantir a integridade dos ativos da marca. Essas informações incluem:

* Emissor ou signatário - Informações sobre a entidade ou empresa que emitiu a assinatura digital para certificar ou assinar o ativo.
* Data de emissão - A data em que a Content Credential foi aplicada ao ativo.
* Crédito e uso - Informações sobre o produtor do ativo, incluindo nome, identificadores de mídia social ou outras informações relacionadas à identidade.
* Processo - Registros de qualquer edição ou modificação feita no ativo.
* Detalhes do dispositivo — informações sobre o aplicativo ou dispositivo usado para criar ou editar o ativo.
* Ferramenta de IA usada - se a IA gerativa foi usada para editar ou criar o ativo, o nome do modelo usado pode ser incluído.
* Outras informações relevantes - dados adicionais também podem ser incluídos para ajudar a oferecer mais contexto sobre o histórico de um ativo.

Para obter informações abrangentes sobre o histórico de ativos, você pode usar a [ferramenta de inspeção](https://contentauthenticity.adobe.com/inspect) do Adobe Content Authenticity.

O Content Credentials persiste com o arquivo de imagem. Quando uma imagem gerada ou editada com IA gerativa é carregada ou exportada do [!DNL Adobe Journey Optimizer B2B Edition], sua Content Credentials é preservada.

>[!NOTE]
>
>Alguns métodos de importação de imagens para seu conteúdo, como extrair uma imagem de um PDF ou de uma fonte incorporada (base64), podem não preservar o Content Credentials original. Nesses casos, o Content Credentials não pode ser lido da fonte e nenhum é criado para o resultado.

>[!BEGINSHADEBOX]

## Persistência do Content Credentials por meio de canais {#channels}

Quando você inclui imagens em seu email ou mensagens de WhatsApp, o Content Credentials das imagens entregues também é mantido:

* **Email** - Quando você usar uma ação de jornada _Enviar email_, adicione a imagem ao seu conteúdo de email da biblioteca _Assets_. Quando o email é entregue, o recipient pode baixar a imagem da mensagem e a Content Credentials fica intacta.
* **WhatsApp** - Adicione a imagem ao seu modelo de mensagem do WhatsApp na sua conta comercial do Meta. Você pode adicioná-lo diretamente do seu próprio sistema ou baixar um arquivo de imagem da biblioteca do _Assets_. Use o modelo para uma ação de jornada _Enviar WhatsApp_. Quando a mensagem do WhatsApp é entregue, o recipient pode baixar a imagem da mensagem e a Content Credentials fica intacta.

>[!ENDSHADEBOX]

## Ações que afetam o Content Credentials {#cc-workflows}

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Content Credentials são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

Ao gerar ou editar uma imagem com ferramentas de IA gerativa no [!DNL Journey Optimizer B2B Edition], o Content Credentials é anexado automaticamente a essa imagem e nenhuma ação é necessária da sua parte.

### Gerar uma imagem {#generate}

**_Exemplo:_** Gere uma imagem de banner para um email a partir de um prompt de texto que descreve o visual desejado. Os Content Credentials são anexados à imagem gerada.

Quando você cria uma nova imagem a partir de um prompt de texto, de uma imagem de referência ou gera uma imagem semelhante, o Content Credentials é sempre anexado.

### Cortar uma imagem {#crop}

**_Exemplos:_**

* Cortar uma imagem de banner gerada para ajustá-la a uma página da Web. As Content Credentials são preservadas durante o corte.
* Use uma foto de arquivo carregada como plano de fundo de email e corte-a para caber na tela. Se a foto não transporta informações de IA gerativas, o Content Credentials não é criado.

Quando você faz um ajuste em um arquivo de imagem, como recortá-lo nas dimensões solicitadas, ele retém o Content Credentials somente se a imagem de origem já as tiver. O recorte recria os pixels da imagem, que normalmente remove essa Content Credential. Portanto, o AI Assistant a lê da imagem de origem antes do recorte e, em seguida, a recria e anexa novamente ao resultado recortado. O corte em si não adiciona uma nova ação de IA gerativa; ele preserva a existente.

### Adicionar uma sobreposição de texto

**_Exemplo:_** Produza um título promocional como uma sobreposição de texto em uma imagem de fundo gerada para uma página de aterrissagem. A Content Credentials da imagem de fundo é preservada.

Ao renderizar o texto gerado sobre uma imagem de plano de fundo, as Content Credentials são anexadas à imagem resultante somente se a imagem de plano de fundo já tiver Content Credentials. A renderização da sobreposição produz uma nova imagem, de modo que a ferramenta de edição de imagens lê a Content Credentials no plano de fundo e as reanexa ao resultado. A etapa de sobreposição não adiciona uma nova ação de IA gerativa.

### Sobrepor uma imagem

**_Exemplos:_**

* Crie um cabeçalho de email combinando uma imagem de produto gerada com um plano de fundo gerado. O resultado carrega o Content Credentials, refletindo ambas as fontes de IA geradoras.
* Combine duas fotos de marca carregadas em uma imagem de colagem. Como nenhuma imagem de origem carrega uma ação de IA gerativa, o Content Credentials não é criado.

Quando você compõe duas ou mais imagens juntas e qualquer uma das imagens de origem tem Content Credentials, a imagem combinada as retém, mescladas em um único elemento de metadados do Content Credentials. A composição produz uma nova imagem a partir das fontes, o que normalmente remove essas Content Credentials. Mas as ferramentas de edição de imagens leem cada uma antes da composição e, em seguida, criam um único elemento combinado do Content Credentials que lista cada origem que contribuiu para uma ação geradora de IA.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see Content Credentials directly within the _Assets_ library. When you open the asset details, any image with Content Credentials (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the Content Credentials remain intact with the asset.

_To access Content Credentials:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->