---
title: Jornada controle de tráfego
description: Saiba como o controle de tráfego do jornada inscreve cada pessoa na jornada de melhor ajuste quando ela se qualifica para várias pessoas e como ajustar pesos e analisar decisões.
hide: true
autotag-review: '2026-10-16T18:41:12.165Z'
TQID: 'https://experienceleague.adobe.com/oD1nTkrgqGZ-nzfHNFS66XvjQkn5FmOZ-cI3EDKnb4U'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 4515ee43-e3ce-55db-9ba1-60b2b42b9d75
    internal-label: Privacy
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
subfeature_v2:
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
    internal-label: Decisioning
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d9b663ab-b785-4c49-8fc3-d3dda520c908
    internal-label: Automated decisioning
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 050fcccbef4e84a540d415cfabc65f25310c062f
workflow-type: tm+mt
source-wordcount: '2692'
ht-degree: 0%
---
# Jornada controle de tráfego

Em [!DNL Adobe Journey Optimizer B2B Edition], os públicos-alvo se sobrepõem com frequência. Um diretor de marketing em uma empresa de serviços financeiros pode se qualificar para a jornada do setor, a jornada de juros do produto e a jornada da conta da empresa no mesmo dia. Sem coordenação, essa pessoa é inscrita nos três e recebe mensagens concorrentes ou redundantes. Use o _controle de tráfego de Jornada_ para inscrever cada pessoa na jornada de uma pessoa que melhor se adapta quando ela se qualifica para mais de uma jornada ao mesmo tempo.

O controle de tráfego de jornadas analisa todas as pessoas qualificadas para mais de uma jornada participante. Ele compara o que você sabe sobre a pessoa com cada finalidade de jornada e inscreve a pessoa na melhor correspondência. Uma pessoa que se qualifica para apenas uma jornada está inscrita nessa jornada. Uma pessoa que se qualifica para nenhum não está inscrita.

## Benefícios do controle de tráfego de jornadas {#benefits}

O controle de tráfego de jornadas substitui o gerenciamento de sobreposição manual por uma decisão registrada e adequada para cada pessoa.

| Sem controle de tráfego de jornada | Com controle de tráfego de jornada |
|---|---|
| Uma pessoa que corresponde a vários públicos é inscrita em várias jornadas e recebe mensagens sobrepostas. | Cada pessoa está inscrita em no máximo uma jornada participante para cada avaliação. |
| As equipes gerenciam a sobreposição manualmente com segmentos de exclusão e regras de público-alvo. Essas regras ficam mais difíceis de manter a cada nova jornada. | O sistema escolhe com base na adequação. Você não cria ou mantém a lógica de exclusão. |
| É difícil explicar por que uma pessoa recebeu uma determinada jornada. | Todas as decisões são registradas e visualizadas, incluindo a pontuação de cada jornada concorrente. |
| A fadiga das mensagens e as mensagens mistas reduzem o engajamento. | Cada pessoa recebe uma experiência relevante e consistente. |

## Exemplos de uso {#examples}

Use o controle de tráfego de jornadas quando suas jornadas direcionam públicos sobrepostos. Por exemplo:

* **Programas de enfermagem do setor**: você executa jornadas separadas para serviços financeiros, saúde e manufatura. Um contato não tem valor de setor, mas seu perfil está vinculado à conta de um banco. O controle de tráfego de jornada corresponde o contato à jornada de Serviços Financeiros, em vez de inscrevê-los nos três.
* **Campanhas de interesse de produto**: você executa uma jornada para cada linha de produto. Um cliente potencial com sinais de interesse recentes em dois produtos está inscrito na jornada do produto com maior interesse.
* **Mensagens com base em função**: você executa uma jornada para avaliadores técnicos e outra para patrocinadores executivos. O cargo e a função de uma pessoa decidem em qual jornada ela se junta.
* **Programas Enterprise e SMB**: você executa jornadas diferentes por tamanho de empresa. O segmento de cliente de um contato e as informações da conta decidem em qual jornada ele se associa.
* **Novas inicializações de jornadas**: você publica uma nova jornada em um público que já é coberto por outras jornadas. O controle de tráfego de jornada avalia a sobreposição para que você não recrie as regras de público-alvo existentes.

