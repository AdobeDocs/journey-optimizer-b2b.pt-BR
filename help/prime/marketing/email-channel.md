---
title: Canal de email
description: Adicionar nós de ação de email às jornadas de conta - crie novos emails ou use emails existentes do Marketo Engage para comunicações direcionadas no Journey Optimizer B2B edition.
feature: Email Authoring, Account Journeys
role: User
autotag-review: '2026-06-18T20:30:25.418Z'
TQID: 'https://experienceleague.adobe.com/K3OZnLvtSdwSq6AT4JlRQ62t32d6smIJ4K9EEnK-QUc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 2%

---

# Canal de email

O [!DNL Adobe Journey Optimizer B2B Prime] traz uma experiência moderna de criação e entrega de email de nível empresarial para os profissionais de marketing B2B. Esta versão apresenta ferramentas de design de email reprojetadas e um conjunto completo de controles de capacidade de entrega de email.

>[!NOTE]
>
>Se você estiver enviando um email pela primeira vez, verifique se o [canal de email e a capacidade de entrega](../admin/configuration-email-deliverability.md) estão configurados.

## Visão geral do canal de email {#overview}

* **Configurações de canal de email** - Gerencie a identidade do remetente, o comportamento de resposta, os tipos de mensagem de marketing vs. transacional e o rastreamento.
* **Controles de capacidade de entrega de email** - Configure seu canal de capacidade de entrega de email, incluindo delegação de subdomínio (métodos totalmente delegados e CNAME), DMARC, configuração automática SPF/DKIM e suporte a pool de IP compartilhado.
* **Ação Enviar email** - De uma jornada, adicione um nó de ação _Enviar email_, incluindo a personalização usando atributos de perfil (sintaxe Handlebars).
* **Ferramentas visuais de design de email de arrastar e soltar** - Projete o conteúdo de email com estruturas, componentes de conteúdo, temas, suporte para o modo escuro e fragmentos visuais reutilizáveis.
* **Ativos do Marketo Design Studio** — escolha imagens e ativos de uma cópia única da biblioteca de ativos do Marketo Engage diretamente na tela de email.
* **Modelos e fragmentos reutilizáveis** — Salve cabeçalhos, rodapés, CTAs e layouts completos de email comuns e reutilize-os no jornada.
* **Controle de Acesso com Base em Função (RBAC)** — Aplique permissões granulares para criar, editar, aprovar e enviar email.

## Principais conceitos {#key-concepts}

Antes de criar emails para jornadas de pessoas e criar conteúdo de email, analise estes conceitos:

| Conceito | No Prime [!DNL Journey Optimizer B2B Prime] |
| ------- | ---------------------- |
| **_Espaço de design de email_** | A tela visual e as ferramentas de design usadas para compor conteúdo de email. Ele inclui componentes de layout de arrastar e soltar, templates, fragmentos, temas e um editor de personalização. |
| **_Modelo_** | Um layout de email reutilizável que está disponível para criar um novo email. Ele pode ser um modelo integrado fornecido pelo Adobe ou um modelo personalizado criado pela sua equipe. |
| **_Fragmento visual_** | Um bloco reutilizável de conteúdo (como cabeçalho, rodapé, CTA, aviso de isenção legal) que pode ser inserido em vários emails. A atualização de um fragmento propaga a alteração para cada email que o utiliza. |
| **_Tema_** | Uma predefinição de estilo reutilizável (cores, tipografia, espaçamento, estilos de botão) aplicada em um email. |
| **_token do Personalization_** | Uma expressão Handlebars — por exemplo, `{{profile.firstName}}` — resolvida no momento do envio usando os dados de perfil de cada recipient. |
| **_Ação Enviar email_** | O nó de ação de jornada que usa uma configuração de canal e conteúdo de email para entregar um email. |

## Adicionar um email de uma jornada

Para enviar email de uma jornada, adicione um nó _Faça uma ação_ e configure-o para enviar email.

1. Na tela de jornada, clique no ícone **+** e selecione **[!UICONTROL Realizar uma ação]**.

