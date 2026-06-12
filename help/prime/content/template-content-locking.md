---
title: Bloqueio de conteúdo para modelos de email
description: Use as configurações de governança no Journey Optimizer B2B Prime para bloquear conteúdo em modelos de email no nível da estrutura ou do componente, controlando quais autores de email podem editar.
badgeBeta: label="Beta" type="informative" tooltip="Esse recurso faz parte de uma versão beta limitada."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Bloqueio de conteúdo para modelos de email

O bloqueio de conteúdo permite que os autores de modelos definam regras de governança que restringem quais partes de um modelo de email podem ser modificadas quando o modelo for usado em uma jornada. Isso ajuda as equipes de marca e conformidade a proteger os principais elementos de design — como cabeçalhos, logotipos e conteúdo legal — enquanto permite que as equipes de marketing personalizem a mensagem dentro da estrutura aprovada.

>[!NOTE]
>
>O bloqueio de conteúdo é um recurso de governança no nível do editor. Ele controla o que os autores podem editar no espaço de design de email, mas não impede alterações feitas por meio da API.

Somente usuários com a permissão **[!UICONTROL Gerenciar modelos de conteúdo]** podem definir configurações de governança.

## Modos de governança {#modes}

Ao ativar o controle em um modelo, selecione um dos dois modos:

| Modo | Descrição |
| ---- | ----------- |
| **[!UICONTROL Bloqueio de conteúdo]** | Bloquear seletivamente estruturas ou componentes específicos. As áreas desbloqueadas permanecem editáveis para os autores. |
| **[!UICONTROL Somente leitura]** | Bloquear o modelo inteiro. Os autores podem aplicá-la a um email, mas não podem modificar nenhuma parte de seu conteúdo. |

## Habilitar governança {#enable}

1. Abra o modelo no espaço de design de email.
1. No painel direito, clique no componente **[!UICONTROL Corpo]** para selecioná-lo.
1. Ativar/desativar **[!UICONTROL Governança]**.
1. Na lista suspensa de modo, selecione **[!UICONTROL Bloqueio de conteúdo]** ou **[!UICONTROL Somente leitura]**.

Se você selecionou **[!UICONTROL Bloqueio de conteúdo]**, continue com o bloqueio de elementos individuais.

### Bloquear uma estrutura {#lock-structure}

1. Na tela de desenho, selecione a estrutura (layout da coluna) que deseja proteger.
1. No painel direito, habilite a opção de alternância **[!UICONTROL Estrutura de bloqueio]**.

Todo o conteúdo aninhado em uma estrutura bloqueada é bloqueado automaticamente. Para permitir que um componente específico dentro de uma estrutura bloqueada permaneça editável, selecione o componente e habilite **[!UICONTROL Editável]** no painel direito.

### Bloquear um componente {#lock-component}

Em uma estrutura editável, é possível bloquear componentes de conteúdo individuais.

1. Selecione o componente na tela.
1. No painel direito, habilite a opção **[!UICONTROL Bloquear conteúdo]**.

### Permitir adições de conteúdo {#allow-additions}

Ao usar o modo **[!UICONTROL Bloqueio de conteúdo]**, você pode permitir que os autores adicionem novo conteúdo ao modelo, mantendo os elementos bloqueados protegidos:

1. Habilitar **[!UICONTROL Permitir adição de conteúdo]**.
1. Escolha se os autores podem adicionar estruturas e componentes de conteúdo ou apenas componentes de conteúdo.

## Identificar elementos bloqueados {#identify}

A **[!UICONTROL árvore de navegação]** no painel esquerdo mostra ícones de bloqueio e lápis para ajudar os autores a identificar rapidamente o que podem ou não modificar:

* Um **ícone de bloqueio** indica um elemento bloqueado.
* Um **ícone de lápis** indica um elemento que é editável.

Os elementos bloqueados são indicados visualmente na tela quando um autor abre o modelo.

## Considerações

As configurações de governança são salvas com o modelo. Qualquer email criado a partir de um modelo controlado herda sua configuração de bloqueio no momento em que é aplicado. A atualização das configurações de governança em um modelo não afeta os emails criados anteriormente a partir dele.
