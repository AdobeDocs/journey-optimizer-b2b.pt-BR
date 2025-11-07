---
title: Qualificador de Vendas
description: Saiba como usar o aplicativo Qualificador de vendas para acelerar e manter suas jornadas.
feature: Account Journeys, AI Assistant
role: User
source-git-commit: 8fb86fe3434a5acdec6fd638fad571a0bc901884
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 1%

---


# Qualificador de Vendas

>[!NOTE]
>Este recurso está atualmente com a Disponibilidade Limitada e não está disponível para todos os usuários.
>

O qualificador de vendas é um aplicativo complementar orientado por IA para o Adobe Journey Optimizer B2B edition que contém o Account Qualification Agent e foi projetado para simplificar os fluxos de trabalho dos BDRs (Business Development Representatives, representantes de desenvolvimento de negócios). O qualificador de vendas automatiza os fluxos de trabalho de qualificação de prospecto, alcance externo e envolvimento do comprador em todos os canais, reduzindo a carga manual de BDR e acelerando a velocidade do pipeline para empresas B2B corporativas.
Use os plug-ins do navegador e do email para acessar a business intelligence diretamente nos CRMs ou no Outlook.

O qualificador de vendas está incluído no AJO B2B, mas é um aplicativo separado no AEP Experience Cloud.

![Página inicial do Qualificador de Vendas](assets/home-screen.png)

## Account Qualification Agent

O Account Qualification Agent (AQA) é o coração do qualificador de vendas. O AQA usa IA para ler suas contas e determinar quais estão prontas para a próxima etapa.  Ele auxilia na pesquisa, elaboração de email e atualizações de CRM.

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

* Mostrar meus clientes em potencial atribuídos ainda sem envolvimento
* Mostre-me todos os clientes em potencial que não fazem parte de nenhum envolvimento autônomo
* Forneça-me um resumo detalhado sobre `<company>`, incluindo seu grupo de compras, sinais recentes de intenção e nosso compromisso anterior.

É possível entender imediatamente quais contas e leads são mais ativos e mostrar a maior intenção, para que você possa concentrar sua energia onde ela tem mais impacto.

Repita sua jornada refinando seus prompts para obter os resultados necessários. Por exemplo:

* Rascunhar um email de acompanhamento do contexto, como chamadas de ganhos ou relatórios. Até 120 palavras. Linha de assunto: cativante, incorporando um tema chave. Introdução: gancho com uma cotação direta de fontes de contexto. Corpo: conecte-se aos pontos problemáticos e às propostas de valor. CTA: proponha uma breve chamada para explorar mais detalhadamente.

* O objetivo deste email é iniciar uma conversa e criar credibilidade. Esboçar um e-mail com menos de 120 palavras que tenha um tom consultivo e empático. Evite uma abordagem de vendas muito familiar e não use as expressões &quot;espere que esteja bem&quot;, &quot;apenas conferindo&quot; ou &quot;por favor&quot;.

## Clientes potenciais

Essa janela lista todos os leads aos quais você tem acesso. É rápido verificar itens como Status do lead e Última atividade.

![Ver todos os seus clientes em potencial na tabela de Clientes potenciais](assets/prospects.png)

Clique no ícone Filtrar ![ícone Filtrar](../assets/icon-filter.png) para filtrar por status de cliente potencial.

## Planos de engajamento

Essa janela fornece detalhes sobre quaisquer planos de Engajamento definidos.

![Planos de participação](assets/engagement-plans.png)

Para criar um novo plano de Envolvimento, clique em **[!UICONTROL Criar plano de envolvimento]**.

1. No estágio Detalhes, forneça um nome e uma descrição opcional. Clique em **[!UICONTROL Salvar e continuar]**.
1. No estágio Selecionar prospetos, selecione os clientes potenciais que devem pertencer a esse plano.
1. No estágio Definir cadência, defina os parâmetros do plano.
1. No estágio de Pré-visualização, verifique se tudo está funcionando como esperado.

## Caixa de saída de email

O painel Caixa de saída de email lista todos os emails automatizados enviados.

## Reservas da reunião

Esse painel exibe todas as reuniões configuradas por meio da automação.

## Caixa de entrada do chat

Este painel exibe todas as suas threads de bate-papo.

![Caixa de entrada do chat](assets/chat-inbox.png)

Você não só pode interagir com os clientes, como também pode ver um resumo do contato e um resumo do segmento, para que possa saber rapidamente onde está no segmento.

## Integrações

Com as integrações, o Qualificador de vendas pode aproveitar os CRMs e outras fontes de dados para enriquecer os perfis dos clientes e aproveitar as atividades de vendas:

* Integre o à sua caixa de entrada de emails para acompanhar emails recebidos relevantes e ajudar a gerar respostas.
* Leia e atualize dados do CRM, como Salesforce ou Microsoft® Dynamics, ZoomInfo ou Buildwidth.

