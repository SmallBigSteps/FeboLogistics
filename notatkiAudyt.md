# Cele długoterminowe
s - zwiększamy flote o 30 aut w tym roku
s - chcemy kupić magazyn w Iralndii 
s - dalszy rozwój transportu, spedycji, usług celnych i magazynu
s - obecnie mamy dużo pracy do oznaczenia wszystkiego na magazynie
s - docelowo do kupienia mala firma transportowa w Iralndii za kilka lat
s - spedycja nie robi takeigo modelu jak transport relizujace grupówke
s - celem jest powiekszenie magazynu
s - magazyn zwiększony w stojadąłach zwiększenie cross docking
s - magazyn dla kientów - na razie nie zakładamy kompletowania i usług dla dostawców
s - zwiększenie liuczzby pojazdów do 200 (sky is the limit)
s - rozwój spedycji - zarówno konraktowa jak i spot
s - branże elektronika, hiogh value, cel TAPA, opakownia, oświetlenie, spożywka, cześci, farmaceutyka jakie certyfikaty tego wymagają
s - dostawy just in time - dedykowane 
s - możliwość rozdzielenia produktów high value na boxach i pozostałe gdzie indziej
s - towary minimalnie paleta
s - dystrybucja do poziomu plety wchodzi w grę
s - plan na ponadnormatywne łądunki w przyszłości

# TMS - ustalenia z autorem
s - stock technologiczny PHP LARAVEL + MYSQL
s - SERVER W HOSTERZE - NIEMCZECH / DEDYK 
s - FRONT JS I JQERRY
s - BRAK DOKUMENTACJI
s - GŁÓWNE PROCESY
s - API DO POWER BI - CSV / JEST - WSZYSTKIE REKORDY I FILTR NA DATE / 
s - JAK WYGLĄDA STRUKTURA W MYSQL - GŁÓWNA TABLA ZE ZLECENIAMI I TRASAMI
s - KOLEGA Z POWER BI MA NOTATKI + ODEZWE
s - ZLECENIA MAGAZYNOWE TROCHĘ DOSTOSOWUJĄ DO POTRZEB ROZWIĄZANIE 
s - NIEKONWENCOJONALNE UŻYCIE
s - KSeF - 40% czasu w systemie to tematy księgowe, fv zrobiona jest pod optima
s - założenie było, żeby wysyłać z Optimy
s - Optima nie ma api i ma duży dług technologiczny
s - w tms dodanie korekt
s - tms robienie wysyłi do KSEF
s - uswanie fv w TMS nie możliwe
s - Daniel lista pozycji
s - oznaczenie płatności w TMS
s - optima księgowa stoi lokalnie na serwerach
s - optima kiedy będzie wersja chmurowa
s - jest aplikacja ale kierowcy nie chcę instalować
s - i jest strona responsywna to jeden projekt, korzysta z tego samego backendu
s - helpdeskowe projekty rzedzko się zdarzają - przychód źle się liczy przez daty i adrsy
s - podpięcie się do lokalizacji gps i dkv
s - km są na podstawie google maps - jest integracja pod here maps

# IT
s - logTMS - backup programisty, 
s - logTMS - informatycy powinni mieć dostęp do admina na linux 
s - logTMS - hosting VPS Hetzner Online
s - optima - MS SQL Server Express: Bezpłatny, ale posiada limity (wykorzystanie do 1.4 GB RAM, baza danych do 10 GB)
s - optima - serwer z linux
s - brak zasobów dedykowanyhc pod R&D ale możliwe skompletowanie jakiegoś sprzętu polesingowego
s - jest jakieś zasilenie PowerBI z serwera MS SQL Optimy
s - informatycy mają wiedzę na temat przygotowania zasobów po ewentualne nowe rozwiązania i dostęp do sprzętu poleasingowego
s - open VPN file server i kontrolel domeny i optima
s - community wersje - przydałoby się jakieś paloalto 
s - brak zabezpieczeń vlan (brak dotepu do przełaczników - warto zainwestować)
s - nis2 - do sprawdzenia z prawnikiem czy podlegaja - założenia przychodowe i formy dzialalności
s - poczta w azurze / exchange online - office 365 - dużo skrzynek współdzielonych
s - serwer drugi w głownej serwerowni - (magazyn szafka + mały nas do zrobienia)
s  przepustowość słaba stare przełaczniki (warto rozważyć inwestycje w nowe)
s - na potrzeby poprzedniego wdrożenia TMS była kompletowana maszyna rds(Remote Desktop Services) to technologia firmy Microsoft (część systemu Windows Server), która umożliwia użytkownikom zdalny dostęp do pulpitów lub konkretnych aplikacji zainstalowanych na centralnym serwerze

