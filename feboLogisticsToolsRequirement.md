## Specyfikacja narzędzi

# CRM
w - konieczna organizacja w CRM kalendarza spotkań widoczny dla innych użytkowników
w - każde spotkanie z klientem powinno mieć notatkę, która potem z wykorzystniem chata 

# TMS
w - TMS - wdrożenie systemu zewnętrznego wymaga jego ciągłego utrzymywania i aktualziacji aby miało to sens
w - czy można przez API ściągnąć dane z dashboard - ściągać i udostępniać
w - dane w  dashboard można ściągnąć do excel i z pomocą poverQuery zrobić jakiś widok dla planistów w google sheets
w - trzeba byłoby dodać kilka informacji w dashbord - czy do planowania do irlandii czy nie (zarządzanie priorytetami)
w - najlepiej jakby zweryfikowan cmr wysyłany był do klienta automatycznie, 
w - czy są jakieś dedykowane narzędzia do crossdocingu (interLNA)
w - zlecenia nie są wprowadzane do systemu dopóki nie znajdą przewoźnika na nie konieczne jest maksymalne ułatwienie wprowadzania zleceń w celu ułatwienia dzielenia się informacją o zleceniu i szukania przewoźnika - minimalizacja progu wejścia i zlecenia wstępne
w - przydałby się panel do zarządzania przewoźnikami i kierowcami (wyjazdy, terminy itp.)
w - przydałby się status odprawy celnej w TMS
w - przydałby się moduł rozliczenia kierowców w TMS
w - integracja z Optima
w - tms nie ma instancji testowej 
w - obsługa klientów jest specyficzna czy moduł tms LTL jest wstanie to obsłuzyć
w - model biznesowy zakłada zbieranie ładunków na magazyn, ładowanie naczepy różnymi zleceniami i wysłykna ma nagazyn w irlandii tam znów magazyn i rozładunek, czy jest jakiś system to obługujący (nie jest to typowa kurierka na własnej flocie, natomiast spedycyjnie robimy wszystko na różnych pojazdach)
w - jeżeli model biznesowy różni się od tego co oferuje rynek może zamiast TMS lepiej skupić się na rozwoju modułu zleceń i tras a resztę trzymać w zewnętrznym TMS
w - na potrzeby transportu najlepiej byłoby mieć tylko magazyn crossdock natomiast mieć dodatkowo wms
w - jak odchudzić bieżący TMS i skupić się na kluczowej kwesti a w pozostałych wykorzystywać zewnętrzny TMS - strategia powolnego wyjścia z TMS
w - może wziąć z InterLAN albo z innego TMS moduł bazowy (zlecenia, kierowcy, fv, itp.) a w LogTMS zostawić łączenie zleceń w trasy i obsługę cross dokingu

# aplikacja typu AI RAG do wyceny zleceń 
w - rozpoznać możliwość liczenia km z wykorzystanie API Here
w - spedytorzy mają inne modele wyceniania, nie ma polityki cenowej, brak informacji planisty o spotkaniu z klientem jakieś notatki po spotkaniu, które powinny być podsumowanie w RAG

# n8n / CRON
w - tracking wysyłany mailem - może automat AI odpowiadający o na status zlecenia na podstawie danych w TMS ale ich nie ma
w - agentów AI do uzupełniania danych na stronach rządowych w zakresie odprawy celnej np. GMR ()
w - czy można zrobić jakoś tanio RPA do GMR, ewentuaknie do sprawdzenia czy HMRC ma api i obsługa przez n8n
w - jest strona do sprawdzenia czy tranzyt jest zaknięty (można sprawdzić na stronie ec.europa), przyadałobby się narzędzie, które sprawdza zamknięcie tranzytu
w - czy armatorzy promowi mają jakieś możliwości do generowanie GMR przy bookingu promu, w calais jest bookowanie na podstawie nr rej, więc totalnie automat
w - jak połączyć wykupienie promu z wyrobieniem GMR
w - spalanie powyżej 26l na czerowo i analiza - p -xrośba do kierowcy o informacje na temat spalan do automatyzacji
w - bot do wyciągania danych z beef, wyrzucał wszystkie maile do excela i wysłanie spam listy (warto zrobić)

# Zekju/Slickshift
w - do weryfikacji czy Zekju udźwignie dzielenie się komunikacją w celu obsługi nocnej i dziennej zmiany
w - przygotować export zlecenia z TMS, który można zaciągnąć do Zekju zamiast integracji
w - przydałoby się zrobić CMR Matcher - do weryfikacji z możliwościami Zekju
w - chcielibyśmy zrobić rozliczenie wydatków w aplikacji dla kierowców czy pozwala na to Zekju
w - nie ma narzędzie dla dyspozytora, do obserwowania swoich aut w trasie - do sprawdzenia Zekju, Slickshift (mail od Daniela) i inni dostawcy

