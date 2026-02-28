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