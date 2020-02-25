# Scenariusze lub procedury testowe

### Scenariusze
**Scenariusz testowy**, (specyfikacja procedury testowej- test procedure specification, skrypt testowy) jest uporządkowanym zbiorem przypadków testowych, które są wykorzystywane do przetestowania określonej funkcjonalności systemu. Opisuje kolejność wykonywania przypadków testowych. Może również zawierać informacje dotyczące specjalnych wymagań (np. dla środowiska testowego), które muszą być spełnione przed wykonaniem danego zestawu testów. Schemat wykonywania procedur testowych jest określany mianem harmonogramu wykonania testu.

### Przykładowa organizacja specyfikacji procedury testowej:
1. Zbiory testów
   1. ogólny opis (jak poszczególne przypadki testowe są budowane w zbiory testów o wspólnym celu testowania);
   2. unikatowy identyfikator dla każdego zbioru testów;
   3. cel (jaki jest cel poszczególnych zbiorów testów);
   4. priorytet (jeśli konieczny);
   5. zawartość/śledzenie (lista identyfikatorów przypadków testowych wchodzących w skład poszczególnych zbiorów testów).
2.Procedury testowe
   1. ogólny opis procedur wyprowadzonych ze zbiorów testów;
   2. unikatowy identyfikator dla każdej procedury testowej;
   3. cel (jaki jest cel poszczególnych procedur testowych);
   4. priorytet (jeśli konieczny);
   5. konfiguracja początkowa (opisuje niezbędne do wykonania czynności przed uruchomieniem danej procedury testowej; zwykle zawiera opis warunków wstępnych dla pierwszego przypadku testowego);
   6. uruchamiane przypadki testowe (lista przypadków w kolejności ich uruchomienia);
   7. związek z innymi procedurami (opisuje zależności między tą a innymi procedurami testowymi, które np. wymuszają wykonanie całych procedur testowych w określonej kolejności);
   8. konfiguracja końcowa (opisuje niezbędne do wykonania czynności, jakie należy wykonać po zakończeniu procedury testowej, np. rozmontowanie środowiska testowego, wyczyszczenie bazy danych). 
