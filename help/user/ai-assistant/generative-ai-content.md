---
title: IA gerativa para conteúdo
description: Saiba como criar emails personalizados e páginas de aterrissagem com IA gerativa no  [!DNL Journey Optimizer B2B Edition], incluindo práticas recomendadas de solicitação.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 2%

---

# IA gerativa para conteúdo {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Geração de conteúdo de IA"
>abstract="Depois de criar o layout, você pode usar as ferramentas de IA gerativas no [!DNL Journey Optimizer B2B Edition] para aprimorar o conteúdo. Esse recurso simplifica o processo de personalização e melhoria de conteúdo, ajustando o conteúdo de acordo com seu prompt descritivo."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Conteúdo de referência"
>abstract="Use _Conteúdo de referência_ para carregar um arquivo de ativo com conteúdo que forneça contexto adicional para a IA gerativa em [!DNL Journey Optimizer B2B Edition], ou para selecionar um arquivo carregado anteriormente. Essa opção garante que todos os materiais necessários estejam disponíveis para aprimorar a qualidade e a relevância do conteúdo gerado."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Termos de IA gerativa do Adobe"
>abstract="O acesso a esse recurso está sujeito à concordância com as Diretrizes do usuário da IA generativa da Adobe Experience Cloud. Revise qualquer saída desse recurso para precisão e verifique se ele é apropriado para seu caso de uso."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Diretrizes do usuário da IA generativa da Adobe"

A IA gerativa para conteúdo no [!DNL Adobe Journey Optimizer B2B Edition], viabilizada pelo Microsoft Azure OpenAI e pelo Adobe Firefly, fornece sugestões de variação de conteúdo proativa para texto e imagens. Otimize o impacto do conteúdo fazendo experiências com diferentes títulos e imagens principais.

