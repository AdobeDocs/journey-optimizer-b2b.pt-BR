---
applyTo: "**/*.md"
source-git-commit: 0f90b37c1ed8e4da0840f64179a0e99e0fe786d7
workflow-type: tm+mt
source-wordcount: '5174'
ht-degree: 1%
---

# Documentação da Adobe Experience League: Instruções do código Claude

Você está ajudando um autor técnico no repositório de documentação pública da Adobe Experience League (`journey-optimizer-b2b.en`). Cada parte do conteúdo que você rascunha, edita ou revisa DEVE seguir todas as regras abaixo. Em caso de dúvida sobre a terminologia, consulte os wikis referenciados usando a ferramenta Confluence MCP (`mcp__adobe-wiki-confluence`).

---

## &#x200B;1. Voz, tom e estilo

### Escrita focada no usuário

Centralize o usuário, não o recurso. Escreva o que o usuário pode **fazer**, não o que o recurso faz.

- Use a segunda pessoa (&quot;você&quot;) e o humor imperativo para obter instruções.
- Use &quot;você&quot; quando falar com o público sobre si mesmos, não &quot;usuários&quot;. &quot;Usuários&quot; é aceitável ao se referir a uma função (por exemplo, um administrador que gerencia usuários).
- EVITE &quot;O recurso X permite que você...&quot; ou &quot;O recurso X permite que você...&quot;. Coloque o usuário como assunto ou use o humor imperativo.
  - Incorreto: &quot;A API do servidor pode ser usada em servidores.&quot;
  - Bom: &quot;Usar a API do servidor em servidores&quot;.
  - Ruim: &quot;Campos calculados permitem a criação de valores...&quot;
  - Bom: &quot;usar campos calculados para criar valores...&quot;
- Considere o &quot;você pode&quot;. É apropriado, mas pode ser usado em excesso, criando frases repetitivas ou com palavras.
- Use &quot;selecionar&quot; para escolher as opções de uma lista ou para destacar o texto. Use &quot;clique&quot; somente para ações explícitas do mouse. Evite nomear o tipo de controle (botão, link), a menos que seja necessário para desambiguação.
- Use &quot;Abrir&quot; / &quot;Fechar&quot; para aplicativos e janelas ou painéis principais.
- Use &quot;Sair&quot; para sair de um site ou experiência (por exemplo, &quot;Sair do Report Builder&quot;).
- Use &quot;ir para&quot; ou &quot;navegar para&quot; para navegação.
- Use &quot;Reproduzir vídeo&quot;, não &quot;Assistir vídeo&quot;. Nem todo mundo está assistindo.
- Use &quot;Exibir&quot;, &quot;Mostrar&quot; ou &quot;Ir para todos&quot;, e não &quot;Ver todos&quot;. Nem todo mundo está vendo.
- Use &quot;entrar&quot; / &quot;sair&quot;, não &quot;entrar&quot; / &quot;sair&quot;.
- Evite &quot;a fim de&quot;. Em vez disso, use &quot;para&quot;.
- Evite &quot;utilizar&quot;. Em vez disso, use &quot;use&quot;.
- Evite adjetivos vagos como &quot;rápido&quot; ou &quot;fácil&quot;. Seja preciso: &quot;Esse processo geralmente leva 5 minutos.&quot;
- Evite advérbios fracos: muito, extremamente, incrivelmente.

### Estrutura de frase e parágrafo

- Meta ≤ 20 palavras por frase (o guia de criação diz ≤35 no máximo). Um pensamento por frase.
- Parágrafos: máx. 125 palavras, idealmente ≤100. Máximo de 4 a 5 frases. Sem paredes de texto.
- Use a voz ativa. Evite construções e nomeações passivas (por exemplo, use &quot;criar&quot; e não &quot;criação&quot;).
- Use estrutura simples de sujeito-verbo-objeto.
- Evite assuntos falsos (&quot;É...&quot;, &quot;Há...&quot;).
- Use a mesma palavra de maneira consistente. Não gire sinônimos.
- Não há exemplos específicos de humor, gíria, jargão ou cultura (deve se localizar bem).
- Use a vírgula de Oxford em listas de três ou mais itens.
- Soletre números inteiros de zero a nove; use numerais para 10 e acima.
- Sem ponto e vírgula. Em vez disso, use um ponto final e uma nova frase.

### Scannability

- Os leitores devem compreender o escopo do artigo somente a partir do título, dos cabeçalhos e das legendas.
- Máximo de 2 a 5 subseções por seção.
- Direcione 7 etapas por tarefa; 10 é o máximo prático. Divida procedimentos mais longos em subtarefas.
- Máximo de 8 itens por lista com marcadores.
- Use tabelas quando elas facilitarem a verificação das listas de termos/definições.
- O conteúdo deve pontuar abaixo do grau 10 em um teste de legibilidade (após a remoção de substantivos e títulos adequados).

### Gravação para descoberta de IA

Os assistentes de IA e as ferramentas de pesquisa exibem cada vez mais o conteúdo do Experience League nas respostas geradas.

- Coloque os termos principais (nomes de produtos, nomes de recursos, tarefas) no corpo de texto e no texto do link, não apenas em imagens ou tabelas complexas. Os sistemas de IA dependem de texto legível.
- Escreva cabeçalhos e primeiros parágrafos claros e independentes. As ferramentas de IA muitas vezes as extraem isoladamente; elas devem fazer sentido sem contextos circundantes.
- Mantenha as frases curtas e diretas. A prosa concisa é mais fácil para a IA analisar e citar com precisão.
- Use formatos estruturados (etapas numeradas, marcadores curtos, cabeçalhos de estilo de definição) para procedimentos e comparações. A estrutura ajuda a IA a identificar a resposta correta.
- Inclua sinônimos ou termos alternativos na primeira utilização (por exemplo, &quot;ECID (Experience Cloud ID)&quot;) para melhorar a recuperação de formulações de consulta variadas.
- Verifique se os campos de metadados (título, descrição, tags de recursos) estão completos e precisos.

---

## &#x200B;2. Sintaxe do Adobe Markdown (Experience League)

### Frontmatter (obrigatório em todos os arquivos)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