![Integração do Outlook com o Qualificador de Vendas](assets/outlook.png)

### Configurar uma nova integração

Para iniciar uma nova integração, clique em **[!UICONTROL Criar integração]** na parte superior direita.

![Detalhes da integração](assets/integration-details.png)

Aqui definimos o URL da integração e estabelecemos a carga útil a ser enviada.

1. Forneça um nome exclusivo e uma descrição (opcional) para a integração.
1. Defina o campo URL para o endpoint de autenticação de integração do site de integração.
1. Em Parâmetros de Caminho, defina o método HTTP.
1. Em Parâmetros de cabeçalho, defina os cabeçalhos HTTP que precisam ser enviados. Geralmente, um objeto JSON que é enviado e requer um cabeçalho de tipo de conteúdo.
1. Em Parâmetros de consulta, estabeleça os parâmetros necessários.
1. Em Autenticação, configure as informações de logon para o site de integração.

   * None
   * OAuth 2.0
   * Chave de API
   * Autenticação básica

1. Defina os valores de limitação e cache na seção Configuração de carga.
1. Em Configuração de carga, clique no ícone de lápis. Na caixa de diálogo Colar carga, cole ou insira seu objeto de carga JSON.
   * Carga da solicitação : um objeto JSON que contém dados para enviar o site de integração.
   * Carga de resposta: a estrutura de dados que você espera obter em retorno.
1. Clique em [!UICONTROL Testar Conexão] para verificar se suas configurações estão corretas.

Quando as configurações de conexão forem válidas, clique em **[!UICONTROL Salvar como rascunho]**.

Quando voltar à tabela principal de Integrações, selecione a integração e clique em **[!UICONTROL Ativar]** para ativar a integração ou em **[!UICONTROL Salvar como rascunho]**.



#### Gerenciar acesso

É possível gerenciar o acesso a usuários e que tipo de dados é compartilhado com diferentes grupos de usuários.

Clique em **[!UICONTROL Gerenciar acesso]** para abrir a caixa de diálogo Gerenciar Acesso.

Essa caixa de diálogo lista todos os rótulos que foram estabelecidos pela sua organização. Selecione os rótulos que deseja aplicar a essa integração.

Se precisar de um novo rótulo, clique em **[!UICONTROL Criar rótulo]** e preencha:

* Nome
* Nome amigável
* Descrição

## Configurações de representante

É aqui que você insere informações sobre você: detalhes pessoais, configurações de email e calendário e disponibilidade de chat.

### Detalhes

A guia Detalhes é onde você insere informações sobre você mesmo:

![Configurações de Detalhes do Qualificador de Vendas](assets/details.png)

### Configurações de email

Na guia Configurações de email, configure suas conexões de email.

![Configurações de email](assets/email-settings.png)

#### Conexões de email

Clique em **[!UICONTROL Conectar]** e siga o procedimento de logon do Microsoft.

#### Assinatura de email

Configurar a assinatura de email usada em emails gerados automaticamente.

### Configurações do calendário

Na guia Configurações do calendário, defina o fuso horário e a disponibilidade.

![Configurações do calendário](assets/calendar-settings.png)

#### Conexão de calendário

Clique em **[!UICONTROL Conectar]** e siga o procedimento de logon do Microsoft para integrar seu calendário.

#### Email de confirmação da reunião

Quando um cliente confirma uma reunião com você, ele recebe o email de confirmação como uma resposta.
Use essas configurações para definir o assunto e o corpo do email.

#### Preferências

Defina a duração da reunião padrão e o tempo desejado entre as reuniões consecutivas.

### Configurações de chat

Nesta guia, defina a disponibilidade de chat do Timezone Live.

![Configurações de chat](assets/chat-settings.png)

## Gerenciamento de representantes

Nesse painel, uma tabela é mostrada de todos os representantes definidos e seu status do calendário.

## Desempenho da reunião

Este painel apresenta análises sobre as reuniões concluídas.

## Configuração do plug-in do Chrome

O plug-in do Assistente de IA para Chrome está disponível na [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Quando o plug-in é instalado no Chrome, o logotipo do Adobe aparece no meio à direita quando você está em um site integrado:

* aplicativos web do Adobe
* Salesforce
* Outlook
* Microsoft Dynamics e aplicativos web
* aplicativos Google

## Editar barra de navegação esquerda

Na parte inferior esquerda do aplicativo, clique em **[!UICONTROL Editar]** para controlar quais dos ícones estão visíveis na navegação. Você também pode arrastá-los e soltá-los para reordenar como desejar.

## Vídeo de demonstração

O vídeo a seguir fornece uma breve demonstração do qualificador de vendas e do Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476566?captions=por_br)
