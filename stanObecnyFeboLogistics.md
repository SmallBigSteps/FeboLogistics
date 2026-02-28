# **Raport Stanu Obecnego Rozwiązań Cyfrowych FeboLogistics**

## **1\. Kontekst Biznesowy i Ambicje Strategiczne**

FeboLogistics funkcjonuje jako operator 3PL/4PL z silną specjalizacją w korytarzach transportowych Polska – Wielka Brytania – Irlandia – Włochy. Firma znajduje się w fazie intensywnego skalowania:

* **Cele:**  
  * Zwiększenie floty do 200 jednostek (w tym roku dodatkowych 30 jednostek), zwiększenie przestrzeni magazynowej w obecnym budynku i zwiększenie zakresu usług magazynowych, zakup magazynu w Irlandii.  
  * W celu zwiększenia portfolio rozpatrywana są przewozy high value, pharma, just in time, ponadnormatywne i dystrybucyjne do poziomu palety. W tym celu rozpatrywana jest certyfikacja ISO, TAPA i pharma (GDP, ATP, CEIV Pharma IATA).  
  * W ramach obsługiwanych branży obecnie nie ma i nie planowane jest specjalizacja w jednym kluczowym kierunku co pomaga uniknąć efektu sezonowości.  

* **Model:**  
  * Hybryda transportu własnego i spedycji kontraktowej z silnym komponentem cross-dockingu w hubie w Stojadłach z wykorzystaniem naczep double deck i wynajmowanej przestrzeni magazynowej w Irlandii.  
  * Dodatkowo realizowana jest spedycja spotowa (głównie FTL), usługi celne (głównie na własne potrzeby) i magazyn (większa część magazynu wynajęta w całości, pozostała przestrzeń wykorzystywana pod cross-doking i  w małej skali usługi magazynowe do poziomu palety).    

* **Wizja:**  
  * Osiągnięcie pozycji regionalnego lidera w usługach logistycznych z wykorzystaniem cross dokingu na kierunku Polska \- Irlandia wraz z rozbudową usług towarzyszących oraz zwiększenie konkurencyjności poprzez rozwój technologiczny, a następnie rozwój nowych kierunków zgodnych z modelem biznesowym.

## **2\. Architektura IT i Infrastruktura**

Obecny ekosystem technologiczny opiera się na dwóch przeciwstawnych biegunach:

### **2.1. System Operacyjny (LogTMS)**

* **Technologia:** PHP Laravel \+ MySQL, frontend w JS/jQuery.  
* **Hosting i backup:**  
  * Serwer dedykowany (Hetzner, Niemcy)  
  * Backup realizowany tylko po stronie dostawcy  
  * Dostęp administratorski ze strony firmy obsługującej infrastrukturę IT oraz programisty.  
* **Charakterystyka:** System autorski, elastyczny, ale pozbawiony dokumentacji. Skupia 40% logiki na tematach księgowych, co obciąża procesy operacyjne. Procesom realizowanym w systemie brakuje wielu dodatkowych informacji co przekłada się na braki w danych analitycznych. System jest mało elastyczny pod kątem dodawania nowych pól (konieczne dodanie przez programistę)  
* **Moduły:**   
  * Kluczowy moduły zleceń od klientów z możliwością i łączenia ich w całości lub w części w trasy  
  * Istotny moduł bieżącego statusu operacyjnego pojazdu na podstawie, którego planowane są pojazdy  
  * Zlecenia magazynowe (realizowane w systemie są nie do końca zgodnie z założeniami systemu)  
  * Podstawowy dashboard pojazdów  
  * Fakturowanie z wysyłką zleceń do klientów (wprowadzanie zleceń do Optima poprzez OCR utworzonych FV) / obsługa KSeF w trakcie realizacji 40% prac  
  * Koszty realizacji zlecenia (głównie FV od przewoźników)  
  * Aplikacja mobilna i strona responsywna dla kierowców przewoźników pozwalająca na dostęp do podstawowych informacji  
* **Intergrowalność:**  
  * System obecnie posiada API umożliwiające pobieranie danych w formacie CSV z tabel baz danych,  
  * System obecnie nie zasila innych systemów (szczególnym minusem jest brak integracji z Optima np odnośnie do statusu płatności)  
  * Integracja z dostawcą GPS na w zakresie pozycji pojazdu  
  * KM liczone na podstawie google maps (możliwe podpięcie pod HERE maps)   
* **Rozwój i utrzymanie**:  
  * Prace rozwojowe oparte są o zgłoszenia do developera obsługującego system. Brak standaryzacji zgłoszonych prac i możliwości śledzenia ich statusu.  
  * Problemy operacyjne zgłaszane są na bieżąco (obecnie nie ma ich dużo), ale brak SLA

### **2.2. System Finansowy (Comarch Optima)**

* **Instalacja:**  
  * On-premise (lokalnie w HQ) na serwerze Windows.  
  * Dostęp dla użytkowników z wykorzystaniem RDS  
