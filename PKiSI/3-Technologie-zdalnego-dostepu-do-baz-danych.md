# Technologie zdalnego dostępu do baz danych 
Dzięki technologiom zdalnego dostępu do bazy danych realizowany jest dostęp aplikacji do danych przechowywanych i zarządzanych przez różne serwery SQL.

- ODBC, 
- OLE DB, 
- DAO,
- ADO,
- ADO.NET,
- JDBC,
- JDO

### ODBC
Składa się na niego zbiór funkcji API, dzięki którym możliwy stał się dostęp do relacyjnych baz danych. Dzięki niemu tworzone aplikacje 
mogły uzyskać dostęp do danych składowanych w plikach jak również w serwerach SQL

### OLE DB
Interfejs ten stanowi rozwinięcie opracowane przez firmę Microsoft standardu ODBC. Głównym założeniem OLE DB jest uogólnienie modelu 
klient-serwer ODBC do modelu konsument danych - dostawca danych. 

### DAO
Model DAO ma strukturę hierarchiczną. Podstawę hierarchii modelu danych stanowi silnik bazy danych. Przestrzenie robocze stanowią otoczenie 
dla otwieranych baz danych w ich obrębie (każda sesja reprezentowana jest przez jeden obiekt). Pierwsza technologia która posłużyła się 
obiektami dostępu do danych

### ADO
Wykorzystuje OLE.DB do łączenia się z bazami danych, ale implementacja jest zdecydowanie uproszczona. Jest warstwą odnoszącą się do interfejsu 
na poziomie aplikacji, a nie systemu operacyjnego.

### ADO.NET
Firma Microsoft wprowadziła obsługę XML-a. Dzięki temu w założeniach ADO.NET miało działać w zasadzie na każdej platformie, która obsługuje 
standard XML. Jest to technologia ukierunkowana głównie na tworzenie aplikacji wielowarstwowych, rozproszonych na kilku serwerach. 
W odniesieniu do klasycznego ADO ADO.NET korzysta z dwóch warstw: połączeniowej i bezpołączeniowej. Warstwa połączeniowa jest mocno powiązana 
z używanym dostawcą danych, najczęściej z konkretnym SZBD. Warstwa bezpołączeniowa jest niezależna od dostawców danych. Wykorzystywana jest, 
gdy nie jest wymagany ciągły dostęp do źródła danych. Oferuje możliwość pracy na danych tymczasowych, które mogą być odczytywane i pobierane 
w strumieniach xml, jak i plikach. Dane pobrane ze źródła danych przechowywane i przetwarzane są na lokalnym komputerze użytkownika, zazwyczaj 
w postaci lokalnej bazy danych.

### JDBC
Standard JDBC pozwala tworzyć interfejsy programowe API (Application Programming Interface) wyższego poziomu: 
SQLJ − osadzony SQL dla Javy, oraz JavaBlend − bezpośrednie odwzorowanie tabel relacyjnej bazy danych na klasy Javy. Sama aplikacja dostęp 
do danych uzyskać może na kilka sposobów; są one następujące: moduł JDBC z bezpośrednim połączeniem z bazą danych, moduł sterujący JDBC dla 
oprogramowania pośredniczącego bazy danych, częściowy moduł sterujący JDBC, połączenie JDBC-ODBC

### JDO
JDO stanowi alternatywę dla JDBC. Udostępnia obiektowy mechanizm trwałości i standardowe interfejsy umożliwiające korzystanie z baz danych. 
Rekordy z relacyjnej bazy danych traktowane są jako obiekty. Współpracuje z relacyjnymi i obiektowymi bazami danych, jak również innymi 
rodzajami systemów. Na obiektowy model JDO składa się zestaw klas Javy i plik metadanych XML (zawierający wytyczne modelowania)


## II wersja 

ADO.NET można podzielić na: mechanizm dostępu do danych oraz system przechowywania danych. Uproszoną architekturę ADO.NET, której głównymi 
komponentami są: zbiór danych (DataSet) oraz dostarczyciel danych (Data Provider). Źródło danych może znajdować się w fizycznej bazie danych 
lub pliku XML. Data Provider wykonuje połączenia i wysyła polecenia, a DataSet reprezentuje dane w pamięci. Dostarczyciel danych 
(Data Provider) jest odpowiednikiem sterownika, którego zadaniem jest połączenie się z bazą danych lub odczytanie odpowiedniego pliku, 
ukrywając przy tym szczegóły implementacyjne. ADO.NET zapewnia obsługę baz danych MS SQL Server, Oracle oraz technologii OLE.DB. W ADO dane 
pomiędzy źródłem danych i aplikacją transportowane były w formie zbioru rekordów (RecordSet) bez względu na to, czy pochodziły z jednej, 
czy z wielu tabel. W ADO.NET zbiór rekordów został zastąpiony przez zbiór danych. Dane znajdujące się w zbiorze danych zawarte są w tabelach 
(DataTable). Jeśli aplikacja żąda od ADO.NET zwrócenia danych z dwóch tabel, to dane zwracane są w formie dwóch tabel, które znajdują się 
w zbiorze danych. Relacje pomiędzy ta-belami znajdującymi się w zbiorze danych reprezentowane są przez instancję klasy DataRelation.

Aktualnie najczęściej używaną i zarazem wiodącą technologią Microsoft jest ADO.NET. Interfejsy ODBC i OLE DB nie są już tak popularne jak kiedyś (m.in. ze względu na efektywność dostępu czy też brak dostępu do specjalizowanych funkcji najnowszych wersji SQL Servera) ale nadal znajdują swoje zastosowanie, choć w znacznie mniejszym stopniu niż przed laty.
