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
Bazy danych
s  logTMS - backup programisty, 
s - logTMS - informatycy powinni mieć dostęp do admina na linux 
s - logTMS - hosting VPS Hetzner Online
s - optima - MS SQL Server Express: Bezpłatny, ale posiada limity (wykorzystanie do 1.4 GB RAM, baza danych do 10 GB)
s - optima - serwer z linux

Ocena zasobów pod R&D: 
s - brak zasobów dedykowanyhc pod R&D ale możliwe skompletowanie jakiegoś sprzętu polesingowego
s - jest jakieś zasilenie PowerBI z serwera MS SQL Optimy
s - informatycy mają wiedzę na temat przygotowania zasobów po ewentualne nowe rozwiązania i dostęp do sprzętu poleasingowego

Bezpieczeństwo i dostępu zdalnego:
s - open VPN file server i kontrolel domeny i optima
s - community wersje - przydałoby się jakieś paloalto 
s - brak zabezpieczeń vlan (brak dotepu do przełaczników - warto zainwestować)
s - nis2 - do sprawdzenia z prawnikiem czy podlegaja - założenia przychodowe i formy dzialalności

Środowisko Chmurowe: 
s - poczta w azurze / exchange online - office 365 - dużo skrzynek współdzielonych

Backup: Jaka jest polityka i jakie zasoby są backupowane?
s - serwer drugi w głownej serwerowni - (magazyn szafka + mały nas do zrobienia)
s  przepustowość słaba stare przełaczniki (warto rozważyć inwestycje w nowe)
s - na potrzeby poprzedniego wdrożenia TMS była kompletowana maszyna rds(Remote Desktop Services) to technologia firmy Microsoft (część systemu Windows Server), która umożliwia użytkownikom zdalny dostęp do pulpitów lub konkretnych aplikacji zainstalowanych na centralnym serwerze

Narzędzia zewnetrzne
 - wykupiony jest jest chatGPT business

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
- klienci
  s   - nie wierzą w tracking automatyczny, chcą GPS ()
  s   - obecnie brak podpięcia pod p44, shippeo, itp
  s   - klienci obecnie nie oczekują takich danych
s - TMS  ma ograniczone ilości informacji
s - TMS  wysyła zlecenie ze swoimi warunkami do klienta (ważne!!!), maila dostaje osoba kontaktowa
s - CMR jest dodawany do systemu i klientów z FV
s - bardzo mała aplikacji klienckich do wrzucania CMR
s - ważna jest specyfika klienta (niskie ładunki, bez nacisku na pilny termin)

# Planowanie
w - aplikacja typu RAG do wyceny zleceń (policzenie km i podanie relacji + porównanie z ostatnio zrealizowanymi)
s - magazyn pełni funkcję przeładunkową i kompletowania tras, czyli ściagamy kilka zleceń na magazyn a następnie wrzucamy na naczepę 
s - planista planuje zlecenia i przekazuje informacje na magazyn,
s - obecnie słownie przekazywane jest co jest ładowane co ma być załadowane i hostorycznie odtwarzana jest trasa
s - jest moduł pokazujacy zlecenia nieprzypisane do tras
s - ładunki nieprzypisane mogą być na różnych magazynach
s - dzielenie przychodów przy trasach wymaga pobierania i dzielenie 
s - mechanizm dzielenia przychodów na trasę jest dość skomplikowany, ciężko jest na dzić obliczyć ile zarabiliśmy na naczepie, gdyż stawka na km nie ma wielkiego znaczenia tak jak km na pojazd - liczy się głównie stawka na naczepie
s - analizę trzeba podzielić na małe kroki do wdrożenia i duze kroki do wdrożenia
s - obecny system nie wiadomo jak przydzila przychody ze zleceń do tras i nie działo to poprawnie
s - konieczność znalezienia magazynu w różnych krajach który przetrzyma część łądunku na czas rozładowania
s - klienci na rozładunkach często wymagają tylko jednego piętra
s - kluczowy jest tranzyt w weekend, mimo wszystko klienci chcą krókite tranzyty,
s - dystrybucja najlepiej będzie swoimi autami, w iralndii jest jedna solówka, która ma zmienianego kierowcę
s - kierowcy mają metrówki aby infomrować o dostępności ładunku
s- obecnie magzyn jest zajęty jednym klientem więc wdrażanie wms jest mieszane (klient sam tym rozporządza)
s - ściagamy klientów na nasz magazyn w celu cross dockingu głównie z okolic mazowsza
s - kompletowanie ładunku w PL i sprzedawanie spedycji