* **Baza danych:** MS SQL Server Express (darmowa, ale posiada krytyczne limity: 10 GB bazy, 1.4 GB RAM).  
* **Charakterystyka:** System do księgowości.  
* **Luka integracyjna:** Brak API między TMS a Optimą. Dane sczytywane niedoskonałym mechanizmem OCR, co generuje błędy, szczególnie przy fakturach zagranicznych.

### **2.3. Infrastruktura Sieciowa i Bezpieczeństwo**

* **Łączność:**  
  * open VPN w wersji Community  
  * stare przełączniki sieciowe o niskiej przepustowości, brak segmentacji VLAN.  
* Inne:  
  * File server \- cyfrowe archiwum  
  * Poczta w Azure (exchange online i office 365\) \- dużo skrzynek współdzielonych  
  * Pozostałość po poprzednim TMS (serwer linux)  
* Backup  
  * Lokalnie na drugi serwer  
  * Słaba przepustowość przełaczników  
* Bezpieczeństwo:  
  * Oprogramowanie w wersji community  
  * Ryzyko podlegania pod   
* **Rozwój:** Brak zasobów dedykowanych pod R\&D

## **3\. Sprzedaż i Relacje z Klientem**

Obszar ten charakteryzuje się wysoką orientacją na jakość relacji, przy jednoczesnym braku wsparcia przez zintegrowane narzędzia systemowe:

### **3.1. Struktura i Model Sprzedaży**

* **Zespół:** 3 handlowców dedykowanych oraz spedytorzy handlowi, którzy łączą opiekę nad klientem z operacjami. Klienci spedycyjni obsługiwani są dwutorowo przez handlowców i spedytorów w zależności od zadań.  
* **Segmentacja:**  
  * Koncentracja na średnich przedsiębiorstwach (np. producenci z przychodami do 30 mln zł)  
  * Specyfika klienta (niskie i lekkie ładunki, bez nacisku na pilny termin)  
* **Podejście:** Jakość nad ilością — unikanie masowego *cold mailingu* i *cold callingu* na rzecz spotkań bezpośrednich i pielęgnacji relacji.  
* **Cel:** Utrzymanie i rozwój współpracy z bieżącymi klientami oraz pozyskiwanie nowych.

### **3.2. Zarządzanie Relacjami (CRM)**

* **System:** TMS posiada uproszczony moduł CRM (widok Kanban, poziomy klientów), który jest niewystarczający dla potrzeb działu ze względu na ograniczone funkcjonalności i zbierane dane.  
* **Luki funkcjonalne:** Brak wspólnego kalendarza spotkań widocznego dla zespołu, brak historii kontaktów i notatek dostępnych dla planistów. Prowadzi to do sytuacji, w których handlowcy nie pamiętają o wcześniejszych wizytach u danego klienta.

### **3.3. Pozyskiwanie i Weryfikacja**

* **Narzędzia:** LinkedIn (wykorzystywany do identyfikacji osób decyzyjnych), bazy kontaktów branżowych.  
* **Analityka historyczna:** Wyszukiwanie klientów na podstawie danych z systemu (np. powtarzające się ładunki typu "spot" jako potencjał na kontrakt).

### **3.4. Komunikacja i Tracking**

* **Poczta:** Wykorzystywany Outlook z kalendarzem, jednak bez synchronizacji z modułem CRM w TMS.  
* **WhatsApp:** Główny kanał komunikacji (używany przez większość klientów i kierowców). Pracownicy sami rejestrują konta, co uniemożliwia archiwizację danych i tworzy silosy informacyjne na prywatnych telefonach.  
* **Tracking:** Klienci nie ufają automatycznym powiadomieniom; wymagają bezpośrednich danych z GPS lub statusów wysyłanych ręcznie mailem. Brak integracji z platformami typu p44 czy Shippeo.  
* **PODs**: CMR jest dodawany do systemu i wysyłany do klientów z FV. Mała liczba klientów wymagających korzystanie z ich platform do wrzucania CMR

### **3.5. Wycena i Planowanie**  
* **Polityka cenowa:** Brak ujednoliconej polityki; każdy spedytor stosuje własne modele wyceny.  
* **Specyfika ładunków:** Koncentracja na towarach niskich, bez silnego nacisku na terminy, często wymagających tylko jednego piętra załadunku.  
* **Zlecenia:** Wprowadzane ręcznie (brak AI do zaciągania danych). Istnieje funkcja kopiowania zleceń historycznych. TMS wysyła warunki zlecenia automatycznie do osoby kontaktowej po stronie klienta (co jest bardzo ważną polityką firmy).

### **4.1. Model Operacyjny i Przepływ Towarów**

