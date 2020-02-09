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
