---
title: Dividir e mesclar caminhos
description: Saiba mais sobre os caminhos divididos e os tipos de nó dos caminhos de mesclagem que você pode usar para orquestrar as jornadas de conta no Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '2141'
ht-degree: 6%

---

# Dividir e mesclar caminhos

Use os nós de caminho dividido e mesclado na jornada da conta para orquestrar as jornadas da conta de acordo com as condições definidas para contas ou pessoas. Você pode segmentar o público-alvo da jornada ou a lista de contas de acordo com as condições, definir um caminho com nós de ação e evento para cada segmento e, em seguida, combinar os segmentos e continuar a jornada.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

Um nó _Split paths_ define um ou mais caminhos segmentados com base em filtros de conta ou de pessoas.

>[!NOTE]
>
>Há suporte para, no máximo, 25 caminhos.

## Dividir caminhos por contas

Os caminhos divididos por contas podem incluir ações e eventos de contas e pessoas. Esses caminhos podem ser divididos ainda mais.

_Como funciona um caminho dividido por nó de contas?_

* Cada caminho adicionado inclui um nó final com a capacidade de adicionar nós a cada borda.
* Os nós divididos por conta podem ser aninhados (você pode dividir o caminho por contas repetidamente).
* A avaliação de cada caminho é de cima para baixo. Se uma conta corresponder ao primeiro e ao segundo caminhos, ela continuará somente pelo primeiro caminho.
* Dois ou mais caminhos podem ser combinados usando um nó de mesclagem.
* O nó oferece suporte à definição de um caminho _[!UICONTROL Outras contas]_, em que você pode adicionar ações ou eventos para contas que não correspondam a um dos segmentos/caminhos definidos.

