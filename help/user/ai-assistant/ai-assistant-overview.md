---
title: Assistente de IA no Journey Optimizer B2B edition
description: Saiba mais sobre o AI Assistant e como ele pode ajudar você a navegar pelos conceitos do produto e acessar insights operacionais personalizados para seu ambiente.
feature: AI Assistant
role: User, Admin
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 4%

---

# Assistente de IA no Journey Optimizer B2B edition

O Assistente de IA no Journey Optimizer B2B edition foi criado a partir da mesma base tecnológica do [Assistente de IA no Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}. É uma experiência de conversação que você pode usar para acelerar seus fluxos de trabalho no Adobe Journey Optimizer B2B edition. Você pode usar o Assistente de IA para entender melhor os recursos do produto, solucionar problemas ou pesquisar informações e encontrar insights operacionais para o Journey Optimizer B2B edition.

>[!IMPORTANT]
>
>É necessário um contrato com as [diretrizes de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) para que você possa usar o Assistente de IA no Journey Optimizer B2B edition. Este contrato também contém o contrato público beta para que você possa usar os recursos adicionais do Assistente de IA à medida que forem implantados na capacidade beta.

+++Exibir a interface do contrato do usuário

![A primeira página do contrato de usuário.](./assets/user-agreement-1.png)

![A última página do contrato de usuário.](./assets/user-agreement-2.png)

+++

## Recursos do Assistente de IA no Journey Optimizer B2B edition

Para formular uma resposta às suas perguntas enviadas, o Assistente de IA consulta um banco de dados e traduz os dados do banco de dados em uma resposta legível. Essa resposta é uma representação interna de dados subjacentes e também é conhecida como _&#x200B;**_Gráfico de Conhecimento_**&#x200B;_ — uma Web abrangente de conceitos, dados e metadados para uma determinada resposta. O Gráfico de conhecimento consiste em subgráficos que são referenciados sempre que as consultas são enviadas:

* Documentação do Experience League.
* Artefatos operacionais, como esquemas, campos, públicos e jornadas.

Considere qual tipo de pesquisa é necessário antes de submeter uma consulta do Assistente do AI:

### Conhecimento do produto

O conhecimento do produto refere-se a conceitos e tópicos fundamentados na documentação do Journey Optimizer B2B edition na Adobe Experience League. As perguntas sobre o conhecimento do produto podem ser especificadas mais detalhadamente nos seguintes subgrupos:

| Conhecimento do produto | Exemplos |
| --- | --- |
| Aprendizado apontado | <li>O que é um grupo de compras? <li> Mostrar um exemplo de modelo de funções de grupo de compra? |
| Abrir descoberta | <li>Quais são as etapas para criar grupos de compra? <li>Como faço para usar campos personalizados em modelos de funções de um grupo de compra? |
| Solução de problemas | <li>Por que não foram criados grupos para minha jornada? <li>Por que não consigo encontrar eventos de experiência para ouvir na jornada? |

### Insights operacionais

_Os insights operacionais_ referem-se às respostas que o AI Assistant gera sobre os objetos de metadados (atributos, públicos-alvo de conta, fluxos de dados, conjuntos de dados, destinos, jornadas de conta, esquemas, fontes, modelos de grupo de compra e interesses de solução). Esses insights incluem contagens, pesquisas e impacto de linhagem. Eles não observam nenhum dado na sandbox.

* Qual público-alvo de conta tem o maior tamanho de público-alvo e qual é esse tamanho?
* Quantos públicos-alvo de conta nunca foram usados em nenhuma jornada?
* Qual interesse de solução de uso do jornada ativo _x_?

Você pode fazer perguntas ao Assistente de IA sobre seus insights operacionais nos seguintes domínios:

| Domínio | Metadados compatíveis | Metadados incompatíveis |
| --- | --- | --- |
| Atributos/campos | <li>Pesquisa de nome de atributo <li>Atributo - relacionamento de esquema <li>Relação atributo-conjunto de dados <li>Atributo - relacionamento de público <li>Relação atributo-destino | <li>Classe de atributo <li>Auditoria <li>Status de desativação <li>Rótulos <li>Valor armazenado em atributos |
| Públicos-alvo da conta <br><br>**_Observação:_**&#x200B;o Assistente de IA B2B da AJO só pode responder a perguntas de públicos-alvo para Públicos-alvo da conta, enquanto o Assistente de IA da Experience Platform só pode responder a perguntas de Públicos-alvo de pessoa | <li>Contagem de público-alvo <li>Tipo de público-alvo (streaming ou lote) <li>Datas de criação/modificação <li>Status de ativação <li>Contagem de membros <li>Duplicar públicos <li>Pesquisa de nome e ID | <li>Sobreposições de público <li>Ativação de público-alvo <li>Auditoria <li>Criar/modificar <li>Rótulos <li>Tendências de qualificação de membros |
| Fluxos de dados | <li>Contagens de fluxo de dados <li>Status do fluxo de dados <li>Fluxo de dados - relação do conjunto de dados <li>Fluxo de dados - relacionamento de origem | <li>Criação/modificação <li>Relações fluxo-lote de dados <li>Contagem de perfis de assimilação |
| Conjuntos de dados | <li>Contagem do conjunto de dados <li>Status de habilitação do perfil <li>Data de criação/modificação <li>Relação entre conjunto de dados e esquema <li>Conjunto de dados - relacionamento de público-alvo <li>Conjunto de dados - relação de atributo <li>Relação entre conjunto de dados e fluxo de dados <li>Pesquisa de nome <li>Pesquisa de nome e ID | <li>Auditoria <li>Criado por <li>Relação entre conjunto de dados e lote <li>Criação/modificação do conjunto de dados <li>Tamanho do conjunto de dados <li>Número de perfis <li>Número de linhas <li>Pesquisa de valor |
| Destinos | <li>Contagens de destino configuradas <li>Relação destino - público <li>Relação de atributo de destino | <li>Configuração de conta <li>Informações de credencial da conta <li>Perfis únicos ativados |
| Jornadas (Jornadas de conta) | <li>Contagem <li>Pesquisa de nome e ID <li>Status da jornada <li>Datas de criação/modificação | <li>Atributos - Auditoria de relacionamentos de jornada <li>Criação/modificação <li>Criado por |
| Esquemas | <li>Contagens de esquema <li>Data de criação/modificação <li>Esquema - Relação de atributo <li>Relação esquema - conjunto de dados <li>Esquema - relacionamento de público <li>Status de habilitação do perfil <li>Pesquisa de nome <li>Pesquisa de nome e ID | <li>Auditoria <li>Criação/modificação <li>Criado por <li>Grupos de campos <li>Identidades <li>Namespaces de identidade <li>Rótulos <li>Número de perfis |
| Origens | <li>Contagens de conta <li>Status da conta <li>Fluxos de dados ativos/inativos para cada conta <li>Source connector - relação de fluxo de dados <li>Relação conta Source - fluxo de dados | <li>Informações de credenciais da conta <li>Métricas de assimilação de dados de configuração de conta <li>Número de perfisOrigem - relacionamentos em lotes |
| Modelo do grupo de compra | <li>Contagens <li>Status <li>Funções <li>Pesquisa de nome e ID | <li>Regras de função |
| Interesse da solução | <li>Contagens <li>Status <li>Interesse da solução - Relacionamento do modelo do grupo de compra <li>Pesquisa de nome e ID | <li>Interesse da solução - Relacionamento do grupo de compra |