# Pozyskiwanie Klienta i Rozszerzenie Współpracy notatki: Krystian
s - skupiamy się na średnich klientach
s - dział hanfdlowy 3 handlowców + spedytorzy handlowi (dbają również o kientów)
s - stramy się klientów spedycyjnych obsługiwać dwutorowo przez handlowców
s - cel: 
    - pielegnacja relacji 
    - rozszrzenie współpracy (zarówno zwiększamy volumeny i cross selling)
    - stawiamy na spotkania
    - TMS ma moduł CRM (nie spełnia do końca oczekiwań)
        - jest Kanban i poziomy klientów
        - programista nie chcce zwiększyć zepołu
s - potencjalnie dodawanie klientów 
s - handlowiec zapomniał, że był już u klienta jak temu zapobiegać
s - konieczne zaciągnięcie klientów z bieżącego systemu
s - w CRM nie ma kalendarza spotkań widoczny dla innych użytkowników
s - outlook jako poczta (integracja z kalendarzem w poczcie)
s - udostępnianie kalendarzy dla innych
s - do komunikacji wykorzystywany jest whatsup ale nie konto prywatne
s - skupiamy się na jakości a nie na cold mailingu i cold callu
s - budowanie relacji z klientem (co lubi, czego nie lubi)
s - fire TMS kiedyś był w systemie, w firmie był winsped (nieprzystosowny do polskiego rynku)
s - w irlandii wszyscy korzystają z azyra - integracja z InterLAN?
s - handlowiec pozyskuje zlecenia i wprowadza do systemu
s - wprowadzanie zleceń do systemu ręcznie bez AI (czy MTS ma API??), jest możliwość kopiowania zleceń
s - klienci
  s   - nie wierzą w tracking automatyczny, chcą GPS ()
  s   - obecnie brak podpięcia pod p44, shippeo, itp
  s   - klienci obecnie nie oczekują takich danych
s - TMS  ma ograniczone ilości informacji
s - TMS  wysyła zlecenie ze swoimi warunkami do klienta (ważne!!!), maila dostaje osoba kontaktowa
s - CMR jest dodawany do systemu i klientów z FV
s - bardzo mała aplikacji klienckich do wrzucania CMR
s - ważna jest specyfika klienta (niskie ładunki, bez nacisku na pilny termin)

# Planowanie
s - magazyn pełni funkcję przeładunkową i kompletowania tras, czyli ściagamy kilka zleceń na magazyn a następnie wrzucamy na naczepę 
s - planista planuje zlecenia i przekazuje informacje na magazyn,
s - obecnie słownie przekazywane jest co jest ładowane co ma być załadowane i hostorycznie odtwarzana jest trasa
s - jest moduł pokazujacy zlecenia nieprzypisane do tras
s - ładunki nieprzypisane mogą być na różnych magazynach
s - dzielenie przychodów przy trasach wymaga pobierania i dzielenie 
s - mechanizm dzielenia przychodów na trasę jest dość skomplikowany, ciężko jest na dziś obliczyć ile zarabiliśmy na naczepie, gdyż stawka na km nie ma wielkiego znaczenia tak jak km na pojazd - liczy się głównie stawka na naczepie
s - analizę trzeba podzielić na małe kroki do wdrożenia i duze kroki do wdrożenia
s - obecny system nie wiadomo jak przydzila przychody ze zleceń do tras i nie działo to poprawnie
s - konieczność znalezienia magazynu w różnych krajach który przetrzyma część łądunku na czas rozładowania
s - klienci na rozładunkach często wymagają tylko jednego piętra
s - kluczowy jest tranzyt w weekend, mimo wszystko klienci chcą krókite tranzyty,
s - dystrybucja najlepiej będzie swoimi autami, w iralndii jest jedna solówka, która ma zmienianego kierowcę
s - kierowcy mają metrówki aby infomrować o dostępności ładunku
s - obecnie magzyn jest zajęty jednym klientem więc wdrażanie wms jest mieszane (klient sam tym rozporządza)
s - ściagamy klientów na nasz magazyn w celu cross dockingu głównie z okolic mazowsza
s - kompletowanie ładunku w PL i sprzedawanie spedycji

