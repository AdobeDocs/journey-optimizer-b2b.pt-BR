---
title: Metadados C2PA
description: Saiba como o Adobe Journey Optimizer B2B edition aplica automaticamente metadados C2PA a imagens geradas ou editadas com ferramentas de IA geradora e o que isso significa para o seu conteúdo.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: dd969d66eab5649ccb19fe6582dafe0b7304772c
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# Metadados do C2PA

As organizações de marketing estão mais preocupadas do que nunca com a transparência do conteúdo, a divulgação de IA e a prevenção de adulteração de ativos. O Content Authenticity Initiative (CAI) na Adobe cria ferramentas compatíveis com o padrão técnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _Os metadados C2PA_ são informações criptografadas e invioláveis que ajudam os visualizadores a entender a linhagem do conteúdo e garantir a integridade dos ativos da marca. Essas informações incluem:

* Emissor ou signatário - Informações sobre a entidade ou empresa que emitiu a assinatura digital para certificar ou assinar o ativo.
* Data de emissão - A data em que os metadados do C2PA foram aplicados ao ativo.
* Crédito e uso - Informações sobre o produtor do ativo, incluindo nome, identificadores de mídia social ou outras informações relacionadas à identidade.
* Processo - Registros de qualquer edição ou modificação feita no ativo.
* Detalhes do dispositivo — informações sobre o aplicativo ou dispositivo usado para criar ou editar o ativo.
* Ferramenta de IA usada - se a IA gerativa foi usada para editar ou criar o ativo, o nome do modelo usado pode ser incluído.
* Outras informações relevantes - dados adicionais também podem ser incluídos para ajudar a oferecer mais contexto sobre o histórico de um ativo.

Para obter informações abrangentes sobre o histórico de ativos, você pode usar a [ferramenta de inspeção](https://contentauthenticity.adobe.com/inspect) do Adobe Content Authenticity.

Os metadados C2PA persistem com o arquivo de imagem. Quando uma imagem gerada ou editada com IA gerativa é carregada para ou exportada do [!DNL Adobe Journey Optimizer B2B Edition], seus metadados C2PA são preservados.

>[!NOTE]
>
>Alguns métodos de importação de imagens para seu conteúdo, como extrair uma imagem de um PDF ou de uma fonte incorporada (base64), podem não preservar os metadados C2PA originais. Nesses casos, os metadados C2PA não podem ser lidos na origem e nenhum é criado para o resultado.

>[!BEGINSHADEBOX]

## Persistência de metadados C2PA por meio de canais {#channels}

Quando você inclui imagens em seu e-mail ou mensagens de WhatsApp, os metadados C2PA para as imagens entregues também são mantidos:

* **Email** - Quando você usar uma ação de jornada _Enviar email_, adicione a imagem ao seu conteúdo de email da biblioteca _Assets_. Quando o email é entregue, o recipient pode baixar a imagem da mensagem e os metadados do C2PA ficam intactos.
* **WhatsApp** - Adicione a imagem ao seu modelo de mensagem do WhatsApp na sua conta comercial do Meta. Você pode adicioná-lo diretamente do seu próprio sistema ou baixar um arquivo de imagem da biblioteca do _Assets_. Use o modelo para uma ação de jornada _Enviar WhatsApp_. Quando a mensagem do WhatsApp é entregue, o recipient pode baixar a imagem da mensagem e os metadados do C2PA estão intactos.

>[!ENDSHADEBOX]

## Ações que afetam os metadados do C2PA {#cc-workflows}

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Os metadados C2PA são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

Ao gerar ou editar uma imagem com ferramentas de IA gerativa no [!DNL Journey Optimizer B2B Edition], os metadados C2PA são anexados automaticamente a essa imagem e nenhuma ação é necessária da sua parte.

### Gerar uma imagem {#generate}

**_Exemplo:_** Gere uma imagem de banner para um email a partir de um prompt de texto que descreve o visual desejado. Os metadados C2PA são anexados à imagem gerada.

Quando você cria uma nova imagem a partir de um prompt de texto, de uma imagem de referência ou gera uma imagem semelhante, os metadados C2PA são sempre anexados.

### Cortar uma imagem {#crop}

**_Exemplos:_**

* Cortar uma imagem de banner gerada para ajustá-la a uma página da Web. Os metadados C2PA são preservados por meio do corte.
* Use uma foto de arquivo carregada como plano de fundo de email e corte-a para caber na tela. Se a foto de estoque não transporta informações de IA gerativas, os metadados C2PA não são criados.

Quando você faz um ajuste em um arquivo de imagem, como recortá-lo nas dimensões solicitadas, ele retém os metadados C2PA somente se a imagem de origem já os tinha. O recorte recria os pixels da imagem, o que normalmente remove esses metadados C2PA. Portanto, o Assistente de IA os lê da imagem de origem antes do recorte e, em seguida, os recria e anexa novamente ao resultado recortado. O corte em si não adiciona uma nova ação de IA gerativa; ele preserva a existente.

### Adicionar uma sobreposição de texto

**_Exemplo:_** Produza um título promocional como uma sobreposição de texto em uma imagem de fundo gerada para uma página de aterrissagem. Os metadados C2PA da imagem de fundo são preservados.

Quando você renderiza o texto gerado sobre uma imagem de fundo, os metadados C2PA são anexados à imagem resultante somente se a imagem de fundo já tiver metadados C2PA. A renderização da sobreposição produz uma nova imagem, de modo que a ferramenta de edição de imagens lê os metadados C2PA do plano de fundo e os reanexa ao resultado. A etapa de sobreposição não adiciona uma nova ação de IA gerativa.

### Sobrepor uma imagem

**_Exemplos:_**

* Crie um cabeçalho de email combinando uma imagem de produto gerada com um plano de fundo gerado. O resultado carrega metadados C2PA, refletindo ambas as fontes de IA geradoras.
* Combine duas fotos de marca carregadas em uma imagem de colagem. Como nenhuma imagem de origem carrega uma ação de IA gerativa, os metadados C2PA não são criados.

Quando você compõe duas ou mais imagens juntas e qualquer uma das imagens de origem tem metadados C2PA, a imagem combinada a retém, mesclada em um único elemento de metadados C2PA. A composição produz uma nova imagem a partir das fontes, o que normalmente remove esses metadados C2PA. Mas as ferramentas de edição de imagens leem os metadados de origem antes da composição e criam um único elemento de metadados C2PA combinado que lista cada origem que contribuiu para uma ação geradora de IA.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
