---
title: Personalidades derivadas
description: Use personas derivadas no Journey Optimizer B2B Prime para direcionar listas de pessoas e caminhos de jornada. Saiba mais sobre os mapeamentos de persona padrão e o filtro Persona derivado.
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 4632a06ce5a17713fdcaecf6eac8c051bc984e28
workflow-type: tm+mt
source-wordcount: 650
ht-degree: 2%

---

# Personas derivadas

A classificação personalizada transforma dados brutos do cliente em dados semânticos do comprador, entendendo que a IA pode usar para gerar contexto e impulsionar decisões personalizadas em cada canal e jornada. Esse perfil unificado capacita:

* _Ramificação da Jornada_ - Dividir caminhos de clientes em potencial por persona, profundidade de participação e função
* _Arbitragem de Jornada_ - Determina a qual criação um cliente potencial pertence agora, evitando colisões de mensagens em programas simultâneos
* _Personalização de conteúdo_ - Conteúdo que é narrativas específicas de função (&quot;para um executivo&quot; vs. &quot;para um profissional&quot;)
* _Contexto do Qualificador de Vendas_ - Os BDRs recebem um resumo em uma tela mostrando &quot;quem é essa pessoa, com o que ela se importa, onde ela está na jornada do comprador&quot;

## Personas padrão {#default-ersonas}

Para a versão Beta do Journey Optimizer B2B Prime, as seguintes personas padrão são definidas de acordo com o atributo de título do cargo:

| Persona | Cargos |
| ------- | ---------- |
| [!UICONTROL CXO/EVP] | CEO, CIO, CTO, CMO, CFO, vice-presidente executivo de estratégia |
| [!UICONTROL VP/VP] | Vice-presidente de marketing, vice-presidente de vendas, vice-presidente de operações, vice-presidente de produtos, vice-presidente de TI |
| [!UICONTROL Gerente/Gerente sênior] | Gerente de marketing sênior, gerente de TI, gerente de operações, gerente de vendas, gerente de RH |
| [!UICONTROL Colaborador Individual] | Executivo de contas, engenheiro de software, especialista em marketing, representante de sucesso do cliente |
| [!UICONTROL Analista] | Analista de negócios, Analista de dados, Analista de pesquisa de mercado, Analista financeiro, Analista de operações |
| [!UICONTROL Desenvolvedor] | Desenvolvedor front-end, desenvolvedor back-end, desenvolvedor de pilha completa, desenvolvedor de aplicativos móveis, engenheiro de DevOps |
| [!UICONTROL Equipe profissional] | Especialista de RH, consultor jurídico, analista de conformidade, gerente de projeto, especialista em aquisição |
| [!UICONTROL Consultor] | Consultor de gerenciamento, consultor de TI, consultor de processos de negócios, consultor de marketing |
| [!UICONTROL Outras] | Especialista do setor, consultor independente, consultor independente, especialista no assunto |

>[!NOTE]
>
>Na versão de Disponibilidade geral, você poderá editar qualquer um desses perfis padrão de acordo com as necessidades da sua organização. Também oferecerá suporte a definições e mapeamento de persona personalizados.

## Filtrar por persona derivada {#derived-persona-filter}

O Journey Optimizer B2B Prime deriva uma persona para cada registro de pessoa avaliando os atributos do registro em relação às personas definidas. Você pode usar o resultado inferido — a _Pessoa derivada_ — como filtro ao definir o público-alvo para uma lista de pessoas ou para segmentação em uma jornada de pessoa.

O filtro _[!UICONTROL Persona Derivada]_ aparece no painel de filtro na categoria **[!UICONTROL Atributos de pessoa]**.

### Listas de pessoas {#people-lists}

Ao adicionar ou remover membros de uma [lista estática de pessoas](./people-lists.md#static-list) ou ao definir as regras de associação para uma [lista dinâmica de pessoas](./people-lists.md#dynamic-lists), você pode filtrar por Persona Derivada para direcionar todas as pessoas cujos atributos correspondam a uma persona configurada específica.

![Filtragem de persona derivada para uma lista de pessoas](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Lista estática — Adicionar membros**

1. Abra a lista estática e clique em **[!UICONTROL Adicionar pessoas]** na parte superior direita.

1. Na caixa de diálogo de filtro, expanda **[!UICONTROL Atributos de pessoas]** e arraste **[!UICONTROL Persona derivada]** para a tela.

1. Na condição de filtro, escolha **[!UICONTROL é]** e selecione uma ou mais personalidades na lista.

1. Clique em **[!UICONTROL Concluído]** para aplicar o filtro e qualificar as pessoas correspondentes na lista.

**Lista dinâmica — Definir regras de associação**

1. Abra a lista dinâmica e selecione a guia **[!UICONTROL Regras]**.

1. Clique em **[!UICONTROL Editar regras]**.

1. Na caixa de diálogo de filtro, expanda **[!UICONTROL Atributos de pessoas]** e arraste **[!UICONTROL Persona derivada]** para a tela.

1. Na condição de filtro, escolha **[!UICONTROL é]** e selecione uma ou mais personalidades na lista.

1. Clique em **[!UICONTROL Concluído]** para salvar a regra.

   A associação é atualizada automaticamente à medida que os registros de pessoa são avaliados em relação à regra.

### Jornadas de pessoas {#person-journeys}

Ao configurar a segmentação para uma jornada de pessoa em um nó [_Dividir caminhos_](../marketing/split-merge-paths-nodes.md), você pode usar uma pessoa derivada como um filtro de perfil de pessoa para controlar quais pessoas entram no caminho de jornada.

![Filtragem de persona derivada para uma condição de caminho dividido](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Clique no nó **[!UICONTROL Split paths]** na tela de jornada.

1. No painel de propriedades do nó à direita, clique em **[!UICONTROL Aplicar condição]** ou **[!UICONTROL Editar condição]** para um caminho.

1. Na caixa de diálogo de filtro, expanda **[!UICONTROL Atributos de pessoas]** e arraste **[!UICONTROL Persona derivada]** para a tela.

1. Na condição de filtro, escolha **[!UICONTROL é]** e selecione uma ou mais personalidades na lista.

1. Clique em **[!UICONTROL Concluído]** para salvar o filtro para o caminho.

