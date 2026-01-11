---
title: Aplicativos de página única
description: Crie experiências da Web para aplicativos de página única (SPAs) - configure o rastreamento de exibições, manipule conteúdo dinâmico e gerencie a navegação no lado do cliente no Journey Optimizer B2B edition.
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="No momento, esse recurso está em uma versão beta limitada"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Aplicativos de página única

Os aplicativos de página única (SPAs) apresentam desafios exclusivos para personalização da Web, pois atualizam dinamicamente o conteúdo da página sem recarregamentos completos de página. O Journey Optimizer B2B edition fornece ferramentas especializadas para lidar com a personalização de SPA de maneira eficaz.

## Noções básicas sobre SPAs

Ao contrário dos sites tradicionais de várias páginas, em que cada navegação aciona um carregamento de página completo, os SPAs usam o JavaScript para atualizar o conteúdo dinamicamente, mantendo uma única página do HTML. Essa abordagem cria várias considerações para experiências na Web:

* **Nenhuma página recarregada** - As alterações de conteúdo ocorrem sem acionar os eventos tradicionais de carregamento de página.
* **Exibições virtuais** - Diferentes _exibições_ ou _telas_ dentro do SPA que precisam ser rastreadas como páginas separadas.
* **Roteamento do lado do cliente** - Os roteadores JavaScript (como o Roteador React, o Roteador Vue e o Roteador Angular) manipulam a navegação em vez de solicitações do servidor.
* **DOM dinâmico** - Os elementos da página podem ser criados, modificados ou removidos após o carregamento inicial.

## Configurar suporte a SPA

Para personalizar SPAs de maneira eficaz, você precisa configurar o rastreamento de exibições para que o Journey Optimizer B2B edition possa identificar quando os usuários navegam entre exibições virtuais.

### Configurar declarações de visualização

Trabalhe com sua equipe de desenvolvimento para implementar declarações de exibição usando o Adobe Web SDK. O uso dessas declarações de exibição envolve chamar o comando `sendEvent` com informações de exibição sempre que o SPA navega para uma nova exibição.

**Exemplo de implementação:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Exibir convenções de nomenclatura

Use nomes de exibição descritivos e consistentes que correspondam à estrutura lógica do aplicativo:

| Exibir | Exemplo de nome |
| ---- | ------------ |
| Página inicial | `home` |
| Lista de produtos | `product-list` |
| Detalhes do produto | `product-detail` |
| Carrinho de compras | `cart` |
| Check-out | `checkout` |
| Painel de conta | `account-dashboard` |

>[!NOTE]
>
>Os nomes de exibição fazem distinção entre maiúsculas e minúsculas. Use uma convenção de nomenclatura consistente (recomenda-se usar letras minúsculas com hifens) na implementação.

## Criar experiências da Web para SPAs

Ao criar experiências da Web para SPAs, considere as seguintes práticas recomendadas:

### Exibições específicas do Target

* Na [configuração do canal da Web](../admin/configure-channels-web.md), configure regras de correspondência de URL que se alinhem à sua estrutura de roteamento de SPA.

* Ao criar modificações, especifique a exibição à qual a modificação deve se aplicar.

* Use seletores de CSS que direcionem elementos específicos para cada visualização.

### Lidar com conteúdo dinâmico

Os SPAs geralmente carregam o conteúdo dinamicamente após a renderização inicial da página. Use essas técnicas para garantir que as modificações sejam aplicadas corretamente:

#### Aguardar elementos

Configure as modificações para aguardar os elementos de destino existirem antes de aplicar:

1. No editor não visual, adicione uma modificação com um seletor de CSS.

1. Habilite **[!UICONTROL Aguardar elemento]** e especifique o tempo máximo de espera.

1. A modificação se aplica assim que o elemento de destino aparece no DOM.

#### Usar observadores de mutações

Para conteúdo altamente dinâmico, o Web SDK inclui observadores de mutação integrados que detectam quando novos elementos são adicionados à página. Esses observadores garantem que as modificações sejam aplicadas mesmo quando os elementos são carregados de forma assíncrona.