# dyspozytor
- whatsUP - podstawowe narzędzie komunikacji - wysyłanie infrormacji głównie po polsku ale kierowcy w dużej części obcokrajowcy
- kierowca jest na sałe zalogowany ma link aktywacyjny 
- przydałby się podgląd dyspozytora do aplikacji
- aplikacja jest w języku polskim przydałby się wersje językowe
- powiadomienia z maila o aktywności na aplikacji
- aplikacja do robienia CMR ma ramkę i wysyła zdjęcie
- nazwa pliku jest w cyrylicy
- szkolenie z obsługi gBOX dla koordynatora
- kierowca dostaje plan na kilka dni, ale nie jest on nigdzie zapisywany
- powtarzane trasy nie są szczegółowo podawan kierowcy
- kierowcy mają swoje nawigacje
- bookowanie promów na bezpośrednich platformach
- w formatce celnej w excelu dodać bazę danych, żeby szybciej zaciagać informacje powtarzajace się 
- każdy ma swój folder z odprawami, który mógłby być wspólny
- jest tabelka z kontaktami dla każdego kierowcy
- Piotrek ogarnia awarie, kierowca kontaktuje bezpośrednio z nim, Piotrek informuje o tym, żeby przekazać informaccje dalej na grupie że jest problem spedytor wysłkuje swoje i działa
- na tej samej grupie jest informacja o tym, żę kierowca jest do wyjazdu
- na grupie ładunki iformacja co kwotujemy żęby się nie dublowć
- planowanie włoch manualnie 
- brak zleceń wstępnych w TMS i kiedy ono jest do dyspozycji
- często wysyłane są dostępne auta do klienta i podsyłane do tego zlecenia - do wysłanai capacity
- generowanie maila z datą i miejscem rozłądunku i autem
- trans i timo jako uzupełnienie 
- spedytor odpowiada za ściagnięcie kierowcy, importy do planowane do PL 
- tabela planistyczna skupia sięgłównie na irlandii i gb
- czy można przez API ściągnąć dane z dashboard
- dane w  dashboard można ściągnąć do excel i z pomocą poverQuery zrobić jakiś widok dla planistów w google sheets
- trzeba byłoby dodać kilka informacji w dashbord - czy do planowania do irlandii czy nie 
- część zdjęć od kierowcy puszczane jest przez onlinecamscanner
- instrukcje dla kierowct
- może chat do pytań kierowców? RAG
- przestoje u klienta, przydałoby się jakieś narzędzie do wspomagania śledzenia problemów 0 raczej nie jest to duż skala ale do sprawdzenia
- spóźnienia do wysłania do klientów 
- whatsUP strasznie muli czemu? na telefonie działa...
- na grupach dodawane są co najmniej dwie osoby w przypadku kontaktu z klientem
- na mailach masz przekierowanie
- spedytor informujee klientów i kierowców przy pójściu na urlop
- dashboard z drzewem przedstawiającym strukturę
- rozpatrzeć korzystanie z here maps - gBOX ma wyznaczanie trasy, 
- przy wyznaczaniu trasy podawane są strategiczne punkty
- rejestrowanie kosztów trasy opłaty drogowe - trasy są głównie cykliczne i można byłoby stworzyć najtańsze korytarze i informować o tym kierowców
- kierowcy robią checklistę ale nie ma dużo problemów z imigrantami
- jaki jest współczynnik same day loading
- wtyczka na mailu kategoryzująca maile - rozpoznać wdrożenie tego outlook - copilot
- rozpoznać możliwość liczenia km z wykorzystanie API Here
- pracownik sam rejestruje sobie konto whatrsUP (problem z kierowcami bo nie ma archiwizacji danych i na telefonie jest pełne archiwum)
- kierowcy nie mają służbowych telefonów + mają ekwiwalent za wykorzysstanie internetu
    - przewoźnicy mają nasze naczepy i nasz GPS,\
    - na ciągnikach jest Gbox - eurowag z czasem pracy kierowcy (integracja z TMS?)
    - spotowi nie są w ogóle śledzeni 