Use os recursos de IA gerativa para criação de conteúdo no [!DNL Journey Optimizer B2B Edition] para aproveitar os recursos de IA gerativa da Adobe. Crie texto e visuais personalizados para emails, mensagens SMS, páginas de aterrissagem e muito mais. Ao criar uma campanha completa ou simplesmente refinar ativos específicos, esses recursos ajudam você a alinhar o conteúdo perfeitamente às diretrizes da sua marca, economizando tempo valioso.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Para acessar esses recursos em [!DNL Journey Optimizer B2B Edition], você deve ter a permissão _[!UICONTROL Assistente de IA]_ > _[!UICONTROL Gerar conteúdo]_. Para obter mais informações sobre como um administrador de produto pode conceder permissões de recursos, consulte [Editar funções para permissões de produto](../admin/user-management.md#edit-roles-for-product-permissions).

As ferramentas do Assistente de IA para geração de conteúdo são compatíveis com os seguintes tipos de ativos:

* [Emails](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Landing pages](../content/ai-assistant-landing-pages.md)

## Orientações gerais e limitações {#general-guidelines-and-limitations}

Seu uso de recursos de IA gerativa está sujeito às [Diretrizes de usuário da IA gerativa da Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Com o compromisso da Adobe com a transparência no uso de ferramentas de IA gerativa para criação de mídia, a Adobe aplica [credenciais de conteúdo](https://helpx.adobe.com/br/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} para qualquer conteúdo ou projeto que inclua um ativo gerado por [!DNL Firefly] quando ele for baixado ou exportado.

Revise estas diretrizes gerais para o uso da IA gerativa para conteúdo no [!DNL Journey Optimizer B2B Edition]:

* Use prompts bem definidos para que o modelo de IA gerativa seja interpretado com precisão. O objetivo de marketing ou o prompt fornecido afeta fortemente a qualidade do conteúdo gerado.

* Faça upload de arquivos de referência de conteúdo para ter conteúdo preciso sobre a marca. Caso contrário, o conteúdo será baseado em informações disponíveis publicamente. O conteúdo carregado pode estar nos seguintes formatos de arquivo: PDF, JPEG, PNG ou ZIP (contendo formatos de arquivo compatíveis). O tamanho máximo de um arquivo carregado é de 50 MB. Arquivos maiores ou um grande número de imagens podem funcionar, mas isso aumenta o tempo de processamento.

* Use um modelo específico da marca ou personalizado para criar seu conteúdo de email. São recomendados modelos de e-mail com até 8 a 10 imagens.

* Relate quaisquer saídas problemáticas usando a miniatura para cima, a miniatura para baixo ou os ícones de sinalizador ao selecionar variantes.

## Solicitar práticas recomendadas para IA gerativa {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Orientações do prompt"
>abstract="Explore a documentação do [!DNL Journey Optimizer B2B Edition] para saber como criar prompts efetivos que produzam conteúdo de marketing de alta conversão e sob a marca."

Este guia ajuda a estruturar suas solicitações, comunicar a intenção com clareza e garantir que a IA produza mensagens que se alinhem às diretrizes da sua marca, às necessidades do público-alvo e às metas da campanha.

Saiba como escrever prompts eficazes que permitem que o AI Assistant gere conteúdo de marketing de alta qualidade e sob marca, adaptado aos seus objetivos.

### Usar a estrutura CO-STAR {#costar-framework}

Para obter melhores resultados com o conteúdo gerado, organize seus prompts usando a estrutura CO-STAR. Essa abordagem estruturada fornece clareza exatamente para o que você precisa.

| Componente | O que significa | Por que isso importa |
| --- | ---- | ------ |
| **C - Contexto** | Histórico de sua campanha, produto ou situação | Fornece compreensão para uma visão geral |
| **O - Objetivo** | Sua meta de marketing específica | Orienta o que o conteúdo deve alcançar |
| **S - Estilo** | Como você deseja se comunicar | Define a abordagem |
| **T - Tom** | Estilo emocional e voz | Forma como a mensagem é exibida |
| **A - Público** | O público-alvo que você está direcionando | Garante que a mensagem repercuta com as pessoas certas |
| **R - Requisitos** | Restrições específicas ou must-haves | Define limites e elementos críticos |

{style="table-layout:fixed"}

### Noções básicas de solicitação {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Fazer</th>
<th>Não</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Usar a estrutura CO-STAR para a estrutura
<li>Seja explícito sobre conteúdo novo ou existente
<li>Fornecer foco para o uso do documento com orientação específica de extração
<li>Fazer seleções de tom, estratégia e localidade
<li>Combinar objetivos de marketing com recursos de tipo de conteúdo
<li>Gerar várias variantes para teste A/B</ul>
</td>
<td>
<ul><li>Solicitar alterações estruturais, estilo ou edição de imagem em prompts
<li>Mencionar tom/estratégia em prompts, se disponível nas opções
<li>Use objetivos vagos como _promover o produto_
<li>Solicitar seleções de elementos condicionais
<li>Esperar modificações de layout por meio de prompts</ul>
</td>
</tr>
</tbody>
</table>

### Conteúdo não suportado em prompts

>[!TIP]
>
>Use as ferramentas de design ou o [!DNL Adobe Express] para modificações visuais/de imagem.

As seguintes solicitações **_não têm suporte_** e devem ser tratadas por outras ferramentas:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz vermelha">  Modificações na estrutura de email</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz vermelha">  Alterações no estilo visual</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz vermelha">  Operações de edição de imagens</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selecionar seções específicas para alterar</li>
<li>Exclusão ou clonagem de elementos</li>
<li>Seleções condicionais</li>
<li>Adição ou remoção de seções de layout</li>
</ul>
</td>
<td>
<ul>
<li>Formatação de texto (negrito, itálico, tamanho da fonte)</li>
<li>Modificações de cores</li>
<li>Estilo de layout (bordas, preenchimento, margens)</li>
<li>Efeitos visuais (sombras)</li>
</ul>
</td>
<td>
<ul>
<li>Alterações de fundo</li>
<li>Adicionar sobreposições de texto ou logotipos</li>
<li>Recorte ou redimensionamento de imagem</li>
<li>Ajustes de cor</li>
<li>Substituição de imagem</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista de verificação de qualidade {#quality-checklist}

Antes de gerar o conteúdo, verifique o seguinte:

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Limpar objetivo**: indica claramente a ação, o produto/serviço, o valor e o contexto.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Público-alvo definido**: especifica a demografia, a função ou o segmento.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Alinhamento do tipo de conteúdo**: o objetivo corresponde ao canal ou formato selecionado.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Revisar seleções**: o tom, a estratégia e a localidade são escolhidos, não os inclua no prompt.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **O foco do documento está especificado**: realça qual conteúdo ou seções serão referenciados.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Marca aplicada**: as diretrizes de marca adequadas estão selecionadas.

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Escopo realista**: evitar solicitações de alterações de layout, estilo ou edições estruturais.

### Objetivos eficazes de marketing {#marketing-objectives}

Ao criar objetivos de marketing, verifique se eles são claros, acionáveis e mensuráveis. Evite declarações vagas ou genéricas.

**Exemplos de bons objetivos:**

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Inscreva-se na unidade para a avaliação gratuita de 30 dias do novo painel de análise alimentado por IA&quot;

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Gerar clientes em potencial para o webinário B2B sobre como &#39;Reduzir os custos da nuvem em 40%&#39; a partir de 15 de março&quot;

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promover o desconto de tempo limitado de 25% em assinaturas premium, até 25 de dezembro&quot;

**Exemplos a serem evitados:**

![Cruz vermelha](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promover o produto&quot; (muito vago)

![Cruz vermelha](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Fazer com que as pessoas assinem acordos&quot; (valor não claro)

![Cruz vermelha](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Email sobre novos recursos&quot; (sem finalidade)

#### Estruturar o objetivo

Sempre forneça contexto e a proposta de valor para produzir conteúdo relevante. Use a seguinte fórmula para ajudá-lo a escrever objetivos efetivos: **Ação + Produto/Serviço + Valor/Benefício + Urgência/Contexto**

**Exemplos de bons objetivos:**

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Incentive os downloads do novo aplicativo móvel que ajuda os usuários a rastrear hábitos de vida sustentáveis com recomendações personalizadas e ecológicas&quot;

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promova o registro para o workshop exclusivo sobre técnicas avançadas de visualização de dados para profissionais de marketing&quot;

![Marca de seleção verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promova a participação no evento de lançamento do produto apresentando o revolucionário assistente de escrita de IA que economiza mais de 5 horas por semana&quot;

**Exemplos a serem evitados:**

![Cruz vermelha](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Anunciar novo aplicativo&quot; (proposta de valor e contexto ausentes)

![Riscar o vermelho](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Fazer com que as pessoas se inscrevam para o workshop&quot; (carece de especificidade sobre público-alvo e benefícios)

![Cruz vermelha](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promover evento&quot; (sem ação, valor ou urgência claros)

#### Exemplo de prompts por tipo de canal {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Email</strong></td>
<td>"Crie prospetos de empresas apresentando três histórias de sucesso de clientes com métricas detalhadas de ROI (Oracle: 45% de redução de custos, Accenture: 200% de aumento de lead, Microsoft: 60% de economia de tempo). Direcionem os diretores de TI para empresas com mais de 1.000 funcionários"</td>
</tr>
<tr>
<td><strong>Páginas de destino</strong></td>
<td>"Converta visitantes B2B em clientes potenciais qualificados demonstrando como a solução de segurança corporativa impede 99,9% dos ataques cibernéticos, com declarações da Fortune 500 e auditoria de segurança gratuita"</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Novo conteúdo versus modificação de conteúdo existente {#new-vs-modify}

Indique claramente se a sua solicitação envolve a geração de novo conteúdo ou a atualização de material existente. Esta distinção é importante porque orienta a IA na seleção da abordagem adequada e garante um resultado mais preciso e útil.

#### Criação de novo conteúdo

Aplique esta estratégia quando estiver lançando campanhas de marketing, revelando novas soluções ou iniciando uma comunicação atualizada/atualizada. Ela garante que sua mensagem comece forte e se alinhe às suas metas.

**Como avisar** ➤ Ao criar um novo conteúdo, concentre-se no seu objetivo de marketing sem fazer referência ao conteúdo existente.

>[!BEGINSHADEBOX &quot;Exemplos&quot;]

* **Avaliação do SaaS**: &quot;Inicie o novo software CRM para proprietários de pequenas empresas, destacando 50% de economia de tempo, qualificação de cliente potencial 90% mais rápida e oferecendo uma avaliação gratuita de 30 dias com integração personalizada&quot;
* **Anúncio de recursos**: &quot;Anuncie novos recursos de integração de API que reduzem o tempo de desenvolvimento em 60% para clientes corporativos, direcionando tomadores de decisão técnicos&quot;
* **Promoção de eventos**: &quot;Impulsione inscrições para o webinário sobre &quot;Tendências de marketing digital 2024&quot;, com especialistas da Google, Meta e Adobe, enfatizando insights acionáveis e vagas limitadas (500 no máximo)&quot;

>[!ENDSHADEBOX]

#### Modificação de conteúdo existente

>[!TIP]
>
>Para modificações padrão, como elaborar, resumir ou simplificar, selecione **_Refinar_** em vez de escrever prompts personalizados.

Use um prompt de modificação quando precisar atualizar ou adaptar suas campanhas de marketing atuais. Esse método oferece suporte a melhorias incrementais, garantindo que suas mensagens permaneçam relevantes sem iniciar do zero.

**Como avisar** ➤ Ao modificar conteúdo existente, especifique claramente o que deseja alterar e como alterá-lo.

>[!BEGINSHADEBOX &quot;Exemplos&quot;]

* **Atualização da campanha**: &quot;Modifique o email de inicialização do programa para se concentrar nos recursos de segurança da empresa em vez dos benefícios gerais de produtividade, direcionando os tomadores de decisão de TI com certificações de conformidade&quot;
* **Tabela dinâmica de público-alvo**: &quot;Adapte o convite de demonstração de software para direcionar especificamente a área de saúde, substituindo exemplos genéricos por casos de uso da área de saúde e benefícios de conformidade com a HIPAA&quot;
* **Atualização da temporada**: &quot;Atualize a campanha promocional do 3º trimestre para compras de fim de ano do 4º trimestre, mudando o foco das ofertas escolares para as ofertas de fim de ano, com ênfase no envio rápido&quot;

>[!ENDSHADEBOX]

## Configurações avançadas de texto {#text-settings}

Além de usar um prompt claro e bem formado, as configurações de texto nas ferramentas de conteúdo do Assistente do AI incluem configurações de texto que você pode usar para otimizar as saídas geradas.

>[!TIP]
>
>Use as opções _[!UICONTROL Estratégia de comunicação]_ e _[!UICONTROL Tom]_ nas _[!UICONTROL Configurações de texto]_ em vez de mencionar essas características no prompt.

### Tipos de estratégia de comunicação

A estratégia de comunicação determina como você apresenta a mensagem para maximizar o impacto. Estratégias diferentes funcionam melhor para metas diferentes, seja para criar urgência, estabelecer confiança ou promover ação imediata. Escolha a estratégia que melhor se alinha aos objetivos da campanha e à mentalidade do público-alvo.

| **Estratégia** | **Recomendado para** | **Estilo de mensagem** | **Exemplos** |
| ------------ | ------------ | ------------------- | ------------ |
| **Urgente** | Ofertas sensíveis ao tempo, prazos e ação imediata | Cria pressão imediata com linguagem baseada no tempo | <li>&quot;Atue agora: a oferta expira à meia-noite&quot; <li>&quot;Inscreva-se hoje mesmo antes que as vagas se encham&quot; <li>&quot;A venda rápida de 48 horas começa agora&quot; |
| **FOMO (Medo de ficar de fora)** | Ofertas limitadas, eventos, acesso exclusivo | Usa dicas de urgência, escassez e pressão de tempo | <li>&quot;Só faltam 24 horas! Estoque limitado com 40% de desconto&quot; <li>&quot;Última chance: o preço antecipado dos pássaros termina amanhã&quot; <li>&quot;Restam apenas 100 pontos beta&quot; |
| **Prova social** | Construção de confiança, testemunhos, produtos populares | Aproveita as experiências e a validação de outras pessoas | <li>&quot;Junte-se a mais de 50.000 clientes satisfeitos&quot; <li>&quot;Classificados como 4,9/5 estrelas por profissionais do setor&quot; <li>&quot;Confiável para empresas da Fortune 500&quot; |
| **Escassez** | Inventário limitado, versões exclusivas, itens de alta demanda | Enfatiza disponibilidade limitada e exclusividade | <li>&quot;Restam apenas 5 em estoque&quot; <li>&quot;Edição limitada: 100 unidades disponíveis&quot; <li>&quot;Lançamento exclusivo: primeiro a chegar, primeiro a ser servido&quot; |
| **Incentivo** | Promoções, programas de recompensa, ofertas especiais | Destaca benefícios e recompensas tangíveis | <li>&quot;Obtenha 20% de desconto em seu primeiro pedido&quot; <li>&quot;Ganhe pontos duplos neste fim de semana&quot; <li>&quot;Frete gratuito em pedidos acima de US$ 50&quot; |
| **Exclusividade** | Produtos Premium, experiências VIP, ofertas somente para membros | Usa posicionamento premium e linguagem de acesso especial | <li>&quot;Convite exclusivo para visualização privada&quot; <li>&quot;A associação Elite desbloqueia análises avançadas&quot; <li>&quot;Junte-se a algumas empresas da Fortune 500 que já nos usam&quot; |
| **Gamification** | Campanhas de engajamento, programas de fidelidade, conteúdo interativo | Usa mecânica de jogos e linguagem de realização | <li>&quot;Desbloquear o próximo nível de recompensa&quot; <li>&quot;Desafios completos para ganhar medalhas&quot; <li>&quot;Suba na tabela de classificação por prêmios exclusivos&quot; |
| **Informativo** | Educação, pesquisa, produtos complexos, liderança de pensamento | Usa fatos, dados, insights e explicações | <li>&quot;5 insights da análise de mais de 10.000 interações&quot; <li>&quot;Novas pesquisas revelam três abordagens inovadoras&quot; <li>&quot;Guia completo para a implementação de IA no marketing&quot; |
| **Educação e Insights** | Conteúdo de aprendizado, tendências do setor, práticas recomendadas | Fornece conhecimentos valiosos e argumentos acionáveis | <li>&quot;Conheça técnicas avançadas com um guia especializado&quot; <li>&quot;Descubra 7 estratégias que os principais profissionais de marketing usam&quot; <li>&quot;Saiba como otimizar seu fluxo de trabalho em 5 etapas&quot; |

### Definir o tom correto {#tone}

O tom molda como o público-alvo percebe e responde à mensagem. Sempre selecione um tom que se alinhe à voz da sua marca e ao estágio da jornada do perfil.

Revise as opções de tom disponíveis, incluindo quando cada uma funciona melhor e exemplos de conteúdo que se ajustam a cada estilo.

| Tonalidade | Melhor para | Exemplo de conteúdo |
| ---- | ----- | ----- |
| Profissional | Comunicações B2B, anúncios formais | &quot;Temos o prazer de anunciar nossa parceria estratégica...&quot; |
| Empático | Suporte ao cliente, tópicos confidenciais | &quot;Entendemos o quanto essa questão deve ser frustrante para você...&quot; |
| Humorístico | Campanhas envolventes, conteúdo alegre | &quot;Aviso: pode causar sérios ganhos de produtividade!&quot; |
| Emocionante | Lançamentos de produtos, promoções de eventos | &quot;Este é o momento pelo qual vocês estavam esperando!&quot; |
| Inspirador | Campanhas motivacionais, finalidade da marca | &quot;Juntos, podemos fazer a diferença no mundo...&quot; |
| Persuasivo | Campanhas de vendas, conversões | &quot;Não perca essa oportunidade de tempo limitado para...&quot; |
| Amigável | Engajamento do cliente, mensagens de boas-vindas | &quot;Que bom que você está aqui conosco!&quot; |
| Formal | Comunicações legais, avisos oficiais | &quot;Esta é uma notificação das seguintes alterações...&quot; |
| Pedidos de desculpas | Recuperação de serviço, resolução de problemas | &quot;Bodea sinceramente pede desculpas por qualquer inconveniente causado...&quot; |
| Assertivo | Conteúdo de liderança, mensagens autoritativas | &quot;Aqui está o que você precisa fazer agora...&quot; |
| Contar histórias | Narrativas de marca, conexões emocionais | &quot;Tudo começou com uma pergunta simples...&quot; |
| Conversação | Campanhas de incentivo, construção de relacionamentos | &quot;Vamos falar sobre como este programa pode ajudá-lo...&quot; |

## Conteúdo de referência otimizado {#reference-content}

>[!TIP]
>
>Se você já tiver carregado um ativo por meio do menu **[!UICONTROL Referenciar conteúdo]**, não será necessário referenciá-lo no prompt. O sistema usa automaticamente todos os documentos selecionados.

Os arquivos de conteúdo de referência fornecem informações fatuais que enriquecem o conteúdo gerado com detalhes específicos e precisos. Ao fazer upload de documentos, como folhetos de produtos ou white papers, altere o aviso para incluir quais partes terão foco:

* **Em vez de** _&quot;Usar o folheto de produto&quot;_ **usar** _&quot;Concentrar-se nos recursos avançados de segurança e certificações de conformidade, especificamente conformidade SOC 2 e criptografia de dados&quot;_

* **Em vez de** _&quot;Consultar os estudos de caso&quot;_ **usar** _&quot;Destacar resultados de ROI de clientes da área de saúde, especificamente a redução de 40% no Centro Médico Regional&quot;_

* **Em vez de** _&quot;Incluir detalhes técnicos&quot;_ **você deve usar** _&quot;Enfatizar os recursos de integração de API e os benefícios do desenvolvedor, concentrando-se nos pontos de extremidade da API REST e no SLA com 99,9% de tempo de atividade&quot;_

### Refinamento de conteúdo

Depois que o conteúdo for gerado, use o recurso **_[!UICONTROL Refinar]_** para iterar e aprimorar com as seguintes opções:

* **[!UICONTROL Elaborar]** - O Assistente de IA pode ajudá-lo a expandir tópicos específicos, fornecendo detalhes adicionais para melhor compreensão e engajamento.

* **[!UICONTROL Resumir]** - Informações extensas podem sobrecarregar os visualizadores da página. Use o Assistente de IA para condensar os pontos principais em resumos claros e concisos que chamem a atenção e os incentivem a ler mais.

* **[!UICONTROL Refrase]** - Reescreva a mensagem preservando seu significado. Essa opção ajuda a gerar texto alternativo, melhorar o fluxo ou ajustar o estilo sem alterar a mensagem principal.

* **[!UICONTROL Usar linguagem mais simples]** - Simplifique a linguagem, garantindo clareza e acessibilidade para um público-alvo maior.

* **[!UICONTROL Traduzir]** - Traduza o texto para outro idioma. (Atualmente, o único idioma suportado é o inglês.)

* **[!UICONTROL Alterar tom]** - Ajuste o tom da mensagem para alinhá-la ao seu estilo de comunicação, tornando-a mais amigável, profissional, urgente ou inspiradora.

* **[!UICONTROL Alterar estratégia de comunicação]** - Modifique a abordagem de mensagens com base em seus objetivos, como criar urgência ou enfatizar um apelo interessante.