1. Nas propriedades do nó à direita, defina a ação como **[!UICONTROL Enviar email]**.

   ![Executar uma ação - Enviar email](./assets/person-action-node-send-email.png){width="450"}

1. Escolha a fonte do e-mail:

   * **Criar/editar email** - Escolha esta opção para definir o conteúdo do email, incluindo a linha de assunto, as informações do remetente e o corpo do email no espaço de design do email.

   * **[!UICONTROL Usar um email personalizado para IA]** - Escolha esta opção para refinar um email gerado para IA no espaço de design de email. Esses emails são otimizados para que os clientes da caixa de entrada assistida por IA fundamentem seus resumos e respostas em suas ofertas e planos de ação.

1. Clique em **[!UICONTROL Criar email]**.

1. Na caixa de diálogo _[!UICONTROL Criar email]_, digite um **[!UICONTROL Nome]** exclusivo (obrigatório) e uma **[!UICONTROL Descrição]** (opcional).

1. Clique em **[!UICONTROL Criar]**.

## Definir as propriedades e ações do email

1. Com o nó _[!UICONTROL Enviar email]_ selecionado na tela de jornada, clique em **[!UICONTROL Editar email]** nas propriedades do nó à direita.

<!-- Staging environment broken -->

para o email e uma **[!UICONTROL linha de assunto]**.

Isso abre a guia **[!UICONTROL Ações]**, na qual você pode selecionar ou criar a configuração de email a ser usada.

1. (Opcional) Selecione um conjunto de regras nas Regras de negócio para aplicar regras de limitação à sua ação de email.

Você pode usar a [opção de otimização de tempo de envio](./email-send-time-optimization.md) para prever o melhor momento para enviar a mensagem e maximizar o engajamento com base no histórico de taxas de abertura e de clique. Saiba como

Selecione o botão Editar conteúdo e crie seu conteúdo conforme desejado usando o Designer de email.

Volte para a tela de jornada. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais.

Para obter mais informações sobre como criar, configurar e publicar uma jornada, consulte esta página.


### Definir configurações de email {#email-settings}

Defina as configurações na guia **[!UICONTROL Detalhes]** do painel de resumo do nó.

| Configuração | Descrição |
| ------- | ----------- |
| **[!UICONTROL De nome]** | Nome do remetente exibido no cabeçalho do email. Suporta tokens de personalização. |
| **[!UICONTROL Do email]** | Endereço de email do remetente. Padrões da configuração do canal. Aceita personalização. |
| **[!UICONTROL Endereço para resposta]** | Endereço que recebe respostas dos destinatários. Aceita personalização. |
| **[!UICONTROL Linha de assunto]** | Linha de assunto do email. Editável a partir do valor inserido na criação. |
| **[!UICONTROL Domínio de marca]** | Domínio usado para envio específico da marca. |
| **[!UICONTROL IP dedicado]** | Endereço IP específico para rastreamento da capacidade de entrega. |
| **[!UICONTROL Email operacional]** | Quando ativado, ignora a supressão de recusa e cancelamento de inscrição. Use apenas para mensagens operacionais legítimas. |
| **[!UICONTROL Incluir exibição como página da Web]** | Gera um link de página da Web para o conteúdo de email. |
| **[!UICONTROL Desabilitar o rastreamento de aberturas]** | Impede o rastreamento da atividade de email aberta. |
| **[!UICONTROL Pré-cabeçalho]** | Texto resumido exibido após a linha de assunto nas visualizações da caixa de entrada. |
| **[!UICONTROL Endereços CC]** | Adicione até 25 campos de email de cliente potencial ou Empresa para receber uma cópia. |

### Verificar alertas {#alerts}

[!DNL Journey Optimizer B2B Prime] apresenta problemas no canto superior direito do editor de email. Resolva todos os erros antes de ativar a jornada — os avisos são somente recomendações.

**Erros** (impedir ativação de jornada):

* O nome do remetente está vazio
* Linha de assunto ausente
* O conteúdo do email está vazio

**Avisos** (recomendações):

* O link para opção de não participação não está presente no corpo do email
* A versão de texto do HTML está vazia
* Links vazios detectados
* Email excede 100 K