# Spedytor
s - whatsUP - podstawowe narzędzie komunikacji - wysyłanie infrormacji głównie po polsku ale kierowcy w dużej części obcokrajowcy
s - kierowca jest na sałe zalogowany ma link aktywacyjny 
s - aplikacja jest w języku polskim przydałby się wersje językowe
s - powiadomienia z maila o aktywności na aplikacji
s - aplikacja do robienia CMR ma ramkę i wysyła zdjęcie
s - nazwa pliku jest w cyrylicy
s - kierowca dostaje plan na kilka dni, ale nie jest on nigdzie zapisywany
s - powtarzane trasy nie są szczegółowo podawan kierowcy
s - kierowcy mają swoje nawigacje
s - bookowanie promów na bezpośrednich platformach
s - jest tabelka z kontaktami dla każdego kierowcy
s - Piotrek ogarnia awarie, kierowca kontaktuje bezpośrednio z nim, Piotrek informuje o tym, żeby przekazać informaccje dalej na grupie że jest problem spedytor wysłkuje swoje i działa
s - na tej samej grupie jest informacja o tym, żę kierowca jest do wyjazdu
s - na grupie ładunki iformacja co kwotujemy żęby się nie dublowć
s - planowanie włoch manualnie 
s - brak zleceń wstępnych w TMS i kiedy ono jest do dyspozycji
s - często wysyłane są dostępne auta do klienta i podsyłane do tego zlecenia - do wysłanai capacity
s - generowanie maila z datą i miejscem rozłądunku i autem
s - trans i timo jako uzupełnienie 
s - spedytor odpowiada za ściagnięcie kierowcy, importy do planowane do PL 
s - tabela planistyczna skupia sięgłównie na irlandii i gb
s - część zdjęć od kierowcy puszczane jest przez onlinecamscanner
s - instrukcje dla kierowct
s - przestoje u klienta, przydałoby się jakieś narzędzie do wspomagania śledzenia problemów 0 raczej nie jest to duż skala ale do sprawdzenia
s - spóźnienia do wysłania do klientów 
s - whatsUP strasznie muli czemu? na telefonie działa...
s - na grupach dodawane są co najmniej dwie osoby w przypadku kontaktu z klientem
s - na mailach masz przekierowanie
s - spedytor informujee klientów i kierowców przy pójściu na urlop
s - przy wyznaczaniu trasy podawane są strategiczne punkty
s - kierowcy robią checklistę ale nie ma dużo problemów z imigrantami
s - jaki jest współczynnik same day loading (przy tym modelu biznesowym nie jst to kluczowe)
s - pracownik sam rejestruje sobie konto whatrsUP (problem z kierowcami bo nie ma archiwizacji danych i na telefonie jest pełne archiwum)
s - kierowcy nie mają służbowych telefonów + mają ekwiwalent za wykorzysstanie internetu
    s - przewoźnicy mają nasze naczepy i nasz GPS,\
    s - na ciągnikach jest Gbox - eurowag z czasem pracy kierowcy (integracja z TMS?)
    s - spotowi nie są w ogóle śledzeni 
s - kierowca ma aplikacje webową, gdzie może wrzucić zdjęcie i ma informacje o zleceniu
s - kierowcy mają cam scanner robią zdjęcie dodaja do whatsup i spedytor wrzuca do systemu - czy cam scaner ma ramkę
s - docinanie zdjęcia w narzędziu microsoft (automat do wycinania)
s - standardowo dyspozytor ma dwa dni na zamknięcie zlecenia
s - dla TMS kluczowa jest obsługa części zlecenia 
s - spedycja kontraktowa jest obsługiwana jak kierowcy w transporcie
s - przewoźnicy kontraktowi najczęściej udtępniają auta i kierowców + sami jeżdżą
s - nie ma możliwości odpalenia nocnej zmiany przez brak przekazywania informacji, na whatsUP jest cała komunikacja przez co nie jest to proste w obsłudze może warto rozpatrzeć ZekJu
s - przewoźnicy kontraktowi robią to samo co nasza flota, traktowani są jak własna flota (byli kierowcy itp.)
s - na spedycji SPOT jesT wszstko co się trafi