## Seleção por ajuste {#dimensions}

Quando uma pessoa se qualifica para mais de uma jornada, o controle de tráfego de jornada compara o perfil da pessoa com o nome e a descrição de cada jornada candidata. A comparação abrange quatro dimensões.

| Dimensão | O que é comparado |
|---|---|
| Setor | A indústria da pessoa. Se o setor estiver ausente, o setor da conta vinculada. |
| Ajuste funcional | A função e o cargo da pessoa. |
| Tamanho da empresa | O segmento de cliente da pessoa, o tipo de conta e o contexto de gastos. |
| Intenção | O produto para o qual a pessoa mostrou o maior interesse recente. |

Lembre-se dos seguintes pontos:

* **As descrições e os nomes das Jornadas são importantes.** Eles informam ao sistema para que serve cada jornada. Descrições específicas e precisas produzem melhores correspondências.
* **Dados ausentes ignorados, não adivinhados.** Se uma pessoa não tiver valor para uma dimensão, o controle de tráfego de jornada deixa essa dimensão para essa pessoa. Ele toma a decisão sobre as dimensões que têm dados.

O registro de decisão de cada pessoa nas visualizações de relatórios mostra a pontuação de cada jornada concorrente e as dimensões usadas. Uma dimensão sem dados é marcada como excluída.

### Comparações {#comparisons}

Para cada dimensão, o controle de tráfego de jornadas compara o texto relevante da pessoa, como um título de cargo, com a descrição de cada jornada. Ela usa dois métodos:

* **Significado semelhante**: o texto significa algo próximo à descrição?
* **Correspondência de palavra-chave**: o texto usa os mesmos termos que a descrição?

O resultado mais forte dos dois métodos torna-se a pontuação da jornada para essa dimensão.

Cada dimensão propõe sua jornada de melhor pontuação, mas somente se a pontuação limpar um limite de qualidade mínimo. As jornadas sem uma proposta de qualificação são descartadas. Os pesos configurados classificam as jornadas restantes por suas pontuações ponderadas combinadas. A jornada com a pontuação mais alta é selecionada. O vencedor não é necessariamente a jornada com mais propostas. Uma correspondência forte em uma única dimensão é mais significativa do que várias correspondências mais fracas.

Cada registro de decisão armazena as seguintes informações:

* A jornada selecionada e as jornadas concorrentes
* As pontuações para cada dimensão e a pontuação combinada
* Um valor de confiança
* Um nível de contrato Alto, Medium ou Baixo, que mostra quantas dimensões suportaram o vencedor

<!-- CONFIRM with Engineering: whether to describe the fallback when no dimension produces a qualifying match. The source says the person is still enrolled in one eligible journey, selected consistently, with a 0% (Low) confidence decision record. Also confirm how "consistent" should be phrased. -->

## Configuração {#configuration}

Para definir os pesos da dimensão de controle de tráfego de jornada e simular a pontuação:

1. Na navegação à esquerda, vá para **[!UICONTROL Gerenciamento de Jornadas]** > **[!UICONTROL Controle de tráfego de Jornadas]**.

1. Selecione a guia **[!UICONTROL Configuração]**.

![Guia Configuração de controle de tráfego de Jornada com quatro cartões de peso de dimensão, cada um definido como Medium a 25% e botão Salvar pesos](./assets/journey-traffic-control-configuration.png){width="800" zoomable="yes"}

### Ajustar pesos da dimensão {#weights}

Por padrão, todas as quatro dimensões têm um peso de _Medium_ e contribuem igualmente, a 25% cada. Ajuste os pesos para alterar o quanto cada dimensão influencia as decisões.

