---
title: Ouvir um evento
description: Saiba mais sobre o tipo de nó Ouvir um evento que você pode usar para orquestrar suas jornadas de conta no Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 13%

---

# Ouvir um evento

Adicione o nó _Ouvir um evento_ para mover o público-alvo para a próxima etapa da jornada da conta quando ocorrer um evento.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Assista ao vídeo de visão geral](#overview-video)

>[!NOTE]
>
>Não é possível adicionar esse tipo de nó no caminho dividido por pessoas.

## Eventos de conta

Analise um evento com base na conta quando quiser mover a conta para frente na jornada de acordo com os eventos acionados pela atividade da conta.

### Eventos e restrições

| Evento | Restrições |
| ----- | ----------- |
| A conta teve um momento interessante | Tipo (Email, Marco ou Web)<br/>Restrições adicionais (opcional): <li>Descrição</li><li>Origem</li><li>Data da atividade</li> <br/>Tempo limite (opcional) |
| Alteração no valor dos dados da conta | Atributo<br/>Restrições adicionais (opcional): <li>Novo valor</li><li>Valor anterior</li><li>Data da atividade</li> <br/>Tempo limite (opcional) |
| Alteração no Estágio de Grupo de Compras | Interesse da solução<br/>Restrições adicionais (opcional): <li>Novo estágio</li><li>Fase anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| Alteração no Status do Grupo de Compras | Interesse da solução<br/>Restrições adicionais (opcional): <li>Novo status</li><li>Status anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| Alteração na pontuação de integridade | Interesse da solução<br/>Restrições adicionais (opcional): <li>Nova pontuação</li><li>Pontuação anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |
| Alteração na pontuação de engajamento | Interesse da solução<br/>Restrições adicionais (opcional): <li>Nova pontuação</li><li>Pontuação anterior</li><li>Data da atividade</li>Tempo limite de <br/> (opcional) |

### Adicionar um evento de conta

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Contas]** para o tipo de evento.

   ![Nó de Jornada - escutar eventos na conta](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Selecione um evento na lista.

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

## Eventos de pessoas

Analise um evento com base em pessoas quando quiser mover a conta para frente na jornada de acordo com os eventos acionados pela atividade de pessoas.

### Eventos e restrições

| Tipo de entrada | Evento | Restrições |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | Atribuído ao Grupo de Compras | Interesse da solução<br/><br/>Restrições adicionais (opcional): <li>Função</li><li>Data da atividade</li><br/>Tempo limite (opcional) |
| | Clica em link no email | Email<br/><br/>Restrições adicionais (opcional): <li>Link</li><li>ID do link</li><li>É um dispositivo móvel</li><li>Dispositivo</li><li>Plataforma</li><li>Navegador</li><li>É conteúdo preditivo</li><li>É atividade de bot</li><li>Padrão de atividade do bot</li><li>Navegador</li><li>Data da atividade</li><li>Número número de vezes</li><br/>Tempo limite (opcional) |
| | Cliques no link do SMS | Email<br/><br/>Restrições adicionais (opcional): <li>Link</li><li>Dispositivo</li><li>Plataforma</li><li>Data da atividade</li><li>Número número de vezes</li><br/>Tempo limite (opcional) |
| | Alterações no valor de dados | Atributo de pessoa<br/><br/>Restrições adicionais (opcional): <li>Novo valor</li><li>Valor anterior</li><li>Motivo</li><li>Origem</li><li>Data da atividade</li><li>Número número de vezes</li><br/>Tempo limite (opcional) |
| | Abre o email | Email<br/><br/>Restrições adicionais (opcional): <li>Link</li><li>ID do link</li><li>É um dispositivo móvel</li><li>Dispositivo</li><li>Plataforma</li><li>Navegador</li><li>É conteúdo preditivo</li><li>É atividade de bot</li><li>Padrão de atividade do bot</li><li>Navegador</li><li>Data da atividade</li><li>Número número de vezes</li><br/>Tempo limite (opcional) |
| | Removido do Grupo de Compras | Interesse da solução<br/>Data da atividade (opcional)<br/>Tempo limite (opcional) |
| | A pontuação é alterada | Nome da pontuação<br/><br/>Restrições adicionais (opcional):<li>Alterar</li><li>Nova pontuação</li><li>Urgência</li><li>Prioridade</li><li>Pontuação relativa</li><li>Urgência relativa</li><li>Data da atividade</li><li>Número número de vezes</li><br/>Tempo limite (opcional) |
| | Rejeições de SMS | Mensagem SMS<br/><br/>Restrições adicionais (opcional): <li>Data da atividade</li><li>Número mínimo de vezes</li><br/>Tempo limite (opcional) |
| Marketo Engage | Visita página da Web | Página da Web <br/> Selecione uma ou mais páginas do Marketo Engage para corresponder. <br/><br/>Restrições adicionais (opcional): <li>Cadeia de consulta</li><li>Endereço IP do cliente</li><li>Referenciador</li><li>Agente do usuário</li><li>Mecanismo de pesquisa</li><li>Pesquisar consulta</li><li>Token</li><li>Navegador</li><li>Plataforma</li><li>Dispositivo</li><li>Data da atividade</li> |
| | Preenche formulário | Formulário <br/> Selecione um ou mais formulários do Marketo Engage para corresponder.  <br/><br/>Restrições adicionais (opcional): <li>Data da atividade</li><li>Cadeia de consulta</li><li>Endereço IP do cliente</li><li>Referenciador</li><li>Agente do usuário</li><li>Plataforma</li><li>Dispositivo</li><br/>Tempo limite (opcional) |
| Adobe Experience Platform | Definição de evento | Tipo de evento <br/><br/>Restrições adicionais (opcional): <li>Campos</li> <br/>Restrições adicionais (sem suporte): <li>Data da atividade</li><li>Número número de vezes</li>Tempo limite de <br/> (opcional) |

### Adicionar um evento de pessoas

1. Navegue até o editor de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Ouvir um evento]**.

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para o tipo de evento.

   ![Nó de Jornada - escutar eventos em pessoas](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Selecione um evento na lista.

1. Clique em **[!UICONTROL Editar evento]** e defina os detalhes do evento.

### Ouvir o evento do Marketo Engage

Se você tiver páginas da Web criadas na instância conectada do Marketo Engage, poderá acionar um evento com base em uma visita/sem visita às páginas da Web do Marketo Engage, bem como aos formulários do Marketo Engage que não foram/foram preenchidos.

1. Selecione um nó **[!UICONTROL Ouvir um evento]** no editor de jornadas.

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para o tipo de evento.

1. Clique na seta do seletor **[!UICONTROL Selecionar evento de pessoas]** e role o menu até a seção **[!UICONTROL Marketo Engage]**.

1. Selecione um tipo de atividade de Participação no mercado:

   * **[!UICONTROL Visita à Página da Web]**.
   * **[!UICONTROL Preenche O Formulário]**

   ![Ouvir um evento de experiência](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Editar evento]** e defina uma ou mais páginas da Web para corresponder e quaisquer restrições adicionais para o evento.

   * (Obrigatório) Na caixa de diálogo _[!UICONTROL Editar evento]_, defina a **[!UICONTROL página da Web]** ou Preenche a restrição de formulário. Use **[!UICONTROL is]** (padrão) para corresponder em uma ou mais páginas ou formulários selecionados. Use **[!UICONTROL não]** para corresponder a todas as visitas/formulários da página, com a exclusão de uma ou mais páginas/formulários selecionados. Ou use **[!UICONTROL é qualquer]** para corresponder a qualquer visita de página da Web ou formulário preenchido do Marketo Engage.

   * (Opcional) Clique em **[!UICONTROL Adicionar restrição]** e escolha o campo que deseja usar para a restrição. Defina o operador e o valor do campo.

     ![Ouvir um evento de experiência](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Você pode repetir essa ação para incluir restrições de campo adicionais, conforme necessário.

   * Quando as restrições forem definidas, clique em **[!UICONTROL Concluído]**.

1. Se necessário, defina a opção **[!UICONTROL Tempo limite]** para limitar o período de tempo para ouvir o evento (consulte [Adicionar um tempo limite a um nó de evento](#add-a-timeout-to-an-event-node)).

1. No editor de jornadas, adicione o próximo nó a ser executado quando o evento ocorrer.

### Analise um evento de experiência

Os administradores podem configurar as definições de evento baseadas no Adobe Experience Platform (AEP), que permitem aos profissionais de marketing criar jornadas de conta que reagem aos [Eventos de experiência do AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent). O uso de eventos de experiência da AEP em jornadas de conta é um processo de duas etapas:

1. [Criar e publicar uma definição de evento da AEP](../admin/configure-aep-events.md).

2. Em uma jornada de conta, adicione um nó _Ouvir um evento_ e selecione uma definição de evento do Experience Platform para um evento com base em pessoas.

_Para incluir um Evento de Experiência na jornada:_

1. Selecione um nó **[!UICONTROL Ouvir um evento]** no editor de jornadas.

1. Nas propriedades do nó à direita, escolha **[!UICONTROL Pessoas]** para o tipo de evento.

1. Clique na seta do seletor **[!UICONTROL Selecionar evento de pessoas]** e role o menu até a seção **[!UICONTROL Adobe Experience Platform]**.

   ![Ouvir um evento de experiência](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Selecione o evento.

   O tipo de evento é exibido como vazio nos detalhes do nó.

   ![Editar o evento](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Clique em **[!UICONTROL Editar evento]** e defina os tipos de evento e quaisquer restrições adicionais para o evento.

   * (Obrigatório) Na caixa de diálogo _[!UICONTROL Editar evento]_, defina o tipo de evento. Você pode usar o operador padrão **[!UICONTROL is]** para corresponder um ou mais tipos de evento selecionados. Ou você pode usar o operador **[!UICONTROL não]** para corresponder em todos os tipos de evento com a exclusão de um ou mais tipos de evento selecionados.

   * (Opcional) Clique em **[!UICONTROL Adicionar restrição]** e escolha o campo que deseja usar para a restrição. Defina o operador e o valor do campo.

     ![Ouvir um evento de experiência](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >As restrições para _data de atividade_ e _número mínimo de vezes_ não são suportadas.

     Você pode repetir essa ação para incluir restrições de campo adicionais, conforme necessário.

   * Quando as restrições forem definidas, clique em **[!UICONTROL Concluído]**.

1. Se necessário, defina a opção **[!UICONTROL Tempo limite]** para limitar o período de tempo para ouvir o evento (consulte [Adicionar um tempo limite a um nó de evento](#add-a-timeout-to-an-event-node)).

1. No editor de jornadas, adicione o próximo nó a ser executado quando o evento ocorrer.

1. Conclua os nós restantes para sua jornada e [publique-a](./journey-overview.md).

   Quando a jornada está ativa (publicada) e atinge o nó _Ouvir um evento_, ela começa a ouvir eventos de experiência da AEP.

## Adicionar um tempo limite a um nó de evento

Se necessário, defina a quantidade de tempo que a jornada aguarda pelo evento. A jornada termina após um tempo limite, a menos que você defina um caminho de tempo limite, em que é possível adicionar outros nós.

1. Habilitar a opção **[!UICONTROL Tempo limite]**.

1. Selecione a duração pela qual a jornada aguarda a ocorrência de um evento antes de atingir o tempo limite.

   Você pode optar por finalizar o caminho aqui ou executar um curso de ação diferente definindo outro caminho.

1. Para criar um novo caminho na jornada, onde você pode adicionar ações e eventos aplicáveis a contas quando o evento não ocorrer, marque a caixa de seleção **[!UICONTROL Definir caminho de tempo limite]**.

   ![Nó de evento de Jornada - definir caminho de tempo limite](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Vídeo de visão geral

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
