# Projektowanie aplikacji internetowych w architekturze wielowarstwowej.

## Projektowanie aplikacji internetowych w architekturze wielowarstwowej.
### Najprostsza wersja dwie warstwy:
  - **Klient** - Prezentacja danych i interfejs użytkownika, przesyłanie żądań do serwera.
  - **Serwer** - Odbieranie i przetwarzanie żądań od klienta, zarządzanie i przechowywanie danych.

Jest on prosty i szybki w implementacji jednak ze względu na przechowywanie dużej ilości informacji/logiki nie są przyjazne rozbudowie, rozmiary klienta stają się za dużo a jego niezawodność i efektywność spada. Kolejnym problemem jest to, że każdy klient musi oddzielnie otrzymać aktualizację, różne wersje klienta mogą prowadzić do niespójności w czasie pracy systemu. Można to rozwiązać poprzez zapisywanie reguł w plikach DLL lub wykorzystać mechanizmy wyzwalaczy i procedur wbudowanych w bazie danych. Można nazwać t wtedy architekturą dwu i pół warstwową.

### Architektura trójwarstwowa
O architekturę 3-warstwową opiera się aktualnie wiele aplikacji internetowych. W architekturze tej wyróżnia się następujące warstwy:

  - **Warstwa prezentacji _(front-end)_** -  Interfejs użytkownika, Odpowiedzialny za interakcję z użytkownikiem końcowym (wyświetlanie i wprowadzanie danych). W tej warstwie działają aplikacje klienckie takie jak np. przeglądarki internetow
  - **Warstwa serwerów aplikacji _(back-end)_** - Zawiera logikę aplikacji, odpowiada za komunikację z bazą danych i przesyłanie danych do warstwy prezentacji. Może zawirać także wszystkie inne elementy. Tutaj też przygotowywane są dane wysłane  do warstwy prezentacji (aplikacji klienckich). W tej warstwie realizowane są wszelkiego rodzaju funkcjonalności biznesowe. Z drugiej strony logika warstwy odpowiedzialna jest za komunikację z warstwą danych. Warstwa biznesowa stanowi swego rodzaju pomost pomiędzy warstwą aplikacji i warstwą danych dodając elementy przetwarzania.
  - **Warstwa danych** - odpowiedzialna za przechowywane danych. W tej warstwie mamy np. bazę danych.
  
### Istnieją także architektury o większej ilości warstw.
Reasumując, architektura 3-warstwowa to architektura aktualnie najbardziej popularna w rozwiązaniach dla aplikacji web. Systemy informatyczne mogą być jednak zbudowane z różnej liczby warstw. Realizujących wymagane specyficzne funkcjonalności.

#### Zalety architektury warstwowej
- **modyfikowalność** - separacja danego typu funkcjonalności w ramach pojedynczej warstwy, a zmiany w jednej warstwie nie wymuszają zmian w pozostałych (przy zachowaniu niezmienności interfejsów modyfikowanej warstwy)
- **prostota wykorzystania warstwy** - komunikacja pomiędzy warstwami odbywa się przez wyznaczone i dobrze zdefiniowane punkty styku (interfejsy) - sama implementacja mechanizmów warstwy jest ukryta, co też wpływa ogranicza możliwość popełnienia błędów (np. poprzez wywoływanie niedozwolonych - wewnętrznych - funkcjonalności)
- **spójność i przejrzystość** - każda z warstw realizuje konkretne (spójne logicznie) funkcje i komunikuje się tylko i wyłącznie z warstwami znajdującymi się bezpośrednio nad i pod nią
- **wielokrotne wykorzystanie** - konkretne warstwy można bezpośrednio wykorzystywać w wielu aplikacjach (np. ta sama warstwa biznesowa i dwie różne warstwy prezentacji jedna na potrzeby przeglądarki internetowej a druga aplikacji mobilnej).

### Wady architektury warstwowej
dodatkowe warstwy mogą wpływać na wydajność aplikacji (dodatkowe operacje związane z odebraniem danych z poprzedniej warstwy i przygotowaniem danych do przekazania do kolejnej warstwy, dodatkowe transakcje i synchronizacja).
