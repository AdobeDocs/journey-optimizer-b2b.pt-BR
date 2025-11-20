---
title: Mapeamento de persona
description: Saiba como configurar o mapeamento pessoal para marketing B2B. Mapeie os atributos de pessoa no Journey Optimizer B2B edition para criar modelos de função e otimizar o direcionamento de grupos de compra.
feature: Setup, Buying Groups
role: Admin
source-git-commit: 278add74cc8d1aedd7809fd4675627f26501b0df
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Mapeamento de personas

As personas são um aspecto principal em uma abordagem de marketing baseado em conta (ABM) porque ajudam os profissionais de marketing a ajustar suas estratégias às necessidades, preferências e pontos problemáticos específicos dos indivíduos nas contas de destino. Os profissionais de marketing podem criar perfis detalhados para cada persona, incluindo o histórico, as responsabilidades, os pontos problemáticos e os canais de comunicação preferidos. Com essas definições, os administradores podem configurar personas de acordo com os atributos de pessoa no Journey Optimizer B2B edition, para que os modelos de funções possam usar condições de função simplificadas e consistentes que capturam essas personas.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Definição pessoal e limitações de uso:

* É possível ter até 20 personalidades definidas na lista _[!UICONTROL Mapeamento de persona]_.
* Cada persona pode incluir até cinco atributos em sua definição.
* Em todas as personalidades definidas, você pode usar até dez atributos de pessoa diferentes.

>[!BEGINSHADEBOX]

**Caso de uso: variações de cargo**

Muitas equipes de marketing e vendas usam cargos como uma maneira de identificar diferentes perfis em uma conta. Mas os títulos dos contatos podem ser inconsistentes e usar várias variações para funções semelhantes. Ao criar modelos de funções de grupos de compra, pode ser necessário definir cada título de cargo relacionado possível para uma determinada função. É possível simplificar essas definições e trazer pessoas com títulos de trabalho semelhantes para uma persona inferida, que você pode aproveitar em diferentes modelos de funções para grupos de compra.

Por exemplo, você pode configurar uma persona chamada _Gerenciamento de Produto_ e defini-la usando o atributo de título de trabalho para valores de _Gerente de Produto_, _Sr. Gerente de produto_, _Gerente de produto sênior_, _PM_, _Sr. PM_, _PM Principal_ e _Gerente de Produto Principal_. Em seguida, use esta persona em um modelo de Funções no qual a condição corresponda em _A persona é o Gerenciamento de Produto_. Usando a persona configurada, a criação de cada modelo de função é simplificada e não requer uma condição complicada que possa corresponder a cada título de cargo possível.

>[!ENDSHADEBOX]

## Acessar os perfis configurados

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.