* **Konsolidacja (Cross-docking):** Magazyn pełni kluczową funkcję przeładunkową. Proces polega na ściąganiu wielu zleceń (głównie z Mazowsza) na magazyn centralny, a następnie kompletowaniu ich w trasy i ładowaniu na naczepy międzynarodowe.  
* **Łańcuch Dostaw:** Model zakłada zbieranie ładunków w PL \-\> wysyłkę na magazyn przeładunkowy w Irlandii \-\> ponowne składowanie/przeładunek w IRL \-\> ostateczny rozładunek u klienta.  
* **Dystrybucja:** w Irlandii realizowana jest głównie własnymi autami (w tym jedna solówka z systemem rotacji kierowców) w Polsce własne auta \+ spedycja.  
* **Wymagania Załadunkowo/Rozładunkowe:** Specyfika klientów często narzuca ograniczenia techniczne związane z brakiem możliwości ładowania double deck. Kluczowe jest wykorzystanie tranzytu w weekend co wypełnia lukę na rynku (większość przewoźników nie chcę ładować na koniec tygodnia aby nie płacić kierowcy za weekend) i zapewnia klientom możliwie krótki tranzyt, gdyż często z ich perspektywy weekend nie jest uwzględniany.

### **4.2. Koordynacja Planista – Magazyn**

* **Komunikacja:** Przekazywanie informacji o tym, co i kiedy ma zostać załadowane, odbywa się obecnie głównie w formie słownej, maliowej lub z wykorzystaniem komunikatora WhatsApp. W TMS są tworzone zlecenia magazynowej, ale brakuje jasnego cyfrowego pomostu przekazującego instrukcje załadunkowe bezpośrednio do personelu magazynowego.  
* **Odtwarzanie Danych:** Trasy są często odtwarzane w systemie post-factum, co uniemożliwia monitorowanie postępów planowania w czasie rzeczywistym.  
* **Zarządzanie Przestrzenią:** Kierowcy wykorzystują metrówki do ręcznego informowania planistów o dostępności wolnego miejsca na naczepie.

### **4.3. Rozliczanie i Rentowność Tras**

* **Podział Przychodów:** Mechanizm przydzielania przychodów ze zleceń do konkretnych tras w obecnym systemie TMS nie działa poprawnie. Dzielenie zysków wymaga ręcznego pobierania i przeliczania danych.  
* **Kluczowe Metryki:** Model biznesowy Febo opiera się na "stawce na naczepie". Tradycyjne wskaźniki (stawka za km czy km na pojazd) mają drugorzędne znaczenie w porównaniu do efektywności wykorzystania przestrzeni ładunkowej przy wielu zleceniach LTL na jednej trasie.  
* **Zasoby w TMS:** Istnieje moduł pokazujący zlecenia nieprzypisane do tras (które mogą znajdować się fizycznie na różnych magazynach), jednak obecny moduł LTL nie w pełni obsługuje specyficzny model biznesowy firmy.

## **5\. Obsługa Zleceń i Komunikacja z Kierowcami**

Obszar ten opiera się na intensywnej wymianie informacji w czasie rzeczywistym, zdominowanej przez narzędzia mobilne i komunikatory:

### **5.1. Ekosystem Komunikacyjny (WhatsApp)**

* **Główne Narzędzie:** WhatsApp jest fundamentem operacyjnym. Służy do wysyłania planów, instrukcji, informacji o gotowości kierowcy do wyjazdu oraz zgłaszania awarii.  
* **Bariery Językowe:** Komunikacja odbywa się głównie w języku polskim, mimo że duża część kierowców to obcokrajowcy. Brak wbudowanych mechanizmów tłumaczenia instrukcji wewnątrz procesów.  
* **Zarządzanie Grupami:** Istnieją dedykowane grupy, np. "Ładunki" (zapobieganie dublowaniu kwotowań) czy grupy operacyjne z klientami (zawsze co najmniej dwie osoby po stronie Febo).  
* **Ograniczenia Techniczne:** Wersja desktopowa WhatsApp wykazuje niską wydajność ("muli") przy dużej skali wiadomości, mimo poprawnego działania na telefonach.  
* **Kontakty:** Każdy kierowca otrzymuje tabelę z kontaktami w poszczególnych sprawach.  
* **Klienci:** Do klientów wysyłana jest lista dostępnych aut w danym obszarze i często sami zgłaszają zainteresowanie na konkretny przewóz.  
* **Struktura firmy:** Firma ma stosunkowo mało pracowników, ale nie ma miejsca w którym można byłoby sprawdzić strukturę.

### **5.2. Aplikacje i Narzędzia Kierowcy**

* **Aplikacja Webowa:** Kierowcy są stale zalogowani przez link aktywacyjny. Pozwala ona na podgląd zlecenia i przesyłanie zdjęć (np. CMR). Aplikacja jest dostępna tylko w języku polskim.  
* **Dokumentacja Cyfrowa:** Wykorzystywany jest CamScanner lub OnlineCamScanner (z funkcją ramki do docinania zdjęć). Nazwy plików często generowane są w cyrylicy, co utrudnia ich późniejszą kategoryzację.  
* **Nawigacja i GPS:** Kierowcy korzystają z własnych urządzeń nawigacyjnych. Na ciągnikach zainstalowany jest Gbox (Eurowag) do śledzenia czasu pracy, jednak brak jest pełnej integracji z TMS.

