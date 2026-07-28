---
title: Construtor de script
description: Use o Construtor de scripts, um assistente habilitado por IA no espaço de design de email, para gerar scripts de personalização Handlebars e converter scripts do Marketo Engage Velocity no Journey Optimizer B2B edition.
feature: AI Assistant, Generative AI, Personalization, Email Authoring
role: User, Developer
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
autotag-review: '2026-07-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0004f8fba0c3d4ae89063418e4d3ef8fea22b0c3
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 2%

---

# Construtor de script

O _Construtor de Scripts_ é um assistente habilitado para IA disponível no espaço de design de email [!DNL Adobe Journey Optimizer B2B Edition]. Isso ajuda os profissionais de marketing e desenvolvedores de email a criarem scripts de personalização com mais rapidez e ajuda na migração do [!DNL Marketo Engage], convertendo a lógica de personalização existente no [!DNL Journey Optimizer B2B Edition] sem reescrever o código manualmente.

>[!AVAILABILITY]
>
>O Construtor de scripts está disponível atualmente para selecionar clientes como uma versão beta limitada para emails somente em **_jornadas de conta_**. O suporte a jornadas pessoais está planejado para uma versão futura. Para obter acesso, entre em contato com o representante da Adobe.

A criação de personalização condicional de email, como alternância de blocos de idioma por localidade, troca de conteúdo por região ou persona ou inserção de valores de perfil dinâmico ou objeto personalizado, requer a criação de _Handlebars_. Se você migrar de [!DNL Marketo Engage], terá o desafio adicional de reescrever scripts _Velocity_ linha por linha. O Construtor de scripts aborda os dois obstáculos de uma única interface conversacional:

* Gere um novo script de personalização Handlebars a partir de uma descrição em linguagem simples.
* Cole um script do Velocity [!DNL Marketo Engage] e converta-o em um script do Handlebars equivalente com mapeamento automático de tokens.
* Pré-visualizar, editar, validar e salvar a saída diretamente no email, sem copiar e colar entre as ferramentas.

## Diretrizes e limitações

>[!IMPORTANT]
>
>O acesso do usuário ao Construtor de Scripts é controlado através das mesmas permissões usadas para outros recursos de IA gerativa no [!DNL Journey Optimizer B2B Edition]. Para obter informações sobre como conceder permissões de recursos, consulte [Habilitar acesso ao Assistente de IA](../ai-assistant/enable-ai-assistant-access.md).

Antes de usar o Construtor de Scripts, reveja as [diretrizes e limitações](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations) que se aplicam aos recursos de IA gerativa em [!DNL Journey Optimizer B2B Edition]. A aceitação do [Contrato de usuário](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} também é necessária para que você possa usar os recursos de IA.

