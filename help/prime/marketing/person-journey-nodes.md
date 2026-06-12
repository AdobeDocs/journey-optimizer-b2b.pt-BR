---
title: Adicionar nós de Jornada
description: Página de espaço reservado para nós de jornada de pessoas.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 2%

---

# Adicionar nós do jornada

Depois de criar uma jornada de pessoa, adicione o público-alvo e crie a jornada usando nós. O mapa de jornada fornece uma tela, onde você pode criar seus casos de uso de marketing B2B em várias etapas.

O nó _[!UICONTROL Audiência da pessoa]_ é automaticamente o primeiro nó na jornada. Depois de selecionar o público-alvo, crie sua jornada combinando os diferentes nós de ação, evento e design como um cenário de várias etapas e canais. Cada nó de uma jornada representa uma etapa ao longo de um caminho lógico.

## Nó de público-alvo de pessoa

O nó de público-alvo pessoa especifica quais registros de pessoa entram na jornada. Quando você cria uma jornada de pessoa, a jornada sempre começa com um nó de público-alvo de pessoa que define sua entrada.

1. Clique no nó para selecioná-lo.
1. No painel de propriedades do nó à direita, use uma das seguintes opções de entrada para o nó de jornada do público-alvo de pessoa:

   * **[!UICONTROL Lista dinâmica]** - Use uma lista dinâmica de pessoas baseada em regras. As regras de lista são avaliadas no tempo de execução da jornada para qualificar membros da jornada. As pessoas que depois se desqualificam para a lista dinâmica não são removidas da jornada.

   * **[!UICONTROL Lista estática]** - Use uma lista estática de pessoas como membro da sua jornada. A associação de lista atual é avaliada no tempo de execução da jornada para qualificar membros para a jornada. As pessoas removidas posteriormente da lista estática não são removidas da jornada.

## Nós de ação de pessoas

Em uma jornada de pessoa, use uma ação em pessoas quando quiser aplicar uma alteração a todas as pessoas no caminho do nó. Para uma jornada de conta, esse tipo de nó pode ser usado no caminho dividido por pessoas ou no caminho dividido por contas.

### Ações e restrições

| Ação | Contrastes |
| ------ | ---------- |
| **[!UICONTROL Enviar email]** | <li>Criar email <li>Otimização do tempo de envio (opcional) |
| **[!UICONTROL Alterar valor de dados]** | <li>Selecionar atributo de pessoa <li>Definir novo valor |

### Adicionar um nó de ação

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Executar uma ação]**.

1. Nas propriedades do nó à direita, selecione uma ação na lista e defina os valores para a ação.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Enviar email]

