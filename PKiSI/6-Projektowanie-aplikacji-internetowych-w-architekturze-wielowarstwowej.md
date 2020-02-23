# Projektowanie aplikacji internetowych w architekturze wielowarstwowej.

## Projektowanie aplikacji internetowych w architekturze wielowarstwowej.
### Najprostsza wersja dwie warstwy:
  - **Klient** - Prezentacja danych i interfejs użytkownika, przesyłanie żądań do serwera.
  - **Serwer** - Odbieranie i przetwarzanie żądań od klienta, zarządzanie i przechowywanie danych.

Jest on prosty i szybki w implementacji jednak ze względu na przechowywanie dużej ilości informacji/logiki nie są przyjazne rozbudowie, rozmiary klienta stają się za dużo a jego niezawodność i efektywność spada. Kolejnym problemem jest to, że każdy klient musi oddzielnie otrzymać aktualizację, różne wersje klienta mogą prowadzić do niespójności w czasie pracy systemu. Można to rozwiązać poprzez zapisywanie reguł w plikach DLL lub wykorzystać mechanizmy wyzwalaczy i procedur wbudowanych w bazie danych. Można nazwać t wtedy architekturą dwu i pół warstwową.

### Architektura trójwarstwowa
  - **Warstwa prezentacji(front-end)** -  Interfejs użytkownika.
  - **Warstwa serwerów aplikacji** - Zawiera logikę aplikacji, odpowiada za komunikację z bazą danych i przesyłanie danych do warstwy prezentacji. Może zawirać także wszystkie inne elementy
  - **Warstwa serwerów danych** - Przechowywanie danych

> https://www.computerworld.pl/news/Kuchnia-architektury-klient-serwer-architektura-wielowarstwowa,293248,2.html


Jeżeli mówimy o architekturze warstwowej (ang. tier architectrue) to zawsze mamy na myśli architekturę n warstwową, gdzie n > 0.

Najbardziej popularne architektury warstwowe to:
- architektura jednowarstwowa (n = 1)
- architektura dwuwarstwowa (n = 2)
- architektura trójwarstwowa (n = 3)
Architektura jednowarstwowa
Całe oprogramowanie zamknięte jest w jednej "warstwie". Przykładem są proste aplikacje desktopowe.
 
Architektura dwuwarstwowa
Oprogramowanie podzielone jest na dwie warstwy - przykładem architektury dwuwarstwowej jest klient-serwer. Oprogramowanie klienta to jedna warstwa a serwera druga. Więcej informacji na temat architektury klient-serwer znaleźć można w dziale architektura klient-serwer.
 
Architektura trójwarstwowa
O architekturę 3-warstwową opiera się aktualnie wiele aplikacji internetowych. W architekturze tej wyróżnia się następujące warstwy:
Warstwa prezentacji (ang. presentation tier) - odpowiedzialna za interakcję z użytkownikiem końcowym (wyświetlanie i wprowadzanie danych). W tej warstwie działają aplikacje klienckie takie jak np. przeglądarki internetowe 
Warstwa biznesowa (ang. business tier) - odpowiedzialna za przetwarzanie danych (żądań) od użytkownika.  Tutaj też przygotowywane są dane wysłane  do warstwy prezentacji (aplikacji klienckich). W tej warstwie realizowane są wszelkiego rodzaju funkcjonalności biznesowe. Z drugiej strony logika warstwy odpowiedzialna jest za komunikację z warstwą danych. Warstwa biznesowa stanowi swego rodzaju pomost pomiędzy warstwą aplikacji i warstwą danych dodając elementy przetwarzania.
Warstwa danych (ang. persistance tier) - odpowiedzialna za przechowywane danych. W tej warstwie mamy np. bazę danych.
Czy istnieją architektury więcej niż 3-warstwowe?
Tak. Istnieją takie architektury. Jedną z bardziej znanych architektur jest model ISO OSI RM (ang. ISO Open Systems Interconnection Reference Model), gdzie występuje 7 warstw.
W przypadku architeketury 4-warstwowej na pewno na uwagę zasługuje podejście "A Four-Tier Engagement Platform", proponowane przez Michael Facemire, John McCarthy.
 
W ramach aplikacji web można dokonać abstrakcyjnego podziału warstwy w modelu 3-warstwowym, np. w warstwie biznesowej wyróżnić  warstwę dostępu do danych (encje + DAO - ang. Data Access Object) oraz warstwę usługową, w której to zlokalizowana zostanie logika biznesowa aplikacji.
 
 
Reasumując, architektura 3-warstwowa to architektura aktualnie najbardziej popularna w rozwiązaniach dla aplikacji web. Systemy informatyczne mogą być jednak zbudowane z różnej liczby warstw. Realizujących wymagane specyficzne funkcjonalności. Decydując się na architekturę warstwową i wprowadzając kolejne warstwy należy mieć na uwadze zarówno zalety jak i wady takiego rozwiązania.
 



Zalety architektury warstwowej
Jeżeli chodzi o zalety architektury wielowarstwowej to wydaje się, być ich całkiem sporo. Główne zalety to przede wszystkim:
modyfikowalność - separacja danego typu funkcjonalności w ramach pojedynczej warstwy, a zmiany w jednej warstwie nie wymuszają zmian w pozostałych (przy zachowaniu niezmienności interfejsów modyfikowanej warstwy)
prostota wykorzystania warstwy - komunikacja pomiędzy warstwami odbywa się przez wyznaczone i dobrze zdefiniowane punkty styku (interfejsy) - sama implementacja mechanizmów warstwy jest ukryta, co też wpływa ogranicza możliwość popełnienia błędów (np. poprzez wywoływanie niedozwolonych - wewnętrznych - funkcjonalności)
spójność i przejrzystość - każda z warstw realizuje konkretne (spójne logicznie) funkcje i komunikuje się tylko i wyłącznie z warstwami znajdującymi się bezpośrednio nad i pod nią
wielokrotne wykorzystanie - konkretne warstwy można bezpośrednio wykorzystywać w wielu aplikacjach (np. ta sama warstwa biznesowa i dwie różne warstwy prezentacji jedna na potrzeby przeglądarki internetowej a druga aplikacji mobilnej).
 
Wady architektury warstwowej
Jeżeli chodzi o wady architektury warstwowej, to na co należy zwrócić uwagę to na pewno to, że:
dodatkowe warstwy mogą wpływać na wydajność aplikacji (dodatkowe operacje związane z odebraniem danych z poprzedniej warstwy i przygotowaniem danych do przekazania do kolejnej warstwy, dodatkowe transakcje i synchronizacja).
