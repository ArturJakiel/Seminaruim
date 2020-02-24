# Projektowanie aplikacji typu klient-serwer.

Architektura klient-serwer to tzw. architektura dwu-warstwowa. W systemie zorganizowanym w tej architekturze wyróżnia się dwa typy komponentów: serwer i klient. Klient łączy się do serwera, który z kolei udostępnia zasoby. Można powiedzieć, że serwer dostarcza usług swojemu klientowi. Z reguły do serwera podłącza się większa liczba klientów.

Komunikacja pomiędzy serwerem oraz klientami odbywa się za pomocą konkretnego protokołu rozumianego przez obie strony. Mogą to być standardowe protokoły typu np. HTTP, SMTP, FTP.

Klient z reguły zawiera interfejsy użytkownika, a serwer posiada dostęp do bazy danych.

Najbardziej popularne dzisiaj rozwiązania architektury klient-serwer to oczywiście sieć www, gdzie rolę serwerów pełnią serwery www a rolę klientów: przeglądarki internetowe.

Architektura klient-serwer posiada następujące zalety:
- Jest stosunkowo prosta w implementacji
- Umożliwia łatwe zarządzanie oprogramowanie serwera, a w szczególnym przypadku jeżeli jest to serwer www i cała aplikacja znajduje się na serwerze, osoby upoważnione w prosty sposób mogą wprowadzać jej modyfikacje/aktualizacje
- Jeżeli serwer przechowuje dane to architektura klient-serwer podnosi poziom ich bezpieczeństwa, gdyż nie są one rozproszone po innych często nieznanych węzłach, na których działa oprogramowanie klienta oraz
- Daje możliwość łatwiejszego zarządzania tymi danymi jako, że baza danych jest scentralizowana.

Jeżeli chodzi o wady to przede wszystkim architektura ta jest mało elastyczna i słabo rozszerzalna, dlatego dzisiaj często wybiera się rozwiązania N>2 warstwowe (N-tier).