### **5.3. Operacje Spedycyjne i Koordynacja**

* **Planowanie Pracy:**  
  * Kierowca otrzymuje plan na kilka dni, jednak nie jest on zapisywany systemowo.  
  * Trasy powtarzalne nie są szczegółowo rozpisywane w instrukcjach.  
  * Planiści planują i przekazują do realizacji głównie kierunek do irlandii  
  * Spedytor odpowiada za ściągnięcie kierowcy/przewoźnika do PL (szuka dla niego ładunku jeżeli nie ma takiego od planistów).  
* **Obsługa Awarii i Incydentów:**  
  * W przypadku awarii proces jest wieloetapowy — kierowca kontaktuje się bezpośrednio z osobą odpowiedzialną, która w razie potrzeby instruuje spedytora na grupie WhatsApp o konieczności podjęcia dalszych działań.  
  * Odnośnie do incydentów nie ma jednego ustalonego schematu. Przestoje u klientów nie są monitorowane, a informacje o spóźnieniach udostępniane jeżeli klient o to dopytuje.  
* **Spedycja Kontraktowa:** Traktowana na równi z flotą własną. Przewoźnicy kontraktowi często udostępniają pojazdy wraz z kierowcami lub jeżdżą osobiście.  
* **Obsługa SPOT:** Obejmuje "wszystko co się trafi" na giełdach (Trans, Timo), stanowiąc uzupełnienie dla głównej floty.  
* **Zamknięcie zlecenia:** Potwierdzenie realizacji, zebranie POD na co spedytor ma dwa dni od zakończenia zlecenia.  
* **Nocna zmiana:** Na dziś ciężko wprowadzić w związku z ograniczeniami przepływu informacji między dzienną i nocną zmianą (wszystko jest na WhatsApp). 

### **5.4. Administracja i Logistyka Promowa**

* **Rezerwacje:** Bookowanie promów odbywa się manualnie bezpośrednio na platformach operatorów.  
* **Odprawy Celne:** Każdy spedytor posiada własny folder z odprawami (brak wspólnej bazy). Dane w formatkach celnych (Excel) są wprowadzane ręcznie bez automatycznego zaciągania powtarzalnych informacji.  
* **Zlecenia Wstępne:** W systemie TMS brakuje funkcjonalności zleceń wstępnych oraz informacji o ich dostępności dla dyspozytora.  
* **Planowanie kierowców:** 
 * Wyjazdy kierowców planowane ustalane są z działem technicznym na grupie WhatsApp.
 * TMS nie posiada dedykowanego miejsca do zarządzania dostępnością kierowców (istniejące widoki terminów). 
 * Kadry korzystają z systemu w ograniczonym zakresie.


### **5.5. Monitoring i Raportowanie**

* **Powiadomienia:** Aktywność w aplikacji kierowcy generuje powiadomienia mailowe dla spedytorów.  
* **Dashboardy:** Istnieją dashboardy przedstawiające strukturę floty ("drzewo"), z których dane można eksportować do Excela i przetwarzać w PowerQuery na potrzeby widoków planistycznych.  
* **Luki w Śledzeniu:** Przewoźnicy spotowi nie są w ogóle śledzeni. Brak jest systemowych narzędzi do monitorowania przestojów u klienta czy automatycznego raportowania spóźnień.

## **6\. Obsługa Magazynu i Cross-docking**

Magazyn stanowi centralny punkt operacyjny, łączący funkcje przeładunkowe z usługami składowania długoterminowego:

### **6.1. Systemowe Zarządzanie Magazynem**

* **Moduł TMS:** Obsługa magazynu opiera się na dedykowanym module wewnątrz systemu TMS, który jest obecnie uznawany za wystarczający dla bieżących potrzeb.  
* **Typy Zleceń:** System rozróżnia standardowe zlecenia transportowe od dedykowanych "zleceń magazynowych" na konkretne usługi składowania. Po utworzeniu zlecenia na magazynowanie, system automatycznie wysyła potwierdzenie mailowe do klienta.  
* **Kalendarz:** Dostępność i praca personelu magazynowego koordynowana jest poprzez kalendarz dostępności magazynierów.  
* **POD:** Obecny system pozwala na generowanie CMR wraz z kodem kreskowym.

### **6.2. Zarządzanie Przestrzenią i Składowaniem**

* **Struktura Magazynu:** Przestrzeń jest podzielona na sekcje regałowe (przeznaczone do długiego składowania) oraz miejsca na podłodze (dedykowane dla krótkiego składowania i szybkiego cross-dockingu).  
* **Identyfikacja:** Regały są oznaczone, jednak system nie pozwala obecnie na precyzyjne określenie procentowego stopnia wykorzystania danej lokalizacji. Brak jest również dokładnej informacji systemowej o precyzyjnym miejscu składowania konkretnego ładunku.  
* **Cross-docking:** Proces operacyjny polega na zrzucie towaru, naklejeniu etykiety z kodem kreskowym (generowanym i drukowanym bezpośrednio z TMS) oraz ponownym załadowaniu na trasę.  
* **Awizacja:** Rezerwacja miejsca na magazynie odbywa się poprzez proces awizacji slotu.

