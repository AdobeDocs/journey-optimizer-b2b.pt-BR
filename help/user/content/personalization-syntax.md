---
title: Sintaxe de personalização
description: Saiba mais sobre a sintaxe de personalização com base em Handlebars no Journey Optimizer B2B edition, incluindo expressões, auxiliares, tipos literais e regras de formatação.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, sintaxe, personalização
exl-id: 91bbead6-aca0-4f39-9ab5-798b26ab81ee
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
autotag-review: 2026-03-30T22:05:22.123Z
TQID: https://experienceleague.adobe.com/n--W9LWqVlmHK4y8TI9E-ip4qr5X1xfgKj5pkWd8wJM
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 3%

---

# Sintaxe de personalização {#personalization-syntax}

As expressões no [!DNL Journey Optimizer B2B Edition] [editor de personalização](./personalization.md#personalization-editor) são baseadas na sintaxe de modelo _Handlebars_. Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos de Handlebars parecem texto regular com expressões Handlebars incorporadas.

Para obter mais detalhes sobre Handlebars e como ele funciona, consulte a [documentação de HandlebarsJS](https://handlebarsjs.com/){target="_blank"}.

## Regras gerais

Exemplo de expressão simples:

```
{{account.accountName}}
```

Em que:

* `account` é um namespace.
* `accountName` é um token composto por atributos.

  >[!NOTE]
  >
  >A estrutura de atributos está definida em um [Esquema XDM do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/home){target="_blank"}.

* Os identificadores podem ser qualquer caractere Unicode, exceto para o seguinte:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* A sintaxe diferencia maiúsculas de minúsculas.

* As palavras **true**, **false**, **null** e **undefined** só são permitidas na primeira parte de uma expressão de caminho.

* Em Handlebars, os valores retornados por {\{expression}\} são _HTML-escaped_. Se a expressão contiver `&`, a saída de escape de HTML retornada será gerada como `&amp;`. Se você não quiser que Handlebars escape um valor, use o +triple-stash_.

<!--
 For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. 
-->

* Para argumentos de funções literais, o analisador de linguagem de modelo não oferece suporte ao símbolo de barra invertida sem escape único (`\`). Este caractere deve ser evitado com um símbolo adicional de barra invertida (`\`). Por exemplo:

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Auxiliares {#helpers-all}

Uma função auxiliar Handlebars é um identificador simples que pode ser anexado com parâmetros. Cada parâmetro é uma expressão Handlebars. Esses auxiliares podem ser acessados de qualquer contexto em um modelo de email.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!--
 These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name.

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). 
-->

Para obter informações mais detalhadas sobre essas funções, consulte [Funções auxiliares](./personalization-helper-functions.md).

## Tipos literais {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] dá suporte aos seguintes tipos literais:

| Literal | Definição |
| ------- | ---------- |
| String | Um tipo de dados composto de caracteres entre aspas duplas. <br>Exemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Um tipo de dados que é verdadeiro ou falso. |
| Inteiro | Um tipo de dados que representa um número inteiro. Pode ser positivo, negativo ou zero. <br>Exemplos: `-201`, `0`, `412` |
| Matriz | Um tipo de dados que é composto como um grupo de outros valores literais. Ela usa colchetes para agrupar e vírgulas para delimitar entre valores diferentes. <br> **Observação:** não é possível acessar diretamente as propriedades dos itens em uma matriz. <br> Exemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>O uso da variável **xEvent** não está disponível em expressões de personalização. Qualquer referência a xEvent resulta em falhas de validação.
