# Metody rozwiązywania układów równań liniowych
Układów równań liniowych jest to wynik koniunkcji przynajmniej dwóch równań z niewiadomymi. W programowaniu układ równiań liniowych sprowadzamy do notacji wektorowej opisując ją za pomocą macierzy. 

Podstawową metodą rozwiązywania układów równań jest przekształcanie danego układu w inny, który ma ten sam zbiór rozwiązań – układy takie nazywa się równoważnymi. Operacje elementarne które wykożystujemy na macierzach to:
- dodanie do równania innego równania pomnożonego przez liczbę,
- zamiana dwóch równań miejscami,
- pomnożenie równania przez liczbę różną od zera.


1. metody eliminacyjne, do których zaliczamy:
   -  metodę eliminacji Gaussa,
   -  metodę rozkładu L U, 
   -  metodę Choleskiego-Banachiewicza 
2. metody iteracyjne, do których należą:
   -  metoda Jacobiego, 
   -  metoda Gaussa – Seidla



#### występują 2 grópy metod:
- metody dokładne: Jeśli rozwiązanie układu równań polega na takim przekształceniu danych, że po wykonianiu działań arytmetycznych po skończonej liczbie działań otrzymujemy rozwiązanie rozwiązanie bez zaokrogleń.
- metody iteracyjne gdzie przybliżone rozwiązanie wprowadzamy do wzoru iteracujnego i wynik tego działania wprowadzamy ponownie do wzoru iteracujnego i powtarzając do momętu aż otrzymamy wynik którego różnica pomiędy otrzymanym a wcześniejszym wynikiem jest dla nas wyztarczająca.

- Oba algorytmy opisano w przypadku, gdy układ jest oznaczony. Jeśli układ jest sprzeczny, to uzyskuje się (co najmniej jedno) równanie sprzeczne, które mówi o sprzeczności całego układu. 
- Jeśli układ jest nieoznaczony, to niektóre zmienne przenosi się do prawych części równań i rozwiązanie podaje się w postaci wyrażania jednych zmiennych przez inne 

#### lista wysztkich metod:
- Metoda wyznaczników
- Metoda podstawienia
- Redukcja wsteczna
- Metoda Cramera
- Metoda Cholesky’ego
- Metoda Givensa
- Eliminacja Gausa
- Metoda JordanaGaussa

## Eliminacja Gausa 
Metoda eliminacji Gaussa, w której układ przekształca się do równoważnego z nim układu równań z rosnącą liczbą zmiennych;
Służy na obliczania rzędu macierzy, obliczania macierzy odwrotnej, obliczania wartości wyznacznika oraz wyznaczenia rozkładu LU, wykorzystujący operacje elementarne

## Metoda JordanaGaussa
Metoda eliminacji Gaussa-Jordana, w której układ przekształca się dalej (poprzez kolejne podstawienia równań z mniejszą liczbą zmiennych do tych z większą) do równoważnego z nim układu równań liniowych wiążących bezpośrednio każdą zmienną z pewną wartością.

## Metoda LU 
Metoda rozwiązywania układu równań liniowych. polegająca na macierzy trójkątnych, dolnotrójkątnej (dolnej) i górnotrójkątnej (górnej). Metoda pozwala także na szybkie wyliczenie wyznacznika macierzy układu. 

Żeby ten rozkład macierzy był jednoznaczny, zakłada się, że elementy na głównej przekątnej jednej z macierzy, L albo U są równe 1. Podczas obliczeń może wystąpić dzielenie przez zero. 

### Rozkład LU jest wyznaczany za pomocą metody Doolittle’a

Występuje tutaj częściowy wybór elementu podstawowego, czyli  element w macierzy **A**, który jest używany do zerowania odpowiadających współczynników z kolejnych równań. Przy stosowaniu metody Doolittle’a wybiera się element podstawowy zawsze z przekątnej głównej, i jeśli **a***kk*  jest równe zero, metoda zawodzi.

W metodach zmodyfikowanych wybierany jest ten element z danej **k**-tej kolumny, który ma największy moduł. Następnie wiersz, w którym znajduje się wybrany element, zamieniany jest z **k**-tym wierszem, co powoduje, że element podstawowy pojawia się na przekątnej głównej. To gwarantuje, że podczas obliczeń nie wystąpi dzielenie przez zero.

##  Metoda iteracyjna
Metody iteracyjne (przybliżone) służą obliczaniu przybliżonych wartości pierwiastków układu równań liniowych za pomocą kolejnych aproksymacji(powtórzeń). W tym celu należy przyjąć pewien dowolny wektor **`x(0)`** jako rozwiązanie początkowe i według określonego schematu tworzyć kolejno ciąg wektorów **`x(1), x(2),..., x(n),...`** tak, aby wektor **`x(n+1)`** lepiej przybliżał rozwiązanie dokładne od wektora **`x(n)`**.

Każda metoda iteracyjna dotycząca rozwiązania problemu **`F(x) = 0`** , do poprawnego zdefiniowania wymaga podania dwóch informacji: <br/>1. funkcji iteracyjnej, czasem nazywanej równieżschematem iteracyjnym, <br/>2. warunku lub warunków zakończenia obliczeń. 

Funkcja iteracyjna służy do wyznaczenia kolejnego, lepszego w sensie pewnych norm (wystarczająco dobrego) przybliżonego wyniku, poszukiwanego na podstawie rozwiązania poprzedniego natomiast warunki zakończenia obliczeń służą do stwierdzenia, czy ostatnio znalezione przybliżenie jest na tyle dobre, aby obliczenia zakończyć. 

#### O ile funkcja iteracyjna zależy ściśle od klasy problemu i metody jego rozwiązania, o tyle warunki zakończenia obliczeń zwykle należą do dwóch kategorii:
1. **błąd zbieżności**, rozumiany jako iloraz normy z zmiany rozwiązania na podstawie ostatnio wykonanym kroku iteracyji oraz założeń z bieżącego rozwiązania
2. **błąd residuum**, rozumiany jako iloraz normy z wyrażenia **`F(x)`** obliczonej dla rozwiązania bieżącego i rozwiązania początkowego. 

### Metody:
- Metoda Jacobiego
- Gaussa-Seidela
