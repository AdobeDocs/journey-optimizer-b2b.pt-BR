---
title: Nós de espera
description: Use nós de espera para pausar a progressão da jornada e controlar o tempo de saída por duração, data ou configurações avançadas de dia e hora.
feature: Account Journeys, Person Journeys
role: User
exl-id: fecab788-4e8e-490a-bcca-bc3ab43411d9
source-git-commit: 7a05e6aed76d15aa6d0d0a7dd244bf299d549782
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Esperar nós

Use um nó _Wait_ quando quiser pausar a progressão da jornada por uma determinada duração antes de passar para a próxima etapa.

Há duas maneiras de definir o tempo de espera:

* Uma data específica na qual você deseja avançar para o próximo nó na jornada
* Uma duração relativa (número de minutos, horas, dias, semanas ou meses)

## Adicionar o nó de espera

1. Navegue até o mapa de jornadas.

1. Clique no ícone de adição ( **+** ) em um caminho e escolha **[!UICONTROL Aguardar]**.

   ![Adicionar nó de jornada - espera](./assets/add-node-wait.png){width="440"}

1. Nas propriedades do nó à direita, defina o **[!UICONTROL Type]** de tempo a ser aguardado antes que a jornada continue para o próximo nó no caminho.

   * **[!UICONTROL Duração]** - Defina um número específico de dias, horas ou minutos decorridos entre a entrada e a saída do nó de espera.
   * **[!UICONTROL Data]** - Especifique uma data e hora específicas para a saída.

   ![Nó de Jornada - espera](./assets/node-wait.png){width="500"}

## Configurações avançadas de espera

Habilite a opção **[!UICONTROL Deve terminar em]** para configurar uma _etapa de espera avançada_ e garantir que suas mensagens cheguem às pessoas e aos membros da conta no momento ideal. Essa configuração oferece controle preciso sobre quando uma pessoa ou conta sai de uma etapa de espera e prossegue para o próximo nó na jornada. Em vez de um número fixo de horas ou dias, desde a entrada até a saída, você pode agendar ações para que ocorram em horários e dias específicos da semana.

Com uma _etapa de espera avançada_, você define **_quando_** a pessoa ou conta deve sair, e não apenas quanto tempo deve esperar.

![nó de Jornada - etapa de espera avançada](./assets/node-wait-advanced.png){width="500"}

>[!AVAILABILITY]
>
>As configurações avançadas de espera estão disponíveis para ambientes [!DNL Journey Optimizer B2B Edition] que são provisionados na [arquitetura simplificada](../simplified-architecture.md).

### Tipos de espera

| Tipo de espera | Descrição | Configuração |
| --------- | ----------- | ------------- |
| **Hora específica do dia** | Manter até um horário específico (como 9:00 AM) | Defina a hora (hora e minuto). Sai na próxima ocorrência desse horário (para o fuso horário selecionado). |
| **Dia da semana específico** | Manter até um dia específico (como terça-feira) | Selecione um dia da semana. Se nenhuma hora for especificada, o sai à meia-noite (para o fuso horário selecionado) no próximo dia correspondente. |
| **Intervalo ou combinação de dias** | Manter até qualquer dia dentro de um intervalo (como segunda a sexta-feira) ou em qualquer um dos dias especificados | Selecione os dias de destino. Se nenhuma hora for especificada, o sai à meia-noite (para o fuso horário selecionado) no próximo dia correspondente. |
| **Combinação de tempo + dia** | Combine ambos para um agendamento preciso (como terça-feira às 10h):00 | Selecione os dias de destino e defina o horário de destino. Sai na próxima ocorrência de dia/hora (para o fuso horário selecionado). |

### Cenários comuns

Os cenários a seguir ilustram como você pode aplicar cenários típicos à configuração do nó de espera:

+++Chegada de email durante o horário comercial

**Cenário:** você comercializa para clientes B2B que leem emails no trabalho. Você deseja que todos os emails cheguem durante o horário comercial.

**Solução:** configure sua etapa de espera para liberar clientes potenciais às 9:00 da manhã nos dias da semana (de segunda a sexta-feira). Não importa quando um lead entra no nó de espera, ele recebe seu email durante o horário comercial.

+++

+++Tempos de envio consistentes para públicos dinâmicos

**Cenário:** seu público-alvo muda diariamente à medida que novas contas ou clientes potenciais se qualificam. Deseja que todos os clientes em potencial recebam o primeiro email ao mesmo tempo, independentemente de quando se qualificaram.

**Solução:** Defina a etapa de espera para terminar em um horário específico (como 10h:00). Todos os clientes em potencial, sejam eles qualificados à meia-noite ou ao meio-dia, saiam da etapa de espera juntos às 10h:00.

+++

+++Tarefas de acompanhamento em conformidade com a SLA

**Cenário:** sua equipe de vendas tem uma SLA de dois dias úteis para acompanhar clientes em potencial qualificados para marketing. Finais de semana não contam.

**Solução:** configure a etapa de espera para liberar clientes potenciais somente em dias úteis. Um lead qualificado na sexta-feira é encaminhado para acompanhamento na segunda ou terça-feira, não durante o fim de semana.

+++

### Exemplos de entrada e saída

| Aguardar configuração | Entradas de conta/cliente potencial | Saídas da conta/lead |
| ------------------ | ------------------- | ------------------ |
| 9h :00, Qualquer dia | Segunda-feira 11:00 AM | Terça-feira, 9:00 AM |
| 9h :00, Qualquer dia | Segunda-feira, 7:00 AM | Segunda-feira, 9:00 AM |
| Terça-feira, sem horário definido | Sexta 3:00 PM | Terça-feira, 12:00 AM |
| 10:00 AM, de segunda a sexta-feira | Sábado 2:00 PM | Segunda-feira, 10:00 AM |
| 10:00 AM, de segunda a sexta-feira | Quarta-feira, 8:00 AM | Quarta-feira, 10:00 AM |