Nó do ![Jornada - caminhos divididos por conta](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

### Condições de caminho da conta

| Condições de caminho | Descrição |
| --------------- | ----------- |
| Atributos de contas | Atributos do perfil da conta, incluindo: <li>Receita anual <li>Cidade <li>País <li>Tamanho do funcionário <li>Setor <li>Nome <li>Código SIC <li>Estado |
| [!UICONTROL Filtros especiais] > [!UICONTROL Tem Grupo de Compras] | A conta tem ou não membros de grupos de compra. Também podem ser avaliados em relação a um ou mais dos seguintes critérios: <li>Interesse da solução <li>Status do Grupo de Compras <li>Pontuação de integridade <li>Pontuação de engajamento |
| [!UICONTROL Filtros especiais] > [!UICONTROL Tem oportunidade] | A conta está ou não relacionada a uma oportunidade. Também podem ser avaliados em relação a um ou mais dos seguintes atributos de oportunidade: <li>Valor<li>Data de encerramento<li>Descrição<li>Receita esperada<li>Trimestre fiscal<li>Ano fiscal<li>Categoria de previsão<li>Nome da categoria de previsão<li>Está encerrado<li>Foi ganho <li>Data da última atividade <li>Fonte de pessoas<li>Nome <li>Próxima etapa <li>Probabilidade<li>Quantidade<li>Estágio <li>Tipo |

### Adicionar um caminho dividido pelo nó da conta

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](./assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para a divisão.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

   ![Nó de caminho dividido - adicionar condição](./assets/node-split-properties-apply-condition.png){width="500"}

1. No editor de condições, adicione um ou mais filtros para definir o caminho dividido.

   * Arraste e solte atributos de filtro da navegação à esquerda e conclua a definição de correspondência.

   * Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você escolhe corresponder todas as condições de atributo ou qualquer condição.

     ![Nó de caminho dividido - lógica de filtro de contas de condições](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e repita as etapas anteriores para adicionar condições aplicáveis a este caminho.

   Você também pode rotular cada caminho com base nessas condições ou usar os rótulos padrão.

1. Se necessário, reordene os caminhos de acordo com a prioridade desejada para a divisão.

   A filtragem de caminho é avaliada em ordem decrescente. Cada conta continua pelo primeiro caminho correspondente.

   Clique nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista de caminhos.

   ![Nó de caminho dividido - reordenar caminhos](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Habilite a opção **[!UICONTROL Outras contas]** para definir o caminho padrão para contas que não correspondem aos segmentos/caminhos definidos.

   Quando essa opção não está ativada, a jornada termina para contas que não correspondem a um segmento/caminho definido na divisão.

## Dividir caminhos por pessoas

Os caminhos divididos por pessoas podem incluir somente ações de pessoas. Esses caminhos não podem ser divididos novamente e se unem automaticamente.

_Como funciona um caminho dividido por nó de pessoas?_

* Divisão por nós de pessoas em uma combinação de divisão de mesclagem de _nó agrupado_. Os caminhos divididos se mesclam automaticamente para que todas as pessoas no público-alvo possam avançar para a próxima etapa sem perder o contexto da conta.
* Os nós Split by people não podem ser aninhados (não é possível adicionar um caminho dividido para pessoas em um caminho que esteja neste nó agrupado).
* A avaliação de cada caminho é de cima para baixo. Se uma pessoa corresponder ao primeiro e ao segundo caminhos, ela continuará somente pelo primeiro caminho.
* O nó oferece suporte ao uso de _relações conta-pessoa_, que permitem filtrar pessoas com base em sua função (como contratante ou funcionário em tempo integral), conforme definido na relação.
* O nó oferece suporte à definição de um caminho _[!UICONTROL Outras pessoas]_, em que você pode adicionar ações ou eventos para pessoas que não correspondem a um dos segmentos/caminhos definidos.

![Nó do Jornada - caminhos divididos por pessoas](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Condições de caminho de pessoas

| Condições de caminho | Descrição |
| --------------- | ----------- |
| [!UICONTROL Atributos da pessoa] | Atributos do perfil de pessoa, incluindo: <li>Cidade</li><li>País</li><li>Data de nascimento</li><li>Endereço de email</li><li>Email inválido</li><li>Email suspenso</li><li>Nome</li><li>Região inferida</li><li>Nome do cargo</li><li>Sobrenome</li><li>Número do celular</li><li>Número de telefone</li><li>Código postal</li><li>Estado</li><li>Inscrição cancelada</li><li>Motivo do cancelamento de inscrição</li> |
| [!UICONTROL Histórico de atividades] > [!UICONTROL Email] | Atividades de email com base nas condições avaliadas usando uma ou mais mensagens de email selecionadas anteriormente na jornada: <li>[!UICONTROL Link clicado no email] <li>E-mail aberto <li>O email foi entregue <li>Email enviado <br>**[!UICONTROL Alternar para filtro de inatividade &#x200B;]**- Use esta opção para filtrar com base na falta de atividade (uma pessoa não tinha a atividade de email). |
| [!UICONTROL Histórico de atividades] > [!UICONTROL Mensagem SMS] | Atividades de SMS com base em condições que são avaliadas usando uma ou mais mensagens SMS selecionadas anteriormente na jornada: <li>[!UICONTROL Link clicado em SMS] <li>[!UICONTROL SMS Devolvido] <br>**[!UICONTROL Alternar para filtro de inatividade &#x200B;]**- Use essa opção para filtrar com base na falta de atividade (uma pessoa não tinha a atividade de SMS). |
| [!UICONTROL Histórico de atividades] > [!UICONTROL Valor dos dados alterado] | Para um atributo de pessoa selecionado, ocorreu uma alteração de valor. Esses tipos de alterações incluem: <li>Novo valor<li>Valor anterior<li>Motivo<li>Origem<li>Data da atividade<li>Número número de vezes <br>**[!UICONTROL Alternar para o filtro de inatividade &#x200B;]**- Use essa opção para filtrar com base na falta de atividade (uma pessoa não teve uma alteração no valor de dados). |
| [!UICONTROL Histórico de Atividades] > [!UICONTROL Teve Um Momento Interessante] | Atividade de momento interessante definida na instância associada do Marketo Engage. As restrições incluem: <li>Data importante<li>Email<li>Web <br>**[!UICONTROL Alternar para filtro de inatividade &#x200B;]**- Use esta opção para filtrar com base na falta de atividade (uma pessoa não teve um momento interessante). |
| [!UICONTROL Histórico de atividades] > [!UICONTROL Página da Web visitada] | Atividade da página da Web que para uma ou mais páginas da Web gerenciadas pela instância do Marketo Engage associada. As restrições incluem: <li>Página da Web (obrigatório)<li>Data da atividade<li>Endereço IP do cliente <li>Cadeia de consulta <li>Referenciador <li>Agente do usuário <li>Mecanismo de pesquisa <li>Pesquisar consulta <li>URL personalizada <li>Token <li>Navegador <li>Plataforma <li>Dispositivo <li>Número número de vezes <br>**[!UICONTROL Alternar para o filtro de inatividade &#x200B;]**- Use essa opção para filtrar com base na falta de atividade (uma pessoa não visitou a página da web). |
| [!UICONTROL Filtros especiais] > [!UICONTROL Membro do Grupo de Compras] | A pessoa é ou não é um membro do grupo de compra avaliado em relação a um ou mais dos seguintes critérios: <li>Interesse da solução</li><li>Status do Grupo de Compras</li><li>Pontuação de integridade</li><li>Pontuação de engajamento</li><li>Função</li> |
| [!UICONTROL Filtros especiais] > [!UICONTROL Membro da Lista] | A pessoa é ou não membro de uma ou mais listas do Marketo Engage. |
| [!UICONTROL Filtros especiais] > [!UICONTROL Membro do programa] | A pessoa é ou não é membro de um ou mais programas do Marketo Engage. |

### Condições de caminho conta-pessoa

| Condições de caminho | Descrição |
| --------------- | ----------- |
| [!UICONTROL Função na conta] | Uma função na conta é atribuída ou não à pessoa. Restrições opcionais: <li>Nome da função |

### Adicionar um caminho dividido pelo nó de pessoas

>[!NOTE]
>
>Quando você divide caminhos por pessoas, um nó _Fechar caminhos divididos_ é inserido automaticamente para encerrar a divisão. Um caminho dividido por pessoas permite somente _Realizar uma ação_ em nós de pessoas.

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   ![Adicionar nó do jornada - caminhos divididos](./assets/add-node-split.png){width="300"}

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para a divisão.

1. Defina os **[!UICONTROL Atributos usados para as condições]**.

   * Escolha **[!UICONTROL Somente atributos de pessoas]** para usar condições relacionadas ao perfil de pessoa.
   * Escolha **[!UICONTROL Somente atributos Conta-Pessoa]** para usar condições relacionadas à associação de função da pessoa em uma conta.

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

1. No editor de condições, adicione um ou mais filtros para definir o caminho dividido.

   * Arraste e solte qualquer um dos atributos de pessoas da navegação à esquerda e conclua a definição de correspondência.

     >[!NOTE]
     >
     >Se você tiver campos de pessoa personalizados definidos no esquema de público-alvo da conta no Experience Platform, esses campos também estarão disponíveis para uso como atributos de pessoa em condições.

   * Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você escolhe corresponder todas as condições de atributo ou qualquer condição.

     ![Nó de caminho dividido - lógica de filtro de pessoa de condições](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Clique em **[!UICONTROL Concluído]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e repita as etapas anteriores para adicionar condições aplicáveis a este caminho.

   Você também pode rotular cada caminho com base nessas condições ou usar os rótulos padrão.

1. Se necessário, reordene os caminhos de acordo com a prioridade desejada para a divisão.

   A filtragem de caminho é avaliada em ordem decrescente. Cada pessoa continua pelo primeiro caminho que corresponde a.

   Clique nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista de caminhos.

   ![Nó de caminho dividido - reordenar caminhos](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Habilite a opção **[!UICONTROL Outras pessoas]** para adicionar um caminho padrão para pessoas que não correspondam aos caminhos definidos.

   Quando essa opção não está ativada, as pessoas que não correspondem a um segmento/caminho definido passam pela divisão e avançam para a próxima etapa da jornada.

   Quando você tem condições definidas para cada caminho para dividir o público no nível das pessoas, é possível adicionar ações que deseja realizar nas pessoas.

### Filtragem de atividade

Para um caminho dividido por pessoas, você pode definir um caminho de acordo com a atividade da pessoa relacionada a:

* Mensagens de email de antes na jornada
* Mensagens SMS de versões anteriores na jornada
* Alteração no valor dos dados no perfil da pessoa
* Um momento interessante (rastreado no Marketo Engage) associado a um email, página da Web ou marco
* Visita a uma página da Web rastreada no Marketo Engage

>[!BEGINSHADEBOX &quot;Filtragem de inatividade&quot;]

Para cada filtro de _[!UICONTROL Histórico de atividades]_, você pode habilitar a opção **[!UICONTROL Alternar para filtro de inatividade]**. Essa opção altera o filtro para uma avaliação de ausência desse tipo de atividade. Por exemplo, se você deseja criar um caminho para pessoas que _&#x200B;**não**&#x200B;_ abriram um email anteriormente na jornada, adicione o filtro _[!UICONTROL Email]_ > _[!UICONTROL Email aberto]_. Ative a opção de inatividade e especifique o email. É uma prática recomendada usar a restrição _[!UICONTROL Data da atividade]_ para definir um período de tempo para a inatividade.

![Dividir caminho por condição de pessoas para comprar associação de grupo](./assets/node-split-people-condition-inactivity.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

### Filtragem de associação

Na seção _[!UICONTROL Filtros Especiais]_, há vários filtros que você pode usar para avaliar a associação de uma pessoa em um grupo de compra ou lista de Marketo Engage. Por exemplo, se você deseja criar um caminho para pessoas que são membros de um grupo de compra e receberam uma função específica, adicione o filtro _[!UICONTROL Filtros especiais]_ > _[!UICONTROL Membro do grupo de compra]_. Para o filtro, defina a associação como _true_, selecione um _[!UICONTROL Interesse da solução]_ associado a um ou mais grupos de compra e defina a _[!UICONTROL Função]_ que você deseja corresponder.

![Dividir caminho por condição de pessoas para comprar associação de grupo](./assets/node-split-people-condition-buying-group-membership.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;associação à lista do Marketo Engage&quot;]

No Marketo Engage, as _Campanhas inteligentes_ verificam a associação de programas para garantir que os clientes potenciais não recebam emails duplicados e não sejam membros de vários fluxos de emails ao mesmo tempo. No Journey Optimizer B2B, você pode verificar a associação à lista do Marketo Engage como uma condição para o caminho dividido por pessoas para ajudar a eliminar a duplicação em atividades de jornada.

Para usar a associação de lista em uma condição de divisão, expanda **[!UICONTROL Filtros Especiais]** e arraste a condição **[!UICONTROL Membro da Lista]** para o espaço de filtro. Conclua a definição do filtro para avaliar a associação em uma ou mais listas do Marketo Engage.

![Dividir caminho por condição de pessoas para associação à lista de Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

## Mesclar caminhos

Adicione um nó _Merge paths_ para combinar diferentes caminhos divididos por conta em sua jornada.

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

1. Clique no nó dividido para abrir as propriedades à direita.

1. Clique em [!UICONTROL Adicionar caminho] para criar três caminhos.

1. Adicione uma combinação de ações e eventos a cada caminho.

1. Clique no ícone de adição ( **+** ) de qualquer um desses caminhos e escolha **[!UICONTROL Mesclar]** nas opções exibidas.

   ![Nó do Jornada - caminhos de mesclagem](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Nas propriedades do nó dos caminhos de mesclagem, selecione os caminhos que deseja mesclar.

   ![Nó do Jornada - caminhos de mesclagem](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Nesse ponto, os caminhos são mesclados para que as contas dos caminhos selecionados sejam combinadas em um único caminho que possa continuar avançando pela jornada.

1. Se necessário, você pode desfazer a mesclagem de caminhos navegando de volta para as propriedades do nó dos caminhos de mesclagem e desmarcando a caixa de seleção de todos os caminhos que deseja remover.

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443261/?learn=on&captions=por_br)