# WMS
w - planiści powinni zarządzać przestrzenią cross dokingu
w - warto rozpatrzeć inwestycję w lepszy system magazynowy z możliwością skalowania na inne obiekty, corss dokingu i integracją z TMS (zamiast rozwijać własne narzędzie)
w - qr kody na regałach i miejscach magazynowych tak aby można było zarządzać przestrzenią + do sprawdzenia jakie są nejlepsze praktyki zarządzania crossdokingiem bo nie ma sensu oznaczanie każdej palety za 20 np, tylko pierwszą i oznaczyć jako paczka 20
w - konieczne jest zarządzanie rożnymi magazynami i to w innych krajach
w - zarządzanie siecia magazynów i przejazdami w przyszłości

# Manifest celny 
w - platforma custran.com miesięczna subsktrypca (ENS, i T2) - CZY MA API / czy można robić draft przez API i potwierdzać go przez agenta
w - doprowadzić do tego aby dane z maila (spedytorzy wysyłają formatkę manifest) - do weryfikacji czy wszystkie informacje są w TMS nie
w - custran ma bazę danych nadawców i odbiorców z wprowadzonych T2 (dane dla commercial) jest eksport do excel jak je zmapować z bazą danych w TMS

# asystent AI do wyznaczania kodów celnych
do której można pisać w języku naturalnym RAF + lista towarów, które najczęściej jeżdżą (notebookLM) - może warto zrobić notebookLM podpięty pod stronę - z wyszukiwarką kodów + wytyczne wykonania + zapisywanie zapytań i rejestrowanie

# KSeF
w - możliwa integracja z Saldeo w celu obsługi procesu FV (kosztowe Ksef jak i inne) 
w - saldeo ma specjalna wtyczkę w Optima przez co integracja nie wymaga dodaktowych kosztów
w - saldeo ma API przez co może służyć jako alternatywa do API optima

# wyszukiwanie nowych klientów
w - bazy kontaktów osób zajmujących się konkretną dziedziną w jakiejś firmie 
w - główne źródło to linked in czy jesty możliwość korzystania z chata żeby sprawdzić kto jest tam za co odpowiedzialny
w - dostęp do bazy linked in przez AI (żeby poztyskać konkretny kontakt)
w - wyszukiwanie klientów głównie na podstawie danych historycznych, na podstawie bazy danych z systemu (jak wyciagać takie dane - kilkukrotnie powtórzony spot powinien mieć proponowany kontakt)
w - baza danych producentów konkretnych porduktów średniej wielkości przedsiębiorst do np do 30mln przychodów - raczej melodia przyszłosci nie musi być od razu
w - szkolenie AI (perplexity, tworzenie asystentów AI)

# goodloading dla doubledeck 
w -wrzucasz w program ilość palet i rozmarach i pokazuje jak to rozłożyć (pomysł na aplikację zewnętrzną) - wykorzystanie do podwójnych podłóg - google AI (oprzeć się na flocie Febo) - narzędzie dla planistów
w - fajnie byłoby to połączyć w systemie (czy obsłuży to TMS) - pozyskać informację z TMS
w - jak łączyć zlecenia ze sobą w narzędziu planistycznym (znaczenie ma waga, kolejność rozładunku, wymiar, podlłoga ma cztery sekcje, na każdej sekcji można zrobic inny podział - ładunki non stack)

# hurtownia danych
w - KPI   - procent załadowanej naczepy, ilość ładunków w poszczególnych relacjach
w - KPI   - przychód jest po dacie rozładunku
w - KPI   - statystyki pokazujące dywersyfikację przychodu per klient i rodzaj klient (bardzo pożądane)
w - szkolenie z excel w podstawowej analizy danych w excelu - z wykorzystaniem AI
w - warto wprowadzać małe rozwiązania excel i cykliczne spotkanie w celu omówienia 
w - nauczyć ludzi szykować sobie raport w excelu i jak będzie już dotarty to przenosić do PowerBI
w - jaka jest polityka korzystania z BI, co będzie potem po zrobieniu raportu - kluczowa jest polityka ustalenia co robimy po weryfikacji raportu - czyli jak zauważymy jakieś odchylenia to jakie działania mam podjąć
w - nie wiadomo jak przydzila przychody ze zleceń do tras i nie działo to poprawnie - \KPI