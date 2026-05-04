---
title: Testar renderização de email
description: Teste a renderização de email em clientes de desktop, móveis e da Web com a integração Litmus para garantir a compatibilidade da caixa de entrada no Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cad51180-f8ce-4cb7-aefc-437847b5d6d6
autotag-review: '2026-03-30T22:28:13.343Z'
source-git-commit: 8fe8318d7e1c63cbaa2749fc3928eb0a12967bd9
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 2%

---

# Testar renderização de email com o Litmus

Para testar seus emails, você pode usar uma conta corporativa do [Litmus](https://www.litmus.com/email-testing){target="_blank"} da Journey Optimizer B2B edition. Com essa integração, você pode pré-visualizar a renderização de email em clientes de email populares. Essa ferramenta ajuda a garantir que o conteúdo de email tenha uma ótima aparência e funcione conforme projetado em cada caixa de entrada.

>[!AVAILABILITY]
>
>Essa integração só está disponível para usuários do Journey Optimizer B2B edition com contas do Litmus Enterprise. Para obter mais informações, consulte a [página de soluções no site do Litmus](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Quando o design do email estiver concluído e pronto para ser testado, clique em **[!UICONTROL Simular conteúdo]** no espaço de design de email.

1. Clique em **[!UICONTROL Renderizar email]** na parte superior direita.

   ![Botão Renderizar email](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Se você ainda não tiver se conectado à sua conta Litmus a partir do Journey Optimizer B2B edition, a página exibida fornecerá uma opção para iniciar uma conta de avaliação ou conectar-se à conta existente.

1. Clique em **[!UICONTROL Conectar sua conta Litmus]** na parte superior direita ou use o link dentro da página.

   ![Conectar sua conta Litmus](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Insira suas credenciais de conta Litmus e clique em **[!UICONTROL Entrar]**.

1. Clique em **[!UICONTROL Conectar]** para confirmar a conexão entre o Litmus e o Journey Optimizer B2B edition e enviar o conteúdo do email para renderização.

   >[!IMPORTANT]
   >
   >Ao conectar sua conta do Litmus com o Journey Optimizer B2B edition, você concorda que as mensagens de teste são enviadas para o Litmus. Esse conteúdo é gerenciado no Litmus e não no Adobe. Como consequência, a política de retenção de dados por email Litmus se aplica a esses emails, incluindo dados de personalização que podem ser incluídos nas mensagens de teste.

1. Clique em **[!UICONTROL Executar teste]** na parte superior direita para gerar visualizações de email.

   ![Executar um teste de renderização Litmus](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Verifique seu conteúdo de email em clientes populares de desktop, móveis e baseados na Web.

   Clique na miniatura exibida para exibir os detalhes de qualquer um dos testes de cliente renderizados.

   ![Visualizações de email Litmus](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Quando terminar de revisar, clique na seta para trás ( ![ícone Mostrar ou ocultar filtros](../../assets/do-not-localize/icon_back-arrow.svg) ) na parte superior esquerda para retornar à página Simular conteúdo.

   Você pode selecionar outro perfil e fazer outro teste de renderização ou retornar ao espaço de design do email para fazer os ajustes necessários com base na sua revisão.