### **6.3. Finanse i Rozliczenia Magazynowe**

* **Cennik:** Istnieje zdefiniowany cennik na przetrzymywanie towaru (palety), przy czym wyceny niestandardowe są ustalane indywidualnie. Faktury za usługi magazynowe wystawiane są bezpośrednio z systemu TMS.  
* **Zmienność Operacyjna:** Dane o planowanym czasie składowania na zamówieniu klienta często różnią się od stanu faktycznego (daty ulegają przesunięciom), co wymaga elastyczności w rozliczeniach.  
* **Obsługa Płatności:** Magazynierzy są uprawnieni do przyjmowania płatności na miejscu.

### **6.4. Wyzwania Operacyjne i Koordynacja**

* **Zarządzanie Zespołem:** Kluczowym zadaniem jest zarządzanie dostępnością pracowników magazynowych w korelacji z harmonogramem planowanych załadunków, o których informacje płyną z TMS.  
* **Agencja Celna:** W związku z otwieraniem własnej agencji celnej, magazyn musi wydzielić i zarządzać przestrzenią, w której będą oczekiwać odprawione samochody.  
* **Terminowość:** Największym wyzwaniem wpływającym na płynność pracy magazynu jest obecnie brak terminowości kierowców (opóźnienia w oknach czasowych).  
* **Zarządzanie Siecią:** Model zakłada konieczność koordynacji operacji na różnych magazynach, w tym w innych krajach (Irlandia), co wymaga sprawnego przepływu informacji o statusie ładunków między obiektami.

## **8\. Obsługa Celna i Agencja Celna**

Obszar ten stanowi krytyczny, wysoce manualny pomost między spedycją a urzędami państwowymi, realizowany w trybie 24/7:

### **8.1. Ekosystem Narzędziowy i Platformy**

* **Główne Systemy:**  
  * **Custran.com:** Platforma chmurowa (model subskrypcyjny) używana do generowania ENS oraz T2.  
  * **Hussar:** Aplikacja desktopowa pełniąca funkcję analogiczną do Custran (generowanie numerów LRN, obsługa T2).  
  * **Akanea:** Aplikacja desktopowa wykorzystywana głównie do generowania ENS.  
* **Portale Rządowe i Branżowe:**  
  * **HMRC:** Rejestracja dokumentów w celu uzyskania dwóch numerów GMR (Goods Movement Reference).  
  * **PBN (Pre-Boarding Notification):** Obsługa przez rządową stronę roro-control.  
  * **douane.gov:** Portal do wprowadzania danych z systemu Akanea (ENS).  
  * **EC Europa:** Strona wykorzystywana do ręcznego sprawdzania, czy tranzyt został poprawnie zamknięty.

### **8.2. Przepływ Informacji i Dokumentacji**

* **Inicjacja Procesu:** Spedytorzy przesyłają do agenta celnego manifest w formacie Excel (dane z maila). Dodatkowo informacja o konieczności odprawy przekazywana jest na WhatsApp.  
* **Weryfikacja:** Agent celny ręcznie porównuje zgodność danych między manifestem Excel, dokumentem CMR a wygenerowanym dokumentem T2.  
* **Zamykanie Tranzytu:** Kierowca otrzymuje dokument ENS (często na WhatsApp), skanuje go, co skutkuje zamknięciem tranzytu T2. Zdjęcie potwierdzające odbiór T2 z urzędu trafia na dedykowaną skrzynkę mailową.  
* **Archiwizacja:** Komplet dokumentów celnych jest składowany na dysku wspólnym. Równolegle prowadzony jest manualny rejestr odpraw w pliku Excel, do którego dostęp mają wszyscy uprawnieni pracownicy.

### **8.3. Komunikacja z Kierowcą**

* **Kanał WhatsApp:** Główny kanał przesyłania kompletu dokumentów (GMR, ENS, T2) bezpośrednio do kierowcy. Dokumenty wysyłane są po uzyskaniu statusu "released" w systemach celnych.  
* **Wyzwania Komunikacyjne:** Aplikacja desktopowa WhatsApp wykazuje niestabilność na komputerach agentów, co utrudnia płynną wysyłkę plików dokumentacji.

### **8.4. Zarządzanie Kodami HS i Towarami**

* **Klasyfikacja:** Kody HS wyszukiwane są ręcznie w systemie ISZTAR na podstawie opisu towaru z CMR.  
* **Uogólnienia:** W przypadku niejednoznaczności spedytorzy/agenci wybierają opcje uogólnione (np. "pozostałe").  
* **Bazy Danych:** System Custran posiada własną bazę nadawców i odbiorców zbudowaną na podstawie historycznych T2 (możliwość eksportu/importu), jednak baza ta nie jest zmapowana z bazą klientów w głównym TMS.

### **8.5. Organizacja Pracy i Kierunki**

