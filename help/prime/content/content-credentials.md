---
title: Content Credentials
description: Saiba como o Adobe Journey Optimizer B2B Prime aplica automaticamente o Content Credentials a imagens geradas com IA gerativa e o que isso significa para o seu conteúdo.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: edb796d131c2b058215b73519b845125432d84f8
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 0%

---

# Content Credentials

As organizações de marketing estão mais preocupadas do que nunca com a transparência do conteúdo, a divulgação de IA e a prevenção de adulteração de ativos. O Content Authenticity Initiative (CAI) na Adobe cria ferramentas compatíveis com o padrão técnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). O _Content Credentials_ é o conjunto de metadados criptografados e invioláveis que podem ajudar os visualizadores a entender a linhagem do conteúdo e garantir a integridade dos ativos da marca. Essas informações incluem:

* Emissor ou signatário — Informações sobre a entidade ou empresa que emitiu a assinatura digital para certificar ou assinar o ativo.
* Data de emissão — A data em que a Content Credential foi aplicada ao ativo.
* Crédito e uso — Informações sobre o produtor do ativo, incluindo nome, identificadores de mídia social ou outras informações relacionadas à identidade.
* Processo — Registros de qualquer edição ou modificação feita no ativo.
* Detalhes do dispositivo — Informações sobre o aplicativo ou dispositivo usado para criar ou editar o ativo.
* Ferramenta de IA usada — se a IA gerativa foi usada para criar o ativo, o nome do modelo usado pode ser incluído.
* Outras informações relevantes — dados adicionais também estão incluídos para ajudar a oferecer mais contexto sobre o histórico de um ativo.

Para obter informações abrangentes sobre o histórico de ativos, você pode usar a [ferramenta de inspeção](https://contentauthenticity.adobe.com/inspect) do Adobe Content Authenticity.

O Content Credentials persiste com o arquivo de imagem. Quando uma imagem gerada ou editada com IA gerativa é carregada ou exportada do [!DNL Adobe Journey Optimizer B2B Prime], sua Content Credentials é preservada.

>[!NOTE]
>
>Alguns métodos de importação de imagens para seu conteúdo, como extrair uma imagem de um PDF ou de uma fonte incorporada (base64), podem não preservar o Content Credentials original. Nesses casos, o Content Credentials não pode ser lido da fonte e nenhum é criado para o resultado.

>[!BEGINSHADEBOX]

## Persistência do Content Credentials por meio de canais {#channels}

Quando você inclui imagens em seu email ou mensagens de WhatsApp, o Content Credentials das imagens entregues também é mantido:

* **Email** - Quando você usar uma ação de jornada _Enviar email_, adicione a imagem ao seu conteúdo de email da biblioteca _Assets_. Quando o email é entregue, o recipient pode baixar a imagem da mensagem e a Content Credentials fica intacta.
* **WhatsApp** - Adicione a imagem ao seu modelo de mensagem do WhatsApp na sua conta comercial do Meta. Você pode adicioná-lo diretamente do seu sistema ou baixar um arquivo de imagem da biblioteca do _Assets_. Use o modelo para uma ação de jornada _Enviar WhatsApp_. Quando a mensagem do WhatsApp é entregue, o recipient pode baixar a imagem da mensagem e a Content Credentials fica intacta.

>[!ENDSHADEBOX]

## Geração de imagem {#generate}

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Content Credentials são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

Quando você usa a IA gerativa para criar uma imagem para o seu conteúdo de email no [!DNL Journey Optimizer B2B Prime], a Content Credentials é anexada automaticamente à imagem gerada e nenhuma ação é necessária da sua parte. As ferramentas de IA gerativa produzem um elemento de Content Credentials combinado para variantes de imagens com credenciais existentes, incluindo a origem original.

>[!NOTE]
>
>No momento, o [!DNL Journey Optimizer B2B Prime] não oferece suporte a ações de edição manual de imagens. Os workflows do Content Credentials para essas ações não se aplicam no momento.
