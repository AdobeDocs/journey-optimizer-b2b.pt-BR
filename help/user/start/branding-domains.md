---
title: Configurar domínios de marca
description: Configure os domínios de marca para que cada uma das marcas tenha seus próprios links de rastreamento de marca.
feature: Setup, Channels
role: Admin
exl-id: ccbcbbee-a5be-46fe-bae0-ab026e5cdb72
source-git-commit: 0f34a98753b71b388c822ef4a26dbae6b4c8fb1b
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 89%

---

# Configurar domínios de marca

Um domínio de marca no Marketo Engage é um subdomínio personalizado (como `links.yourcompany.com`) usado para reescrever links e rastrear cliques em email e garantir que eles reflitam sua marca em vez de um domínio genérico. Cada domínio de marca atua como um domínio de rastreamento de cliques para aprimorar a capacidade de entrega e a confiança, correspondendo seus links de email e de página de aterrissagem ao seu domínio.

* Ele substitui links genéricos por sua própria marca em hiperlinks de email.
* Quando um lead de conta clica em um link, ele é redirecionado por meio desse domínio personalizado para permitir o rastreamento de desempenho enquanto parece legítimo para filtros de email.
* Se você tiver várias marcas, poderá configurar domínios de marca adicionais para serem compatíveis com diferentes unidades de negócios ou marcas.

>[!BEGINSHADEBOX]

**CNAMEs exclusivos para links de rastreamento**

Os links de rastreamento de email devem ser novos e exclusivos para a instância do Marketo Engage anexada. Se você tiver CNAMEs existentes para rastrear links que apontam para uma instância do Marketo Engage pré-existente (produção), eles não poderão ser reutilizados sem modificação.

Você pode compartilhar a identidade visual do domínio do caminho de retorno entre a instância do Marketo Engage de produção e a instância anexada, mas essa é uma alteração de back-end. Abra um tíquete de suporte e forneça seu prefixo do Marketo Engage (Munchkin ID) e seu novo prefixo do Journey Optimizer B2B edition (Munchkin ID) para solicitar a marca de domínio do caminho de retorno compartilhado.

>[!ENDSHADEBOX]