Campos opcionais adicionais usados neste repositório: `solution`, `type`, `role`, `exl-id`. Corresponder ao padrão dos arquivos existentes.

**IMPORTANTE:** NÃO adicione `exl-id` ao criar uma nova página. Ele é gerado automaticamente no momento da publicação. Apenas `exl-id` campos que já existem em páginas existentes devem ser preservados.

**Regras de metadados de título:**

- Letras maiúsculas e minúsculas (somente no Experience League que usa letras maiúsculas).
- Máximo de 60 caracteres (inglês). O sistema anexa `| Adobe Experience Platform` automaticamente. Considere isso em comprimento.
- NÃO adicione o pipe ou o nome do produto. Ele é adicionado automaticamente.
- Pense nisso como a versão SEO do nome da sua página (o que os usuários procuram).
- Título do conceito: frase substantiva (por exemplo, &quot;Relatório de exibições de página&quot;).
- Título da tarefa: frase verbal (por exemplo, &quot;Criar um segmento para exibições de página&quot;).
- Os acrônimos não são aprovados pelo Marketing para a maioria dos usos, mas o uso limitado é aceitável para SEO, entradas de índice, metadados de descrição e cabeçalhos nos quais o comprimento é uma preocupação.

**Regras de metadados de descrição:**

- Primeira letra da frase em maiúscula. Idealmente, 150 a 160 caracteres; máximo de 160.
- Uma a duas frases concisas. A primeira frase resume; a segunda é uma call to action.
- Comece as descrições de conceito com &quot;Saiba mais sobre...&quot; ou &quot;Entenda...&quot;.
- Inicie as descrições de tarefa com &quot;Saiba como...&quot; ou um verbo imperativo.
- NÃO comece com o nome do produto. Comece com um verbo para SEO.
- NÃO copie o texto do primeiro parágrafo (com outra finalidade).
- Se um campo de metadados começar com uma marca `[!DNL]` ou ``, coloque todo o valor do campo entre aspas ou a validação falhará.

### Cabeçalhos

- `#` = H1 (título do artigo, um por página). `##` = seções principais H2. `###` = H3, etc.
- NÃO ignore os níveis de cabeçalho (por exemplo, não pule de H2 para H4).
- Meta ≤ 5 palavras. Máximo de 69 caracteres (inglês).
- Linha em branco antes E depois de cada cabeçalho.
- Cada cabeçalho deve ser seguido de, pelo menos, uma frase do corpo do texto. NUNCA empilhe dois cabeçalhos ou coloque uma nota, lista ou tabela diretamente sob um cabeçalho sem um parágrafo primeiro.
- IDs de âncora personalizadas: `## Section title {#section-id}` (minúsculas, hifenizadas, sem pontos).
- Evite nomes de âncora que entrem em conflito com o JavaScript/CSS: pesquisa, resultados, conteúdo, cabeçalho, rodapé, navegação, barra lateral, paginação etc.
- NÃO coloque selos ou elementos de Markdown dentro do texto do cabeçalho.
- NÃO use cabeçalhos abstratos de palavra única como &quot;Visão geral&quot; ou &quot;Introdução&quot; isoladamente. Sempre descreva a visão geral ou a introdução.
- NÃO numere H1s. Para tutoriais, use &quot;Etapa 1: ...&quot; em subtítulos em vez de âncoras numeradas.
- Primeira letra da frase para todos os cabeçalhos (exceto substantivos próprios e elementos da interface).
- Títulos de conceito: substantivos e frases substantivas (por exemplo, &quot;Visão geral da segmentação&quot;).
- Cabeçalhos de tarefas: verbos imperativos (por exemplo, &quot;Criar um fluxo de trabalho de direcionamento&quot;). Evite gerúndios (-ing formas).
- Evite enumerar verbos com -ment ou -ion (use &quot;Criar um roteiro&quot; e não &quot;Criação de roteiro&quot;).
- Mantenha a estrutura de cabeçalho paralela dentro das seções.
- Nenhuma ID de âncora de cabeçalho duplicada em um documento.
- Se um cabeçalho incluir numerais, especifique uma ID de cabeçalho explícita que não comece com um número (por exemplo, `## Release notes for 2016 {#release-notes-2016}`).

### Links

- Referências cruzadas internas: caminhos relativos à raiz começando com `/help/`: `[link text](/help/path/to/file.md)`
- Deep links para âncoras: `[text](/help/path/to/file.md#anchor-id)`
- Links externos (fora deste repositório): `https://` URLs absolutas. Elas são abertas em uma nova guia automaticamente.
- Abrir explicitamente em nova guia: anexar `{target="_blank"}` (usar para links entre guias).
- Links de referência (usando o estilo `[1]: url`): funcionam somente com URLs absolutas.
- NÃO adicione o mesmo arquivo várias vezes em um índice.
- Evite URLs brutos no corpo de texto. Sempre use texto de link descritivo.
- Nunca use &quot;clique aqui&quot; ou &quot;link&quot; como texto de link. Os leitores de tela exibem links fora do contexto e não podem distinguir várias instâncias de &quot;clique aqui&quot;.
- O texto do link deve deixar o destino claro por conta própria.
- Para listas de referência cruzada &quot;Mais informações&quot;, use um subtítulo `More help on this topic` com uma lista com marcadores.

### Imagens

