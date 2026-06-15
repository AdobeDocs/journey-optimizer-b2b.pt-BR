---
title: Criação de email
description: Use as ferramentas de design de email do Journey Optimizer B2B Prime, incluindo modelos de email, fragmentos, personalização, modo escuro e validação.
autotag-review: '2026-06-12T22:51:19.543Z'
TQID: 'https://experienceleague.adobe.com/-mtyiJ98caCTuTKaZbzYrYKiQoxolq-hMw7p5h7bNpY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: e7bdffdc-2950-4be5-8c23-84240a995090
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 2f4929e4fadeee87b9e31298d2a1de269fc007d5
workflow-type: tm+mt
source-wordcount: 2789
ht-degree: 1%

---

# Criação de email

No [!DNL Adobe Journey Optimizer B2B Prime], o espaço de design de email fornece uma tela visual onde os profissionais de marketing compõem emails. As ferramentas de design de email nos painéis à esquerda e na parte superior (estruturas, componentes de conteúdo, modelos, fragmentos e muito mais) oferecem suporte à criação do zero com arrastar e soltar. Você também pode optar por iniciar com base em um modelo, colar HTML bruto ou reunir mensagens de fragmentos visuais reutilizáveis.

>[!IMPORTANT]
>
>Para obter a configuração do administrador de subdomínios, autenticação, pools de IP e configurações de canal de email, consulte [Entregabilidade de email e configuração de canal](../admin/configuration-email-deliverability.md).

