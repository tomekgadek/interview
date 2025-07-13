# interview

Popularne pytania rekrutacyjne na stanowisko **Junior Java Developer**

### Bazy danych

Jakie mamy rodzaje złączeń?

Odp: inner join, left (outer) join, right (outer) join, full join.

Co takkego dodasz, aby przyśpieszyć wyszukiwanie na kolumnie?

Odp: Aby przyspieszyć wyszukiwanie po kolumnie w bazach danych, dodajemy indeks (index) na tej kolumnie.

Co takiego może się wydarzyć, gdy będzie nadmiar indeksów?

Odp: Może wystąpić spadek wydajności podczas operacji modyfikujących dane.

Podaj definicję transakcji?

Odp: Zbiór operacji na bazie danych, które w istocie stanowią pewną całość i jako takie powinny być wykonane wszystkie lub żadna z nich. Transakcja składa się z 3 etapów: rozpoczęcia, wykonania, zamknięcia.

Co to jest ACID?

Zbiór właściwości gwarantujących poprawne przetwarzanie transakcji w bazach danych.

A - atomicity (niepodzielność) | Albo transakcja się wykona albo nie.
C - consistency (spójność) | Po wykonaniu transakcji nie będzie naruszona integralność bazy danych.
I - isolation (izolacja) | Jeśli dwie transakcje wykonują się współbieżnie to zwykle nie widzą wprowadzonych przez siebie zmian.
D - durability (trwałość) | System potrafi uruchomić się i udostępnić spójne, nienaruszone aktualnie dane zapisane w ramach zatwierdzonych transakcji.