- Sintaxe: `![alt text](path/to/image.png)`
- Redimensionar: `{width="300"}` ou `{width="50%"}`
- Alinhar: `{align="center"}` ou `{align="right"}`
- Zoom: `{zoomable="yes"}`
- Exibição modal: `{modal="regular"}`. NÃO combine com um link.
- Largura recomendada: 640 a 2000 px. Tamanho máximo do arquivo: 5 MB recomendado; limite rígido de 100 MB. Máximo de 100 imagens por artigo.
- As imagens ficam em uma subpasta `assets/` relativa ao arquivo Markdown.
- Imagens que NÃO devem ser localizadas ficam em uma subpasta `do-not-localize/`.
- Sempre capture capturas de tela usando o tema **Leve** na interface do usuário do produto Experience Cloud, não o tema Escuro.
- NÃO mostrar os dados do cliente em capturas de tela.
- NÃO documente interfaces de terceiros em capturas de tela. Em vez disso, vincule à documentação do próprio fornecedor.
- NÃO use capturas de tela apenas para rastrear o progresso pelas telas ou mostrar elementos óbvios da interface do usuário.
- NÃO inclua ilustrações de ícones facilmente identificáveis mais de uma vez por artigo.
- NÃO use imagens de código. Em vez disso, use blocos de código.
- NÃO use cores isoladamente para transmitir informações (não acessíveis a usuários daltônicos).
- NÃO use gráficos animados que piscam mais de três vezes por segundo (risco de captura).
- Verifique se as imagens têm bom contraste e estão nítidas.
- Diretrizes de tamanho do pixel da captura de tela: 2000 px máx para grande, 672 px para médio, 300 px para pequeno e 30-35 px para ícones.
- Para chamadas de retorno: use HEX #EB1000 vermelho, espessura de linha de 3 px, raio de canto de 8 px.

### Texto alternativo

O texto alternativo é indexado pelo Google e lido por leitores de tela. Sempre escreva com cuidado.

- Descreva o que a imagem mostra, não apenas o nome da tela.
- Use frases completas com gramática e pontuação adequadas.
- Inclua texto relevante da imagem.
- Use palavras completas, não abreviações. Os leitores de tela escrevem abreviações.
- NÃO comece com &quot;Esta imagem mostra...&quot;. Apenas descreva o conteúdo diretamente.
- O texto alternativo geralmente não é necessário para imagens meramente decorativas, mas o fornece quando em dúvida.

| Bom texto alternativo | Evitar |
|---|---|
| Captura de tela do Construtor de público-alvo mostrando os filtros demográficos geográficos e de idade selecionados. | Construtor de público-alvo |
| Selecione uma extensão no catálogo de extensões. | Biblioteca de extensões |

### Vídeos

- Sintaxe: `>[!VIDEO](https://video.tv.adobe.com/v/xxxxx/?quality=12&learn=on)`
- Adicione `?quality=12&learn=on` ao final de todas as URLs de vídeo para obter a melhor reprodução.
- Os vídeos NÃO devem ser reproduzidos automaticamente. Não adicione `?autoplay=true` na documentação.
- Sempre forneça uma alternativa em texto, transcrição ou link para instruções escritas: &quot;Para obter instruções escritas, consulte [link].&quot;
- Use legendas relevantes.
- Habilite transcrições com `{transcript=true}` em vídeos individuais ou adicione `auto-video-transcripts: true` a `TOC.md` para um guia inteiro.

### Observações e recomendações

```markdown
>[!NOTE]
>
>Note content here.

>[!TIP]
>
>Tip content here.

>[!IMPORTANT]
>
>Important content here.

>[!WARNING]
>
>Warning content here.

>[!CAUTION]
>
>Caution content here.
```

Tipos adicionais: `[!ADMIN]`, `[!AVAILABILITY]`, `[!PREREQUISITES]`, `[!INFO]`, `[!ERROR]`, `[!SUCCESS]`.

Regras de sintaxe CRÍTICA:
- Deve haver uma linha `>` em branco entre a linha da marca e o conteúdo.
- Toda linha de continuação deve começar com `>`.
- A sintaxe de citação de bloqueio (`>` sem uma marca ) é suportada, mas é renderizada como uma citação de bloqueio simples. NÃO o use esperando chamadas de estilo.
- NÃO adicione comentários dentro de componentes de bloco, como listas de marcadores, especialmente listas de marcadores aninhadas. O comentário pode alterar a renderização da lista.

### Guias

```markdown
>[!BEGINTABS]

>[!TAB Tab label]

Tab content here.

>[!TAB Another tab]

More content.

>[!ENDTABS]
```

- NÃO aninhe conjuntos de guias.
- NÃO aninhe conjuntos de guias em listas.
- Os títulos das tabulações não podem ser formatados com negrito ou itálico.
- A pesquisa na página (Ctrl+F) não encontra conteúdo em guias ocultas.

### Seções flexíveis

```markdown
+++Click to expand
Content here.

* Bullet one
* Bullet two

+++
```

- Adicione linhas em branco acima e abaixo de listas e blocos de código dentro de recolhíveis.
- NÃO aninhe seções que podem ser recolhidas dentro de seções que podem ser recolhidas.
- Cabeçalhos dentro de recolhíveis são permitidos, mas não recomendados.
- Observação: Localizar na página (Ctrl+F) detecta texto recolhido no Chrome, mas não no Safari.

### Sombrear caixas

```markdown
>[!BEGINSHADEBOX "Optional Title"]

Content with gray background.

>[!ENDSHADEBOX]
```

### Blocos de código

- Inline: backticks simples `` `code` ``. Use para nomes de cookies, nomes de arquivos, valores, parâmetros, comandos e URLs de amostra que não devem ser validados.
- Blocos cercados: três backticks com identificador de linguagem (permite o realce da sintaxe e um botão Copiar).
- Atributos opcionais: `{line-numbers="true"}`, `{start-line="7"}`, `{highlight="11-13, 16"}`
- Os blocos de código NÃO estão localizados. Não é necessário adicionar DNL ou UICONTROL dentro deles.
- Use acentos graves (não aspas) para código, nomes de arquivo, parâmetros e texto digitado.
- NÃO use imagens de código. Sempre use blocos de código.

### Medalhas

- Em linha: `[!BADGE Beta]{type=Informative}`
- Metadados (acima de H1): `badgePremium: label="Premium" type="Positive"`
- Tipos: `Informative` (azul), `Positive` (verde), `Negative` (vermelho), `Neutral` (cinza escuro), `Caution` (amarelo)
- Máximo de 2 selos em metadados por artigo.
- NÃO coloque medalhas em cabeçalhos.
- NÃO use selos para informações que se tornam rapidamente obsoletas (por exemplo, &quot;Novo&quot;).
- Os rótulos de selo estão localizados. Mantenha-os concisos.
- Para o selo beta, use somente o frontmatter `badgeBeta`. NÃO coloque um emblema em linha no H1.
- Se quiser que uma URL de selo seja aberta em uma nova guia, adicione `newtab=true` à sintaxe do selo.