Use esta ação para enviar um email. Depois de criar o email para o nó, você pode criar, personalizar e visualizar mensagens de email no espaço de design de email (consulte [Criação de email](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Você pode usar a [Otimização de hora de envio](../marketing/email-send-time-optimization.md) para personalizar o tempo de entrega de email prevendo quando cada perfil tem maior probabilidade de participar.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Alterar valor de dados]

Use esta ação para alterar o valor de um atributo de perfil de pessoas no banco de dados. Selecione o atributo e defina o novo valor.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++

## Nós de evento

Adicione o nó _Ouvir um evento_ para mover o público-alvo para a próxima etapa da jornada quando ocorrer um evento.

### Filtros de evento de pessoas

| Filtros | Descrição |
| ------- | ----------- |
| Histórico de atividades > Email | Atividades de email com base nas condições avaliadas usando uma ou mais mensagens de email selecionadas: <li>Clicou em um link no email <li>Email aberto |
| Histórico de atividades > Valor de dados alterado | Para um atributo de pessoa selecionado, ocorreu uma alteração de valor. Esses tipos de alterações incluem: <li>Novo valor <li>Valor anterior <li>Motivo <li>Fonte <li>Data da atividade <li> Número número de vezes |

### Adicionar um nó de evento

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para o tipo de evento.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Selecione um evento na lista.

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

>[!NOTE]
>
>No momento, a funcionalidade de tempo limite do Listen para um nó de evento não funciona e será ativada em uma fase posterior.

## Nós de caminhos divididos

Use nós divididos para segmentar pessoas de acordo com as condições definidas. Crie caminhos para a lista de público-alvo de acordo com as condições, defina cada caminho com nós de ação e evento para o segmento e, em seguida, combine os caminhos e continue a jornada.

Um nó Caminhos divididos define um ou mais caminhos segmentados com base em filtros de pessoas.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_**Como funciona um caminho dividido por nó de pessoas**_

* A avaliação de cada caminho é de cima para baixo. Se uma pessoa corresponder ao primeiro e ao segundo caminhos, ela continuará somente pelo primeiro caminho.
* O nó oferece suporte à definição de um caminho _Outras pessoas_, em que você pode adicionar ações ou eventos para pessoas que não correspondem a um dos segmentos/caminhos definidos.

### Filtros correspondentes

Para cada caminho definido para o nó, use os seguintes tipos de filtro para corresponder pessoas de acordo com uma ou mais condições:

* Histórico de atividades - Você pode definir um caminho de acordo com a atividade da pessoa relacionada a:

   * Mensagens de email
   * Alteração no valor dos dados

* Atributos de pessoa - Defina uma condição de acordo com os atributos de uma pessoa, como país, cargo ou associação à lista.

### Adicionar um nó de caminhos divididos

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Dividir caminhos]**.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. Para definir uma condição aplicável ao _[!UICONTROL Caminho 1]_, clique em **[!UICONTROL Aplicar condição]**.

1. No editor de condições, adicione um ou mais filtros para definir o caminho dividido.

   * Arraste e solte qualquer um dos filtros de pessoas da navegação à esquerda e conclua a definição de correspondência.

   * Ajuste as condições aplicando a **[!UICONTROL lógica de Filtro]** na parte superior. Você escolhe corresponder todas as condições ou qualquer uma delas.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Clique em **[!UICONTROL Concluído]**.

1. Para adicionar mais caminhos, clique em **[!UICONTROL Adicionar caminho]** e repita as etapas anteriores para adicionar condições aplicáveis ao caminho.

   Você também pode rotular cada caminho com base nessas condições ou usar os rótulos padrão.

1. Se necessário, reordene os caminhos de acordo com a prioridade desejada para a divisão.

   A filtragem de caminho é avaliada em ordem decrescente. Cada pessoa continua pelo primeiro caminho que corresponde a.

   Clique nas setas para cima e para baixo na parte superior direita de cada cartão de caminho para movê-lo para cima ou para baixo na lista de caminhos.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Habilite a opção **[!UICONTROL Outras pessoas]** para adicionar um caminho padrão para pessoas que não correspondam aos caminhos definidos.

   Quando essa opção não está ativada, as pessoas que não correspondem a um segmento/caminho definido passam pela divisão e avançam para a próxima etapa da jornada.

Quando você tem condições definidas para cada caminho, pode adicionar nós de ação ou evento que deseja aplicar às pessoas em um caminho.

## Nós dos caminhos de mesclagem

1. Navegue até o mapa de jornadas e localize o nó de caminhos divididos com dois ou mais caminhos.

   Cada caminho deve ter uma combinação de ações e eventos em cada caminho.

1. Clique no ícone de adição ( **+** ) ao final de qualquer um desses caminhos e escolha **[!UICONTROL Mesclar caminhos]** nas opções exibidas.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. Nas propriedades do nó à direita, selecione os caminhos que deseja mesclar.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   Nesse ponto, os caminhos são mesclados para que as pessoas dos caminhos selecionados se combinem a um único caminho que possa continuar avançando pela jornada.

1. Se necessário, você pode desfazer a mesclagem de caminhos navegando de volta para as propriedades do nó dos caminhos de mesclagem e desmarcando a caixa de seleção de todos os caminhos que deseja remover.