{style="table-layout:fixed"}

Para perguntas sobre insights operacionais, as respostas podem não refletir o estado atual da interface do usuário. Os dados que sustentam essas perguntas são atualizados uma vez a cada 24 horas. Por exemplo, as alterações que os usuários fazem no Real-Time CDP durante o dia são sincronizadas com os armazenamentos de dados à noite e, em seguida, ficam disponíveis para perguntas do usuário de manhã. Faça logon em uma sandbox para saber sobre dados específicos relacionados a objetos.

### Escopo do recurso

Atualmente, o escopo do Assistente de IA é o seguinte:

* **Conhecimento de produto**: o AI Assistant pode responder a perguntas de conhecimento de produto do Real-Time Customer Data Platform e do Adobe Journey Optimizer B2B edition.

* **Insights operacionais**: você pode fazer perguntas ao Assistente de IA sobre insights operacionais para os seguintes objetos de dados: atributos, públicos-alvo de conta, fluxos de dados, conjuntos de dados, destinos, jornadas de conta, esquemas, fontes, modelos de grupo de compra e interesses de solução.

### Privacidade, segurança e governança

O Assistente de IA no Journey Optimizer B2B edition foi criado com privacidade, segurança e governança na vanguarda. Consulte as seguintes informações para saber mais sobre os recursos focados na confiança do cliente que você pode esperar do Assistente de IA:

* Nenhum dado pessoal é usado pelo Assistente de IA hoje, mesmo para fins de treinamento.

* O Assistente de IA não tem conhecimento dos dados do cliente, como pessoas, conta, oportunidades e grupos de compras.

* Você deve ter permissão explícita para interagir com o Assistente de IA.

   * Um administrador pode definir permissões usando a [Interface de Permissões](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} e a [Admin Console](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/browse){target="_blank"}.

   * As permissões são granulares e o administrador da sandbox pode configurar quais usuários podem fazer diferentes categorias de perguntas (perguntas baseadas em conhecimento do produto com o Assistente de IA ou perguntas sobre insights operacionais).

* Você pode exibir um log de suas interações anteriores com o AI Assistant com uma política de retenção de 30 dias.

* O Assistente de IA é baseado em dados específicos da sandbox e na documentação pública do Adobe ao responder aos prompts do usuário. Os dados não são compartilhados em sandboxes.

* Os prompts fornecidos ao Assistente de IA não são compartilhados com outros clientes.

### Perguntas frequentes

Esta é uma lista de respostas para perguntas frequentes sobre o Assistente de IA no Journey Optimizer B2B edition.

**As informações do Assistente de IA são fornecidas em tempo real?**

Os dados apresentados nas respostas do Assistente de IA são atualizados diariamente. Esse ciclo significa que os dados incluídos nas respostas do podem ser até 24 horas mais antigos do que os dados exibidos na interface do usuário no momento da resposta.

**Quais são os recursos do Assistente de IA?**

O Assistente de IA pode resolver consultas de conhecimento de produtos da Adobe e responder a perguntas relacionadas a insights operacionais de seus artefatos operacionais.

**O Assistente de IA pode fornecer informações sobre os dados do cliente?**

Não. O Assistente de IA não tem acesso aos dados do cliente e, portanto, não é visualizado nem usado pelo Assistente de IA.

**Minhas informações pessoais são usadas nos dados de treinamento do Assistente de IA?**

O Assistente de IA não usa informações pessoais para fins de treinamento. Não forneça nenhuma informação pessoal sobre você (incluindo seu nome ou informações de contato) ou qualquer outra pessoa ao Assistente de IA.

## Próximas etapas

Com uma compreensão geral do Assistente de IA, prossiga para ativar e usar o Assistente de IA durante os workflows. Consulte a seguinte documentação para obter mais informações:

* [Habilitar o acesso ao Assistente de IA](./enable-ai-assistant-access.md)
* [Orientação para perguntas](./question-guidance.md)
* [Usar o Assistente de IA](./use-ai-assistant.md)