### Listas

- Use `*` ou `-` consistentemente em um único artigo. Verifique a convenção do arquivo existente. A mistura de marcadores causa um erro de validação.
- Para listas numeradas, use `1.` para cada item. O GitHub/EDS os numera automaticamente corretamente.
- Listas de marcadores: quando a ordem não é importante. Listas numeradas: para etapas e procedimentos ordenados.
- Para um procedimento de etapa única, use um marcador (`*`) em vez de `1.`.
- Mantenha as entradas da lista breves. Normalmente uma frase ou menos.
- Use pontos para frases completas; omita pontos para entradas de palavra única ou frase incompleta (aplique a regra consistentemente em uma lista).
- NÃO termine os itens da lista com ponto e vírgula, vírgula ou conjunção como &quot;e&quot; ou &quot;ou&quot; quando os itens forem lidos como uma série simples.
- Todas as entradas da lista devem ser gramaticalmente paralelas.
- Recuar conteúdo aninhado: 3 espaços para listas numeradas, 2 para listas de itens.
- Listas surround com linhas em branco.
- NÃO use listas de tarefas (caixas de seleção `- [ ]` estilo GitHub). Eles não são compatíveis com o Experience League.

### Tabelas

- Use tabelas de markdown padrão.
- Para layouts complexos (células mescladas, bordas desligadas), o HTML `<table>` é permitido.
- Circundar tabelas com linhas em branco.
- Use `{style="table-layout:auto"}` para tabelas de largura automática quando necessário.
- Evite capturas de tela em células da tabela. Pequenos ícones ou miniaturas são aceitáveis em células.

### Visualizar destaque de recursos

Use um span para conteúdo de visualização em linha e um div para conteúdo de visualização de vários parágrafos:

```markdown
<span class="preview">This feature is in limited availability.</span>
```

```markdown
<div class="preview">

Multiple paragraphs of preview content here.

</div>
```

### Trechos e inclusões

```markdown
{{$include /path/to/snippet.md}}
```

Use para blocos de conteúdo reutilizáveis compartilhados em vários artigos.

### Caracteres especiais

- Evite caracteres especiais no corpo de texto com uma barra invertida: `\#`, `\*`, `\[`, `\]`.
- Use entidades HTML para colchetes angulares: `&lt;`, `&gt;`, `&amp;`.
- Use entidades HTML para símbolos especiais: `&reg;`, `&mdash;`, `&ndash;`.

### Comentários

Usar comentários do HTML para rascunho de texto ou notas para outros autores:

```markdown
<!-- This is a comment. Not rendered in the published doc. -->
```

Os comentários ESTÃO visíveis para usuários editando em GitHub.com. NÃO inclua informações confidenciais nos comentários.

NÃO adicione comentários dentro de componentes de bloco como listas de itens (especialmente aninhadas). Os comentários podem quebrar a lista de renderização. Nos arquivos TOC.md, não comente linhas no meio da lista do TOC; em vez disso, mova os comentários para o final do arquivo.

### Ações do teclado

Coloque cada tecla em negrito em um atalho de teclado: **cmd** + **shift** + **p**.

### Nomeação de arquivos e pastas

- Nomes de arquivo do Markdown: minúsculas com hifens. Sem maiúsculas, sublinhados, pontos ou espaços.
- Usar lesmas descritivas: `create-calculated-metric.md`, `calculated-metric-overview.md`. Evite nomes de arquivo simples como `overview.md` ou `introduction.md`, a menos que o IA exija um nome fixo.
- Evite nomes de arquivo que entrem em conflito com JavaScript/CSS: `metadata.md`, `search.md`.
- Nomes de arquivo do ativo: preferencial minúsculas; letras maiúsculas e sublinhados permitidos, mas não recomendados.

---

## &#x200B;3. Tags de localização (CRÍTICAS)

Sempre aplique tags de localização. A tradução automática é executada automaticamente em cada confirmação no principal.

### `[!DNL Product Name]`: Não Localizar

Use para nomes de produtos de marca que devem permanecer em inglês.

**Aplicar a:**
- Nomes de produtos da Adobe: `[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`, `[!DNL Experience Platform]`
- Nomes de produtos de terceiros: `[!DNL Mozilla Firefox]`, `[!DNL Workfront]`
- Nomes funcionais que podem confundir a tradução: `[!DNL Pass]`, `[!DNL Campaign]`
- Operadores booleanos usados como termos lógicos: `[!DNL AND]`, `[!DNL OR]`

**NÃO aplicar a:**
- URLs, nomes de arquivo ou nomes de diretório
- Blocos de código (não localizados por padrão)
- Acrônimos (ficar em inglês automaticamente)
- Termos já existentes no banco de dados Não traduzir

