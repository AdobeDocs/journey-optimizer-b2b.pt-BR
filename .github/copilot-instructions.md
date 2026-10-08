---
source-git-commit: 1b4d8ad802265b537eb09439cfe34b97a3e61448
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%
---
# Instruções do repositório do GitHub Copilot

Quando a orientação geral nas instruções de Claude copiadas entrar em conflito com as convenções específicas do repositório ou instruções específicas da tarefa, siga as instruções específicas do repositório ou da tarefa.

## Finalidade

Use estas instruções do repositório para o trabalho de documentação neste repositório. Mantenha as edições concisas, tecnicamente precisas e alinhadas aos padrões de documentação da Adobe Experience League.

## Escrever no estilo de documentação do repositório

- Prefira um idioma claro, direto e focado no usuário.
- Mantenha as frases curtas e digitalizáveis.
- Prefira um idioma específico e acionável a texto de marketing ou de preenchimento.
- Evite seções padronizadas, como &quot;Tópicos relacionados&quot;, &quot;Perguntas frequentes&quot; ou blocos de resumo genéricos, a menos que sejam explicitamente necessários.
- Use links cruzados no contexto em vez de blocos de navegação de fim de página.
- Não adicione uma lista de referências ou uma seção &quot;Tópicos relacionados&quot; ao final de um artigo. Apresente links relacionados quando eles forem relevantes no conteúdo e explique como cada destino está relacionado ao tópico atual.
- Não use uma linguagem espacial, como &quot;abaixo&quot; ou &quot;acima&quot;, para descrever a ordem do documento; use &quot;seguinte&quot;, &quot;anterior&quot; ou &quot;na próxima seção&quot; em vez disso.

## Regras de nomenclatura da documentação externa

- Não use as siglas de produto do Adobe em documentações externas.
- A primeira menção dos nomes de produtos da Adobe deve usar o nome completo do produto, incluindo &quot;Adobe&quot; quando apropriado.
- Use tags DNL para nomes de produtos no conteúdo, por exemplo:
  - [!DNL Adobe Experience Platform]
  - [!DNL Adobe Journey Optimizer B2B Edition]
  - [!DNL Experience Platform]
  - [!DNL Journey Optimizer B2B Edition]
- Substitua as referências somente de acrônimo, como &quot;AEP&quot; e &quot;AJO B2B&quot;, por seus nomes completos de produtos na documentação voltada para o usuário.
- Quando um produto for introduzido pela primeira vez, insira o nome completo. As menções posteriores podem usar o nome de produto mais curto sem a sigla e manter a tag DNL quando o nome do produto aparecer no texto da interface ou dos documentos.
- Aplique esses termos de forma consistente no título da página, no primeiro parágrafo e em todos os rótulos ou links cruzados que sejam visíveis para os leitores.

## Convenções de nomenclatura específicas do repositório

- Use &quot;Adobe Journey Optimizer B2B Edition&quot; para o nome do produto em documentos voltados para o usuário.
- Use &quot;Adobe Experience Platform&quot; para o nome da plataforma em documentos voltados para o usuário.
- Use o nome do produto em sua forma completa na primeira menção e mantenha as referências posteriores curtas e consistentes.
- Para referências de conjunto de dados, preserve os nomes e as IDs do conjunto de dados real exatamente como eles aparecem no contrato de origem, mesmo quando eles incluam prefixos herdados como `AJOB2B-`.

## Orientação de marcação e formatação

- Escreva um Markdown válido com sabor de GitHub.
- Mantenha os cabeçalhos concisos e descritivos.
- Use tabelas somente quando elas ajudarem os leitores a verificar detalhes técnicos.
- Use links relativos para referências repo-locais.
- Mantenha os blocos de código e os caminhos de campo exatos e copiáveis.
- Evite referências de produto redundantes nos cabeçalhos se o título da página já as indicar.

## Lista de verificação de validação antes da conclusão

- Certifique-se de que não haja acrônimos para produtos Adobe em conteúdo voltado para o usuário.
- Certifique-se de que as primeiras menções usem o nome completo do produto.
- Verifique se os nomes de produtos estão marcados com [!DNL ...], onde exigido pelo estilo do repositório.
- Certifique-se de que o documento evite problemas de formatação padronizada e texto espacial.
- Garantir que o conteúdo técnico permaneça preciso e os links cruzados no contexto sejam preservados.
