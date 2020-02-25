# Rola testowania oprogramowania w metodykach zwinnych wytwarzania oprogramowania

## Zwinne techniki wytwarzania oprogramowania
- Zdolność do szybkiej i sprawnej odpowiedzi na zmieniające się wymagania z kontrolą ryzyka
- Elastyczność i zdolność szybkiej i skutecznej adaptacji
- Osiągnięcie satysfakcji klienta poprzez szybkość wytwarzania oprogramowania
- Działające oprogramowanie jest dostarczane okresowo (tygodniowo, miesięcznie)
- Podstawową miarą postępu jest działające oprogramowanie
- Późne zmiany w specyfikacji nie mają destrukcyjnego charakteru na proces
wytwarzania oprogramowania 
- Bliska, dzienna współpraca pomiędzy biznesem a developmentem
- Bezpośredni kontakt jako najlepsza forma komunikacji w zespole i poza nim
- Ciągła uwaga nastawiona na aspekty techniczne oraz dobry projekt (design)
- Prostota
- Samozarządzalność zespołów
- Regularna adaptacja do zmieniających się wymagań

## Najpopularniejsze metodyki Agile wytwarzania oprogramowania:

### Kanban  
jest metodą zarządzania tworzeniem produktów, kładąc nacisk na ciągłe dostawy jednocześnie nie obciążając nadmiernie zespołu deweloperskiego pracą. Jest to proces mający na celu pomóc zespołom współpracować bardziej efektywnie.

Kanban opiera się na 3 podstawowych zasadach:
- **Wizualizację** tego co robisz dzisiaj (przepływ pracy): widzenie wszystkich elementów we wzajemnym kontekście może być bardzo pouczające 
- **Ogranicz** ilość pracy w toku: to pomaga zrównoważyć przepływ pracy więc zespół nie zaczyna i nie zobowiązuje się do zbyt dużej pracy w tym samym czasie 
- **Zwiększenia** przepływu: kiedy coś jest skończone, rozpoczynana jest następna najważniejsza rzecz z rejestru zadań

> Kanban sprzyja stałej współpracy i zachęca do aktywnej, ciągłej nauki i doskonalenia poprzez określenie najlepszego możliwego przepływu pracy zespołowej.

### Lean 
just in time, minimalizowanie wydatków, kosztów, jak najwięcej wyprodukować. tylko to co teraz potrzebujemy bez zapasów. 

### Siedem zasad Lean:
- Eliminacja strat (ang. Eliminate Waste)
- Tworzenie jakości i spójności (ang. Build Quality In)
- Wzmocnienie pozyskiwania wiedzy (ang. Create Knowledge)
- Podejmowanie decyzji najpóźniej, jak to możliwe (ang. Defer Commitment)
- Wdrażanie najwcześniej, jak to możliwe (ang. Deliver Fast)
- Respektowanie zespołu (ang. Respect People)
- Spojrzenie na całość (ang. Optimize the Whole)

### XP - eXtreme Programming
tworzenie małych i średnich "projektów wysokiego ryzyka", czyli takich, w których nie wiadomo do końca, co się tak naprawdę robi i jak to prawidłowo zrobić. Przyświeca temu koncepcja prowadzenia projektu informatycznego, wywodząca się z obserwacji innych projektów, które odniosły sukces.

**Cechy**:
- Ciągłe modyfikacje architektury
- Testy podzespołów
- Stały kontakt z klientem

## SCRUM
Kładzie szczególny nacisk na wykorzystywanie informacji zwrotnej z etapu na etap, na samoorganizację zespołów, a przede wszystkim, na wytworzenie przetestowanych, działających i dających się użyć „przyrostów” produktu.

- Wszystko to jest realizowane w krótkich, najczęściej 2-3 tygodniowych odcinkach czasów, zwanych „sprintami”.
Jest opartym o empiryzm, zwinnym (ang. agile) sposobem planowania i kontrolowania przebiegu prac projektowych.
- Jest iteracyjnym i inkrementalnym sposobem wytwarzania oprogramowania (szczególnie o wysokim stopniu złożoności i/lub ryzyka).
- Jest narzędziem porządkującym i kontrolującym interesy osób zaangażowanych w realizację projektu.
- Jest narzędziem porządkującym komunikację i maksymalizującym stopień współpracy wewnątrz– i pozazespołowej.
- Jest opartym o samoorganizację sposobem zwiększania produktywności zespołu prowadzi do głębokich strukturalnych przemian organizacji mających na celu jej uzwinnienie i wyszczuplenie.
- Nie wprowadza nowych i nie interferuje z już stosowanymi praktykami inżynierskimi.
- Jest skalowalny od pojedynczych zespołów do całych organizacji i przedsiębiorstw

### Testowanie w Agile
- Skupienie się i uznanie za priorytetowe traktowanie wymagań opartych na ryzyku, ponieważ nie jest możliwe przeanalizowanie wszystkiego
- Automatyzacja testów w celu zwiększenia wydajności
- Częstsze wykorzystywanie testów eksploracyjnych, by zmniejszyć czas pomiędzy dostarczeniem kodu a wykonaniem testów, jednocześnie podkreślając potrzebę tworzenia działającego kodu
- Przystosowanie do zmian od sprintu do sprintu

### Testowanie w SCRUM
- Powinno być integralną częścią procesu wytwórczego tzn. nie powinno być kierowane do odrębnego procesu, dedykowanych Sprintów czy specjalistycznych zespołów.
- Jedną z koncepcji SCRUM jest Test Driven Development (TDD) łącząca proces kodowania systemu z tworzeniem testów dla tej funkcjonalności. Testy, dane testowe, scenariusze testów jednostkowych mają powstawać przed lub ewentualnie w trakcie samego kodowania.
- Testowanie nie powstrzymuje wypuszczenia produktu na rynek ale pozwala na postęp projektu
- Tester dostarcza feedback i dodatkowe informacje
- Feedback jest natychmiastowy
- Nie ma zespołu testerów, jest Zespół SCRUM

### Zespół SCRUM
- W skład Zespołu Scrumowego wchodzą: Właściciel Produktu (ang. Product Owner), Zespół Deweloperski (ang. Development Team) oraz Scrum Master.
- Zespoły są samoorganizujące się i międzyfunkcjonalne.
- Samoorganizujące się zespoły samodzielnie decydują, w jaki sposób najlepiej wykonywać pracę.
- Zespoły międzyfunkcjonalne posiadają wszelkie kompetencje niezbędne do ukończenia pracy.

Generalizując, metodę tę określić można, jako ogromną, uszeregowaną pod względem ważności listę. Tak jak w przypadku Scruma, wymagania w Kanbanie są śledzone poprzez etap, w jakim znajdują się w danym momencie (zadanie [to-do], rozwój [in development], test [in test], wykonane [done]).

Jednak w przeciwieństwie do Scruma, metoda Kanban nie jest osadzona w czasie. Nacisk położony jest tu priorytet. Jeśli programista jest gotowy, by rozpocząć nowe zdanie, pobiera je z listy zadań (to-do), kierując się jego priorytetem. Ponieważ Kanban zakłada mniej spotkań planistycznych, to konieczna jest bardzo bliska współpraca między członkami zespołu. W środowisku tego typu, jeśli programiści pracują o wiele szybciej, niż testerzy, mogą pojawić się problemy z tzw. wąskim gardłem. W takich przypadkach każdy członek zespołu powinien wkroczyć i udzielić pomocy w danym obszarze. Sprostanie takiemu mechanizmowi wymaga od członków grupy dużej elastyczności i zdolności do adaptacji. 