**No texto do link:** Remova os colchetes para evitar problemas de renderização. Use `[Adobe](https://www.adobe.com)` não `[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: Controles de Interface do Usuário

Use para elementos de interface: opções, campos, guias, páginas, menus, botões e nomes de recursos conforme aparecem na interface do. Essa é a tag mais importante para a qualidade da tradução. Trate-o como obrigatório em procedimentos.

**Aplicar a:**
- Todos os elementos da interface do usuário clicáveis nas etapas de procedimento (obrigatório)
- Nomes de recursos e elementos de navegação conforme mostrado no produto
- Nomes de página, opções, campos e guias conforme rotulados na interface

**Formatação:**
- Negrito nas etapas e na navegação: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Itálico aceitável em texto conceitual (sem etapa) para maior clareza.
- Nas tabelas do HTML: use `<span class="uicontrol">term</span>` em vez de ``.
- No texto do link: remova os colchetes da tag.

**Capitalização:** Corresponda exatamente à interface.

**NÃO aplicar a:**
- Termos genéricos usados conceitualmente: &quot;segment&quot;, &quot;metric&quot;, &quot;campaign&quot; (somente tag ao fazer referência explícita ao elemento da interface)
- Frases longas (a menos que o próprio nome do elemento da interface do usuário seja uma frase longa)
- Blocos de código ou acrônicos
- Descrições dos ícones. Use o nome do cursor/dica de ferramenta do ícone, se disponível; não marque descrições genéricas como &quot;ícone de lápis&quot;

### `[!DONOTLOCALIZE]`: Excluir seções inteiras

Quebrar conteúdo que deve permanecer em inglês em todas as localidades:

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Não necessário dentro de blocos de código. Elas não estão localizadas por padrão.

### Onde as tags podem e não podem ser usadas

**Pode ser usado em:** parágrafos, listas, cabeçalhos, tabelas, selos, texto alternativo e metadados.

**Não pode ser usado em:** blocos de código, siglas.

**Regra de metadados:** se um campo de metadados (título ou descrição) começar com uma marca `[!DNL]` ou ``, coloque todo o valor do campo entre aspas ou a validação falhará.

---

## &#x200B;4. Estrutura de informações e tipos de conteúdo

### Três tipos de conteúdo: mantenha-os separados

- **Conceito**: o que e por quê. Apresentações, visões gerais e histórico. Use cabeçalhos de substantivo/frase-substantiva.
- **Tarefa**: Como. Procedimentos passo a passo. Use cabeçalhos de verbos imperativos. Sempre precedido por um conceito.
- **Referência**: campos, parâmetros, opções, códigos de erro. Use tabelas. Recolher com outro material de referência.

### Estrutura do artigo

- Abra o com um contexto conceitual que oriente o leitor.
- Em seguida, vá para tarefas e, em seguida, material de referência.
- Responda uma pergunta focada por página. Não muito largo, não muito estreito.
- Página de conceito com páginas de tarefa filho (várias páginas), OU conceito H1 + subtítulos de tarefa H2 (página única).
- Apresente sinônimos ou nomes antigos uma vez (por exemplo, &quot;ECID (Experience Cloud ID)&quot;) para conectar termos de pesquisa.

### Etapas

- Cada etapa é um único comando: uma frase completa com um ponto (ou dois pontos, se introduzir uma sublista).
- As etapas sempre começam com um verbo ou uma meta antes da ação: &quot;Para executar o relatório, selecione Executar&quot;.
- Combine pequenas ações que ocorrem no mesmo local na interface do usuário em uma única etapa quando a frase permanece clara.
- Direcione 7 etapas por tarefa; 10 é o máximo prático. Divida tarefas mais longas em subtarefas.
- Use um único marcador (não `1.`) para um procedimento que tenha apenas uma etapa.
- NÃO use cabeçalhos como etapas na documentação do produto. Para tutoriais longos de várias páginas, use os subtítulos de estilo &quot;Etapa 1: ...&quot; quando necessário.
- Coloque as informações da etapa (texto explicativo) recuadas em uma nova linha após a etapa.
- Coloque capturas de tela recuadas após a etapa ou ação que faz com que a tela apareça.
- Repita nomes de página, guia ou painel em etapas para que os leitores saibam onde estão.

### Arquivos do índice (TOC.md)

- Primeira letra maiúscula para todas as entradas (exceto substantivos próprios e elementos da interface).
- Entradas de conceito: substantivos e frases substantivas.
- Entradas de tarefa: verbos imperativos (não gerúndios).
- Mantenha as entradas paralelas.
- Cada cabeçalho de seção no índice deve ter uma ID de âncora válida: `+ Processing rules {#processing-rules}`
- Um cabeçalho de seção (principal) no índice não pode ser um link. Ele deve ter uma ID de âncora.
- NÃO adicione o mesmo arquivo várias vezes em um índice.
- NÃO comente as linhas no meio de uma lista do sumário. Mover comentários para o final do arquivo.

### Ocultar arquivos da navegação

Use o **método V2** para todos os trabalhos novos. O método V1 está obsoleto.

**V2 (atual): `{hide-from-toc}` no TOC.md**

Coloque `{hide-from-toc}` diretamente em `TOC.md` antes do artigo ou da seção que você deseja ocultar. NÃO o adicione ao primeiro plano do artigo.

```
+ {hide-from-toc} [Article title](filename.md)
+ {hide-from-toc} Section name {#section-id}
  + [Nested article](nested.md)
```

- Os artigos ocultos permanecem acessíveis por meio do URL direto.
- Uma seção cujas entradas estão todas ocultas desaparecerá da navegação à esquerda.

**V1 (obsoleto): `hidefromtoc: yes` no front-matter**

```yaml
hidefromtoc: yes
```

NÃO use isso em páginas novas. O artigo ainda deve ser exibido em `TOC.md` para publicação, mas não será exibido na navegação à esquerda.

**Ocultando dos mecanismos de pesquisa: `hide: yes` no frontmatter**

```yaml
hide: yes
```

Isso exclui a página da pesquisa externa e interna. A configuração `hide: yes` define `index: no` automaticamente. Use isso além de `{hide-from-toc}` quando quiser que uma página seja ocultada da navegação e da pesquisa.

---

## &#x200B;5. Terminologia e marca

Fonte autoritativa: [wiki de Terminologia Voltada para o Usuário do AEP](https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology). Sempre consulte a ferramenta Confluence MCP (`mcp__adobe-wiki-confluence`) para obter a versão mais recente.

### Nomes de produtos

Sempre use essas formas exatas. Inclua &quot;Adobe&quot; na primeira referência em um guia; você pode soltá-lo em menções subsequentes, quando a política permitir.

NÃO inclua &quot;o&quot; antes dos nomes dos produtos, a menos que o nome oficial o inclua.
- Correto: &quot;Introdução ao Assistente de IA.&quot;
- Incorreto: &quot;Introdução ao Assistente de IA.&quot;

| Correto | NUNCA usar |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (referência secundária) | Plataforma (sozinha, a menos que o contexto não seja ambíguo) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secundário) | Real-time CDP (&quot;t&quot; em minúsculas) |
| Adobe Real-Time Customer Data Platform | — |
| Perfil do cliente em tempo real | Perfil do cliente em tempo real, Perfil unificado |
| Adobe Journey Optimizer | AJO |
| Adobe Journey Optimizer B2B Edition | AJO B2B |
| Prime B2B Adobe Journey Optimizer | Prime B2B AJO |
| Adobe Marketo Optimizer | AMO |
| Adobe Marketo Engage | Marketo (pode ser usado como adjetivo) |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secundário) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Conexões do Adobe Real-Time CDP | Conexões do RTCDP, Conexões do AEP, Conexões (sozinhas) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tags (nome do produto) | Launch (desaprovado) |
| Gestão de decisões | Offer Decisioning (somente entre parênteses: &quot;anteriormente Offer Decisioning&quot;) |
| sequência de dados (uma palavra, minúsculas) | sequência de dados, configuração de borda |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsoleto) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

