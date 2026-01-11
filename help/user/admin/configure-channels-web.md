---
title: Configurações do canal da Web
description: Saiba como definir as configurações de canal da Web para definir propriedades da Web e regras de correspondência de páginas para entrega de conteúdo no Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Configurações do canal da Web

Uma configuração da Web é uma propriedade da Web identificada por um URL em que o conteúdo é entregue. Ele pode corresponder a um único URL de página ou a várias páginas para que as experiências da Web possam fornecer modificações em uma ou várias páginas da Web. Essas configurações são necessárias para que os profissionais de marketing [adicionem nós de ação de personalização da Web no jornada](../content/web-experiences.md#create-a-web-experience) e [criem modificações na experiência](../content/web-experience-design.md) para uma campanha.

>[!BEGINSHADEBOX]

**Pré-requisitos**

Para usar canais da Web, o site deve ter a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementada para identificação de visitantes e entrega de conteúdo. Verifique se a versão do Adobe Experience Platform Web SDK é a 2.16 ou superior.

A configuração do canal da Web no Journey Optimizer B2B edition requer as [permissões](../admin/user-management.md#b2b-product-permissions) a seguir:

* _[!UICONTROL Configurações de Canal]_ > _[!UICONTROL Gerenciar Predefinições de Mensagens]_ - Necessário para criar, atualizar e excluir configurações de canal Web.
* _[!UICONTROL Configurações de Canal]_ > _[!UICONTROL Exibir Predefinições de Mensagens]_ - Necessário para exibir configurações de canal da Web.

>[!ENDSHADEBOX]

## Criar uma configuração de canal da Web

1. Na navegação à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]**.

1. Em _[!UICONTROL Web]_, no painel de navegação, selecione **[!UICONTROL Configurações de canal]**.

   ![Acessar as configurações de canal da Web](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Clique em **[!UICONTROL Criar configuração de canal]** na parte superior direita.

1. Insira um **[!UICONTROL Nome]** (obrigatório) e uma **[!UICONTROL Descrição]** (opcional) para a configuração.

   >[!NOTE]
   >
   >Os nomes devem começar com uma letra (A-Z) e podem conter apenas caracteres alfanuméricos. Você também pode usar sublinhado `_`, ponto `.` e hífen `-` caracteres.

1. Na seção **[!UICONTROL Configurações da Web]**, selecione uma das seguintes opções:

   * **[!UICONTROL Página única]** - Se quiser aplicar as alterações a uma única página, insira ou selecione uma **[!UICONTROL URL de página]**.

     ![Selecionando uma URL de página para uma configuração de canal da Web de página única](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Regra de correspondência de páginas]** - Para direcionar várias URLs correspondentes à mesma regra, crie uma [regra de correspondência de páginas](#build-a-pages-matching-rule) e insira uma **[!UICONTROL URL de criação e visualização padrão]**.

1. Clique em **[!UICONTROL Enviar]** para salvar suas alterações.

Depois de salvar a configuração, ela estará em um status de _Rascunho_ e estará disponível aos profissionais de marketing quando eles usarem um canal da Web em suas jornadas. Você pode continuar editando a configuração enquanto ela permanecer no estado de rascunho. Você também pode excluir uma configuração de canal da Web de rascunho clicando no ícone _Mais_ (**...**) ao lado do nome e escolhendo **[!UICONTROL Excluir]**.

Assim que o canal da Web for usado em uma jornada, ele será movido para o status _Ativo_. Nesse estado, é possível editar o nome e a descrição da configuração. Não é possível alterar as configurações da Web ou excluir a configuração.

## Regras de correspondência de páginas {#pages-matching-rule}

Ao criar uma configuração da Web, você pode criar uma _[!UICONTROL regra de correspondência de páginas]_ para direcionar várias URLs que correspondam à mesma regra. Essas regras permitem aplicar as mesmas alterações de conteúdo em várias páginas.

Por exemplo, talvez você queira aplicar as alterações em um banner principal em todo o site ou adicionar uma imagem superior que seja exibida em todas as páginas do produto.

### Criar uma regra

1. Ao [criar uma configuração de canal da Web](#create-a-web-channel-configuration), escolha **[!UICONTROL Regra de correspondência de páginas]**.

1. Defina seus critérios para os campos **[!UICONTROL Domínio]** e **[!UICONTROL Página]** usando os diferentes operadores em cada seção para criar a regra.

   +++Operadores de domínio

   Use os seguintes operadores para domínios correspondentes de acordo com o valor da string inserido:

   | Operador | Descrição | Exemplos |
   | --- | --- | --- |
   | [!UICONTROL Igual] | Correspondência exata do domínio. | |
   | [!UICONTROL Começa com] | Corresponde a todos os domínios (incluindo subdomínios) que começam com a cadeia de caracteres inserida. | `Starts with: dev` corresponde a todos os domínios e subdomínios que começam com `dev`, como `dev.example.com`, `dev.products.example.com` e `developer.example.com` |
   | [!UICONTROL Termina com] | Corresponde a todos os domínios (incluindo subdomínios) que terminam com a cadeia de caracteres inserida. | `Ends with: example.com` corresponde a todos os domínios e subdomínios que terminam com `example.com`, como `stage.example.com`, `prod.example.com` e `myexample.com` |
   | [!UICONTROL Correspondência de curinga] | Permite definir uma correspondência curinga no meio da cadeia de caracteres, como `dev.*.example.com`. As regras de validação exigem que o valor contenha apenas um curinga (asterisco) quando o operador for _correspondente a curinga_. | `Wildcard matching: dev.*.example.com` corresponde a domínios como `dev.products.example.com`, `dev.mytest.products.example.com` e `dev.blog.example.com` |
   | [!UICONTROL Qualquer] | Corresponde a todos os domínios. É útil ao testar um caminho específico entre domínios. | |

   +++

   +++Operadores de caminho

   Use os seguintes operadores para caminhos correspondentes de acordo com o valor da string inserido:

   | Operador | Descrição | Exemplos |
   | --- | --- | --- |
   | [!UICONTROL Igual] | Correspondência exata do caminho. | |
   | [!UICONTROL Começa com] | Corresponde a todos os caminhos (incluindo subcaminhos) que começam com a cadeia de caracteres. | |
   | [!UICONTROL Termina com] | Corresponde a todos os caminhos (incluindo subcaminhos) que terminam com a cadeia de caracteres. | |
   | [!UICONTROL Qualquer] | Corresponde a todos os caminhos. É útil ao direcionar todos os caminhos em um ou vários domínios. | |
   | [!UICONTROL Correspondência de curinga] | Permite definir um curinga interno dentro do caminho, como `/products/*/detail`. O caractere curinga `*` no componente de caminho corresponde a qualquer sequência de caracteres até o primeiro caractere `/`.  E `/*/` corresponde a qualquer sequência de caracteres (incluindo subcaminhos). | `Wildcard matching: /products/*/detail` corresponde a caminhos como `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` e `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contém] | O valor é convertido em um curinga, como `*mystring*`, e corresponde a todos os caminhos que contêm a sequência de caracteres. | `Contains: product` corresponde a todos os caminhos que contêm a cadeia de caracteres `product`, como `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` e `example.com/home/product/page` |

   +++

   Por exemplo, para dar suporte a alterações de conteúdo em todas as páginas de solução do _LumaSecure_ do seu site _Bodea_, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Inicia com]** > `bodea` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `lumasecure`.

   ![Definindo uma regra de correspondência de páginas para uma configuração de canal da Web](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Se o caso de uso exigir várias regras, clique em **[!UICONTROL Adicionar outra regra de página]** e repita a etapa anterior.

   * É possível definir até 10 regras.

   * Use os operadores **[!UICONTROL Or]** ou **[!UICONTROL Exclude]** entre as diferentes regras.

     _[!UICONTROL Or]_ é o operador padrão para definir várias regras e é útil para adicionar várias definições de critérios que podem ser correspondidos.

     _[!UICONTROL Excluir]_ é útil quando uma das páginas que correspondem à regra definida não deve ser direcionada. Por exemplo, você pode direcionar todas as `bodea.com` páginas que contenham `lumasecure`, mas excluindo as páginas do blog (como `bodea.com/blogs/lumasecure/latest-release`).

   ![Regras de correspondência de páginas com exclusão](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Insira a **[!UICONTROL URL padrão de criação e visualização]**.

   Essa etapa garante que as páginas geradas ou correspondidas pela regra tenham um URL designado para fins de design de conteúdo de experiência na Web e pré-visualização.

## Duplicação de um canal da Web

É possível duplicar uma configuração de canal da Web existente e alterá-la para criar um novo canal da Web com base em um existente. Uma configuração de canal da Web ativo salva na biblioteca não pode ser modificada.

1. Clique no ícone do _Mais menu_ (**...**) para a variante e escolha **[!UICONTROL Duplicar]**.

   ![Clique no ícone de mais nenu para duplicar uma configuração de canal da Web existente](./assets/config-web-channels-more-menu.png){width="450"}

   Esta ação cria um canal da Web duplicado com `_Copy_nnn` anexado ao nome.

1. Clique no nome do canal da Web duplicado para editar os parâmetros.

   * Altere o nome e a descrição para corresponder à finalidade ou aos itens na regra.
   * Se necessário, altere o URL da página única.
   * Se necessário, altere a regra de correspondência de páginas de acordo com seus requisitos.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Enviar]**.