* **Dostępność:** Obsługa celna prowadzona jest przez 7 dni w tygodniu w godzinach 08:00 – 24:00 (często do 01:00 w zależności od potrzeb nocnej zmiany).  
* **Zasięg Operacyjny:** Obecnie własna obsługa koncentruje się na relacjach Irlandia \<-\> Polska. Pozostałe kierunki realizowane są przy wsparciu zewnętrznych agencji.  
* **Szablony:** Różne kierunki (np. tranzyt z UE) wymagają stosowania odmiennych szablonów manifestu w Excelu przesyłanych do partnerów.

### **8.6. Wyzwania Operacyjne**

* **Manualność:** Procesy takie jak przepisywanie danych z manifestów do systemów celnych czy generowanie PBN/GMR odbywają się bez automatycznego zaciągania danych z TMS.  
* **Monitoring:** Brak systemowego statusu odprawy celnej w TMS; informacja o zamknięciu tranzytu wymaga sprawdzania zewnętrznych stron www.  
* **Integracja:** Brak bezpośredniego połączenia między wykupionym biletem promowym a automatycznym wygenerowaniem numeru GMR.

## **9\. Post-Realizacja i Finanse**

Obszar ten koncentruje się na domykaniu operacji transportowych pod kątem finansowym oraz integracji danych operacyjnych z systemami księgowymi:

### **9.1. Proces Fakturowania Sprzedaży**

* **Struktura Zespołu:** Obsługa fakturowania jest rozdzielona osobowo — inne osoby odpowiadają za fakturowanie transportu własnego, a inne za obszar spedycji \+ zespół księgowości i osoba odpowiadająca za płatności.  
* **Przebieg w TMS:**  
  * Fakturowanie odbywa się w oparciu o filtry w TMS (np. "zamknięte zlecenia").  
  * Przed wystawieniem faktury następuje weryfikacja danych ze zlecenia klienta z danymi wprowadzonymi do systemu (m.in. stawki, daty rozładunku).  
  * Błędy są raportowane wstecznie do spedytorów w celu poprawy danych.  
  * Warunki fakturowania (np. terminy płatności, specyficzne wymogi klienta) są zaciągane bezpośrednio z karty klienta w TMS.  
* **Fakturowanie Zbiorcze:** System umożliwia generowanie faktur zbiorczych dla klientów.  
* **Autofakturowanie:** Funkcja ta istnieje w TMS, jednak jej powszechne użycie jest ograniczone przez niewystarczającą jakość danych wejściowych.

### **9.2. Obsługa Płatności i Windykacja**

* **Moduł Płatności w TMS:** System posiada moduł do oznaczania faktur jako zapłacone. Możliwe jest rozliczanie wpłat masowych (jeden przelew za wiele faktur).  
* **Monitoring:** Brak jest obecnie dedykowanych raportów podsumowujących fakturowanie oraz raportów o zleceniach niezamkniętych, co utrudnia bieżącą kontrolę przychodów.  
* **Luki w Integracji:** Brak automatycznego połączenia wyciągów bankowych z modułem płatności w TMS (rozliczenia manualne).

### **9.3. Procesy Kosztowe i Obieg Faktur**

* **Kanały Wpływu:** Faktury kosztowe (spedycyjne, paliwowe, administracyjne) wpływają wieloma kanałami: mailowo (dedykowana skrzynka), poprzez WhatsApp oraz w formie papierowej.  
* **Monitoring:** Brak jest obecnie dedykowanych raportów podsumowujących koszty (rachunek zysków i strat jest przygotowany jako roboczy w PowerBI).

### **9.4. Integracja z Księgowością (Optima)**

* **Eksport Danych:** Księgowanie sprzedaży polega na eksporcie faktur z TMS i ich imporcie do Optimy poprzez OCR (z ograniczoną skutecznością).  
* **Problem OCR:** Obecnie Optima wykorzystuje własny moduł OCR do wczytywania faktur, który wykazuje niską skuteczność w przypadku faktur zagranicznych.  
* **Interfejsy API:** Comarch Optima posiada moduł API, który można aktywować, jednak obecnie nie ma bezpośredniej, dwukierunkowej integracji TMS \<-\> Optima (np. synchronizacja statusu płatności czy danych kontrahentów).

### **9.5. Raportowanie i Analiza Finansowa**

* **PowerBI:** Raporty bazują na danych wyciąganych z Optimy.  
* **Wyzwania Analityczne:**  
  * Brak modułu budżetowania w bieżących strukturach systemowych.  
  * Brak modułu do rozliczania kierowców w TMS.  
  * Niska wiarygodność raportów BI w czasie rzeczywistym z powodu opóźnień w spływie dokumentów i braku rezerw kosztowych.

### **9.6. Wyzwania i Bariery**