1. Clique em **[!UICONTROL Mapeamento de persona]** no painel intermediário para exibir a lista de personas.

   ![Acessar as personalidades configuradas](./assets/configuration-persona-mapping.png){width="800" zoomable="yes"}

   Nesta página, você pode [criar](#create-a-persona), [editar](#edit-a-persona) ou [excluir](#delete-a-persona) personas.

   A lista Mapeamento de pessoas está organizada como uma tabela e exibe os perfis atualizados mais recentemente na parte superior (classificado por _[!UICONTROL Última atualização]_). Você pode personalizar a tabela exibida ao clicar no ícone _Configurações de coluna_ ( ![Configurações de coluna](../assets/do-not-localize/icon-column-settings.svg) ) no canto superior direito e marcar ou desmarcar as caixas de seleção da coluna.

![Colunas a serem exibidas na lista de mapeamento de persona](./assets/configuration-persona-mapping-list-columns.png){width="300"}

1. Para acessar os detalhes de uma persona, clique no nome.

### Personas padrão

A lista _Mapeamento de persona_ inclui cinco personas padrão definidas de acordo com o atributo de título do trabalho. Você pode editar qualquer um desses perfis padrão de acordo com as necessidades de sua organização:

| Persona | Cargos |
| ------- | ---------- |
| CXO / EVP - CXO / Vice-presidente executivo | CEO, CIO, CTO, CMO, CFO, vice-presidente executivo de estratégia |
| Vice-presidente/Vice-presidente sênior | Vice-presidente de marketing, vice-presidente de vendas, vice-presidente de operações, vice-presidente de produtos, vice-presidente de TI |
| Diretor sênior / Diretor - Diretor sênior / Diretor | Diretor de engenharia, Diretor sênior de produto, Diretor financeiro, Diretor de sucesso do cliente |
| Gerente sênior / Gerente - Gerente sênior / Gerente | Gerente de marketing sênior, gerente de TI, gerente de operações, gerente de vendas, gerente de RH |
| Contribuinte Individual - Contribuinte Individual | Executivo de contas, engenheiro de software, especialista em marketing, representante de sucesso do cliente |
| Analista - Analista | Analista de negócios, Analista de dados, Analista de pesquisa de mercado, Analista financeiro, Analista de operações |
| Desenvolvedor - Desenvolvedor | Desenvolvedor front-end, desenvolvedor back-end, desenvolvedor de pilha completa, desenvolvedor de aplicativos móveis, engenheiro de DevOps |
| Equipe profissional - Equipe profissional | Especialista de RH, consultor jurídico, analista de conformidade, gerente de projeto, especialista em aquisição |
| Consultor - Consultor | Consultor de gerenciamento, consultor de TI, consultor de processos de negócios, consultor de marketing |
| Outro - Outro | Especialista do setor, consultor independente, consultor independente, especialista no assunto |

### Filtragem de lista

Para localizar o perfil desejado, insira uma cadeia de texto na barra de pesquisa para corresponder perfis por nome,

![Filtrar os mapeamentos de persona exibidos](./assets/configuration-persona-mapping-search.png){width="700" zoomable="yes"}

## Criar uma persona

1. Na navegação à esquerda, escolha **[!UICONTROL Administração]** > **[!UICONTROL Configuração]**.

1. Clique em **[!UICONTROL Mapeamento de persona]** no painel intermediário.

1. Clique em **[!UICONTROL Criar persona]**.

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** exclusivos (opcional) para a persona.

   ![Criar um mapeamento personalizado](./assets/configuration-persona-mapping-new.png){width="700" zoomable="yes"}

1. Selecione os atributos a serem usados para corresponder à persona.

   * Clique em **[!UICONTROL Selecionar atributos de pessoa]**.

   * Na caixa de diálogo, marque a caixa de seleção de cada atributo que você deseja mapear (no máximo cinco).

     Você pode personalizar a tabela exibida clicando no ícone _Configurações de coluna_ ( ![Configurações de coluna](../assets/do-not-localize/icon-column-settings.svg) ) no canto superior direito.

     Para filtrar a lista de atributos por nome, digite uma string de texto na barra de pesquisa. Você também pode clicar no ícone _Filtro_ ( ![Ícone Filtro](../assets/do-not-localize/icon-filter.svg) ) na parte superior esquerda para filtrar a lista exibida por tipo, _Padrão_ ou _Personalizado_.

     ![Caixa de diálogo Selecionar atributos pessoais](./assets/configuration-persona-mapping-select-attributes.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Salvar]**.

     Os atributos selecionados são preenchidos na seção _[!UICONTROL Atributos pessoais]_.

1. Para cada atributo, insira os valores separados por vírgula que você deseja corresponder ao atributo.

   No lugar de um valor, você também pode adicionar um prompt que pode ser usado para identificar uma correspondência. Por exemplo, você poderia inserir

1. Clique em **[!UICONTROL Enviar]**.

## Editar uma persona

Clique no nome da persona para acessar e editar os detalhes dela,

Você pode alterar o nome ou a descrição, adicionar atributos ou atualizar os valores do atributo. Clique em **[!UICONTROL Enviar]** quando as alterações forem concluídas.

## Excluir um perfil

Excluir uma pessoa a remove da lista _Mapeamento de pessoas_ e ela não está mais disponível para uso em modelos de funções.

1. Na página _[!UICONTROL Mapeamento pessoal]_, localize o perfil que deseja excluir.

1. Ao lado do nome, clique no ícone de reticências (**...**) para e escolha **[!UICONTROL Excluir]**.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Excluir]**.
