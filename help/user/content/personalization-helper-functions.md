---
title: Funções de ajuda
description: Guia de referência para funções auxiliares de personalização no Journey Optimizer B2B edition. Ele inclui sintaxe e exemplos para sequências, datas, matemática e muito mais.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, sintaxe, personalização
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 6%

---

# Funções de ajuda

Use as funções Auxiliar no editor de personalização para definir experiências de conteúdo personalizadas com precisão e eficiência manipulando dados, realizando cálculos e formatando conteúdo. Explore e experimente essas funções, operadores e auxiliares para descobrir como eles trabalham juntos para ajudá-lo a criar jornadas personalizadas orientadas por dados.

>[!AVAILABILITY]
>
>As funções auxiliares estão disponíveis para ambientes B2B edition do Journey Otimizer que são provisionados na [arquitetura simplificada](../simplified-architecture.md).

## Funções de agregação

Use funções de agregação para agrupar vários valores para formar um único valor de resumo. Também é possível usar as funções de matriz e de lista para definir interações com matrizes, listas e strings com mais facilidade.

### média {#average}

Use a função `average` para retornar a média aritmética de todos os valores selecionados na matriz.

+++Sintaxe

```sql
{%= average(array) %}
```

**Exemplo**

A operação a seguir retorna o preço médio de todas as ordens.

```sql
{%=average(orders.order.price)%}
```

+++

### contagem {#count}

Use a função `count` para retornar o número de elementos dentro da matriz especificada.

+++Sintaxe

```sql
{%= count(array) %}
```

**Exemplo**

A operação a seguir retorna o número de ordens na matriz.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Use a função `max` para retornar o maior valor selecionado na matriz.

+++Sintaxe