No [!DNL Journey Optimizer B2B Prime], cada email está associado a uma ação _[!UICONTROL Enviar Email]_ em uma jornada. O fluxo de trabalho completo, desde o design da jornada até a definição de email, acontece em uma experiência contínua. Quando você [adicionar um nó _Enviar email_](../marketing/person-journey-nodes.md#add-an-action-node) a uma jornada de pessoa, clique em **[!UICONTROL Criar email]** para iniciar o processo de design de conteúdo de email.

Essa ação inicia o espaço de design de email, onde você pode escolher como deseja criar seu email a partir das seguintes opções:

* [Crie o email do zero](#build-from-scratch) usando a interface de design visual. Crie o componente de layout de email por componente usando a função arrastar e soltar em uma tela em branco. Esse método é melhor para criar novos modelos ou emails únicos.

* Importe o HTML para o editor de código ou trabalhe lado a lado com a tela visual. O fluxo de trabalho completo de importação do HTML com uploads de .html e .zip está no roteiro do Beta.

* [Selecione um modelo existente](#create-from-template) em uma lista de modelos de email predefinidos ou personalizados. Esse método é mais adequado para casos de uso de email repetíveis.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have AI Assitant convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

## Ferramentas de design de email {#email-design-tools}

* **Barra de ferramentas superior:** Salvar, Voltar, Alternar para o editor de código, controles de visualização.
* **Painel esquerdo:** Estruturas (layouts de coluna), Conteúdo (texto, botão, imagem, divisor, social, HTML), Fragmentos, Modelos, Árvore de navegação (hierarquia de estilo DOM do email).
* **Tela do Centro:** editor do WYSIWYG com visualização móvel e de área de trabalho.
* **Painel direito:** configurações e estilos do componente selecionado no momento, incluindo propriedades de conteúdo, plano de fundo, borda, preenchimento e personalização.

## Práticas recomendadas de design de email {#design-best-practices}

Seguir as práticas recomendadas do HTML e do CSS ajuda a garantir a renderização consistente entre os clientes de email.

| Abordagem | Orientação |
| -------- | -------- |
| **Recomendado** | Layouts estáticos baseados em tabela · Tabelas HTML e tabelas aninhadas · Larguras de modelo de 600 a 800 px · CSS simples em linha · Fontes seguras para a Web |
| **Use com cuidado** | Imagens de plano de fundo (suporte limitado ao cliente) · Fontes personalizadas da Web (sempre definir uma fonte de fallback) · Layouts com mais de 800 px · Mapas de imagem |
| **Evitar** | JavaScript, iframes ou Flash · Áudio ou vídeo incorporado · Formulários HTML · Layouts baseados em Div |

>[!NOTE]
>
>O conteúdo do email também deve atender aos requisitos de acessibilidade digital aplicáveis. Cabeçalhos de estrutura logicamente, fornecem texto alternativo para todas as imagens e verificam o contraste de cores nos modos claro e escuro.

## Criar um email a partir de uma jornada {#email-from-journey}

1. Clique no botão **[!UICONTROL Editar email]** para prosseguir para a etapa de configuração de email.
1. Na próxima tela, selecione uma configuração de canal criada anteriormente no menu suspenso **[!UICONTROL Configuração de email]**. Somente as configurações Ativas são listadas.
1. Insira um Rótulo para a ação (visível na tela de jornada) e um Nome de email interno.
1. Insira a linha Assunto.
1. Opcionalmente, alterne **[!UICONTROL Habilitar o rastreamento de URL]** para este nó de email.
1. Clique em **[!UICONTROL Editar conteúdo]** para abrir o espaço de design de email.

### A tela Editar conteúdo {#edit-content-screen}

Nessa tela, você confirma os detalhes do remetente (herdados da configuração do canal), define a linha de assunto e abre o espaço de design de email para criar o corpo. O pré-cabeçalho é configurado no espaço de design de email (consulte [Configuração do pré-cabeçalho](#preheader)).

* **Do Nome, Do Email, Cco:** Herdado da configuração de canal. Somente leitura nesta tela.
* **Linha de assunto:** Necessária. O Personalization é compatível.
* **Editar corpo do email:** Abre o espaço de design de email.

>[!NOTE]
>
>O tamanho do email é limitado a 100 KB por prática recomendada do ISP. O Prime avisa no editor se isso for excedido. Erros (assunto ausente, corpo ausente, configuração de canal excluída) impedem que a jornada seja ativada até que seja resolvida.

## Criação do zero {#design-from-scratch}

### Passo a passo: criar um email do zero {#build-from-scratch}

1. No nó de email da jornada, clique em **[!UICONTROL Editar conteúdo]** → **[!UICONTROL Editar corpo do email]**.
1. Na tela Criar seu email, clique em **[!UICONTROL Criar do zero]**.
1. Clique em **[!UICONTROL Confirmar]** para abrir uma tela em branco.
1. No painel à esquerda, arraste uma **[!UICONTROL Estrutura]** (1-coluna, 1:1, 2:2, n:n coluna) para a tela.
1. Arraste os componentes de **[!UICONTROL Conteúdo]** para as colunas da estrutura: Texto, Botão, Imagem, Divisor, Social, HTML.
1. Clique em qualquer componente na tela para selecioná-lo. O painel direito mostra as guias Configurações e Estilos.
1. Use a guia **[!UICONTROL Configurações]** para configurar as opções específicas do componente (conteúdo do texto, fonte da imagem, URL do botão).
1. Use a guia **[!UICONTROL Estilos]** para configurar o preenchimento, a borda, o plano de fundo, a fonte e a cor.
1. Use o ícone da **[!UICONTROL Árvore de navegação]** no painel esquerdo para saltar entre componentes em um email profundamente aninhado.
1. Alterne entre as visualizações da Área de trabalho e do Mobile usando os ícones na barra de ferramentas superior.
1. Clique em **[!UICONTROL Salvar]** (ou use a lista suspensa Salvar para obter opções de salvamento adicionais).
1. Clique em **[!UICONTROL Voltar]** para retornar às propriedades de email.

### Componentes de conteúdo disponíveis {#content-components}

| Componente | Descrição |
| --------- | ----------- |
| **Texto** | Rich text com formatação (negrito, itálico, tamanho da fonte, cor, alinhamento, listas, links). |
| **Botão** | CTA clicável. Oferece suporte a cor de fundo, borda, preenchimento, comportamento de focalização e URLs personalizados. |
| **Imagem** | Inserir do Marketo Design Studio (seletor de ativos). Suporta texto alternativo, alinhamento, link e rastreamento de cliques. |
| **Divisor** | Régua horizontal com espessura e cor configuráveis. |
| **Social** | Ícones de mídia social pré-estilizados com configuração de link. |
| **HTML** | Bloco bruto de HTML para conteúdo avançado. Útil para incorporar marcação codificada manualmente. |

### Estruturas e layouts de coluna {#structures}

As estruturas definem a grade de colunas do email. As estruturas disponíveis incluem: 1 coluna, 1:1 (duas colunas iguais), 1:2 / 2:1 (duas colunas assimétricas), 1:1:1 (três colunas iguais) e n:n (várias colunas personalizadas). Use estruturas para controlar como o conteúdo flui em dispositivos móveis — a maioria das estruturas é reduzida a uma única coluna em telas estreitas por padrão.

>[!TIP]
>
>Mantenha a estrutura de email simples. Layouts de duas ou três colunas fornecem renderização consistente entre clientes de email (especialmente Outlook e Gmail). Estruturas profundamente aninhadas podem ser renderizadas de forma imprevisível.

### Definição do pré-cabeçalho {#preheader}

O pré-cabeçalho é o trecho de texto exibido após a linha de assunto nas visualizações da caixa de entrada. No Prime, o pré-cabeçalho é configurado na tela visual no espaço de design de email, não na tela de propriedades de email ao lado da linha de assunto.

1. Abra o email no espaço de design de email.
1. Na tela de desenho, localize a área de pré-cabeçalho na parte superior do corpo do email.
1. Clique na região de texto do pré-cabeçalho e insira a cópia do pré-cabeçalho.
1. Aplique tokens de formatação e personalização conforme necessário usando os controles de rich text.
1. Clique em **[!UICONTROL Salvar]**.

>[!TIP]
>
>Mantenha seu pré-cabeçalho entre 40 e 100 caracteres. Ele deve complementar a linha de assunto (não repeti-la) e dar ao recipient um motivo extra para abrir o email.

## Trabalhar com modelos {#templates}

Os modelos são layouts de email reutilizáveis. Eles aceleram a criação de e-mails, reforçam a consistência da marca e facilitam a colaboração em equipe.

### Tipos de modelo {#template-types}

* **Modelos de exemplo (prontos para uso).** Cerca de 20 modelos prontos que abrangem casos de uso comuns (alcance com base em conta, convites para eventos, criação, anúncios de produtos). Disponível imediatamente para todos os clientes.
* **Modelos salvos (personalizados).** Modelos criados pela sua equipe — criados do zero em **[!UICONTROL Gerenciamento de conteúdo]** → **[!UICONTROL Modelos]**, ou salvos de um email existente usando a opção &quot;Salvar como modelo&quot;.

### Criar um email a partir de um modelo {#create-from-template}

1. No nó de email da jornada, clique em **[!UICONTROL Editar conteúdo]** → **[!UICONTROL Editar corpo do email]**.
1. Na tela Criar seu email, a guia **[!UICONTROL Modelos de amostra]** é selecionada por padrão.
1. Navegue pela galeria. Use a caixa de pesquisa para filtrar por nome ou categoria.
1. Alterne para a guia **[!UICONTROL Modelos salvos]** para exibir os modelos criados pela sua equipe.
1. Clique em uma miniatura de modelo para pré-visualizá-la.
1. Clique em **[!UICONTROL Usar este modelo]** para aplicá-lo. O conteúdo do modelo é aberto na tela no espaço de design de email.
1. Personalizar texto, imagens e links. A estrutura herdada do template pode ser modificada como um email do zero.
1. Clique em **[!UICONTROL Salvar]** → **[!UICONTROL Voltar]** para retornar às propriedades de email.

### Criar um modelo reutilizável {#create-reusable-template}

1. Navegue até **[!UICONTROL Gerenciamento de conteúdo]** → **[!UICONTROL Modelos]**.
1. Clique em **[!UICONTROL Criar modelo]**.
1. Insira um nome e uma descrição. Selecione **[!UICONTROL Email]** como canal.
1. Clique em **[!UICONTROL Criar]**. O espaço de design de email é aberto para edição.
1. Crie o modelo (do zero, de um modelo existente ou colando o HTML).
1. Habilitar opcionalmente **[!UICONTROL Configurações de governança]**:
   * Permitir edição de estrutura e conteúdo — controla se os autores de email podem alterar a estrutura do modelo ou somente seu conteúdo.
   * Bloquear componentes específicos — torne os componentes individuais somente leitura quando usados em um email.
1. Clique em **[!UICONTROL Salvar]**. O modelo agora está disponível para todos os usuários na galeria Modelos salvos.

### Salvar um email como modelo {#save-as-template}

1. Abra um email existente no espaço de design de email.
1. No menu suspenso **[!UICONTROL Salvar]**, clique em **[!UICONTROL Salvar como modelo]**.
1. Insira um nome e uma descrição.
1. Opcionalmente, defina as configurações de Governança.
1. Clique em **[!UICONTROL Salvar]**.

>[!NOTE]
>
>Os modelos salvos e seu conteúdo de email são independentes. A edição de um modelo não atualiza retroativamente os emails criados a partir dele. Para propagar alterações em muitos emails, use fragmentos visuais em vez de modelos.

## Fragmentos visuais {#visual-fragments}

Um fragmento visual é um bloco de conteúdo reutilizável — um cabeçalho, rodapé, CTA, aviso legal, conjunto de links sociais — que pode ser inserido em muitos emails. Ao atualizar um fragmento, a alteração se propaga automaticamente para cada email que o utiliza. Os fragmentos são a maneira recomendada de aplicar a consistência da marca e centralizar as atualizações de conteúdo.

### Criar um fragmento visual {#create-fragment}

1. Navegue até **[!UICONTROL Gestão de conteúdo]** → **[!UICONTROL Fragmentos]**.
1. Clique em **[!UICONTROL Criar fragmento]**.
1. Selecione **[!UICONTROL Fragmento visual]** como o tipo. Insira um nome e uma descrição.
1. Clique em **[!UICONTROL Criar]**. O espaço de design de email é aberto para edição.
1. Arraste estruturas e componentes de conteúdo para a tela para criar o fragmento (por exemplo, uma estrutura de uma coluna com uma imagem de logotipo, um cabeçalho e uma lista de links de navegação).
1. (Opcional) Marque os campos como **[!UICONTROL Editáveis]** para torná-los personalizáveis por uso:
   * Selecione um componente e, no painel direito, abra a seção **[!UICONTROL Campos Editáveis]**.
   * Adicione campos com valores padrão (por exemplo, um campo de origem de imagem com um URL de logotipo padrão, um campo de texto com um título padrão).
   * Os autores de email que usam o fragmento podem substituir esses campos sem quebrar a estrutura do fragmento.
1. Clique em **[!UICONTROL Salvar]**.

### Inserir um fragmento em um email {#insert-fragment}

1. Abra o email no espaço de design de email.
1. No painel à esquerda, clique em **[!UICONTROL Fragmentos]**.
1. Procure ou pesquise o fragmento desejado.
1. Arraste o fragmento para a tela de desenho no local desejado.
1. Se o fragmento tiver Campos editáveis, configure os valores no painel direito.
1. Clique em **[!UICONTROL Salvar]**.

>[!TIP]
>
>Use fragmentos para qualquer conteúdo que deve permanecer consistente em todos os emails: o cabeçalho da marca, o rodapé legal, a barra de links sociais e o bloco de cancelamento de inscrição. Quando a equipe jurídica atualiza o aviso de isenção de responsabilidade, você altera um fragmento e cada email é atualizado.

## Personalização {#personalization}

O Prime usa a sintaxe Handlebars para personalização. Os tokens são substituídos no momento do envio por valores dos dados de perfil de cada recipient.

### Onde você pode personalizar {#where-you-can-personalize}

* **Linha de assunto** — ponto de personalização mais comum.
* **Pré-cabeçalho** — definido dentro da tela visual; oferece suporte a tokens de atributos de perfil.
* **Texto do corpo do email** — nomes e outros atributos de perfil inseridos em linha.
* **URLs de Botão** — acrescentar parâmetros por destinatário.

>[!NOTE]
>
>Somente atributos de perfil estão disponíveis no Editor do Personalization nesta versão.

### Inserir um token de personalização {#insert-token}

1. No espaço de design de email (ou na tela de propriedades de email da linha de assunto), clique no campo onde deseja inserir um token.
1. Clique no ícone de personalização (geralmente rotulado como **[!UICONTROL Abrir caixa de diálogo de personalização]** ou **[!UICONTROL Adicionar expressão]**).
1. Na caixa de diálogo de personalização, navegue pela árvore de esquema à esquerda. Os atributos de perfil (nome, sobrenome, email, cargo e outros campos de perfil) são listados.
1. Selecione um atributo. O Prime insere a expressão Handlebars correspondente — por exemplo, `{{profile.firstName}}`.
1. Adicione um valor de fallback para tratar dados ausentes: `{{profile.firstName | default: "there"}}`.
1. Clique em **[!UICONTROL Confirmar]** ou **[!UICONTROL Inserir]**. A expressão aparece em linha no campo.

### Padrões de personalização comuns {#personalization-patterns}

Use expressões Handlebars como a seguir (a personalização usa a mesma sintaxe descrita em [Passo a passo: insira um token de personalização](#insert-token)):

* **`{{profile.lastName}}`** — Inserir o sobrenome do destinatário.
* **`{{profile.jobTitle}}`** — Fazer referência ao título do trabalho do destinatário no corpo do texto.
* **`{{profile.firstName}}, ready to take the next step?`** — Combinar token e texto estático embutido.

Para uma saudação de nome com um fallback quando o valor estiver ausente, use o auxiliar do `default` como mostrado nas etapas de personalização anteriores (por exemplo, nome com padrão `"there"`).

### Handlebars helpers {#handlebars-helpers}

Além de `default`, o editor de personalização inclui auxiliares Handlebars integrados para lógica condicional, transformação de texto e formatação de data. Use o navegador de função do editor para explorar os auxiliares disponíveis e inseri-los com a sintaxe correta.

>[!TIP]
>
>No espaço de design de email, digite `{{` diretamente em qualquer campo de texto para acionar uma lista suspensa de preenchimento automático em linha listando os atributos de perfil disponíveis. Não é necessário abrir a caixa de diálogo de personalização completa para inserções rápidas.

### Expressões assistidas por IA {#ai-personalization}

O Assistente de IA no editor de personalização pode gerar expressões Handlebars a partir de uma descrição em linguagem simples, explicar o que uma expressão existente faz e identificar possíveis problemas. Use-a para acelerar a criação de expressões, especialmente para lógica condicional ou auxiliares de formatação de data.

## Adicionar ativos do Marketo Design Studio {#marketo-assets}

O Prime disponibiliza seus ativos existentes do Marketo Design Studio no espaço de design de email. Você pode navegar e inserir essas imagens em seus emails diretamente do seletor de ativos.

>[!IMPORTANT]
>
>A disponibilidade do ativo no Prime é baseada em uma **cópia única** dos seus ativos do Marketo Design Studio. Recarregar ou modificar ativos no Marketo após a cópia inicial **não** será refletido no Prime. Os uploads de imagem diretamente no Prime também não são compatíveis com esta versão. O gerenciamento de ativos digitais nativos no Prime — incluindo upload, navegação de pastas, pesquisa e edição de imagens — faz parte do escopo do Beta.

### Tipos de arquivo compatíveis {#asset-file-types}

* **Totalmente compatível (visível no seletor, incorporável em linha):** JPG, PNG, GIF, WebP.
* **Acessível com avisos:** SVG (com um aviso de que alguns clientes de email não renderizam o SVG).
* **Não suportado nesta versão:** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, arquivos binários, PSD, AI, INDD.

### Inserir uma imagem do Marketo Design Studio {#insert-image}

1. No espaço de design do email, arraste um componente de conteúdo da **[!UICONTROL Imagem]** para a tela (ou clique em uma imagem existente para substituí-la).
1. No painel direito, clique em **[!UICONTROL Marketo Engage Assets]**.
1. O seletor de ativos é aberto. Procure pastas ou pesquise por nome de arquivo.
1. Selecione o ativo desejado.
1. Clique em **[!UICONTROL Selecionar]**. A imagem é inserida em seu email a partir da cópia do ativo disponível no Prime.
1. No painel direito, configure:
   * Texto alternativo (recomendado para acessibilidade e para clientes que bloqueiam imagens por padrão).
   * Alinhamento.
   * Destino do link — tornar a imagem clicável.
1. Clique em **[!UICONTROL Salvar]**.

## Modo escuro {#dark-mode}

A renderização no modo escuro tem suporte por meio de consultas de mídia `prefers-color-scheme` CSS. As ferramentas de design de email incluem uma pré-visualização no modo escuro e opções para definir o estilo personalizado para clientes de email, ajudando você a validar se o texto permanece legível, se os logotipos são visíveis e se as cores da marca se mantêm contra planos de fundo escuros.

Para obter orientações detalhadas sobre visualização, definição de configurações personalizadas do modo escuro, suporte a clientes de email e práticas recomendadas de teste, consulte [Modo escuro para conteúdo de email](./email-dark-mode.md).

## Validação de conteúdo de email {#validation}

Antes de ativar a jornada, o conteúdo do email deve ser válido. O Prime exibe alertas de nível de conteúdo no email e na tela de jornada. Esta seção aborda os alertas que você pode ver e como resolvê-los.

### Alertas de conteúdo comuns e como resolvê-los {#content-alerts}

| Alerta | O que significa | Como resolver |
| ----- | ------------- | -------------- |
| **Linha de assunto ausente** | O campo Linha de assunto está vazio. | Abra o email e insira uma linha de assunto na tela Editar conteúdo. Os tokens do Personalization são permitidos, mas o campo não pode estar vazio. |
| **O corpo do email está vazio** | A tela no espaço de design de email não tem conteúdo. | Clique em **[!UICONTROL Editar corpo do email]** para abrir o espaço de design de email. Arraste pelo menos uma Estrutura e um componente Conteúdo para a tela e clique em Salvar. |
| **Configuração de canal não selecionada** | Nenhuma configuração de email foi escolhida para o nó de email. | Na tela de propriedades do email, selecione uma configuração de canal ativo na lista suspensa **[!UICONTROL Configuração de email]**. |
| **Configuração de canal excluída** | A configuração de canal selecionada anteriormente foi excluída ou não está mais ativa. | Abra as propriedades de email e selecione outra configuração de canal ativo. Se nenhum estiver disponível, um administrador deverá criar ou reativar um. |
| **O tamanho do email excede 100 KB** | O tamanho total do email (HTML, CSS em linha, conteúdo codificado) é maior que o limite de 100 KB das práticas recomendadas do ISP. | Reduzir o tamanho do email: substitua imagens grandes em linha por imagens hospedadas externamente do Marketo Design Studio, remova o CSS em linha não usado e simplifique as estruturas aninhadas. |
| **Token de personalização não resolvido** | Um token Handlebars faz referência a um atributo de perfil sem fallback e o atributo pode estar ausente para alguns destinatários. | Adicione um fallback usando o auxiliar Handlebars `default`, conforme descrito em [Personalization](#personalization). Como alternativa, restrinja o público-alvo da jornada aos perfis em que o atributo é garantido. |
| **Imagem não carregada** | Um componente de imagem faz referência a um ativo que não está mais disponível. | Clique na imagem, abra o seletor de ativos e selecione novamente o ativo no Marketo Design Studio. |

### Revisar e resolver alertas {#resolve-alerts}

1. Abra a jornada que contém o nó de email. Os nós de email com alertas não resolvidos são sinalizados com um emblema vermelho na tela.
1. Clique no nó email para abrir o painel de propriedades.
1. Revise a seção **[!UICONTROL Alertas]** no painel de propriedades. Cada alerta é vinculado ao campo ou à tela em que o problema pode ser resolvido.
1. Resolva cada alerta individualmente — por exemplo, insira uma linha de assunto ausente, selecione uma configuração de canal ou abra o espaço de design de email para corrigir o conteúdo.
1. Depois de resolver todos os alertas, clique em **[!UICONTROL Salvar]** no nó de email.
1. Confirme se o selo vermelho no nó de email está limpo.

>[!NOTE]
>
>Os alertas devem ser apagados antes que a jornada possa continuar. Os avisos não são bloqueados, mas devem ser revisados (por exemplo, um email que usa um token sem um fallback pode ser renderizado com valores vazios para alguns destinatários).
