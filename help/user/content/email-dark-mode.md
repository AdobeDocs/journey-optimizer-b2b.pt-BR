---
title: Modo escuro para conteúdo de email
description: Saiba mais sobre o design de email no modo escuro no Journey Optimizer B2B edition. Visualize a renderização, personalize as configurações, garanta a acessibilidade e teste entre clientes de email.
feature: Email Authoring
topic: Content Management
hidefromtoc: true
role: User
level: Beginner, Intermediate
keywords: modo escuro, email, cor, design
source-git-commit: 9cb77da73778c313392af1c42632d6b9e7e92f3b
workflow-type: tm+mt
source-wordcount: '1600'
ht-degree: 6%

---

# Modo escuro para conteúdo de email {#dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode"
>title="Alternar para o modo escuro"
>abstract="Alterne para o modo escuro, que permite pré-visualizar a renderização e definir configurações personalizadas. <br>A renderização final depende do cliente de email do destinatário. Observe que todos os clientes de email não são compatíveis com o modo escuro personalizado."

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_preview"
>title="Alternar para o modo escuro"
>abstract="Alterne para o modo escuro para visualizar a renderização nos clientes de email compatíveis. <br>A renderização final depende do cliente de email do destinatário. Observe que todos os clientes de email não são compatíveis com o modo escuro."

_Modo escuro_ permite que um cliente ou aplicativo de email de suporte exiba emails com planos de fundo mais escuros e cores mais claras para texto, botões e outros elementos visuais. Esse tipo de monitor pode reduzir a tensão ocular, economizar bateria e melhorar a legibilidade em ambientes com pouca luminosidade, proporcionando uma experiência de visualização mais confortável. Como uma tendência crescente nos principais sistemas operacionais e aplicativos, agora é uma consideração importante no design de email moderno para garantir que o conteúdo permaneça legível e visualmente atraente para todos os usuários.

![Diagrama de conceito dos modos claro e escuro mostrando a renderização de conteúdo em temas claros e escuros](../assets/do-not-localize/light-dark-mode.svg){width="50%"}

À medida que você [cria seu conteúdo de email](./email-authoring.md) no espaço de design visual do [!DNL Journey Optimizer B2B Edition], é possível alternar para o modo de exibição _&#x200B;**[!UICONTROL Escuro]**&#x200B;_. Nesta visualização, também é possível definir configurações personalizadas específicas para oferecer suporte a clientes de email quando o modo escuro estiver ativado.

## Considerações do cliente de email

Há uma variação significativa na maneira como diferentes clientes de email e aplicativos aplicam o modo escuro. Por isso, você deve considerar as expectativas para a renderização no modo escuro com cuidado. Antes de usar o modo escuro no espaço de design de email, considere os seguintes casos de uso de cliente de email:
<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

+++Clientes que não oferecem suporte ao modo escuro

Alguns clientes de email não oferecem suporte a esse recurso, como:

* [!DNL Yahoo! Mail]
* [!DNL AOL]

Se você definir configurações personalizadas de modo escuro no design de email, esses clientes de email não poderão exibir nenhuma renderização de modo escuro. <!--Regardless of whether the interface is in light or dark mode, your email will render the same.-->

+++

