# Metody rozwiązywania funkcji logicznych w algebrze Boole'a.

## Algebra Boole'a 
  określa działania na dwuelementowym zbiorze {prawda, fałsz} odpowiadającemu zbiorowi {0,1}, na którym określono podstawowe działania: sumy, iloczynu i negacji oraz podstawowe prawa: przemienności, łączności, rozdzielności i De Morgana. 

**Minimalizacja funkcji boolowskich** polega na znalezieniu dla danej funkcji formuły minimalnej, która jest jak najmniej skomplikowana. 

### Jeśli funkcja ma małą liczbę zmiennych (od 2 do 6) można zastosować tutaj

**Metodę tablic Karnaugha** - jest to metoda graficzna zapisana w specjalnej tablicy zwanej mapą lub siatką Karnaugha, wówczas znalezienie minimalnej formuły odbywa się na drodze intuicyjnej. Dla większej ilości zmiennych staje się zbyt trudna i tu z pomocą przychodzą metody komputerowe np. **Metoda Quine’a-McCluskey’a** która jest bardziej wygodna dla większej ilości zmiennych jednak zakres jej zastosowań jest także ograniczony ponieważ problem, który rozwiązuje, jest trudny: czas działania algorytmu rośnie wykładniczo z rozmiarem zadania. Mechanizm działania tych metod jest prawie taki sam, tyle że Karnaugh jest graficzna, a McCluskeya tekstowa więc łatwiej ją zaimplementować w komputerze.

Najbardziej znaną i uznawaną za najskuteczniejszą jest metoda ESPRESSO opracowana w latach 80. Polega na iteracyjnym stosowaniu różnych procedur, z których najważniejsze to Ekspansja, Pokrycie nienadmiarowe i Uzupełnienie. Są to bardzo złożone procedury, których omówienie zajęło by dużo czasu.

## Etapy przy metodzie Karnaugh

Postępujemy według następujących punktów:

1. Funkcję należy przedstawić w postaci kanonicznej lub tabelarycznej.
2. Tworzymy tabelę dla odpowiedniej ilości zmiennych
3. W kratki tabeli wpisujemy wartości funkcji ("0", "1" lub "-") zgodnie z postacią funkcji.
4. Zakreślamy pola (grupy) w siatce tabeli zgodnie z następującymi zasadami:
   1. Pole jest kwadratem lub prostokątem o bokach będących potęgą 2
   2. Pola obejmują kratki sąsiednie, kratki skrajne (pola mogą być "zawinięte" przez brzeg tablicy)
   3. Grupy muszą objąć wszystkie "1".
   4. Grupy nie mogą obejmować "0".
   5. Stany nieokreślone "-" mogą, ale nie muszą być zakreślane.
   6. Grupy powinny być jak największe.
   7. Ilość grup powinna być możliwie mała.
   8. Grupy mogą na siebie zachodzić.
5. Odczytu funkcji wykonujemy według zasad:
   1. Jeżeli zmienna przyjmuje dla danego pola wartość 1 to piszemy ją wprost.
   2. Jeżeli zmienna przyjmuje dla danego pola wartość 0 to piszemy ją z negacją.
   3. Jeżeli zmienna przyjmuje dla danego pola wartości 0 i 1 (zmienia wartość), to jej nie piszemy.