* **Jakość Danych:** Niestaranność spedytorów przy zamykaniu zleceń uniemożliwia pełną automatyzację fakturowania.  
* **Walidacje:** Brakuje systemowych walidacji na kartach klientów pod kątem poprawności stawek VAT czy danych adresowych przed wystawieniem FV.  
* **Rozproszona Dokumentacja:** Wielokanałowość wpływających dokumentów kosztowych (papier, mail, WhatsApp) generuje ryzyko zagubienia faktur.  
* **KSeF:** Wdrożenie obsługi KSeF jest w toku. Rozważane są scenariusze pobierania faktur bezpośrednio z rządowej platformy i ich dalsza obróbka.

## **10\. Windykacja i Zarządzanie Należnościami**

Obszar windykacji łączy działania automatyczne z manualną obsługą relacji z klientami, mając na celu utrzymanie płynności finansowej:

### **10.1. Struktura i Organizacja Działu**

* **Zespół:** Dwie osoby dedykowane do działu windykacyjno-weryfikacyjnego.  
* **Komunikacja:** Maile wysyłane są zazwyczaj ze skrzynek imiennych pracowników, jednak zespół posiada również dostęp do wspólnej skrzynki "windykacja".  
* **Specyfika Klienta:** Duża część klientów opóźnia płatności do momentu podjęcia bezpośredniego kontaktu przez dział windykacji.

### **10.2. Automatyzacja Windykacji**

* **Harmonogram Powiadomień:** System posiada automatyczne mechanizmy wysyłki przypomnień:  
  * 3 dni przed terminem płatności.  
  * 7 dni po terminie.  
  * 14 dni po terminie.  
* **Skuteczność Automatów:** Odpowiedzi klientów na automatyczne powiadomienia są rzadkie, co wymusza przejście do kontaktu manualnego.

### **10.3. Procesy Operacyjne i Rejestracja Danych**

* **Monitoring Przyczyn:** Przyjęty standard zakłada, że najpóźniej 7 dni po terminie płatności dział windykacji musi znać konkretną przyczynę braku wpłaty.  
* **Zarządzanie Terminami:** Windykatorzy mają możliwość wpisania do systemu deklarowanego terminu zapłaty uzyskanego od klienta.  
* **Wymogi Dokumentowe:** Na profilu klienta w TMS oznaczone są specyficzne wymagania dotyczące dokumentów (np. konieczność przesłania oryginału wraz z kopią), co ma zapobiegać opóźnieniom wynikającym z błędów formalnych.  
* **Ubezpieczenie Należności:** Firma korzysta z ubezpieczenia należności, co istotnie wpływa na dyscyplinę klientów w zachowywaniu terminów płatności.

### **10.4. Analityka i Monitoring DSO**

* **Narzędzia:** Wskaźnik DSO (Days Sales Outstanding) monitorowany jest bezpośrednio w systemie Optima oraz poprzez raporty w PowerBI.  
* **Zmienność w Czasie:** Obecnie brakuje zaawansowanych narzędzi do sprawdzania i wizualizacji zmian w danych płatniczych w dłuższych trendach czasowych.

### **10.5. Wyzwania i Luki Analityczne**

* **Ocena Klienta:** Brak jest systemowego mechanizmu oceny klientów, którzy generują dużą liczbę niedopłat lub uporczywie spóźniają się z płatnościami (analiza kosztów windykacji vs marża z klienta).  
* **Dostęp do Informacji:** Brakuje narzędzi typu "hurtownia danych" lub wewnętrznych interfejsów analitycznych (np. chat analityczny), które pozwalałyby kadrze zarządzającej na szybkie uzyskiwanie odpowiedzi na pytania o trendy płatnicze bez konieczności manualnego przygotowywania raportów.

## **11\. Obsługa Techniczna Własnej Floty**

Dział techniczny odpowiada za utrzymanie sprawności pojazdów, zarządzanie wyposażeniem oraz bieżący monitoring eksploatacyjny:

### **11.1. Zarządzanie Pojazdami w Systemie**

* **TMS jako centralna baza:** System TMS zawiera kompletne informacje o pojazdach, w tym daty przeglądów i inne kluczowe terminy operacyjne.  
* **Inspecto:** Do przeprowadzania szczegółowych inspekcji pojazdów wykorzystywane jest narzędzie Inspecto. Pracownicy działu technicznego oraz kierowcy regularnie wykonują przeglądy ciągników i naczep z użyciem tej aplikacji.  
* **Rezerwacje:** Dział techniczny ma możliwość rezerwowania pojazdów bezpośrednio w dashboardzie planistycznym, co jest sygnalizowane odpowiednią notatką dla dyspozytorów.

### **11.2. Monitoring Eksploatacji i Paliwa**

* **Tacho i przebiegi:** Systematycznie realizowane są odczyty danych z tachografów. Przebiegi pojazdów są dodatkowo monitorowane w dedykowanym pliku Excel na podstawie, którego planowane są obsługi.  
* **Zarządzanie Tankowaniami:** Wszystkie tankowania są rejestrowane w systemie TMS. Kierowcy dodatkowo zapisują tankowania na papierowych kartach drogowych, co według ocen nie jest procesem czasochłonnym.  
* **Analiza Spalania:** Spalanie analizowane jest codziennie. Przyjęto normę 26l/100km – przekroczenie tej wartości skutkuje oznaczeniem na czerwono i prośbą do kierowcy o wyjaśnienie przyczyny (analiza raportów spalania trafia również do zarządu).  
* **Stacje Paliw:** Kierowcy korzystają z wyznaczonych stacji. W przypadku ich braku, personel wyznacza stacje DKV bezpośrednio na portalu operatora.

