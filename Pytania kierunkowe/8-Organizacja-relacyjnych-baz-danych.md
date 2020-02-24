# Organizacja relacyjnych baz danych.

Relacyjna baza danych to opisany i zorganizowany zbiór tabel połączonych relacjami między sobą. Ten sposób przechowywania informacji pozwala na uniknięcie powtarzania się danych oraz przeprowadzanie analiz na podstawie wielu tabel.

Każda tabela składa się z rekordów (tak nazywamy pojedyncze wiersze). Poszczególne rekordy składają się z pól (komórek), przechowujących jedną daną.

Aby istniała możliwość utworzenia z tabel relacyjnego modelu danych, przynajmniej w jednej z nich musi występować klucz główny –  kolumna służąca do identyfikacji poszczególnych rekordów tabeli. Wartości w kluczu podstawowym muszą być unikalne, aby istniała możliwość przypisania jednego wiersza tabeli do jednej wartości klucza.

Relację ustanawiamy pomiędzy dwoma tabelami na podstawie wartości klucza podstawowego pierwszej tabeli oraz tzw. klucza obcego drugiej tabeli.

### Wyróżniamy trzy rodzaje relacji:
- **jeden do jednego** – jednemu rekordowi z tabeli A odpowiada tylko jeden wiersz z tabeli B. Rodzaj ten występuje stosunkowo rzadko, ponieważ wszystkie informacje przechowywane w ten sposób można zamieścić w jednej tabeli.
- **jeden do wielu** – jednemu rekordowi z tabeli A odpowiada wiele rekordów z tabeli B. Jest to najpowszechniejszy typ relacji.
- **wiele do wielu** – rekord w tabeli A może mieć wiele dopasowanych wiele wierszy z tabeli B oraz odwrotnie. Taki typ jest możliwy do zdefiniowania tylko poprzez dodanie do modelu trzeciej tabeli (zwanej tabelą łącza), w której będą znajdowały się wartości kluczy podstawowych tabel A oraz B.