**&quot;Tempo real&quot;** sempre usa R maiúsculo e T maiúsculo quando faz parte de um nome de produto (Real-Time CDP, Perfil do cliente em tempo real, Real-Time Customer Data Platform).

**Edições**: &quot;edições&quot; são genericamente em minúsculas; &quot;Edição&quot; é capitalizado como parte de um nome de edição de produto (por exemplo, &quot;Adobe Real-Time CDP B2C Edition&quot;).

**Abreviações em comunicações externas**: NÃO abreviar nomes de produtos na documentação voltada para o usuário. Não há AEP, CJA, AJO ou RTCDP nos documentos. Exceções limitadas: os acrônimos podem aparecer entre parênteses na primeira utilização quando auxiliam o SEO, ou em entradas do índice, metadados de descrição e cabeçalhos nos quais o comprimento é uma preocupação.

### Terminologia de recurso e conceito

| Correto | NÃO usar |
|---|---|
| encaminhamento de eventos | encaminhamento pelo lado do servidor, Launch Server Side |
| incluir na lista de permissões | lista de permissões |
| INCLUIR NA LISTA DE BLOQUEIOS / INCLUIR NA LISTA DE BLOQUEIOS | blacklist |
| primário / réplica OU primário / secundário (servidores) | master / slave |
| principal (ramificação GitHub) | master |
| hacker ético | hacker de chapéu branco |
| remarketing | redirecionamento |
| grupo de campos | mixin (obsoleto), Extensões, Mixins |
| expiração automática de dados | TTL, tempo de vida útil, expiração |
| sandbox de não produção | preparo (como um nome de ambiente) |
| definição de segmento | segmento (sozinho, quando significa a definição) |
| ID (sempre usar maiúsculas) | ID |
| assimilação / assimilação / assimilado | integração (para adicionar dados à Platform) |
| conjunto de dados/conjuntos de dados | Arquivo de dados, arquivos de conjunto de dados |
| controle de acesso | permissões (para o recurso Plataforma) |
| widget | cartão métrico (obsoleto) |
| variável de espaço reservado | variável fictícia |
| indisponível / bloqueado / desativado / desativado | esmaecido |
| verificação de coerência | verificação de sanidade |
| incorporado | nativo (como sinônimo de interno) |
| alta prioridade | unha imperfeita |
| legacy | cláusula avô |
| principal / principal / origem | principal (como descritor) |

**Capitalização específica do Analytics:**
- Os nomes dos painéis são em minúsculas: em branco, atribuição, experimentação, forma livre (exceção: &quot;Tela de Jornada&quot;)
- Os nomes da visualização são em minúsculas: barra, rosca, histograma, linha, mapa de árvore, texto

### Termos exclusivos internos: NUNCA use em documentos voltados para o público

Estes termos aparecem em Jira, wikis e discussões internas, mas nunca devem aparecer na documentação:

| Termo interno | Use no lugar dele |
|---|---|
| AEP | Adobe Experience Platform |
| PALMA | gerenciamento de sandbox/controle de acesso |
| BIOMA | ambiente |
| Hidratação / hidratação | criar/preencher |
| Perfil unificado | Perfil do cliente em tempo real |
| Preparo (ambiente) | sandbox de não produção |
| DTM | Tags |
| Locatário | Organização/organização IMS |
| CRUD | criar, ler, atualizar e excluir (soletrar) |
| Siphon, BSO, Ethos | nomes de código internos, nunca externos |
| Lúpulo | GDPR interno/termo de controle de acesso |
| Ritmo | termo de publicidade não voltada para o usuário |
| Canal de processamento | termo da infraestrutura interna do Adobe |

---

## &#x200B;6. Idioma inclusivo e acessibilidade

### Princípios linguísticos inclusivos

- Use termos neutros em termos de gênero: &quot;representante de vendas&quot; não &quot;vendedor&quot;, &quot;moderador&quot; não &quot;presidente&quot;.
- Prefira uma segunda pessoa (&quot;você&quot;) para evitar pronomes de gênero.
- Use &quot;eles&quot; no singular para uma pessoa cujo gênero é desconhecido. NÃO utilize ele/ela ou ele/ela.
- Inclua nomes de culturas não brancas em exemplos (por exemplo, Ayesha, Ibrahim, Vignesh, Quynh). NÃO use apenas nomes culturalmente brancos (John, Bill, Karen, Amy).
- NÃO confunda sexo (masculino/feminino) com gênero (homem/mulher).
- Capitalize nacionalidades, povos, raças (diferentes de &quot;brancas&quot;, de acordo com o AP Stylebook) e tribos.
- Use a linguagem de uma pessoa: &quot;pessoas que usam tecnologia assistiva&quot;, não &quot;os deficientes&quot;.
- Evite eufemismos como &quot;deficientes de forma diferente&quot;. Evite descritores usados como substantivos: &quot;o cego&quot;, &quot;o surdo&quot;.
- Evite termos que reflitam a identidade (apropriação cultural): animal espiritual, Sherpa, pow wow, guru, ninja, tribo.

### Terminologia não inclusiva a ser evitada

| Usar | Não |
|---|---|
| INCLUIR NA LISTA DE PERMISSÕES / INCLUIR NA LISTA DE BLOQUEIOS / INCLUIR NA LISTA DE BLOQUEIOS | lista de permissões/lista negra |
| primário / réplica OU primário / secundário | master / slave |
| principal (ramificação git) | master |
| alta prioridade | unha imperfeita |
| variável de espaço reservado | variável fictícia |
| indisponível / bloqueado / desativado / desativado | esmaecido |
| verificação de coerência | verificação de sanidade |
| incorporado | nativo (como sinônimo) |
| autoridade/especialista | guru / ninja |
| membros do seu grupo | membros da sua tribo |
| reunião | pow wow / circular os vagões |
| modelo de papel / espírito parente | espírito animal |
| guia | Sherpa |
| legacy | cláusula avô |
| empreendimento fútil | março da morte |
| ridículo / incompetente / imprevisível | idiota / manco / louco |
| hacker ético / antiético | chapéu branco / hacker chapéu preto |
| Reproduzir vídeo | Assistir ao vídeo |
| Exibir / Mostrar / Ir para todos | Ver tudo |