```sql
{%= max(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais alto de todas as ordens.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Use a função `min` para retornar o menor valor selecionado na matriz.

+++Sintaxe

```sql
{%= min(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais baixo de todas as ordens.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

Use a função `sum` para retornar a soma de todos os valores selecionados na matriz.

+++Sintaxe

```sql
{%= sum(array) %}
```

**Exemplo**

A operação a seguir retorna a soma de todos os preços das ordens.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Funções aritméticas {#maths}

Use funções aritméticas para realizar cálculos básicos em valores.

### adicionar {#add}

Use a função `+` (adição) para localizar a soma de duas expressões de argumento.

+++Sintaxe

```sql
{%= double + double %}
```

**Exemplo**

A operação a seguir soma o preço de dois produtos diferentes.

```sql
{%= product1.price + product2.price %}
```

+++

### multiplicar {#multiply}

Use a função `*` (multiplicação) para localizar o produto de duas expressões de argumento.

+++Sintaxe

```sql
{%= double * double %}
```

**Exemplo**

A operação a seguir localiza o produto do estoque e o preço de um produto para localizar o valor bruto do produto.

```sql
{%= product.inventory * product.price %}
```

+++

### subtrair {#substract}

Use a função `-` (subtração) para localizar a diferença de duas expressões de argumento.

+++Sintaxe

```sql
{%= double - double %}
```

**Exemplo**

A operação a seguir encontra a diferença de preço entre dois produtos diferentes.

```sql
{%= product1.price - product2.price %}
```

+++

### dividir {#divide}

Use a função `/` (divisão) para localizar o quociente de duas expressões de argumento.

+++Sintaxe

```sql
{%= double / double %}
```

**Exemplo**

A operação a seguir encontra o quociente entre o total de produtos vendidos e o dinheiro total ganho para ver o custo médio por item.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### restante {#remainder}

Use a função `%` (restante) para localizar o restante após dividir as duas expressões de argumento.

+++Sintaxe

```sql
{%= double % double %}
```

**Exemplo**

A operação a seguir verifica se a idade da pessoa é divisível por cinco.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Matrizes e funções de lista {#arrays}

Use essas funções para facilitar a interação com matrizes, listas e sequências de caracteres.

### countOnlyNull {#count-only-null}

Use a função `countOnlyNull` para contar o número de valores nulos em uma lista.

+++Sintaxe

```sql
{%= countOnlyNull(array) %}
```

**Exemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retorna 3.

+++

### countWithNull {#count-with-null}

Use a função `countWithNull` para contar todos os elementos de uma lista, incluindo valores nulos.

+++Sintaxe

```sql
{%= countWithNull(array) %}
```

**Exemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retorna 6.

+++

### distinct {#distinct}

Use a função `distinct` para obter valores de uma matriz ou lista com valores duplicados removidos.

+++Sintaxe

```sql
{%= distinct(array) %}
```

**Exemplo**

A operação a seguir especifica as pessoas que fizeram pedidos em mais de um armazenamento.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

Use a função `distinctCountWithNull` para contar o número de valores diferentes em uma lista, incluindo os valores nulos.

+++Sintaxe

```sql
{%= distinctCountWithNull(array) %}
```

**Exemplo**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Retorna 3.

+++

### head {#head}

Use a função `head` para retornar o primeiro item em uma matriz ou lista.

+++Sintaxe

```sql
{%= head(array) %}
```

**Exemplo**

A operação a seguir retorna a primeira das cinco ordens principais com o preço mais alto. Mais informações sobre a função `topN` podem ser encontradas na [primeira `n` da seção de matriz](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

A função `topN` classifica uma matriz em ordem decrescente com base na expressão numérica fornecida e retorna os primeiros `N` itens. Se o tamanho da matriz for menor que `N`, ela retornará toda a matriz classificada.

+++Sintaxe

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{ARRAY}` | A matriz ou lista para classificar. |
| `{VALUE}` | A propriedade usada para classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens para retornar. |

**Exemplo**

A operação a seguir retorna as cinco primeiras ordens com o preço mais baixo.

```sql
{%= topN(orders,price, 5) %}
```

+++

### no {#in}

Use a função `in` para determinar se um item é membro de uma matriz ou lista.

+++Sintaxe

```sql
{%= in(value, array) %}
```

**Exemplo**

A operação a seguir define as pessoas com aniversários em março, junho ou setembro.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### inclui {#includes}

Use a função `includes` para determinar se uma matriz ou lista contém um determinado item.

+++Sintaxe

```sql
{%= includes(array,item) %}
```

**Exemplo**

A operação a seguir define as pessoas cuja cor favorita inclui vermelho.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### cruzamentos {#intersects}

A função `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

+++Sintaxe

```sql
{%= intersects(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas cujas cores favoritas incluem pelo menos uma das cores vermelha, azul ou verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

A função `bottomN` classifica uma matriz em ordem crescente com base na expressão numérica fornecida e retorna os primeiros `N` itens. Se o tamanho da matriz for menor que `N`, ela retornará toda a matriz classificada.

+++Sintaxe

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- | 
| `{ARRAY}` | A matriz ou lista para classificar. |
| `{VALUE}` | A propriedade usada para classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens para retornar. |

**Exemplo**

A operação a seguir retorna as cinco últimas ordens com o preço mais alto.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Use a função `notIn` para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>A função `notIn` *também* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata da função `in`.

+++Sintaxe

```sql
{%= notIn(value, array) %}
```

**Exemplo**

A operação a seguir define as pessoas com aniversários que não são em março, junho ou setembro.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Use a função `subsetOf` para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, que todos os elementos na matriz A são elementos da matriz B.

+++Sintaxe

```sql
{%= subsetOf(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas que visitaram todas as cidades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### supersetOf {#superset}

Use a função `supersetOf` para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

+++Sintaxe

```sql
{%= supersetOf(array1, array2) %}
```

**Exemplo**

A operação seguinte define as pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Funções de data e hora {#date-time}

Use as funções de data e hora para executar operações de data e hora em valores.

### addDays {#add-days}

A função `addDays` ajusta uma determinada data por um número especificado de dias, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addDays(date, number) %}
```

**Exemplo**

* Entrada: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

A função `addHours` ajusta uma determinada data por um número especificado de horas, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addHours(date, number) %}
```

**Exemplo**

* Entrada: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Saída: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

A função `addMinutes` ajusta uma determinada data por um número especificado de minutos, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addMinutes(date, number) %}
```

**Exemplo**

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Saída: `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

A função `addMonths` ajusta uma determinada data por um número especificado de meses, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addMonths(date, number) %}
```

**Exemplo**

* Entrada: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

A função `addSeconds` ajusta uma determinada data por um número especificado de segundos, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addSeconds(date, number) %}
```

**Exemplo**

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

A função `addYears` ajusta uma determinada data por um número especificado de anos, usando valores positivos para incrementar e valores negativos para decrementar.

+++Sintaxe

```sql
{%= addYears(date, number) %}
```

**Exemplo**

* Entrada: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2026-11-01T17:19:51Z`

+++

### idade {#age}

Use a função `age` para recuperar a idade de uma determinada data.

+++Sintaxe

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

A função `ageInDays` calcula o número de dias decorridos entre a data especificada e a data atual. Usa negativo para datas futuras e positivo para datas passadas.

+++Sintaxe

```sql
{%= ageInDays(date) %}
```

**Exemplo**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Ásia/Calcutá)

* Entrada: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Saída: `5`

+++

### ageInMonths {#age-months}

A função `ageInMonths` calcula o número de meses decorridos entre a data especificada e a data atual. Usa negativo para datas futuras e positivo para datas passadas.

+++Sintaxe

```sql
{%= ageInMonths(date) %}
```

**Exemplo**

currentDate = 2025-01-07T12:22:46.993748+05:30(Ásia/Calcutá)

* Entrada: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Saída: `12`

+++

### compareDates {#compare-dates}

A função `compareDates` compara a primeira data de entrada com a outra. Ele retorna 0 se a data1 for igual à data2, -1 se a data1 for anterior à data2 e 1 se a data1 for posterior à data2.

+++Sintaxe

```sql
{%= compareDates(date1, date2) %}
```

**Exemplo**

* Entrada: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Saída: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

A função `convertZonedDateTime` converte uma data-hora em um determinado fuso horário.

+++Sintaxe

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Exemplo**

* Entrada: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Saída: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Use a função `currentTimeInMillis` para recuperar a hora atual em milissegundos da época.

+++Sintaxe

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Use a função `dateDiff` para recuperar a diferença entre duas datas em número de dias.

+++Sintaxe

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth` retorna o número que representa o dia do mês.

+++Sintaxe

```sql
{%= dayOfMonth(datetime) %}
```

**Exemplo**

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Saída: `5`

+++

### DayOfWeek {#day-week}

Use a função `dayOfWeek` para recuperar o dia da semana.

+++Sintaxe

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Use a função `dayOfYear` para recuperar o dia do ano.

+++Sintaxe

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

A função `diffInSeconds` retorna a diferença entre duas datas em termos de segundos.

+++Sintaxe

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Exemplo**

* Entrada: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Saída: `50`

+++

### extractHours {#extract-hours}

A função `extractHours` extrai o componente de hora de um determinado carimbo de data/hora.

+++Sintaxe

```sql
{%= extractHours(date) %}
```

**Exemplo**

* Entrada: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `17`

+++

### extractMinutes {#extract-minutes}

A função `extractMinutes` extrai o componente de minuto de um carimbo de data/hora especificado.

+++Sintaxe

```sql
{%= extractMinutes(date) %}
```

**Exemplo**

* Entrada: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `19`

+++

### extractMonths {#extract-months}

A função `extractMonth` extrai o componente de mês de um determinado carimbo de data/hora.

+++Sintaxe

```sql
{%= extractMonths(date) %}
```

**Exemplo**

* Entrada: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `11`

+++

### extractSeconds {#extract-seconds}

A função `extractSeconds` extrai o segundo componente de um determinado carimbo de data/hora.

+++Sintaxe

```sql
{%= extractSeconds(date) %}
```

**Exemplo**

* Entrada: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `51`

+++

### formatDate {#format-date}

Use a função `formatDate` para formatar um valor de data e hora. O formato deve ser um padrão Java `DateTimeFormat` válido.

+++Sintaxe

```sql
{%= formatDate(datetime, format) %}
```

Onde a primeira string é o atributo de data e o segundo valor é como você deseja que a data seja convertida e exibida.

>[!NOTE]
>
> Se um padrão de data for inválido, a data voltará ao formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemplo**

A operação a seguir retorna a data no seguinte formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Caracteres padrão {#pattern-characters}

Algumas letras de padrão podem parecer semelhantes, mas representam conceitos diferentes.

| Padrão | Significado | Exemplo (para `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Ano civil (ano padrão) | `2023` |
| `Y` | Ano com base em semana (ISO 8601). Pode diferir nos limites do ano. | `2024` (31 de dezembro de 2023 cai na primeira semana de 2024) |
| `M` | Mês do ano (1-12 ou texto como `Jan`, `January`) | `12` ou `Dec` |
| `m` | Minuto da hora (0-59) | `15` |
| `d` | Dia do mês (1-31) | `31` |
| `D` | Dia do ano (1-366) | `365` |

#### Formatar data com suporte local {#format-date-locale}

Você pode usar a função `formatDate` para formatar um valor de data e hora em sua representação sensível a idioma correspondente, como para um local desejado. O formato deve ser um padrão Java `DateTimeFormat` válido.

+++Sintaxe

```sql
{%= formatDate(datetime, format, locale) %}
```

Onde a primeira string é o atributo de data, o segundo valor é como você deseja que a data seja convertida e exibida, e o terceiro valor representa o local no formato de string.

>[!NOTE]
>
> Se um padrão de data for inválido, a data voltará ao formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Você pode usar formatação e localidades válidas conforme resumido na [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e nas [Localidades com suporte](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exemplo**

A operação a seguir retorna a data no seguinte formato: MM/dd/AA e localidade FRANÇA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

A função `getCurrentZonedDateTime` retorna a data e a hora atuais com informações de fuso horário.

+++Sintaxe

```sql
{%= getCurrentZonedDateTime() %}
```

**Exemplo**

* Entrada: `{%= getCurrentZonedDateTime() %}`
* Saída: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

A função `diffInHours` retorna a diferença entre duas datas em termos de horas.

+++Sintaxe

```sql
{%= diffInHours(endDate, startDate) %}
```

**Exemplo**

* Entrada: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Saída: `10`

+++

### diffInMinutes {#diff-minutes}

A função `diffInMinutes` retorna a diferença entre duas datas em termos de minutos.

+++Sintaxe

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Exemplo**

* Entrada: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Saída: `60`

+++

### diffInMonths {#months-difference}

A função `diffInMonths` retorna a diferença entre duas datas em termos de meses.

+++Sintaxe

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Exemplo**

* Entrada: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Saída: `3`

+++

### setDays {#set-days}

Use a função `setDays` para definir o dia do mês para a data-hora especificada.

+++Sintaxe

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Use a função `setHours` para definir a hora da data-hora.

+++Sintaxe

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

A função `toDateTime` converte a cadeia de caracteres em data. Retorna a data da época como saída para entrada inválida.

+++Sintaxe

```sql
{%= toDateTime(string, string) %}
```

**Exemplo**

* Entrada: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Saída: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Use a função `toUTC` para converter um datetime em UTC.

+++Sintaxe

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Use a função `truncateToStartOfDay` para modificar uma determinada data-hora, definindo-a para o início do dia com a hora 00:00.

+++Sintaxe

```sql
{%= truncateToStartOfDay(date) %}
```

**Exemplo**

* Entrada: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Saída: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Use a função `truncateToStartOfQuarter` para truncar uma data-hora para o primeiro dia de seu trimestre (como 1º de janeiro, 1º de abril, 1º de julho, 1º de outubro) em 00:00.

+++Sintaxe

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Exemplo**

* Entrada: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

A função `truncateToStartOfWeek` modifica uma determinada data-hora definindo-a para o início da semana (segunda-feira às 00:00).

+++Sintaxe

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Exemplo**

* Entrada: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Saída: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Use a função `truncateToStartOfYear` para modificar uma determinada data-hora, truncando-a para o primeiro dia do ano (1° de janeiro) em 00:00.

+++Sintaxe

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Exemplo**

* Entrada: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Use a função `weekOfYear` para recuperar a semana do ano.

+++Sintaxe

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Use a função `diffInYears` para retornar a diferença entre duas datas em termos de anos.

+++Sintaxe

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Exemplo**

* Entrada: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Saída: `5`

+++

## Funções do operador {#operators}

Use as funções booleano e de comparação para executar avaliações lógicas.

### e {#and}

A função `and` é usada para criar uma conjunção lógica.

+++Sintaxe

```sql
{%= query1 and query2 %}
```

**Exemplo**

A operação a seguir retorna todas as pessoas com país de origem (França) e ano de nascimento (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### ou {#or}

A função `or` é usada para criar uma disjunção lógica.

+++Sintaxe

```sql
{%= query1 or query2 %}
```

**Exemplo**

A operação a seguir retorna todas as pessoas com país de origem (França) ou ano de nascimento (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### é igual a {#operator-equals}

A função `=` (igual a) verifica se um valor ou expressão é igual a outro valor ou expressão.

+++Sintaxe

```sql
{%= expression = value %}
```

**Exemplo**

A operação a seguir verifica se o país do endereço residencial é a França.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### diferente de {#notequal}

A função `!=` (diferente de) verifica se um valor ou expressão é **não** igual a outro valor ou expressão.

+++Sintaxe

```sql
{%= expression != value %}
```

**Exemplo**

A operação a seguir verifica se o país do endereço residencial não é a França.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### maior que {#greaterthan}

Use a função `>` (maior que) para verificar se o primeiro valor é maior que o segundo valor.

+++Sintaxe

```sql
{%= expression1 > expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas estritamente após 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### maior que ou igual a {#greaterthanorequal}

Use a função `>=` (maior que ou igual a) para verificar se o primeiro valor é maior que ou igual ao segundo valor.

+++Sintaxe

```sql
{%= expression1 >= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em ou após 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### menor que {#lessthan}

Use a função de comparação `<` (menor que) para verificar se o primeiro valor é menor que o segundo valor.

+++Sintaxe

```sql
{%= expression1 < expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas antes de 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### menor que ou igual a{#lessthanorequal}

Use a função de comparação `<=` (menor que ou igual a) para verificar se o primeiro valor é menor que ou igual ao segundo valor.

+++Sintaxe

```sql
{%= expression1 <= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em 2000 ou antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Funções dinâmicas {#dynamic-helpers}

Use as funções auxiliares dinâmicas para usar avaliações condicionais, iteração e atribuições de variáveis para personalização dinâmica.

### Valor de fallback padrão {#default-value}

O auxiliar `Default Fallback Value` será usado para retornar um valor de fallback padrão se um atributo estiver vazio ou nulo. Esse mecanismo funciona para atributos de Perfil e eventos de Jornada.

+++Sintaxe

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Neste exemplo, o valor `there` será exibido se o atributo `firstName` desse perfil estiver vazio ou nulo.

+++

### if (condições) {#if-function}

O auxiliar `if` é usado para definir um bloco condicional.
Se a expressão evaluation retornar true, o bloco será renderizado, caso contrário, será ignorado.

+++Sintaxe

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Após o auxiliar `if`, você pode inserir uma instrução `else` para especificar um bloco de código a ser executado, se a mesma condição for falsa.
A instrução `elseif` especifica uma nova condição para testar se a primeira instrução retorna falso.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### a menos que {#unless}

Use o auxiliar `unless` para definir um bloco condicional. Por oposição ao auxiliar `if`, se a avaliação da expressão retornar falso, o bloco será renderizado.

+++Sintaxe

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemplo**

Renderize algum conteúdo com base na extensão de endereço de email:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### cada {#each}

Use o auxiliar `each` para iterar sobre uma matriz.

A estrutura auxiliar é ```{{#each ArrayName}}``` SeuConteúdo `{{/each}}`

Você pode usar a palavra-chave `this` dentro do bloco para fazer referência a itens de matriz individuais. Use `{{@index}}` para renderizar o índice do elemento da matriz.

+++Sintaxe

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Exemplo**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exemplo**

Renderize uma lista de produtos que este usuário tem em seu carrinho:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### com {#with}

Use o auxiliar `with` para alterar o token de avaliação da parte do modelo.

+++Sintaxe

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

O auxiliar `with` é útil também para definir uma variável de atalho.

**Exemplo**

Use `with` para aliases de nomes de variáveis longos para nomes mais curtos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

A função `let` permite que uma expressão seja armazenada como uma variável a ser usada posteriormente em uma consulta.

+++Sintaxe

```sql
{% let variable = expression %} {{variable}}
```

**Exemplo**

O exemplo a seguir permite calcular a soma total dos preços dos produtos no carrinho com preços entre 100 e 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Metadados de execução {#execution-metadata}

>[!AVAILABILITY]
>
>Esse recurso está com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Use o `executionMetadata` para capturar e armazenar pares de valores chave personalizados dinamicamente no contexto de execução da mensagem.

Com essa função, é possível anexar informações contextuais a qualquer ação nativa de suas campanhas ou jornadas. Use-a para exportar dados contextuais de delivery em tempo real para sistemas externos para várias finalidades, como rastreamento, análise, personalização e processamento downstream.

>[!NOTE]
>
>As ações personalizadas não oferecem suporte à função `executionMetadata`.

Por exemplo, você pode usar o auxiliar do `executionMetadata` para anexar uma ID específica a cada entrega enviada para cada perfil. Essas informações são geradas durante o tempo de execução e os metadados de execução enriquecidos podem ser exportados para reconciliação downstream com uma plataforma de relatórios externa.

+++Sintaxe

```
{{executionMetadata key="your_key" value="your_value"}}
```

Nesta sintaxe, `key` refere-se ao nome dos metadados e `value` são os metadados a serem mantidos.

**Como funciona**

Selecione qualquer elemento do conteúdo do canal dentro de uma campanha ou jornada e, usando o editor de personalização, adicione o auxiliar do `executionMetadata` a esse elemento.

>[!NOTE]
>
>A função `executionMetadata` não está visível quando o conteúdo em si é exibido.

No tempo de execução, o valor dos metadados é adicionado ao **[!UICONTROL Conjunto de Dados de Evento de Feedback de Mensagem]** existente com a seguinte adição de esquema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Há um limite superior de 2 kb nos pares de valores principais por ação. Se o limite de 2Kb for excedido, a mensagem ainda será entregue, mas qualquer um dos pares de valores principais poderá ser truncado.

**Exemplo**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

Neste exemplo, assumindo `profile.person.name.firstName` = &quot;Alex&quot;, a entidade resultante é:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Funções do mapa {#maps}

Use funções de mapa na personalização para facilitar a interação com mapas.

### get {#get}

Use a função `get` para recuperar o valor de um mapa para uma determinada chave.

+++Sintaxe

```sql
{%= get(map, string) %}
```

**Exemplo**

A operação a seguir obtém o valor do mapa de identidade para a chave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### chaves {#keys}

Use a função `keys` para recuperar todas as chaves de um determinado mapa.

+++Sintaxe

```sql
{%= keys(map) %}
```

**Exemplo**

A operação a seguir recupera todas as chaves do mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

+++

### valores {#values}

A função `values` é usada para recuperar todos os valores de um determinado mapa.

+++Sintaxe

```sql
{%= values(map) %}
```

**Exemplo**

A operação a seguir recupera todos os valores do mapa `identityMap`.

```sql
{%= values(identityMap) %}
```

+++

## Funções matemáticas {#math}

Saiba como usar funções matemáticas no editor de personalização.

### absoluto {#absolute}

Use a função `absolute` para converter um número em seu valor absoluto.

+++Sintaxe

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Use a função `formatNumber` para formatar qualquer número em sua representação sensível a linguagem.

Ele aceita um número e uma string representando o local e retorna uma string formatada do número no local desejado.

+++Sintaxe

```sql
{%= formatNumber(number/double,string) %}: string
```

Você pode usar formatação e localidades válidas conforme resumido na [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e nas [Localidades com suporte](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Exemplo**

Esta consulta retorna uma string formatada em árabe correspondente a 123456.789 como o número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Use a função `random` para retornar um valor aleatório entre 0 e 1.

+++Sintaxe

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Use a função `roundDown` para arredondar um número para baixo.

+++Sintaxe

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Use a função `roundUp` para arredondar um número para cima.

+++Sintaxe

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

A função `toHexString` converte qualquer número em sua cadeia de caracteres hexadecimal.

+++Sintaxe

```sql
{%= toHexString(number) %}: string
```

**Exemplo**

Esta consulta retorna o valor hexadecimal de 158 como 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Use a função `toInt` para converter tipos (número, duplo, inteiro, longo, flutuante, curto, byte, booleano, string) em um inteiro.

+++Sintaxe

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Exemplo**

Esta consulta retorna o valor inteiro de 42,6 como 42.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Use a função `toPercentage` para converter um número em porcentagem.

+++Sintaxe

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Use a função `toPrecision` para converter um número na precisão necessária.

+++Sintaxe

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

A função `toString` converte qualquer número em sua representação de cadeia de caracteres.

+++Sintaxe

```sql
{%= toString(string) %}: string
```

**Exemplo**

Esta consulta retorna `"12"`.

```sql
{%= toString(12) %} 
```

+++

## Funções do objeto {#objects}

Funções de objeto para consultar propriedades ou atributos de objeto.

### isNull {#isNull}

A função `isNull` determina se uma referência de objeto não existe.

+++Sintaxe

```sql
{%= isNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa não existe.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

A função `isNotNull` determina se existe uma referência de objeto.

+++Sintaxe

```sql
{%= isNotNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa existe.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Funções de string {#string-functions}

Saiba como usar funções de string no editor de personalização.

### camelCase {#camelCase}

A função `camelCase` coloca a primeira letra de cada palavra de uma cadeia de caracteres em maiúscula.

+++Sintaxe

```sql
{%= camelCase(string)%}
```

**Exemplo**

A função a seguir coloca a primeira letra de uma palavra em maiúscula no endereço do perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

A função `charCodeAt` retorna o valor ASCII de um caractere, como a função `charCodeAt` no JavaScript. Ele pega uma string e um inteiro (definindo a posição de um caractere) como argumentos de entrada e retorna seu valor ASCII correspondente.

+++Sintaxe

```sql
{%= charCodeAt(string,int) %}: int
```

**Exemplo**

A função a seguir retorna o valor ASCII de `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

A função `concat` combina duas cadeias de caracteres em uma.

+++Sintaxe

```sql
{%= concat(string,string) %}
```

**Exemplo**

A função a seguir combina o perfil cidade e país em uma única sequência.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### contém {#contains}

Use a função `contains` para determinar se uma cadeia de caracteres contém uma subsequência especificada.

+++Sintaxe

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A sequência de caracteres a ser verificada. |
| `STRING_2` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplos**

* A função a seguir verifica se o nome do perfil contém a letra A (em maiúsculas ou minúsculas). Se o perfil retornar, retorna `true`. Caso contrário, retornará `false`.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o email da pessoa contém a cadeia de caracteres `2010@gm`.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

Use a função `doesNotContain` para determinar se uma cadeia de caracteres não contém uma subsequência especificada.

+++Sintaxe

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A sequência de caracteres a ser verificada. |
| `STRING_2` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o endereço de email da pessoa não contém a cadeia de caracteres `2010@gm`.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Use a função `doesNotEndWith` para determinar se uma cadeia de caracteres não termina com uma subcadeia especificada.

+++Sintaxe

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o email da pessoa não termina com `.com`.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Use a função `doesNotStartWith` para determinar se uma cadeia de caracteres não inicia com uma subcadeia especificada.

+++Sintaxe

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não inicia com `Joe`.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Use a função `encode64` para codificar uma cadeia de caracteres para preservar as Informações Pessoais (PI), como a ser incluída em uma URL.

+++Sintaxe

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

Use a função `endsWith` para determinar se uma sequência de caracteres termina com uma subsequência especificada.

+++Sintaxe

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o email da pessoa termina com `.com`.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### é igual a {#equals}

Use a função `equals` para determinar se uma cadeia de caracteres é igual à cadeia especificada, com distinção entre maiúsculas e minúsculas.

+++Sintaxe

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa é `John`.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Use a função `equalsIgnoreCase` para determinar se uma cadeia de caracteres é igual à cadeia especificada, sem diferenciar maiúsculas de minúsculas.

+++Sintaxe

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa é `John`.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Use a função `extractEmailDomain` para extrair o domínio de um endereço de email.

+++Sintaxe

```sql
{%= extractEmailDomain(string) %}
```

**Exemplo**

A consulta a seguir extrai o domínio de email do endereço de email pessoal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Use a função `formatCurrency` para converter qualquer número em sua representação de moeda sensível ao idioma correspondente, dependendo da localidade transmitida como uma cadeia de caracteres no segundo argumento.

+++Sintaxe

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exemplo**

Esta consulta retorna £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Use a função `getUrlHost` para recuperar o nome de host de uma URL.

+++Sintaxe

```sql
{%= getUrlHost(string) %}: string
```

**Exemplo**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Retorna &quot;www.myurl.com&quot;

+++

### getUrlPath {#get-url-path}

Use a função `getUrlPath` para recuperar o caminho após o nome de domínio de uma URL.

+++Sintaxe

```sql
{%= getUrlPath(string) %}: string
```

**Exemplo**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Retorna &quot;/contact.html&quot;

+++

### getUrlProtocol {#get-url-protocol}

Use a função `getUrlProtocol` para recuperar o protocolo de uma URL.

+++Sintaxe

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemplo**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Retorna &quot;http&quot;

+++

### indexOf {#index-of}

Use a função `indexOf` para retornar a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

+++Sintaxe

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Retorna 6.

+++

### isEmpty {#isEmpty}

Use a função `isEmpty` para determinar se uma cadeia de caracteres está vazia.

+++Sintaxe

```sql
{%= isEmpty(string) %}
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil estiver vazio. Do contrário, retorna `false`.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Use a função `isNotEmpty` para determinar se uma cadeia de caracteres não está vazia.

+++Sintaxe

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil não estiver vazio. Do contrário, retorna `false`.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Use a função `lastIndexOf` para retornar a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

+++Sintaxe

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Retorna 7.

+++

### leftTrim {#leftTrim}

Use a função `leftTrim` para remover espaços em branco do início de uma cadeia.

+++Sintaxe

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Use a função `length` para obter o número de caracteres em uma cadeia de caracteres ou expressão.

+++Sintaxe

```sql
{%= length(string) %}
```

**Exemplo**

A função a seguir retorna o comprimento do nome da cidade do perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### curtir {#like}

Use a função `like` para determinar se uma cadeia de caracteres corresponde a um padrão especificado.

+++Sintaxe

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A expressão que deve corresponder à primeira sequência. Há dois caracteres especiais suportados para a criação de uma expressão: `%` e `_`. <ul><li>`%` é usado para representar zero ou mais caracteres.</li><li>`_` é usado para representar exatamente um caractere.</li></ul> |

**Exemplo**

A consulta a seguir recupera todas as cidades em que os perfis vivem contendo o padrão `es`.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Use a função `lowerCase` para converter uma cadeia de caracteres em letras minúsculas.

+++Sintaxe

```sql
{%= lowerCase(string) %}
```

**Exemplo**

Essa função converte o nome do perfil em letras minúsculas.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

Use a função `matches` para determinar se uma sequência de caracteres corresponde a uma expressão regular específica. Para obter mais informações sobre padrões correspondentes em expressões regulares, consulte [a documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Sintaxe

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com `John`.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### máscara {#mask}

Use a função `mask` para substituir uma parte de uma cadeia de caracteres por caracteres &quot;X&quot;.

+++Sintaxe

```sql
{%= mask(string,integer,integer) %}
```

**Exemplo**

A consulta a seguir substitui a sequência &quot;123456789&quot; por caracteres &quot;X&quot;, com exceção do primeiro e dos últimos 2 caracteres.

```sql
{%= mask("123456789",1,2) %}
```

A consulta retorna `1XXXXXX89`.

+++

### md5 {#md5}

Use a função `md5` para calcular e retornar o hash md5 de uma cadeia de caracteres.

+++Sintaxe

```sql
{%= md5(string) %}: string
```

**Exemplo**

```sql
{%= md5("hello world") %}
```

Retorna &quot;5eb63bbbbe01eed093cb22bb8f5acdc3&quot;

+++

### notEqualTo {#notEqualTo}

Use a função `notEqualTo` para determinar se uma cadeia de caracteres não é igual à cadeia especificada.

+++Sintaxe

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não é `John`.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Use a função `notEqualWithIgnoreCase` para comparar duas cadeias de caracteres ignorando maiúsculas e minúsculas.

+++Sintaxe

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina se o nome da pessoa não é `john`, sem distinção entre maiúsculas e minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Use a função `regexGroup` para extrair informações específicas com base na expressão regular fornecida.

+++Sintaxe

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING}` | A sequência de caracteres a ser verificada. |
| `{EXPRESSION}` | A expressão regular que deve corresponder à primeira sequência. |
| `{GROUP}` | Grupo de expressão para correspondência. |

**Exemplo**

A consulta a seguir extrai o nome de domínio de um endereço de email.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

Use a função `replace` para substituir uma determinada substring em uma string por outra substring.

+++Sintaxe

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A cadeia de caracteres em que a subcadeia de caracteres deve ser substituída. |
| `{STRING_2}` | A subcadeia de caracteres a ser substituída. |
| `{STRING_3}` | A substring de substituição. |

**Exemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Retorna `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Use a função `replaceAll` para substituir todas as subsequências de um texto que correspondam à expressão regex pela sequência de caracteres de substituição literal especificada. O Regex tem tratamento especial de `\` e `+` e todas as expressões regex seguem a estratégia de escape do PQL. A substituição continua do início da cadeia de caracteres até o fim. Por exemplo, a substituição de `aa` por `b` na cadeia de caracteres `aaa` resulta em `ba` em vez de `ab`.

+++Sintaxe

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Quando a expressão usada como segundo argumento for um caractere regex especial, use barra invertida dupla (`//`).  Os caracteres de regex especiais são: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Saiba mais em [documentação do Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

A função `rightTrim` remove espaços em branco do final de uma cadeia de caracteres.

+++Sintaxe

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

A função `sha256` calcula e retorna o hash sha256 de uma cadeia de caracteres.

+++Sintaxe

```sql
{%= sha256(string) %} : string
```

**Exemplo**

```sql
{%= sha256("Eliechxh")%}
```

Retorna `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### split {#split}

Use a função `split` para dividir uma cadeia de caracteres por um determinado caractere.

+++Sintaxe

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

Use a função `startsWith` para determinar se uma sequência de caracteres inicia com uma subsequência especificada.

+++Sintaxe

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, está definido como verdadeiro. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com `Joe`.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

A função `stringToDate` converte um valor de cadeia de caracteres em um valor de data-hora. Leva dois argumentos: representação de string de uma representação de data-hora e representação de string do formatador.

+++Sintaxe

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

Use a função `string_to_integer` para converter um valor de cadeia de caracteres em um valor inteiro.

+++Sintaxe

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Use a função `stringToNumber` para converter uma cadeia de caracteres em número. Ele retorna a mesma string que a saída para entrada inválida.

+++Sintaxe

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Use a função `substr` para retornar a subcadeia de caracteres da expressão de cadeia de caracteres entre o índice inicial e o índice final.

+++Sintaxe

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Use a função `titleCase` para colocar as primeiras letras de cada palavra de uma cadeia de caracteres em maiúsculas.

+++Sintaxe

```sql
{%= titleCase(string) %}
```

**Exemplo**

Se a pessoa mora na Washington High Street, essa função retornará `Washington High Street`.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Use a função `toBool` para converter um valor de argumento em um valor booleano, dependendo de seu tipo.

+++Sintaxe

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Use a função `toDateTime` para converter a cadeia de caracteres em data. Retorna a data da época como saída para entrada inválida.

+++Sintaxe

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Use a função `toDateTimeOnly` para converter um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida. Esta função aceita os tipos de campo string, date, long e integer.

+++Sintaxe

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

A função `trim` remove todos os espaços em branco do início e do fim de uma cadeia de caracteres.

+++Sintaxe

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

A função `upperCase` converte uma cadeia de caracteres em letras maiúsculas.

+++Sintaxe

```sql
{%= upperCase(string) %}
```

**Exemplo**

Esta função converte o sobrenome do perfil em letras maiúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Use a função `urlDecode` para decodificar uma cadeia de caracteres codificada em URL.

+++Sintaxe

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Use a função `urlEncode` para codificar uma cadeia de caracteres como uma URL.

+++Sintaxe

```sql
{%= urlEncode(string) %}: string
```

+++