+++Clientes aplicando seu próprio modo escuro {#default-support}

Alguns clientes de email aplicam sistematicamente seu próprio modo escuro padrão a todos os emails recebidos. Eles ajustam automaticamente cores, planos de fundo, imagens e outros elementos de acordo com suas configurações de modo escuro e configurações externas não são possíveis. Esses clientes incluem:

* Gmail (Webmail Para Desktop, iOS, Android™, Webmail Para Dispositivos Móveis)
* Outlook Windows
* Outlook Windows Mail

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->
Nesse caso, as configurações do modo escuro do cliente substituem as configurações personalizadas do modo escuro definidas no [!DNL Journey Optimizer B2B Edition]

+++

+++Clientes que oferecem suporte ao modo escuro personalizado

Muitos dos clientes de email mais populares oferecem a opção de renderizar o modo escuro personalizado com a consulta `@media (prefers-color-scheme: dark)`, que é o método usado pelos estilos de email [!DNL Journey Optimizer B2B Edition]. Esta lista de clientes inclui:

* Apple Mail macOS
* Apple Mail iOS
* Outlook macOS
* Outlook.com
* Outlook iOS
* Outlook Android™

Nesse caso, as configurações específicas definidas no [!DNL Journey Optimizer B2B Edition] são renderizadas. No entanto, algumas restrições podem se aplicar de acordo com cada cliente de email. Por exemplo, alguns clientes (como o Apple Mail 16 (macOS 13)) não geram o modo escuro se as imagens estiverem presentes no conteúdo de email.

Para obter os melhores resultados, teste seu conteúdo com os clientes de email que você está direcionando. Para ver uma simulação que se aproxime o máximo possível do resultado final de cada cliente, use a integração [renderização de teste de email Litmus](./email-test-rendering.md) no espaço de design de email.

+++

## Design para modo escuro

À medida que você estiliza o conteúdo de email para o modo escuro no [!DNL Journey Optimizer B2B Edition], o espaço de design visual fornece dois tipos de ferramentas:

* Use a [função de visualização](#preview-default-dark-mode) para revisar a renderização padrão do modo escuro para a maioria dos clientes de email de suporte.

* Se quiser substituir as configurações padrão de clientes de email de suporte, defina e aplique configurações personalizadas do modo escuro ao seu conteúdo de email. [Saiba mais](#define-custom-dark-mode)

### Visualizar modo escuro padrão {#preview-dark-mode}

<!-- Should work with templates and themes, NOT for LP and fragments - but TBC with eng. 
>[!NOTE]
>
>Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Abra o conteúdo do email no espaço de design de email.

   Na parte superior direita da tela de desenho, há um seletor de claro-escuro que alterna a exibição do conteúdo entre o modo claro (padrão) e escuro.

   ![Tela de design de email mostrando o seletor de modo de luz no canto superior direito](./assets/email-color-mode-light-selector.png){width="700" zoomable="yes"}

1. Altere o seletor para _Modo escuro_ ( ![Ícone de modo escuro](../assets/do-not-localize/icon-content-dark-mode.svg) ).

   A tela de desenho exibe o conteúdo usando o modo escuro padrão preview.x

   Por padrão, a visualização do modo escuro aplica o esquema de cores `full color invert` a todos os elementos, exceto imagens e ícones. Esse esquema de cores detecta áreas com elementos claros e escuros e os inverte. Os planos de fundo claros se tornam escuros e o texto escuro se torna claro, ou os planos de fundo escuros se tornam claros e o texto claro se torna escuro.

   ![Tela de design de email mostrando o seletor de modo escuro e o conteúdo de email exibidos no modo escuro](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>A renderização final pode variar de acordo com o cliente de email do recipient. Para ver uma simulação que se aproxime o máximo possível do resultado final para cada cliente de email, use a integração [Renderização de email de teste Litmus](./email-test-rendering.md).

### Definir configurações personalizadas do modo escuro {#custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_image"
>title="Usar uma imagem específica para o modo escuro"
>abstract="Você pode selecionar outra imagem para exibir quando o modo escuro estiver ativado. <br>A adição de uma imagem específica para o modo escuro não garante que ela seja renderizada corretamente em todos os clientes de email. Observe que todos os clientes de email não são compatíveis com o modo escuro personalizado."

Depois de alternar para o modo escuro, você pode optar por editar elementos de estilo específicos do seu conteúdo, que são exibidos somente quando o modo escuro está ativado no cliente de email do recipient (desde que seja compatível com esse recurso).

>[!NOTE]
>
>A renderização final no modo escuro depende de cada cliente de email, portanto, os resultados podem variar de um para o outro. Revise as [considerações sobre o cliente de email](#email-client-considerations) para obter mais informações.

O estilo de modo escuro personalizado no espaço de design de email usa o <!-- `@media (prefers-color-scheme: dark)` method--> Consulta CSS `@media (prefers-color-scheme: dark)`, que detecta se o cliente de email está definido para o modo escuro e aplica o design de tema escuro definido no seu email.

_Para definir configurações personalizadas do modo escuro :_

1. Se necessário, mova o seletor para _Modo escuro_ ( ![Ícone de modo escuro](../assets/do-not-localize/icon-content-dark-mode.svg) ) na parte superior direita da tela de design.

1. Edite quaisquer atributos de cor de estilo, como texto, planos de fundo ou botões.

   ![Painel de configurações de estilo de texto no modo escuro mostrando opções de cor e fonte](./assets/email-color-mode-dark-text-settings.png){width="700" zoomable="yes"}

1. Para as imagens e ícones, defina ativos específicos somente para o modo escuro.

   Não é possível alterar as cores das imagens e dos ícones, mas você pode definir ativos alternativos a serem usados no modo escuro. Você pode experimentar diferentes combinações de cores para seus ícones ou fazer ajustes de cores e saturação para imagens fotográficas.

   ![Ícones com combinações de cores diferentes](../assets/do-not-localize/color-contrast-images-diagram.svg){width="80%"}

   Selecione qualquer imagem e alterne para o **[!UICONTROL modo escuro]** usando a opção dedicada no painel **[!UICONTROL Configurações]**. Em seguida, selecione um ativo de imagem diferente.

   ![Configurações de imagem no modo escuro mostrando a opção de selecionar outro ativo de imagem para o modo escuro](./assets/email-color-mode-dark-image-settings.png){width="700" zoomable="yes"}

   Consulte [Adicionar ativos de imagem](./email-authoring.md#add-image-assets) para obter mais informações sobre como selecionar um ativo de imagem.

1. A qualquer momento durante as alterações de design, selecione **[!UICONTROL Alternar para o modo de exibição dinâmico]** para verificar como o conteúdo pode ser renderizado em vários tamanhos de dispositivo.

   Nesta exibição, altere o seletor para _Modo escuro_ ( ![Ícone de modo escuro](../assets/do-not-localize/icon-content-dark-mode.svg) ) para visualizar a versão de modo escuro do seu conteúdo em diferentes dispositivos.

   ![Painel de exibição em tempo real mostrando o conteúdo de email no modo escuro em diferentes tamanhos de dispositivo](./assets/email-color-mode-dark-live-view.png){width="800" zoomable="yes"}

   >[!CAUTION]
   >
   >A visualização em tempo real é uma visualização genérica criada para comparar a aparência da renderização em vários tamanhos de dispositivo. A renderização final pode variar dependendo do cliente de email do recipient.

1. Quando as alterações no modo escuro estiverem concluídas, clique em **[!UICONTROL Simular Conteúdo]**.

   ![Tela de design de email com o botão Simular Conteúdo realçado para teste no modo escuro](./assets/email-color-mode-dark-simulate-content.png){width="700" zoomable="yes"}

   Use os revisores e revisores de texto para testar o design do email. Consulte [Visualizar e testar seu conteúdo de email](./email-simulate-content.md) para obter mais informações.

1. Se você tiver uma conta do Litmus Enterprise, selecione **[!UICONTROL Renderizar email]** para ver a renderização final do modo escuro para vários clientes de email no Litmus.

   Consulte [Testar renderização de email com Litmus](./email-test-rendering.md) para obter mais informações.

   >[!CAUTION]
   >
   >Embora a simulação se aproxime da forma como os emails aparecem no modo escuro, a renderização real pode ser diferente devido a variações nos provedores de serviços de email ou nas configurações no nível do dispositivo.

## Práticas recomendadas {#best-practices}

À medida que a adoção do modo escuro aumenta nos principais clientes de email, é essencial considerar como seus emails são renderizados em ambientes claros e escuros, esteja você usando o [modo escuro personalizado](#define-custom-dark-mode) ou não.

O modo escuro pode alterar cores, planos de fundo e imagens — às vezes substituindo as opções de design. Para garantir a consistência visual, a acessibilidade e a integridade da marca, siga estas práticas recomendadas:

| Prática |            |
| -------- | ---------- |
| Otimize suas imagens e logotipos | Lista de verificação:<ul><li>Salve logotipos e ícones como arquivos PNG com fundo transparente para evitar caixas brancas visíveis no modo escuro. <li>Evite imagens com fundos brancos ou claros codificados. <li>Se a transparência não for uma opção, coloque as imagens em um plano de fundo sólido no design para evitar inversões de cores estranhas. |
| Veja seus planos de fundo | Lista de verificação:<ul><li>Verifique se há contraste suficiente entre o texto e as cores do plano de fundo para facilitar a leitura nos modos claro e escuro. <li>Evite depender apenas das cores do plano de fundo para o conteúdo crítico. Alguns clientes substituem as cores do plano de fundo no modo escuro, portanto, verifique se as informações principais ainda estão visíveis. |
| Criar conteúdo acessível no modo escuro | Lista de verificação:<ul><li>Use combinações de cores fáceis de distinguir para pessoas com daltonismo. <li>Use uma paleta de tons médios para garantir o contraste em planos de fundo claros e escuros. <li>Use combinações de cores acessíveis com alto contraste para melhorar a legibilidade e atender aos padrões do [!DNL Web Content Accessibility Guidelines (WCAG)]. Use ferramentas como o [!DNL WebAIM Contrast Checker] para verificar o contraste de cores. <li>Evite fontes finas, pois isso pode afetar a legibilidade. Se sua marca requer uma fonte fina, coloque-a em negrito no modo escuro. <li>Ignorar branco puro em preto puro, o que pode causar tensão ocular e pode ser invertido automaticamente em alguns clientes de email. <li>Fornecer estilo de fallback acessível se o modo escuro não for compatível. |
| Testar seus emails em um ambiente no modo escuro | Lista de verificação:<ul><li>Use a [visualização de modo escuro](#preview-dark-mode) no espaço de design de email, que usa esquemas de cores invertidas para detectar problemas antecipadamente. <li>Use uma conta Litmus Enterprise com a opção [[!UICONTROL Renderizar email]](./email-test-rendering.md) para simular seus designs nos principais clientes de email (como Apple Mail, Gmail e Outlook) e ver como as cores e as imagens se comportam no modo escuro. |

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->