### Acessibilidade: descrição da interface

NÃO descreva os elementos da interface do usuário por cor ou posição da tela. A cor não funciona para usuários daltônicos ou leitores de tela. A posição da tela não é confiável com tecnologias assistivas.

**Usar linguagem cronológica, não linguagem espacial:**

| Usar | Não |
|---|---|
| Primeiro, Próximo, Finalmente | Acima, Abaixo |
| Na barra de menus | À esquerda |
| Antes / Depois | Na parte superior/inferior da tela |

**Descreva o que os controles fazem, não como eles são:**

| Usar | Não |
|---|---|
| Selecionar pesquisa | Clique no ícone de lupa |
| Editar | O ícone de lápis |
| Ligado / Desligado | Alternar / alternar / ativar |
| Menu | Gaveta lateral |
| Inserir e-mail | Digite seu endereço de email |
| Salvar | O botão &quot;Salvar&quot; |
| Cancelar | Fechar |

NÃO use cores sozinhas para transmitir informações. Sempre emparelhar cor com texto ou forma.

### Acessibilidade: texto alternativo

- Descreva o que a imagem mostra, não apenas o nome da tela.
- Use frases completas com gramática e pontuação adequadas.
- Inclua texto relevante da imagem.
- Use palavras completas, não abreviações. Os leitores de tela escrevem abreviações em voz alta.
- As imagens que transmitem informações independentemente do texto ao redor DEVEM ter texto alternativo.
- Imagens meramente decorativas podem omitir texto alternativo, mas é uma boa prática incluí-lo.
- Testar imagens com um simulador de daltonismo quando a cor é usada para transmitir significado.
- NÃO use gráficos animados que piscam mais de três vezes por segundo (risco de captura).

### Acessibilidade: links

- Nunca use &quot;clique aqui&quot; ou &quot;link&quot; como texto de link.
- Deixar o destino claro apenas a partir do texto do link.
  - Bom: &quot;consulte os pré-requisitos do RTCDP no Guia do usuário do RTCDP&quot;.
  - Ruim: &quot;Clique aqui para obter os pré-requisitos&quot;.

### Acessibilidade: vídeos

- Os vídeos NÃO devem ser reproduzidos automaticamente.
- Sempre forneça uma alternativa em texto, transcrição ou link para instruções escritas.
- Inclua legendas relevantes em todos os vídeos.
- Quando possível, vincule a instruções escritas: &quot;Para obter instruções escritas, consulte [link].&quot;

---

## &#x200B;7. Ortografia e pontuação

### Ortografia do inglês americano

| Usar | Não |
|---|---|
| cor | cor |
| reconhecer | reconhecer |
| licença | licença |
| enquanto | enquanto |
| expiração | expiração |
| medidor | medidor |
| entre | entre |

### Regras de pontuação

- As aspas de fechamento saem de vírgulas e pontos.
- Aspas de reserva para citar pessoas. Não coloque aspas nas sequências da interface do usuário (use UICONTROL e negrito nas etapas).
- Use itálico para termos usados como termos (não aspas): *perfil*, não &quot;perfil&quot;.
- Use acentos graves para código, parâmetros, nomes de arquivo e texto digitado: `datasetId`.
- Negrito: somente para elementos da interface em procedimentos (com UICONTROL) e termos principais na primeira introdução. As linhas de lead em negrito são aceitáveis nos layouts de Perguntas frequentes que não usam perguntas no nível do cabeçalho.
- Itálico: para ênfase, palavras estrangeiras, termos que estão sendo definidos ou nomes conceituais em texto sem etapas.
- Negrito + itálico combinados: `***text***`.
- NÃO use regras horizontais (`---` ou `***`). Eles não são compatíveis com o Experience League.
- NÃO use travessões (—), travessões (-) ou hifens em prosa. Reescreva a frase em vez disso. Os hifens são permitidos somente em adjetivos compostos que aparecem na interface do usuário, nomes de arquivo e código.
- Dois pontos: use para introduzir uma lista. Use letra maiúscula na primeira palavra após os dois pontos quando uma frase inteira for seguida (ou a palavra for um substantivo adequado).
- Sem ponto e vírgula. Em vez disso, use um ponto final e uma nova frase.

---

## &#x200B;8. SEO e Findability

- Incluir termos de pesquisa (palavras-chave) nos primeiros parágrafos.
- Use termos que os leitores realmente pesquisam. Inclua sinônimos e nomes de termos anteriores, quando útil.
- Palavras-chave nos cabeçalhos: inclui nomes de recursos, elementos de interface e a tarefa que está sendo executada.
- O texto alternativo em imagens é indexado pelo Google. Torne-o descritivo e significativo.
- Evite colocar termos essenciais somente em tabelas ou imagens complexas (não indexadas de forma confiável por IA ou pesquisa).
- Metadados da descrição: use a linguagem natural com palavras-chave. NÃO use palavras-chave aleatórias. O Google pode rebaixar conteúdo para palavras-chave.
- Mantenha os campos de metadados (título, descrição, tags de recursos) completos e precisos — as superfícies de descoberta usam metadados para filtrar e classificar os resultados antes de ler o conteúdo da página.

---

## &#x200B;9. Convenções de arquivo e repositório