- kierowca ma aplikacje webową, gdzie może wrzucić zdjęcie i ma informacje o zleceniu
- kierowcy mają cam scanner robią zdjęcie dodaja do whatsup i spedytor wrzuca do systemu - czy cam scaner ma ramkę
- docinanie zdjęcia w narzędziu microsoft (automat do wycinania)
- najlepiej jakby zweryfikowan cmr wysyłany był do klienta automatycznie, standardowo dyspozytor ma dwa dni na zamknięcie zlecenia
- dla TMS kluczowa jest obsługa części zlecenia 
- spedycja kontraktowa jest obsługiwana jak kierowcy w transporcie
- przewoźnicy kontraktowi najczęściej udtępniają auta i kierowców + sami jeżdżą
- nie ma możliwości odpalenia nocnej zmiany przez brak przekazywania informacji, na whatsUP jest cała komunikacja przez co nie jest to proste w obsłudze może warto rozpatrzeć ZekJu
- przewoźnicy kontraktowi robią to samo co nasza flota, traktowani są jak własna flota (byli kierowcy itp.)
- na spedycji SPOT jesT wszstko co się trafi

# Magazyn-Transport planowanie tras
- obecne WMS wydają siębyć zbyt rozbudowane i wdrożenie zby kosztowne
- magazyn głównie służy do crossdockingu a nie do storage, 
- obecnie mamy moduł w TMS
- mamy kalendarz dostępności magazynierów
- z TMS mam informacje o tym co mam załadować
- czy są jakieś dedykowane narzędzia do crossdocingu (interLNA)
- jest przejści z zgłoszenia na magazyn na trasę
- możliwość generowania CMR i kodu kreskowego
- drukarka do etykiet drukujemy kod kreskowy
- sązupełnie inne zlecenia na usługę magazynową zlecenie magazynowe 
- istotne jest zarządzanie częścią z regałami na długie składowanie i na podłodze na krótkie składowanie
- przy stworzeniu zlecenia na magyznowanie wysyłany jest mail do klienta na magazynowanie
- mamy cennik na przetrzymywanie towaru (może warto zrobić jakiś prosty kalkulator) - palety
- niestandardowe wyceny indywidualnie
- awizacja miejsca na magazynie polega na rezerwacji slotu
- obecnie mamy oznaczone regały, ale nie mamy możliwości oznaczenia ile miejsca jest wykorzystywane
- klientów weryfikuje dział weryfikacji klienta,
- przyjmowanie płatności przez magazynierów
- na zamówieniu klienta jest informacja ile będzie składowane ale bywa różnie i daty się zmieniają
- faktury magazynowe są wystawiane z TMS
- cross doking zrzuca towar i naklejka kod kreskowy, następnie ładuje 
- planiści powinni zarządzać przestrzenią cross dokingu
- główne zadanie polega na zarządzaniu dostępnością magazynierów i tym co mają kiedy ładować
- otwieranie agencji celnej aby oclić ładunki
- dla agencji celnej konieczne jest zarządzanie miejscem w któym będą stały odprawione saomchody
- pytanie czy kupić system rozbudowany i wykorzystywać część, czy obecny rozbudować, czy kupoić coś prostego
- obecnie kluczowym problemem jest terminowość kierowców
- przydałoby się informacja gdzie dany ładunek jest składowany
- na dziś program jest wystarczający
- qr kody na regałach i miejscach magazynowych tak aby można było zarządzać przestrzenią + do sprawdzenia jakie są nejlepsze praktyki zarządzania crossdokingiem bo nie ma sensu oznaczanie każdej palety za 20 np, tylko pierwszą i oznaczyć jako paczka 20
- teoretycznie lepiej byłoby mieć mocniejszy stystem, z możliwością rozbudowy
- konieczne jest zarządzanie rożnymi magazynami i to w innych krajach
- zarządzanie siecia magazynów i przejazdami w przyszłości