1. Para cada dimensão, defina o nível de ponderação:

   * **[!UICONTROL Desligado]**
   * **[!UICONTROL Baixo]**
   * **[!UICONTROL Medium]**
   * **[!UICONTROL Alta]**

   A porcentagem em cada cartão mostra o compartilhamento dessa dimensão depois que suas configurações são combinadas. Para remover uma dimensão de decisões, defina-a como **[!UICONTROL Desativada]**.

   ![Cartões de peso da Dimension com intenção definida como Alta em 55%, Medium do setor em 27% e adequação funcional e Tamanho da empresa Baixo em 9%](./assets/journey-traffic-control-dimensions.png){width="600"}

   A porcentagem mostrada em cada cartão é a contribuição normalizada dessa dimensão após combinar todas as seleções, sempre totalizando 100%. Se você elevar uma dimensão, o sistema normaliza automaticamente as outras para que o total permaneça em 100%.

   Você pode clicar em **[!UICONTROL Redefinir para ser igual]** para retornar todas as dimensões para uma ponderação uniforme.

1. Quando quiser aplicar os pesos ajustados, selecione **[!UICONTROL Salvar pesos]**.

   >[!NOTE]
   >
   >Para salvar as alterações nos pesos da dimensão, você deve ter a _[!UICONTROL Gerenciar configurações de administrador B2B]_ [permissão de produto](../admin/user-management.md#b2b-product-permissions).

### Simular pontuação {#simulate-scoring}

Antes de confirmar pesos para produção, você pode simular como o controle de tráfego se comportaria com essas alterações. A simulação não requer que o controle de tráfego do jornada seja habilitado. Ele avalia os perfis que já estão nas jornadas ativas e aplica a lógica de controle de tráfego a eles. Então você pode julgar se os resultados parecem certos para as configurações de peso.

Clique em **[!UICONTROL Simular pontuação]**.

O cabeçalho de resultados resume a execução:

* **Perfis avaliados** — quantos perfis foram pontuados e em quantas jornadas.
* **Média de conflitos/perfil** — o número médio de jornadas concorrentes por perfil.
* **Pontuação média de correspondência** — a confiança média das jornadas selecionadas.

![Simular resultados de pontuação com 20 perfis avaliados em 5 jornadas, 1,0 conflitos de média e 70% de pontuação de correspondência média](./assets/journey-traffic-control-simulate-scoring.png){width="700" zoomable="yes"}

Cada perfil avaliado aparece como um cartão mostrando a jornada selecionada, o raciocínio principal, os sinais de intenção e a pontuação de correspondência. Selecione um perfil para abrir uma exibição detalhada:

* **Pontuação de correspondência** — A correspondência geral, com um detalhamento codificado por cores por dimensão.
* **Pontuações por jornada** — As jornadas para as quais essa pessoa se qualificou, qual foi selecionada e por quê.
* **Dimensões consideradas** — Os dados de dimensão que determinaram a decisão, expansíveis para mostrar os sinais subjacentes.

![Painel de detalhes do perfil com 77% de pontuação de correspondência, pontuações por jornada com uma jornada selecionada e as dimensões consideradas](./assets/journey-traffic-control-simulate-scoring-profile-details.png){width="450" zoomable="yes"}

Se necessário, ajuste os pesos da dimensão e clique em **[!UICONTROL Executar novamente]** para executar a simulação novamente.

Você também pode clicar em **[!UICONTROL Amostra de novas pessoas]** para executar a simulação novamente usando uma nova amostra aleatória.

Quando estiver satisfeito com o resultado, você poderá clicar em **[!UICONTROL Salvar pesos]** para confirmar os pesos. As novas decisões de controle de tráfego usam as novas configurações imediatamente, mas as decisões anteriores não são afetadas. Os pesos que você testou aparecem na guia _[!UICONTROL Configuração]_ principal e são usados para qualquer controle de tráfego do jornada que esteja avaliando em seu ambiente ativo.

Também é possível sair da página sem aplicar os pesos.

## Revisar relatórios {#reporting}

Use as exibições de relatórios para ver como o tráfego do jornada controla as pessoas inscritas. Revisar decisões por jornada ou por execução.

### Relatórios por jornada {#reporting-by-journey}

A exibição **[!UICONTROL Por Jornada]** resume as jornadas sob controle de tráfego.

| Métrica | Descrição |
|---|---|
| Jornadas controladas | Jornadas que participam do controle de tráfego. |
| Jornadas contestadas | Jornadas que compartilham pessoas com pelo menos uma outra jornada. |
| Perfis contestados | Pessoas distintas reivindicadas por duas ou mais jornadas. |
| Pessoas inscritas | Pessoas distintas inscritas. |

Para cada jornada, a exibição também mostra os seguintes valores:

* **[!UICONTROL Inscrito]**: o número total de pessoas inscritas.
* **[!UICONTROL Incontestado]**: pessoas que se qualificaram apenas para esta jornada.
* **[!UICONTROL Ganhou]**: pessoas que se qualificaram para várias jornadas e foram inscritas nesta.
* **[!UICONTROL Taxa de vitória]**: a frequência com que a jornada ganhou quando as pessoas competiram por ela.

![Por exibição de relatório do Jornada com métricas de resumo e uma tabela de jornadas mostrando valores de taxa de inscrição, não contestado, ganho e ganho](./assets/journey-traffic-control-reporting-by-journey.png){width="700" zoomable="yes"}

Filtre a lista por [status da jornada](./journeys-overview.md#journey-status): [!UICONTROL Ao Vivo], [!UICONTROL Concluído], [!UICONTROL Anulado] ou [!UICONTROL Todos].

Para ver onde as pessoas contestadas de uma jornada acabavam, abra a jornada. A exibição detalhada mostra as jornadas nas quais as pessoas foram inscritas. Para ver a pontuação de correspondência, as jornadas concorrentes, a pontuação de cada uma e as dimensões usadas, expanda o registro de decisão de qualquer pessoa inscrita. Pesquisar por nome, ID do cliente potencial ou ID do perfil.

![Exibição detalhada da Jornada com métricas de inscrição, um gráfico de onde os perfis contestados chegaram e uma tabela de pessoas inscritas](./assets/journey-traffic-control-reporting-by-journey-detail.png){width="700" zoomable="yes"}

Para comparar como o produto da indústria ou intenção é distribuído entre jornadas, selecione **[!UICONTROL Comparar jornadas]** e escolha pelo menos duas e até 20 jornadas ativas.

<!-- Figure placeholders: By Journey overview, journey detail "Where contested profiles landed", and a decision record. Redact person names and use clean sample journey names without test prefixes. Choose runs with healthy enrollment counts. -->

### Relatório por execução {#reporting-by-run}

Selecione **[!UICONTROL Por Execução]** para exibir uma lista de cada execução de avaliação com as seguintes informações:

* A hora da execução
* Como a execução foi acionada: *agendada*, *na publicação* ou *manual*
* O número de pessoas avaliadas, inscritas e não inscritas

![Ao executar o modo de exibição de relatório com intervalo de tempo e filtros de gatilho e uma tabela de execuções com contagens avaliadas, inscritas e não inscritas](./assets/journey-traffic-control-reporting-by-run.png){width="700" zoomable="yes"}

Filtre a lista por intervalo de tempo (24 horas, 7 dias, 30 dias ou todo o tempo) e tipo de acionador.

Para ver um diagrama de fluxo das pessoas avaliadas para as jornadas nas quais elas foram inscritas, abra uma execução. Um detalhamento de cada jornada mostra quantas pessoas foram **[!UICONTROL Não Inscritas]**, **[!UICONTROL Inscritas]**, **[!UICONTROL Arbitradas]** (escolhidas entre as jornadas concorrentes) e **[!UICONTROL Não Contestadas]**. Para qualquer jornada em uma execução, você também pode exibir as pessoas avaliadas, seus resultados, as jornadas com as quais competiram e suas pontuações de correspondência.

![Diagrama de fluxo mostrando as pessoas avaliadas e seus resultados de inscrição nas jornadas](./assets/journey-traffic-control-reporting-by-run-flow-chart.png){width="500" zoomable="yes"}

<!-- CONFIRM with Product: what the scheduled and on-publish triggers mean for customers, and the content of the Not enrolled tooltip. -->

## Processo de execução de avaliação {#run-process}

Cada execução segue a mesma sequência. O controle de tráfego de jornada lê apenas os dados já presentes no ambiente [!DNL Journey Optimizer B2B Edition] e não requer fontes de dados adicionais.

1. O controle de tráfego de jornada aguarda a conclusão com êxito da [atualização de perfil](../data/data-availability-timing.md#daily-refresh) de pessoa e conta em seu ambiente. Se a atualização falhar, nenhuma execução será iniciada nos dados obsoletos.

1. A associação de público é calculada em [!DNL Adobe Experience Platform] e [sincronizada](../data/data-availability-timing.md#platform-sync) para [!DNL Journey Optimizer B2B Edition]. Após a conclusão da segmentação, o sistema aguarda a conclusão da sincronização por até 30 minutos. Se a sincronização for concluída antes, o processamento será iniciado imediatamente. Se 30 minutos se passarem primeiro, o processamento será iniciado mesmo assim. Se a sincronização terminar mais tarde, uma nova execução será iniciada nos dados atualizados.

1. O sistema monta as jornadas candidatas. Somente jornadas que estão ativas e habilitadas para controle de tráfego participam. O sistema lê o status, o nome e a descrição de cada jornada.

1. O sistema lê a associação de público-alvo e o contexto de perfil em pequenos lotes.

1. O sistema verifica a qualificação. Uma pessoa está qualificada para uma jornada somente quando todos os itens a seguir são verdadeiros:

   * A jornada está ativa e ativada para controle de tráfego.
   * Atualmente, a pessoa é membro do público da jornada.
   * A pessoa não foi inscrita anteriormente nessa jornada.
   * A pessoa não está inscrita nessa jornada.

1. O sistema seleciona uma jornada. Uma pessoa com uma jornada qualificada está inscrita nela. Uma pessoa sem jornada qualificada não está inscrita. Para uma pessoa com várias jornadas qualificadas, o sistema compara o perfil da pessoa com o nome e a descrição de cada jornada nas [quatro dimensões](#dimensions).

1. O sistema envia a inscrição para a jornada selecionada por meio do mecanismo de inscrição de jornada padrão.

1. O sistema salva cada decisão e resultado de inscrição para relatórios e auditoria.

1. Os pontos de verificação do sistema avançam à medida que os lotes são concluídos, registram o resultado e enviam uma notificação de conclusão.

## Dados usados e armazenados {#data}

O controle de tráfego de jornadas usa os seguintes dados do seu ambiente.

| Dados | Fonte | Usar |
|---|---|---|
| Status, nome e descrição da jornada | Suas jornadas | Decida quais jornadas participam e para que servem cada jornada. |
| Associação de público-alvo | [!DNL Experience Platform] públicos-alvo sincronizados em [!DNL Journey Optimizer B2B Edition] | Identifique quem se qualifica para cada jornada. |
| Perfil da pessoa, como setor, cargo e função e segmento do cliente | Seus dados pessoais | Fornecer as dimensões do setor, adequação funcional e tamanho da empresa. |
| Perfil de conta vinculado, como setor e tipo de conta | Os dados da sua conta | Preencha o setor quando o valor da própria pessoa estiver ausente e o contexto da conta de fornecimento. |
| Interesse do produto | Seus [dados de intenção](../admin/intent-data.md) | Forneça a dimensão de intenção. É usado o produto com o maior interesse e o mais recente. |
| Histórico de inscrições | Registros gravados por execuções anteriores | Evite inscrever a mesma pessoa na mesma jornada repetidamente. |
| Status atual da inscrição | [!DNL Journey Optimizer B2B Edition] | Evite inscrever uma pessoa que já esteja na jornada. |

Para cada execução, o controle de tráfego do jornada armazena um resumo de execução. Para cada pessoa inscrita, ele armazena um registro de decisão de inscrição. Ambos são armazenados nos armazenamentos de dados gerenciados pela Adobe de seu ambiente. Eles alimentam os relatórios e impedem inscrições repetidas.

<!-- 
CONFIRM with Engineering, Security, and Legal before publishing. The source material does not state any of the following data handling commitments:
- Where processing occurs and data residency.
- Whether meaning similarity comparison uses a third-party or externally hosted AI service, and whether profile text leaves the Adobe environment.
- Whether customer data is used to train models shared with other customers.
- The retention period for decision and enrollment records, and how they are deleted when a person is erased (link to privacy requests).
- Encryption in transit and at rest, role-based access to the reports, and tenant isolation. 
-->

## Configurar o controle de tráfego do jornada {#setup}

Você pode habilitar o controle de tráfego de jornada diretamente em uma [jornada de pessoa](./create-publish-journey.md) individual quando ela estiver no status _Rascunho_.

1. Certifique-se de que a jornada de pessoa tenha um nome e uma descrição que forneça uma finalidade e uma meta claras para a jornada.

   Esses nomes e descrições são a base para a correspondência.

1. Clique em **[!UICONTROL ... Mais]** na parte superior direita da tela de jornada e escolha **[!UICONTROL configurações de controle de tráfego de Jornada]**.

   ![Menu jornada mais de pessoa de rascunho, abrir listagem de Duplicar, Excluir, configurações de controle de tráfego de Jornada e configurações de Reentrada](./assets/person-journey-draft-more-menu.png){width="400"}

1. Na caixa de diálogo, habilite a opção **[!UICONTROL Habilitar controle de tráfego de jornada]**.

   A caixa de diálogo de configurações explica o comportamento: quando ativada, a jornada se torna um candidato e o modelo avalia e recomenda a jornada mais adequada para uma pessoa qualificada para várias jornadas ativas.

   ![Caixa de diálogo de configurações de controle de tráfego de Jornada com a opção Habilitar controle de tráfego de jornada ativada, além dos botões Cancelar e Salvar](./assets/journey-traffic-control-enable-dialog.png){width="450"}

   >[!IMPORTANT]
   >
   >A opção pode ser alterada a qualquer momento enquanto a jornada permanece no status _Rascunho_. Depois de publicar a jornada com o controle de tráfego de jornada ativado, ela avalia a entrada nessa jornada e você não pode mais desativar a configuração.

1. Clique em **[!UICONTROL Salvar]**.

1. [Publicar](./create-publish-journey.md#publish-a-journey) a jornada de pessoa.

## Limitações e dependências {#limitations}

As seguintes dependências afetam quando e como o controle de tráfego do jornada funciona:

* **Sincronização de público-alvo**: as decisões dependem da associação de público-alvo atualizada sincronizada de [!DNL Experience Platform] para [!DNL Journey Optimizer B2B Edition]. O tempo de execução segue a segmentação e a conclusão da sincronização. Não é uma programação fixa.
* **Atualização de perfil**: uma execução só começa depois que a atualização de perfil de pessoa e conta é bem-sucedida.
* **Metadados da Jornada**: somente jornadas ativas habilitadas para controle de tráfego participam. A qualidade da correspondência depende dos nomes e descrições que você escreve.
* **Integridade do perfil**: a qualidade depende dos dados de pessoa, conta e intenção que você mantém. Dimensões ausentes são ignoradas.

O controle de tráfego do Jornada tem as seguintes limitações:

* **Uma jornada para cada pessoa**: uma pessoa está inscrita em no máximo uma jornada para cada execução.
* **A seleção não garante a inscrição**: até que a sincronização de [!DNL Experience Platform] seja concluída, alguns perfis poderão ser avaliados sem uma identificação de pessoa Marketo correspondente. A jornada está selecionada, mas a inscrição pode não ser bem-sucedida. Essas pessoas aparecem como *Não inscritas* em executar relatório.
* **Nenhuma inscrição repetida**: o controle de tráfego de Jornadas não inscreve uma pessoa em uma jornada na qual ela foi inscrita anteriormente. Para permitir que as pessoas se requalifiquem para uma jornada, use [configurações de reentrada do jornada](./journey-re-entry.md).
* **Não em tempo real**: as decisões são tomadas quando ocorre uma execução, não quando um perfil é alterado.
* **Quatro dimensões fixas**: você pode ajustar a importância da indústria, ajuste funcional, tamanho da empresa e intenção, mas não pode adicionar dimensões.
* **Correspondência baseada em texto**: nomes e descrições de Jornadas são comparados com texto de perfil. Jornadas com descrições vagas, vazias ou semelhantes são mais difíceis de diferenciar. Jornadas fracamente diferenciadas podem produzir resultados com baixa confiança.

O controle de tráfego da jornada decide apenas em qual jornada elegível uma pessoa está inscrita. Isso não altera suas jornadas ou públicos-alvo.

<!-- CONFIRM with Product and Engineering: the maximum number of governed journeys, maximum audience size for each run, supported editions and regions, and any language limitations for text matching. -->