### Estruturas SPA

As experiências da Web do Journey Optimizer B2B edition funcionam com estruturas SPA populares:

| Estrutura | Considerações |
| --------- | -------------- |
| **Reagir** | As modificações se aplicam depois que o React renderiza componentes para o DOM. Use nomes de classe ou atributos de dados para direcionamento. |
| **Angular** | Direcionar elementos após a execução da detecção de alterações do Angular. Evite direcionar elementos com `*ngIf` antes que eles sejam renderizados. |
| **Vue.js** | Aguarde o `nextTick` do Vue para garantir que os elementos estejam no DOM. Use referências ou atributos personalizados para um direcionamento estável. |
| **Next.js / Nuxt.js** | Para páginas SSR/SSG, verifique se a hidratação do Web SDK está concluída antes de esperar modificações. |

## Práticas recomendadas para personalização de SPA

### Usar seletores estáveis

Os SPAs geralmente geram nomes de classe ou IDs dinâmicos (especialmente com soluções CSS em JS). Como alternativa, você pode usar:

* **Atributos de dados** - Adicione atributos de dados personalizados (`data-testid`, `data-section`, etc.) aos elementos que deseja direcionar.
* **HTML semântica** - Direcionamento baseado na estrutura e nos elementos semânticos do HTML.
* **Atributos de ID** - Use atributos de ID estáveis sempre que possível.

**Exemplo:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**Seletor de CSS:** `[data-action="signup"]`

### Testar visualizações

Ao testar as experiências da Web de SPA:

1. Navegue por todas as exibições nas quais as modificações se aplicam.

1. Testar o fluxo de usuário completo, incluindo:
   * Navegação direta para uma exibição (deep linking)
   * Navegação de outras exibições no SPA
   * Navegação para trás e para a frente do navegador

1. Verifique se as modificações são reaplicadas ao retornar a uma exibição visitada anteriormente.

### Lidar com transições de exibição

Alguns SPAs usam animações ou transições entre exibições. Considere:

* **Tempo** - Verifique se as modificações se aplicam após a conclusão das animações de transição.
* **Visibilidade do elemento** - Os elementos podem existir, mas estar ocultos durante as transições.
* **Cintilação** - Aplique modificações cedo o suficiente para evitar alterações de conteúdo visíveis.

## Solução de problemas

Ao revisar as alterações no design de SPA, use as seguintes recomendações para resolver alguns problemas comuns:

* **Modificações que não aparecem** - Se as modificações não estiverem aparecendo em seu SPA:

   1. **Verificar rastreamento de exibição** - Verifique se `sendEvent` chamadas incluem o nome de exibição correto.

   1. **Verificar a existência do elemento** - Certifique-se de que os elementos de destino estejam no DOM quando as modificações forem aplicadas.

   1. **Revisar seletores** - Confirmar se os seletores de CSS correspondem à estrutura DOM real.

   1. **Verificar console** - Procure erros de JavaScript que possam impedir modificações.

* **Modificações que aparecem brevemente e depois desaparecem** - Esse problema normalmente ocorre quando o SPA renderiza novamente e substitui os elementos modificados:

   1. Use seletores de CSS mais específicos que permaneçam estáveis nas renderizações.

   1. Permitir que os observadores de mutação reapliquem as modificações quando os elementos forem recriados.

   1. Trabalhe com sua equipe de desenvolvimento para adicionar atributos estáveis aos elementos do público-alvo.

* **Duplicar modificações** - Se as modificações aparecerem várias vezes:

   1. Verifique se os eventos de rastreamento de exibição são acionados apenas uma vez por transição de exibição.

   1. Verifique se as modificações têm escopo para exibições específicas em vez de serem aplicadas globalmente.

## Tópicos relacionados

* [Visão geral das experiências da Web](./web-experiences.md)
* [Design de experiência online](./web-experience-design.md)
* [Configurações do canal da Web](../admin/configure-channels-web.md)