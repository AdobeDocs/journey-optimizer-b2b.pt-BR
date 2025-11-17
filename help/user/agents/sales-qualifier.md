---
title: Qualificador de Vendas
description: Automatize a qualificação de prospecto B2B e o alcance com o Qualificador de vendas. Ele fornece pesquisa alimentada por IA, elaboração de email, integração de CRM e planos de engajamento para BDRs.
feature: AI Assistant, Sales Insights, Account Journeys
role: User
source-git-commit: dc6495a65b89cb3993c4b72706298181a3b555db
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 1%

---


# Qualificador de Vendas

>[!NOTE]
>Este recurso está atualmente com a Disponibilidade Limitada e não está disponível para todos os usuários.
>

O Sales Qualifier é um aplicativo complementar orientado por IA para o Adobe Journey Optimizer B2B edition que contém o Account Qualification Agent e foi projetado para simplificar os fluxos de trabalho para BDRs (Business Development Representatives, representantes de desenvolvimento de negócios). O Sales Qualifier automatiza os fluxos de trabalho de qualificação de prospecto, alcance externo e envolvimento do comprador entre canais. Ele reduz a carga manual de BDR e acelera a velocidade do pipeline para empresas B2B corporativas.
Use os plug-ins do navegador e do email para acessar a business intelligence diretamente nos CRMs ou no Outlook.

O qualificador de vendas está incluído no Journey Optimizer B2B edition, mas é um aplicativo separado dentro da Experience Platform Experience Cloud.

![Página inicial do Qualificador de Vendas](assets/home-screen.png)

## Account Qualification Agent

O Account Qualification Agent (AQA) é o coração do qualificador de vendas. O AQA usa IA para ler suas contas e determinar quais estão prontas para a próxima etapa. Ele auxilia na pesquisa, elaboração de email e atualizações de CRM.

![Account Qualification Agent](assets/acc-qualification-agent.png)

* **Pesquisa de cliente potencial**

  Realize pesquisas de clientes potenciais usando a recuperação automática e a exibição de informações importantes de clientes potenciais (como cargo, contratos recentes, associação a grupos de compras) para fornecer uma visão completa em segundos.

* **Pesquisa de conta**

  Realizar pesquisas de conta usando recuperação automática e exibição de informações detalhadas sobre a empresa de um cliente potencial. Essas informações incluem sinais vitais da empresa, notícias recentes, prioridades estratégicas e os principais membros envolvidos.

* **Emails de rascunho**

  Gerar rascunhos de email sintetizando a pesquisa de prospecto e insights de conta para produzir conteúdo de email único relevante e personalizado com base no objetivo do BDR.

* **Emails do plano de engajamento**

  Criar rascunhos de email do plano de engajamento personalizados para cada etapa de uma cadência de alcance definido pelo BDR, garantindo que toda a sequência seja personalizada

### Uso básico

Os agentes da IA do Adobe usam _consultas de linguagem natural_, o que significa que eles usam o mesmo idioma no prompt de texto que você usaria ao falar com uma pessoa. Quanto mais detalhado você for, melhores serão os resultados.

Usando a linguagem natural, você pode solicitar que o agente:

* `Show me my assigned leads with no engagement yet`
* `Show me all my leads that are not part of any autonomous engagement`
* `Give me a detailed summary on Acme company, including their buying group, recent intent signals, and our past engagement.`

Você pode entender imediatamente quais contas e leads são os mais ativos e mostrar a maior intenção, para que possa concentrar sua energia onde ela tem mais impacto.

Repita sua jornada refinando seus prompts para obter os resultados necessários. Por exemplo:

* Rascunhar um email de acompanhamento do contexto, como chamadas de ganhos ou relatórios. Até 120 palavras. Linha de assunto: cativante, incorporando um tema chave. Introdução: gancho com uma cotação direta de fontes de contexto. Corpo: conecte-se aos pontos problemáticos e às propostas de valor. CTA: proponha uma breve chamada para explorar mais detalhadamente.

* O objetivo deste email é iniciar uma conversa e criar credibilidade. Esboçar um e-mail com menos de 120 palavras que tenha um tom consultivo e empático. Evite uma abordagem de vendas muito familiar e não use as expressões &quot;espere que esteja bem&quot;, &quot;apenas conferindo&quot; ou &quot;por favor&quot;.

## Clientes potenciais

Essa janela lista todos os leads aos quais você tem acesso. É uma verificação rápida em itens, como status de lead e última atividade.

![Ver todos os seus clientes em potencial na tabela de Clientes potenciais](assets/prospects.png)

Clique no ícone _Filtro_ ![Filtro](../../assets/do-not-localize/icon_filter-outline.svg) para filtrar a lista exibida por status de cliente potencial.

## Planos de engajamento

Essa janela fornece detalhes sobre quaisquer planos de Engajamento definidos.

![Planos de participação](assets/engagement-plans.png)

Para criar um novo plano de Envolvimento, clique em **[!UICONTROL Criar plano de envolvimento]**.

1. No estágio _Detalhes_, forneça um nome e uma descrição opcional. Clique em **[!UICONTROL Salvar e continuar]**.
1. No estágio _Selecionar prospetos_, selecione os clientes potenciais que devem pertencer a este plano.
1. No estágio _Definir cadência_, defina os parâmetros do plano.
1. No estágio _Visualizar_, verifique se tudo está funcionando como esperado.

## Caixa de saída de email

O painel Caixa de saída de email lista todos os emails automatizados enviados.

## Reservas da reunião

Esse painel exibe todas as reuniões configuradas por meio da automação.

## Caixa de entrada do chat

Este painel exibe todas as suas threads de bate-papo.

![Caixa de entrada do chat](assets/chat-inbox.png)