# Magazyn-Transport planowanie tras
s - obecne WMS wydają siębyć zbyt rozbudowane i wdrożenie zby kosztowne
s - magazyn głównie służy do crossdockingu a nie do storage, 
s - obecnie mamy moduł w TMS
s - mamy kalendarz dostępności magazynierów
s - z TMS mam informacje o tym co mam załadować
s - jest przejści z zgłoszenia na magazyn na trasę
s - możliwość generowania CMR i kodu kreskowego
s - drukarka do etykiet drukujemy kod kreskowy
s - są zupełnie inne zlecenia na usługę magazynową zlecenie magazynowe 
s - istotne jest zarządzanie częścią z regałami na długie składowanie i na podłodze na krótkie składowanie
s - przy stworzeniu zlecenia na magyznowanie wysyłany jest mail do klienta na magazynowanie
s - mamy cennik na przetrzymywanie towaru (może warto zrobić jakiś prosty kalkulator) - palety
s - niestandardowe wyceny indywidualnie
s - awizacja miejsca na magazynie polega na rezerwacji slotu
s - obecnie mamy oznaczone regały, ale nie mamy możliwości oznaczenia ile miejsca jest wykorzystywane
s - klientów weryfikuje dział weryfikacji klienta,
s - przyjmowanie płatności przez magazynierów
s - na zamówieniu klienta jest informacja ile będzie składowane ale bywa różnie i daty się zmieniają
s - faktury magazynowe są wystawiane z TMS
s - cross doking zrzuca towar i naklejka kod kreskowy, następnie ładuje 
s - główne zadanie polega na zarządzaniu dostępnością magazynierów i tym co mają kiedy ładować
s - otwieranie agencji celnej aby oclić ładunki
s - dla agencji celnej konieczne jest zarządzanie miejscem w któym będą stały odprawione saomchody
s - pytanie czy kupić system rozbudowany i wykorzystywać część, czy obecny rozbudować, czy kupoić coś prostego
s - obecnie kluczowym problemem jest terminowość kierowców
s - przydałoby się informacja gdzie dany ładunek jest składowany
s - na dziś program jest wystarczający

# Obsługa Zlecenia (Operacje) - Marcin
s - dashboard pojazdy (pokazuje status opercyjny pojazdu) - główne narzędzie do komunikacji między 
s - próbowano odwzroować tablicę planistyczną (obiekt zlecenia i obiekt zasobów do polączenia)
s - kadry korzystają z tms 
s - nie ma miejsca na zarządzanie dostępnością kierowców (jest dashboard pokazujacy teminy itd ale )
s - spedycja spotowa
s - giełdy są tylko do sprzedaży
s - spedytor ma kilka stałych firmy z którymi działa i pozyskuje zlecenie
s - spedytorzy też pozyskują nowych klientów (spedytorzy mają jakieś preferncje na kraje ale nie ma oganiczeń na kraj)
s - obecnie jest 11 spedytorów na swoich klientach i dwóch pomocniczych wspierających w obsłudze
s - plus jeden spedytor rozwijający pozyskanych klientów przez dział handlowy
s - weryfikacja klienta polega na wysłaniu wiadomości do działu weryfikacji klienta, jest na to procedura
s - limity na klienta są w tms i są zarządzane przez osoby posiadające dostęp
s - atradius i eurdept sprawdzenie - do weryfikacji ile to zajmuje czasu i czy warto proces zoptymalizować, weryfikacja trwa krótko 5min wiec nie wiadomo czy warto optymalizować
s - weryfikajca przewoźnika też jest procedura tylko obsługiwana mailem
s - w systemie przewoźnik może być aktywowany tylko przez wyznaczone osoby
s - przewoźnik wysyła licencje, ocp, i rejestr
s - planowanie wdrożenia rekomendacji dla jdg
s - raczej system działa poprawnie,
s - do rozpatrzenia czy w whataUP można dodać formatkę wprowadzenia informacji w wersji podstawowej
s - spedycja dodaje zlecenie przez szybkie dodawanie (działa szybciej niż na transporcie)
s - po uzupełnieniu idzie mail do spedytora i przewoźnika
s - dla spedytora zlecenie i tras to jest to samo, pod dodaniu CMR jest zamykane zlecenie
s - są trzy statusy zleceń otwarte, zamknięte i w trakcie realizacji, 
s - automat wystawia FV do klienta z CMR po uzupełnieniu danych na zleceniu
s - wystawianie zleceń na giełdy ręcznie
s - zlecenia nie są wprowadzane do systemu dopóki nie znajdą przewoźnika na nie
s - przez to, że spedytorzy sprzedają zlecenia od swoich klientów to nie było potrzeby dodawania ich do systemu wcześniej
s - zlecenia są kopiowane z poprzedniego,
s - miesiąc do miesiąca pod kontem klienta liczba zleceń i marża, ewentualnie też przychód
s - w fire TMS było łatewiej niż w obecnym
s - pracwonik widzi w TMS swój wynik
s - sprawdzanie ciągłości łądunków na kliencie pozawala określić czy klient cały czas nam daje zlecenia czy 
s - na koniec miesiąca kierownik robi podsumowanie w excelu i to jest miejsce do optymalizacji
s - w obecnym PowerBI są prawie gotowe raport
s - w TMS nie ma informacji o typie ładunku typu LTL, FTL, itp.
s - reklamacje do spedytorów zajmują dużo czasu (zebranie wszystkich informacji - może warto zrobić asystenta AI i szablon)
s - rejestr reklamacji wprowadzony ale jeszcze nia działa 

