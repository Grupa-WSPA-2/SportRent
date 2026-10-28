# Słownik SportRent — wersja 0.3
## 1. Cel słownika

Celem słownika jest ujednolicenie terminologii wykorzystywanej podczas analizy wymagań, projektowania, implementacji i testowania systemu SportRent.

## 2. Lista pojęć

| Lp. | Pojęcie | Definicja | Synonimy | Źródło |
|---:|---|---|---|---|
| 1 | SportRent | System informatyczny wspomagający obsługę wypożyczalni sprzętu sportowego. | system wypożyczalni | Opracowanie własne |
| 2 | Sprzęt sportowy | Przedmioty wykorzystywane do uprawiania sportu lub aktywności fizycznej. | wyposażenie sportowe | PWN, opracowanie własne |
| 3 | Wypożyczenie | Udostępnienie sprzętu klientowi na określony czas. | najem, wynajem | PWN, opracowanie własne |
| 4 | Zwrot | Oddanie wcześniej wypożyczonego sprzętu do wypożyczalni. | oddanie sprzętu | Opracowanie własne |
| 5 | Klient | Osoba korzystająca z usług wypożyczalni. | użytkownik wypożyczalni | Opracowanie własne |
| 6 | Pracownik | Osoba obsługująca system i realizująca operacje związane z wypożyczeniami. | operator | Opracowanie własne |
| 7 | Dostępność | Informacja określająca, czy sprzęt może zostać wypożyczony. | status dostępności | Opracowanie własne |
| 8 | Rezerwacja | Zgłoszenie chęci skorzystania ze sprzętu w określonym terminie. | zamówienie terminu | Opracowanie własne |
| 9 | Katalog sprzętu | Zbiór informacji o sprzęcie oferowanym przez wypożyczalnię. | lista sprzętu | Opracowanie własne |
| 10 | Kategoria sprzętu | Grupa, do której przypisany jest sprzęt o podobnym przeznaczeniu. | typ sprzętu | Opracowanie własne |
| 11 | Cena wypożyczenia | Kwota pobierana za korzystanie ze sprzętu przez określony czas. | opłata za wynajem | Opracowanie własne |
| 12 | Termin wypożyczenia | Okres, w którym klient korzysta ze sprzętu. | okres wynajmu | Opracowanie własne |
| 13 | Termin zwrotu | Ustalona data, do której sprzęt powinien zostać oddany. | data oddania | Opracowanie własne |
| 14 | Historia wypożyczeń | Zestawienie wcześniejszych i zakończonych wypożyczeń. | rejestr wypożyczeń | Opracowanie własne |
| 15 | Aktywne wypożyczenie | Wypożyczenie, które nie zostało jeszcze zakończone zwrotem. | bieżące wypożyczenie | Opracowanie własne |
| 16 | Uszkodzenie | Stan, w którym sprzęt jest zniszczony lub nie działa prawidłowo. | wada, defekt | Opracowanie własne |
| 17 | Status sprzętu | Informacja o aktualnym stanie sprzętu, np. dostępny, wypożyczony lub uszkodzony. | stan sprzętu | Opracowanie własne |
| 18 | Baza danych | Uporządkowany zbiór danych przechowywanych i wykorzystywanych przez system. | baza | PWN, opracowanie własne |
| 19 | Rekord | Zestaw powiązanych danych opisujących jeden obiekt. | wpis | Terminologia informatyczna |
| 20 | Formularz | Element interfejsu służący do wprowadzania lub edycji danych. | formularz danych | Terminologia informatyczna |
| 21 | Interfejs użytkownika | Część systemu, za pomocą której użytkownik wykonuje operacje. | UI, ekran aplikacji | Terminologia informatyczna |
| 22 | Wymaganie funkcjonalne | Opis funkcji lub działania, które system powinien realizować. | FR | Materiały z analizy wymagań |
| 23 | Wymaganie niefunkcjonalne | Opis cechy jakościowej lub ograniczenia systemu. | NFR | Materiały z analizy wymagań |
| 24 | Walidacja danych | Sprawdzenie, czy wprowadzone dane spełniają określone reguły. | weryfikacja danych | Terminologia informatyczna |
| 25 | Uprawnienia | Określony zakres operacji, które użytkownik może wykonywać w systemie. | prawa dostępu | Terminologia informatyczna |
| 26 | Administrator | Osoba zarządzająca konfiguracją lub uprawnieniami systemu, jeśli taka rola zostanie przewidziana. | admin | Opracowanie własne |
| 27 | Kaucja | Kwota zabezpieczająca wypożyczalnię na wypadek określonych szkód lub niewywiązania się z warunków wypożyczenia. | depozyt | Opracowanie własne |
| 28 | Raport | Zestawienie danych przedstawiające wybrane informacje z systemu. | zestawienie | Terminologia informatyczna |

## 3. Synonimy

W projekcie należy stosować przede wszystkim pojęcia podstawowe:
- Wypożyczenie — zamiast zamiennego używania słów „najem” i „wynajem” w nazwach funkcji systemu.
- Sprzęt sportowy — zamiast naprzemiennego stosowania określeń „wyposażenie sportowe” i „sprzęt”.
- Zwrot — zamiast określenia „oddanie sprzętu” w nazwach operacji.
- Termin zwrotu — zamiast „daty oddania”, gdy chodzi o planowany termin.
- Historia wypożyczeń — zamiast „rejestru wypożyczeń” w interfejsie użytkownika.
- Status sprzętu — zamiast „stanu sprzętu” w polach systemowych.

Synonimy ułatwiają zrozumienie dokumentacji, ale w interfejsie i wymaganiach należy konsekwentnie stosować wybrane nazwy.

## 4. Homonimy i pojęcia wieloznaczne

| Pojęcie | Możliwe znaczenia | Znaczenie w projekcie SportRent |
|---|---|---|
| Karta | Karta płatnicza, karta dokumentu, karta produktu | Widok szczegółowych informacji o sprzęcie, jeśli taki element zostanie zastosowany |
| Model | Model matematyczny, model danych, model produktu | Wariant lub typ sprzętu albo model danych — zależnie od kontekstu |
| Rekord | Nagranie muzyczne, wynik sportowy, wpis w bazie danych | Wpis przechowujący dane o sprzęcie, kliencie lub wypożyczeniu |
| Status | Stan sprawy, status przesyłki, status obiektu w systemie | Aktualny stan sprzętu lub wypożyczenia |
| Klient | Osoba kupująca usługę, klient programu komputerowego | Osoba korzystająca z wypożyczalni |
| Baza | Podstawa czegoś, obiekt wojskowy, baza danych | Baza danych systemu SportRent |


## 5. Źródła

- PWN — Wielki słownik języka polskiego PWN: https://wsjp.pl/
- Terminologia informatyczna — dokumentacja i materiały dydaktyczne dotyczące analizy wymagań oraz systemów informatycznych.
- Opracowanie własne — definicje przygotowane przez zespół na potrzeby projektu SportRent.
- Materiały projektowe — karta projektu, wywiad z klientem i dokumentacja wymagań SportRent.
