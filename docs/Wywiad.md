Wywiad 1 — SportRent

Projekt: System wypożyczalni sprzętu sportowego
Wersja dokumentu: 0.1
Data: do uzupełnienia
Czas trwania: 15 minut
Forma: wywiad krzyżowy — zajęcia 3

1. Uczestnicy
Osoba	Rola w wywiadzie
Nazar Ostapenko	Koordynator / prowadzący rozmowę
Bohdan Poderiako	Analiza wymagań / protokolant
Kyrylo Skliarov	Backend / obserwator wymagań
Andriy Rushchak	Frontend / obserwator
Rostyslav Svistelnytskyi	Testowanie / notowanie pytań
Przedstawiciel wypożyczalni	Klient

Uwaga: należy potwierdzić, kto faktycznie pełnił poszczególne role podczas wywiadu.

2. Cel wywiadu

Celem rozmowy było poznanie potrzeb klientów i pracowników wypożyczalni sprzętu sportowego oraz ustalenie podstawowych zasad działania systemu SportRent.

Podczas wywiadu chcieliśmy dowiedzieć się:

jakie rodzaje sprzętu będą dostępne w systemie;
jak klienci będą sprawdzać dostępność sprzętu;
jak będzie przebiegał proces wypożyczania i zwracania sprzętu;
jakie uprawnienia będą mieli pracownicy i administrator;
jakie problemy mogą występować podczas obsługi wypożyczeń.
3. Ustalenia
Nr	Ustalenie	Status
U-01	System powinien umożliwiać sprawdzanie dostępności sprzętu sportowego.	Do potwierdzenia
U-02	Pracownik powinien mieć możliwość rejestrowania wypożyczeń i zwrotów.	Do potwierdzenia
U-03	Administrator powinien móc dodawać i edytować informacje o sprzęcie.	Do potwierdzenia
U-04	Przy każdym wypożyczeniu należy zapisać datę wypożyczenia i planowany termin zwrotu.	Do potwierdzenia
U-05	System powinien przechowywać informacje o klientach i ich wypożyczeniach.	Do potwierdzenia
U-06	Należy ustalić zasady postępowania w przypadku uszkodzenia lub zagubienia sprzętu.	Wymaga ustalenia
4. Cytaty klienta

Poniższe przykłady należy zastąpić rzeczywistymi wypowiedziami klienta z przeprowadzonego wywiadu.

„Chciałbym wiedzieć, jaki sprzęt jest dostępny przed przyjściem do wypożyczalni”.
„Pracownik powinien szybko sprawdzić, kto wypożyczył dany sprzęt i kiedy ma go zwrócić”.
„Dobrze byłoby otrzymywać przypomnienie o zbliżającym się terminie zwrotu”.
5. Nowe terminy do słownika
Słowo klienta	Znaczenie	Synonim / homonim?	Termin w słowniku
Wypożyczenie	Przekazanie sprzętu klientowi na określony czas.	Nie mylić z rezerwacją.	Wypożyczenie
Zwrot	Oddanie wcześniej wypożyczonego sprzętu do wypożyczalni.	Nie mylić z anulowaniem rezerwacji.	Zwrot sprzętu
Dostępność	Informacja, czy dany egzemplarz sprzętu można aktualnie wypożyczyć.	Nie mylić z samą obecnością sprzętu w magazynie.	Dostępność sprzętu
Rezerwacja	Zgłoszenie chęci wypożyczenia sprzętu w określonym terminie.	Nie mylić z faktycznym wypożyczeniem.	Rezerwacja
Termin zwrotu	Ustalona data, do której klient powinien oddać sprzęt.	Nie mylić z datą wypożyczenia.	Termin zwrotu
6. Zauważone sprzeczności i kwestie do wyjaśnienia
Kwestia	Problem	Jak rozstrzygnąć?
Dostępność sprzętu	Sprzęt może znajdować się w wypożyczalni, ale być już wypożyczony.	Ustalić, jak system ma określać dostępność.
Rezerwacja i wypożyczenie	Klient może zarezerwować sprzęt, ale jeszcze go nie odebrać.	Ustalić, czy system ma obsługiwać rezerwacje.
Uszkodzony sprzęt	Sprzęt może zostać zwrócony w złym stanie i nie nadawać się do kolejnego wypożyczenia.	Ustalić sposób rejestrowania uszkodzeń i zmian dostępności.
7. Otwarte pytania
Nr	Pytanie	Właściciel	Status
Q-01	Czy klient musi posiadać konto, aby wypożyczyć sprzęt?	Nazar Ostapenko	Otwarte
Q-02	Czy system powinien automatycznie naliczać opłaty za opóźniony zwrot?	Bohdan Poderiako	Otwarte
Q-03	Czy klient powinien móc samodzielnie rezerwować sprzęt przez system?	Kyrylo Skliarov	Otwarte
Q-04	Jak należy postępować w przypadku zagubienia lub uszkodzenia sprzętu?	Rostyslav Svistelnytskyi	Otwarte
Q-05	Czy system powinien wysyłać przypomnienia o terminie zwrotu?	Andriy Rushchak	Otwarte
8. Wnioski zespołu
System SportRent powinien ułatwiać sprawdzanie dostępności sprzętu sportowego.
Ważną częścią systemu będzie obsługa wypożyczeń i zwrotów.
Należy określić uprawnienia klientów, pracowników i administratora.
Trzeba ustalić zasady obsługi opóźnionych zwrotów, uszkodzeń i rezerwacji.
Zebrane informacje należy wykorzystać do uzupełnienia słownika dziedzinowego i wymagań systemu.
9. Dalsze działania
Uzupełnić dokument o rzeczywiste odpowiedzi i cytaty klienta.
Zaktualizować słownik w pliku docs/02-slownik.md.
Uzupełnić potrzeby w pliku docs/03-wymagania.md.
Utworzyć Issues dla nierozstrzygniętych pytań.
Przypisać każde zadanie do konkretnego członka zespołu.

Status dokumentu: wersja robocza — do uzupełnienia po przeprowadzeniu wywiadu.