# Obsługa Zlecenia (Operacje) - Marcin
- dashboard pojazdy (pokazuje status opercyjny pojazdu) - główne narzędzie do komunikacji między 
- próbowano odwzroować tablicę planistyczną (obiekt zlecenia i obiekt zasobów do polączenia)
- kadry korzystają z tms 
- nie ma miejsca na zarządzanie dostępnością kierowców (jest dashboard pokazujacy teminy itd ale )
- przydałoby się zrobić CMR Matcher
- chcielibyśmy zrobić rozliczenie wydatków w aplikacji dla kierowców
- spedycja spotowa
- giełdy są tylko do sprzedaży
- spedytor ma kilka stałych firmy z którymi działa i pozyskuje zlecenie
- spedytorzy też pozyskują nowych klientów (spedytorzy mają jakieś preferncje na kraje ale nie ma oganiczeń na kraj)
- obecnie jest 11 spedytorów na swoich klientach i dwóch pomocniczych wspierających w obsłudze
- plus jeden spedytor rozwijający pozyskanych klientów przez dział handlowy
- weryfikacja klienta polega na wysłaniu wiadomości do działu weryfikacji klienta, jest na to procedura
- limity na klienta są w tms i są zarządzane przez osoby posiadające dostęp
- atradius i eurdept sprawdzenie - do weryfikacji ile to zajmuje czasu i czy warto proces zoptymalizować, weryfikacja trwa krótko 5min wiec nie wiadomo czy warto optymalizować
- weryfikajca przewoźnika też jest procedura tylko obsługiwana mailem
- w systemie przewoźnik może być aktywowany tylko przez wyznaczone osoby
- przewoźnik wysyła licencje, ocp, i rejestr
- planowanie wdrożenia rekomendacji dla jdg
- raczej system działa poprawnie,
- do rozpatrzenia czy w whataUP można dodać formatkę wprowadzenia informacji w wersji podstawowej
- spedycja dodaje zlecenie przez szybkie dodawanie (działa szybciej niż na transporcie)
- po uzupełnieniu idzie mail do spedytora i przewoźnika
- dla spedytora zlecenie i tras to jest to samo, pod dodaniu CMR jest zamykane zlecenie
- są trzy statusy zleceń otwarte, zamknięte i w trakcie realizacji, 
- automat wystawia FV do klienta z CMR po uzupełnieniu danych na zleceniu
- wystawianie zleceń na giełdy ręcznie
- zlecenia nie są wprowadzane do systemu dopóki nie znajdą przewoźnika na nie
- przez to, że spedytorzy sprzedają zlecenia od swoich klientów to nie było potrzeby dodawania ich do systemu wcześniej
- zlecenia są kopiowane z poprzedniego,
- miesiąc do miesiąca pod kontem klienta liczba zleceń i marża, ewentualnie też przychód
- w fire TMS było łatewiej niż w obecnym
- pracwonik widzi w TMS swój wynik
- sprawdzanie ciągłości łądunków na kliencie pozawala określić czy klient cały czas nam daje zlecenia czy 
- na koniec miesiąca kierownik robi podsumowanie w excelu i to jest miejsce do optymalizacji
- w obecnym PowerBI są prawie gotowe raport
- w TMS nie ma informacji o typie ładunku typu LTL, FTL, itp.
- reklamacje do spedytorów zajmują dużo czasu (zebranie wszystkich informacji - może warto zrobić asystenta AI i szablon)
- rejestr reklamacji wprowadzony ale jeszcze nia działa 
- czy samofkturowanie może przynieść jakieś korzyści, szczególnie biorąc pod uwagę KSEF

