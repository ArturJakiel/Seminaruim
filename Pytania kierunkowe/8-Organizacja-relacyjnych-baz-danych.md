# Organizacja relacyjnych baz danych.

Relacyjna baza danych to opisany i zorganizowany zbiór tabel połączonych relacjami między sobą. Ten sposób przechowywania informacji pozwala na uniknięcie powtarzania się danych oraz przeprowadzanie analiz na podstawie wielu tabel.

Każda tabela składa się z rekordów (tak nazywamy pojedyncze wiersze). Poszczególne rekordy składają się z pól (komórek), przechowujących jedną daną.

Aby istniała możliwość utworzenia z tabel relacyjnego modelu danych, przynajmniej w jednej z nich musi występować klucz główny –  kolumna służąca do identyfikacji poszczególnych rekordów tabeli. Wartości w kluczu podstawowym muszą być unikalne, aby istniała możliwość przypisania jednego wiersza tabeli do jednej wartości klucza.

Relację ustanawiamy pomiędzy dwoma tabelami na podstawie wartości klucza podstawowego pierwszej tabeli oraz tzw. klucza obcego drugiej tabeli.

### Baza danych jest relacyjna w momencie gdy spełnia 12 postulatów Codda czyli:
- **Postulat informacyjny** – dane są reprezentowane jedynie poprzez wartości atrybutów wierszach tabel. 
- **Postulat dostępu** – każda wartość w bazie danych jest dostępna poprzez podanie nazwytabeli, atrybutu i wartości klucza podstawowego. 
- **Postulat dotyczący wartości NULL** - dostępna jest specjalna wartość NULL dla reprezentacji zarówno wartości nieokreślonej, jak i nieadekwatnej.
- **Postulat dotyczący katalogu** – wymaga się, aby system obsługiwał wbudowany katalog relacyjny z bieżącym dostępem dla uprawnionych użytkowników.
- **Postulat języka danych** – system musi dostarczać pełny język przetwarzania danych, który może być używany zarówno w trybie interaktywnym, jak i w obrębie programów aplikacyjnych, obsługuje operacje definiowania danych, operacje manipulowania danymi,ograniczenia związane z bezpieczeństwem i integralnością oraz operacje zarządzania transakcjami. 
- **Postulat modyfikowalności perspektyw** – system musi umożliwiać modyfikowanieperspektyw, o ile jest ono semantycznie realizowalne. 
- **Postulat modyfikowalności danych** – system musi umożliwiać operacje modyfikacji danych, musi obsługiwać operatory INSERT, UPDATE oraz DELETE. 
- **Postulat fizycznej niezależności danych** – zmiany fizycznej reprezentacji danych i organizacji dostępu nie wpływają na aplikacje. 
- **Postulat logicznej niezależności danych** – zmiany wartości w tabelach nie wpływają na aplikacje. 
- **Postulat niezależności więzów spójności** – więzy spójności są definiowane w bazie i nie zależą od aplikacji.
- **Postulat niezależności dystrybucyjnej** – działanie aplikacji nie zależy od modyfikacji i dystrybucji bazy. 
- **Postulat bezpieczeństwa względem operacji niskiego poziomu** — operacje niskiego poziomu nie mogą naruszać modelu relacyjnego i więzów spójności.

### Klucze 
**Klucz kandydujący** to taki atrybut który posiada cechy jednoznaczności (jest unikalny dla dwóch wybranych krotek) oraz nieredukowalności(żaden z podzbiorów wybranych z danego atrybutu nie posiada cech jednoznaczności). Spośród nich wybieramy, **klucz główny** więc jest określenie na jeden wybrany klucz kandydujący jednak w większości przypadków jest to nowa kolumna. **Klucz obcy** to nowy atrybut dla krotki zawierający jej identyfikator, czyli jej klucz główny. Dzięki takim połączeniom uzyskujemy 3 rodzaje powiązań pomiędzy tabelami. 

### Wyróżniamy trzy rodzaje relacji:
- **jeden do jednego** – jednemu rekordowi z tabeli A odpowiada tylko jeden wiersz z tabeli B. Rodzaj ten występuje stosunkowo rzadko, ponieważ wszystkie informacje przechowywane w ten sposób można zamieścić w jednej tabeli.
- **jeden do wielu** – jednemu rekordowi z tabeli A odpowiada wiele rekordów z tabeli B. Jest to najpowszechniejszy typ relacji.
- **wiele do wielu** – rekord w tabeli A może mieć wiele dopasowanych wiele wierszy z tabeli B oraz odwrotnie. Taki typ jest możliwy do zdefiniowania tylko poprzez dodanie do modelu trzeciej tabeli (zwanej tabelą łącza), w której będą znajdowały się wartości kluczy podstawowych tabel A oraz B.
