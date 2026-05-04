---
title: Insights no CRM
description: Acesse os grupos de compra do Journey Optimizer B2B edition diretamente nos CRMs. Os membros da equipe de vendas podem visualizar dados de engajamento e identificar oportunidades de vendas com Insights no CRM.
feature: Sales Insights, Buying Groups
role: User
exl-id: c55a1fce-2ddc-481b-9f60-5e67a4bf9633
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-03-30T21:40:22.011Z'
source-git-commit: ff337a5f215daee1ea6dbe8d6b643087ac3324e2
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 2%

---

# Insights no CRM

O [!DNL In-CRM Insights] é um aplicativo baseado na web que se integra ao Salesforce e ao Microsoft Dynamics 365, dando a você acesso a [!DNL Journey Optimizer B2B Edition] grupos de compras diretamente no seu CRM. Ele reúne fontes de dados de vendas, facilitando a identificação de oportunidades para maior envolvimento e potencial de vendas.

## Instalação

O processo de instalação inclui:

* Configuração de permissões e grupos de usuários
* Instalação do pacote de software
* Fazer logon por meio do CRM

### Definir permissões

Os usuários que instalam o software devem ter permissões para instalar pacotes do Salesforce.

Para acessar o aplicativo, os usuários devem ter uma função de membro com a permissão **Insights de Vendas:View Insights de Vendas**.

Se quiser restringir usuários a apenas [!DNL In-CRM Insights]:

1. Crie uma [função personalizada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) e atribua a ela a permissão **Insights de vendas: Exibir insights de vendas**.
1. Crie um novo [grupo de usuários](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Adicione um perfil de produto do Experience Platform ao grupo.

### Instalar o pacote

Para instalar o pacote In-CRM Insights, siga as etapas para Salesforce ou Microsoft Dynamics.

#### Salesforce

1. Baixe o [pacote do instalador do In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Após fazer logon, você será redirecionado para a página de instalação do pacote.
1. Selecione a opção **[!UICONTROL Instalar para Todos os Usuários]** e clique em **[!UICONTROL Instalar]**.

   ![Instalar o pacote In-CRM Insights](assets/incrm-install-sf.png){width=500}

1. Aprove o acesso de terceiros na caixa de diálogo e clique em **[!UICONTROL Continuar]**.
1. Quando a instalação terminar, clique em **[!UICONTROL Concluído]**.

   Agora ele está listado na página **Pacotes Instalados** e o **Journey Optimizer B2B edition** está listado no Inicializador de Aplicativos.

   ![Insights no CRM configurados no Salesforce](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Baixe o [pacote do instalador do In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Vá para o [Portal do Power Apps](https://make.powerapps.com/){target=_blank}.
1. Depois de entrar, selecione o ambiente do pacote e navegue até **[!UICONTROL Soluções]** no menu esquerdo.
1. Clique em **[!UICONTROL Importar solução]**.
1. Procure e carregue o pacote do instalador e clique em **[!UICONTROL Avançar]**.
1. Verifique os detalhes do pacote e clique em **[!UICONTROL Avançar]**.
1. Em _Variáveis de ambiente_, verifique se o valor está definido como `prod` (não altere o valor) e clique em **[!UICONTROL Importar]**.
1. Quando a instalação for concluída, o **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL Grupos de compras]** será exibido na barra de navegação esquerda.

   ![Insights no CRM disponíveis no Microsoft Dynamics](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Exibir seus grupos de compra

Siga as instruções para fazer logon em sua conta da Adobe. Seus grupos de compra estão carregados e disponíveis para visualização.

Depois de selecionar um grupo de compras, você pode procurar os [detalhes do grupo](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). Isso é o mesmo que os dados e insights exibidos no Journey Optimizer B2B edition, mas os dados são somente leitura até [!DNL In-CRM Insights].
