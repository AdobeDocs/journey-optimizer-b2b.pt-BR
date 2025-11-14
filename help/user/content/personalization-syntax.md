---
title: Sintaxe de personalização
description: Saiba mais sobre a sintaxe de personalização com base em Handlebars no Journey Optimizer B2B edition, incluindo expressões, auxiliares, tipos literais e regras de formatação.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, sintaxe, personalização
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

---

# Sintaxe de personalização {#personalization-syntax}

As expressões no [!DNL Journey Optimizer B2B Edition] [editor de personalização](./personalization.md#personalization-editor) são baseadas na sintaxe de modelo _Handlebars_. Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos de Handlebars parecem texto regular com expressões Handlebars incorporadas.

Para obter mais detalhes sobre Handlebars e como ele funciona, consulte a [documentação de HandlebarsJS](https://handlebarsjs.com/){target="_blank"}.

## Regras gerais

Exemplo de expressão simples:

```
{{account.accountName}}
```

Onde:

* `account` é um namespace.
* `accountName` é um token composto por atributos.

  >[!NOTE]
  >
  >A estrutura de atributos está definida em um [Esquema XDM do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}.

* Os identificadores podem ser qualquer caractere Unicode, exceto para o seguinte:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* A sintaxe diferencia maiúsculas de minúsculas.

* As palavras **true**, **false**, **null** e **undefined** só são permitidas na primeira parte de uma expressão de caminho.

* Em Handlebars, os valores retornados por {\{expression}\} são _HTML-escaped_. Se a expressão contiver `&`, a saída de escape de HTML retornada será gerada como `&amp;`. Se você não quiser que Handlebars escape um valor, use o +triple-stash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

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

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

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
