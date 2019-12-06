# Metody przetwarzania i rozpoznawania obrazów

## Cyfrowa reprezentacja obrazu
Każdy obraz można przedstawić za pomocą nieskończenie wielu wartości. Reprezentacja takiego obrazu sprowadza się w systemach dyskretnych do przybliżenia wartości danego fragmentu obrazu analogowego do możliwie dokładnej wartości cyfrowej, którą komputer będzie w stanie zapisać i odczytać.

Konwersja obrazów rzeczywistych na postać cyfrową polega na próbkowaniu obrazu i kwantowaniu próbek. Próbkowanie obrazu polega w uproszczeniu na narzuceniu siatki prostokątnej na obraz. Każdy węzeł takiej siatki stanowi jeden punkt obrazu wyjściowego.

Zmieniając rozmiary tej siatki można modyfikować rozdzielczość obrazu, czyli dokładność odwzorowania jego struktury. Za dokładność odwzorowania barw tego obrazu odpowiada ilość bitów przypadających na jeden piksel.

## Metody przetwarzania

Przetwarzanie obrazów zakłada istnienie obrazu, na którym będą wykonywane jakieś operacje. Te operacje pozwalają ulepszyć a także zmodyfikować obraz dla własnych potrzeb.

Znanych jest wiele różnych metod przetwarzania obrazów. Ogólnie można wyróżnić wśród nich kilka podstawowych grup. Są to: 
- przekształcenia geometryczne, 
- przekształcenia punktowe, 
- przekształcenia z wykorzystaniem filtrów, 
- przekształcenia widmowe
- przekształcenia morfologiczne.

### Przekształcenia geometryczne
Typowe dla tych przekształceń to przesunięcia, odbicia, obroty, skalowanie. Zaliczamy do nich również kadrowanie obrazów. Operacje te bazują na działaniach macierzowych na zmiennych określających położenie pikseli w obrazie.

- przesunięcie równoległe,
- symetria środkowa,
- obrót,
- symetria osiowa,
- jednokładność,
- powinowactwo osiowe,
- przekształcenie liniowe i afiniczne.

### Przekształcenia punktowe
Przekształcenia punktowe operują na pojedynczych pikselach niezależne od ich sąsiednich pikseli. Przykłady takich operacji to: negatyw, konwersja na skalę szarości, progowanie czy zmiana poziomów jasności.

### Przekształcenia wykorzystujące filtry
Tę grupę przekształceń tworzą przekształcenia wykorzystujące sąsiedztwo pikseli. Operacje tego typu wykonuje się stosując odpowiednie filtry lub maski. Istotę operacji wyjaśnia rysunek.

Operację wykonuje się na każdym pikselu obrazu wejściowego. Wynik operacji zapisuje się w nowym docelowym obrazie. Tytułowe filtry to tzw. maski. Są to najczęściej kwadratowe tablice wartości. 

## Rozpoznawanie obrazów
Cyfrowe przetwarzanie obrazu jest generowanie opisu cyfrowy obrazu w celu dalszego przetwarzania. Przykładem takiego działania jest OCR czy też OMR. Dalsze przetwarzanie i ostateczna klasyfikacja obrazu częstokroć dokonywana jest przy wykorzystaniu metod inteligencji obliczeniowej.

### Rodzaje rozpoznawania obrazu 
Klasyczny problem w wizji komputerowej, przetwarzaniu obrazu i wizji maszynowej polega na określeniu, czy dane obrazu zawierają określony obiekt, cechę lub aktywność.

- rozpoznawanie twarzy
- rozpoznawanie pisma, druku
- rozpoznawanie wzorców 
- analiza ruchu
  - Egomotion
  - Śledzenie (tracking)
  - Ruch optyczny
- rekonstrukcja sceny
- odbudowa obrazu

### Metody klasyfikacji obiektów, wzorców
Jednym z etapów rozpoznawania obrazów jest klasyfikacja obiektu, o którym udało nam się zebrać odpowiednie, niezbędne informacje, do odpowiedniej predefiniowanej przez nas grupy. Np. obiekt, który ma cztery średniej długości proste i cienkie nogi, na których znajduje się prostokątna pozioma płaszczyzna, który także posiada prostopadłą do niej druga płaszczyznę, w większości przypadków zostałby zaklasyfikowany jako krzesło.

W tym momencie możemy powiedzieć, że naszym zadaniem jest na podstawie pozyskanych z obrazu cech obserwowanego obiektu zaklasyfikować go do odpowiedniej klasy obiektów, np. do krzeseł.

#### Metoda decyzyjno-teoretyczne
Za Reprezentowanie cech obiektu za pomocą wektorów. Cechy te możemy wyznaczyć samemu na podstawie wstępnej analizy obiektu, która ma na celu wyłonienie istotnych cech, bądź mogą być ona nam narzucone z góry. Mają one na celu ułatwienie nam jednoznacznego rozpoznania obiektu. Wartości cech mogą pochodzić bezpośrednio z przeprowadzonych pomiarów, próbkowania fali, czy skanowania obrazu w odpowiednim obszarze (zależnie od przypadku). Za pomocą wyznaczonego wektora cech przypisanego do konkretnego obiektu możemy jednoznacznie określić położenie tego obiektu w przestrzeni cech, która ma tyle wymiarów ile liczb zawiera wektor (ile jest cech).

Przestrzeń cech jest z góry podzielona w taki sposób, aby odpowiednie jej regiony opisywały obiekty jednej klasy, np. krzesła, albo niebo. Regiony takie nazywane są obszarami decyzyjnymi i każdy punkt, wyznaczony przez odpowiedni wektor, znajdujący się wewnątrz tego samego obszaru klasyfikowany jest do tej samej grupy/klasy.

#### Metoda strukturalna
Wzorzec, opisywany jest za pomocą ogromnej, ale skończonej ilości "słów" kluczowych, które określą elementy budują obiekt. Nie ma więc już w sensie stricto wektora cech zbudowanego z liczb określającego pojedyncze cechy obiektu W tym podejściu problem rozpoznania obiektu na obrazie sprowadzony jest więc do odpowiedzi na pytanie: czy dany wzór przynależy do języka tworzonego przez zdefiniowaną przez nas gramatykę?

