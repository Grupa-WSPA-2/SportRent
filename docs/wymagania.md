Wymagania — SportRent
Potrzeby
ID	Potrzeba	Źródło	Typ	Kto zgłasza
N-01	Klient chce sprawdzić dostępność sprzętu przed wypożyczeniem.	Założenie zespołu — do potwierdzenia w wywiadzie	potrzeba	Klient
N-02	Pracownik chce szybko rejestrować wypożyczenia i zwroty.	Założenie zespołu — do potwierdzenia w wywiadzie	potrzeba	Pracownik
N-03	Administrator chce aktualizować informacje o sprzęcie.	Założenie zespołu — do potwierdzenia w wywiadzie	potrzeba	Administrator
N-04	System nie powinien pozwalać na jednoczesne wypożyczenie tego samego egzemplarza dwóm klientom.	Założenie zespołu — do potwierdzenia w wywiadzie	żądanie	Pracownik
N-05	Pracownik chce sprawdzać historię wypożyczeń.	Założenie zespołu — do potwierdzenia w wywiadzie	potrzeba	Pracownik
N-06	Administrator chce ograniczyć dostęp do funkcji zgodnie z rolą użytkownika.	Założenie zespołu — do potwierdzenia w wywiadzie	potrzeba	Administrator
Wymagania funkcjonalne (wstępne)
ID	Wymaganie	Potrzeba
FR-01	System umożliwia klientowi przeglądanie katalogu sprzętu sportowego.	N-01
FR-02	System umożliwia klientowi wyszukiwanie sprzętu według nazwy.	N-01
FR-03	System umożliwia klientowi filtrowanie sprzętu według kategorii.	N-01
FR-04	System umożliwia klientowi sprawdzenie dostępności wybranego egzemplarza sprzętu.	N-01
FR-05	System umożliwia pracownikowi rejestrowanie nowego wypożyczenia.	N-02
FR-06	System umożliwia pracownikowi rejestrowanie zwrotu sprzętu.	N-02
FR-07	System umożliwia pracownikowi przeglądanie aktywnych wypożyczeń.	N-02
FR-08	System umożliwia pracownikowi sprawdzenie terminu zwrotu sprzętu.	N-02
FR-09	System umożliwia administratorowi dodawanie nowych egzemplarzy sprzętu.	N-03
FR-10	System umożliwia administratorowi edytowanie informacji o sprzęcie.	N-03
FR-11	System umożliwia administratorowi zmianę statusu sprzętu.	N-03
FR-12	System uniemożliwia utworzenie nakładających się wypożyczeń tego samego egzemplarza.	N-04
FR-13	System umożliwia pracownikowi przeglądanie historii wypożyczeń.	N-05
FR-14	System umożliwia administratorowi tworzenie i dezaktywowanie kont użytkowników.	N-06
FR-15	System umożliwia administratorowi przypisywanie ról i uprawnień użytkownikom.	N-06
Wymagania niefunkcjonalne (wstępne)
ID	Kategoria	Wymaganie	Potrzeba
NFR-01	Wydajność	Dla katalogu zawierającego do 10 000 egzemplarzy 95% zapytań o listę sprzętu powinno być obsłużonych w czasie do 2 sekund w uzgodnionym środowisku testowym.	N-01
NFR-02	Wydajność	Sprawdzenie dostępności pojedynczego egzemplarza powinno trwać nie dłużej niż 2 sekundy dla 95% zapytań w środowisku testowym.	N-01
NFR-03	Użyteczność	Nowy pracownik powinien być w stanie zarejestrować wypożyczenie w ciągu maksymalnie 2 minut po krótkim szkoleniu.	N-02
NFR-04	Niezawodność	Po zapisaniu wypożyczenia system powinien zachować dane po ponownym uruchomieniu aplikacji.	N-02
NFR-05	Spójność danych	System powinien odrzucić próbę utworzenia dwóch nakładających się wypożyczeń tego samego egzemplarza, także przy równoczesnych żądaniach.	N-04
NFR-06	Bezpieczeństwo	Każda operacja wymagająca uprawnień administratora powinna być niedostępna dla użytkownika bez tej roli.	N-06
NFR-07	Bezpieczeństwo	Hasła użytkowników powinny być przechowywane w postaci bezpiecznych skrótów kryptograficznych, a nie jako zwykły tekst.	N-06
NFR-08	Utrzymywalność	Kod powinien być podzielony na moduły, a podstawowe operacje biznesowe powinny mieć testy automatyczne.	N-02
Uwagi
Wymagania są wstępne i wymagają weryfikacji z klientem.
Wartości liczbowe w wymaganiach niefunkcjonalnych są propozycjami do uzgodnienia.
Każde wymaganie jest powiązane z co najmniej jedną potrzebą.
Po wywiadzie należy zaktualizować źródła potrzeb i ustalić priorytety wymagań.