Você pode interagir com clientes e ver resumos do contato e da thread, para que possa saber rapidamente onde está na thread.

## Integrações

Com as integrações, o Qualificador de vendas pode aproveitar os CRMs e outras fontes de dados para enriquecer os perfis dos clientes e aproveitar as atividades de vendas:

* Integre o à sua caixa de entrada de emails para acompanhar emails recebidos relevantes e ajudar a gerar respostas.
* Leia e atualize dados do CRM, como Salesforce ou Microsoft® Dynamics, ZoomInfo ou Buildwidth.

![Integração do Outlook com o Qualificador de Vendas](assets/outlook.png)

### Configurar uma nova integração

Para iniciar uma nova integração, clique em **[!UICONTROL Criar integração]** na parte superior direita.

![Detalhes da integração](assets/integration-details.png)

Defina o URL da integração e estabeleça a carga útil a ser enviada:

1. Forneça um nome exclusivo e uma descrição (opcional) para a integração.
1. Defina o campo URL para o endpoint de autenticação de integração do site de integração.
1. Em Parâmetros de Caminho, defina o método HTTP.
1. Em Parâmetros de cabeçalho, defina os cabeçalhos HTTP que precisam ser enviados. Geralmente, é um objeto JSON enviado e requer um cabeçalho de tipo de conteúdo.
1. Em Parâmetros de consulta, estabeleça os parâmetros necessários.
1. Em Autenticação, configure as informações de logon para o site de integração.

   * None
   * OAuth 2.0
   * Chave de API
   * Autenticação básica

1. Defina os valores de limitação e cache na seção **[!UICONTROL Configuração de carga]**.
   * Clique no ícone de lápis.
   * Na caixa de diálogo _Colar carga_, cole ou insira seu objeto de carga JSON.

      * **[!UICONTROL Solicitar carga]** - Um objeto JSON que contém dados para enviar ao site de integração.
      * **[!UICONTROL Carga de resposta]** - A estrutura de dados que você espera retornar.

1. Clique em **[!UICONTROL Testar Conexão]** para verificar se suas configurações estão corretas.

Quando as configurações de conexão forem válidas, clique em **[!UICONTROL Salvar como rascunho]**.

Quando você voltar à tabela principal de _[!UICONTROL Integrações]_, selecione a integração e clique em **[!UICONTROL Ativar]** para ativar a integração. Se você não estiver pronto para ativá-lo, clique em **[!UICONTROL Salvar como rascunho]**.

#### Gerenciar acesso

Você pode gerenciar o acesso aos usuários e o tipo de dados que são compartilhados com diferentes grupos de usuários.

Clique em **[!UICONTROL Gerenciar acesso]** para abrir a caixa de diálogo _[!UICONTROL Gerenciar Acesso]_.

Essa caixa de diálogo lista todos os rótulos estabelecidos para sua organização. Selecione os rótulos que deseja aplicar a essa integração.

Se precisar de um novo rótulo, clique em **[!UICONTROL Criar rótulo]** e insira as informações do rótulo:

* Nome
* Nome amigável
* Descrição

## Configurações de representante

As configurações de representante especificam informações sobre você, incluindo detalhes pessoais, configurações de email e calendário e disponibilidade de bate-papo.

### Detalhes

A guia **[!UICONTROL Detalhes]** é onde você insere informações sobre si mesmo:

![Configurações de Detalhes do Qualificador de Vendas](assets/details.png)

### Configurações de email

Na guia **[!UICONTROL Configurações de email]**, configure suas conexões de email.

![Configurações de email](assets/email-settings.png)

* **[!UICONTROL Conexões de email]** - Clique em **[!UICONTROL Conectar]** e siga o procedimento de logon do Microsoft.

* **[!UICONTROL Assinatura de email]** - Configure a assinatura de email usada em emails gerados automaticamente.

### Configurações do calendário

Na guia **[!UICONTROL Configurações do calendário]**, defina o fuso horário e a disponibilidade.

![Configurações do calendário](assets/calendar-settings.png)

* **[!UICONTROL Conexão do calendário]** - Clique em **[!UICONTROL Conectar]** e siga o procedimento de logon do Microsoft para integrar seu calendário.

* **[!UICONTROL Email de confirmação da reunião]** - Quando um cliente confirma uma reunião com você, ele recebe o email de confirmação como resposta. Use essas configurações para definir o assunto e o corpo do email.

* **[!UICONTROL Preferências]** - Defina a duração da reunião padrão e o tempo que você deseja entre reuniões consecutivas.

### Configurações de chat

Na guia **[!UICONTROL Configurações de chat]**, defina a disponibilidade de chat do Fuso Horário em Tempo Real.

![Configurações de chat](assets/chat-settings.png)

## Gerenciamento de representantes

O painel _[!UICONTROL Gerenciamento de representantes]_ exibe os representantes definidos e seu status de calendário.

## Desempenho da reunião

Este painel apresenta análises sobre as reuniões concluídas.

## Configurar o plug-in do Chrome

O plug-in do Assistente de IA para Chrome está disponível na [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Quando o plug-in é instalado no Chrome, o logotipo do Adobe aparece no meio à direita quando você está em um site integrado:

* aplicativos web do Adobe
* Salesforce
* Outlook
* Microsoft Dynamics e aplicativos web
* aplicativos Google

## Editar a barra de navegação esquerda

Na parte inferior esquerda do aplicativo, clique em **[!UICONTROL Editar]** para controlar quais dos ícones estão visíveis na navegação. Você também pode arrastá-los e soltá-los para reordenar como desejar.

## Vídeo de demonstração

O vídeo a seguir fornece uma breve demonstração do qualificador de vendas e do Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476566?captions=por_br)