### **11.3. Utrzymanie i Wyposażenie**

* **Przygotowanie do Trasy:** Po zjeździe na bazę pracownicy przeglądają jednostki i uzupełniają brakujące wyposażenie. Zauważalna jest wysoka dbałość kierowców o powierzone mienie (rzadkie przypadki gubienia wyposażenia).  
* **Zapas Opon:** Standardem wyposażenia są dwa koła zapasowe na wypadek wystrzału opony w trasie.

### **11.4. Obsługa Awarii i Napraw**

* **Zgłoszenia:** Kierowcy zgłaszają problemy bezpośrednio przez WhatsApp. W zależności od skali usterki, informacja trafia do konkretnej osoby lub na wspólną grupę operacyjną.  
* **Naprawy Assistance:** Wszystkie interwencje assistance są rejestrowane w Excelu i później weryfikowane pod kątem zgodności z otrzymanymi fakturami.  
* **Awarie weekendowe:** Dział techniczny zapewnia wsparcie również w weekendy w przypadku nagłych awarii w trasie.

### **11.5. Zarządzanie Szkodami i Ubezpieczeniami**

* **Dokumentacja Szkód:** W przypadku uszkodzeń, kierowca ma obowiązek zebrać pełną dokumentację zdjęciową na miejscu. Po powrocie na bazę odbywają się oględziny i dodatkowa sesja zdjęciowa.  
* **Szkody Zagraniczne:** Naprawy i formalności związane ze szkodami za granicą są procesowane przez polskie oddziały partnerów/ubezpieczycieli.  
* **Polityka AC:** Firma przyjęła zasadę niewykorzystywania polisy AC w przypadku szkód o wartości poniżej 2 tys. zł.  
* **Odpowiedzialność Kierowcy:** W sytuacjach wynikających z rażącego niedbalstwa, kierowcy są obciążani kosztami naprawy. Wszystkie zgłoszone incydenty są ewidencjonowane w rejestrze szkód.

## **12\. Analityka i Raportowanie**

Obszar analityki opiera się na wykorzystywaniu danych bezpośrednio z wielu systemów źródłowych przy wsparciu zewnętrznych ekspertów:

### **12.1. Ekosystem Raportowy i Narzędzia**

* **PowerBI:** Główne narzędzie analityczne. Zarządzanie kontem i infrastrukturą PowerBI realizowane jest przez zewnętrznych informatyków.  
* **Excel:** Powszechnie wykorzystywany do obróbki danych pobieranych bezpośrednio z TMS oraz innych narzędzi zewnętrznych (np. portale paliwowe DKV).  
* **Zasoby Zewnętrzne:** Procesy raportowe przygotowuje zewnętrzny analityk / konsultant PowerBI. Posiada on szerokie doświadczenie w pracy z systemem Comarch Optima oraz zna strukturę jego tabel bazodanowych.

### **12.2. Źródła i Przepływ Danych**

* **LogTMS:** Dane pobierane są poprzez API w formacie plików CSV na potrzeby PowerBI lub importowane do plików Excel.  
* **Comarch Optima:** Dostęp do danych realizowany jest poprzez VPN bezpośrednio z tabel bazy MS SQL (zapytania SQL).  
* **Narzędzia Zewnętrzne:** Raporty operacyjne (np. zestawienia tankowań DKV) są ręcznie pobierane z portali dostawców i integrowane w środowisku Excel/PowerBI.

### **12.3. Standardy i Zakres Raportowania**

* **Standardy Kontrolingu:** Raportowanie finansowe dąży do zgodności ze standardem kontrolingu (KSRF 300).  
* **Analiza Wyników:** Przygotowane są kluczowe dokumenty finansowe, takie jak Bilans oraz Rachunek Zysków i Strat (P\&L), jednak obecnie nie są one w pełni wykorzystywane w bieżącym zarządzaniu operacyjnym.  
* **Budżetowanie:** Dane analityczne stanowią podstawę do tworzenia budżetów (BDGT).

### **12.4. Wyzwania w Analizie Rentowności**

* **Logika Przychodu na Trasę:** Jednym z największych wyzwań jest poprawne wyliczenie przychodu przypadającego na konkretną trasę. Logika ta jest trudna do zdefiniowania w systemie, a uzyskanie konkretnego fragmentu kodu odpowiedzialnego za te obliczenia w TMS jest obecnie bardzo utrudnione.  
* **Zrozumienie Danych:** Przychód na trasę jest obecnie parametrem trudnym do interpretacji i uzyskania w sposób zautomatyzowany, co ogranicza precyzję analiz rentowności poszczególnych jednostek transportowych.
