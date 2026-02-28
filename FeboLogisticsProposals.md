
w - do wprowadzenia WMS (potencjalnie do wykorzystania na wielu magazynach w różnych krajach)
w - wdrożenie rozwiązań AI (n8n)
w - optymalizacja procesów w księgowości RPA

w - utworzenie hurtowni danych
w - zamiast korzystać z OCR dla FV przychodowych lepiej siciągać je z KSeF
w - wdrożenie systemu zewnętrznego wymaga jego ciągłego utrzymywania i aktualziacji aby  miało to sens
w - przydałby się jakiś system do współpracy z dostawcą JIRA lub coś w tym stylu i ustalenie cyklicznych spotkań
w - zamiast rozwoju aplikacji dla kierowców do rozpatrzenia Zekju
w -- system magazynowy zewnętrzny najlepiej 
w - NAS do backup - jest dostepny w HQ ale po przeprowadzce nie jest skonfigurowant
w - brak zabezpieczeń vlan (brak dotepu do przełaczników - warto zainwestować)
w - oraz niejasny status zgodności z dyrektywą NIS2.
w - pod R&D ale możliwe skompletowanie jakiegoś sprzętu polesingowego - plan w zalożności od narzędzi
w - nie korzystali, dotychczas głównie serwery plików / do rozpatrzenia czy nie lepiej inwestować w jakis hosting vps do nowych narzędzi
w - community wersje - przydałoby się jakieś paloalto 
w - rozpoznanie rynku dostawców zewnętrznych pod kątem CRM z możliwością integracji
w - narzędzie crm powinno być nastawione na obsługę bieżącą zleceń i obsługę handlową
w - integracja z CRM powinna zaimportować dane z TMS
w - konieczna organizacja w CRM kalendarza spotkań widoczny dla innych użytkowników
w - większość klientów korzysta z whatsUP może warto rozważyć konto business
w - tracking wysyłany mailem - może automat AI odpowiadający o na status zlecenia na podstawie danych w TMS ale ich nie ma
 - wyszukiwanie nowych klientów
    - bazy kontaktów osób zajmujących się konkretną dziedziną w jakiejś firmie 
    - główne źródło to linked in czy jesty możliwość korzystania z chata żeby sprawdzić kto jest tam za co odpowiedzialny
    - dostęp do bazy linked in przez AI (żeby poztyskać konkretny kontakt)
    - wyszukiwanie klientów głównie na podstawie danych historycznych, na podstawie bazy danych z systemu (jak wyciagać takie dane - kilkukrotnie powtórzony spot powinien mieć proponowany kontakt)
    - baza danych producentów konkretnych porduktów średniej wielkości przedsiębiorst do np do 30mln przychodów - raczej melodia przyszłosci nie musi być od razu
 - szkolenie AI (perplexity)
 - tłumaczenia kontraktów - wykupić konto na DeepL
 - sprawwdzać pozyskiwane zlecenia pod kątem warunków zlecenia żeby wyrzucić niebezpieczne elementy a następnie z AI wyłapać niebezpieczne paragrafy + dodać jakieś kluczowe ryzykowne zapisy
 - aplikacja goodloading dla trans - wrzucasz w program ilość palet i rozmarach i pokazuje jak to rozłożyć (pomysł na aplikację zewnętrzną) - wykorzystanie do podwójnych podłóg - google AI (oprzeć się na flocie Febo) - narzędzie dla planistów
 - fajnie byłoby to połączyć w systemie (czy obsłuży to TMS) - pozyskać informację z TMS
 - jak łączyć zlecenia ze sobą w narzędziu planistycznym (znaczenie ma waga, kolejność rozładunku, wymiar, podlłoga ma cztery sekcje, na każdej sekcji można zrobic inny podział - ładunki non stack)
 - spedytorzy mają inne modele wyceniania, nie ma polityki cenowej, brak informacji planisty o spotkaniu z klientem jakieś notatki po spotkaniu, które powinny być podsumowanie w RAG
 - każde spotkanie z klientem powinno mieć notatkę, która potem z wykorzystniem chata 
 - KPI 
    - zapotrzebowanie z rozmów (kontrola tabeli na koniec spotkania z informacją gdzie są braki)
    - handlowcy pomagają ładować spot
    - w TMS jest dashboard, który pokazuje auta i to co jest zaplanowane dla auta
    - w budowie jest BI (informująy ile zleceń)
    - procent załadowanej naczepy, ilość ładunków w poszczególnych relacjach
    - przychó jest po dacie rozładunku
    - statystyki pokazujące dywersyfikację przychodu per klient i rodzaj klient (bardzo pożądane)
- budowa hurtowni danych (do analizy)
- szkolenie z excel w podstawowej analizy danych w excelu - z wykorzystaniem AI
- warto wprowadzać małe rozwiązania excel i cykliczne spotkanie w celu omówienia 
- bot do wyciągania danych z beef, wyrzucał wszystkie maile do excela i wysłanie spam listy (warto zrobić)
- web scrapper dodatek do przeglądarki do ściągania danych z giełdy
- nauczyć ludzi szykować sobie raport w excelu i jak będzie już dotarty to przenosić do PowerBI
- jaka jest polityka korzystania z BI, co będzie potem po zrobieniu raportu - kluczowa jest polityka ustalenia co robimy po weryfikacji raportu - czyli jak zauważymy jakieś odchylenia to jakie działania mam podjąć
- do rozpatrzenia metabase na własnych zasobach - jeżeli mamy własne zasoby
c - KSeF - do ustalenia czy obsługuje kontrahentów zagranicznych
c - nis2 - do sprawdzenia z prawnikiem czy podlegaja - założenia przychodowe i formy dzialalności
- obsługa klientów jest specyficzna czy moduł tms LTL jest wstanie to obsłuzyć
- nie wiadomo jak przydzila przychody ze zleceń do tras i nie działo to poprawnie - \KPI
- model biznesowy zakłada zbieranie ładunków na magazyn, ładowanie naczepy różnymi zleceniami i wysłykna ma nagazyn w irlandii tam znów magazyn i rozładunek, czy jest jakiś system to obługujący (nie jest to typowa kurierka na własnej flocie, natomiast spedycyjnie robimy wszystko na różnych pojazdach)
- jeżeli model biznesowy różni się od tego co oferuje rynek może zamiast TMS lepiej skupić się na rozwoju modułu zleceń i tras a resztę trzymać w zewnętrznym TMS
- na potrzeby transportu najlepiej byłoby mieć tylko magazyn crossdock natomiast mieć dodatkowo wms
