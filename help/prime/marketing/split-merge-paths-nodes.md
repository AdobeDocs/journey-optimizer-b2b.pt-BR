---
title: Nós Dividir e Mesclar Caminhos
description: Espaço reservado
autotag-review: '2026-06-12T23:04:27.208Z'
TQID: 'https://experienceleague.adobe.com/TZlkuuES1Q2ZlG-ND-tIu6cVBRA65hIfotDcroER9Mc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 569
ht-degree: 0%

---

# Dividir e mesclar nós de caminhos



## Nós de caminhos divididos

Use nós divididos para segmentar pessoas de acordo com as condições definidas. Crie caminhos para a lista de público-alvo de acordo com as condições, defina cada caminho com nós de ação e evento para o segmento e, em seguida, combine os caminhos e continue a jornada.

Um nó Caminhos divididos define um ou mais caminhos segmentados com base em filtros de pessoas.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**Como funciona um caminho dividido por nó de pessoas**&#x200B;_

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