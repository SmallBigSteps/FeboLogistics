
### **Rekomendacje Rozwoju Ekosystemu Cyfrowego FeboLogistics**

#### **1. Strategiczna Architektura Systemowa (Core IT)**
W celu wsparcia skalowania floty do 200 jednostek oraz rozwoju hubu cross-dockingowego, proponuje się zmianę podejścia z systemów autorskich na integrację wyspecjalizowanych rozwiązań zewnętrznych:

*   **1.1. Rozwój i Odchudzanie LogTMS:**
    *   **Strategia wyjścia:** Stopniowe przenoszenie modułów fakturowania, kadr, floty i kart paliwowych do systemów zewnętrznych.
    *   **Specjalizacja:** Pozostawienie w LogTMS jedynie kluczowej logiki łączenia zleceń w trasy i obsługi cross-dockingu.
    *   **Utrzymanie:** Konieczność zapewnienia ciągłej aktualizacji i instancji testowej dla systemu.
    *   **Współpraca z deweloperem:** Wdrożenie systemu ticketowego (np. JIRA) do zarządzania zapotrzebowaniem użytkowników i pracami programistycznymi.

*   **1.2. Wdrożenie Systemu WMS:**
    *   **Charakterystyka:** Zewnętrzne, stabilne narzędzie z możliwością skalowania na inne obiekty (w tym magazyn w Irlandii).
    *   **Funkcjonalność:** Zarządzanie siecią magazynów, przejazdami oraz precyzyjna identyfikacja miejsc składowania (kody QR na regałach).

*   **1.3. Profesjonalizacja CRM:**
    *   **Narzędzie:** Przejście na zewnętrzny system nastawiony na aktywną obsługę handlową.
    *   **Funkcje krytyczne:** Wspólny kalendarz spotkań, obowiązkowe notatki ze spotkań (przetwarzane przez AI) oraz mapowanie struktury kontaktów u klienta.

#### **2. Finanse, Księgowość i Integracja KSeF**
Automatyzacja procesów rozliczeniowych w celu wyeliminowania błędów ręcznego wprowadzania danych:

*   **2.1. Obsługa Faktur i Płatności:**
    *   **KSeF:** Wykorzystanie platformy Saldeo lub analogicznej do pobierania faktur kosztowych i ich integracji z Optimą.
    *   **Automatyzacja:** Bezpośredni transfer faktur przychodowych z TMS do Optimy poprzez KSeF (zamiast zawodnego OCR).
    *   **Płatności:** Integracja wyciągów bankowych z modułem płatności w TMS.

*   **2.2. Moduły Finansowe w TMS:**
    *   Wdrożenie systemowego rozliczania kierowców oraz walidacji danych kontrahentów (stawki VAT, adresy).

#### **3. Komunikacja i Zarządzanie Operacyjne**
Cyfryzacja punktów styku między biurem, magazynem a kierowcami:

*   **3.1. Ekosystem WhatsApp Business:**
    *   Wdrożenie Zekju/Slickshift w celu zapewnienia ciągłości przepływu informacji (umożliwi to uruchomienie nightshift).
    *   Tłumacznie w czasie rzeczywistym w platformech Zekju/Slickshift.
    *   Weryfikacja płatnych planów i formatek wiadomości WhatsApp Business w komunikacji wewnętrznej.

*   **3.2. Narzędzia Wspomagające Kierowców:**
    *   Przygotowanie wielojęzycznych wersji instrukcji (DeepL) i dysku sieciowego na którym te dokumenty będą dostępne.
    *   Cyfrowy Panel Kontaktowy Kierowcy: Opracowanie tabeli kontaktów przypisanych do konkretnych spraw, zasilanej danymi systemowymi.


#### **4. Analityka, Raportowanie i Data Science**
Przejście od raportowania w Excelu do dynamicznego zarządzania danymi (Business Intelligence):

*   **4.1. Hurtownia Danych i Power BI:**
    *   Konsolidacja rozproszonych danych (TMS, Optima, DKV) w jednej hurtowni (POC).
    *   Udostępnienie raportów Power BI użytkownikom bez licencji poprzez SharePoint.
    *   Automatyzacja raportów cyklicznych (CRON) dla zleceń niezamkniętych i monitoring KPIs (np. procent załadowania naczepy, dywersyfikacja przychodów).
    *   Analityka Opensource (Metabase): Przeprowadzenie analizy potrzeb i ROI dla wdrożenia narzędzia Metabase jako uzupełnienia ekosystemu analitycznego.

