# interview

Popularne pytania rekrutacyjne na stanowisko **Junior Java Developer**

### Bazy danych

**Jakie mamy rodzaje złączeń?**

> inner join, left (outer) join, right (outer) join, full join.

**Co takkego dodasz, aby przyśpieszyć wyszukiwanie na kolumnie?**

> Aby przyspieszyć wyszukiwanie po kolumnie w bazach danych, dodajemy indeks (index) na tej kolumnie.

**Co takiego może się wydarzyć, gdy będzie nadmiar indeksów?**

> Może wystąpić spadek wydajności podczas operacji modyfikujących dane.

**Podaj definicję transakcji?**

> Zbiór operacji na bazie danych, które w istocie stanowią pewną całość i jako takie powinny być wykonane wszystkie lub żadna z nich. Transakcja składa się z 3 etapów: rozpoczęcia, wykonania, zamknięcia.

**Co to jest ACID?**

> Zbiór właściwości gwarantujących poprawne przetwarzanie transakcji w bazach danych.

> A - atomicity (niepodzielność) | Albo transakcja się wykona albo nie.

> C - consistency (spójność) | Po wykonaniu transakcji nie będzie naruszona integralność bazy danych.

> I - isolation (izolacja) | Jeśli dwie transakcje wykonują się współbieżnie to zwykle nie widzą wprowadzonych przez siebie zmian.

> D - durability (trwałość) | System potrafi uruchomić się i udostępnić spójne, nienaruszone aktualnie dane zapisane w ramach zatwierdzonych transakcji.

**Jakie mamy poziomy izolacji transakcji (model ANSI)?**

> *read uncommitted* – jedna transakcja może odczytywać wiersze, na których działają inne transakcje (najniższy poziom izolacji).

> *read committed* – transakcja może odczytywać tylko wiersze zapisane.

> *repeatable read* – transakcja nie może czytać ani zapisywać na wierszach odczytywanych lub zapisywanych w innej transakcji.

> *serializable (szeregowalne)* – wyniki współbieżnie realizowanych zapytań muszą być identyczne z wynikami tych samych zapytań realizowanych szeregowo (pełna izolacja).

**Co to jest relacja?**

> Relacje bazy danych są powiązaniami między tabelami, które są tworzone na podstawie instrukcji łączenia w celu odtworzenia danych.

**Co to jest 'klucz główny'?**

Unikalna wartość identyfikująca jednoznacznie każdy rekord tabeli (klucz może być złożony).

**Co to jest 'klucz obcy'?**

Wykorzystuje się go do tworzenia powiązania pomiędzy parą tabel, gdzie w jednej tabeli ten zbiór atrybutów jest kluczem obcym, a w drugiej kluczem głównym (referencja do tabeli).

### Java

**W jaki spsób możemy tworzyć wątki?**

Implementujemy interfejs *Runnable* lub dziedziczymy po klasie *Thread*.

**Strumienie Java - kiedy tak naprawdę się wykonują?**

W Javie strumienie (Stream) są leniwe (*lazy evaluation*), co oznacza, że operacje na strumieniach nie są wykonywane natychmiast. Wykonują się dopiero w momencie wywołania operacji terminalnej (np. forEach(), collect(), count(), findFirst(), anyMatch(), allMatch(), reduce()).

**Który fragment kodu będzie bardziej wydajny?**

```java
String name1 = "abc"; // 1
String name2 = new String("abc"); // 2
```

Bardziej optymalna będzie wersja `1`. Wykorzystywany jest tzw. **string pool**. Jest to specjalny obszar w pamięci, gdzie przechowywane są literały tekstowe. Wersja `2` tworzy nowy obiekt.

**Jaki wyjątek przerwie transakcję? (np. przy użyciu JPA, Hibernate i Spring)**

Wyjątek niekontrolowany. Może to być wyjątek **RuntimeException** i wszystkie jego podklasy.

**Jakie mamy rodzaje wyjątków w Java?**

Mamy `2` rodzaje wyjątków w Java:

+ Checked exceptions (sprwdzane, np. IOException - dziedziczące po Exception).
+ Unchecked exceptions (niesprawdzane, np. NullPointerException - dziedziczące po RuntimeException).

**Czy kluczem w mapie może być obiekt?**

Tak, w Javie obiekt może być kluczem w mapie (np. w HashMap, TreeMap, LinkedHashMap). Nie musi to być **String** czy **Integer**.

Nie zapominamy o poprawnym nadpisaniu **equals()** i **hashCode()**. Zadbajmy o to, aby obiekt był niemutowalny. Gdy chcemy skorzystać z takiej opcji dla **TreeMap** to nie zapominamy zaimplementować interfejsu **Comparable** lub **Comparator**.

### Git

**Co to jest rebase?**

**git rebase** to alternatywa dla merge, która przepisuje historię commitów, aby uzyskać czystą, liniową historię zmian.

### Spring

**Jakie mamy rodzaje wstrzykiwania zależności (DI)?**

W Spring Framework istnieją trzy główne rodzaje wstrzykiwania zależności:

+ Konstruktor,
+ Setter,
+ Pole.
