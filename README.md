# SportRent
## Opis projektu
SportRent to system informatyczny wspomagający zarządzanie wypożyczalnią sprzętu sportowego.

## Cel projektu
Celem systemu jest ułatwienie sprawdzania dostępności sprzętu oraz obsługi wypożyczeń i zwrotów.

## Główne funkcje
- Rejestracja i logowanie użytkowników.
- Przeglądanie dostępnego sprzętu.
- Sprawdzanie dostępności sprzętu.
- Rejestrowanie wypożyczeń i zwrotów.
- Zarządzanie informacjami o sprzęcie.
- Przeglądanie historii wypożyczeń.

## Technologie
- Frontend:  HTML, CSS, JavaScript.
- Backend: Java Spring Boot.
- Baza danych: PostgreSQL.
- Kontrola wersji i współpraca: GitHub.

## Zespół
- Nazar Ostapenko — Koordynator.
- Bohdan Poderiako — Baza danych / Analiza wymagań.
- Kyrylo Skliarov — Backend.
- Andriy Rushchak — Frontend / UI.
- Rostyslav Svistelnytskyi — Testowanie.

## 2. Lista przypadków użycia

| ID | Nazwa przypadku użycia | Aktor główny | Powiązane wymagania | Plik ze scenariuszem |
| :--- | :--- | :--- | :--- | :--- |
| **PU-01** | Przeglądanie katalogu i sprawdzanie dostępności sprzętu | Klient, Pracownik | WF-01, WF-02 | [scenariusze.md](./scenariusze.md#pu-01) |
| **PU-02** | Rezerwacja sprzętu sportowego online | Klient | WF-03, WF-04 | [scenariusze.md](./scenariusze.md#pu-02) |
| **PU-03** | Opłacenie rezerwacji i blokada kaucji | Klient, System płatności | WF-05, WNF-02 | [scenariusze.md](./scenariusze.md#pu-03) |
| **PU-04** | Wydanie sprzętu w punkcie wypożyczalni | Pracownik | WF-06, WF-07 | [scenariusze.md](./scenariusze.md#pu-04) |
| **PU-05** | Zwrot sprzętu, weryfikacja stanu i zwrot kaucji | Pracownik | WF-08, WF-09 | [scenariusze.md](./scenariusze.md#pu-05) |
