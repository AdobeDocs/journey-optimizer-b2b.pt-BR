---
title: Lista de verificação de configuração
description: Conclua as tarefas de configuração iniciais para sua instância do Journey Optimizer B2B Prime, incluindo a configuração de acesso do usuário e a infraestrutura de capacidade de entrega de email.
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f467931a-9b22-4ca8-869f-adfbd64061ceid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0f264f00c8018324abf1d409ddc381c6dcc9c08a
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 10%

---

# Lista de verificação de configuração

Conclua essas tarefas para habilitar a funcionalidade na instância [!DNL Journey Optimizer B2B Prime] provisionada.

## Habilitar acesso do usuário {#enable-user-access}

Quando o provisionamento estiver concluído e as sandboxes estiverem vinculadas, configure o acesso do [!DNL Journey Optimizer B2B Edition] para sua equipe e usuários.

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fornecer acesso e permissões ao produto</strong> para usuários</td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Criar um perfil de produto do Journey Optimizer B2B edition na Admin Console (configuração única/inicial apenas)</td>
<td><a href="./user-management.md#create-profile">Criar perfil</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Adicionar um grupo de usuários na Admin Console</td>
<td><a href="./user-management.md#add-user-group">Adicionar grupo de usuários</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Atribuir o perfil de produto ao grupo de usuários no Admin Console</td>
<td><a href="./user-management.md#assign-profile">Atribuir perfil de produto</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Adicionar usuários ao grupo de usuários no Admin Console</td>
<td><a href="./user-management.md#add-users">Adicionar usuários</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Editar funções integradas ou criar uma função personalizada com permissões de produto</td>
<td><a href="./user-management.md#edit-role-permissions">Editar funções</a> <br/> <a href="./user-management.md#create-a-custom-role">Criar uma função personalizada</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Adicionar usuários ou grupos a funções no Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Adicionar usuários</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Adicionar grupos</a></td>
</tr>
</tbody>
</table>

## Capacidade de entrega de email {#email-deliverability}

Antes que os profissionais de marketing possam enviar emails do jornada, configure a infraestrutura de envio para sua organização, incluindo a delegação de subdomínio, a autenticação de email e as configurações de canal.

<table>
<thead>
<tr>
<th colspan="2">Tarefa</th>
<th>Detalhes e instruções</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Definir configurações de capacidade de entrega de email e canal</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Delegar um subdomínio à Adobe (totalmente delegado ou CNAME)</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">Totalmente delegado</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Configurar o DMARC para o subdomínio</td>
<td><a href="./email-deliverability.md#configure-dmarc">Configurar DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Revisar e atribuir um pool de IPs</td>
<td><a href="./email-deliverability.md#review-ip-pool">Revisar pool de IPs</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Caixa de seleção para tarefa"/></td>
<td>Criar uma configuração de canal de email</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">Configurar canal de email</a></td>
</tr>
</tbody>