# Agencja celna
- odprawy T2
- platforma custran.com miesięczna subsktrypca (ENS, i T2) - CZY MA API
- dane z maila (spedytorzy wysyłają formatkę manifest) - do weryfikacji czy wszystkie informacje są w TMS
- przeprawy są dostępne po realizacji promu
- czy można robić draft przez API i potwierdzać go przez agenta
- RPA może się nie sprawdzić bo raczej zależy nam na autoamtycznym uzupełnianiau
- prowadzony jest rejestr w excel
- agent wysyła komplet dokumentów kierowcy na whatsup
- pytanie czy whatsup masz jakąś opcję pokazywania tylko dokumentów
- problem z whatsup na kompach, gdyż ma zdarza się że sięwywali
- aplikacja desktopowa hussar czy jest płatny (pytanie czy jest moduł w interLAN)
- hussar mniej wiecej to samo tylko custran.com tylko wersja desktopowa
- w aplikacji hussar generuje numer lrn i kierowca odbiera T2 z urzędu i przesyła zdjecie - T2 wpada na oddzielną skrzynkę
- dane z t2 do rejestru excel do którego każdy ma dostęp
- komplet dokumentów jest też na dysku wspólnym
- poza mailem jest jeszcze dodatkowa informacja na whatsUP o konieczności zrobienia odprawy
- odprawy robi się od 8 do 24, 7 dni w tygodniu 
- zmiana nocna kończy się koło 23 ale zdarza si i 1
- po zrobieniu T2 na stronie rządowej customs-roro-control-web do zrobienia pbn 
- po aktualizacji w custom i zmienie statusu na relased - i robimy S&S
- potem na stronie HMRC wrzuca się wszystkie dokumenty (w celu zrobienia dwóch GMR) - do rozpatrzenia czy mozę zrobić spedytor
- wysyłamy kierowcy GMR na whatsUP
- następnie zrobienie ENS na akanea - desktopowa aplikacja
- po zrobieniu ENS w akanea trzeba wrzucic na stronie rządowej douane.gov
- kierowca dostaje ens i po zeskanowaniu T2 sie zamyka
- przy tranzycie z ue inne szablon excel Manifest i wysyłane do innych agencji (tylko w zakresie utworzenia T2 cała reszta podobnie jak powyżej)
- obecnie obsługa celna z irlandii do PL i z PL do Irlandii, pozostałe kierunki ze wsparciem
- eCMR do rozpatrzenia czy jest potencjał namówienia klientów
- sprawdzane jest czy dane na manifest excel i cmr i wygenerowane t2 sie zgadza
- custran ma bazę danych nadawców i odbiorców z wprowadzonych T2, pytanie czy ejst dostęp do tej bazy danych i jak je zmapować z bazą danych w TMS
- jest kontakt do dostawcy custran. - można się z nim skontaktować odnośnie do API
- custran ma opcję eksportu i importu nadawców i odbiorców
- wyszukiwarka kodów hs - isztar, wyszukiwarka kodów - na podstawie nazwy w CMR szukana jest najbliższy towar zazwyczaj uogólniany poprzez wybór opcji pozostałe - jak wyciągnąć numer od klientów
- przydała by się baza kodów do której można pisać w języku naturalnym + lista towarów, które najczęściej jeżdżą
- może warto zrobić notebookLM podpięty pod stronę - z wyszukiwarką kodów + wytyczne wykonania + zapisywanie zapytań i rejestrowanie
- czy można zrobić jakoś tanio RPA do GMR, ewentuaknie do sprawdzenia czy HMRC ma api i obsługa przez n8n
- przydałby się status odprawy celnej w TMS
- jest strona do sprawdzenia czy tranzyt jest zaknięty (można sprawdzić na stronie ec.europa), przyadałobby się narzędzie, które sprawdza zamknięcie tranzytu
- czy armatorzy promowi mają jakieś możliwości do generowanie GMR przy bookingu promu, w calais jest bookowanie na podstawie nr rej, więc totalnie automat
- jak połączyć wykupienie promu z wyrobieniem GMR