# Agencja celna
s - odprawy T2
s - platforma custran.com miesięczna subsktrypca (ENS, i T2) - CZY MA API
s - dane z maila (spedytorzy wysyłają formatkę manifest) - do weryfikacji czy wszystkie informacje są w TMS nie
s - przeprawy są dostępne po realizacji promu
s - RPA może się nie sprawdzić bo raczej zależy nam na autoamtycznym uzupełnianiau
s - prowadzony jest rejestr w excel
s - agent wysyła komplet dokumentów kierowcy na whatsup
s - problem z whatsup na kompach, gdyż ma zdarza się że sięwywali
s - aplikacja desktopowa hussar czy jest płatny (pytanie czy jest moduł w interLAN)
s - hussar mniej wiecej to samo tylko custran.com tylko wersja desktopowa
s - w aplikacji hussar generuje numer lrn i kierowca odbiera T2 z urzędu i przesyła zdjecie - T2 wpada na oddzielną skrzynkę
s - dane z t2 do rejestru excel do którego każdy ma dostęp
s - komplet dokumentów jest też na dysku wspólnym
s - poza mailem jest jeszcze dodatkowa informacja na whatsUP o konieczności zrobienia odprawy
s - odprawy robi się od 8 do 24, 7 dni w tygodniu 
s - zmiana nocna kończy się koło 23 ale zdarza si i 1
s - po zrobieniu T2 na stronie rządowej customs-roro-control-web do zrobienia pbn 
s - po aktualizacji w custom i zmienie statusu na relased - i robimy S&S
s - potem na stronie HMRC wrzuca się wszystkie dokumenty (w celu zrobienia dwóch GMR) - do rozpatrzenia czy mozę zrobić spedytor
s - wysyłamy kierowcy GMR na whatsUP
s - następnie zrobienie ENS na akanea - desktopowa aplikacja
s - po zrobieniu ENS w akanea trzeba wrzucic na stronie rządowej douane.gov
s - kierowca dostaje ens i po zeskanowaniu T2 sie zamyka
s - przy tranzycie z ue inne szablon excel Manifest i wysyłane do innych agencji (tylko w zakresie utworzenia T2 cała reszta podobnie jak powyżej)
s - obecnie obsługa celna z irlandii do PL i z PL do Irlandii, pozostałe kierunki ze wsparciem
s - sprawdzane jest czy dane na manifest excel i cmr i wygenerowane t2 sie zgadza
s - custran ma bazę danych nadawców i odbiorców z wprowadzonych T2, pytanie czy ejst dostęp do tej bazy danych i jak je zmapować z bazą danych w TMS
s - jest kontakt do dostawcy custran. - można się z nim skontaktować odnośnie do API
s - custran ma opcję eksportu i importu nadawców i odbiorców
s - wyszukiwarka kodów hs - isztar, wyszukiwarka kodów - na podstawie nazwy w CMR szukana jest najbliższy towar zazwyczaj uogólniany poprzez wybór opcji pozostałe - jak wyciągnąć numer od klientów

# Post-Realizacja & Finans
s - osobne osoby do fakakturawania transportu i speedycji
s - w TMS ustawiamy filtry - zamknięte zlecenia
s - weryfikiacja zlecenia od klienta z dantmi w systemie
s - w przypadku błędów zgłoszenie do spedytora
s - weryfikacja daty rozładunku
s - warunki fakturowania pochodzą ze zlecenia
s - na kliencie można dodać informacje o wymaganiach klienta
s - jest moduł płatności w TMS w którym oznaczane są FV jako zapłacone
s - jak klient płaci za wiele to oznaczane są płatności
s - fakturowanie zbiorcze
s - nie ma raportów podsumowujacych fakturowanie
s - autofakturowanie - problemem jest jakość danych, ponoć jest w TMS ale przydałoby się dodać
s - jakieś walidacje na klientach pod kątem stawki VAT
s - księgowanie polega na eksporcie FV z TMS
s - optima ma ocr, który ściąga fv 
s - czemu dane z OCR a nie API z TMS
s - OCR działa słabo dla FV zagarnicznych
s - whatsUP i mail ale papier albo mail
s - faktury spedycyjna wpadają na jednego maila
s - faktury w papierze
s - proces płatności, terminy płatności 
s - jak wygląda dostęp do bazy danych optima
s - czy optima ma API i czy jest integracji TMS z Optimy
s - brak budżetowania
s - optima ma moduł API możliwy do aktywowania