Familiarize-se com a [linguagem de modelo Handlebars](https://handlebarsjs.com/guide/){target="_blank"}, a [sintaxe de personalização](./personalization-syntax.md) e as [funções auxiliares](./personalization-helper-functions.md) compatíveis com o [!DNL Journey Optimizer B2B Edition]. O Construtor de scripts gera Handlebars válidos para você, mas entender a sintaxe o ajudará a revisar e editar a saída com confiança.

## Abrir Construtor de scripts {#open-script-builder}

O Construtor de scripts está disponível no [editor de personalização](./personalization.md) enquanto você [cria conteúdo de email](./email-authoring.md) para uma jornada de conta.

1. No espaço de design de email, selecione o componente no qual deseja adicionar ou substituir um script de personalização.

1. Para abrir o editor de personalização, clique no ícone _Adicionar personalização_ ( ![Adicionar personalização](../../assets/do-not-localize/icon-personalization-field.svg) ).

1. No editor, selecione **[!UICONTROL Construtor de Scripts]**.

   ![Editor do Personalization - selecione Construtor de scripts](./assets/personalization-script-builder-select.png){width="700" zoomable="yes"}

   >[!BEGINSHADEBOX]

   Na primeira vez que você acessar o Construtor de Scripts, revise os [_[!UICONTROL Termos de Uso da IA Gerativa &#x200B;]_](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} e confirme seu contrato.

   ![Caixa de diálogo do contrato de Termos de Uso da IA Gerativa no Construtor de Scripts](./assets/personalization-script-builder-gen-ai-terms.png){width="400"}

   >[!ENDSHADEBOX]

   O painel Construtor de scripts é aberto com uma interface de bate-papo conversacional.

   ![editor do Personalization - painel Construtor de scripts](./assets/personalization-script-builder-welcome.png){width="700" zoomable="yes"}

1. Inicie o chat de acordo com o que deseja fazer:

   * [Gerar um novo script](#generate-personalization-script)
   * [Converter um script existente do Velocity](#convert-marketo-velocity-script)

## Gerar um script de personalização {#generate-personalization-script}

Use o Construtor de scripts para criar um novo script de personalização Handlebars a partir de uma descrição em linguagem simples, sem escrever a expressão você mesmo.

O Construtor de scripts inclui uma biblioteca de mapeamento que resolve campos de cliente potencial e conta do [!DNL Marketo Engage] para seus atributos de perfil XDM [!DNL Journey Optimizer B2B Edition] equivalentes, com base no [mapeamento de campo XDM](../admin/xdm-field-management.md) definido para sua organização.

1. Na interface de chat do Construtor de script, descreva a lógica de personalização desejada.

   Por exemplo, descreva o atributo, o objeto personalizado ou a condição que determina qual variante de conteúdo será exibida.

1. Revise o script Handlebars gerado no painel de visualização.

1. Edite o script diretamente no painel de visualização se desejar refinar a lógica ou a redação.

1. Clique em **[!UICONTROL Validar]** para verificar o script em relação ao esquema [!DNL Journey Optimizer B2B Edition].

   A validação captura erros de sintaxe e referências de token não resolvidas antes de salvar o script, de modo que a personalização corrompida nunca seja publicada em um email ativo.

1. Clique em **[!UICONTROL Salvar]** para inserir o script diretamente no local selecionado no email.

## Converter um script do Marketo Engage Velocity {#convert-marketo-velocity-script}

Use o Construtor de scripts para migrar um script existente do Velocity [!DNL Marketo Engage] para um script do Handlebars equivalente para [!DNL Journey Optimizer B2B Edition].

1. No bate-papo do Construtor de scripts, digite `Convert this` e cole o script do Velocity que deseja converter.

   O Construtor de scripts analisa as construções do Velocity, corresponde as referências de token aos atributos de perfil XDM e gera o script Handlebars equivalente.

1. Revise o [relatório de conversão](#review-conversion-report) e [resolva os tokens que precisam de mapeamento manual](#resolve-tokens-without-mapping).

1. [Visualize e valide](#preview-validate-script) o script gerado e, em seguida, salve-o diretamente no email.

### Construções Velocity compatíveis {#supported-velocity-constructs}

O Construtor de scripts converte as seguintes construções de fluxo de controle do Velocity [!DNL Marketo Engage] em suas Handlebars equivalentes ou expressões de Conteúdo condicional:

| Construção de velocidade | Handlebars ou equivalente de Conteúdo condicional |
| ------------------- | --------------------------------------------- |
| `#if` / `#elseif` / `#else` | Handlebars `{{#if}}`, `{{else if}}` e `{{else}}` auxiliares de bloco ou uma regra de [!DNL Journey Optimizer B2B Edition] [conteúdo condicional](./conditional-content.md) |
| `#set` | Uma atribuição de variável Handlebars no script gerado |

Ela traduz a lógica condicional baseada em segmentos em regras de [conteúdo condicional](./conditional-content.md) que replicam o comportamento de ramificação, incluindo emails com muitos blocos de variante de idioma.

Se uma construção do Velocity não tiver Handlebars direto ou conteúdo condicional equivalente, o Construtor de scripts a sinalizará no [relatório de conversão](#review-conversion-report) em vez de gerar uma expressão incompleta ou incorreta.

### Revisar o relatório de conversão {#review-conversion-report}

Após cada conversão, o Construtor de scripts exibe um relatório estruturado que lista:

* Tokens que foram mapeados com sucesso.
* Tokens que exigem resolução manual.
* Construções Velocity sem Handlebars direto equivalente.

Use o relatório para confirmar se a conversão foi concluída antes de resolver quaisquer tokens restantes e salvar o script.

### Resolver tokens sem um mapeamento {#resolve-tokens-without-mapping}

Para tokens que não estão na biblioteca de mapeamento, como atributos de cliente potencial personalizados ou objetos [!DNL Marketo Engage] personalizados, o Construtor de Scripts tenta resolver um mapeamento na seguinte ordem:

1. Ele sugere um mapeamento provável com base nos campos XDM disponíveis e, para objetos personalizados, as [classes baseadas em modelo](./personalization.md#custom-datasets) configuradas para sua organização, quando existir uma correspondência confiável.

1. Se não conseguir sugerir uma correspondência confiante, ele solicita o mapeamento correto no bate-papo.

Quando você confirma um mapeamento para um token que não estava na biblioteca, o Construtor de scripts pergunta se você deseja lembrar a decisão. Se você concordar, o mapeamento será lembrado para a instância de origem [!DNL Marketo Engage], identificada por sua Munchkin ID, para que o mesmo token seja resolvido automaticamente na próxima vez que você converter um script dessa instância.

### Pré-visualizar e validar o script {#preview-validate-script}

Antes de confirmar uma conversão, o Construtor de scripts exibe uma visualização lado a lado do script Velocity original e da saída Handlebars gerada, com suporte à edição em linha. Use a visualização para comparar as duas versões e fazer os ajustes diretamente no script gerado.

Clique em **[!UICONTROL Validar]** para verificar Handlebars gerados em relação ao esquema [!DNL Journey Optimizer B2B Edition]. A validação é executada novamente ao salvar, para que a personalização corrompida nunca seja publicada em um email em tempo real.

Quando estiver satisfeito com o resultado, clique em **[!UICONTROL Salvar]** para inserir o script diretamente no local escolhido no email.

<!--
### Save reusable conversion profiles {#save-reusable-conversion-profiles}

Save your field mappings and segment mappings as a reusable conversion profile so that your token schema does not need to be re-entered for each script or migration batch. Select a saved profile at the start of a conversion to apply its mappings automatically.

### Audit logs {#conversion-audit-logs}

Script Builder records an audit log for every conversion event, including which scripts were processed, which tokens were remapped, which tokens required manual intervention, and who approved the final output. Use the audit log to review migration activity across your organization.

-->