# Post-Realizacja & Finans
- osobne osoby do fakakturawania transportu i speedycji
- w TMS ustawiamy filtry - zamknięte zlecenia
- weryfikiacja zlecenia od klienta z dantmi w systemie
- w przypadku błędów zgłoszenie do spedytora
- weryfikacja daty rozładunku
- warunki fakturowania pochodzą ze zlecenia
- na kliencie można dodać informacje o wymaganiach klienta
- jest moduł płatności w TMS w którym oznaczane są FV jako zapłacone
- jak klient płaci za wiele to oznaczane są płatności
- fakturowanie zbiorcze
- nie ma raportów podsumowujacych fakturowanie
- raport zleceń niezamknietych by się przydał
- autofakturowanie - problemem jest jakość danych, ponoć jest w TMS ale przydałoby się dodać
- jakieś walidacje na klientach pod kątem stawki VAT
- księgowanie polega na eksporcie FV z TMS
- optima ma ocr, który ściąga fv 
- czemu dane z OCR a nie API z TMS
- OCR działa słabo dla FV zagarnicznych
- pomysł na to, żeby ściagać FV z KSEF
- jak obsłużyć FV ściągnięte z KSeF
- saldeo aplikacja do ściąganie FV kosztowych (jakie są koszty)
- whatsUP i mail ale papier albo mail
- faktury spedycyjna wpadają na jednego maila
- faktury w papierze
- wykorzystanie n8n do rozesłanie proces fv kosztowych
- proces płatności, terminy płatności 
- połączenie wyciągów bankowych z modyłem płatności (czy w tms jest taka możliwość)
- jak wygląda dostęp do bazy danych optima
- czy optima ma API i czy jest integracji TMS z Optimy
- przydałby się moduł rozliczenia kierowców e-KTR
- raportowanie w powerBI, rachuynek zysków i strat
- brak budżetowania
- optima ma moduł API możliwy do aktywowania
- możliwa integracja z Saldeo w celu obsługi procesu FV (kosztowe Ksef jak i inne) 
- saldeo ma specjalna wtyczkę w Optima przez co integracja nie wymaga dodaktowych kosztów
- saldeo ma API przez co może służyć jako alternatywa do API optima




# Windykacja
- widnykator może wpisać deklarowany temin zapłaty
- ubezpieczenie należności wpływa na zachowanie terminów płatności
- na profilu klienta jest oznaczone jakie dokumenty wymagają klienci (oryginał + kopia)
- 2 osoby w dziale windykacyjno weryfikacyjnym 
- jest automat windykacyjny 3 dni przed terminem i 7 dni po i 14 dni po
- na automaty rzadko ktoś odpowiada
- 7 dni od terminu płątności windykacja ma wiedzieć czemu nie ma płatności
- DSO jest w optima i jest PowerBI w temacie
- maile zazwyczaj są bezpośrednio ze skrzynki immiennej ale mają też dostęp do skrzynki windykacja
- dużo klientów nie płaci w terminie do póki się nie odezwiemy
- brakuje narzędzie do sprawdzania danych w czasie
- brakuje klienta który realizuje dużo niedopłat i ocenia go pod jakimś kątem np. pod katem opóźnioneych płatności i kosztów windykacji
- przydałoby się jakieś narzędzie do analizy danych wewnętrzny chat analizujacy trendy na klientach
- marcin ma fajne pytania ale brakuje narzędzia które szybko na nie odpowie - jakieś narzędzie w stylu BI, które odpowiadałoby na pytania
- przydałoby się stworzenie hurtowni danych