*   **4.2. Analiza Wyników i Edukacja:**
    *   Wdrożenie cyfrowego monitorowania P&L, Cashflow i Budżetu.
    *   Szkolenia z zaawansowanej obsługi Excela przy wsparciu AI.
    *   Przeniesienie codziennej analizy do Power BI (np. spalania - automatyczne flagowanie odchyleń powyżej 26l).

#### **5. Nowoczesne Technologie (AI i Automatyzacja)**
Wykorzystanie sztucznej inteligencji i narzędzi workflow do eliminacji powtarzalnych zadań:

*   **5.1. Automatyzacja Workflow (n8n/RPA):**
    *   Optymalizacja procesów operacyjnych (n8n) i księgowych (RPA).
    *   Automatyczne sprawdzanie zamknięcia tranzytów (ec.europa) oraz uzupełnianie danych na stronach rządowych (GMR/HMRC).

*   **5.2. Agenci i Asystenci AI (RAG):**
    *   **Strategia AI:** Weryfikacja potencjału ChatGPT Business pod kątem usprawnień procesowych (szkolenia wewnętrznych).
    *   **Wycena:** Aplikacja do estymacji stawek na podstawie danych historycznych i API Here Maps.
    *   **Obsługa:** Czat AI dla kierowców (instrukcje) oraz asystent do obsługi reklamacji w spedycji.
    *   **Cło:** Asystent do wyznaczania kodów HS w języku naturalnym.
    *   **Bezpieczeństwo:** AI Verifier do analizy paragrafów w zleceniach pod kątem ryzyk prawnych.
    *   **Asystent AI do Reklamacji:** Wdrożenie narzędzia wspomagającego spedycję w obsłudze incydentów i reklamacji
    *   **Asystent Marketingowy AI:** Opracowanie i wdrożenie narzędzia wspierającego procesy budowania wizerunku oraz komunikacji rynkowej

#### **6. Specyficzne Optymalizacje Operacyjne**
Narzędzia dedykowane dla konkretnych wąskich gardeł procesowych:

*   **6.1. Planowanie i Magazyn:**
    *   Wdrożenie Goodloading lub utworzenie własnej aplikacji dla naczep double deck w celu optymalizacji przestrzeni (waga, kolejność rozładunku).
    *   Monitoring terminowości na slotach magazynowych poprzez geofencing.
    *   Rozbudowa strony WWW o kalkulator usług magazynowych.
    *   Uproszczenie wprowadzania zleceń wstępnych w celu ułatwienia wymiany informacji o wolnych mocach przerobowych.
    *   Tablica Planistyczna: Prezentacja danych z TMS w formie wspomagającej planowanie
    *   Geofencing: Wykorzystanie wirtualnych stref do monitorowania terminowości kierowców na slotach magazynowych

*   **6.2. Cło, Sprzedaż i Limity:**
    *   Optymalizacja manifestu celnego (integracja Excel z bazą TMS i platformami celnymi).
    *   Wykorzystanie bazy Custran jako źródła leadów dla handlowców.
    *   Wykorzystanie AI (LinkedIn, Perplexity) do budowy baz producentów i identyfikacji osób decyzyjnych.
    *   Wdrożenie DeepL API do automatycznego tłumaczenia kontraktów i dokumentacji.
    *   BtrustUP: Wdrożenie unikalnego narzędzia do weryfikacji przewoźników przy zwiększaniu skali spedycj

*   **6.2. Ogólne:**
    *   Struktura High-Level: Przygotowanie schematu informacyjnego określającego kompetencje pracowników i tematykę, w której można się z nimi kontaktować.

#### **7. Infrastruktura IT i Bezpieczeństwo**
Zapewnienie stabilności i bezpieczeństwa fundamentów technologicznych:

*   **7.1. Sieć i Cyberbezpieczeństwo:**
    *   Wdrożenie firewalla klasy Palo Alto (zastąpienie wersji community) oraz segmentacji VLAN.
    *   Audyt prawny pod kątem zgodności z dyrektywą NIS2.
    *   Konfiguracja posiadanego serwera NAS do celów backupu (zlecenie zewnętrzne).

*   **7.2. Sprzęt i Innowacje:**
    *   Skompletowanie sprzętu R&D (poleasingowego) lub wykorzystanie VPS do własnych aplikacji.