# Windykacja
s - widnykator może wpisać deklarowany temin zapłaty
s - ubezpieczenie należności wpływa na zachowanie terminów płatności
s - na profilu klienta jest oznaczone jakie dokumenty wymagają klienci (oryginał + kopia)
s - 2 osoby w dziale windykacyjno weryfikacyjnym 
s - jest automat windykacyjny 3 dni przed terminem i 7 dni po i 14 dni po
s - na automaty rzadko ktoś odpowiada
s - 7 dni od terminu płątności windykacja ma wiedzieć czemu nie ma płatności
s - DSO jest w optima i jest PowerBI w temacie
s - maile zazwyczaj są bezpośrednio ze skrzynki immiennej ale mają też dostęp do skrzynki windykacja
s - dużo klientów nie płaci w terminie do póki się nie odezwiemy
s - brakuje narzędzie do sprawdzania danych w czasie
s - brakuje klienta który realizuje dużo niedopłat i ocenia go pod jakimś kątem np. pod katem opóźnioneych płatności i kosztów windykacji

# Dział techniczny
s - odczyty tacho,
s - raportowanie przebiegów i spalania
s - w TMS jest wszystko na temat pojazdów, terminy, 
s - incpekcje w inspecto
s - po zjeździe dorzucamy wszystkie brakujące wyposażenie
s - kierowcy raczej nie gubią wyposażenia
s - w pliku excel monitorowanie przebiegów
s - dział tech może rezerwować pojazd w dashboard i wpisuje w notace 
s - dwa koła zapasowe przy wystrzale opon
s - zgłoszenie bezpośrednio od kierowców na whatsUP - w zależnosci od skali problemu zgłoszenie na grupie whatsUP
s - w przypadku napraw szkodowych - kierowca kontaktuje się i zbiera dokumentacje - po powrocie na bazie oględziny i zdjęcia 
s - w przypadku zagranicznych przez polski oddział
s - prowadzony jest rejestr szkód zgłoszonych
s - wszystki naprawy assistance są też są rejestrowane w excel i porównywana z fv
s - ac do 2tyś nie wkorzystujemy
s - jeżlei kierowca ma rażące niedbalstwo to obciążamy
s - weekendy awarie 
s - pracownicy przeglądają i szykują naczepy i ciągniki
s - pracownicy robią inspecto
s - wyznaczone są stacje paliwa, które otrzymują kierowcy
s - w przypadku braku stacji, wyznaczania stacji dkv na portalu
s - spalanie kierowców analizowane codziennie, może warto power BI
s - spalanie powyżej 26l na czerowo i analiza - p -xrośba do kierowcy o informacje na temat spalani
s - rejestrowane są wszystkie tankowaniaTMS - ustalenia z autorem
s - tankowanie kierowca rejestruje na karcie drogowej
s - kart drogowe nie zajmuje dużo czasu
s - raport spalania wysłana do zarządu - power BI i hurtownia danych

# Analityka
s - obecnie głównie PowerBI przygotowywany przez zewnętrznego analityka + raporty do ściągnięcia z TMS i innych narzędzi do obsługi w excel
s - dane źródłowe:
  s  - TMS - API z plikami csv, importy do pliku excel
  s  - OPTIMA vpn + MA SQL (raporty bezpośrednio z tabel)
   s - inne: raporty excel do ściągnięcia w narzędziu (np. DKV) 
s - konto PowerBI - zarzadzane przez informatyków zewnętrznych
s - konsultant PowerBI ma doświadczenie w Optima zna układ tabel
s - standary raportów zgodnie z standardem kontrolingu - (KSRF) 300
s - rachunek zysków i strat oraz bilans przygotowany, ale nie wykorzystywany
s - podstawa do tworzenia BDGT
s - przychód na trasę nie jest zrozumiały i ciężko - dostać fragment kodu to wyliczający