>[!PREREQUISITES]
>
>Antes de editar ou adicionar um domínio na interface do usuário, você deve ter um [CNAME mapeado para um domínio do Marketo Engage fornecido pela Adobe](https://experienceleague.adobe.com/pt-br/docs/marketo/using/getting-started/initial-setup/setup-steps#customize-your-landing-page-urls-with-a-cname){target="_blank"}.
>
>Ao adicionar um domínio, o sistema verifica se há SSLs pré-existentes, que podem ter sido criados manualmente antes. Se encontrar essa validação, crie seu domínio sem selecionar a criação de SSL e depois conecte-o como um procedimento separado.

## Acessar domínios de marca na Marketo Engage

1. Vá para a área **[!UICONTROL Administrador]** na sua instância do Marketo Engage e selecione **[!UICONTROL Email]**.

1. Role para baixo até o painel **[!UICONTROL Domínios de marca]**.

   ![Painel Domínios de marca no Admin em Email, mostrando o domínio padrão](./assets/me-admin-email-branding-domains.png){width="700" zoomable="yes"}

   A lista exibe o domínio padrão da instância do Marketo Engage.

## Editar seu domínio de marca padrão

A primeira etapa ao trabalhar com domínios de marca é editar o domínio de marca padrão definido na instância do Marketo Engage.

>[!NOTE]
>
>Você não pode definir um domínio de marca adicional até ter editado o domínio padrão genérico.

1. No painel _[!UICONTROL Domínios de Identidade Visual]_, selecione o domínio genérico e clique em **[!UICONTROL Editar]** na parte superior.

   ![Painel Domínios de marca com o domínio genérico selecionado](./assets/me-admin-email-branding-domains-edit-default.png){width="500"}

1. Na caixa de diálogo _[!UICONTROL Editar domínio de marca]_, digite o nome do domínio padrão no campo **[!UICONTROL Domínio]**.

   ![Caixa de diálogo Editar Domínio de Identidade Visual](./assets/me-admin-email-branding-domains-edit-default-name.png){width="400"}

1. Se você tiver vários espaços de trabalho definidos para sua instância do Marketo Engage, clique em **[!UICONTROL Avançar]**.

   Selecione cada um dos espaços de trabalho aos quais deseja aplicar o domínio principal atualizado.

   ![Caixa de diálogo Editar Domínio de Identidade Visual com seleção de espaço de trabalho para o domínio primário](./assets/me-admin-email-branding-domains-edit-default-workspaces.png){width="400"}

1. Clique em **[!UICONTROL Salvar]**.

## Definir um domínio adicional

Após editar o domínio padrão, é possível adicionar outro domínio de marca para oferecer suporte a várias marcas no ambiente do Journey Optimizer B2B Edition, em que cada um tem seus próprios links de rastreamento de marca. Ao adicionar um domínio, você tem as seguintes opções:

>* _Tornar Domínio Primário_: Tornar este o domínio primário do espaço de trabalho. Ao selecionar essa opção, todos os emails não enviados existentes são definidos como o domínio primário padrão e todos os emails recém-criados são automaticamente padronizados para esse domínio primário. Os profissionais de marketing podem escolher um domínio alternativo de marca onde necessário.
>
>* _Gerar Certificado SSL_: crie uma SSL (Secure Sockets Layer) com a criação do domínio. O primeiro domínio de rastreamento inicia uma configuração única da infraestrutura que pode levar algumas horas. O sistema envia uma notificação após a conclusão.

_Para adicionar o domínio :_

1. No painel _[!UICONTROL Domínios de Identidade Visual]_, clique em **[!UICONTROL Adicionar]** na parte superior.

   Painel ![Domínios de marca com o botão Adicionar na parte superior](assets/me-admin-email-branding-domains-add.png){width="500"}

1. Na caixa de diálogo _[!UICONTROL Novo Domínio de Identidade Visual]_, digite o nome do domínio de identidade visual no campo **[!UICONTROL Domínio]**.

1. (Opcional) Marque a caixa de seleção **[!UICONTROL Gerar certificado SSL]** para gerar automaticamente um SSL para o domínio.

   ![Caixa de diálogo Novo Domínio de Identidade Visual](assets/me-admin-email-branding-domains-add-name.png){width="400"}

   Se necessário e disponível, você também pode marcar a caixa de seleção _Tornar Domínio Primário_.

   >[!NOTE]
   >
   >**_SSLs personalizados_**: se você precisar de um SSL personalizado, poderá enviar um [tíquete de suporte](https://experienceleague.adobe.com/pt-br/support){target="_blank"}. Não use a caixa de seleção para criação de SSL.

1. Se você tiver vários espaços de trabalho definidos para sua instância do Marketo Engage, clique em **[!UICONTROL Avançar]**.

   Se necessário, selecione cada um dos espaços de trabalho aos quais deseja aplicar o novo domínio como o domínio primário.

   ![Caixa de diálogo Novo Domínio de Marca com seleção de espaço de trabalho para aplicar o domínio primário](assets/me-admin-email-branding-domains-add-workspaces.png){width="400"}

1. Clique em **[!UICONTROL Salvar]**.

## Editar SSLs para domínios de marca existentes

Siga estas etapas para habilitar o SSL nos domínios existentes.

1. Na área _[!UICONTROL Administrador]_, selecione **[!UICONTROL Email]**.

1. No painel _[!UICONTROL Domínios de Identidade Visual]_, selecione a linha de domínio e clique em **[!UICONTROL Adicionar SSL]**.

   Painel ![Domínios de marca com Adicionar SSL no início](./assets/me-admin-email-branding-domain-add-ssl.png){width="500"}

1. Na caixa de diálogo, clique em **[!UICONTROL Confirmar]**.

   ![Caixa de diálogo de confirmação Gerar Certificado SSL](./assets/me-admin-email-branding-domain-generate-ssl-cert-confirm.png){width="400"}

## Mensagens de erro

| Erro | Detalhes |
| ----- | ------- |
| `Domain already exists.` | Já existe um domínio com o mesmo nome. |
| `Domain is not mapped to the default domain.` | O domínio personalizado não está mapeado corretamente para o domínio padrão. Verifique as configurações de mapeamento de domínio e certifique-se de que a configuração DNS aponte para o domínio padrão correto. |
| `SSL certificates could not be issued due to unsupported CAA records. Request your IT to update your CAA records.` | Os registros CAA não estão atualizados. Para aqueles que usam certificados SSL gerenciados pela Adobe, os registros CAA devem ser atualizados para certificados recomendados pelo fornecedor. |
| `SSL certificate has already been issued.` | Já existe um certificado SSL para este domínio personalizado. Nenhuma ação adicional é necessária, a menos que o certificado expire ou precise ser reemitido. |
| `The default domain was not found. Please contact Support for assistance.` | Ocorreu um problema ao tentar localizar o domínio padrão. Entre em contato com o suporte da Adobe para acionar uma investigação. |
| `Unexpected error encountered while creating a domain. Please contact Support for assistance.` | Ocorreu um erro inesperado. Colete registros e detalhes de erros e, em seguida, encaminhe o problema para o suporte da Adobe. |

## Excluir um domínio de marca

>[!NOTE]
>
>Para excluir o domínio primário de marca (em um ou mais espaços de trabalho), primeiro selecione um domínio de marca diferente para ser o principal de cada espaço de trabalho.
>
>A exclusão de um domínio **_não_** exclui o certificado SSL. Essa proteção evita erros de usuário que resultam na ausência de certificados SSL em um site. Se você quiser remover os certificados SSL, entre em contato com o suporte da Adobe.

No painel _[!UICONTROL Domínios de Identidade Visual]_, selecione o domínio e clique em **[!UICONTROL Excluir]** na parte superior.
