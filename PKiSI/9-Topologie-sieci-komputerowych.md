# Topologie sieci komputerowych.

Topologia magistrali charakteryzuje się tym, że wszystkie urządzenia podłącza się do wspólnego medium transmisyjnego. Powszechnie stosowanym w tej topologii medium transmisyjnym był kabel koncentryczny. Jedną z wad tej topologii, była niewielką przepustowość (maksymalnie do 10 Mb/s). Poza niską przepustowością, charakteryzowała ją również duża podatność na awarię sieci. W momencie przerwania kabla koncentrycznego cała sieć przestawała działać.

W topologii pierścienia każde urządzenie podłączone jest z dwoma sąsiadami, tworząc zamknięty krąg. Podobnie jak w przypadku topologii magistrali, przy budowie nie stosuję się dużej ilości okablowania oraz dodatkowych urządzeń. Ponadto można wykorzystać różne media transmisyjne, począwszy od kabla koncentrycznego, po skrętkę miedzianą, aż do kabli światłowodowych. Wadą tego rodzaju topologii jest fakt, iż przerwanie medium lub awaria jednego z komputerów powoduje przerwę w działaniu całej sieci. Aby temu zapobiec stosuje się tzw. podwójny pierścień, czyli podwaja się liczę połączeń pomiędzy urządzeniami. Wówczas taką topologię nazywa się topologią podwójnego pierścienia.

W topologii gwiazdy urządzenia podłączone są do centralnego punktu, stanowiącego punkt dostępu do sieci. Dawniej punkt ten stanowiły koncentratory (ang. hub), obecnie natomiast stosuje się przełączniki (ang. switch). W lokalnych sieciach jest to najczęściej spotykana topologia, ponieważ jest prosta w zaprojektowaniu, budowie oraz rozbudowie, odporna na awarie i łatwo zarządzalna. Dodatkowym plusem jest fakt, iż można przy jej budowie wykorzystać różne media transmisyjne, takie jak miedziana skrętka, kabel światłowodowy czy fale radiowe (WLAN). Istotną wadę stanowić może natomiast koszt budowy, ponieważ wymagane jest zastosowanie dodatkowych urządzeń (switchy) oraz wiele metrów okablowania.

### Topologie logiczne określają sposób przepływu danych w sieci:

Topologia punkt-punkt – w tej topologii przesył danych odbywa się tylko pomiędzy dwoma urządzeniami w sieci, które mogą być do siebie podłączone bezpośrednio, jak również z wykorzystaniem urządzeń pośredniczących (np. switch’y).

Topologia wielodostępowa – w tej topologii przesył danych odbywa się poprzez jedno medium transmisyjne (np. kabel koncentryczny), które współdzielone jest przez wiele urządzeń. Urządzenie transmitujące dane wysyła je do wszystkich (ang. broadcasting), ale tylko urządzenie, do którego dane były adresowane odczytuje je, pozostałe urządzenia je ignorują.