# dział techniczny
- odczyty tacho,
- raportowanie przebiegó i spalania
- w TMS jest wszystko na temat pojazdów, terminy, 
- incpekcje w inspecto
- po zjeździe dorzucamy wszystkie brakujące wyposażenie
- kierowcy raczej nie gubią wyposażenia
- w pliku excel monitorowanie przebiegów -
- dział tech może rezerwować pojazd w dashboard i wpisuje w notace 
- dwa koła zapasowe przy wystrzale opon
- zgłoszenie bezpośrednio od kierowców na whatsUP - w zależnosci od skali problemu zgłoszenie na grupie whatsUP
- w przypadku napraw szkodowych - kierowca kontaktuje się i zbiera dokumentacje - po powrocie na bazie oględziny i zdjęcia 
- w przypadku zagranicznych przez polski oddział
- prowadzony jest rejestr szkód zgłoszonych
- wszystki naprawy assistance są też są rejestrowane w excel i porównywana z fv
- ac do 2tyś nie wkorzystujemy
- jeżlei kierowca ma rażące niedbalstwo to obciążamy
- weekendy awarie 
- pracownicy przeglądają i szykują naczepy i ciągniki
- pracownicy robią inspecto
- wyznaczone są stacje paliwa, które otrzymują kierowcy
- w przypadku braku stacji, wyznaczania stacji dkv na portalu
- spalanie kierowców analizowane codziennie, może warto power BI
- spalanie powyżej 26l na czerowo i analiza - p -xrośba do kierowcy o informacje na temat spalani
- rejestrowane są wszystkie tankowaniaTMS - ustalenia z autorem
- stock technologiczny PHP LARAVEL + MYSQL
- SERVER W HOSTERZE - NIEMCZECH / DEDYK 
- FRONT JS I JQERRY
- BRAK DOKUMENTACJI
- GŁÓWNE PROCESY
- API DO POWER BI - CSV / JEST - WSZYSTKIE REKORDY I FILTR NA DATE / 
- JAK WYGLĄDA STRUKTURA W MYSQL - GŁÓWNA TABLA ZE ZLECENIAMI I TRASAMI
- KOLEGA Z POWER BI MA NOTATKI + ODEZWE
- ZLECENIA MAGAZYNOWE TROCHĘ DOSTOSOWUJĄ DO POTRZEB ROZWIĄZANIE 
- NIEKONWENCOJONALNE UŻYCIE
- KSeF - 40% czasu w systemie to tematy księgowe, fv zrobiona jest pod optima
- KSeF - do ustalenia czy obsługuje kontrahentów zagranicznych
- założenie było, żeby wysyłać z Optimy
- Optima nie ma api i ma duży dług technologiczny
- w tms dodanie korekt
- tms robienie wysyłi do KSEF
- uswanie fv w TMS nie możliwe
- Daniel lista pozycji
- oznaczenie płatności w TMS
- optima księgowa stoi lokalnie na serwerach
- optima kiedy będzie wersja chmurowa
- jest aplikacja ale kierowcy nie chcę instalować
- i jest strona responsywna to jeden projekt, korzysta z tego samego backendu
- serwer wrzucany jest czasem do spamu wszytko idzie przez postMark
- spotkania do przekazywanie informacji
- helpdeskowe projekty rzedzko się zdarzają - przychód źle się liczy przez daty i adrsy
- podpięcie się do lokalizacji gps i dkv
- km są na podstawie google maps - jest integracja pod here maps
- system magazynowy zewnętrzny najlepiej 
- tankowanie kierowca rejestruje na karcie drogowej
- kart drogowe nie zajmuje dużo czasu
- raport spalania wysłana do zarządu - power BI i hurtownia danych




# PowerBI
- dane źródłowe:
    - TMS - API z plikami csv
    - OPTIMA vpn + MA SQL (raporty bezpośrednio z tabel)
    - raporty excel (DKV)
- konto PowerBI - zarzadzane przez informatyków zewnętrznych
- konsultant PowerBI ma doświadczenie w Optima zna układ tabel
- standary raportów zgod nie z standardem kontrolingu - (KSRF) 300
- rachunek zysków i strat oraz bilans przygotowany, ale nie wykorzystywany
- podstawa do tworzenia BDGT
- przychód na trasę nie jest zrozumiały i ciężko - dostać fragment kodu to wyliczający
- tms nie ma instancji testowej 
- ściąganie danych z TMS i np. DKV i inych źródeł (np. KSeF)
- czy dkv ma api do ściągania raportów





# Przemyślenia końcowe
- jak odchudzić bieżący TMS i skupić się na kluczowej kwesti a w pozostałych wykorzystywać zewnętrzny TMS
- może wziąć z InterLAN albo z innego TMS moduł bazowy (zlecenia, kierowcy, fv, itp.) a w LogTMS zostawić łączenie zleceń w trasy i obsługę cross dokingu
- przydałby się jakiś manual do log TMS
- nie ma narzędzie dla dyspozytora, do obserwowania swoich aut w trasie - do sprawdzenia Zekju, Slickshift (mail od Daniela) i inni dostawcy