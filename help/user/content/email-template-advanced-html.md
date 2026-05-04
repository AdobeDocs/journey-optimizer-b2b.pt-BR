---
title: Modo HTML avançado para design de modelo de email
description: Use o modo HTML avançado para visualizar e editar diretamente a fonte de HTML bruta do seu conteúdo de modelo de email no espaço de design de email no Journey Optimizer B2B edition.
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
exl-id: 92af078b-29b4-4507-ae43-55dc4dd4b748
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: adfaa694-5e52-4b2d-8c6b-20a18ae4b51b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 0216cf3b1cbc1124b50ad99e649778aef71f5aca
workflow-type: tm+mt
source-wordcount: 583
ht-degree: 0%

---

# Modo HTML avançado para design de modelo de email

O _modo HTML avançado_ fornece um modo de exibição que permite aos usuários experientes visualizar e editar diretamente o código fonte bruto para o conteúdo do modelo de email. Esse modo é ideal quando você deseja inserir expressões sofisticadas, como lógica condicional, diretamente na origem. Também é útil para fazer ajustes estruturais que vão além do que as ferramentas de design visual expõem.

<!-- 
We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. 
-->

>[!AVAILABILITY]
>
>Este recurso está atualmente em _Disponibilidade Limitada_ e não está disponível para todos os usuários.

## Limitações importantes

Antes de usar o modo avançado do HTML para [criação de modelo de email](./email-template-authoring.md), verifique se você compreende as seguintes limitações:

* **Sem validação** — O editor do HTML não executa verificação de sintaxe ou de layout. Revise seu código cuidadosamente antes de salvar.

* **Atualizações de conteúdo** — futuras alterações do sistema podem afetar ou substituir modificações feitas na marcação padrão no modo HTML avançado. Verifique o conteúdo após as atualizações de produto para garantir que ele seja renderizado conforme esperado.

* **Suporte limitado** — a Adobe não pode solucionar problemas de renderização ou erros de conteúdo resultantes de modificações de código personalizadas feitas no modo HTML avançado.

* **Restrições de visualização** — A simulação de conteúdo (visualização com perfis) só está disponível no modo de exibição de desktop, não diretamente no modo de exibição de origem do HTML.

### Acessar o modo HTML avançado

O modo HTML avançado pode ser acessado na barra de ferramentas, na parte superior do espaço de design visual, quando você tiver um modelo de email carregado na tela.

1. Abra ou [crie um modelo de email](./email-templates.md#create-an-email-template) e abra o espaço de design para editar o conteúdo.

1. No espaço de design, clique no ícone do _[!UICONTROL HTML]_ ( ![HTML](../assets/do-not-localize/icon-code.svg) ) na barra de ferramentas.

   ![Clique no ícone HTML na barra de ferramentas do espaço de design do modelo de email](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   Se esta for a primeira vez que você abre o modo avançado do HTML (ou se um mês ou mais tiver decorrido), uma mensagem de aviso será exibida. Revise as informações e clique em **[!UICONTROL OK]** para continuar.

   ![Revise o aviso do modo HTML Avançado e clique em OK para continuar](./assets/email-template-html-mode-warning.png){width="500"}

   A tela de design alterna para a exibição de origem bruta do HTML.

1. Revise o código e adicione as alterações desejadas ao conteúdo do email.

   No _modo HTML Avançado_, você tem acesso direto à fonte completa do HTML do conteúdo do seu modelo de email:

   * Visualize e modifique qualquer parte da marcação bruta do HTML.
   * Insira [expressões de personalização](./personalization.md) avançadas diretamente na origem.
   * Adicionar a lógica do [conteúdo condicional](./conditional-content.md) usando a sintaxe de expressão.
   * Adicione atributos personalizados do HTML, tags de rastreamento ou outra marcação que não esteja disponível por meio dos controles do editor visual.

   ![Modo HTML avançado com fonte de HTML bruta do conteúdo de email](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >Insira o código HTML e CSS correto; a Adobe não fornece validação de sintaxe ou suporte para código personalizado.

   A simulação e o salvamento de conteúdo não estão disponíveis no modo avançado do HTML por motivos de compatibilidade. Você pode voltar para a visualização da área de trabalho para visualizar seu conteúdo e salvar o modelo. As edições feitas são preservadas ao alternar entre a exibição de origem do HTML e a exibição de design visual.

   Se você clicar em **[!UICONTROL Salvar]** ou **[!UICONTROL Salvar e fechar]** na parte superior direita enquanto estiver no modo HTML avançado, uma caixa de diálogo de alerta será exibida para informá-lo de que você deve sair do modo HTML avançado antes de salvar o modelo e sair do espaço de design.

   ![A caixa de diálogo de alerta que foi salva está desabilitada no modo HTML avançado](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. Clique no ícone da _[!UICONTROL Área de Trabalho]_ ( ![Área de Trabalho](../assets/do-not-localize/icon-desktop-spectrum-1.svg) ) na barra de ferramentas para alternar do modo HTML avançado (o modo de exibição de origem do HTML) para a tela de design visual.

   As edições são preservadas ao alternar entre exibições.