- O Frontmatter é necessário em cada arquivo `.md`.
- As imagens ficam em uma subpasta `assets/` relativa ao arquivo Markdown.
- Imagens que não devem ser localizadas ficam em uma subpasta `do-not-localize/`.
- Os arquivos de índice (`TOC.md`) definem a estrutura de navegação à esquerda. Atualize-as ao adicionar ou remover páginas.
- Use links relativos à raiz (`/help/...`) para referências cruzadas entre documentos neste repositório.
- Para links para documentos fora deste repositório, use URLs `https://experienceleague.adobe.com/...` absolutas.
- Nomeação da ramificação: nenhum prefixo de nome de usuário. Use o número do tíquete Jira e uma descrição em caixa de título (por exemplo, `PLAT-12345-Update-Guardrail-Limits`). Nomeie a ramificação e o título da PR usando o mesmo formato.
- Os componentes discretos (cabeçalhos, blocos de código cercados, listas) devem estar entre linhas em branco.
- Somente um H1 (`#`) por documento. A primeira linha após o material de frente deve ser o H1.

---

## &#x200B;10. Revisar lista de verificação

Ao revisar ou editar a documentação, verifique cada item abaixo.

**Voz e estilo**

- [ ] Voz focada no usuário. Nenhum &quot;permite&quot;, &quot;permite&quot;
- [ ] &quot;você&quot; usou em vez de &quot;usuários&quot; ao endereçar o público diretamente
- [ ] Segunda pessoa e humor imperativo em procedimentos
- [ ] Voz ativa durante todo o
- [ ] Alvo das frases ≤ 20 palavras
- [ ] Sem adjetivos vagos (&quot;rápido&quot;, &quot;fácil&quot;). Substituir por descrições precisas.
- [ ] Os termos principais aparecem no corpo de texto (não somente em imagens ou tabelas) para a descoberta de IA

**Estrutura e cabeçalhos**
- [ ] Cabeçalhos: primeira letra maiúscula, ≤5 palavras / 69 caracteres, seguido de corpo de texto, sem cabeçalhos empilhados
- [ ] Nenhum nível de cabeçalho ignorado
- [ ] Os títulos de conceito são frases substantivas; os títulos de tarefa são verbos imperativos
- [ ] Etapas do Target 7 por tarefa; máx. 10. Os procedimentos de etapa única usam um marcador, não `1.`
- [ ] Máximo de 8 itens por lista com marcadores

**Terminologia**
- [ ] Corrija os nomes e formulários de produtos (Seção 5)
- [ ] Nenhum termo obsoleto: mixin, TTL, Offer Decisioning, Launch, Perfil unificado, Tempo real (t minúsculo), Sensei
- [ ] Nenhum termo interno: AEP, PALM, BIOME, hidrato, preparo, DTM, locatário, pipeline
- [ ] Nenhum termo não inclusivo: whitelist, blacklist, master/slave, sanity check, fictício, esmaecido, nativo, guru, ninja, espírito animal, Sherpa, marcha da morte, pow wow, tribo
- [ ] Não &quot;o&quot; antes dos nomes de produtos (por exemplo, não &quot;o Adobe Experience Platform&quot;)

**Marcas de localização**
- [ ] `` em todos os nomes de elementos da interface do usuário; negrito nas etapas
- [ ] `[!DNL]` em todos os nomes de produtos e terceiros
- [ ] operadores booleanos marcados: `[!DNL AND]`, `[!DNL OR]`
- [ ] Nenhuma marca dentro dos blocos de código
- [ ] campos de metadados que começam com uma marca são colocados entre aspas

**Sintaxe de Markdown**
- [ ] Sintaxe de advertência correta (linha `>` em branco entre a marca e o conteúdo)
- [ As listas ] usam marcadores consistentes; as listas numeradas usam `1.` para cada item
- [ ] Nenhuma lista de tarefas (`- [ ]`)
- [ ] Nenhuma regra horizontal (`---` entre o conteúdo)
- [ ] Linhas em branco envolvendo cabeçalhos, blocos de código, listas e tabelas
- [ ] Nenhuma imagem de código. Use blocos de código.
- [ As capturas de tela do ] usam o tema claro; sem dados do cliente; sem interface de terceiros

**Acessibilidade**
- [ ] Texto alternativo: frases completas, palavras completas, descreve o conteúdo (não apenas o nome da tela)
- [ ] Sem linguagem direcional/espacial: sem &quot;acima&quot;, &quot;abaixo&quot;, &quot;à esquerda&quot;, &quot;no canto superior direito&quot;
- [ ] O texto do link descreve o destino. Não clicar aqui
- [ ] Vídeos não definidos para reprodução automática; transcrições ou alternativas escritas fornecidas
- [ ] Nenhuma cor usada sozinha para transmitir informações

**Arquivos e links**

- [ ] Formatação necessária: título (primeira letra maiúscula, ≤60 caracteres), descrição (150 a 160 caracteres)
- [ ] Não há URLs vazias no corpo de texto. Sempre use texto de link descritivo.
- [ ] Links internos relativos à raiz; links absolutos para referências entre repositórios
- [ ] Os nomes de arquivo estão em minúsculas com hifens; descrição em slugs (não desnuda `overview.md`)
- [ ] Imagens em `assets/`; imagens não localizadas em `do-not-localize/`

---

## &#x200B;11. Referências externas

Use a ferramenta MCP correta com base no tipo de recurso:

- **Tíquetes e problemas do Jira** (`jira.corp.adobe.com`): usar a ferramenta Corp Jira MCP (`mcp__corp-jira`)
- **Wiki/Páginas de Confluência** (`wiki.corp.adobe.com`): usar a ferramenta Confluence MCP (`mcp__adobe-wiki-confluence`)
- **Experience League público/páginas da Web**: usar WebFetch

**Páginas wiki internas (use a ferramenta Confluence MCP):**
- **Wiki de terminologia**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology
- **Guia de estilo da plataforma**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1938986972/Platform+style+guide
- **Guia de acessibilidade e inclusão**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2234798784/Writing+for+accessibility+and+inclusivity
- **Guia de janelas flutuantes de ajuda contextual**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2575057078/How+to+add+contextual+help+popovers+to+the+Experience+Platform+documentation+and+UI

**Público (use WebFetch):**
- **Visão geral da localização**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localization-overview
- **Referência das marcas de localização**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localize
- **Sintaxe de Markdown do Experience League**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/markdown-syntax
- **Folha de características do Markdown**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/cheatsheet
- **Referência de estilo das notas de versão**: https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest

**Clone local:**
- **Repositório do guia de criação:** use um check-out disponível do guia de criação da Adobe Experience League ou de sua documentação pública.
