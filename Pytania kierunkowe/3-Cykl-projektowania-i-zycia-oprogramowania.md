# Cykl projektowania i życia oprogramowania

## Podstawowe czynności związane z tworzeniem oprogramowania:
### Określenie wymagań i specyfikacji (Planowanie)
  Wymagania stanowią opis wykonywanych przez system funkcji oraz sposobów ich realizacji. Wymagania w teorii nie powinny zawierać szczegółów technicznych implementacji kodu lub samego projektu jednak w praktyce często muszą być one zawarte w wymaganiach. W tej fazie ważnym jest zebranie specyfiki od klienta. Klient jednak często nie rozumie specyfiki funkcjonowania programów a wykonawca nie zna specyfiki dziedziny zastosowań. Po zebraniu odpowiedniej listy wymagań musimy je podzielić na wymagania funkcjonalne oraz niefunkcjonalne. 

### Projektowanie
  W tej fazie rozstrzygane są wszystkie kwestie budowy systemu tak aby realizował postawione wymagania.  Na tym etapie fo fazie zbierania wymagań możemy zwrócić większą uwagę na potencjalną wydajność, niezwaodność oraz łatwoć konserwacji systemu. Powinniśmy także wzbogacić postawione wymagania o uszczegółowienie modeli obiektowych, zarządzania pamięicią, zarządzaniem danych i szczegółami interfejsu graficznego oraz nad możliwościami optymalizacji systemu. Jeżeli projektowanie realizujemy w metodologii obiektowej efektem tych prac powinien być szczegółowy model klas uwzględniający dziedziczenie, atrybuty oraz metody poszczególnych klas.
  
### Analiza
  etap gdzie powstaje szczegółowy projekt systemu spełniającego ustalone wcześniej wymagania użytkownika. Powstaje logika systemu, jego architektura, interfejsy.

### Implementacja
  Polega na napisaniu kodu źródłowego w oparciu o efekty poprzednich faz.
  Na tym etapie oprócz samego stworzenia kodu dochodzi także do ponownego użycia kodu z innych programów. Możemy wykorzystać gotowe komponenty lub fragmenty istniejącego kodu. Ważnym jest też zrozumienie ponownie wykorzystywanego kodu aby brak rozumienia nie generował dodatkowych błędów. W późniejszej fazie implementacji ważna jest także refaktoryzacja czyli zmniejszenie poprawa struktury klas i zawartości samych klas, często także skrócenie kodu z zachowaniem tej samej funkcjonalności.  

### Testowanie
  Testowanie polega na na wyłapaniu błędów w oprogramowaniu a także błędów jakie może popełnić użytkownik. Na tym etapie opró usunięcia błędów z kodu może dojść też do zmian w interfejsie użytkownika aby był on bardziej czytelny.

### Użytkowanie/Konserwacja (Pielęgnacja)
  Etap w który oprogramowanie trafia do klienta/użytkownika. Konserwacja oprócz wsparcia polega na usuwaniu nie znalezionych w trakcie testów błędów lub błędów powstałych w trakcie użytkowania systemu.

- **Model Kaskadowy**: Wyżej wymienione etapy w sztywnej kolejności.
- **Model ewolucyjny**: Podobny do kaskadowego jednak pozwala na powroty i korygowanie błędów popełnionych we wcześniejszych etapach
- **Prototypowanie**: Tworzenie prototypów z których pewne rozwiązania zostaną zastosowane w finalnym projekcie jednak każdy kolejny prototyp tworzymy od zera, tak samo jak i finalny projekt.
- **Wytwarzanie odkrywcze**: Wariant ewolucyjnego w którym klient otrzymuje coraz to bogatsze wersje oprogramowania. Polega na stałej modyfikacji kodu.

- **Przyrostowe**: kolejne pojedyncze etapy(przyrosty) w oprogramowaniu spełniające nowe zadania.
